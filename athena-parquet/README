## Create Tables
### Raw CSVs
    CREATE EXTERNAL TABLE IF NOT EXISTS flights.raw_data (
    	`year` SMALLINT,  
    	`month` SMALLINT,  
    	`day_of_month` SMALLINT,  
    	`flight_date` STRING,  
    	`op_unique_carrier` STRING,  
    	`flight_num` STRING,  
    	`origin` STRING,  
    	`destination` STRING,  
    	`crs_dep_time` STRING,  
    	`dep_time` STRING,  
    	`dep_delay` DOUBLE,  
    	`taxi_out` DOUBLE,  
    	`wheels_off` STRING,  
    	`arr_delay` DOUBLE,  
    	`cancelled` DOUBLE,  
    	`cancellation_code` STRING,  
    	`diverted` DOUBLE,  
    	`air_time` DOUBLE,  
    	`carrier_delay` DOUBLE,  
    	`weather_delay` DOUBLE,  
    	`nas_delay` DOUBLE,  
    	`security_delay` DOUBLE,  
    	`late_aircraft_delay` DOUBLE  
    ) 
    ROW FORMAT DELIMITED
          FIELDS TERMINATED BY ','
          ESCAPED BY '\"'
          LINES TERMINATED BY '\n'
    LOCATION 's3://INSERT_BUCKET_NAME/raw'
    TBLPROPERTIES (
      'skip.header.line.count'='1',
      'serialization.null.format'=''
    );

### Gzipped CSVs
    CREATE EXTERNAL TABLE IF NOT EXISTS flights.gzip_data (
    	`year` SMALLINT,  
    	`month` SMALLINT,  
    	`day_of_month` SMALLINT,  
    	`flight_date` STRING,  
    	`op_unique_carrier` STRING,  
    	`flight_num` STRING,  
    	`origin` STRING,  
    	`destination` STRING,  
    	`crs_dep_time` STRING,  
    	`dep_time` STRING,  
    	`dep_delay` DOUBLE,  
    	`taxi_out` DOUBLE,  
    	`wheels_off` STRING,  
    	`arr_delay` DOUBLE,  
    	`cancelled` DOUBLE,  
    	`cancellation_code` STRING,  
    	`diverted` DOUBLE,  
    	`air_time` DOUBLE,  
    	`carrier_delay` DOUBLE,  
    	`weather_delay` DOUBLE,  
    	`nas_delay` DOUBLE,  
    	`security_delay` DOUBLE,  
    	`late_aircraft_delay` DOUBLE  
    ) 
    ROW FORMAT DELIMITED
          FIELDS TERMINATED BY ','
          ESCAPED BY '\"'
          LINES TERMINATED BY '\n'
    LOCATION 's3://INSERT_BUCKET_NAME/raw'
    TBLPROPERTIES (
      'skip.header.line.count'='1',
      'serialization.null.format'='',
      'compressionType'='gzip'
    );

### Parquet Files using Snappy
    CREATE EXTERNAL TABLE IF NOT EXISTS flights.parquet_snappy_data (
    	`year` SMALLINT,  
    	`month` SMALLINT,  
    	`day_of_month` SMALLINT,  
    	`flight_date` STRING,  
    	`op_unique_carrier` STRING,  
    	`flight_num` STRING,  
    	`origin` STRING,  
    	`destination` STRING,  
    	`crs_dep_time` STRING,  
    	`dep_time` STRING,  
    	`dep_delay` DOUBLE,  
    	`taxi_out` DOUBLE,  
    	`wheels_off` STRING,  
    	`arr_delay` DOUBLE,  
    	`cancelled` DOUBLE,  
    	`cancellation_code` STRING,  
    	`diverted` DOUBLE,  
    	`air_time` DOUBLE,  
    	`carrier_delay` DOUBLE,  
    	`weather_delay` DOUBLE,  
    	`nas_delay` DOUBLE,  
    	`security_delay` DOUBLE,  
    	`late_aircraft_delay` DOUBLE  
    )
    STORED AS PARQUET
    LOCATION 's3://INSERT_BUCKET_NAME/parquet'
    tblproperties ("parquet.compress"="SNAPPY")

## Queries
