This project involves the development and implementation of an end-to-end application for Flight Prediction using Snowflake. The workflow spans from data ingestion to building a web application with Streamlit, fully integrated with Snowflake.

The data resides in AWS S3, and I have created a storage integration object and an external stage to seamlessly load data from S3 into Snowflake. After ingestion, the data was enriched, transformed, and utilized for training machine learning models. A prediction application was then developed using Streamlit in Snowflake.

To structure and scale the data processing effectively, I implemented the Medallion Architecture:
- The Bronze Layer is represented by the `FLIGHT_DATA` table, which holds raw, unprocessed source data in its original form for auditing or reprocessing purposes.
- The Silver Layer is embodied by the `AIRLINE_ENRICHED` table, where data is cleaned, transformed, and enriched to create a refined dataset ready for analytics.
- The Gold Layer corresponds to the `AIRLINE_ML_MODEL_DATA` table, where the data is meticulously curated and prepared for machine learning model training and evaluation, ensuring high-quality inputs for optimal performance.

This architecture ensures a structured and scalable approach to managing and analyzing data throughout the application.
