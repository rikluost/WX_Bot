# Weather Chatbot with Rasa Open source 2.0 Conversational AI 

## introduction

As natural language processing (NLP) technology and chatbot systems over the past few years have evolved quickly, also the usefulness of chatbots has increased. The motivation of chatbots is productivity; they have instant access to information they refer to and are efficient in assisting users. (Brandtzaeg, 2017, *Why people use chatbots*). Weather chatbot is an excellent use case example for the technology.

The content of a chatbot consists of the personality, conversation flows and the information it can deliver to the user. Personality is created by interactions and responses and by acting differently in different situations. These responses should be designed so that it maximises the engagement between the bot and the user (Katz, 2019, *The Ultimate Guide to chatbot personality*, Chatbots Magazine). An important part of the engagement is the ability to respond to any chitchat. The weather chatbot described here aims to use these principles, however due to the efforts required, in a rather minimalistic way leaving plenty of room for future improvements.

## Weather data

The weather data format chosen here is defined by OpenWeather (OpenWeatherMap.com, n.d), which provides weather data freely for developers. Auckland, Wellington, and Christchurch data are prefetched for testing purposes. For activating the API, modify:

```python
use_openweather_API = True
API_key = "Insert your key here"
```


## Conversation Flow

The conversation is initiated by the end-user. A greeting or a goodbye should reset any prior assumptions or knowledge collected by the bot during previous interactions. When time or weather detail are not contained in the query, the bot shall report the current and generic weather conditions. When the city is not provided in the query, the bot shall request for it. Any further specifics in the query should be answered in more detail if information is available. 

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

Replace all files in the wxbot directory with the files in the project

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


