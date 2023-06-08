# Natural Language Processing Application

The application is designed to take unstructured prompts from users and convert them into a request body format. It is built using Python and is intended to be run in Google Colab. This request body is in-line with the rules that are going to be specified in the requirements section.

A CSV file called 'Codes.csv' is used containing the features and their abbreviations. 

### Requirements
1. The prompts entered by the user must be in natural language and may not follow a specific format, therefore the application must be able to extract relevant info from unformatted text.
2. The request body should include:
    1. booleanFormulas: The Boolean formulas for which the model types should be resolved. (More details on following requirements) 
    2. modelTypeCodes: The model type codes to be considered for the resolution.
    (More details on following requirements)
    3. dates: The dates to which the computation should be performed. Each date must be a date in the format "YYYY-MM-DD".

3. The syntax for the booleanFormulas is as follows. It is only required from the application to handle booleanFormulas with three variables at most. The available variable abbreviations and their meanings are also shown below.:
  Operators -
  And, +
  Or, /
  And Not, +-
  Or not, /-

### Examples:
User Prompt: “I am planning to order the BMW M8 with a sunroof or panorama glass roof sky lounge, and the M Sport Package on 12th April 2018. Is this configuration possible?”

Request Body: 
{
  "modelTypeCodes": ["DZ01"],
  "booleanFormulas": [“+(S403A/S407A)+P337A”],
  "dates": ["2018-04-12"]
}


    
