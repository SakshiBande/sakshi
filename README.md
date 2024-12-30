<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shopping Website</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css">
    <link rel="stylesheet" href="r.css">
</head>
<body>
    <header>
        <div class="navbar">
         <div class="nav-logo border">
         <div class="logo"></div>
         </div>
         <div class="nav-address border">
            <p>Deliver to</p>
            <div class="add-icon">
            <i class="fa-solid fa-location-dot"></i>
            </div>
         </div>
         <div class="nav-search">
            <select>
                <option>All</option>
            </select>
            <input placeholder="Search .." class="search-input">
            <div class="search-icon">
            <i class="fa-solid fa-magnifying-glass"></i>
        </div>
         </div>
         <div class="nav-signin border">
          <a href="f.html">wishlist</a><br>
            <a href="login1.html">sign in</a>
            <p class="nav-second"> Account & lists</p>
           </div>
           <div class="nav-return border">
            <p><span>Returns</span> </p>
            <p class="nav-second">& Orders</p>
           </div>
           <div id="cart-icon" class="cart-icon">
            🛒
          </div>
          <div id="cart-modal" class="cart-modal">
            <div class="cart-modal-content">
              <span id="close-cart" class="close-cart">&times;</span>
              <h2>Your Cart</h2>
              <ul id="cart-items-list">
              </ul>
              <button id="checkout-btn">Checkout</button>
            </div>
          </div>
           </div>
           <div class="panel">
            <div class="panel-all">
                <i class="fa-solid fa-bars"></i>
                <option value="search-input">Gardening</option>
            </div>
            <div class="panel-ops">
                <p>Today's Deal</p>
                <p>Customer Service</p>
                <p>Gift Cards</p>
                <p>Registry</p>
                <p>sell</p>
            </div>
            <div class="panel-deals">
                Shop Deals
            </div>
        </div>
    </header>
    <div class="hero-section" style="background-image: url('hero1.jpg');">
    </div>
    <div class="shop-section">
        <div class="box0 box">
            <div class="box-content">
                <h2>Sports</h2>
                <div class="box-img" style="background-image: url('i1.jpg');"></div>
                <a href="sports.html" class="shop-now">Explore more</a>
            </div>
        </div>
        <div class="box1 box">
            <div class="box-content">
                <h2>Gardening</h2>
                <div class="box-img" style="background-image: url('p1.webp');"></div>
                <a href="box1.html" class="shop-now">Shop now</a>
            </div>
        </div>
        <div class="box2 box">
            <div class="box-content">
                <h2> Start your Fitness Journey</h2>
                <div class="box-img" style="background-image: url('box2.jpg');"></div>
                <p>Shop now</p>
            </div>
        </div>
        <div class="box3 box">
            <div class="box-content">
                <h2>upto 60% off| E-books & Books</h2>
                <div class="box-img" style="background-image: url('box3.webp');"></div>
                <p>Shop now</p>
            </div>
        </div>
        <div class="box4 box">
            <div class="box-content">
                <h2>starting at ₹ 300| Kids Clothes & Collection</h2>
                <div class="box-img" style="background-image: url('box4.jpg');"></div>
                <p>Shop now</p>
            </div>
        </div>
        <div class="box5 box">
            <div class="box-content">
                <h2>Car, Bike parts & Accessories</h2>
                <div class="box-img" style="background-image: url('i.jpg');"></div>
                <p>Shop now</p>
            </div>
        </div>
        <div class="box6 box">
            <div class="box-content">
                <h2>Travel</h2>
                <div class="box-img" style="background-image: url('box5.jpg');"></div>
                <p>Shop now</p>
            </div>
        </div>
        <div class="box7 box">
            <div class="box-content">
                <h2>Grocery</h2>
                <div class="box-img" style="background-image: url('g.jpg');"></div>
                <p>Shop now</p>
            </div>
        </div>
    </div>
    <script>
        // Get elements
        const cartIcon = document.getElementById('cart-icon');
        const cartModal = document.getElementById('cart-modal');
        const closeCart = document.getElementById('close-cart');
        const addToCartButtons = document.querySelectorAll('.add-to-cart');
        const cartItemsList = document.getElementById('cart-items-list');
        // Cart storage
        let cartItems = [];
        // Open the cart modal when the cart icon is clicked
        cartIcon.addEventListener('click', () => {
          cartModal.style.display = 'block';
        });
        // Close the cart modal when the close button is clicked
        closeCart.addEventListener('click', () => {
          cartModal.style.display = 'none';
        });
        // Add product to the cart and show alert message
        addToCartButtons.forEach(button => {
          button.addEventListener('click', () => {
            const productName = button.getAttribute('data-product');
            cartItems.push(productName);
            updateCartItems();
            // Show alert message
            alert(`${productName} has been added to your cart!`);
          });
        });
        // Update the cart modal with the items
        function updateCartItems() {
          cartItemsList.innerHTML = ''; // Clear the list
          cartItems.forEach(item => {
            const listItem = document.createElement('li');
            listItem.textContent = item;
            cartItemsList.appendChild(listItem);
          });
        }
      </script>
    <footer>
        <div class="foot-panel1">
            <a href="ss.html">About Us</a>
        </div>
        <div class="footpanel2">
            <ul>
           <a>Connect with Us</a>
           <a><i class="fa-brands fa-facebook"></i>
            Facebook</a>
           <a><i class="fa-brands fa-x-twitter"></i>
            Twitter</a>
           <a><i class="fa-brands fa-square-instagram"></i>
            Instagram</a>
        </ul>
        <ul>
            <a>Let Us Help You</a>
              <a>Your Account</a>  
                <a>Returns Centre</a>
                <a>Recalls and Product Safety Alerts</a>
               <a>100% Purchase Protection</a> 
              <a>Help</a>  
    
         </ul>
         <ul>
            <a>MAil us</a>
            <a>Sakshi private limited
                
            </a>
         </ul>
        </div>
        <div class="footpanel3">
            <div class="logo">
            </div>
            </div>
                <div class="pages">
            <div class="footpanel4">  
                <div class="copyright">
                    © 1996-2024, Amazon.com, Inc. or its affiliates
                </div>
                </div>
                
    </footer>
</body>
</html>
    

