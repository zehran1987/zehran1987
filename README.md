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
</body>
</html>
