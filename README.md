# 20170124 Google TensorFlow and MS CNTK on One Machine
After much reading and experimentation I'm starting to collect my AI-bits here.

I got TensorFlow and CNTK running together on Windows 10 and Ubuntu 16.04, physical machines with GPU support and VMware virtual machines using Anaconda 4.2.  
There are a ton of installation variants for TensorFlow (Python 2 and 3 (virtualenv), Anaconda, Docker, with and without GPU support on Windows, Linux and Mac) and my common denominator is Anaconda.

With the standard CNTK installation scripts Anaconda 4.1.1 gets installed, but if you install the latest Anaconda to the common base directory first and pass the installation location to the PowerShell scipt, it accepts the version you throw it.  
It will install the desired module versions to its Anaconda environment anyway.

```markdown
cd c:\local
.\install.ps1 -AnacondaBasePath c:\local\Anaconda3
```

Initially I posted a rant on the CNTK forum, because I regarded the suggested `c:\local` location quite weired --- only to find out weeks later when I finally got around to dig into compiling CNTK:  
It had a literal dozen of dependencies on locations and versions of pivotal parts, and `c:\local` was one of them. (apart from the exact Visual Studio 2013 version, the custom Intel MKL DNN version and the exact location of all kinds of Nvidia CUDA libraries,...)  
Sure you could tweak some of that, but I wouldn't want to know what could be hard-coded somewhere and I wouldn't like to run into the endless hassles.

The VS 2013 dependency made me shy away from this, because I already had fattened my physical Windows installation by 20 GB with a basic Visual Studio 2015 for working with Nvidia CUDA and didn't want to risk to screw this up.

So currently I'm waiting for MS to alleviate at least the VS 2013 requirement until I give compiling CNTK another shot.

In the meantime I set up Google Bazel to compile TensorFlow and it sort of worked, at least on Ubuntu, but I rather dig into TensorFlow and CNTK practical examples.

# 20170123 Welcome to Günter's AI Page!
Actually I prefer ballroom dancing, not really dressed up, but still...

![Babycha](images/Babycha1.gif)

And I like to run after balls for the life of me, mainly in soccer / football, (beach) volleyball. Too short for basketball.
