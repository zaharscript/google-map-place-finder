# 🌍 Google Map Place Finder

A full-stack web application that allows users to search for locations using **Nominatim (OpenStreetMap)**. It returns detailed place information (name, address, latitude, longitude, type), and allows export to **CSV** and **Excel** files. Built with **React** on the frontend and **Flask** on the backend.

> 🚀 Live Demo: [https://stunning-gecko-e0aada.netlify.app](https://stunning-gecko-e0aada.netlify.app)

---

## 📁 Project Structure

google-map-place-finder/
├── backend/ # Flask + Nominatim API logic + export logic
├── frontend/ # React app for user interface and results
├── README.md

---

## ⚙️ Tech Stack

### Frontend:

- React
- Tailwind CSS
- Axios
- Vite

### Backend:

- Python
- Flask
- Flask-RESTful
- Flask-CORS
- Pandas
- Requests

### APIs:

- Nominatim API (OpenStreetMap)
- [Google Places API](https://developers.google.com/maps/documentation/places/web-service/overview) _(optional – not currently enabled)_

---

## ✨ Features

- 🔍 Place search via keyword (e.g., "cafe in Kuala Lumpur")
- 📄 Results show name, address, coordinates, type
- 📤 Export results to CSV or Excel
- 🧼 Cleans Arabic characters for standardized formatting
- 🌐 Responsive design for mobile, tablet, and desktop
- 🔐 Future-ready with optional Google API integration

---

## 📦 Getting Started (Local Development)

### 1. Clone the Main Repository

````bash
git clone --recurse-submodules https://github.com/zaharscript/google-map-place-finder.git
cd google-map-place-finder

2. Backend Setup (Flask)

cd backend
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt

# Run server
python app.py

Flask will run on: http://127.0.0.1:5000


3. Frontend Setup (React + Vite)
```bash
cd ../frontend
npm install

Create .env file inside frontend/ folder:
```env
REACT_APP_API_BASE_URL=http://127.0.0.1:5000

Then run:
```bash
npm run dev


React app will be served at: http://localhost:5173

☁️ Deployment
Frontend:
Hosted on Netlify

Build Command: npm run build

Publish Directory: dist/

Backend:
Hosted on Render.com

Startup Command: gunicorn app:app

Add /search and /download/<csv|excel> endpoints

📁 Data Exports
After each search, two files are generated inside the backend's exports/ folder:

places.csv – Standard CSV file

places.xlsx – Excel-compatible file with all results

These files can be downloaded from the frontend directly.

🔐 Optional Google API Integration (Not Enabled)
You may optionally enhance accuracy by falling back to Google Places API when Nominatim returns no results. Contact Google Cloud for API key & pricing.


📸 Screenshots
Search Interface	Results Table

🧑‍💻 Author
Zahar Mokhtar
GitHub: @zaharscript
Location: Malaysia 🇲🇾


📄 License
This project is open source and available under the MIT License.



````
