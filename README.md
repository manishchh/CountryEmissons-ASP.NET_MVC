## Overview

This project provides a platform to track, analyze, and display environmental data across different regions and countries. It includes data models for air quality stations, temperature monitoring, and country emissions tracking.

## Technology Stack

- **Framework:** ASP.NET Core 6.0
- **Language:** C#
- **Database:** SQL Server
- **ORM:** Entity Framework Core 6.0.21
- **Frontend:** Razor Views with Bootstrap
- **Additional Tools:** Swashbuckle (Swagger/OpenAPI)

## Features

- **City Management:** Browse and view details of cities with environmental data
- **Country Tracking:** Track countries and their emissions data over time
- **Region Information:** Manage regions and their environmental characteristics
- **Air Quality Monitoring:** Display and analyze air quality station data
- **Temperature Data:** Track temperature measurements and trends
- **Responsive UI:** Bootstrap-based responsive design
- **REST API:** Swagger/OpenAPI documentation support

## Prerequisites

- .NET 6.0 SDK or later
- SQL Server (LocalDB or full instance)
- Visual Studio 2022 or Visual Studio Code

## Getting Started

### 1. Clone the Repository
```bash
git clone <repository-url>
cd Assig1
```

### 2. Set Up the Database

#### Option A: Using Raw SQL Script (Recommended for Initial Setup)

1. Update the connection string in `appsettings.json`:

```json
{
  "ConnectionStrings": {
    "EnvData": "Server=(localdb)\\mssqllocaldb;Database=EnvData;Trusted_Connection=true;"
  }
}
```

2. Execute the SQL script using SQL Server Management Studio (SSMS) or SQL Server command line:

**Using SSMS:**
- Open SQL Server Management Studio
- Connect to your SQL Server instance
- Open the `EnvData.sql` script file from the `root` directory
- Select the target server and execute the script


### 4. Build the Project

```bash
dotnet build
```

### 5. Run the Application

```bash
dotnet run
```

The application will be available at `https://localhost:5001` (or the port specified in `launchSettings.json`).

## Database Models

- **Country:** Represents a country entity
- **Region:** Geographic regions within countries
- **City:** Cities within regions
- **AirQualityStation:** Monitoring stations for air quality
- **AirQualityData:** Air quality measurements from stations
- **TemperatureData:** Temperature readings and historical data
- **CountryEmission:** Emission data by country over time
- **Element:** Environmental elements being monitored


### Sample Data

The SQL script includes seed data from multiple countries and regions:
- **Time Period:** 2010-2017 (with some data extending to 2018)
- **Regions:** Multiple countries including Andorra, UAE (Abu Dhabi), Australia (Sydney, Western Australia)
- **Measurements:** Air quality (PM10, PM2.5), temperature, and emissions data


