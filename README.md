<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Restaurant & Café Menu</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <style>
    /* General Styles */
body {
  font-family: 'Arial', sans-serif;
  margin: 0;
  padding: 0;
  background: #000; /* Black background */
  color: #000000; /* White text */
}

/* Transparent Navbar */
.navbar {
  background: rgba(0, 0, 0, 0.5) !important;
  transition: background 0.3s ease;
}

.navbar.scrolled {
  background: rgba(0, 0, 0, 0.9) !important;
}

/* Dropdown Menu */
.dropdown-menu {
  background: rgba(0, 0, 0, 0.9);
  border: none;
}

.dropdown-item {
  color: #fff !important;
}

.dropdown-item:hover {
  background: rgba(255, 255, 255, 0.1);
}

/* Home Section */
.home-section {
  height: 100vh;
  background: url('./photos/Rozzis\ -\ Picture\ gallery\ 5.jpg') no-repeat center center/cover;
  display: flex;
  text-shadow: 0 0 10px #ff0000, 0 0 20px #ffcc00, 0 0 30px #ffcc00, 0 0 40px #ffcc00; 
  align-items: center;
  justify-content: center;
  text-align: center;
  color: rgb(0, 0, 0);
}

/* Menu Sections */
.menu-section {
  padding: 60px 0;
}

.card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  background: #1e1e1e; /* Dark card background */
  border: none;
  border-radius: 10px;
  overflow: hidden;
  color: #ffd900; /* White text for cards */
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(255, 255, 255, 0.1); /* Light shadow for contrast */
}
/* About Us Section */
.about-section {
  padding: 60px 0;
  justify-content: center;

  background: #000000; /* Light background */
  text-align: center;
  color: #7c0505;

}

.about-section h2 {
  font-size: 2.5rem;
  margin-bottom: 20px;
}

.about-section p {
  font-size: 1.1rem;
  line-height: 1.8;
  max-width: 800px;
  margin: 0 auto;
}

/* Contact Us Section */
.contact-section {
  padding: 60px 0;
  background: hsl(0, 0%, 0%); /* White background */
  text-align: center;
  color: #7c0505;
  justify-content: center;

}

.contact-section h2 {
  font-size: 2.5rem;
  margin-bottom: 20px;
}

.contact-section p {
  font-size: 1.1rem;
  line-height: 1.8;
  max-width: 800px;
  margin: 0 auto;
}

.contact-info {
  margin-top: 20px;
}

.contact-info p {
  font-size: 1rem;
  margin: 10px 0;
}

.social-media {
  margin-top: 20px;
}

.social-link {
  font-size: 1.5rem;
  margin: 0 10px;
  color: #333; /* Dark text */
  transition: color 0.3s ease;
}

.social-link:hover {
  color: #ffe600; /* Green on hover */
}
.

/* Animations */
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.fade-in {
  animation: fadeIn 1s ease-in;
}

/* Responsive Sidebar */
@media (max-width: 991.98px) {
  .navbar-collapse {
    background: rgba(0, 0, 0, 0.9);
    padding: 10px;
  }
}
  </style>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
    <div class="container">
      <a class="navbar-brand" href="#">Restaurant & Café</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
          <!-- Food Dropdown -->
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="foodDropdown" role="button" data-bs-toggle="dropdown">
              Food
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="food.html#chicken">Chicken</a></li>
              <li><a class="dropdown-item" href="food.html#beef">Beef</a></li>
              <li><a class="dropdown-item" href="food.html#seafood">Seafood</a></li>
            </ul>
          </li>
          <!-- Drinks Dropdown -->
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="drinksDropdown" role="button" data-bs-toggle="dropdown">
              Drinks
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="drinks.html#coffee">Coffee</a></li>
              <li><a class="dropdown-item" href="drinks.html#soft-drinks">Soft Drinks</a></li>
              <li><a class="dropdown-item" href="drinks.html#juices">Juices</a></li>
            </ul>
          </li>
          <li class="nav-item"><a class="nav-link" href="#about">About Us</a></li>
          <li class="nav-item"><a class="nav-link" href="#contact">Contact Us</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Home Section -->
  <section id="home" class="home-section">
    <div class="container">
      <h1>Welcome to Our Restaurant & Café</h1>
      <p>Experience the best food and drinks in town.</p>
    </div>
  </section>

  <!-- Best Food Items -->
  <section id="best-food" class="menu-section">
    <div class="container">
      <h2>Best Food Items</h2>
      <div class="row">
        <!-- Chicken Dish -->
        <div class="col-md-4">
          <div class="card">
            <img src=".//photos/Grilled Chicken.jpg" class="card-img-top" alt="Chicken Dish">
            <div class="card-body">
              <h5 class="card-title">Grilled Chicken</h5>
              <p class="card-text">Juicy grilled chicken with special spices.</p>
              <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#chickenModal">Quick View</button>
            </div>
          </div>
        </div>
        <!-- Beef Dish -->
        <div class="col-md-4">
          <div class="card">
            <img src=".//photos/Beef Steak.jpg" class="card-img-top" alt="Beef Dish">
            <div class="card-body">
              <h5 class="card-title">Beef Steak</h5>
              <p class="card-text">Tender beef steak with garlic butter.</p>
              <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#beefModal">Quick View</button>
            </div>
          </div>
        </div>
        <!-- Seafood Dish -->
        <div class="col-md-4">
          <div class="card">
            <img src=".//photos/Seafood Platter.jpg" class="card-img-top" alt="Seafood Dish">
            <div class="card-body">
              <h5 class="card-title">Seafood Platter</h5>
              <p class="card-text">Fresh seafood platter with lemon butter sauce.</p>
              <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#seafoodModal">Quick View</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Best Drinks Items -->
  <section id="best-drinks" class="menu-section">
    <div class="container">
      <h2>Best Drinks Items</h2>
      <div class="row">
        <!-- Coffee -->
        <div class="col-md-4">
          <div class="card">
            <img src=".//photos/Espresso.jpg" class="card-img-top" alt="Coffee">
            <div class="card-body">
              <h5 class="card-title">Espresso</h5>
              <p class="card-text">Rich and bold espresso coffee.</p>
              <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#coffeeModal">Quick View</button>
            </div>
          </div>
        </div>
        <!-- Soft Drink -->
        <div class="col-md-4">
          <div class="card">
            <img src=".//photos/Cola.jpg" class="card-img-top" alt="Soft Drink">
            <div class="card-body">
              <h5 class="card-title">Cola</h5>
              <p class="card-text">Refreshing cola with ice.</p>
              <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#colaModal">Quick View</button>
            </div>
          </div>
        </div>
        <!-- Juice -->
        <div class="col-md-4">
          <div class="card">
            <img src=".//photos/Orange Juice.jpg" class="card-img-top" alt="Juice">
            <div class="card-body">
              <h5 class="card-title">Orange Juice</h5>
              <p class="card-text">Freshly squeezed orange juice.</p>
              <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#juiceModal">Quick View</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- About Us Section -->
  <section id="about" class="about-section">
    <div class="container">
      <h2>About Us</h2>
      <p>Welcome to <strong>Restaurant & Café</strong>, where we bring you the finest dining experience. Our passion for food and drinks is reflected in every dish we serve. We use only the freshest ingredients to create mouth-watering meals that will leave you craving for more.</p>
      <p>Our team of expert chefs and baristas are dedicated to providing you with an unforgettable experience. Whether you're here for a quick coffee or a full-course meal, we guarantee you'll leave satisfied.</p>
    </div>
  </section>

  <!-- Contact Us Section -->
  <section id="contact" class="contact-section">
    <div class="container">
      <h2>Contact Us</h2>
      <p>We'd love to hear from you! Reach out to us for reservations, inquiries, or just to say hello.</p>
      <div class="contact-info">
        <p><strong>Email:</strong> info@restaurant.com</p>
        <p><strong>Phone:</strong> +20100006594</p>
        <p><strong>Address:</strong> 123 Main Street, City, Country</p>
      </div>
      <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d362.99760985821104!2d30.96096874651916!3d30.05307114386745!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2seg!4v1737568954189!5m2!1sen!2seg" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      <div class="social-media">
        <a href="https://facebook.com" target="_blank" class="social-link"><i class="fab fa-facebook-f"></i></a>
        <a href="https://twitter.com" target="_blank" class="social-link"><i class="fab fa-twitter"></i></a>
        <a href="https://instagram.com" target="_blank" class="social-link"><i class="fab fa-instagram"></i></a>
      </div>
    </div>
  </section>

  <!-- Quick View Modals -->
  <!-- Chicken Modal -->
  <div class="modal fade" id="chickenModal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Grilled Chicken</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body">
            <img src=".//photos/Grilled Chicken.jpg" class="img-fluid" alt="Beef Steak">          <p>Juicy grilled chicken marinated with special spices and served with a side of fresh salad.</p>
          <p><strong>Price:</strong> 400 L.E</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Beef Modal -->
  <div class="modal fade" id="beefModal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Beef Steak</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body">
          <img src=".//photos/Beef Steak.jpg" class="img-fluid" alt="Beef Steak">
          <p>Tender beef steak cooked to perfection, served with garlic butter and mashed potatoes.</p>
          <p><strong>Price:</strong> 500 L.E</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Seafood Modal -->
  <div class="modal fade" id="seafoodModal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Seafood Platter</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body">
          <img src=".//photos/Seafood Platter.jpg" class="img-fluid" alt="Seafood Platter">
          <p>Fresh seafood platter with shrimp, calamari, and fish, served with lemon butter sauce.</p>
          <p><strong>Price:</strong> $22.99</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Coffee Modal -->
  <div class="modal fade" id="coffeeModal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Espresso</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body">
          <img src=".//photos/Espresso.jpg" class="img-fluid" alt="Espresso">
          <p>Rich and bold espresso coffee, perfect for coffee lovers.</p>
          <p><strong>Price:</strong> 60 L.E</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Cola Modal -->
  <div class="modal fade" id="colaModal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Cola</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body">
          <img src=".//photos/Soft Drinks.jpg" class="img-fluid" alt="Cola">
          <p>Refreshing cola served with ice, perfect for any meal.</p>
          <p><strong>Price:</strong> 50 L.E</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Juice Modal -->
  <div class="modal fade" id="juiceModal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Orange Juice</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body">
          <img src=".//photos/Orange Juice.jpg" class="img-fluid" alt="Orange Juice">
          <p>Freshly squeezed orange juice, packed with vitamins.</p>
          <p><strong>Price:</strong> 100 L.E</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Scripts -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <script src="scripts.js"></script>
</body>
</html>
