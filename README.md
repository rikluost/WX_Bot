# Rasa Weather Bot

## Installation
 
Installation assumes existing installation of miniconda or anaconda. 
https://www.anaconda.com/

### pip & rasa

Below are the simple steps for creating a virtual environment, install pip and Rasa Open Source 2.0.

```python
conda create -n rasa
conda activate rasa
conda install -c anaconda pip
pip install rasa
```
In case of issue, please refer to Rasa Open Source installation pages: 
https://rasa.com/docs/rasa/installation/

### Creating and initialising a new project:

```python
mkdir wxbot
cd wxbot
rasa init --no-prompt
```
This will create a new directlry, under which rasa creates all necessary directories and files.

Replace all files in the wxbot directory with the files in the provided template.

## Train the model and run the bot

Train the model with command 

```python
rasa train
```

There are additional actions that need to be started before starting the bot evaluation. These are in ```actions.py``` and ```wx.py``` files. 

```python
rasa run actions
```

Start the discussion with wxbot:

```python
rasa shell
```


