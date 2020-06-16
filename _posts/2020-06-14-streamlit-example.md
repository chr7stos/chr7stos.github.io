---
layout: post
title: Create a dashboard with streamlit and deploy it in aws
---

Streamlit is a fast way to create data apps.

The following are the steps to build such a data app to view open source data.

1. Make sure you have python version > 3.5. The following was tested with python 3.6 on macOS.
2. Create a project directory, let's call it and `cd` inside
3. Install `virtualenv` using `pip install virtualenv` and then create a virtual environment called simply `venv` inside the project directory
4. Activate the virtual environment using `source venv/bin/activate`
5. Install streamlit using `pip install streamlit`
6. Do `pip freeze > requirements.txt` to document everything you installed using in that file to make it easy for the future you to create this virtual environment

