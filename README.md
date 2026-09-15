# Etta-cakes
Online bakery
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Etta Cakes</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #fffafc;
      margin: 0;
      padding: 0;
      color: #333;
    }
    header {
      text-align: center;
      padding: 50px;
      background-color: #fce4ec;
    }
    header h1 {
      font-family: 'Brush Script MT', cursive;
      font-size: 4em;
      color: #f8bbd0;
    }
    nav {
      display: flex;
      justify-content: center;
      background-color: #f3e5f5;
      padding: 10px;
    }
    nav a {
      margin: 0 15px;
      text-decoration: none;
      color: #6a1b9a;
      font-weight: bold;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 40px;
    }
    .product {
      border: 1px solid #eee;
      border-radius: 10px;
      padding: 20px;
      text-align: center;
      background-color: #ffffff;
    }
    .product img {
      max-width: 100%;
      border-radius: 10px;
    }
    .add-to-cart {
      background-color: #ef9a9a;
      color: white;
      border: none;
      padding: 10px 20px;
      margin-top: 10px;
      border-radius: 5px;
      cursor: pointer;
    }
    footer {
      background-color: #f3e5f5;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Etta Cakes</h1>
  </header>
  <nav>
    <a href="#shop">Shop</a>
    <a href="#gallery">Gallery</a>
    <a href="#reviews">Reviews</a>
    <a href="#contact">Contact</a>
  </nav>
  <section id="shop" class="products">
    <div class="product">
      <img src="cake1.jpg" alt="Chocolate Cake">
      <h3>Chocolate Cake</h3>
      <p>Rich and moist chocolate delight.</p>
      <button class="add-to-cart">Add to Cart</button>
    </div>
    <div class="product">
      <img src="cake2.jpg" alt="Red Velvet Cake">
      <h3>Red Velvet Cake</h3>
      <p>Classic red velvet with cream cheese frosting.</p>
      <button class="add-to-cart">Add to Cart</button>
    </div>
  </section>
  <footer>
    <p>Email: info@ettacakes.com | Phone: +234-800-123-4567</p>
  </footer>
</body>
</html>
<!-- Add this inside your <body> after the header/nav -->

<!-- Owner Info Section (secured with password) -->
<section id="owner-info" style="display:none;">
  <h2>Owner Dashboard</h2>
  <form id="ownerForm">
    <label>Email:</label>
    <input type="email" name="ownerEmail" placeholder="Enter email"><br><br>
    <label>Phone Number:</label>
    <input type="tel" name="ownerPhone" placeholder="Enter phone number"><br><br>
    <label>Bank Details (secured):</label>
    <input type="password" name="bankDetails" placeholder="Enter bank details"><br><br>
    <button type="submit">Save Info</button>
  </form>
</section>

<!-- Social Media Icons -->
<div style="text-align:center; margin:20px;">
  <a href="https://wa.me/2348001234567" target="_blank">
    <img src="whatsapp-logo.png" alt="WhatsApp" style="width:40px; margin:10px;">
  </a>
  <a href="https://instagram.com/ettacakes" target="_blank">
    <img src="instagram-logo.png" alt="Instagram" style="width:40px; margin:10px;">
  </a>
</div>

<!-- Hamburger Menu (Protein Bars) -->
<div id="menuToggle" style="cursor:pointer; width:40px; margin:20px;">
  <div style="height:6px; background:#8d6e63; margin:6px 0;"></div>
  <div style="height:6px; background:#8d6e63; margin:6px 0;"></div>
  <div style="height:6px; background:#8d6e63; margin:6px 0;"></div>
</div>

<ul id="menu" style="display:none; list-style:none; padding:0; text-align:center;">
  <li><a href="#cakes">Cakes</a></li>
  <li><a href="#cookies">Cookies</a></li>
  <li><a href="#beverages">Beverages</a></li>
</ul>

<script>
  // Toggle menu visibility
  document.getElementById("menuToggle").onclick = function() {
    const menu = document.getElementById("menu");
    menu.style.display = (menu.style.display === "none") ? "block" : "none";
  };

  // Simple owner form handling (demo only)
  document.getElementById("ownerForm").onsubmit = function(e) {
    e.preventDefault();
    alert("Owner info saved securely!");
    // In real
