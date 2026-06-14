Laptop Price Predictor

A machine learning web app that predicts laptop prices based on hardware specifications. Built with Python, trained using regression models, and deployed via Docker.


Demo

Run locally or pull the Docker image:

bashdocker pull apurva4913/lappy2
docker run -p 8501:8501 apurva4913/lappy2

Then open http://localhost:8501 in your browser.


Features


Predicts laptop price based on specs like RAM, CPU, GPU, storage, and screen size
Interactive UI built with Streamlit
Fully containerized with Docker for easy deployment



Tech Stack


Python 3.9
Scikit-learn
Pandas / NumPy
Streamlit
Docker

Project Structure

├── app.py                  # Streamlit app
├── df.pkl                  # Preprocessed dataset
├── pipe.pkl                # Trained ML pipeline
├── requirements.txt
├── Dockerfile
└── laptop_data.csv


Docker

Build the image yourself:

bashdocker build -t laptop-price-predictor .
docker run -p 8501:8501 laptop-price-predictor


Model

Trained on a dataset of 1000+ laptops. Uses a regression pipeline with feature encoding for categorical variables (brand, CPU, GPU, OS) and numerical features (RAM, storage, screen size, resolution).
