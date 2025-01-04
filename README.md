# Live Currency Converter Dashboard

## Introduction

This project focuses on creating a **Currency Converter Dashboard** using a live API and the **Django** framework. The project aims to provide a user-friendly interface for currency conversion with historical trends and future forecasts.

The project is hosted on an Oracle Cloud virtual machine, allowing it to be globally accessible 24/7 via the link: [Live Dashboard](http://140.238.154.93:8080/).

### Key Features:
- **Live Currency Conversion**: Provides real-time exchange rates fetched from a live API.
- **Historical Trends**: Displays the currency conversion trends for the past 365 days.
- **Forecasting**: Offers a forecast for the currency conversion rates over the next 30 days.
- **Global Access**: Hosted on Oracle Cloud, accessible worldwide.


## Tools and Technologies Used

- **Programming Language**:  
  - **Python**

- **Libraries**:
  - **Requests**: For making HTTP requests and interacting with APIs to request data from the web.
  - **Pandas**: For converting the data into data frames and performing data cleaning and processing.
  - **Plotly and Matplotlib**: For creating visualizations.
  - **Datetime and Date**: For working with dates and times.
  - **Prophet**: For forecasting the selected rates for the next 30 days.
  - **Object-Oriented Programming (OOP)**: Advanced Python concepts like classes and methods have been utilized to structure the code for better reusability, maintainability, and organization.

- **Framework**:  
  - **Django**: For designing the website, as the goal was to create a currency converter hosted on a virtual machine.

- **API Used**:  
  - [Exchange Rates API](https://apilayer.com/)

- **Cloud Technology**:  
  - **Oracle Ubuntu Compute Instance**: For hosting the project.
  - **Gitbash**: For interacting with the virtual machine.
  - **Putty**: For setting up the virtual machine on Oracle Cloud.

- **Website Design**:  
  - **HTML**, **CSS**

- **Version Control**:  
  - **Git**: For committing the code and pulling it to the virtual machine.

- **IDE**:  
  - **Visual Studio**

- **Operating Systems**:  
  - **Windows**, **Linux**

## Project Execution

### 1. Finding an API for Exchange Rates
A reliable API was selected to provide real-time exchange rate data for various currency pairs, ensuring accurate and up-to-date information for the dashboard.

### 2. Selecting a Framework for Dashboard Creation
**Django** was chosen for dashboard development due to its ability to be deployed on a server within a cloud VM. Unlike Tableau or Power BI, Django allows for running the dashboard on a cloud server, offering flexibility and remote access.

### 3. Code with comments explaining the code

**ExchangeRateAPI Class**
The `ExchangeRateAPI` class is responsible for interacting with the API to fetch exchange rate data, transforming the data into a usable format, and utilizing caching mechanisms to avoid redundant API calls. Below is a snippet of the code that demonstrates how this class is structured and utilized in the project.

![Image1](code_part_1.png)

![Image2](code_part_2.png)

**Currency Conversion**
The `CurrencyConverter` class provides the method `convert`, which allows users to convert a specified amount from one currency to another. It retrieves the most recent exchange rates from the `ExchangeRateAPI` class, calculates the conversion based on the exchange rates, and returns the converted amount rounded to two decimal places.

![Image3](code_part_3.png)

**Exchange Rate Analysis**

The `ExchangeRateAnalysis` class is designed to handle data processing and analysis for exchange rates. It provides two key methods:

1. **ETL Process**: 
   - The `etl_process` method performs the data extraction, transformation, and loading (ETL) process. It cleans the data by converting date and rate columns to the appropriate formats, removing rows with missing values, and sorting the data by date and currency.
   
2. **Change Rate**: 
   - The `change_rate` method calculates the percentage change in exchange rates from the previous day. It filters the data to get the most recent and previous dates, computes the percentage change for each currency, and returns the top 5 currencies with the highest gains and losses.

Both methods ensure that the data is cleaned, analyzed, and ready for further use, such as visualizations or reporting.


![Image4](code_part_4.png)



![Image5](code_part_5.png)

