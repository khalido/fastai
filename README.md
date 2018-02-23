Notes for fast.ai's [deep learning course, part 1, 2018 edition](http://course.fast.ai/).

- [Notes for the 2018 course](https://github.com/reshamas/fastai_deeplearn_part1)
- [fast.ai forums](http://forums.fast.ai/), [Part 1, 2018 forums](http://forums.fast.ai/c/part1-v2)

# Lesson 1: Cats & Dogs

[Lesson 1](http://course.fast.ai/lessons/lesson1.html), [wiki](http://forums.fast.ai/t/wiki-lesson-1/9398)

- why fast.ai?
  - fastai is top down, starts with code which does stuff, then slowly peels it back.
  - recommends getting to the end of all lessons then going through again as many times as needed to spend more time on things missed, rather than going slow.
  - so first up, setup a gpu machine to run code on:

- [Paperspace](https://github.com/reshamas/fastai_deeplearn_part1/blob/master/tools/paperspace.md)
- Amazon EC2 - use [AWS Deep Learning AMI (Ubuntu)](https://aws.amazon.com/marketplace/pp/B077GCH38C)
- [Google Cloud](https://medium.com/@howkhang/ultimate-guide-to-setting-up-a-google-cloud-machine-for-fast-ai-version-2-f374208be43)
[](https://github.com/reshamas/fastai_deeplearn_part1)- [Reshma has brilliant setup notes](https://github.com/reshamas/fastai_deeplearn_part1).
[](https://medium.com/@howkhang/ultimate-guide-to-setting-up-a-google-cloud-machine-for-fast-ai-version-2-f374208be43)

Once setup, update the OS and fastai repo:

```
# update the machine OS
sudo apt update
sudo apt upgrade
# make sure the fastai git  repo is up to date
git pull # run this inside the fastai folder
conda env update # updates the fastai env
conda activate fastai # activates fastai env
```

Use JupyterLab:

`conda install -c conda-forge jupyterlab # install jupyterlab`


- first up, we learn how to classify images, with both single and multi-label ones.
- stochastic gradient descent with restarts (SGDR) lowers the learning rate as the model learns, with periodic ‘jumps’ to ensure it doesn’t get stuck in a local minima


