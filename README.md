# Custom Weighted Balanced Loss Function for COVID-19 detection from an imbalanced CXR dataset.

by
Mrinal Tyagi,
Santanu Roy,
Vibhuti Bansal


This paper has been presented as a Poster presentation in 26th International Conference on Pattern Recognition. 

> In this paper, we have worked in a new direction, that is, alleviating the class imbalance problem from CXR dataset by using novel loss function. 
> We have choosen a challengable CXR dataset consisting of 4 classes namely COVID, Normal, Lung Opacity and Viral Pneumonia. 
> The real problem in this dataset is not only the class imbalance, but also huge intra class variance. Hence we come up with a new strategy my modifying bias weights in WCCE based on statistical properties of images in that class. 

> ### Methodology
![Methodology](https://user-images.githubusercontent.com/21031150/194772944-a0816d47-ff16-4f9f-92be-68a861fd1f5a.PNG)

> ### Results (4 Class)
![3](https://user-images.githubusercontent.com/21031150/194773039-0c9bb1ae-7013-4cc2-838c-a48c8f5e2be8.PNG)

> ### Results (3 Class)
![4](https://user-images.githubusercontent.com/21031150/194773047-396cbac5-fd6a-4caf-a230-8d5a5761bf7d.PNG)

## Abstract

> In this paper, we have proposed a novel framework, that is ResNet-18 model along with Custom Weighted Balanced loss function, in order to automatically detect Covid-19 disease from a highly imbalanced Chest X-Ray (CXR) dataset. Covid 19 disease has become a global pandemic, for last two years. Early automatic detection of Covid-19, from CXR images has been the key to survive from this pandemic. In the recent advent, researchers have already proposed several Deep Learning (DL) models, which can detect Covid-19 disease (with higher accuracy) from CXR images. However, Covid-19 detection by DL models are fraught with the problem of class imbalance, since most of the available CXR datasets are found highly imbalanced. In this paper, we have worked in a new direction, that is, alleviating the class imbalance problem from CXR dataset by using novel loss function. First, we choose a challengeable CXR dataset in which there are four classes, they are Covid, Normal, Lung Opacity (LO) and Viral Pneumonia (VP). Later we have identified that real problem of this dataset is not only the class imbalance, but also, huge intra-class variance is observed in Covid class. Therefore, we have come up with a new idea, that is, modifying the bias weights in a Weighted Categorical Cross Entropy (WCCE), based on reducing both of the factors, i.e., class imbalance and intra-class variance from the dataset. For the experimentation, we have chosen a ResNet-18 model which is trained from scratch for a large Chexpert CXR dataset and thereafter it is pre-trained on the Covid CXR dataset. Experimental results suggest that ResNet18 model along with proposed Custom Weighted Balanced loss function, have improved 2-4% accuracy, precision, recall, F1 score and AUC for four class CXR dataset. Furthermore, we have tested the same framework for three class Covid CXR dataset, after excluding LO class. We have achieved 96% accuracy, 97% precision, 96% recall, 97% F1 score and 97% AUC for three class classification task. This is significant (3-4%) improvement than the performance of ResNet-18 model with CCE.


## Software implementation

All source code used to generate the results in the paper are for 4 class experiments and 3 class experiments are in '4 Classes Experiment' and '3 Classes Experiment' folders respectively.
The calculations and figure generation are all run on
[Colab Service](https://colab.research.google.com/notebooks/intro.ipynb).


## Getting the code

You can download a copy of all the files in this repository by cloning the
[git](https://github.com/MrinalTyagi/CWBCCE-COVID19) repository:

    git clone https://github.com/MrinalTyagi/CWBCCE-COVID19.git

or [download a zip archive](https://github.com/MrinalTyagi/CWBCCE-COVID19/archive/refs/heads/main.zip).


## Dependencies

You'll need a working Python environment to run the code.
The recommended way to set up your environment is through the
[Anaconda Python distribution](https://www.anaconda.com/download/) which
provides the `conda` package manager.
Anaconda can be installed in your user directory and does not interfere with
the system Python installation.
The required dependencies are specified in the file `environment.yml`.

We use `conda` virtual environments to manage the project dependencies in
isolation.
Thus, you can install our dependencies without causing conflicts with your
setup (even with different Python versions).

Run the following command in the repository folder (where `environment.yml`
is located) to create a separate environment and install all required
dependencies in it:

    conda env create


## Reproducing the results

Before running any code you must activate the conda environment:

    source activate ENVIRONMENT_NAME

or, if you're on Windows:

    activate ENVIRONMENT_NAME

This will enable the environment for your current terminal session.
Any subsequent commands will use software that is installed in the environment.

For reproducing the results, execute the Jupyter notebooks individually.

To do this, you must first start the notebook server by going into the
repository top level and running:

    jupyter notebook

This will start the server and open your default web browser to the Jupyter
interface. In the page, go into the respective folder and select the
notebook that you wish to view/run.

The notebook is divided into cells (some have text while other have code).
Each cell can be executed using `Shift + Enter`.
Executing text cells does nothing and executing code cells runs the code
and produces it's output.
To execute the whole notebook, run all cells in order.


## License

All source code is made available under a BSD 3-clause license. You can freely
use and modify the code, without warranty, so long as you provide attribution
to the authors. See `LICENSE.md` for the full license text.
