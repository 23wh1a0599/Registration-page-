# Registration-page-

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <title>Registration Form</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            /* Background image with overlay */
            background: 
              linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
              url('https://as2.ftcdn.net/v2/jpg/02/08/27/73/1000_F_208277332_DgdJiQwSzIYw714ovaCwNBaSDdVtJB2M.jpg') no-repeat center center fixed;
            background-size: cover;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            width: 420px;
            padding: 30px;
            background-color: #ffffffcc; /* semi-transparent white */
            border-radius: 12px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.3);
            position: relative;
        }

        h2 {
            text-align: center;
            margin-bottom: 20px;
            color: #333;
        }

        label {
            font-weight: bold;
            margin-top: 10px;
            display: block;
            color: #444;
        }

        input[type="text"],
        input[type="email"],
        input[type="password"],
        input[type="date"],
        select {
            width: 100%;
            padding: 10px;
            margin: 8px 0 20px;
            border: 1px solid #ccc;
            border-radius: 6px;
            font-size: 14px;
        }

        input[type="submit"] {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 12px;
            width: 100%;
            border-radius: 6px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        input[type="submit"]:hover {
            background-color: #0056b3;
        }

        /* Congratulations message style */
        #congrats-message {
            display: none;
            text-align: center;
            font-size: 1.5rem;
            color: #28a745;
            font-weight: bold;
            margin-top: 20px;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Registration Form</h2>
    <form id="registration-form" action="submit_form.php" method="POST">
        <label for="fullname">Full Name:</label>
        <input type="text" id="fullname" name="fullname" required />

        <label for="email">Email Address:</label>
        <input type="email" id="email" name="email" required />

        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required />

        <label for="dob">Date of Birth:</label>
        <input type="date" id="dob" name="dob" required />

        <label for="gender">Gender:</label>
        <select id="gender" name="gender" required>
            <option value="">--Select Gender--</option>
            <option value="Male">Male</option>
            <option value="Female">Female</option>
            <option value="Other">Other</option>
        </select>

        <label for="department">Department:</label>
        <select id="department" name="department" required>
            <option value="">--Select Department--</option>
            <option value="IT">IT</option>
            <option value="CSE">CSE</option>
            <option value="ECE">ECE</option>
            <option value="EEE">EEE</option>
            <option value="CSE-AI&ML">AI and ML</option>
            <option value="Mechanical">Mechanical Engineering</option>
        </select>

        <label for="state">State:</label>
        <select id="state" name="state" required>
            <option value="">--Select State--</option>
            <option value="Telangana">Telangana</option>
            <option value="Adilabad">Adilabad</option>
            <option value="Suryapet">Suryapet</option>
            <option value="Siddipet">Siddipet</option>
            <option value="Mahabubabad">Mahabubabad</option>
        </select>

        <label for="country">Country:</label>
        <select id="country" name="country" required>
            <option value="">--Select Country--</option>
            <option value="United States">United States</option>
            <option value="Canada">Canada</option>
            <option value="United Kingdom">United Kingdom</option>
            <option value="Australia">Australia</option>
            <option value="India">India</option>
        </select>

        <input type="submit" value="Register" />
    </form>
    
    <div id="congrats-message">🎉 Congratulations! Your registration is successful. 🎉</div>
</div>

<script>
    const form = document.getElementById('registration-form');
    const congratsMessage = document.getElementById('congrats-message');

    form.addEventListener('submit', function(event) {
        event.preventDefault(); // prevent form from submitting to server

        // You can add form validation here if needed

        // Hide the form
        form.style.display = 'none';

        // Show congratulations message
        congratsMessage.style.display = 'block';
    });
</script>

</body>
</html>
