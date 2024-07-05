#import streamlit as st
from datetime import datetime

# Set up the title and description of the app
st.title("Voting App")
st.write("Please fill in your details to check your eligibility to vote.")

# Create input fields for the user's information
name = st.text_input("Name")
age = st.number_input("Age", min_value=0, max_value=120)
country = st.text_input("Country")
nida_number = st.text_input("NIDA Number")
street_number = st.text_input("Street Number")
date_of_birth = st.date_input("Date of Birth")
place_of_birth = st.text_input("Where are you from?")

# Check if the user is eligible to vote
if st.button("Check Eligibility"):
    if country.lower() == "tanzania":
        st.success("You are eligible to vote.")
    else:
        st.error("You are not eligible to vote. Only Tanzanian citizens can vote.")

# Display the entered information
st.write("## Your Details")
st.write(f"**Name:** {name}")
st.write(f"**Age:** {age}")
st.write(f"**Country:** {country}")
st.write(f"**NIDA Number:** {nida_number}")
st.write(f"**Street Number:** {street_number}")
st.write(f"**Date of Birth:** {date_of_birth}")
st.write(f"**Place of Birth:** {place_of_birth}")
