# Intro-To-DSP-With-NVIDIA-RAPIDS
This is an introductory notebook to Digital Signal Processing(DSP) using CuSignal and other NVIDIA RAPIDS open-source API. This notebook is still a work in progress and will constantly be updated as time goes on !!!

For the GPU notebook, all the codes were run on paperspace(cloud based platform to access RAPIDS API) since I do not have an NVIDIA GPU locally. I used a Free-P5000 GPU with 30 GB RAM and 8 CPUs

For the CPU notebook, I used an Apple macbook pro.

## Introduction

You are wondering how technology companies manage to make amazing audio systems with clean and clear sounds, well here is the foundation. Thankfully python has become the go-to language for getting started with programing, engineers are also taking advantage of the language for more advance uses. You can learn more about getting started with python [here](https://www.learnpython.org/). 

The main objective of this discussion is to apply basic DSP concepts to see how can we filter out noise from a music or audio recording. There are several applications and APIs that already do this with just function calls, but the aim of this discussion is to apply the basic concepts and introduce students or enthusiasts to DSP using a real world example and how things come together. There are obviously more efficient ways to go about this but that is not our aim for now. Future discussions will involve using machine learning to automatically detect noise and reproduce the desired music/sound. Another applicaton is in training a machine learning model to tell us where the aduio signal is coming from, maybe a hallway, party or an ocean front. I'll try not to inundate this notebook with DSP mathematical ewuati so even the non-engineers can follow. The Mathematics involved in DSP are 'FUN' but it is also nice to visualize these concepts as we learn. Follow closely and I hope you find it helpful.

This notebook will use [NVIDIA RAPIDS](https://rapids.ai/) APIs and libraries, they'll help us take advantage of the amazing GPU speeds and computing power. [cuSignal](https://github.com/rapidsai/cusignal) in particular is very similar to the popular Python [SciPy](https://scipy.org) API used in so many engineering and scientific applications. [CuPy](https://cupy.dev/) is also replacing the popular [NumPy](https://numpy.org/) API in this notebook to take advantage of the GPU processing power. 

Why GPU processing you ask, well in a case where real-time processing is required, the faster the better so why not? You can handle higher sample rates, amongst other advantages. Professors, researchers, students, industry experts can easily leverage existing compatible GPUs they have to use RAPIDS. You don't have a supported GPU to run these APIs and libraries? Don't worry the CPU version of this notebook is included in the repository. Enough of the talk, now let's get into it. 
