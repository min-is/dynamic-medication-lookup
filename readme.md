<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

## Medication Lookup Application

### Overview

This project is a web-based **medication lookup tool** designed to help healthcare providers and patients identify medications, even when the exact spelling or full name is unknown. By combining fuzzy search logic, a modern and accessible UI, and robust backend APIs, the application directly addresses the challenge of medication name uncertainty in clinical and patient settings.

---

## Background

Medication errors and confusion often arise from misspelled or partially remembered drug names. This tool was personally built to empower both clinicians and patients to quickly and safely look up medications, including those with complex names or common misspellings, thereby reducing risk and improving healthcare outcomes.

---

## Features

- **Fuzzy Search \& Suggestions**
    - Supports partial matches and misspellings using advanced string matching (Python backend with `fuzzywuzzy`)[^3].
    - Returns top suggestions in real-time as the user types, highlighting the matched portion of the name[^4].
    - Matches against both primary and alternate medication names, increasing accuracy and usability[^3][^7].
- **Detailed Medication Information**
    - Displays a clear overview, alternate names, and mechanism of action for each medication[^4][^7].
    - Data is sourced from a comprehensive, structured JSON file containing clinical-grade medication information[^7].
- **Modern, Accessible UI**
    - Responsive, dark-themed design with custom fonts and accessibility considerations[^5].
    - Instant feedback and error handling for empty queries or missing data[^4][^5].
- **RESTful API**
    - `/suggestions`: Returns a list of matching medication names based on user input[^2][^3].
    - `/medication/:name`: Returns detailed information for a selected medication[^2][^3].
- **Cross-Stack Implementation**
    - Includes both a Node.js (Express)[^2] and Python (Flask)[^3] backend, showcasing versatility and adaptability.

---

## Methods \& Code Highlights

| Aspect | Implementation Details |
| :-- | :-- |
| **Fuzzy Search** | Python backend uses `fuzzywuzzy` for typo-tolerant and partial string matching[^3] |
| **API Design** | Clean RESTful endpoints for suggestions and medication details[^2][^3] |
| **Frontend Dynamics** | Real-time, debounced search suggestions and detailed result rendering in JS[^4] |
| **UI/UX Design** | Dark mode, responsive CSS, custom font integration, and animation effects[^5] |
| **Error Handling** | Graceful handling of missing data and user errors at both backend and frontend[^2][^4] |
| **Alternate Names** | Search and display logic fully supports alternate and generic names[^3][^4][^7] |


---

## Impact

- **Reduces Medication Errors:** Enables users to find medications even with incomplete or incorrect spellings, reducing the risk of errors in prescribing or self-administration.
- **Empowers Patients:** Patients can independently look up medications, improving their understanding and engagement in their own care.
- **Supports Healthcare Providers:** Clinicians can quickly verify drug names and details, streamlining workflow and improving safety.

---

## Getting Started

### Prerequisites

- **Node.js** (for Express backend) or **Python 3** (for Flask backend)
- `medications.json` file in the project directory[^7].


### Install \& Run (Node.js)

```bash
npm install
npm start
```


### Install \& Run (Python)

```bash
pip install flask fuzzywuzzy
python app.py
```


### Usage

1. Open `index.html` in your browser.
2. Start typing a medication name. Suggestions will appear instantly.
3. Click a suggestion to view detailed information.

---

## File Structure

```
.
├── index.html        # Main web UI
├── script.js         # Frontend logic for search and display
├── style.css         # Modern, accessible styles
├── medications.json  # Structured medication data
├── server.js         # Node.js backend (Express)
├── app.py            # Python backend (Flask + fuzzy search)
```


---

## Example: Medication Data Structure

```json
{
  "name": "Abilify",
  "description": "Abilify (aripiprazole) is an atypical antipsychotic...",
  "alternate_names": ["aripiprazole", "Abilify Maintena", "Aristada"],
  "mechanism_of_action": "Acts as a partial agonist at dopamine D2 receptors..."
}
```


---

## Showcased Skills

- Full-stack web development (Node.js, Python, HTML, CSS, JS)
- Advanced fuzzy search and string matching
- RESTful API design
- Responsive, accessible UI/UX
- Robust error handling and user feedback
- Real-world healthcare application focus

---

## License

This project is provided for educational and demonstration purposes.

---

**Built by [Your Name] to support safer, smarter healthcare.**

<div style="text-align: center">⁂</div>

[^1]: package.json

[^2]: server.js

[^3]: app.py

[^4]: script.js

[^5]: style.css

[^6]: index.html

[^7]: medications.json

