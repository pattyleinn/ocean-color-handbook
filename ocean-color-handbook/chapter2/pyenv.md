<!-- @format -->

**Authors:** Mathabo Malange, Phangoxolo Sishuba

# Python Working Environments

A Python working environment is a tool that helps keep dependencies required by
different projects separate by creating virtual environments for them. They are
useful for instances where you are working on two different projects on the same
machine, where both projects require the same package but different versions of
it.

For example, you are working on `project A` which requires
`packageX version 1.0` which you have installed to your global Python library.
You then switch to work on `project B` on the same machine and install
`packageX but version 2.0` which has several changes from version 1.0. If you
had to go back and run `project A` after installing version 2.0, you would get
all sorts of errors. To avoid this, we use virtual environments, as the name
suggests, which are created as isolated environments for specific projects as
discussed in this
[article](https://www.freecodecamp.org/news/how-to-setup-virtual-environments-in-python/).

## How to Set up a Python Working Environment

To create a Python working environment, we will use the Anaconda Prompt terminal
and the command `conda`. With `conda`, you can create, export, list, remove, and
update environments that have different versions of Python and/or packages
installed in them. Switching or moving between environments is called activating
the environment. You can also share an environment file. Here, we only provide
the steps necessary to create a working Anaconda environment. For more in depth
discussion, please refer to Anaconda
[user’s guide](https://conda.io/projects/conda/en/latest/user-guide/index.html).
As mentioned in {numref}`how-to-proceed` above, before proceeding, please make
sure that you have already installed Anaconda by following the installation
instructions [here](https://docs.anaconda.com/anaconda/install/).

## Creating an environment in Anaconda

Open a terminal or command prompt and verify that Anaconda has been properly
installed and active. In Windows, there is a dedicated Anaconda Prompt that can
be found from the Search bar by typing Anaconda Prompt. In the Unix-based
systems, after the installation is complete and Anaconda activated, the terminal
should have the word _"(base)"_ appear in the terminal. Use the terminal or an
Anaconda Prompt with the following steps:

1. To create an environment:

```
$conda create --name myenv
```

```{note}
Replace "myenv" with the environment name of your choice.
```

When asked to proceed, type y:

`proceed ([y]/n)? `

This creates the "myenv" environment in the `envs` directory of Anaconda. The
command `$ conda env list` print a list of available environments. No packages
will be installed in this environment.

2. To create an environment with a specific version of Python:

```
$conda create -n myenv python=3.9
```

The option "-n" is a short form of the long "--name".

3. To create an environment with a specific package:

```
$conda create -n myenv python=3.9 scipy
```

or

```
$conda create -n myenv python
$conda install -n myenv scipy
```

4. To create an environment with a specific version of a package:

```
$conda create -n myenv scipy=0.17.3
```

5. To create an environment with a specific version of Python and multiple
   packages:

```
$conda create -n myenv python=3.9 scipy=0.17.3 matplotlib
```

```{bulb} **Tip:**
Install all the programs that you want in your environment at the same time. Installing one program at a time can lead to dependency conflicts.
```

6. Once the environment is create, activate it environment with the command

```
$conda activate myenv
```

You can add much more to the conda create command. For details, run

```
$conda create –-help
```

## Creating an environment from an environment file

We can create an Anaconda environment using an environment file. This file can
be created from an existing environment by typing `conda env export`. To limit
the export to only packages that were explicitly installed by the user, use
`conda env export --from-history`. Additionally, environment files can be
created manually. For the latter, follow the guide
[here](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#create-env-file-manually).
Use the terminal or an Anaconda Prompt for the following steps:

1. Create the environment from a file named "environment.yml"

```
$conda env create -f environment.yml
```

Note that the environment name "myenv" is specified inside the "environment.yml"
file. Verify the new environment was installed correctly:

```
$conda env list
$conda info --envs
```

## Updating an environment

You may need to update your environment for a variety of reasons. For example,
it may be the case that:

- One of your core dependencies just released a new version (dependency version
  number update).
- You may need an additional package for data analysis (add a new dependency).
- You may have found a better package and no longer need the older package (add
  new dependency and remove old dependency).

If any of these occur, all you need to do is update the contents of your
environment.yml file accordingly and then run the following command:

```
$conda env update --prefix ./env --file environment.yml --prune
```

The `--prune` option causes `conda` to remove any dependencies that are no
longer required from the environment.
