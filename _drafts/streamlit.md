 # Build a streamlit dashboard and host it in AWS for free

1. Make sure you have python version > 3.5. The following was tested with python 3.6 on macOS.
2. Create a project directory, let's call it and `cd` inside
3. Install `virtualenv` using `pip install virtualenv` and then create a virtual environment called simply `venv` inside the project directory
4. Activate the virtual environment using `source venv/bin/activate`
5. Install streamlit using `pip install streamlit`
6. Do `pip freeze > requirements.txt` to document everything you installed using in that file to make it easy for the future you to create this virtual environment
7. 