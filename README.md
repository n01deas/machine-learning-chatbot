# Rasa Chatbot

Machine learning Chatbot using the Rasa stack.

Rasa NLU for natural language understanding and Rasa Core as a dialog engine.

## What’s inside the bot

- **data/nlu.md** contains training examples for the NLU model  
- **data/stories.md** contains training stories for the Core model  
- **config.yml** contains the model configuration
- **domain.yml** contains the domain of the assistant  
- **credentials.yml** contains credentials for the different channels
- **actions.py** contains custom actions

## How to use this example?

1. Get rasa
   ```
   pip install rasa
   ```

2. Go in your shell to the project
   ```
   cd projectdirectory
   ```

3. Train a Rasa model containing the Rasa NLU and Rasa Core models by running:
    ```
    py -m rasa train
    ```
    The model will be stored in the `/models` directory as a zipped file.

4. Run a Rasa server that connects, for example, to Facebook:
    ```
    py -m rasa run -m models -p 5002 --connector facebook --credentials credentials.yml
    ```
    If you want to connect to a different channel, replace `facebook` with the name of the
    desired channel.
    All available channels are listed in the `credentials.yml` file.

    If you don't want to use any channel, you can chat with your bot
    on the command line, using the following command:
    ```
    py -m rasa shell
    ```
