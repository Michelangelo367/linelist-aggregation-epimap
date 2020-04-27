# Linelist Aggregation Epimap
> Data transformation and aggregation of Linelist for the Epimap

## Installation

I recommend you to install a Python environment with conda, virtualenv or pipenv.

### Conda
For example with conda, 
[download and install miniconda](https://docs.conda.io/en/latest/miniconda.html)

#### Option 1 : Using env.yml
Create the conda environment
```
conda create -n epimap -f env.yml
```

Activate the conda environment
```
activate epimap
```

#### Option 2 : Installing package by package
Create a conda environment
```
conda create -n epimap python=3.8
```

Activate the conda environment
```
activate epimap
```

Install dependencies
```
conda install pandas==1.0.3
conda install xlrd==1.2.0
conda install openpyxl==3.0.3
```

### Virtualenv or pipenv

Setup a virtualenv or pipenv

Install dependencies
```
pip install -r requirements.txt
````

## Development Usage

Run the Python script aggregator.

```
python src/aggregator.py 
```

To release, install pyinstaller `pip install pyinstaller`, and use the following command

````
pyinstaller src/aggregator.py -F --hidden-import="pkg_resources.py2_warn"
````

*Remark : there is an hidden-import argument to fix
[a Pyinstaller issue](https://github.com/pypa/setuptools/issues/1963).*

## User usage

- Rename the data file `Linelist.xlsx` and put it in the same directory as 
`aggregation_epimap.exe`.
- Run `aggregation_epimap.exe` by double-clicking.
- You will see 2 files : `logs.log` containing the logs about all the executions.
and `AggregatedLinelist.xlsx` file if the running is successful

## Tests

Go to the tests directory and run unittest
```
cd tests
python -m unittest discover
```

## License

The project has an [MIT license](Licence.md).
