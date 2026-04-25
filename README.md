💻 Laptop Price Predictor

A Machine Learning web application that predicts laptop prices based on user-provided specifications. This project is built using Python, Flask, and Scikit-Learn and can be deployed on platforms like Render or Heroku.

🚀 Live Demo  
(Add your deployment link here)

🛠️ Features  
- Predicts laptop prices using Machine Learning  
- Uses Random Forest Regressor (~81% accuracy)  
- Simple and responsive UI  
- Data preprocessing and feature engineering  
- API support for external usage  
- Ready for deployment  

📊 Dataset  
The model is trained on a dataset containing:
- Company (Brand)  
- Type (Notebook, Gaming, etc.)  
- RAM (GB)  
- Weight (kg)  
- Screen features (IPS, Touchscreen)  
- CPU & GPU  
- Operating System  

🧠 Model Information  
- Algorithm: Random Forest Regressor  
- Target: Laptop Price  
- Accuracy: ~0.81 (R2 Score)  
- Preprocessing: One-Hot Encoding + Numeric conversion  

📁 Project Structure  
```text
LaptopPricePrediction/
│
├── data/
│   └── laptop_data.csv      # Raw dataset
├── model/
│   ├── laptop_model.pkl     # Trained ML Pipeline
│   └── df.pkl               # Processed dataframe for UI dropdowns
├── static/
│   └── style.css            # Custom styling
├── templates/
│   └── index.html           # Main UI template
├── app.py                   # Flask Backend & API
├── preprocess.py            # Data cleaning & Model training script
├── requirements.txt         # Python dependencies
├── Procfile                 # Deployment instructions
└── runtime.txt              # Python version for deployment
```

---

## ⚙️ Local Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/KaustubhDhumale/Laptop-Price-Prediction.git
   cd Laptop_Price_Prediction
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Train the model (Optional - files are already included):**
   ```bash
   python3 preprocess.py
   ```

4. **Run the app:**
   ```bash
   python app.py
   ```
   Open `http://127.0.0.1:5000` in your browser.

---

## 🌐 API Endpoint
- **URL:** `/api/predict`
- **Method:** `POST`
- **Payload Example:**
  ```json
  {
    "company": "Dell",
    "type": "Notebook",
    "ram": 8,
    "weight": 1.9,
    "touchscreen": 0,
    "ips": 1,
    "cpu": "Intel",
    "gpu": "Nvidia",
    "os": "Windows 10"
  }
  ```

---

## 🚀 Deployment (Render.com)
1. Create a new **Web Service** on Render.
2. Connect your GitHub repository.
3. **Build Command:** `pip install -r requirements.txt`
4. **Start Command:** `gunicorn app:app`

---

## 👤 Author
**Kaustubh Dhumale**
- GitHub:  https://github.com/KaustubhDhumale
