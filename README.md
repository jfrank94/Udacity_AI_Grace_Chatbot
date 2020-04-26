# Udacity_AI_Grace_Chatbot
A RASA-powered chatbot for Grace Cho of the Udacity Bertelsmann AI Program.

A couple of housekeeping rules. In order to install the RASA library and all of its depencies and run everything correctly, please run the folowing commands from this Stackoverflow post. You may need to downgrade your tensorflow version to 1.15.0 depending on whether you have the newest one.

To train the models, type in this command: python -m rasa train

To view the cross-validation score from training the model, type in this command:

python -m rasa test nlu -u nlu.md --config config.yml --cross-validation

For running the chatbot, type in the following:

python -m rasa run actions --actions actions --debug (the debug flag is optional)

Then:

python -m rasa shell --endpoints endpoints.yml
