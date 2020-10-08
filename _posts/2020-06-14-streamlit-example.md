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


```python
import streamlit as st
import altair as alt
import pandas as pd

st.title("Monthly water inflows since 1988 in Cyprus")
st.markdown("""
This is a dashboard with data data.gov.cy **data.gov.cy** and you can get them [here](https://www.data.gov.cy/dataset/μηνιαία-εισροή-νερού-στους-ταμιευτήρες-νερού-φράγματα).   
The goal is to have easy simple visualisations for more of the open data in Cyprus.
""")

df = st.cache(pd.read_csv)("data/monthly_water_inflows_from_1988.csv")

month = st.selectbox('Show available months', df.columns[1:], 0)

st.markdown("Flow of water in Cyprus dams")

chart = alt.Chart(df).mark_line().encode(
    x='YEAR',
    y=month
).interactive()

st.altair_chart(chart)
```
9. Then run `streamlit run streamlit-example.py` and you will be able to view the dashboard in your browser.

### These are the steps to deploy the app in aws
`Coming soon`


