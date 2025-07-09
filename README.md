<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Healthcare Login/Register</title>
  <style>
    * {
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      margin: 0;
      background: linear-gradient(to right, #2bc0e4, #eaecc6);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }

    .container {
      background: white;
      padding: 2rem;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0,0,0,0.1);
      width: 100%;
      max-width: 400px;
      text-align: center;
    }

    .container h2 {
      margin-bottom: 1rem;
      color: #2b7a78;
    }

    .toggle-buttons {
      display: flex;
      justify-content: center;
      margin-bottom: 1rem;
    }

    .toggle-buttons button {
      flex: 1;
      padding: 10px;
      border: none;
      cursor: pointer;
      background-color: #3aafa9;
      color: white;
      font-weight: bold;
      transition: background-color 0.3s;
    }

    .toggle-buttons button.active {
      background-color: #2b7a78;
    }

    form {
      display: none;
      flex-direction: column;
    }

    form.active {
      display: flex;
    }

    input {
      padding: 10px;
      margin: 8px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button.submit-btn {
      background-color: #3aafa9;
      color: white;
      border: none;
      padding: 10px;
      border-radius: 5px;
      font-size: 16px;
      margin-top: 10px;
      cursor: pointer;
    }

    button.submit-btn:hover {
      background-color: #2b7a78;
    }

    .link-buttons {
  margin-top: 15px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.custom-btn {
  background-color: #2b7a78;
  color: white;
  padding: 10px;
  text-align: center;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
  transition: background-color 0.3s;
}

.custom-btn:hover {
  background-color: #205e5b;
}

  </style>
</head>
<body>

<div class="container">
  <h2>Healthcare Login/Register</h2>

  <div class="toggle-buttons">
    <button id="loginToggle" class="active">Login</button>
    <button id="registerToggle">Register</button>
  </div>

  <!-- Login Form -->
  <!-- <form id="loginForm" class="active" onsubmit="event.preventDefault(); window.location.href='empowerment.html';"> -->
    <form id="loginForm" class="active">

    <input type="email" placeholder="Email" required />
    <input type="password" placeholder="Password" required />
    <button type="button" id="loginSubmitBtn" class="submit-btn">Login</button>

    <div class="link-buttons">
  <!-- <a href="empowerment.html" class="custom-btn">Empowerment Page</a>
  <a href="patient_dashboard.html" class="custom-btn">Patient Dashboard Page</a> -->
</div>

  </form>

  <!-- Register Form -->
  <form id="registerForm">
    <input type="text" placeholder="Full Name" required />
    <input type="email" placeholder="Email" required />
    <input type="password" placeholder="Password" required />
    <input type="password" placeholder="Confirm Password" required />
    <button type="submit" class="submit-btn">Register</button>
  </form>
</div>

<script>
  const loginBtn = document.getElementById("loginToggle");
  const registerBtn = document.getElementById("registerToggle");
  const loginForm = document.getElementById("loginForm");
  const registerForm = document.getElementById("registerForm");

  loginBtn.addEventListener("click", () => {
    loginForm.classList.add("active");
    registerForm.classList.remove("active");
    loginBtn.classList.add("active");
    registerBtn.classList.remove("active");
  });

  registerBtn.addEventListener("click", () => {
    registerForm.classList.add("active");
    loginForm.classList.remove("active");
    registerBtn.classList.add("active");
    loginBtn.classList.remove("active");
  });
  document.querySelector("#loginForm .submit-btn").addEventListener("click", function(e) {
  e.preventDefault(); // stop actual form submission
  window.location.href = "empowerment.html"; // redirect
});

</script>

</body>
</html>
     


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Empowering Rural Healthcare</title>
  

  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: #f0f8ff;
      color: #333;
    }

    header {
      background: #2e7d32;
      color: white;
      padding: 30px 20px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 32px;
    }

    .features {
      padding: 30px 10%;
      background: #fff;
    }

    .feature {
      background: #e8f5e9;
      margin-bottom: 20px;
      padding: 20px;
      border-left: 5px solid #2e7d32;
      border-radius: 5px;
    }

    .feature h2 {
      margin-top: 0;
      color: #1b5e20;
    }

    footer {
      background: #2e7d32;
      color: white;
      text-align: center;
      padding: 10px;
      font-size: 14px;
    }

    @media (max-width: 768px) {
      header h1 {
        font-size: 24px;
      }

      .features {
        padding: 20px;
      }
    }
    .go-btn {
  display: inline-block;
  margin-top: 30px;
  padding: 12px 24px;
  background-color: #2e7d32;
  color: white;
  text-decoration: none;
  font-size: 16px;
  border-radius: 6px;
  transition: background-color 0.3s ease;
}

.go-btn:hover {
  background-color: #1b5e20;
}

.feature:hover {
  background-color: #d0f0d0;
  cursor: pointer;
}


  </style>
</head>
<body>
  


  <header>
    <h1>Empowering Rural Healthcare with Smart Accessible Technology</h1>
  </header>

  <section class="features">

  <a href="patient_dashboard.html" style="text-decoration: none;">
    <div class="feature">
      <h2>1. Patient Dashboard</h2>
      <p>View and update vitals such as blood pressure, glucose levels, heart rate, and more.</p>
    </div>
  </a>

  <a href="doctor.html" style="text-decoration: none;">
    <div class="feature">
      <h2>2. Doctor Login</h2>
      <p>Secure login for doctors to monitor assigned patients, view medical history, and provide support.</p>
    </div>
  </a>

  <a href="reminders.html" style="text-decoration: none;">
    <div class="feature">
      <h2>3. Reminders & Alerts</h2>
      <p>Automatic reminders for medication intake, checkups, and vaccination dates.</p>
    </div>
  </a>

  <a href="tips.html" style="text-decoration: none;">
    <div class="feature">
      <h2>4. Local Language Tips</h2>
      <p>Health education and tips provided in Hindi, Bengali, Telugu, etc.</p>
    </div>
  </a>

  <a href="patient_dashboard.html" class="go-btn">Go to Dashboard Now</a>

</section>



  <footer>
    &copy; 2025 Rural HealthTech Initiative | Built for Bharat 🇮🇳
  </footer>

</body>
</html>

    
      
    

    

    





