# 🛋 Advanced Shell Scripting - Pokémon API Automation

This project demonstrates advanced shell scripting techniques by automating API requests to the [PokéAPI](https://pokeapi.co/), extracting and processing data, implementing error handling and retries, and performing parallel data fetching.

## 🗂 Directory Structure

```
Advanced_shell/
├── apiAutomation-0x00             # Task 0: Single API Request
├── data_extraction_automation-0x01 # Task 1: Data Extraction & Formatting
├── batchProcessing-0x02           # Task 2 & 4: Batch Data Fetching + Error Handling
├── summaryData-0x03               # Task 3: Summary CSV Generation
├── batchProcessing-0x04           # Task 5: Parallel Fetching
```

---

## 📌 Tasks

### ✅ 0. API Request Automation

**Objective:**
Make a request to the PokéAPI for **Pikachu** and save the response.

* Output saved in: `data.json`
* Errors saved in: `errors.txt`
* Tool: `curl`

**Example:**

```bash
./apiAutomation-0x00
```

---

### ✅ 1. Extract Pokémon Data

**Objective:**
Parse the JSON file and display Pikachu’s basic info using `jq`, `awk`, and `sed`.

**Expected Output:**

```bash
Pikachu is of type Electric, weighs 6kg, and is 0.4m tall.
```

**Run:**

```bash
./data_extraction_automation-0x01
```

---

### ✅ 2. Batch Pokémon Data Retrieval

**Objective:**
Loop over a Pokémon list and fetch each one’s data into its own JSON file.

* Pokémon: `Bulbasaur`, `Ivysaur`, `Venusaur`, `Charmander`, `Charmeleon`
* Output directory: `pokemon_data/`
* Delay used to avoid rate-limiting.

**Run:**

```bash
./batchProcessing-0x02
```

---

### ✅ 3. Summarize Pokémon Data

**Objective:**
Read all JSON files from `pokemon_data/`, extract name/height/weight, and generate a summary CSV file.

**Output:**

* CSV: `pokemon_report.csv`
* Average height & weight calculated using `awk`.

**Run:**

```bash
./summaryData-0x03
```

---

### ✅ 4. Error Handling and Retry Logic

**Objective:**
Enhance Task 2 by implementing retry logic:

* Retry failed API requests up to 3 times.
* Log failed attempts to `errors.txt`.

**Included in:** `batchProcessing-0x02`

---

### ✅ 5. Parallel Data Fetching

**Objective:**
Speed up batch fetching using background processes.

* All Pokémon fetched in parallel.
* Script waits for all processes using `wait`.

**Run:**

```bash
./batchProcessing-0x04
```

---

## 🔧 Tools & Commands Used

* `curl` – for HTTP requests
* `jq` – for JSON parsing
* `awk`, `sed` – for text formatting
* `bash` – for scripting
* `sleep`, `wait`, `&` – for process control

---

## 📁 Requirements

* Bash 4+
* jq
* curl
* POSIX-compliant tools

Install on Ubuntu/Debian:

```bash
sudo apt update
sudo apt install jq curl
```

---

## 👨‍💼 Author

Made with ❤️ by [Marwa hamed](https://github.com/MARWAHAMED629)
