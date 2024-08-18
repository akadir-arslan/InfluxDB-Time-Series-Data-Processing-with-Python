# InfluxDB Time-Series Data Processing with Python

This project demonstrates how to install, configure, and use InfluxDB, a time-series database, to create and retrieve random moisture level measurements with Python. It includes setting up InfluxDB, writing 100 random measurements, and querying the data to extract and display the results.

---

### Project Overview

This project focuses on working with InfluxDB, a time-series database, to store and retrieve sensor measurements. Using Python, the project simulates moisture level data from various sensors located in different parts of a home. The primary tasks include:

- Installing and configuring InfluxDB.
- Developing a Python application to generate and store moisture measurements.
- Querying and displaying the stored measurements.

---

### Prerequisites

- **InfluxDB Installation:** Download InfluxDB from [the official website](https://www.influxdata.com/downloads/) and install it on your local machine. You can either use Docker or perform a native installation based on your operating system.
- **Python Installation:** Ensure Python is installed on your machine.
- **Python Libraries:** Install the required libraries by running the following commands:
  ```bash
  pip install influxdb_client

### How to Run

  1. **Set Up InfluxDB:**
    - Start InfluxDB after installation.
    - Use the InfluxDB UI to create your organization, user, bucket, and API token.
  2. **Running the Python Script:**
    - Open the provided Jupyter Notebook or Python script.
    - Replace the credentials (`url`, `token`, `bucket`, and `org`) in the script with your InfluxDB instance details.
    - Execute the cells to generate and store 100 random moisture level measurements.
  3. **Query and Display the Data:**
    - Run the provided query to retrieve and display the moisture level data stored in InfluxDB.

### Data Model

The simulated moisture level measurements are structured as follows:

- Measurement: `moisture_level`
- Tags:
  - `location` (e.g., living-room, bathroom)
  - `sensor_type` (e.g., capacitive_sensor, resistive_sensor)
- Fields:
  - `value` (moisture level as a percentage)
  - Timestamp: UTC timestamp generated at the time of data creation

### Project Structure

- influxdb.ipynb: The Jupyter Notebook file containing the code to generate, store, and retrieve the moisture measurements.

### Results

After executing the notebook, you will see the generated measurements being stored in the InfluxDB bucket. The query retrieves the data for the past 10 hours, displaying details like the time, location, sensor type, and moisture level.