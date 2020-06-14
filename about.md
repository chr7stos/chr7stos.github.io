---
layout: page
title: About
permalink: /about/
---


## Me in 10 seconds

I have done research in **biophysics**, I investigated the proton pumping mechanism in bacteriorhodopsin [phase separation in proteins](https://www.academia.edu/1107753/Liquid-Liquid_Phase_Separation_in_Protein_Solutions_Controlled_by_Multivalent_Salts_and_Temperature).

Then I moved to neuroscience for some time, I studied signal correlations in the brains of rodents for potential treatment of Parkinson's disease.

I have been a researcher in solid state physics, focusing on graphene as a new nanomaterial and [organic solar cells](https://www.sciencedirect.com/science/article/abs/pii/S0040609019302780). [Here](https://scholar.google.com/citations?user=i7TBNSMAAAAJ&hl=en) you can find more about my research.

I have then moved outside academia to data engineering and data science roles.    
Some things I have built are:
- a tool written in *python* orchestrating the production data pipeline in secure servers
- a module (again in *python*) extracting data from a production pipeline using json files
- a model predicting subway traffic based on mobile signaling data (it involved a hidden markov model)

## Some public talks I gave:
[Mapping with Folium](https://www.meetup.com/Python-Users-Berlin-PUB/events/xmdjfmywpbmb/) (Python Users Berlin)

[Introduction to (Py)Spark](https://www.meetup.com/fr-FR/PyData-Cyprus/events/259617209/) (PyData Cyprus)
# Build a streamlit dashboard and host it in AWS for free

1. Make sure you have python version > 3.5. The following was tested with python 3.6 on macOS.
2. Create a project directory, let's call it and `cd` inside
3. Install `virtualenv` using `pip install virtualenv` and then create a virtual environment called simply `venv` inside the project directory
4. Activate the virtual environment using `source venv/bin/activate`
5. Install streamlit using `pip install streamlit`
6. Do `pip freeze > requirements.txt` to document everything you installed using in that file to make it easy for the future you to create this virtual environment
7. 