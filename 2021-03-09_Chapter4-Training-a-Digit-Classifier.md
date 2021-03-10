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

Why does SGD use mini-batches?

What are the seven steps in SGD for machine learning?

How do we initialize the weights in a model?

What is loss?

Why can’t we always use a high learning rate?

What is a gradient?

Do you need to know how to calculate gradients yourself?

Why can’t we use accuracy as a loss function?

Draw the sigmoid function. What is special about its shape?

What is the difference between a loss function and a metric?

What is the function to calculate new weights using a learning rate?

What does the DataLoader class do?

Write pseudocode showing the basic steps taken in each epoch for SGD.

Create a function that, if passed two arguments [1,2,3,4] and 'abcd', returns [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd')]. What is special about that output data structure?

What does view do in PyTorch?

What are the bias parameters in a neural network? Why do we need them?

What does the @ operator do in Python?

What does the backward method do?

Why do we have to zero the gradients?

What information do we have to pass to Learner?

Show Python or pseudocode for the basic steps of a training loop.

What is ReLU? Draw a plot of it for values from -2 to +2.

What is an activation function?

What’s the difference between F.relu and nn.ReLU?

The universal approximation theorem shows that any function can be approximated as closely as needed using just one nonlinearity. So why do we normally use more?

Further Research
Create your own implementation of Learner from scratch, based on the training loop shown in this chapter.

Complete all the steps in this chapter using the full MNIST datasets (for all digits, not just 3s and 7s). This is a significant project and will take you quite a bit of time to complete! You’ll need to do some of your own research to figure out how to overcome obstacles you’ll meet on the way.
