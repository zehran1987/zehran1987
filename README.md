<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Zubaiyr Shaikh </title>
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
