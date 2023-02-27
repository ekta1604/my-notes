# Python request module and APIs 

## Get data through an API
```r=requests.get('https://dog.ceo/api/breeds/list/all')```
### here, data can be get via URL API

## Store data in json formate 
```dict=r.json() print(dict)```
### store data in dict variable and print data

## Dataframe - Store data in rows and columns formate
```df=pd.DataFrame(dict.keys())```
### store data in datafarme, get all keys and print them

## Fetch data in nested dictonary 
```
rows = []  

### appending rows
for data in dict:
    
    data_row = dict['message']
      
    for row in data_row:       
        rows.append(row)
### using data frame
df = pd.DataFrame(rows,columns=["Breed names"])
df
```
## Make csv file
``` df.to_csv("dog_list.csv",index=False) ### index=False use to start index number from 1 ```

## Read csv file
``` df1=pd.read_csv("dog_list.csv") ```
## Random number in pandas to use random.randint

## Get UTC time to use datetime.utcnow()

## To store image with time 
``` file_name = f"dog_{random_dog}_{date.strftime('%Y-%m-%d')}.jpg" ```
## Download, open and display image 
```
import requests
from PIL import Image
from io import BytesIO
from IPython.display import display

### Download the image from the URL
response = requests.get("https://images.dog.ceo//breeds//husky//n02110185_14766.jpg")

### Open the image from the response content
img = Image.open(BytesIO(response.content))

### Display the image in the notebook
display(img)
```
