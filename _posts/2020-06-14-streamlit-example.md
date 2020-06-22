---
layout: post
title: Create a dashboard with streamlit and deploy it in aws
---

## What is streamlit?
Streamlit is a fast way to create data apps. You can find more information about it [here](https://www.streamlit.io/).    
Go to gallery and get inspired by amazing data apps built by other people.

## What is the problem I wanted to solve?
There are numerous open data out in the wild internet. They are often found online in various forms, like for example `csv`or `json`.    Unfortunately, most of the places you can find the data, do not offer a way to check how this data look.   
With streamlit, I wanted to build a basic visualisation tool to do a first data exploration.   
This way, you can immediately have a first look at the data before downloading them, to check whether you want to use them.

## How did I solve it?

### These are the steps to build this data app:

1. Make sure you have python version > 3.5. The following was tested with python 3.6 on macOS.
2. Create a project directory, let's call it `streamlit_example` and `cd` inside
3. Install `virtualenv` using `pip install virtualenv` and then create a virtual environment called simply `venv` inside the project directory
4. Activate the virtual environment using `source venv/bin/activate`
5. Install streamlit using `pip install streamlit`
6. Do `pip freeze > requirements.txt` to document everything you installed using in that file to make it easy for the future you to create this virtual environment
7. Create a directory called `data` and download the `csv` from [here](https://www.data.gov.cy/dataset/%CF%84%CF%81%CE%AD%CF%87%CE%BF%CF%85%CF%83%CE%B1-%CF%80%CE%BB%CE%B7%CF%81%CF%8C%CF%84%CE%B7%CF%84%CE%B1-%CF%86%CF%81%CE%B1%CE%B3%CE%BC%CE%AC%CF%84%CF%89%CE%BD). It shows the completeness of water dams in Cyprus.
8. Create a file called `streamlit_example.py` and write the code. You can find the code for this app in this github repository, but here is the code as well:

<script src="https://gist.githubusercontent.com/chr7stos/a1e1c2eb9cab4f08eab76c60432abc6d/raw/7cfa6e60a8794816df6e7c46af851da6653a21f2/streamlit-example.py"></script>

9. Then run `streamlit run streamlit-example.py` and you will be able to view the dashboard in your browser.

### These are the steps to deploy the app in aws


