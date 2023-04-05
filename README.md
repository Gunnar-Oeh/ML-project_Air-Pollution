# ML Project 
- Assignment 3rd Week of neuefische.de DataScience Bootcamp

We took on the https://zindi.africa/competitions/urban-air-pollution-challenge without entering the competition for the multiple day ML-Project within the neuefische.de DataScience Bootcamp. 

Participants:
Dr. Clara Bredow (https://github.com/ClaraBredow)
Isabelle-Carina Flaig (https://github.com/IsabelleCarinaFlaig)
Gunnar Oehmichen (https://github.com/Gunnar-Oeh)

The results before applying a DenseNeuralNetwork are in the presentation [presentation_challenge.pdf]()

---
## Requirements and Environment

Requirements:
- pyenv with Python: 3.9.8

Environment: 

For installing the virtual environment you can either use the Makefile and run `make setup` or install it manually with the following commands: 

```Bash
pyenv local 3.9.8
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

## Usage

In order to train the model and store test data in the data folder and the model in models run:

```bash
#activate env
source .venv/bin/activate

python example_files/train.py  
```

In order to test that predict works on a test set you created run:

```bash
python example_files/predict.py models/linear_regression_model.sav data/X_test.csv data/y_test.csv
```

## Limitations

Development libraries are part of the production environment, normally these would be separate as the production code should be as slim as possible.
