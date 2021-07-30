# Data Stream Pipeline


The purpose of this project is to show a data ingestion pipeline using python.  I will use screenshots to show the actual data being ingested. 
I created an app that generates random data that I use as customer transaction data.  This data represents a consistent data flow (pipeline) into PostgreSQL.  

Company B will represent my database (PostgreSQL).
This screenshot shows the PostgreSQL database prior and post ingestion.
This screenshot shows the ingested data coming into my system then going into PostgreSQL.
Create a custom endpoint and set the stream value to True as this will allow constant flow of data until the requested valued has been reached.

INSTRUCTIONS


1. Create a database called “test_stream” with the following columns (txid, uid, amount)
   Columns:  

  	CREATE TABLE transactions 
    (
	txid uid,
	uid uuid,
	amount money);

 
2. Run the ‘mock_api.py ‘ file by typing “python mock_api.py" in the terminal or running the mock_api.py file in your interpreter. (Pycharm, VScode etc). 
Be sure you are in the directory with the actual file when running the files. 

4. Test it by visiting http://127.0.0.1:5000/very_large_request/10 

5. Run the  “python ingest.py” file. Expect lots of lines of output written to the console,
