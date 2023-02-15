<h3> Python request module and APIs </h3>

<h1> Get data through an API </h1>
```
r=requests.get('https://dog.ceo/api/breeds/list/all')
#here, data can be get via URL API
```

<h1> Store data in json formate </h1>
```
dict=r.json()
print(dict)
#store data in dict variable and print data
```

<h1> Dataframe - Store data in rows and columns formate</h1>
```
df=pd.DataFrame(dict.keys())
df
#store data in datafarme, get all keys and print them
```
<h1> Fetch data in nested dictonary </h1>
```
rows = []  

# appending rows
for data in dict:
    
    data_row = dict['message']
      
    for row in data_row:       
        rows.append(row)
# using data frame
df = pd.DataFrame(rows,columns=["Breed names"])
df
```
<h1>Make csv file</h1>
```
df.to_csv("dog_list.csv",index=False)
#index=False use to start index number from 1 
```

<h1>Read csv file</h1>
```
df1=pd.read_csv("dog_list.csv") 
```
<h1>Random number in pandas to use random.randint</h1>

<h1> Get UTC time to use datetime.utcnow()</h1>

<h1> To store image with time </h1>
```
file_name = f"dog_{random_dog}_{date.strftime('%Y-%m-%d')}.jpg"
```
<h1>Download, open and display image </h1>
```
import requests
from PIL import Image
from io import BytesIO
from IPython.display import display

# Download the image from the URL
response = requests.get("https://images.dog.ceo//breeds//husky//n02110185_14766.jpg")

# Open the image from the response content
img = Image.open(BytesIO(response.content))

# Display the image in the notebook
display(img)
```







