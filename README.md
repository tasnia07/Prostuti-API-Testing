# Prostuti-API-Testing

This repository contains the automated API testing suite built using **Postman** and **Newman** to validate registration inputs, multi-field error exception boundaries, and operational payload constraints.

---

## Prerequisites

Before running the test suite, ensure you have the following tools installed on your local environment:

* **Node.js** (v16.x or higher) -> [Download Node.js](https://nodejs.org/)
* **Postman Desktop App** (Optional, for visual debugging) -> [Download Postman](https://www.postman.com/)

---

## Installation & Setup

1. **Clone or extract** this project directory onto your machine.
2. Open your terminal in the project root folder and install **Newman** globally:
   ```bash
   npm install -g newman

---

## How to Run the Test Suite

### Step 1: Running via Postman App (UI View)
1. Launch the **Postman** application.
2. Click on the **Import** button in the top-left corner.
3. Select and upload the exported JSON collection file (`Prostuti.postman_collection.json`).
4. Click **Import** again to upload your environment variable file (`Prostuti.postman_environment.json`).
5. In the top-right corner of Postman, ensure you select your newly imported environment from the environment dropdown menu.
6. Select the Prostuti collection folder in your sidebar, click **Run Collection** and keep the iteration=1.

### Step 2: Running via CLI (Command Line Interface)
To run the entire test suite instantly from your terminal, execute the following command in your project root directory:

```bash
newman run Prostuti.postman_collection.json -e Prostuti.postman_environment.json -r cli,htmlextra
