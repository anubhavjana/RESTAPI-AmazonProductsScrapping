@Authored by **Anubhav Jana**

Following are the REST API ENDPOINTS:

**POST** /api/scrap?url=<url link>    ---> Returns the scraped amazon url products data with the current timestamp of scrapping

**POST** /api/scrap/add?url=<url link>    ---> Adds the scraped data to the database with the current timestamp of addition

**GET** /api/get                     ---> Returns the list of documents

**GET** /api/get/url?url=<url link>  ---> Returns list of document by url

**PUT** /api/update/price?url=<url link>  --> Updates price if changed

**PUT** /api/update/rating?url=<url link> --> Updates rating if changed


Example : 

          POST /api/scrap?url=https://www.amazon.in/Amazon-Brand-Solimo-Cotton-Paisley/dp/B06WLGNSVJ

          POST /api/scrap/add?url=https://www.amazon.in/Amazon-Brand-Solimo-Cotton-Paisley/dp/B06WLGNSVJ

          GET /api/get/url?url=https://www.amazon.in/Amazon-Brand-Solimo-Cotton-Paisley/dp/B06WLGNSVJ

          PUT /api/update/price?url=https://www.amazon.in/Amazon-Brand-Solimo-Cotton-Paisley/dp/B06WLGNSVJ

          PUT /api/update/rating?url=https://www.amazon.in/Amazon-Brand-Solimo-Cotton-Paisley/dp/B06WLGNSVJ
          
          
Sample pictures has been uploaded for users to view the result on making requests to the API endpoints.

**URLS to test sample: **

https://www.amazon.in/Amazon-Brand-Solimo-Cotton-Paisley/dp/B06WLGNSVJ

https://www.amazon.in/dp/B07X9YN2FJ

https://www.amazon.in/RiteBite-Max-Protein-Work-Out-Almond/dp/B01M69GJOO

https://www.amazon.in/dp/B077GTDWSJ

MongoDB Database : https://cloud.mongodb.com/v2/5ff95e8fbf9c497af5125d85#metrics/replicaSet/5ff96302b4381c4da67a1fa6/explorer/AmazonScrappedDatabase/AmazonScrappedCollection/find

**Username**: anubhav

**Password:** can be found in api_constants.py

**## How to build**:

**Prerequisites**: Docker

Run the following commands:

$ move to the current working directory where the files are there

$ docker image build -t scrap-flaskapp .  #Finds the dockerfile in the current directory and builds an image named scrap-flaskapp: 

$ docker run -it scrap-flaskapp  # Starts running the docker image

Go to your localhost and check.

# Dockerfile has been added to the repo.

-> Uses alpine:latest as the base image
