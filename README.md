# SavR: Save and Savour

## SavR - Food Waste Management System

### Overview
SavR is a comprehensive food waste management system designed to bridge the gap between mass food waste producers and consumers. The platform aims to reduce food wastage by allowing producers to offer surplus food to consumers at negotiable charges. This system not only helps in minimizing food waste but also contributes to reducing the carbon footprint associated with food disposal.

### Problem Being Solved
Food wastage is a significant global issue, with millions of tons of food being discarded every year. This not only leads to economic losses but also has severe environmental impacts, including increased greenhouse gas emissions. SavR addresses this problem by providing a platform where food waste can be efficiently redistributed from producers to consumers, thereby reducing waste and promoting sustainability.

### Features
- **User Authentication**: Secure login and profile management using Auth0.
- **Data Visualization**: Interactive dashboards to visualize carbon footprint reductions and food wastage statistics.
- **Prediction Model**: Machine learning model to predict food wastage based on various factors.
- **Interactive Filters**: Users can filter data based on days, food types, and regions.
- **Streamlit Integration**: Real-time data analysis and visualization using Streamlit.
- **REST API**: Endpoints for filtering data and predicting food wastage amounts.

### Project Structure
```
.gitignore
backend/
    alldata.csv
    config.js
    food_wastage_model.pkl
    index.js
    package.json
    predict.py
    routes/
        auth.js
    server.js
Carbon Footprint Streamlit/
    .streamlit/
    alldata.csv
    dash.html
    dash.py
    dashboard.js
datasavr/
    .ipynb_checkpoints/
    app.py
    app2.py
    Food Wastage prediction.ipynb
    Food Wastage prediction.py
    food_wastage_data.csv
    food_wastage_model.pkl
    Untitled.ipynb
frontend/
    .gitignore
    eslint.config.js
    index.html
    package.json
    postcss.config.js
    public/
README.md
```

### Installation

#### Clone the Repository
```sh
git clone https://github.com/yourusername/savr.git
cd savr
```

#### Backend Setup
```sh
cd backend
npm install
```

#### Frontend Setup
```sh
cd frontend
npm install
```

#### Streamlit Setup
```sh
pip install -r requirements.txt
```

### Usage

#### Start the Backend Server
```sh
cd backend
npm start
```

#### Start the Frontend Server
```sh
cd frontend
npm start
```

#### Run Streamlit Dashboard
```sh
streamlit run dash.py
```

### API Endpoints

#### Filter Data: POST `/filter`
**Request Body:**
```json
{ 
  "day": ["Monday"], 
  "food": ["Biryani"], 
  "region": ["Kallamessery"] 
}
```
**Response:** Filtered data based on the provided criteria.

#### Predict Food Wastage: POST `/predict`
**Request Body:**
```json
{ 
  "type_of_food": "Meat", 
  "number_of_guests": 100, 
  "event_type": "Wedding", 
  "quantity_of_food": 200, 
  "storage_conditions": "Cold Storage", 
  "purchase_history": "Frequent", 
  "seasonality": "Winter", 
  "preparation_method": "Grilled", 
  "geographical_location": "Urban", 
  "pricing": "High" 
}
```
**Response:** Predicted food wastage amount.

### Contributing
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

### License
This project is licensed under the MIT License.

### Acknowledgements
- Auth0
- Streamlit
- Plotly
- Seaborn

### Contact
For any inquiries, please contact [yourname@example.com](mailto:yourname@example.com).

SavR is committed to reducing food wastage and promoting sustainability. Join us in making a difference!