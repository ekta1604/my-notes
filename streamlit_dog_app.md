# Streamlit Dog Application 

## Make an application which select a dog breed from dropdown menu, when user press submit button then it will show an image according to that selected breed of dog

## URL Title in Streamlit 
```st.set_page_config(page_title="Dog Pictures")```

## Load the list of dogs from the CSV file
```dogs_df = pd.read_csv("dog_list.csv")```

# Define the Streamlit form
# For Dropdown menu in Streamlit
```selected_dog = st.selectbox("Select a dog:", dogs_df["Breed names"])```

# Submit button 
```submit_button = st.button("Submit")```

# Create function to get desired URL
# When user select a breed of dog then below URL will generate according to that breed 
```def generate_url(selected_dog: str)-> str:```
    ```return f"https://dog.ceo/api/breed/{selected_dog}/images/random"```
```my_url=generate_url(selected_dog)```

# Create a function to get image URL
# This function will generate response in bytes
```def get_dog_image(my_url: str)-> str:```
    ```response = requests.get(my_url)```
    ```print(response)``
    ```return response.content```
```image_bytes = get_dog_image(my_url)```
```print(image_bytes)```

# store image_bytes in data 
```data = image_bytes```

# streamlit and python do not support image in bytes
# Convert bytes to string
```data_str = data.decode('utf-8')```

# Parse JSON string
```data_json = json.loads(data_str)```

# Fetch value of "message" key
```message_value = data_json['message']```

# Display the image
```if submit_button and image_bytes:```
    ```st.image(message_value)```

