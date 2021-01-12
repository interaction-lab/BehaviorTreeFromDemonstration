# Behavior Tree Robot Action Policy from SAR WoZ Interaction Data

##### This repository was made to facilitate the investigations in developing behavior tree robot action policy from Socially Assistive Robot (SAR) Wizard of Oz (WoZ) Interaction Data. This pipeline processes logged data from a WoZ interaction and generates behavior trees, along with data on the accuracy of the conversion process. These behavior trees are ready to be used alongside the BehaviorTree.CPP library, and redeployed back in the robot.

---
## Install
1. Clone repo
2. Create python3 [virtual environment](https://docs.python.org/3/library/venv.html) and activate it
3. Install python3 requirements via `pip3 install -r requirements.txt`
	1. There are a couple
4. Fix [graphviz error via package install](#graphviz-pip-error)
5. Fix [pyeda library error](#pyeda-literal-error)

## To run:

- Navigate to `BehaviorTreeDev/`
- edit `config.json`
- `python3`: run `python3 run.py`


## Dependencies

- [Python 3](https://www.python.org/downloads/)
- [pandas](https://pandas.pydata.org/pandas-docs/stable/index.html) 
- [scikit-learn](https://scikit-learn.org/stable/index.html)
- [imblearn](https://imbalanced-learn.readthedocs.io/en/stable/index.html)
- [graphviz](https://graphviz.readthedocs.io/en/stable/index.html)
- [matplotlib](https://matplotlib.org/) 
- [lxml](https://lxml.de/)
- [py_trees](https://py-trees.readthedocs.io/en/devel/)

See `requirements.txt` for all python3 packages (currently bugged on WSL). There are two other install issues due to issue with `graphiz` and `pyeda` packages. Fixes below.

### graphviz pip error
graphiz for python is broken. Instead, install via package manager:
```bash
sudo apt-get install graphviz
```
For OSX, likely you will need to `brew install` but this is yet to be tested.

### pyeda literal error
There is a bug is Pyeda library. See [#17](https://github.com/interaction-lab/BTFromSARDemostration/issues/17) for fix.

---

The behavior tree XML file(s) that are generated from the pipeline follow the XML format for behavior trees presented in [BehaviorTree.CPP](https://www.behaviortree.dev/) and [Groot](https://github.com/BehaviorTree/Groot).

