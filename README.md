# Customer Purchase Prediction API

This project is a Machine Learning application designed to predict the likelihood of a customer making a purchase based on their browsing behavior and history. It features a **FastAPI** backend that serves a trained **Scikit-learn** model, complete with a web interface for manual testing.

## 🚀 Features

- **Real-time Prediction:** Calculate purchase probability instantly.
- **Feature Engineering:** Automatically calculates `recency_score` and `engagement_score` internally before prediction.
- **REST API:** Exposes endpoints for programmatic access.
- **Web Interface:** User-friendly HTML form to input customer data and view results.
- **Model Integration:** seamless integration with a pre-trained `.pkl` model using Joblib.

## 📂 Project Structure

```text
CUSTOMER-PURCHASE-PREDICTION/
├── app/
│   ├── models/
│   │   └── prediction.py    # Pydantic models for request/response
│   ├── services/
│   │   └── predictor.py     # Business logic & Feature engineering
│   ├── static/
│   │   ├── css/
│   │   └── js/
│   ├── templates/           # Jinja2 HTML templates
│   └── main.py              # FastAPI application entry point
├── downloaded_model/
│   └── purchase_prediction_model.pkl  # Trained ML model
├── venv/                    # Virtual environment
├── .gitignore
├── Customer_Purchase_Prediction_....ipynb # Training notebook
├── requirements.txt
└── README.md
🛠️ Installation
Clone the repository:

Bash
git clone [https://github.com/your-username/Customer-Purchase-Prediction.git](https://github.com/your-username/Customer-Purchase-Prediction.git)
cd Customer-Purchase-Prediction
Create and activate a virtual environment:

Bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
Install dependencies:

Bash
pip install -r requirements.txt
Note: Ensure requirements.txt includes fastapi, uvicorn, pydantic, pandas, scikit-learn, joblib, jinja2, and python-multipart.

▶️ Usage
To start the server, run the following command from the project root:

Bash
uvicorn app.main:app --reload
The server will start at http://127.0.0.1:8000.
![Project Structure](screenshots/project_structure.png)

![AWS S3 Organization](screenshots/s3_organization.png)
