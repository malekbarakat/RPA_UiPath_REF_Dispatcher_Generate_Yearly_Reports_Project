# RPA UiPath REF Dispatcher - Generate Yearly Reports

## Project Overview
The **RPA_UiPath_REF_Dispatcher_Generate_Yearly_Reports_Project** is an automation process developed by **[Your Name]** using **UiPath**. This dispatcher process is responsible for extracting and adding transaction items to an **Orchestrator Queue** to facilitate the generation of yearly reports.

## Purpose
This dispatcher process is designed to:
- Retrieve required data from a source (such as an application, database, or web portal).
- Process and structure the extracted data into **transaction items**.
- Upload the transaction items into **UiPath Orchestrator Queue** for processing by the **Performer Process**.

## Project Structure
This project follows the **UiPath Robotic Enterprise Framework (REF)**, ensuring scalability, error handling, and reusability.

### 1. **Init State (Initialization)**
- Loads configuration settings from the **Config.xlsx** file.
- Initializes applications and required system connections.
- Retrieves necessary credentials from **Orchestrator Assets**.

### 2. **Get Transaction Data**
- Extracts the required data from the defined source.
- Adds extracted data as **transaction items** to the **Orchestrator Queue**.
- Moves to the next data set until all items are successfully added.

### 3. **Process Transaction** (Not Applicable)
- This dispatcher does not process the transactions directly but ensures they are available in the queue for the **Performer Process**.

### 4. **End Process**
- Cleans up system resources.
- Logs final execution status.

## Dependencies
- **UiPath Studio** (Compatible with version 2021.10 or later)
- **UiPath Orchestrator** (For transaction queue management)
- **UiPath REFramework**
- **Microsoft Excel** (For configuration settings if applicable)

## Configuration
The automation is configured using a **Config.xlsx** file, containing:
- Orchestrator Queue Name
- System/Application URLs
- Credentials (managed in Orchestrator Assets)
- Logging and error-handling settings

## Execution Steps
1. **Open the project** in UiPath Studio.
2. **Update the Config.xlsx** file with required parameters.
3. **Publish the Dispatcher Process** to UiPath Orchestrator.
4. **Schedule or Manually Run** the dispatcher process in Orchestrator.
5. **Monitor execution logs** in UiPath Orchestrator.

## Logging & Error Handling
- **Exception Handling:** Implements `try-catch` blocks for error resilience.
- **Logging:** Uses UiPath’s logging functionality to track workflow execution.
- **Retries:** Configured to retry failed transactions based on **Config.xlsx** settings.

## Future Enhancements
- Support additional data sources.
- Implement notification alerts for errors.
- Optimize data extraction for performance improvements.

## Author
Developed by **[MalekAlBarakat]**, leveraging UiPath’s best practices for RPA automation.
