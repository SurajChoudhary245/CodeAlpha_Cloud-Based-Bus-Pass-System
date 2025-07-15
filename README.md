
# 🚌 Cloud-Based Bus Pass Booking System

This project is a cloud-based ticket/pass issuing platform built using AWS services. It allows users to request a bus pass via a simple web interface, and the backend system generates a unique ticket ID, stores the data securely in a database, and sends a confirmation email using AWS SES.

---

## 🌐 Tech Stack Used

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: AWS Lambda (Python)
- **API Gateway**: AWS API Gateway (REST API)
- **Database**: AWS RDS (MySQL)
- **Email Service**: AWS SES (Simple Email Service)

---

## ✅ Key Features

- 🔒 Prevents duplicate entries and invalid submissions
- 🎫 Generates a unique Ticket ID (UUID-based)
- 💾 Stores pass data securely in RDS (MySQL)
- 📧 Sends confirmation email with ticket details using SES
- 🌍 Fully hosted on cloud – scalable and serverless
- ⚙️ CORS-enabled API Gateway for frontend communication

---

## 📂 Folder Structure

```
cloud-bus-pass-system/
│
├── index.html              # Frontend interface
├── script.js               # JavaScript for API interaction
├── lambda_function.py      # Backend AWS Lambda handler
├── schema.sql              # SQL to create required table
├── style.css               # (Optional) CSS for design
└── README.md               # This file
```

---

## 🛠️ Setup & Deployment Instructions

### 1. 🎨 Frontend
- Open `index.html` locally or host on S3/EC2.
- It has a form that collects user data and sends it to the API endpoint.

### 2. ⚙️ Lambda + API Gateway
- Upload `lambda_function.py` to AWS Lambda
- Connect it to an API Gateway endpoint (`/issuepass`)
- Ensure CORS settings are correct (allow `POST` and `OPTIONS`)

### 3. 🗃️ RDS (MySQL)
Create a table using this query:
```sql
CREATE TABLE bus_passes (
    ticket_id VARCHAR(20) PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100),
    pass_type VARCHAR(50),
    from_location VARCHAR(100),
    to_location VARCHAR(100),
    valid_from DATE,
    valid_till DATE
);
```

### 4. 📬 SES Setup
- Verify your sender email address (e.g., choudharisuraj146@gmail.com)
- Grant Lambda permission for `ses:SendEmail` in IAM Role
- Use region `ap-south-1`

---

## 📷 Screenshots *(Optional)*
Add screenshots of:
- Form page
- Confirmation popup
- Email received

---

## 💡 Improvements (Optional)
- User authentication for admin panel
- Email templates or PDF pass generation
- Expiry-based cleanup Lambda function

---

## 👨‍💻 Author

**Suraj Choudhary**  
📧 choudharisuraj146@gmail.com  
📍 Cloud & InfoSec Student | AWS Intern  

---

## 🔗 Project Links

- **GitHub Repo**: [your_repo_link_here]
- **Live Frontend** (if hosted): [optional_link_here]

---

> 🚀 *Built as part of internship task for CodeAlpha (Cloud Computing Domain)*
