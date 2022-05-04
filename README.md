# MLtutorial

## Prepare ML environment

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh 
```

nb, if you work on MacOS you need to change the first command above to:

```
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh -o Miniconda3-latest-MacOSX-x86_64.sh
```

Answer `yes` to first question to accept license terms.
For the second question about the installation path be sure you insert a path where you have enough space.
Answer `yes` to last question to initialize the environment every time you open a new shell.
This will change your `.bashrc` or `.bash_profile` file in your home directory to point to this conda installation.

To check that this step went fine open a new shell and type `which conda` which should point you to the installed binary file. You can now close the old shell.

### How to create environment from scratch

If you have followed the instructions above you will not need to follow these steps but for completeness here are the instructions to build the environment from scratch after you have download and installed conda as above:

```
conda create --name mltutorial python=3.9
conda activate mltutorial
conda install jupyter
conda install h5py
```

In a new shell start a jupyter notebook with command `jupyter notebook`.




