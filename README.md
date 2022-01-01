
# Intelligent Querying for Target Tracking in Camera Networks using Deep Q-Learning with n-Step Bootstrapping
** PyTorch implementation of our paper titled _Intelligent Querying for Target Tracking in Camera Networks using Deep Q-Learning with n-Step Bootstrapping_, Image and Vision Computing, 2020 

_Anil Sharma, Saket Anand, Sanjit K. Kaul_

[[Paper](https://www.sciencedirect.com/science/article/abs/pii/S0262885620301542)] [[BibTeX](https://dblp.uni-trier.de/rec/journals/corr/abs-2004-09632.html?view=bibtex)]

---
In this repository, we are sharing code for our IMAVIS paper that extends our ICAPS [paper](https://github.com/anilsh/scheduleQueries). We use deep Q-learning with n-step bootstrapping to learn a policy for camera selections. 

---

## Code

The code is organized as follows:
1. ```scripts``` All scripts are provided as python notebooks. 
2. ```data``` It contains data files for all datasets (all 4 sets of NLPR MCT, Duke). It also contains scripts to read these data files and also the training testing split as used in our ICAPS [paper](https://github.com/anilsh/scheduleQueries). Original images of the dataset can be downloaded from the dataset website. 


## Downloading the data

### NLPR MCT benchmark dataset

Download the dataset from the [[official website](http://mct.idealtest.org/Datasets.html)] . This dataset contains four sub-datasets and we have used all four in our method.
We have converted all datasets into trajectory files and only these are used by our method. These are placed in ```data``` folder and necessary scripts are provided to read the files and training/testing split.

---

### Dependencies

The code requires pytorch 1.1.0 and jupyter notebook (should work well with Python 3.5). Apart from it, you need to install scipy, matplotlib, numpy and hickle for loading and plotting purposes. 

### Pre-trained model

The pre-trained model and results for each specific case of the simulation are provide in 'models' . 

### Tables and Figures
In 'plots', you will find various scripts to reproduce all tables and figures reported in the paper. Use [MCT evaluation kit](http://mct.idealtest.org/Datasets.html) to generate MCTA values from the results file. Result files are kept in ```results_icaps``` folder for every case. 


### Training

To train a model from scratch, use any of the notebooks to train DQN policy for NLPR set-4. To train for a different dataset, change ```db_no``` in the notebook accordingly. 


---

If this code helps your research, please cite the following work which made it possible.

```
@inproceedings{sharmaScheduleCameras,
  title =        {Reinforcement Learning based Querying in Camera Networks for Efficient Target Tracking},
  author =       {Sharma, Anil and Anand, Saket and Kaul, Sanjit},
  booktitle =    {ICAPS},
  year =         {2019}
}

@article{Sharma2020IntelligentQF,
  title={Intelligent Querying for Target Tracking in Camera Networks using Deep Q-Learning with n-Step Bootstrapping},
  author={Anil Sharma and Saket Anand and Sanjit Krishnan Kaul},
  journal={ArXiv},
  year={2020},
  volume={abs/2004.09632}
}



```

## License

This code is licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/). Some external dependencies have their own license.

