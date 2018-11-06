Notes for fast.ai's [deep learning course, part 1, v3](http://course.fast.ai/), which teaches deep learning using the [fastai library built on top of pytorch](https://www.fast.ai/2018/10/02/fastai-ai/).

- [Notes for the 2018 course](https://github.com/reshamas/fastai_deeplearn_part1)
- [fast.ai forums](http://forums.fast.ai/), [Part 1, v3 forums](http://forums.fast.ai)

# Setup

- I tried [crestle.ai] which is super simple to use, but its slow and buggy for now
- went with setting up a [p2.xlarge](https://aws.amazon.com/ec2/instance-types/p2/) server on AWS using their [deep learning ami](https://aws.amazon.com/machine-learning/amis/)
- make sure to periodically update the fastai libraries
- login to the server by`ssh -L localhost:8888:localhost:8888 ubuntu@<your instance IP>`
- make sure the fastai git  repo is up to date
`git pull # run this inside the fastai course folder`

# Lesson 1: Cats & Dogs

[Lesson 1](http://course.fast.ai/lessons/lesson1.html), [wiki](http://forums.fast.ai/t/wiki-lesson-1/9398)

- why fast.ai?
  - fastai is top down, starts with code which does stuff, then slowly peels it back.
  - recommends getting to the end of all lessons then going through again as many times as needed to spend more time on things missed, rather than going slow.


- [Lesson 1: Image classification with Convolutional Neural Networks](https://github.com/fastai/fastai/blob/master/courses/dl1/lesson1.ipynb)
  - first up, we learn how to classify images, with both single and multi-label ones.
  - stochastic gradient descent with restarts (SGDR) lowers the learning rate as the model learns, with periodic ‘jumps’ to ensure it doesn’t get stuck in a local minima
  - the fast.ai library has a `lr.find()` method to help find an optimal learning rate. This starts at a very low lr and keeps increasing it until the loss stops decreasing.
  - augment data with the `tfms_from_model()` method, with the transformations to perform passed in with `aug_tfms=`
  - homework: recreate my own versions of the fastai notebooks
- note: the fastai library is frequently updated so `git pull` it from github instead of installing it using pip. to use the fastai library in my own github repo,create a symlink from the folder containing jupyter notebooks to the library like so `ln -s /path/to/fastai/fastai` and import things as per the fastai notebooks.


