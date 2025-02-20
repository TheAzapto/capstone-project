Software Requirement Specification
For
Bloom

Version 1.0

**PREPARED BY**
**Group Name: Zen**

| Aayush Dutta  | BT22GCS125 | Aayush.dutta22@st.niituniversity.in   |
| :------------ | :--------- | :------------------------------------ |
| Drishti Joshi |            | Drishiti.joshi22@st.niituniversity.in |

**Course**: CS 392 \- Capstone Project
**Faculty**: Manish Hurkat
**Date**: 20th February 2025

**Organization:** NIIT University

| CONTENTS                                                                                                                                                                                                                         |    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -- |
| Contents                                                                                                                                                                                                                         | 1  |
| Revision                                                                                                                                                                                                                         | 2  |
| Introduction<br />    Document Purpose <br />    Product Scope <br />    Intended Audience <br />    Definitions, Acronyms and Abbreviations <br />    Document Conventions <br />    References and Acknowledgement | 3  |
| Overall Description<br />    Product Overview <br />    Product Functionality <br />    Design and Implementation Constraints                                                                                             | 6  |
| Specific Requirements<br />    External Interface Requirements <br />    Functional Requirements <br />    Use Case Model                                                                                                  | 8  |
| Other Non-Functional Requirements<br />    Performance Requirements<br />    Safety and Security Requirements <br />    Software Quality Attributes                                                                        | 20 |
| APPENDIX A                                                                                                                                                                                                                       | 21 |
| APPENDIX B                                                                                                                                                                                                                       | 22 |

| REVISIONS |                            |                        |                |
| --------- | :------------------------- | :--------------------- | :------------- |
| Version   | Primary Authority          | Description of Version | Date Completed |
| Draft 1.0 | Aayush Dutta Drishti Joshi | Initial SRS            | 20-02-2024     |

1. # **Introduction**

Bloom is an innovative web application designed to harness social media data for the early identification of mental health issues. Built on the robust MERN stack, Bloom collects real-time data from platforms like Twitter and Facebook, processing vast amounts of unstructured text using advanced natural language processing and machine learning techniques. By analyzing patterns in language and sentiment, the system is able to detect subtle indicators of conditions such as depression and anxiety, and promptly generate alerts for further review by mental health professionals and researchers. This proactive approach not only supports early intervention strategies but also empowers stakeholders with comprehensive, interactive visualizations and detailed reports—making Bloom a vital tool in the modern landscape of mental health care.

   1. ## **Document Purpose**

This document defines the requirements for the “Bloom”. The goal is to develop a web-based application that leverages data mining and machine learning techniques to analyze social media data, extracting early indicators of mental health issues (e.g., depression, anxiety). The system is intended to support mental health researchers, clinicians, and concerned users by providing actionable insights and alerts.

   2. ## **Product Scope**

Bloom is designed as a full-stack web application using the MERN stack (MongoDB, Express.js, React, and Node.js). It will:

* **Ingest Data:** Collect data from social media APIs (e.g., Twitter, Facebook) in real time or via batch processing.
* **Process Data:** Clean and preprocess textual data using NLP techniques.
* **Analyze Data:** Apply data mining and machine learning algorithms (e.g., sentiment analysis, anomaly detection) to identify patterns associated with mental health issues.
* **User Dashboard:** Present analytical results via interactive visualizations, reports, and real-time alerts.
* **User Management:** Support secure user authentication and role-based access for administrators, researchers, and end users.

   3. ## **Intended Audience**

\-	Course Instructor\-	Teaching Assistant\-	Software Development Team

   4. ## **Definitions, Acronyms and Abbreviations**

**MERN Stack:** A JavaScript-based framework including MongoDB, Express.js, React, and Node.js.**NLP:** Natural Language Processing.**UI/UX:** User Interface/User Experience.**API:** Application Programming Interface.**Data Mining:** The process of discovering patterns in large datasets.

   5. ## **Document Conventions**

This document follows IEEE formatting standards. Naming conventions are used for uniformity, and technical terms are defined in Section 1.4.

   6. ## **Reference and Acknowledgements**

**Basic Software Development Toolkit Documentations**

* MERN Stack documentation (MongoDB, Express, React, Node.js).
* Python Machine Learning and NLPTK Libraries

**Research Papers**

* Kim, J., Lee, J., Park, E. *et al.* A deep learning model for detecting mental illness from user content on social media. *Sci Rep* 10, 11846 (2020). [https://doi.org/10.1038/s41598-020-68764-y](https://doi.org/10.1038/s41598-020-68764-y)
* Garg, M. Mental Health Analysis in Social Media Posts: A Survey. *Arch Computat Methods Eng* 30, 1819–1842 (2023). [https://doi.org/10.1007/s11831-022-09863-z](https://doi.org/10.1007/s11831-022-09863-z)
* Wongkoblap A, Vadillo MA, Curcin V. Researching Mental Health Disorders in the Era of Social Media: Systematic Review. J Med Internet Res. 2017 Jun 29;19(6):e228. doi: 10.2196/jmir.7215. PMID: 28663166; PMCID: PMC5509952.
* Rashida, U., Suresh Kumar, K. (2023). Social Media Mining to Detect Mental Health Disorders Using Machine Learning. In: Shakya, S., Du, KL., Ntalianis, K. (eds) Sentiment Analysis and Deep Learning. Advances in Intelligent Systems and Computing, vol 1432\. Springer, Singapore. [https://doi.org/10.1007/978-981-19-5443-6\_68](https://doi.org/10.1007/978-981-19-5443-6_68)

2. # **Overall Description**

   1. # **Product Overview**

Bloom is a standalone web application that integrates with external social media platforms. It will serve as a data aggregation and analysis tool that supports decision-making by mental health professionals and researchers. The system will run on cloud infrastructure and communicate with third-party social media APIs for data collection.

   2. ## **Product Functionality**

**Data Collection Module:**

* Connects to social media APIs.
* Retrieves posts, comments, or tweets based on keywords, hashtags, or user profiles.

**Preprocessing Module:**

* Clean and tokenize text data.
* Remove noise (stop words, duplicates) and normalize text.

**Analytics Engine:**

* Applies NLP and machine learning algorithms to analyze sentiment and detect anomalies.
* Correlates linguistic cues with mental health indicators.

**Alerting System:**

* Generates real-time notifications when potential early signs are detected.

**Dashboard & Reporting:**

* Provides interactive visualizations, charts, and detailed reports.
* Supports exporting data in PDF or CSV formats.

**User Management Module:**

* Implements registration, login, and role-based access control.
* Maintains secure storage of user data in MongoDB.

  3. ## **Design and Implementation Constraints**

**Data Privacy & Compliance:** Must adhere to GDPR, HIPAA (if applicable), and other data protection regulations.

**API Limitations:** Subject to social media API rate limits and data availability.

**Real-Time Processing:** Balancing real-time data ingestion with analysis performance may require careful optimization.

   4. ## **Assumptions and Dependencies**

* Reliable access to social media data and third-party APIs.
* Sufficient computational resources for processing and analysis.
* Continuous updates may be required as API endpoints and social media trends evolve.

3. # **SPECIFIC REQUIREMENTS**

   1. ## **External Interface Requirements**

      1. ### **User Interface**

**UI-1:** The front-end shall be developed using React, providing a responsive design.**UI-2:** Navigation elements, data visualization panels, and alert notifications shall follow standard UI/UX best practices.**UI-3:** Users shall have a clear login, registration, and dashboard interface.

      2. ## **Hardware Interface**

**HI-1:** The system will be hosted on cloud servers (e.g., AWS, Azure) with scalable virtual machines.**HI-2:** The application is designed to run on modern web browsers (Chrome, Firefox, Safari, Edge) and devices (desktop, tablet, mobile).

      3. ## **Software Interface**

**SI-1:** RESTful APIs shall be provided to support communication between the front-end and back-end.**SI-2:** The system will integrate with external social media APIs (Twitter, Facebook) for data collection.**SI-3:** Third-party libraries for NLP (e.g., Natural, TensorFlow.js) shall be integrated into the Node.js environment.

   2. # **Functional Requirement**

      1. ## **Data Collection & Integration**

**FR-1:** The system shall connect to multiple social media APIs to retrieve user posts in real time.**FR-2:** The system shall schedule batch data ingestion for historical analysis.

      2. ## **Data Processing**

**FR-3:** The system shall clean raw text data by removing noise, stop words, and duplicates.**FR-4:** The system shall perform tokenization, stemming, and normalization using NLP libraries.

      3. ## **Data Mining and Analysis**

**FR-5:** The system shall apply sentiment analysis to evaluate the emotional tone of social media posts.**FR-6:** The system shall use machine learning models (e.g., logistic regression, clustering) to detect patterns indicative of mental health issues.**FR-7:** The system shall update its analysis models periodically with new data.

      4. ## **Alert Generation**

**FR-8:** The system shall generate alerts when potential indicators (e.g., high negative sentiment, unusual activity patterns) are detected.**FR-9:** Alerts shall be customizable based on threshold parameters defined by administ

      5. ## **Dashboard and Visualization**

**FR-10:** The system shall present a responsive web-based dashboard built with React.**FR-11:** The dashboard shall display interactive charts, graphs, and reports summarizing the analysis.**FR-12:** Users shall be able to export reports in standard formats (PDF, CSV).

      6. ## **User Authentication and Authorization**

**FR-13:** The system shall provide secure user registration and login.**FR-14:** Role-based access control shall be implemented to differentiate between administrators, researchers, and general users.**FR-15:** The system shall use JWT or a similar mechanism for session management.

      7. ## **Reporting and Data Extraction**

**FR-16:** Users shall be able to generate and download detailed analytical reports.**FR-17:** The system shall log user interactions for audit and research purposes.

   3. # **Use Case Model**

![][image1]

## **Actors**

* **Social Media API:** External data source providing raw social media posts.
* **Mental Health Professional:** Uses the dashboard to view analytics, alerts, and reports.
* **Researcher:** Analyzes data and extracts insights from detailed reports.
* **General User:** Accesses summarized insights and trends via the dashboard.
* **Administrator:** Manages user accounts, configures alert thresholds, and oversees system settings.

## **Use Cases**

### **Use Case \#1 U1: Ingest Social Media Data**

**Author:** Aayush
**Purpose:**
To automatically fetch raw data from social media platforms using API connectors and store it in the database for further analysis.

**Requirements Traceability:**

* SRS – FR-01: Implement API connectors for social media platforms
* SRS – FR-02: Store ingested data in the database

**Priority:** High

**Preconditions:**

* Valid API credentials for accessing social media platforms
* Network connectivity to access external social media APIs

**Post Conditions:**

* Raw social media data is stored in the database
* Logs are updated with the status of data ingestion

**Actors:**

* Social Media API

**Extends:**

* None

**Flow of Events:**

1. **Basic Flow:**

   * The system initiates a scheduled task to connect to social media platforms using API credentials.
   * The system requests new posts or updates from the platforms.
   * The received data is validated for completeness and correctness.
   * Valid data is stored in the database for further processing.
   * The system logs the success of the data ingestion process.
2. **Alternate Flow:**

   * If the API rate limit is exceeded, the system waits for a predefined interval before retrying.
   * If the data format has changed, the system logs an error and alerts the administrator.
3. **Exception Flow:**

   * If the API credentials are invalid or expired, the system logs the error and sends a notification to the administrator.

---

### **Use Case \#2 U2: Process Data**

**Author:** Aayush
**Purpose:**
To clean, tokenize, and preprocess raw social media posts using Natural Language Processing (NLP) techniques, preparing the data for analysis.

**Requirements Traceability:**

* SRS – FR-03: Implement data cleaning and tokenization
* SRS – FR-04: Apply NLP techniques for data preprocessing

**Priority:** High

**Preconditions:**

* Raw social media data is available in the database
* NLP libraries and tools are configured in the system

**Post Conditions:**

* Preprocessed data is stored in the database, ready for analysis
* Logs are updated with the status of data processing

**Actors:**

* System (internal process)

**Extends:**

* None

**Flow of Events:**

1. **Basic Flow:**
   * The system retrieves raw data from the database.
   * Data cleaning is performed to remove irrelevant information (e.g., URLs, special characters).
   * Text is tokenized into individual words or phrases.
   * Stop words are removed, and stemming or lemmatization is applied.
   * The processed data is stored back in the database for analysis.
   * The system logs the success of the data processing task.
2. **Alternate Flow:**
   * If the data contains unsupported characters or encoding issues, the system attempts to standardize the text before processing.
3. **Exception Flow:**
   * If the NLP library encounters an error, the system logs the error and retries the processing. If the error persists, it alerts the administrator.

---

### **Use Case \#3 U3: Analyze Data**

**Author:** Drishti
**Purpose:**
To apply machine learning models to the preprocessed data to determine sentiment scores and detect potential mental health risks.

**Requirements Traceability:**

* SRS – FR-05: Develop and train machine learning models for sentiment analysis
* SRS – FR-06: Implement risk detection algorithms

**Priority:** High

**Preconditions:**

* Preprocessed data is available in the database
* Machine learning models are trained and deployed in the system

**Post Conditions:**

* Analysis results, including sentiment scores and risk assessments, are stored in the database
* Alerts are generated if potential risks are detected
* Logs are updated with the status of data analysis

**Actors:**

* System (internal process)

**Extends:**

* None

**Flow of Events:**

1. **Basic Flow:**
   * The system retrieves preprocessed data from the database.
   * Machine learning models analyze the data to assign sentiment scores.
   * The system evaluates sentiment scores against predefined thresholds to assess potential mental health risks.
   * Analysis results are stored in the database.
   * If risks are detected, the system generates alerts for review.
   * The system logs the completion of the data analysis process.
2. **Alternate Flow:**
   * If the data volume is large, the system processes the data in batches to optimize performance.
3. **Exception Flow:**
   * If the machine learning model fails to process the data, the system logs the error and retries. Persistent issues trigger an alert to the administrator.

---

### **Use Case \#4 U4: Generate Alert**

**Author:** Drishti
To generate alerts when analysis indicates potential mental health risks, prompting further review by professionals.

**Requirements Traceability:**

* SRS – FR-07: Implement alert generation based on analysis results
* SRS – FR-08: Notify relevant users of generated alerts

**Priority:** Medium

**Preconditions:**

* Analysis results indicating potential risks are available
* Alert thresholds are defined in the system

**Post Conditions:**

* Alerts are created and stored in the system
* Notifications are sent to relevant users
* Logs are updated with the status of alert generation

**Actors:**

* System (internal process)

**Extends:**

* None

**Flow of Events:**

1. **Basic Flow:**
   * The system monitors analysis results for indicators exceeding risk thresholds.
   * Upon detecting a potential risk, the system creates an alert with relevant details.
   * The alert is stored in the database and linked to the corresponding data.
   * Notifications are sent to mental health professionals for review.
   * The system logs the creation and notification of the alert.
2. **Alternate Flow:**
   * If the notification system is unavailable, the system queues the alerts and retries sending notifications at regular intervals.
3. **Exception Flow:**
   * If alert generation fails due to data inconsistencies, the system logs the error and alerts the administrator for manual intervention.

---

### **Use Case \#5 U5: View Dashboard**

**Author:** Drishti
**Purpose:**
To provide authenticated users with an interactive dashboard that displays aggregated analytics, real-time alerts, and detailed reports derived from the social media data analysis, facilitating informed decision-making.

**Requirements Traceability:**

* SRS – FR-10: Develop a user-friendly dashboard interface
* SRS – FR-11: Display real-time analytics and alerts
* SRS – FR-12: Provide access to detailed reports

**Priority:** High

**Preconditions:**

* The user must be authenticated and authorized (role: mental health professional, researcher, or general user).
* Relevant analytics data and alerts must be available in the system.

**Post Conditions:**

* The dashboard displays the latest analytics, charts, and alerts.
* User interactions (e.g., filtering, zooming, exporting) are recorded for auditing.

**Actors:**

* Mental Health Professional
* Researcher
* General User

**Extends:**

* U2: User Authentication (ensuring the user is logged in before accessing the dashboard)

**Flow of Events:**

1. **Basic Flow:**
   * The user logs in with valid credentials.
   * The user navigates to the dashboard section.
   * The system retrieves the latest analytics data and alert information from the database.
   * The dashboard renders interactive visualizations (charts, graphs, tables) and displays current alerts.
   * The user interacts with the dashboard (e.g., applies filters, views detailed data).
2. **Alternate Flow:**
   * If data retrieval fails, the system displays an error message with an option to retry loading the dashboard.
3. **Exception Flow:**
   * If the user’s session expires during use, the system prompts for re-authentication and attempts to restore the last dashboard state.

---

### **Use Case \#6 U6: Export Reports**

**Author:** Aayush
**Purpose:**
To enable authorized users (mental health professionals and researchers) to export detailed analytical reports in various formats (e.g., PDF, CSV) for offline analysis and record-keeping.

**Requirements Traceability:**

* SRS – FR-16: Provide functionality to generate and export reports
* SRS – FR-17: Support multiple export formats (PDF, CSV)

**Priority:** Medium

**Preconditions:**

* The user is authenticated and has sufficient permissions (admin, mental health professional, or researcher).
* Analytical report data is available in the system.

**Post Conditions:**

* The selected report is exported in the chosen format and is available for download or sent via email.
* The export action is logged for auditing purposes.

**Actors:**

* Mental Health Professional
* Researcher

**Extends:**

* U5: View Dashboard (as the export function is accessed via the dashboard)

**Flow of Events:**

1. **Basic Flow:**
   * The user navigates to the reports section from the dashboard.
   * The user selects a report and chooses an export format (e.g., PDF or CSV).
   * The system retrieves the corresponding report data from the database.
   * The system formats the report into the selected file type.
   * The report is made available for download, and a confirmation message is shown.
2. **Alternate Flow:**
   * If the export process encounters an error, the system displays an error message and logs the failure.
3. **Exception Flow:**
   * If the user lacks sufficient permissions to export reports, the system denies the request and instructs the user to contact the administrator.

---

### **Use Case \#7 U7: Manage User Accounts**

**Author:** Aayush
**Purpose:**
To allow the system administrator to create, update, and delete user accounts, and manage role-based access control to ensure proper authorization across the application.

**Requirements Traceability:**

* SRS – FR-13: Provide secure user registration and login
* SRS – FR-14: Implement role-based access control
* SRS – FR-15: Enable administrative account management functions

**Priority:** High

**Preconditions:**

* The administrator is authenticated and holds admin privileges.
* The system is fully operational with database connectivity.

**Post Conditions:**

* User account information is updated in the database (creation, modification, or deletion).
* All changes are logged for security and auditing.
* Appropriate notifications are sent if needed.

**Actors:**

* Administrator

**Extends:**

* None

**Flow of Events:**

1. **Basic Flow:**

   * The administrator logs into the system using admin credentials.
   * The administrator navigates to the user management section.
   * The administrator selects an action (create, update, or delete a user account).
   * The administrator enters or modifies the required user details (e.g., name, email, role).
   * The system validates the input and updates the user data in MongoDB.
   * The system confirms the successful update and logs the changes.
2. **Alternate Flow:**

   * If the administrator attempts to create a user with an existing email, the system displays an error message and requests correction.
3. **Exception Flow:**

   * If the system encounters a database error during account updates, the error is logged, and the administrator is notified to retry later.
4. # **Other Non-Functional Requirements**


   1. # **Performance Requirement**

**NFR-1:** The system shall process and update analysis results with a latency of less than 2 seconds for most operations.**NFR-2:** The system shall handle large volumes of data efficiently, supporting scalability to millions of data points.

2. # **Safety and Security Requirements**

**NFR-3:** All data transmissions shall be encrypted using HTTPS.**NFR-4:** Sensitive data stored in the database shall be encrypted.**NFR-5:** The system shall enforce strict authentication and authorization protocols.

3. # **Software Quality Attributes**

**NFR-6:** The system shall be designed to scale horizontally to accommodate increasing loads.
**NFR-7:** The application shall have a 99.5% uptime guarantee and include mechanisms for failover and backup.
**NFR-8:** The user interface shall be intuitive and accessible on desktops, tablets, and smartphones.
**NFR-9:** The system shall include contextual help and documentation for all major functions.
**NFR-10:** The codebase shall be modular, documented, and version-controlled.
**NFR-11:** The system shall support easy updates and integration of new algorithms or features.

# **APPENDIX A**

# **Glossary**

* **Alert:** A notification generated when potential early signs of mental health issues are detected.
* **Data Mining:** The automated process of extracting patterns from large datasets.
* **Digital Phenotyping:** The moment-by-moment quantification of an individual’s behavior using data from digital devices.
* **JWT:** JSON Web Token, a secure way to transmit information for session management.

# **Future Aspect**

* Integration with additional social media platforms as APIs evolve.
* Expansion of analytical models to include image and video analysis for richer data insights.
* Continuous improvement of machine learning models via user feedback and additional labeled data.

# **APPENDIX B**

# **Data Dictionaries**

1. ## **User Collection**

| Field Name       | Data Type | Description                                             |
| ---------------- | --------- | ------------------------------------------------------- |
| `userId`       | String    | Unique identifier for each user (e.g., a UUID).         |
| `name`         | String    | Full name of the user.                                  |
| `email`        | String    | User’s email address; must be unique.                  |
| `passwordHash` | String    | Hashed password for secure authentication.              |
| `role`         | String    | Role of the user (e.g., "admin", "researcher", "user"). |
| `createdAt`    | Date      | Timestamp when the user account was created.            |
| `updatedAt`    | Date      | Timestamp for the last update to the user's profile.    |

2. ## **SocialMediaPosts Collection (Raw Posts)**

| Field Name     | Data Type | Description                                                   |
| -------------- | --------- | ------------------------------------------------------------- |
| `postId`     | String    | Unique identifier for each post.                              |
| `platform`   | String    | Social media platform (e.g., "Twitter", "Facebook").          |
| `userHandle` | String    | The original poster's handle or username.                     |
| `content`    | String    | The full text content of the post.                            |
| `postDate`   | Date      | The original date/time when the post was published.           |
| `rawJSON`    | Mixed     | The complete JSON payload received from the social media API. |
| `fetchedAt`  | Date      | Timestamp when the post was retrieved by the system.          |
| `language`   | String    | Language of the post content (if available).                  |
| `location`   | String    | Geographical location associated with the post (optional).    |

3. ## **ProcessedPosts Collection**

| Field Name             | Data Type       | Description                                                               |
| ---------------------- | --------------- | ------------------------------------------------------------------------- |
| `processedPostId`    | String          | Unique identifier for the processed record.                               |
| `originalPostId`     | String          | Reference to the corresponding `postId` in SocialMediaPosts.            |
| `tokens`             | Array\[String\] | Tokenized words extracted from the content.                               |
| `sentimentScore`     | Number          | Computed sentiment score (e.g., range\-1 \[negative\] to 1 \[positive\]). |
| `extractedKeywords`  | Array\[String\] | List of keywords identified during text analysis.                         |
| `analyzedAt`         | Date            | Timestamp when the post was processed and analyzed.                       |
| `additionalFeatures` | Object          | Optional object to store other extracted features (e.g., emotion tags).   |

4. ## **AnalyticsResults Collection**

| Field Name         | Data Type | Description                                                         |
| ------------------ | --------- | ------------------------------------------------------------------- |
| `resultId`       | String    | Unique identifier for each analytics result.                        |
| `analysisType`   | String    | Type of analysis (e.g., "sentiment", "trend", "anomaly detection"). |
| `aggregatedData` | Object    | Aggregated results (e.g., average sentiment per day, trend lines).  |
| `details`        | String    | Optional detailed description of the analysis outcome.              |
| `generatedAt`    | Date      | Timestamp when the analytics result was generated.                  |

5. ## **Alerts Collection**

| Field Name      | Data Type | Description                                                  |
| --------------- | --------- | ------------------------------------------------------------ |
| `alertId`     | String    | Unique identifier for each alert.                            |
| `triggeredBy` | String    | Source that triggered the alert (e.g., "Analytics Engine").  |
| `alertType`   | String    | Type of alert (e.g., "risk", "warning", "info").             |
| `description` | String    | A brief description of what the alert indicates.             |
| `severity`    | String    | Severity level (e.g., "low", "medium", "high").              |
| `status`      | String    | Current status (e.g., "active", "acknowledged", "resolved"). |
| `createdAt`   | Date      | Timestamp when the alert was generated.                      |
| `updatedAt`   | Date      | Timestamp for the latest status update.                      |

6. ## **Reports Collection**

| Field Name       | Data Type     | Description                                                         |
| ---------------- | ------------- | ------------------------------------------------------------------- |
| `reportId`     | String        | Unique identifier for each report.                                  |
| `generatedBy`  | String        | Identifier for the user or process that generated the report.       |
| `content`      | String/Object | Report content, which can be a text summary or a structured object. |
| `exportFormat` | String        | Format of the report (e.g., "PDF", "CSV").                          |
| `generatedAt`  | Date          | Timestamp when the report was generated.                            |

7. ## **SystemLogs Collection**

| Field Name         | Data Type | Description                                                          |
| ------------------ | --------- | -------------------------------------------------------------------- |
| `logId`          | String    | Unique identifier for each log entry.                                |
| `module`         | String    | Name of the module or service (e.g., "Ingestion", "Analytics").      |
| `logType`        | String    | Type of log (e.g., "error", "info", "warning").                      |
| `message`        | String    | Detailed log message describing the event or error.                  |
| `timestamp`      | Date      | Timestamp when the log was recorded.                                 |
| `additionalData` | Object    | Optional field for storing extra details (e.g., error stack traces). |

[image1]: data:image/png;base64,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QEVklwvZsu0DAGitdnzw2s96ZEjtYRuoiOxyIVu2fQAArdWOD177Wd+lpUuXuqAxbdo0Oyg+9dRT40GDBsUbNmywg3Jl9uzZ8apVq2y1m/csab3aBioiu1y1fOpTn3LLvGTJknjlypXxyJEj42XLlsUHDhywo3bLF77whfjTn/60m6baOut2HTVqVDx48OD4ueeeq6jXNlhtO+yK9r1q+18ttn0AAK3Vjg9e+1nfJR/ghg0bZge5AyUB7vBpvdoGKiK7XNXs27fPLe9Xv/rVtO7NN9+M+/btG99///3BmN137rnnxps2bbLVmenXr1/85S9/Ob7lllsq6glwANCZ2vHBaz/ru+QD3IQJE+J33303rd+1a1c8f/78igD3/vvvxx/60Ifc+DowP/74465+9+7dLkS98MILPrS4x95jjz0W9+/f39VPnDix4oD+s5/9zE1Lw3784x+7A5mmJ2+99ZYLlnrtnDlz0tdYjQQ4zcPkyZPd+1x99dXxnj170mH33XdfOt9+mUSvf/DBB139Sy+9lNY3qjzNwrPLVc2MGTPitWvX2ur4k5/8ZHzmmWemz++66650XatNfO+cX9dHH320G7ZgwQJXr3b1448dO7aiB07b4x133OGGaTu599570+3AhiJtw9rW/bBvfvOb8cCBA+Prrrsu3r9/v5sX/z7aPmv1Gj755JPxZZdd5ob36dMnXr16dTrMBjhts9p2NW/h9qZl0Lzqvc4///z0fVXfiHKzAADapB0fvPazvks+wD3yyCPx8uXL0/prr7023rp1axrg1ANy0kknxXv37k3H0etuvPFGF7j0WKfLwmGiEKbQ5j366KOuB0NmzpxZEbLmzp2bBjgdwHWA9J566ik3vg62VlcBTgfbMWPGpL04F110UTpPDz/8sDsge1OnTnXjipZh+vTp6bDu0uvDxikqu1zVaF374F3LihUrXBt7OkU/YsQI91ivD3uBtd5ffPFF91jbxObNm93jMMANGDCgou30+kYDXBi8nn/+edfunqapaVejedZ+4R/7bUXCAHfeeee5bdbTtqx9SrQMYe+dndeu2PYBALRWOz547Wd9l3yA00HJByQdiHVAUfCpdwpVw/R6ja/rgl577bV0mHo3qtGBWD0pcuSRR7qeG0/XFPkAN27cuIqDmubLvofXSIDT4/Cg7et1sA6XTyHWr0f9r+u5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WqYYAW7AgAHxk08+aasPy+zZs+OxY8fa6qbbsGGDP6i50r9//3jKlCnx+++/b0etau/evfG//Mu/2OrCqNjMUI9ddYWk5bALBgBomfwHuK1bt8bnnHNOPH78ePe4p9oZ4KZNmxbv3r07rduyZYs70N1www3BmNUtXbrUTaOozIaG2uyq6xZtz562l82bNwdD20fLYRcMANAy+Q9wq1evjm+55RZ3gFixYoUd3G1ZBjgZPXp0PGbMmIq6aghwvYZddd1CgAOAXinfAe711193YUenE88999x40KBB6TAFo3HjxsUjRoxwwU6nKPXY03Ldeuut8cqVK+OhQ4fGffv2dfU+wB04cCCeN29evHbt2vQ16uWbPn16/JOf/MSNc9NNN8WXXHKJm9aOHTvca9R75oeddNJJ8bJly1y9VSvALV++3E1PvvCFL7jHd955Zzx37ly3DM8//3y8f//+eNasWS7Eff/7349ffPHFeNSoUfGf//mfu2WaOHFivGDBgqrvmxfhVoa67KrrlmoBbtWqVW67u+CCC1ydtlfVaVzV67H/40B1eo221Z7QctgFAwC0TL4DXBh2wseiA5GeK0CJ76WTt956y4Uc79FHH4379evnHoc9cOrdW7RoUTpenz594ttvvz1esmRJvH79elenkHTNNdfETzzxhAtXCom7du1yw/bt21fz+rxaAU4HTz+fCoA6Pezddddd8Y033ugehz1wCo2DBw9Ox1OYPPbYY5tySrlVgo0M9dlV1y31Apyn7V314XDfUxe+vie0HHbBAAAtk+8AN2zYMNcjJuqVmjlzZvzQQw+55zpATZgwId6+fbt7roNT2EOn4PX3f//3rsfqqKOOSkOTPYXqg53CkKav91EPnMZXj5gOdnv27Elfq/HVq+fLwIED4xkzZqTT8xoJcKKbGlSn3hKFNAU3qXYKdd26dfFVV13lwqk/KOdVxWaGeuyq6xa/vUgYzETbn+rsdmgDnl7z4Q9/OH1+OLQcdsHa4LeS8ifBcz3+efmx/h8d1PuyplwX0ninBM/12quD50Wi5fjn8v+elidcT12x6zWk6f7C1D1brve07jSNRvnx9Z76X8/XhCMENHxN8Fxt12hbNTpeK2g+/baZJ5ovtV/4vB3r6e5yweHLb4BTL5d6t3QqUacXVS677DIX6p577jl3AAoPTGGA27Ztmztlqv8V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
