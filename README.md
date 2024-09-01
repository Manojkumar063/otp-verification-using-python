# otp-verification-using-python


---

# OTP Verification System

### Overview

This project is an **OTP Verification System** built using Python, Flask, and SMTP protocol. It generates a 6-digit OTP, sends it to the user's email for verification, and validates the entered OTP. The system ensures that the OTP sent is valid only for a limited time, adding an extra layer of security.

### Features
- Generates a random 6-digit OTP.
- Sends the OTP to the user's email using SMTP.
- Validates the OTP entered by the user.
- Implements a time-limited OTP to enhance security.
  
### Tech Stack
- **Python**: Core language for the backend.
- **Flask**: Framework for creating the web interface.
- **SMTP (Simple Mail Transfer Protocol)**: Used for sending OTPs to users' emails.
- **Email Validation**: Ensures OTP is verified by the right user.

### Requirements

Before running the project, make sure you have the following installed:

- Python 3.x
- Flask
- smtplib (comes with Python standard library)
- dotenv (for handling environment variables)

Install the required packages via pip:
```bash
pip install Flask python-dotenv
```

### Setup

1. Clone the repository to your local machine.
   ```bash
   git clone https://github.com/your-username/otp-verification-system.git
   ```
   
2. Navigate to the project directory:
   ```bash
   cd otp-verification-system
   ```

3. Set up your environment variables by creating a `.env` file in the root directory with the following information:
   ```bash
   EMAIL_SENDER=your_email@example.com
   EMAIL_PASSWORD=your_password
   ```
   
4. Make sure to enable **less secure app access** on your email account (if using Gmail).

### Usage

1. Run the Flask server:
   ```bash
   python app.py
   ```

2. Open your web browser and navigate to `http://127.0.0.1:5000/`.

3. Enter the email address where you want to receive the OTP.

4. Check your email for the OTP, enter it in the verification form, and submit to complete the process.

### Project Structure

```
otp-verification-system/
│
├── app.py                # Main Flask application
├── otp.py                # OTP generation and validation logic
├── templates/            # HTML templates
│   ├── index.html        # Email input form
│   └── verify.html       # OTP verification form
├── static/               # Static files (CSS, JS)
└── .env                  # Environment variables (not included in the repo)
```

### Future Improvements

- Implementing Twilio SMS for OTP sending.
- Adding database integration for storing user OTPs.
- Adding more robust validation and error handling.
- Implementing time-limited OTPs that expire after a certain duration.

### License

This project is licensed under the MIT License.

