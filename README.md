# Albumy

📸 **Capture and share every wonderful moment.**  
An open-source **Flask** web application for photo sharing, now enhanced with **Azure AI-powered image tagging and search**.

> Example application for *[Python Web Development with Flask](https://helloflask.com/en/book/1)* (《[Flask Web 开发实战](https://helloflask.com/book/1)》).

🎯 **Demo:** http://albumy.helloflask.com  

![Screenshot](https://helloflask.com/screenshots/albumy.png)

---

## 🚀 **New Features Added**

🔹 **AI-Powered Image Tagging:** Automatically tags uploaded images using **Azure AI Vision**.  
🔹 **AI-Generated Alternative Text (Alt Text):** Improves accessibility by generating descriptions for images.  
🔹 **Intelligent Image Search:** Enables searching images based on detected objects, scenes, and AI-generated tags.  
🔹 **Secure API Key Handling:** Uses environment variables to manage sensitive credentials safely.    

---

## 🚀 **Installation**

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/greyli/albumy.git
cd albumy
```

---

## 🔧 **Azure AI Integration Setup**
Albumy uses **Azure AI Computer Vision** for **automated image tagging and search**.

### **2️⃣ Prerequisites**
Before setting up the system, ensure you have:
- An **Azure subscription** → *[Create one for free](https://azure.microsoft.com/en-us/free/ai-services/)*
- Installed **pip** → Run `pip --version` to check. If missing, install the latest Python version.

### **3️⃣ Set Up Azure AI Credentials**
1️⃣ Go to **[Azure Portal](https://portal.azure.com/)** and **create a Vision resource**:  
   - *[Create Computer Vision Resource](https://portal.azure.com/#create/Microsoft.CognitiveServicesComputerVision)*
   - Copy the **Key** and **Endpoint** from the **Keys and Endpoint** page.

2️⃣ Set the environment variables:  
    Open a terminal:
    ```
    **cd albumy*/blueprints**
    ```

   - **Mac/Linux:**
     ```bash
     export AZURE_CV_KEY="your-key"
     export AZURE_CV_ENDPOINT="your-endpoint"
     ```
   - **Windows (Command Prompt):**
     ```cmd
     set AZURE_CV_KEY=your-key
     set AZURE_CV_ENDPOINT=your-endpoint
     ```
   - **Windows (PowerShell):**
     ```powershell
     $env:AZURE_CV_KEY="your-key"
     $env:AZURE_CV_ENDPOINT="your-endpoint"
     ```

---

## 🛠 **Install Dependencies & Run the App**

### **4️⃣ Create and Activate Virtual Environment**
Using **venv** (recommended):
```bash
python -m venv env
source env/bin/activate  # Mac/Linux
env\Scripts\activate  # Windows
pip install -r requirements.txt
```

Or using **conda**:
```bash
conda create --name albumy python=3.8
conda activate albumy
pip install -r requirements.txt
```

### **5️⃣ Install Azure AI Vision API**
```bash
pip install --upgrade azure-cognitiveservices-vision-computervision
```

### **6️⃣ Generate Fake Data and Run the App**
```bash
flask forge
flask run
```
The app will be available at:  
👉 **http://127.0.0.1:5000/**  

---

## 🔑 **Test Account**
- **Email:** `admin@helloflask.com`
- **Password:** `helloflask`

---

## 📜 **License**
This project is licensed under the MIT License (see the [LICENSE](LICENSE) file for details).
