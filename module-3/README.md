CREATE MATERIALIZED VIEW yellowtaxijanjune24.yt_view
AS
(
  SELECT * FROM yellowtaxijanjune24.yellow_taxi_janjun2024
);

SELECT COUNT(*)
FROM yellowtaxijanjune24.yellow_taxi_janjun2024;

SELECT COUNT(DISTINCT PULocationID)
FROM yellowtaxijanjune24.yellow_taxi_janjun2024;

SELECT COUNT(DISTINCT PULocationID)
FROM yellowtaxijanjune24.ytjanjune24_ext;

SELECT PULocationID
FROM yellowtaxijanjune24.yellow_taxi_janjun2024;

SELECT PULocationID, DOLocationID
FROM yellowtaxijanjune24.yellow_taxi_janjun2024;

SELECT COUNT(*)
FROM yellowtaxijanjune24.yellow_taxi_janjun2024
WHERE fare_amount = 0;

SELECT DISTINCT VendorID
FROM yellowtaxijanjune24.yellow_taxi_janjun2024
WHERE tpep_dropoff_datetime BETWEEN '2024-03-01' AND '2024-03-15';

SELECT DISTINCT VendorID
FROM yellowtaxijanjune24.yt_partitioned
WHERE tpep_dropoff_datetime BETWEEN '2024-03-01' AND '2024-03-15';
