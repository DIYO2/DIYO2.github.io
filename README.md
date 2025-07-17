
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Wendy's Restaurant</title>
  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
  <!-- Font Awesome for icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    /* Global Styles */
    body {
      font-family: Arial, sans-serif;
      background-color: #f5f5f5;
      color: #333;
    }
    
    .navbar {
      background-color: #e74c3c;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    
    .navbar-nav .nav-link {
      color: white !important;
      font-weight: bold;
    }
    
    .navbar-nav .nav-link:hover {
      color: #f1c40f !important;
    }
    
    .section-title {
      color: #e74c3c;
      margin-bottom: 30px;
      position: relative;
      display: inline-block;
    }
    
    .section-title:after {
      content: '';
      position: absolute;
      width: 50%;
      height: 3px;
      background: #f1c40f;
      bottom: -10px;
      left: 25%;
    }
    
    /* Promo/Menu Card Styles */
    .promo-img, .menu-img, .item-image {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 8px;
    }
    
    .menu-card, .menu-item {
      transition: transform 0.3s;
      cursor: pointer;
      border: none;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      border-radius: 8px;
      overflow: hidden;
      background: white;
      margin-bottom: 20px;
    }
    
    .menu-card:hover, .menu-item:hover {
      transform: translateY(-5px);
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }
    
    /* Order Page Specific Styles */
    .menu-section {
      background: white;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    
    .cart-section {
      background: white;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      position: sticky;
      top: 100px;
      height: fit-content;
    }
    
    .category-title {
      background-color: #e74c3c;
      color: white;
      padding: 10px 15px;
      border-radius: 5px;
      margin-bottom: 15px;
      font-size: 1.2rem;
    }
    
    .add-btn, .checkout-btn {
      background-color: #e74c3c;
      color: white;
      border: none;
      padding: 8px 15px;
      border-radius: 5px;
      cursor: pointer;
      width: 100%;
      transition: background-color 0.3s;
    }
    
    .add-btn:hover, .checkout-btn:hover {
      background-color: #c1122d;
    }
    
    .cart-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px 0;
      border-bottom: 1px solid #eee;
    }
    
    .quantity-btn {
      background-color: #f5f5f5;
      border: none;
      width: 25px;
      height: 25px;
      border-radius: 50%;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
    }
    
    .remove-btn {
      color: #e74c3c;
      background: none;
      border: none;
      cursor: pointer;
      margin-left: 10px;
    }
    
    /* About Page Styles */
    .about-section {
      padding: 60px 0;
      background-color: #fff;
    }
    
    .about-img {
      width: 100%;
      height: 200px;
      background-color: #ddd;
      border-radius: 8px;
      margin-bottom: 20px;
    }
    
    /* Footer Styles */
    .footer {
      background-color: #e74c3c;
      color: white;
      padding: 20px 0;
      margin-top: 60px;
    }
    
    .social-icon {
      color: white;
      font-size: 1.5rem;
      margin: 0 10px;
      transition: color 0.3s;
    }
    
    .social-icon:hover {
      color: #f1c40f;
    }
    
    /* Responsive Adjustments */
    @media (max-width: 768px) {
      .cart-section {
        position: static;
        margin-top: 30px;
      }
    }
  </style>
</head>
<body>

<!-- Navigation Bar -->
<nav class="navbar navbar-expand-lg">
  <div class="container">
    <a class="navbar-brand text-white fw-bold" href="#home"><i class="fas fa-utensils me-2"></i>Wendy's</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="#home">HOME</a></li>
        <li class="nav-item"><a class="nav-link" href="#menu">MENU</a></li>
        <li class="nav-item"><a class="nav-link" href="#order">ORDER</a></li>
        <li class="nav-item"><a class="nav-link" href="#about">ABOUT</a></li>
      </ul>
    </div>
  </div>
</nav>

<!-- Home Section -->
<section id="home" class="container text-center my-5 py-4">
  <h1 class="mb-4">Welcome to Wendy's</h1>
  <p class="lead">Delicious food served with love since 1969</p>
  
  <!-- Promo Section -->
  <h2 class="section-title mt-5">SPECIAL OFFERS</h2>
  <div class="row mt-4">
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img class="promo-img" src="https://th.bing.com/th/id/R.29dcab600ea1b85c4458906a582292ec?rik=WkOU%2bkVVrlf9Zg&riu=http%3a%2f%2fwww.investors.com%2fimage%2fDPZ-biz03-0301_345.jpg.cms&ehk=hvmnFmf%2fouMCWq6LOVRVz%2bCrgeuCNI3ytpKl%2b%2fM2Yb4%3d&risl=&pid=ImgRaw&r=0" alt="Pizza Special">
        <div class="card-body">
          <h5>Pizza Special</h5>
          <p>Large pizza + drink for $12.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img class="promo-img" src="https://th.bing.com/th/id/R.00516737c43c875eb9b42281d426d2a8?rik=LagRgzVJnldRJA&riu=http%3a%2f%2fwww.nanalyze.com%2fapp%2fuploads%2f2017%2f05%2fBurger-Future-Teaser.jpg&ehk=jozTTbO14ZboLf2uLuubQiBjPdw2nvnJ6lmkq4jwepY%3d&risl=&pid=ImgRaw&r=0" alt="Burger Combo">
        <div class="card-body">
          <h5>Burger Combo</h5>
          <p>Burger + fries + drink $8.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img class="promo-img" src="https://th.bing.com/th/id/R.1b1bfe0c9a409c667bc2a922cb04b0e4?rik=M8kRZ6dycAKsFg&riu=http%3a%2f%2fwendys.com.ph%2fcdn%2fshop%2fcollections%2fSpaghetti.png%3fv%3d1692071329&ehk=MzIcNRR05UdplueXymKi5uFQOlHhGYVVlKfRJz40Pz8%3d&risl=&pid=ImgRaw&r=0" alt="Pasta Night">
        <div class="card-body">
          <h5>Pasta Night</h5>
          <p>2 pastas + garlic bread $15.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img class="promo-img" src="https://media.clickorlando.com/photo/2019/05/01/wendys_1556722867233_21799516_ver1.0_1280_720.JPG" alt="Dessert Deal">
        <div class="card-body">
          <h5>Dessert Deal</h5>
          <p>2 desserts for $6.99</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Menu Section -->
<section id="menu" class="container text-center my-5 py-4">
  <h2 class="section-title">OUR MENU</h2>
  <div class="row mt-4 justify-content-center">
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img src="https://images.builderservices.io/s/cdn/v1.0/i/m?url=https:%2F%2Fstorage.googleapis.com%2Fproduction-hostgator_mexico-v1-0-0%2F690%2F94690%2FcoaK4MZY%2F1f34ad64fccb4d62883db31a719b8514&methods=resize%2C1000%2C5000" class="menu-img" alt="Pizza">
        <div class="card-body">
          <h5>Pizza</h5>
          <p>$12.99 - $18.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img src="https://tse3.mm.bing.net/th/id/OIP.Oj9ppaRfiy0FICs7w-pTtQHaHa?rs=1&pid=ImgDetMain&o=7&rm=3" class="menu-img" alt="Burger">
        <div class="card-body">
          <h5>Burger</h5>
          <p>$8.99 - $12.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img src="https://www.mashed.com/img/gallery/wendys-menu-items-you-cant-get-in-the-u-s/pasta-1715786584.jpg" class="menu-img" alt="Pasta">
        <div class="card-body">
          <h5>Pasta</h5>
          <p>$10.99 - $14.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img src="https://wendys.com.ph/cdn/shop/files/3-pcFriedChicken.png?v=1692067265&width=400" class="menu-img" alt="Fried Chicken">
        <div class="card-body">
          <h5>Fried Chicken</h5>
          <p>$9.99 - $15.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img src="https://www.wendys.com/sites/default/files/styles/max_650x650/public/2021-05/avocado-chicken-salad-1325_medium_US_en.png?itok=u9CGi7kS" class="menu-img" alt="Salad">
        <div class="card-body">
          <h5>Salad</h5>
          <p>$7.99 - $12.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img src="https://tse3.mm.bing.net/th/id/OIP.s79SRapmGEXyiwaexIPV1gHaE8?rs=1&pid=ImgDetMain&o=7&rm=3" class="menu-img" alt="Steak">
        <div class="card-body">
          <h5>Steak</h5>
          <p>$16.99 - $24.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img src="https://www.wendys.com/sites/default/files/styles/max_650x650/public/2021-05/fries-medium-22_medium_US_en.png?itok=oZZGj9O2" class="menu-img" alt="Fries">
        <div class="card-body">
          <h5>Fries</h5>
          <p>$3.99 - $5.99</p>
        </div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 mb-4">
      <div class="menu-card">
        <img src="https://media.clickorlando.com/photo/2019/05/01/wendys_1556722867233_21799516_ver1.0_1280_720.JPG" class="menu-img" alt="Dessert">
        <div class="card-body">
          <h5>Dessert</h5>
          <p>$4.99 - $8.99</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Order Section -->
<section id="order" class="container my-5 py-4">
  <div class="row">
    <div class="col-lg-8">
      <div class="menu-section">
        <h2 class="section-title">Order Online</h2>
        
        <div class="promo-section mb-4">
          <h3 class="category-title">Special Offers</h3>
          <div class="row">
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://th.bing.com/th/id/R.29dcab600ea1b85c4458906a582292ec?rik=WkOU%2bkVVrlf9Zg&riu=http%3a%2f%2fwww.investors.com%2fimage%2fDPZ-biz03-0301_345.jpg.cms&ehk=hvmnFmf%2fouMCWq6LOVRVz%2bCrgeuCNI3ytpKl%2b%2fM2Yb4%3d&risl=&pid=ImgRaw&r=0" alt="Pizza Special" class="item-image">
                <div class="item-name">Pizza Special</div>
                <div class="item-price">$12.99</div>
                <p class="mb-2">Large pizza + drink</p>
                <button class="add-btn" data-name="Pizza Special" data-price="12.99">Add to Cart</button>
              </div>
            </div>
            
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://th.bing.com/th/id/R.00516737c43c875eb9b42281d426d2a8?rik=LagRgzVJnldRJA&riu=http%3a%2f%2fwww.nanalyze.com%2fapp%2fuploads%2f2017%2f05%2fBurger-Future-Teaser.jpg&ehk=jozTTbO14ZboLf2uLuubQiBjPdw2nvnJ6lmkq4jwepY%3d&risl=&pid=ImgRaw&r=0" alt="Burger Combo" class="item-image">
                <div class="item-name">Burger Combo</div>
                <div class="item-price">$8.99</div>
                <p class="mb-2">Burger + fries + drink</p>
                <button class="add-btn" data-name="Burger Combo" data-price="8.99">Add to Cart</button>
              </div>
            </div>
            
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://th.bing.com/th/id/R.1b1bfe0c9a409c667bc2a922cb04b0e4?rik=M8kRZ6dycAKsFg&riu=http%3a%2f%2fwendys.com.ph%2fcdn%2fshop%2fcollections%2fSpaghetti.png%3fv%3d1692071329&ehk=MzIcNRR05UdplueXymKi5uFQOlHhGYVVlKfRJz40Pz8%3d&risl=&pid=ImgRaw&r=0" alt="Pasta Night" class="item-image">
                <div class="item-name">Pasta Night</div>
                <div class="item-price">$15.99</div>
                <p class="mb-2">2 pastas + garlic bread</p>
                <button class="add-btn" data-name="Pasta Night" data-price="15.99">Add to Cart</button>
              </div>
            </div>
          </div>
        </div>
        
        <div class="menu-category mb-4">
          <div class="category-title">Main Dishes</div>
          <div class="row">
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://images.builderservices.io/s/cdn/v1.0/i/m?url=https:%2F%2Fstorage.googleapis.com%2Fproduction-hostgator_mexico-v1-0-0%2F690%2F94690%2FcoaK4MZY%2F1f34ad64fccb4d62883db31a719b8514&methods=resize%2C1000%2C5000" alt="Pizza" class="item-image">
                <div class="item-name">Pizza</div>
                <div class="item-price">$12.99 - $18.99</div>
                <button class="add-btn" data-name="Pizza" data-price="12.99">Add to Cart</button>
              </div>
            </div>
            
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://tse3.mm.bing.net/th/id/OIP.Oj9ppaRfiy0FICs7w-pTtQHaHa?rs=1&pid=ImgDetMain&o=7&rm=3" alt="Burger" class="item-image">
                <div class="item-name">Burger</div>
                <div class="item-price">$8.99 - $12.99</div>
                <button class="add-btn" data-name="Burger" data-price="8.99">Add to Cart</button>
              </div>
            </div>
            
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://www.mashed.com/img/gallery/wendys-menu-items-you-cant-get-in-the-u-s/pasta-1715786584.jpg" alt="Pasta" class="item-image">
                <div class="item-name">Pasta</div>
                <div class="item-price">$10.99 - $14.99</div>
                <button class="add-btn" data-name="Pasta" data-price="10.99">Add to Cart</button>
              </div>
            </div>
            
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://wendys.com.ph/cdn/shop/files/3-pcFriedChicken.png?v=1692067265&width=400" alt="Fried Chicken" class="item-image">
                <div class="item-name">Fried Chicken</div>
                <div class="item-price">$9.99 - $15.99</div>
                <button class="add-btn" data-name="Fried Chicken" data-price="9.99">Add to Cart</button>
              </div>
            </div>
            
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://tse3.mm.bing.net/th/id/OIP.s79SRapmGEXyiwaexIPV1gHaE8?rs=1&pid=ImgDetMain&o=7&rm=3" alt="Steak" class="item-image">
                <div class="item-name">Steak</div>
                <div class="item-price">$16.99 - $24.99</div>
                <button class="add-btn" data-name="Steak" data-price="16.99">Add to Cart</button>
              </div>
            </div>
          </div>
        </div>
        
        <div class="menu-category">
          <div class="category-title">Other Items</div>
          <div class="row">
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://www.wendys.com/sites/default/files/styles/max_650x650/public/2021-05/avocado-chicken-salad-1325_medium_US_en.png?itok=u9CGi7kS" alt="Salad" class="item-image">
                <div class="item-name">Salad</div>
                <div class="item-price">$7.99 - $12.99</div>
                <button class="add-btn" data-name="Salad" data-price="7.99">Add to Cart</button>
              </div>
            </div>
            
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://www.wendys.com/sites/default/files/styles/max_650x650/public/2021-05/fries-medium-22_medium_US_en.png?itok=oZZGj9O2" alt="Fries" class="item-image">
                <div class="item-name">Fries</div>
                <div class="item-price">$3.99 - $5.99</div>
                <button class="add-btn" data-name="Fries" data-price="3.99">Add to Cart</button>
              </div>
            </div>
            
            <div class="col-md-4 mb-4">
              <div class="menu-item">
                <img src="https://media.clickorlando.com/photo/2019/05/01/wendys_1556722867233_21799516_ver1.0_1280_720.JPG" alt="Dessert" class="item-image">
                <div class="item-name">Dessert</div>
                <div class="item-price">$4.99 - $8.99</div>
                <button class="add-btn" data-name="Dessert" data-price="4.99">Add to Cart</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    
    <div class="col-lg-4">
      <div class="cart-section">
        <div class="cart-header">
          <h2 class="section-title">Your Order</h2>
          <span id="item-count">0 items</span>
        </div>
        
        <div class="cart-items" id="cart-items">
          <div class="empty-cart">Your cart is empty</div>
        </div>
        
        <div class="cart-total">
          Total: $<span id="total-price">0.00</span>
        </div>
        
        <button class="checkout-btn" id="checkout-btn">Checkout</button>
      </div>
    </div>
  </div>
</section>

<!-- About Section -->
<section id="about" class="about-section container my-5 py-4">
  <h2 class="section-title">ABOUT US</h2>
  <div class="row about-content align-items-center mb-4">
    <div class="col-md-4">
      <div class="about-img">
        <img src="https://th.bing.com/th/id/R.29dcab600ea1b85c4458906a582292ec?rik=WkOU%2bkVVrlf9Zg&riu=http%3a%2f%2fwww.investors.com%2fimage%2fDPZ-biz03-0301_345.jpg.cms&ehk=hvmnFmf%2fouMCWq6LOVRVz%2bCrgeuCNI3ytpKl%2b%2fM2Yb4%3d&risl=&pid=ImgRaw&r=0" alt="Our Restaurant" class="w-100 h-100" style="object-fit: cover;">
      </div>
    </div>
    <div class="col-md-8">
      <h3>Our Story</h3>
      <p>Founded in 1969, Wendy's has been serving quality food made with fresh ingredients for over 50 years. Our founder, Dave Thomas, believed in doing things the right way, not the easy way. That philosophy still guides us today as we continue to serve our customers with integrity and passion.</p>
    </div>
  </div>
  
  <div class="row about-content align-items-center flex-md-row-reverse mb-4">
    <div class="col-md-4">
      <div class="about-img">
        <img src="https://th.bing.com/th/id/R.00516737c43c875eb9b42281d426d2a8?rik=LagRgzVJnldRJA&riu=http%3a%2f%2fwww.nanalyze.com%2fapp%2fuploads%2f2017%2f05%2fBurger-Future-Teaser.jpg&ehk=jozTTbO14ZboLf2uLuubQiBjPdw2nvnJ6lmkq4jwepY%3d&risl=&pid=ImgRaw&r=0" alt="Our Ingredients" class="w-100 h-100" style="object-fit: cover;">
      </div>
    </div>
    <div class="col-md-8">
      <h3>Quality Ingredients</h3>
      <p>We source only the freshest ingredients for our menu items. From never-frozen beef to crisp vegetables and premium cheeses, we're committed to quality in every bite. Our suppliers meet our high standards for ethical sourcing and sustainable practices.</p>
    </div>
  </div>
  
  <div class="row about-content align-items-center mb-4">
    <div class="col-md-4">
      <div class="about-img">
        <img src="https://th.bing.com/th/id/R.1b1bfe0c9a409c667bc2a922cb04b0e4?rik=M8kRZ6dycAKsFg&riu=http%3a%2f%2fwendys.com.ph%2fcdn%2fshop%2fcollections%2fSpaghetti.png%3fv%3d1692071329&ehk=MzIcNRR05UdplueXymKi5uFQOlHhGYVVlKfRJz40Pz8%3d&risl=&pid=ImgRaw&r=0" alt="Our Team" class="w-100 h-100" style="object-fit: cover;">
      </div>
    </div>
    <div class="col-md-8">
      <h3>Our Team</h3>
      <p>Our dedicated team members are the heart of Wendy's. We invest in training and development to ensure every customer receives excellent service. Many of our employees have been with us for years, building relationships with our regular customers and creating a welcoming atmosphere.</p>
    </div>
  </div>
</section>

<!-- Footer -->
<footer class="footer text-center py-4">
  <div class="container">
    <div class="row">
      <div class="col-md-4 mb-4">
        <h5>QUICK LINKS</h5>
        <p><a href="#home" class="text-white">Home</a></p>
        <p><a href="#menu" class="text-white">Menu</a></p>
        <p><a href="#order" class="text-white">Order</a></p>
        <p><a href="#about" class="text-white">About</a></p>
      </div>
      <div class="col-md-4 mb-4">
        <h5>CONNECT WITH US</h5>
        <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
        <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
        <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
        <a href="#" class="social-icon"><i class="fab fa-yelp"></i></a>
      </div>
      <div class="col-md-4">
        <h5>CONTACT US</h5>
        <p><i class="fas fa-phone me-2"></i>(555) 123-4567</p>
        <p><i class="fas fa-envelope me-2"></i>info@wendys.com</p>
        <p><i class="fas fa-map-marker-alt me-2"></i>123 Main Street, City</p>
      </div>
    </div>
    <hr class="my-4 bg-light">
    <p>&copy; 2025 Wendy's. All rights reserved.</p>
  </div>
</footer>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>

<!-- Cart Functionality -->
<script>
  // Cart functionality
  const cart = {};
  const cartItemsEl = document.getElementById('cart-items');
  const itemCountEl = document.getElementById('item-count');
  const totalPriceEl = document.getElementById('total-price');
  const checkoutBtn = document.getElementById('checkout-btn');
  
  // Add to cart buttons
  document.querySelectorAll('.add-btn').forEach(button => {
    button.addEventListener('click', () => {
      const name = button.getAttribute('data-name');
      const price = parseFloat(button.getAttribute('data-price'));
      
      if (cart[name]) {
        cart[name].quantity++;
        cart[name].totalPrice += price;
      } else {
        cart[name] = {
          price: price,
          quantity: 1,
          totalPrice: price
        };
      }
      
      updateCart();
    });
  });
  
  // Update cart display
  function updateCart() {
    // Clear cart items
    cartItemsEl.innerHTML = '';
    
    let itemCount = 0;
    let totalPrice = 0;
    
    // Add each item to cart display
    for (const [name, item] of Object.entries(cart)) {
      itemCount += item.quantity;
      totalPrice += item.totalPrice;
      
      const cartItemEl = document.createElement('div');
      cartItemEl.className = 'cart-item';
      cartItemEl.innerHTML = `
        <div class="item-name">${name}</div>
        <div class="item-controls">
          <button class="quantity-btn minus" data-name="${name}">-</button>
          <span class="quantity">${item.quantity}</span>
          <button class="quantity-btn plus" data-name="${name}">+</button>
          <button class="remove-btn" data-name="${name}">×</button>
        </div>
        <div class="item-price">$${item.totalPrice.toFixed(2)}</div>
      `;
      
      cartItemsEl.appendChild(cartItemEl);
    }
    
    // Update counters
    itemCountEl.textContent = `${itemCount} ${itemCount === 1 ? 'item' : 'items'}`;
    totalPriceEl.textContent = totalPrice.toFixed(2);
    
    // If cart is empty, show empty message
    if (itemCount === 0) {
      cartItemsEl.innerHTML = '<div class="empty-cart">Your cart is empty</div>';
    }
    
    // Add event listeners to quantity buttons
    document.querySelectorAll('.minus').forEach(btn => {
      btn.addEventListener('click', (e) => {
        const name = e.target.getAttribute('data-name');
        if (cart[name].quantity > 1) {
          cart[name].quantity--;
          cart[name].totalPrice -= cart[name].price;
        } else {
          delete cart[name];
        }
        updateCart();
      });
    });
    
    document.querySelectorAll('.plus').forEach(btn => {
      btn.addEventListener('click', (e) => {
        const name = e.target.getAttribute('data-name');
        cart[name].quantity++;
        cart[name].totalPrice += cart[name].price;
        updateCart();
      });
    });
    
    document.querySelectorAll('.remove-btn').forEach(btn => {
      btn.addEventListener('click', (e) => {
        const name = e.target.getAttribute('data-name');
        delete cart[name];
        updateCart();
      });
    });
  }
  
  // Checkout button
  checkoutBtn.addEventListener('click', () => {
    if (Object.keys(cart).length === 0) {
      alert('Your cart is empty!');
    } else {
      alert(`Order placed! Total: $${totalPriceEl.textContent}`);
      // Clear cart
      for (const key in cart) {
        delete cart[key];
      }
      updateCart();
    }
  });
</script>
</body>
</html>
