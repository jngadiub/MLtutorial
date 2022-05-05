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

Now you can install the ML libraries prepared for you as:

```
git clone https://github.com/jngadiub/MLtutorial.git
cd MLtutorial
conda env create -f mltutorial.yml
conda activate mltutorial
```

### How to create environment from scratch

If you have followed the instructions above you will not need to follow these steps but for completeness here are the instructions to build the environment from scratch after you have download and installed conda as above:

```
conda create --name mltutorial python=3.9
conda activate mltutorial
conda install jupyter
conda install h5py
conda install scikit-learn
pip install tensorflow
conda install pandas
conda install pytorch
conda env export > mltutorial.yml
conda activate mltutorial
```

nb, if you have a GPU available in order to use it you must install `tensorflow-gpu` instead of `tensorflow`.

## Download the data

Assuming you have already cloned the repo, let's download the datasets in advance so that we avoid a bandwidth bottleneck:

```
cd MLtutorial
curl https://cernbox.cern.ch/index.php/s/xmTytsMPvCEA6Ar/download -o Data-MLtutorial.tar.gz
tar -xvzf Data-MLtutorial.tar.gz 
ls Data-MLtutorial/JetDataset/
rm Data-MLtutorial.tar.gz 
```

## Run notebooks

```
git clone https://github.com/jngadiub/MLtutorial.git
cd MLtutorial
```

In a new shell start a jupyter notebook with command `jupyter notebook`. The browser will automatically open the page where you can navigate the folders and files inside the `MLtutorial` folder.




