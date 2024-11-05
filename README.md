# -dataengineering-youtube-statistics-project
🌐 Project Spotlight: Analyzing YouTube Trends Across the Globe with AWS Data Engineering 🌐

I recently completed a data engineering project where I built a pipeline to process and analyze trending YouTube video data across multiple regions. Here’s how I tackled this and the tech stack I used:

🔗 Dataset: https://lnkd.in/gdaNsKKf

 This dataset contains daily trending video stats from regions across the globe. Each file includes video metadata, like title, publish time, views, likes, dislikes, and comment counts, making it ideal for multi-region trend analysis.


🛠 Tools and Technologies:

• AWS Lambda: For automated file conversion on S3 uploads

• AWS Glue: ETL pipeline for data transformation and integration

• Amazon S3: Storage for both raw and processed data

• Amazon Athena: For querying data without needing a dedicated database

• Amazon QuickSight: Dashboarding to visualize trends and insights


🔍 Project Workflow:

1️⃣ Automated Data Transformation:

• Problem: The dataset includes both CSV and JSON files, and JSON isn’t directly queryable in Athena.

• Solution: Implemented a Lambda function to auto-convert JSON files to Parquet upon upload to S3. CSV files were also converted to Parquet using Glue ETL jobs, ensuring consistency and faster querying.

2️⃣ Data Cleaning and Standardization:

• Converted and cleansed data was organized in a dedicated S3 staging bucket and categorized under a cleansed database.

• Transformed data types across the dataset to align with a common schema.

3️⃣ Data Integration and Consolidation:

• Built an AWS Glue job to join data across multiple regions, creating a single unified dataset.

• Stored the final processed data in a separate analytical S3 bucket, ready for analysis.

4️⃣ Interactive Dashboarding:

• Leveraged Amazon Athena to run queries on the unified dataset.

• Created interactive dashboards in Amazon QuickSight to visualize insights, such as regional engagement trends, top-performing channels, and content popularity.



🎯 Results and Insights:

➼ This pipeline automated data processing, reducing the time spent on data preparation and enabling near real-time trend analysis.

➼ QuickSight dashboards provided a comprehensive view of YouTube trends, empowering stakeholders to make data-driven content decisions based on regional preferences and viewer engagement.



💡 Takeaway:

This project highlights the efficiency of serverless AWS tools for large-scale data engineering. By automating data transformation and unifying diverse datasets, I delivered a scalable solution for cross-regional video trend analysis.
