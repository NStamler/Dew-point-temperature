import streamlit as st
import numpy as np

# Constants
a = 17.27
b = 237.7

# Function to calculate dew point temperature
def calculate_dew_point(T_ambient, RH):
    gamma = np.log(RH / 100) + (a * T_ambient) / (b + T_ambient)
    T_dew = (b * gamma) / (a - gamma)
    return T_dew

# Streamlit app
st.title("Dew Point Temperature Calculator")

# Input sliders
T_ambient = st.slider("Ambient Temperature (°C):", min_value=0.0, max_value=50.0, value=25.0, step=0.1)
RH = st.slider("Relative Humidity (%):", min_value=0, max_value=100, value=50, step=1)

# Calculate dew point
T_dew = calculate_dew_point(T_ambient, RH)

# Display result
st.write(f"Dew Point Temperature: **{T_dew:.2f} °C**")
