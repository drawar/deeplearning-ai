# Coursera deeplearning.ai - Deep Learning Specialization - Neural Networks and Deep Learning

This document contains a guide to help you to start experimenting with [Coursera deeplearning.ai](https://www.coursera.org/specializations/deep-learning) specialization assignments **as easily as possible** through a Jupyter notebook running on [FloydHub](https://www.floydhub.com/).

The code in this project was ported from the [official course](https://www.coursera.org/learn/neural-networks-deep-learning), but only the necessary files to run this specific project were selected. The data used in this project is already available as a FloydHub dataset.

You can find the video lectures about Neural Network and Deep Learning  specialization on [Deeplearning.ai's official youtube channel](https://www.youtube.com/watch?v=CS4cs9xVecg&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0).

## Assignment 5: Deep Neural Network - Application.

Congratulations! Welcome to the fourth programming exercise of the deep learning specialization. You will now use everything you have learned to build a deep neural network that classifies *cat vs. non-cat images*.

## Run on FloydHub

Follow the next steps to get a jupyter notebook up and running for Assignment 5.

### 1. Create a FloydHub account

- [Sign up](https://www.floydhub.com/signup) on FloydHub
- Install the floyd CLI on your local machine through these two [steps](https://www.floydhub.com/welcome):

```bash
$ pip install -U floyd-cli

$ floyd login
# Follow the instructions on your CLI
```

### 2. Clone this project to your local machine

```bash
$ cd /path/to/your-project-dir
$ floyd clone deeplearningai/projects/deep-neural-network-application/2
```

### 3. Create your project version on FloydHub

[Create a project](https://www.floydhub.com/projects/create) on FloydHub and then sync the cloned repository with your new project:

```bash
$ floyd init your-project-name
```

### 4. Run the project through a jupyter notebook

- The `--mode` flag specifies that this job should provide us a Jupyter notebook
- The `--data` flag specifies that the cat-vs-noncat dataset should be available at the `/datasets` directory
- The `--env` flag specifies the environment that this project should run on, which is a Tensorflow 1.1.0 + Keras 2.0.6 backend environment with Python 3.5. Even if this is a basic tutorial that can run on every FloydHub environments, we suggest you to always specify an environment, this minimize all the reproducibility issue.

```bash
floyd run \
    --mode jupyter \
    --data deeplearningai/datasets/cat-vs-noncat/1:datasets \
    --env tensorflow-1.1
```

Once the job is started, the jupyter notebook will open in your browser and you are ready to go!

## More about FloydHub platform

- Note that changes you make to the notebook running on Floyd servers are not going to be saved at your local directory, but they are going to be available in the [output](https://www.floydhub.com/deeplearningai/projects/deep-neural-network-application/2/output) section of your job.
- Once you stop the Jupyter notebook job you were running, from the job page, you can click on [Restart](http://blog.floydhub.com/restart-jupyter-notebook-workflow/?utm_medium=email&utm_source=21sep17) to restart your job exactly how you left it and optionally choosing another environment (CPU or GPU). This is a great way to spend less of your GPU hours if you are working on tasks that does not require a GPU.
- If you need any help check our [documentation](http://docs.floydhub.com/) and [forum](https://forum.floydhub.com/).

