# Data Ethics

- Does ethics provide a list of “right answers”?
  - No, it does not. It is way more complicated than that. It also changes in what context you talk about it. There can't be a universal list of rights and wrongs, that can be applied to any question in any field. Maybe one can think of ethics like a new sense, which can be practiced to lead you in the right direction. Or rather directions. When typing "data ethics" into Wikipedia, you'll end up with the following definition: "Big data ethics also known as simply data ethics refers to systemizing, defending, and recommending concepts of right and wrong conduct in relation to data, in particular personal data."

- How can working with people of different backgrounds help when considering ethical questions?
  - You'll have many different perspectives on the problem at hand. Most importantly some perspectives that are completely new to you or that are not obvious to you at first glance.

- What was the role of IBM in Nazi Germany? Why did the company participate as it did? Why did the workers participate?
  - They supplied Nazi Germany with machinery helping them categorize people into different groups with different ways to be killed. Everyone in the company was "just doing their job" soley focused on the technology side or sales side of the job and not caring about how their inventions/technology were/was used. This teaches us to **always** think about what our inventions, algorithms or ideas can be used for. And we as creators have to take measures to make sure that they can only be used as intended or at least in the most positive way.

- What was the role of the first person jailed in the Volkswagen diesel scandal?
  - He was an engineer working on the project.

- What was the problem with a database of suspected gang members maintained by California law enforcement officials?
  - There were babies in the database that were added to it when they were less than 1 year old. The process didn't have the option to remove entries from the database once they were added to it.

- Why did YouTube’s recommendation algorithm recommend videos of partially clothed children to pedophiles, even though no employee at Google had programmed this feature?
  - The base for YouTube's algorithm is reinforcement learning, whose performance measure is watch time. This means that the algorithm recommends videos to you similiar to the ones you've already watched.

- What are the problems with the centrality of metrics?
  - The algorithm has a metric to optimize (in YouTube's case it's watch time) and this will lead to all kinds of different edge cases, which can be exploited by humans interacting with the system. This can cause the above described feedback loops.

- Why did Meetup.com not include gender in its recommendation system for tech meetups?
  - Men expressed more interest in tech meetups than women. Using this data to train a ML algorithm would cause the algorithm to recommend these meetups to a predominantly male audience, which would lead to even fewer women attending the meetups. By now we would already have been in a feedback loop that excludes women from these meetings.

- What are the six types of bias in machine learning, according to Suresh and Guttag?
  - Historical bias: People, processes and society are biased. And this leads to the first problem in data generation. The data can be biased even with perfect sampling and feature selection because the underlying data is already biased. This leads to a very hard to solve problem, since we can't fix it by only changing the algorithm or the model that we are using.
  - representation bias: Occupation prediction algorithms not only reflect the gender imbalances in certain occupations but amplify it. The model recognizes this relationsship between these features and assumes that this relationsship always holds.
  - measurement bias: Models measure either the wrong thing, in the wrong way or incorporate measurements in the wrong way into the prediction. For example are likely (or you can afford it) to got to the doctor for minor, accidental injuries you are also likely to go to the doctor when having a stroke. This causes a correlation, which (in most cases) does not have causal connection. However, this correlation leads to the algorithm to pick it up and include it in its prediction.
  - evaluation bias
  - aggregation bias: Aggregation bias can in my opinion be seen as almost the opposite of measurement bias. Here the model does not factor in important variables, nonlinearities or anything similar, which can result in wrong predictions or recommendations.
  - deployment bias

- Give two examples of historical race bias in the US.
  - Google classifiying a picture of a black user as a gorilla
  - parole algorithm is more likely to give a white person parole than a black person

- Where are most images in ImageNet from?
  - Europe and U.S.

- In the paper “Does Machine Learning Automate Moral Hazard and Error?” why is sinusitis found to be predictive of a stroke?
  - Because the model found the correlation of people being able to afford to go to the doctor for a sinusitis and a stroke. Someone, who goes to the doctor for a sinusitis is also likely to go to the doctor for a stroke.

- What is representation bias?
  - see question about biases

- How are machines and people different, in terms of their use for making decisions?
  - Machines are usually used in a plug-and-play fashion for making decisions: Train the model on the training data and afterwards deploy the algorithm into the real world.
  - Algorithms are generally thought of to be objective and bias-free, which is not the case.

- Is disinformation the same as “fake news”?
  - No, while fake news is completely false, disinformation always contains a tiny bit of truth, half-truths and exaggerations.

- Why is disinformation through autogenerated text a particularly significant issue?
  - Because most people are radicalized in an online environment because we are mostly influenced by the people around us. Using autogeneratred text in an online forum with people already leaning in the "alternate facts" direction it is easy to further push these people into a feedback loop as mentioned above a couple of times. Also this topics opens the discussion about AI-generated forgery (e.g. important government documents or similiar).

- What are the five ethical lenses described by the Markkula Center?
  - The rights approach: Which option best respects the rights of all who have a stake?
  - The justice approach: Which option treats people equally or proportionately?
  - The utilitarian approach: Which option will produce the most good and do the least harm?
  - The common good approach: Which option best serves the community as a whole, not just some members?
  - The virtue approach: Which option leads me to act as the sort of person I want to be?

- Where is policy an appropriate tool for addressing data ethics issues?
  - When the underlying profit incentives have to be changed. E.g. when developing addictive technology.

## Further Research
- Read the article “What Happens When an Algorithm Cuts Your Healthcare”. How could problems like this be avoided in the future?

- Research to find out more about YouTube’s recommendation system and its societal impacts. Do you think recommendation systems must always have feedback loops with negative results? What approaches could Google take to avoid them? What about the government?

- Read the paper “Discrimination in Online Ad Delivery”. Do you think Google should be considered responsible for what happened to Dr. Sweeney? What would be an appropriate response?

- How can a cross-disciplinary team help avoid negative consequences?

- Read the paper “Does Machine Learning Automate Moral Hazard and Error?” What actions do you think should be taken to deal with the issues identified in this paper?

- Read the article “How Will We Prevent AI-Based Forgery?” Do you think Etzioni’s proposed approach could work? Why?

- Complete the section “Analyze a Project You Are Working On”.

- Consider whether your team could be more diverse. If so, what approaches might help?
