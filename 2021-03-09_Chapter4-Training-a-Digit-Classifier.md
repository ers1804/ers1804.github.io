How is a grayscale image represented on a computer? How about a color image?
A grayscale image is represented by an array of numbers. Each number corresponds to a shade of gray with 0 being white and 255 being black.

How are the files and folders in the MNIST_SAMPLE dataset structured? Why?
The files are structured into training and validation data. The data in the training folder is also separated into folders containing data with the same label. This makes training the model and handling the data much easier.

Explain how the “pixel similarity” approach to classifying digits works.
We take the mean of each pixel for every digit and compare a new image to see which image it is the closest to.

What is a list comprehension? Create one now that selects odd numbers from a list and doubles them.
List comprehension saves time and computing power by combining for-loops with accessing the elements of a list.
`list = [x for x in a_list if x%2 != 0]` 

What is a rank-3 tensor?
A three-dimensional tensor.

What is the difference between tensor rank and shape? How do you get the rank from the shape?
The shape describes the length of each axis of the tensor. The rank is the length of the tensor's shape, i.e. a shape of [6131, 28, 28] has rank 3.

What are RMSE and L1 norm?
L1-norm is the mean of the absolute differences of two points. RMSE is the root of the mean of the squared differences between two points.

How can you apply a calculation on thousands of numbers at once, many thousands of times faster than a Python loop?
Using array/tensor-calculations from NumPy or PyTorch. Pytorch tensors can live on the GPU, which makes computations with them even faster.

Create a 3×3 tensor or array containing the numbers from 1 to 9. Double it. Select the bottom-right four numbers.
`tns = tensor([[1,2,3],[4,5,6],[7,8,9]])
tns = tns*2
tns[1:2,1:2]`

What is broadcasting?
PyTorch automatically recognizes, when two tensors have different shapes or sizes and broadcasts the size of the smaller one to that of the larger one. E.g. [1028, 28, 28] and [28,28].

Are metrics generally calculated using the training set or the validation set? Why?
A metridc is calculated on the validation set, because it tells us how good the predictions are. This also prevents overfitting.

What is SGD?
Stochastic gradient descent. Gradient Descent that does not use the complete training set to calculate the update for the weights.

Why does SGD use mini-batches?
Because using only one sample would not yield a stable gradient. Using all samples in the training set would be computationally too expensive. Using a subset of the fullset to update gives us a stable gradient and saves computation power.

What are the seven steps in SGD for machine learning?
1. Initialize the parameters.
2. Calculate the predictions.
3. Calculate the loss.
4. Calculate the gradients.
5. Step the weights.
6. Repeat the process.
7. Stop.

How do we initialize the weights in a model?
We randomly initialize them.

What is loss?
Loss is the mistake that we make during predictions.

Why can’t we always use a high learning rate?
Because SGD might not converge.

What is a gradient?
It's the derivative of a function. In the case of machine learning we usually talk about a gradient at a certain position.

Do you need to know how to calculate gradients yourself?
No.

Why can’t we use accuracy as a loss function?
Because the accuracy only changes if we change the classification of one sample. Thus it wouldn't register smaller changes to the weights and the outcome. For the loss function we need a differentiable function.

Draw the sigmoid function. What is special about its shape?
S-shape. It only assigns values between 0 and 1.

What is the difference between a loss function and a metric?
A metric is to drive human understanding and a loss function is to drive machine learning.

What is the function to calculate new weights using a learning rate?
weights = weights - gradient * tau

What does the DataLoader class do?
Dataloaders return an iterator over as many batches of the data as we want. It also can shuffle the pairs.

Write pseudocode showing the basic steps taken in each epoch for SGD.
for xb, yb in data:
      pred = model(xb)
      loss = loss(xb,yb)
      loss.backward()
      for p in params:
          p -= p.grad()* learning_rate
      p.grad.zero_()

Create a function that, if passed two arguments [1,2,3,4] and 'abcd', returns [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd')]. What is special about that output data structure?
def function(numbers, string):
    list = [(x,y) for x,y in numbers, string]
    return list

What does view do in PyTorch?
Returns a tensor with the same data but of a different shape.

What are the bias parameters in a neural network? Why do we need them?
The bias parameters are the b in the following equation: y = Wx+b We need them so we don't have as many 0s, since most pixels in the picture are white and thus 0.

What does the @ operator do in Python?
Matrix multiplication.

What does the backward method do?
It calculates the gradients of the function.

Why do we have to zero the gradients?
Because calculating gradients is an inplace operation, this means that the previous result is always saved and the new result is added to it.

What information do we have to pass to Learner?
Dataloaders, the model, the optimization function, the loss function and optionally any metrics to print

Show Python or pseudocode for the basic steps of a training loop.
def train_epoch(model):
    for xb,yb in dl:
        calc_grad(xb, yb, model)
        opt.step()
        opt.zero_grad()

What is ReLU? Draw a plot of it for values from -2 to +2.
It is a function that gives the input value if it is >= 0 or gives 0 if that is not the case.

What is an activation function?
A non-linearity between linear layers of the neural network.

What’s the difference between F.relu and nn.ReLU?
nn.ReLU is a model that can be used in nn.Sequential. F.relu just calls the Relu function.

The universal approximation theorem shows that any function can be approximated as closely as needed using just one nonlinearity. So why do we normally use more?
To reduce the number of parameters needed to get good accuracy.

Further Research
Create your own implementation of Learner from scratch, based on the training loop shown in this chapter.

Complete all the steps in this chapter using the full MNIST datasets (for all digits, not just 3s and 7s). This is a significant project and will take you quite a bit of time to complete! You’ll need to do some of your own research to figure out how to overcome obstacles you’ll meet on the way.
