# Projects Description

We are currently working on two different projects:
* Living Systematic Review on Psychedelic Treatments for Psychiatric Disorders: This is small project focusing on a niche area of research. It is a proof of concept of the type of web app and pipeline that we would like to use on a broader scale in future in the project below:
* Neuroscience # TODO: Simona

## Project components
Our final projects should have the following components:
* **Period fetching of newest publications**: We will periodically (e.g. every week) fetch the newest publications via the Pubmed API
* **Relevance Detection**: A language model classifies the new publication as relevant/not relevant for our project
* **Classification and NER**: The abstract (+ method section) of the fetched publication are passed through several fine-tuned BERT models for classification and NER
* **Continuously populated database**: The publications, the results of the relevance detection plus the classification and NER results are saved in database
* **Front-End**: Displays the research and classification/NER results in interactive graphs

Here is a schematic of what the pipeline would look like for the Psynamic Proje:


## What we have developed/are developing
* Fine-tuned models: fine-tuned models for relevance detection, classifciation and NER; saved as Pytorch Checkpoints
* Inference scripts: Python code to load the models and run inference
* Database: setup databases locally
  
  Here is the link to an ER Diagram (on Miro): https://miro.com/app/board/uXjVLLEtnVU=/?share_link_id=52084304523
  

* Fetching newst publication data: a python script to fetch newest research via API and writing it into the database
* Frontend: web app created with Dash (by Plotly), this is what the current protoype looks like:

  

## We need infrastructure & support with
* Store Database: a place to store the database
* Storing Models: a place to store fine-tuned model weights
* Scheduling data fetching & inference: automatically, periodically running python script to fetch data and run inference
* Webhosting: a server or service to host our front-end

