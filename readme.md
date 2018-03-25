# Carworkz-Scraper
## Technologies
##### MongoDB version : 3.4.7
##### NodeJS version : 8.4.0

## APIs
#### 1) Scrap WebPage
url : (GET) localhost:3000/api/scrap

Scraps : [https://www.carworkz.com/mumbai/regular-service](https://www.carworkz.com/mumbai/regular-service) created on **(25-03-2018)**.
 *#Note* : It may not work if structure of the dom changes


#### 2) Reset Data
url : (POST) localhost:3000/api/reset

Clears all the documents from the *Service Centre* collection.


#### 3) Search Service Centre
url : (POST) localhost:3000/api/search

Request object :  application/json

* **name** : string - name of the service centre[case insensitive]
* **authorized_by** : array of string - name of the company (eg.tata,maruti)[case insensitive]
* **services** : array of string - services provided by the centres (eg. reqular,paid)[case insensitive]
* **features** : array of string - features of the service centres (eg. pickup,card,cashless)[case insensitive]
* **min_ratings** : number - will show the centres having rating more than equal to this
All the above parameters are required(non empty) when included in the request object
