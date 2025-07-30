# 🔧 DigiKey Component Lookup Tool

This Python tool lets you search electronic components via the DigiKey API, view detailed info, and export search results.

A stylish and robust Python CLI tool to search electronic components from the DigiKey API, view detailed specs, and export results to file — ideal for engineers, makers, and hobbyists.

Please read the setup instructions fully!
---

## ✨ Features

- 🔎 Search DigiKey components by part name or number  
- 📦 Displays availability, manufacturer, datasheet, category, family, pricing, etc.  
- 📤 Export results to `.csv` or `.xlsx`  
- 📊 Built-in analytics: average stock, manufacturer breakdown  
- 🎨 Styled terminal output (colored for readability)  
- 🪵 Errors logged to `errors.log`  
- 🔄 Automatically installs missing dependencies on first run  
- ✅ Works with Python 3.11+  
- 🔐 Uses `.env` to safely store your DigiKey credentials

---

## 📦 Setup Instructions

### 1. 📥 Clone the repository

```bash
git clone https://github.com/YourUsername/DigiKey-Component-Lookup-Tool.git
cd DigiKey-Component-Lookup-Tool
```

### 2. 🐍 Set up Python virtual environment

```bash
python -m venv venv
```

Activate it:

- **Windows PowerShell:**
```bash
.\venv\Scripts\Activate.ps1
```

- **Mac/Linux:**
```bash
source venv/bin/activate
```

### 3. 📜 Install dependencies

You can manually install all required packages with:

```bash
pip install -r requirements.txt
```

Or simply run:

```bash
python digikey_lookup.py
```

The script will automatically install missing dependencies on first run.

---

## 🔑 DigiKey API Setup

1. Create a free account at [DigiKey Developer Portal](https://developer.digikey.com/)
2. Register an app to get:
   - `DIGIKEY_CLIENT_ID`
   - `DIGIKEY_CLIENT_SECRET`
3. Rename `.env.example` to `.env` and edit the file:

```
DIGIKEY_CLIENT_ID=your_client_id_here
DIGIKEY_CLIENT_SECRET=your_client_secret_here
```

> ✅ Your `.env` is ignored by Git for security. Never upload it to GitHub.

---

## 🚀 Run the Tool

After activating your virtual environment and editing your `.env` file:

```bash
python digikey_lookup.py
```

On first run, a browser will open for DigiKey login and authorization.  
> ⚠️ If the browser shows a warning (e.g., "not private"), you can **safely proceed** — it's part of DigiKey's localhost-based OAuth login.

---

## 🛠️ Example Workflow

```bash
Enter part name or number (or 'q' to quit): atmega328pu
```

- View a list of matching results
- Choose the part number to see full details
- Choose to export (single or all results)
- Save as `.csv` or `.xlsx`
- View analytics:
  - 📊 Average quantity available
  - 🔢 Parts per manufacturer

---

## 📂 Project Structure

```
DigiKey-Component-Lookup-Tool/
├── digikey_lookup.py       # Main script
├── .env.example            # Environment variable template
├── requirements.txt        # All Python dependencies
├── errors.log              # Automatically generated error log
├── README.md               # Full project documentation
└── .gitignore              # Hides venv, .env, etc.
```

---

## 🔒 Security Advice

- Keep your real `.env` file private.
- Do **not** share your DigiKey credentials — even via GitHub.
- Encourage users to generate their own credentials.
- You can include a **video tutorial** showing how to get these keys.

---

## 🧠 Tips for Users

- Python 3.11+ is recommended (script was developed on 3.11.9).
- If you get a `distutils` error, run:

```bash
pip install setuptools
```

- If you get a `ModuleNotFoundError`, try:

```bash
pip install python-dotenv digikey-api pandas openpyxl tabulate
```

---

## 🙏 Credits & Acknowledgements

Thanks to the following resources and tools:

- [DigiKey Developer API](https://developer.digikey.com/)
- [Digikey-API Python Package](https://pypi.org/project/digikey-api/)
- [HurricaneJoef's DigiKey API Example Repo](https://github.com/hurricaneJoef/digikey-api)
- [Pandas](https://pandas.pydata.org/)
- [OpenPyXL](https://openpyxl.readthedocs.io/)
- [python-dotenv](https://pypi.org/project/python-dotenv/)
- [Tabulate](https://pypi.org/project/tabulate/)
- Everyone on Stack Overflow and GitHub whose solutions helped refine this tool!

---

## 📣 Contributing

Found a bug or want to improve the tool? Contributions are welcome!  
Please open an issue or submit a pull request.

---

## 📜 License

MIT License — free for personal and educational use.
