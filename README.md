# GreenFlow

## Description

This project serves to show how to implement a basic Rest API for Data processing and used in the context of Docker Containers and inserting the data to persist in Mongodb.
The project docker-compose will generate two container / services one for the app another for the db where its used Binding Volume to persist the db data to to host in project data folder. Also a User Interface (UI) with streamlit and with it also upload parquet file into memory and persist also in file format in the server side.

## Features

* Rest API Endpoints (base URL: http://localhost:8080/):
  * Summary (returns a breave list of information pertaning the DataSet)
  * cleanDataSet (Cleans The DataSet of missing data from rows and extra spaces)
  * parquettodb (Inserts the DataSet after the Clean up process into MongoDB with the collection name being the name of the file [filename]
* 

## Installation

1. Clone the repository:

   ```
   git clone git@github.com:HCorte/GreenFlow.git
   ```
2. Navigate to the project directory:

   ```
   cd your-repo
   ```
3. Install Virtual Environment

   ```
   python -m venv venv
   ```
4. Activate Virtual Environment

   ```
   source venv/bin/active
   ```
5. Install dependencies (inside the Virtual Environment):

```
   pip install -r requirements.txt
```

## Usage

* Run the project:

  ```
  python src/api.py
  ```
* Open in browser at `<span>http://localhost:8080/Summary</span>` to make a simple test
* Import from the folder postman the collection to postman by:

  * Open Postman -> Select File -> Select "Import..." -> then select the collection inside the postman folder of this project.

## To create Dockers Containers

* Build and run containers
  ```
  docker compose up --build
  ```
* Now can call as usuall the endpoints from postman and the app in container will respond and save in a second container the db as well backup in the host in this project data folder.

## Streamlit Report

* Option to have a brief detailed analysis of your data on Streamlit. 

* Please click on the following link and upload your parquet file: https://dataops.streamlit.app/

## Contributing

* Rest API
* streamlit

## License

This project is licensed under the MIT License.
