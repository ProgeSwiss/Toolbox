Release Note – Currency Exchange Rate Synchronization Solution
  - Version: 0.2.0
  - Release Date: 2025-01-19
  - Solution Name: Currency Exchange Rate Synchronization


Overview
  - This initial release introduces a fully automated mechanism to keep currency exchange rates up to date across the environment, ensuring accurate financial data and reporting.


Key Features
  - Automated Daily Execution:
    A scheduled flow runs every day at 3:30 AM, triggering the update process without requiring manual intervention.

  - Real-Time Exchange Rate Retrieval:
    A child flow connects to FreeCurrencyAPI via a custom connector to fetch the latest exchange rates based on the environment's default currency.

  - Dynamic Dataverse Update:
    The retrieved exchange rates are used to automatically update the Rate field in the Dataverse system table TransactionCurrency for all active currencies.

  - Exchange Rate Logging:
    All updates are logged into a custom Dataverse table called Exchange Rate, providing traceability and historical insight.


Purpose
  This solution ensures that the environment maintains consistent, accurate, and current exchange rate data, supporting finance-related processes and reporting with minimal maintenance effort.


Dependencies
  - Custom Connector to FreeCurrencyAPI
  - Scheduled Flow (runs daily at 03:30 AM)
  - Child Flow for data retrieval and update

Access to Dataverse tables: TransactionCurrency, Exchange Rate

