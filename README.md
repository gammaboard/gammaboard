[![deprecated](http://badges.github.io/stability-badges/dist/deprecated.svg)](http://github.com/badges/stability-badges)

----

## GammaBoard is now integrated and developed in [ctaplot](https://github.com/vuillaut/ctaplot) and will no longer be supported in this repository.

----

# GammaBoard

_A dashboard to show them all._


GammaBoard is a simple jupyter dashboard thought to display metrics assessing the reconstructions performances of 
Imaging Atmospheric Cherenkov Telescopes (IACTs).   
Deep learning is a lot about bookkeeping and trials and errors. GammaBoard ease this bookkeeping and allows quick 
comparison of the reconstruction performances of your machine learning experiments.

It is a working prototype used in CTA, especially by the [GammaLearn](https://gitlab.lapp.in2p3.fr/GammaLearn/) project

## Dependencies
- ctaplot>=0.3.0
- pytables
- pandas
- scikit-learn
- jupyter
- ipywidgets

## Install

```
cd gammaboard
pip install .
```

```
export GAMMABOARD_DATA=path_to_the_data_directory
```

We recommend that you add this line to your bash source file (`$HOME/.bashrc` or `$HOME/.bash_profile`)


## Run GammaBoard

To launch the dashboard, you can simply try the command:
```gammaboard```

This will run a temporary copy of the dashboard (a jupyter notebook).
Local changes that you make will running the dashboard will be discarded afterwards.

GammaBoard is using data in a specific directory storing all your experiments files.
This directory is known under `$GAMMABOARD_DATA` by default.
However, you can change the path access at any time in the dashboard itself.

## Demo

Here is a simple demo of GammaBoard.
- On top the plots (metrics) such as angular resolution and energy resolution.
- Below, the list of experiments in the user folder.

When an experiment is selected in the list, the data is automatically loaded, the metrics computed and displayed.
A list of information provided during the training phase is also displayed.    
As many experiments results can be overlaid.     
When an experiment is deselected, it simply is removed from the plots.



![gammaboard_demo](share/gammaboard.gif)
