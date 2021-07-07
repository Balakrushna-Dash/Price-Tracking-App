# Created by :-
### Balakrushna Dash (19EC10075)
# Price-Tracking-App
#### Overview ::
This python scriepted app is built with keeping intentions of scrapping some e-commerce website and providing the instant information about the price drop of the product.
Currently it is functional in local devices and works perfectly fine for ***Flipkart*** products. But in future this project aims to expand over all e-commerce websites. 
Here I have built a simple website with flask for user interface. Lets dive deep into the insights then..
# Login / Create account ::
This is the entrance of the website accomodating all the user interactions. If new to the website then user has to create one first , if not he/she can diretly enter by filling 
up the login form.

![loginsignin](https://user-images.githubusercontent.com/56407204/124709112-bee7bf00-df18-11eb-982c-df7e10a11253.jpg)

# Home page ::
User will enter this page as sonn as he/she logs in. Here basically the basic instruction about using the website is mentioned. I reccomend to read it before exploring the website.

![home](https://user-images.githubusercontent.com/56407204/124710493-7cbf7d00-df1a-11eb-8500-c24f902bb373.PNG)

# Add Url ::
This pagge is meant for adding URLS and the price upperbound depending on which user wants to notify himself through the app. Any invalid email would be accepted. The valid URL requests given here gets reflected in the ***My Url List*** section.

![add](https://user-images.githubusercontent.com/56407204/124710746-cf009e00-df1a-11eb-9120-e922717f6bcf.PNG)

# My Url list ::
This page shows all the requests of URLS filled by the user. Cancellationn option is also available. Once the price goes beyond the upperbound the product atomatically gets deleted from the list and the email gets sent to the user rightaway.

![my list](https://user-images.githubusercontent.com/56407204/124711168-5ea64c80-df1b-11eb-8c8d-f2e0267b4f98.PNG)

# The price tracking script::
This part basically comprises of the python file ***app2.py*** . Here I am going through the entire database where all the URL request of each and every user is stored. Then using the BeautifulSoup lib I'm parsing the html page of corresponding product page in flipkart. From here I'm searching for the ***div*** tag with ***clas :: " _30jeq3 _16Jk6d "***. Below I have shown why that particular atribute of the div tag is being used for getting the price of the product. 

![proof](https://user-images.githubusercontent.com/56407204/124712749-5818d480-df1d-11eb-9319-38f2c1a2252f.png)

And whenever the price goes beyond the price upperbound , the user gets a notification by registered email by the help of ***Send Mail*** function and the corresponding product gets deleted from the data base using ***Cancel*** function. 
Finally this entire process is carried out inside a loop with a precise time gap (currently 30 sec) 



