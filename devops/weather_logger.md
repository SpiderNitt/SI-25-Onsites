#  Weather Logger in Docker

## Objective

Create a Dockerized system that logs current weather data for a specified city using the OpenWeatherMap API. A Bash script will fetch and parse the data, which will be stored in structured MongoDB collections. A cron job will automate periodic logging and backups of the database.

---

## Problem Statement

You are required to develop a weather logging tool using Bash and Docker. The tool should fetch current weather data for a given city using OpenWeatherMap's API and store the information into a MongoDB container with the following three collections:

- `Cities`
- `Temperatures`
- `Conditions`

You will also automate the data logging process using a cron job and implement regular backups of the MongoDB data.

---

## Functional Requirements

### 1. Weather Data Fetcher Bash Script

**Script Name:** `GetWeatherData.sh`

**Usage:**

```bash
bash GetWeatherData.sh "New York"
```
**Functionality:**

- Fetch current weather data from OpenWeatherMap API:

```
https://api.openweathermap.org/data/2.5/weather?q=CityName&appid=API_KEY&units=metric
```
- Parse the JSON response using awk (or jq if needed).
- Insert structured data into three MongoDB collections:
- Cities: { name, country, lat, lon }
- Temperatures: { city, temp, min, max, humidity, timestamp }
- Conditions: { city, main, description, icon, timestamp }

### 2. MongoDB Container
Deploy MongoDB in a Docker container and ensure it has the following collections:

```
Cities Collection

{
  "name": "New York",
  "country": "US",
  "lat": 40.7128,
  "lon": -74.0060
}

Temperatures Collection
{
  "city": "New York",
  "temp": 24.5,
  "min": 22.0,
  "max": 26.0,
  "humidity": 60,
  "timestamp": "2025-07-10T10:00:00Z"
}

Conditions Collection
{
  "city": "New York",
  "main": "Clear",
  "description": "clear sky",
  "icon": "01d",
  "timestamp": "2025-07-10T10:00:00Z"
}
```
### 3. Cron Job Setup
**Configure a cron job (on host or in a dedicated container) to:**
- Execute GetWeatherData.sh every hour.
- Append new weather entries into MongoDB collections with a timestamp.

### 4. MongoDB Backup Automation
**Create a separate Docker container or script that:**
- Performs a mongodump of the weather database every hour.
- Compresses the dump file (e.g., using tar or gzip).
- Stores the compressed backups in /backups directory.
- Optionally implements backup rotation or pruning.

### Deliverables
- GetWeatherData.sh script.
- Dockerized MongoDB instance with three collections:

    - Cities
    - Temperatures
    - Conditions

- Cron job for hourly logging.
- Cron job or container for hourly database backup.
- Screenshots or logs showing:

    - MongoDB entries from each collection.
    - Backup files stored in /backups.
