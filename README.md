
# Data Processing and Analysis Pipeline

This repository contains a comprehensive data processing and analysis pipeline designed to handle large datasets efficiently. The pipeline includes data cleaning, Kafka streaming, and various data analysis algorithms such as Apriori, PCY, and SON, with results stored in a MongoDB database.

## Overview

The pipeline comprises several stages:

1. **Data Cleaning**: Initially, the dataset underwent cleaning to reduce its size and enhance its usability. Approximately 15 GB of data was extracted from the original 105 GB dataset. Superfluous columns were dropped, leaving only three essential columns for further analysis.

2. **Kafka Producer**: A Kafka producer module was developed to read the preprocessed JSON data file. It sends the data to a Kafka topic line by line, ensuring efficient streaming and processing.

3. **Kafka Consumers**:
   - **Apriori Consumer**: This consumer implements the Apriori algorithm for frequent itemset mining. It extracts valuable patterns from the data stream, aiding in market basket analysis and similar applications.
   - **PCY Consumer**: Another consumer is dedicated to the Park-Chen-Yu (PCY) algorithm. PCY efficiently identifies frequent itemsets using a two-step process, contributing to improved performance and scalability.
   - **Hadoop Mapper and Reducer**: This consumer prepares the data for analysis using the SON algorithm by mapping and reducing it in a Hadoop environment. SON, or "Savasere, Omiecinski, and Navathe," is an algorithm for finding frequent itemsets in large datasets.

4. **Result Storage**: The results obtained from the analysis are stored in a MongoDB database. MongoDB provides a scalable and flexible solution for managing large volumes of data, enabling efficient querying and retrieval.

## Setup Instructions

To set up and run the pipeline locally, follow these steps:

1. Clone the repository to your local machine.
2. Ensure you have Kafka and MongoDB installed and configured properly.
3. Run the data cleaning script to preprocess the dataset.
4. Start the Kafka producer to stream the preprocessed data to Kafka topics.
5. Run each Kafka consumer module to perform the desired analysis tasks.
6. Verify that results are successfully stored in the MongoDB database.

## Dependencies

- Kafka
- MongoDB
- Python 3.x
- Additional Python libraries (specified in requirements.txt)

## Contributors

- [Aitazaz Kamran](https://github.com/AitazazKamran)
- [Contributor 1](https://github.com/MueezRiz)
- [Contributor 2](https://github.com/contributor2)

