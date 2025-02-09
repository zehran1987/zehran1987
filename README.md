<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Shopping Website</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>My Shopping Website</h1>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Shop</a></li>
        <li><a href="#">Cart</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="products">
      <div class="product">
        <img src="product1.jpg" alt="Product 1">
        <h3>Product 1</h3>
        <p>$20.00</p>
        <button onclick="addToCart('Product 1', 20)">Add to Cart</button>
      </div>
      <div class="product">
        <img src="product2.jpg" alt="Product 2">
        <h3>Product 2</h3>
        <p>$30.00</p>
        <button onclick="addToCart('Product 2', 30)">Add to Cart</button>
      </div>
      <div class="product">
        <img src="product3.jpg" alt="Product 3">
        <h3>Product 3</h3>
        <p>$25.00</p>
        <button onclick="addToCart('Product 3', 25)">Add to Cart</button>
      </div>
    </section>

    <section class="cart">
      <h2>Shopping Cart</h2>
      <ul id="cart-items"></ul>
      <p>Total: $<span id="cart-total">0.00</span></p>
      <button onclick="checkout()">Checkout</button>
    </section>
  </main>

  <footer>
    <p>&copy; 2023 My Shopping Website</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f4f4f4;
}

header {
  background-color: #333;
  color: #fff;
  padding: 10px 0;
  text-align: center;
}

header h1 {
  margin: 0;
}

nav ul {
  list-style: none;
  padding: 0;
}

nav ul li {
  display: inline;
  margin: 0 10px;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
}

main {
  padding: 20px;
}

.products {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.product {
  background-color: #fff;
  border: 1px solid #ddd;
  padding: 20px;
  margin: 10px;
  text-align: center;
  width: 200px;
}

.product img {
  max-width: 100%;
  height: auto;
}

.cart {
  margin-top: 20px;
  background-color: #fff;
  padding: 20px;
  border: 1px solid #ddd;
}

footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 10px 0;
  position: fixed;
  width: 100%;
  bottom: 0;
}
        <button onclick="addToCart('Product 3', 25)">Add to Cart</button>
      </div>
    </section>

    <section class="cart">
      <h2>Shopping Cart</h2>
      <ul id="cart-items"></ul>
      <p>Total: $<span id="cart-total">0.00</span></p>
      <button onclick="checkout()">Checkout</button>
    </section>
  </main>

  <footer>
    <p>&copy; 2023 My Shopping Website</p>
  </footer>

  <script src="script.js"></script>
  let cart = [];
let total = 0;

function addToCart(name, price) {
  cart.push({ name, price });
  total += price;
  updateCart();
}

function updateCart() {
  const cartItems = document.getElementById('cart-items');
  const cartTotal = document.getElementById('cart-total');
  
  // Clear the cart display
  cartItems.innerHTML = '';
  
  // Add each item to the cart display
  cart.forEach(item => {
    const li = document.createElement('li');
    li.textContent = `${item.name} - $${item.price.toFixed(2)}`;
    cartItems.appendChild(li);
  });

  // Update the total
  cartTotal.textContent = total.toFixed(2);
}

function checkout() {
  alert(`Thank you for your purchase! Total: $${total.toFixed(2)}`);
  cart = [];
  total = 0;
  updateCart();
}
</body>
</html>
