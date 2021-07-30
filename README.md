# Data Stream Pipeline

Description

I'm sharing a pipeline I created from a data stream using FLASK. The data will represent customers transactions and be scheduled to run daily using CRONTAB. The data will stream into a PosgreSQL database for 3 hours straight.  I will show the PostgreSQL dashboard so you can see the flow of incoming data. Feel free to get creative with this project and make it your own.  



Think of Company A as a retailer's production database receiving sales in real-time. You are Company B and work for Company A as a data engineer.  You will simply create and schedule an ETL pipeline from Company A's production database to PostgreSQL. Schedule the ETL process using CRONTAB which is available on all linux based systems.  



ETL Execution



1 . Copy the attached mock_api.py and ingest.py files separately into your text editor or download files.    



2 . Create a database called “test_stream” with the following columns (txid, uid, amount)
 	Columns:  

  		CREATE TABLE transactions (
		txid int, 
		uid uuid PRIMARY KEY,
		amount money);

 
3. Run the ‘mock_api.py ‘ file by typing “python mock_api.py” in the terminal or 			running the mock_api.py file in your interpreter. (Pycharm, VScode etc). Be sure you 	are in the directory with the actual files, when running the files. 

4. Test your mock_api app by visiting http://127.0.0.1:5000/very_large_request/10 (You should see a sample of the data in your browser)

5. Run the  “python ingest.py” file.  (Expect lots of lines of output running on your 	systems terminal)

6. Check to see if the data is streaming into PostgreSQL without any issues   

7. Stop the data ingestion test and schedule the ingestion to occur daily with 	CRONTAB

8. Create a new crontab or use the existing one if you want the job to run on midnight 	every day.

9. VOILA you've just created your first data pipeline.  

