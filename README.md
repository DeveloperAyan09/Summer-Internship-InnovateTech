# Summer-Internship-InnovateTech
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>InnovateTech E-commerce</title>
    <style>
        /* CSS Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Body Styling */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            line-height: 1.6;
        }

        /* Header and Navigation */
        header {
            background-color: #333;
            color: white;
            padding: 1em 0;
            text-align: center;
        }

        nav ul {
            list-style-type: none;
            text-align: center;
        }

        nav ul li {
            display: inline;
            margin: 0 15px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }

        /* Main Content Styling */
        main {
            padding: 20px;
        }

        h1 {
            text-align: center;
            margin-bottom: 20px;
        }

        p {
            text-align: center;
        }

        /* Footer Styling */
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em 0;
            position: relative;
            bottom: 0;
            width: 100%;
            margin-top: 40px;
        }

        /* Product Catalog */
        .product-catalog {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin-top: 20px;
        }

        .product {
            background-color: rgb(189, 35, 35);
            border: 1px solid #ccc;
            margin: 10px;
            padding: 10px;
            width: 30%;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .product img {
            max-width: 100%;
            height: auto;
        }

        /* Form Styling */
        form {
            max-width: 400px;
            margin: 0 auto;
            padding: 20px;
            background-color: rgb(230, 225, 89);
            border: 1px solid #0d0d0d;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        form label {
            display: block;
            margin-bottom: 10px;
            font-weight: bold;
        }

        form input {
            width: 100%;
            padding: 8px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        form button {
            width: 100%;
            padding: 10px;
            background-color: #333;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        form button:hover {
            background-color: #555;
        }

        /* Validation Styling */
        .error {
            color: red;
            font-size: 0.9em;
            display: none;
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="products.html">Products</a></li>
                <li><a href="about.html">About Us</a></li>
                <li><a href="contact.html">Contact</a></li>
                <li><a href="login.html">Login</a></li>
            </ul>
        </nav>
    </header>

    <!-- Main Content for Home Page -->
    <main>
        <h1>Welcome to InnovateTech!</h1>
        <p>Your one-stop shop for the latest tech products.</p>
    </main>

    <!-- Products Page -->
    <section class="product-catalog">
        <article class="product">
            <img src="c:\Users\ASUS\Desktop\summerproject\VR box.JPEG.png" alt="Product 1">
            <h2>InnovateTech VR Box</h2>
            <p>Immerse yourself in a world of virtual reality with the InnovateTech VR Box, a perfect gateway to experience gaming, movies, and 3D content like never before..</p>
        </article>

        <article class="product">
            <img src="c:\Users\ASUS\Desktop\summerproject\Eco Sound Box.JPEG.png" alt="Product 2">
            <h2>InnovateTech Eco Sound Box</h2>
            <p>Experience powerful, eco-friendly sound with the InnovateTech Eco Sound Box, designed for environmentally-conscious music lovers.</p>
        </article>

        <article class="product">
            <img src="c:\Users\ASUS\Desktop\summerproject\Projector.JPEG.png" alt="Product 3">
            <h2>InnovateTech Mini Projector</h2>
            <p>Transform any room into a personal theater with the InnovateTech Room Projector, the ultimate device for movie nights, presentations, and gaming.</p>
        </article>
    </section>

    <!-- About Us Page -->
    <main>
        <h1>About Us</h1>
        <p>InnovateTech is a leading e-commerce platform for tech enthusiasts. Our mission is to provide the latest and greatest tech products at affordable prices.</p>
    </main>

    <!-- Contact Us Page -->
    <main>
        <h1>Contact Us</h1>
        <p>Feel free to reach out to us via email or phone.
        Gmail:   ayanhussain09786@gmail.com 
        Mobile:   7389970073      
        </p>
    </main>

    <!-- Registration/Login Form -->
    <main>
        <h1>Login</h1>
        <form action="submit_login.html" method="post" onsubmit="return validateLoginForm()">
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
            <span class="error" id="emailError">Please enter a valid email address.</span><br>

            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required>
            <span class="error" id="passwordError">Password must be at least 6 characters long.</span><br>

            <button type="submit">Login</button>
        </form>

        <h2>Not a member? Register below!</h2>
        <form action="submit_registration.html" method="post" onsubmit="return validateRegistrationForm()">
            <label for="reg-email">Email:</label>
            <input type="email" id="reg-email" name="reg-email" required>
            <span class="error" id="regEmailError">Please enter a valid email address.</span><br>

            <label for="reg-password">Password:</label>
            <input type="password" id="reg-password" name="reg-password" required>
            <span class="error" id="regPasswordError">Password must be at least 6 characters long.</span><br>

            <button type="submit">Register</button>
        </form>
    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 InnovateTech. All rights reserved.</p>
    </footer>

    <script>
        // Client-side validation for the login form
        function validateLoginForm() {
            var email = document.getElementById('email').value;
            var password = document.getElementById('password').value;
            var emailError = document.getElementById('emailError');
            var passwordError = document.getElementById('passwordError');

            emailError.style.display = 'none';
            passwordError.style.display = 'none';

            var emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6}$/;

            if (!emailPattern.test(email)) {
                emailError.style.display = 'block';
                return false;
            }

            if (password.length < 6) {
                passwordError.style.display = 'block';
                return false;
            }

            return true;
        }

        // Client-side validation for the registration form
        function validateRegistrationForm() {
            var email = document.getElementById('reg-email').value;
            var password = document.getElementById('reg-password').value;
            var regEmailError = document.getElementById('regEmailError');
            var regPasswordError = document.getElementById('regPasswordError');

            regEmailError.style.display = 'none';
            regPasswordError.style.display = 'none';

            var emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6}$/;

            if (!emailPattern.test(email)) {
                regEmailError.style.display = 'block';
                return false;
            }

            if (password.length < 6) {
                regPasswordError.style.display = 'block';
                return false;
            }

            return true;
        }
    </script>
</body>
</html>
