# udacity-data-engineering-data-lakes

# Project: Spark and Data Lakes

## Introduction

<p>A music streaming startup, Sparkify, has grown their user base and song database even more and want to move their data warehouse to a data lake. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.</p>

<p>Sparkify want to build an ETL pipeline that extracts their data from S3, processes them using Spark, and loads the data back into S3 as a set of dimensional tables. This will allow their analytics team to continue finding insights in what songs their users are listening to.</p>


## Project Datasets

### Song Dataset

The first dataset is a subset of real data from the [Million Song Dataset](http://millionsongdataset.com/).
Each file is in JSON format and contains metadata about a song and the artist of that song. 

The files are partitioned by the first three letters of each song's track ID. For example, here are filepaths to two files in this dataset.

>**s3://udacity-dend/song_data/A/B/C/TRABCEI128F424C983.json**<br>
>**s3://udacity-dend/song_data/A/A/B/TRAABJL12903CDCF1A.json**


Below is an example of what a single song file, **TRAABJL12903CDCF1A.json**, looks like.<br>

```
{
    "num_songs": 1, 
    "artist_id": "ARJIE2Y1187B994AB7", 
    "artist_latitude": null, 
    "artist_longitude": null, 
    "artist_location": "", 
    "artist_name": "Line Renaud", 
    "song_id": "SOUPIRU12A6D4FA1E1", 
    "title": "Der Kleine Dompfaff", 
    "duration": 152.92036, <br>
    "year": 0    
}
```


## <br>Project Files

In addition to the data files, the project workspace includes 5 files:

**1. dl.cfg**                    Contains the Secret Key for ASW access<br>
**2. create_bucket.py**          Create bucket in AWS S3 to store the extracted dimentional tables.<br>
**3. etl.py**                    Loading song data and log data from S3 to Spark, transforms data into a set of dimensional tables, then save the table back to S3 <br>
**4. etl.ipynb**                 Used to design ETL pipelines <br>
**5. README.md**                 Provides project info<br>

## Configuration

Remember to set key and secret in **./aws/dl.cfg** before run **etl.py**<br>

[AWS]<br>
key = <br>
secret = <br>

## Build ETL Pipeline

**etl.py** will process the entire datasets.

## Author

**Angelina Frimpong**
    
