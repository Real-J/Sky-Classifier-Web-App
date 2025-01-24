# 🌤 Sky Classifier Web App

A Django-based web application that allows users to upload images of the sky and classifies them as **Cloudy**, **Overcast**, or **Sunny** using a pre-trained deep learning model.

---

## 🚀 Features
- **Image Upload**: Upload sky images directly through the web interface.
- **Deep Learning Classification**: Uses a pre-trained model to predict the weather condition based on the uploaded image.
- **Real-Time Predictions**: Instant classification with a user-friendly result display.
- **Responsive Interface**: Simple and intuitive design.

---

## 🔧 Installation and Setup

### **1. Clone the Repository**
```bash
git clone https://github.com/Real-J/sky-classifier.git
cd sky-classifier
```

### **2. Set Up a Python Virtual Environment**
```bash
python -m venv sky_env
source sky_env/bin/activate       # On Linux/Mac
sky_env\Scripts\activate          # On Windows
```

### **3. Configure Django Settings**
- Ensure your `settings.py` includes the following:
  ```python
  MEDIA_URL = '/media/'
  MEDIA_ROOT = BASE_DIR / 'media'
  ```
- Create a `media` directory in the project root:
  ```bash
  mkdir media
  ```

### **4. Add Your Pre-trained Model**
Place your `.keras` file in the `classify/model/` directory:
```
classify/model/sky_model.keras
```

### **5. Run Database Migrations**
```bash
python manage.py makemigrations
python manage.py migrate
```

### **6. Start the Django Development Server**
```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000/` in your browser to access the app.

---

## 🖼 How It Works
1. Upload a sky image on the app’s main page.
2. The image is processed and passed to the pre-trained deep learning model.
3. The app displays the uploaded image along with its predicted class (e.g., **Cloudy**, **Overcast**, **Sunny**).

---

## 🪠 Technologies Used
- **Frontend**: HTML, CSS
- **Backend**: Python, Django
- **Deep Learning**: TensorFlow, Keras
- **Model**: MobileNetV2-based image classification model

---

## 🐂 Project Structure
```
sky_classifier/
├── classify/
│   ├── model/
│   │   ├── sky_model.keras   # Pre-trained classification model
│   ├── templates/
│   │   ├── classify/
│   │   │   ├── upload.html   # Image upload page
│   │   │   ├── result.html   # Prediction result page
│   ├── views.py              # Handles image upload and prediction logic
│   ├── urls.py               # URL routing for the classify app
├── media/                    # Stores uploaded images
├── sky_classifier/
│   ├── settings.py           # Django project settings
│   ├── urls.py               # Main project URLs
├── manage.py                 # Django management script
```

---

## 🔢 Example Results

![Input Image](webresult.png)


---

## 📜 License
This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Contributions
Contributions, issues, and feature requests are welcome! Feel free to fork this repository and submit a pull request.

---


