## Introduction
Helping system for COVID-19, it can estimate your healthy situation depend on your location and surrounding situation.

## Ideas
The ideas behind this app is from Chinese Health Code. In the COVID-19 situation, there is an increased risk every time we go outside. So I use a accumulated points to represent the healthy situation. Every time the user goes to another place, it increases the infection possibilty. In addition, it is risky to go to crowded place. I have calculated the ideal number people in the scan area of bluetooth based on Wolrd Health Organization's recommendation. https://www.who.int/emergencies/diseases/novel-coronavirus-2019
The health points are all based on location and bluetooth information. Nothing is stored in the device and uploaded to the server. This is because, I think the app should work without the Internet. Because there are people don't use data plan.
The health value is based on those conditions:
    1.You get 20 points subtracted every time you register a new place in the phone.
    2.You get 20 points subtracted if there are more than 17 people around you in radius of 10 meters.
    3.You get 100 points subtracted if there are more than 97 people around you in radius of 10 meters.
    4.You get nothing subtracted if there are less than 17 people around you in radius of 10 meters.
    
The calculation is based on:
Minimum of social distancing: 1.8 meters.
Maximum of air aerosol and droplet infection: 4 meters.

## Location and Surrounding
Please press GET PLACE and choose your location when you arrive at new place.
You can press PLACE button to get recent place you have been.
If you want to know that if you are safe or not, Please click nearby devices and click scan for devices.
Then click return scanned devices. 
After this, you can click ENV button to get approximately number of people around you.

## Health Value
Health value is a great tool to measure your health situation, every time you scan or get places,
Our system will give you a health evaluation. If you score is under 400, please consider stay at home.

## Code
Added part is in MapsActivityCurrentPlace.java onCreate(), onActivityResult() and openPlacesDialog()

API is deleted, please add a API key when test it.
