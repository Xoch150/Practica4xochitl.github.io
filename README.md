<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Tienda de Ropa Deportiva</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>🏋️ Tienda de Ropa Deportiva</h1>
  </header>

  <section class="products">
    <div class="product">
      <img src="https://via.placeholder.com/150" alt="Camiseta Deportiva">
      <h2>Camiseta Deportiva</h2>
      <p>$15.00</p>
      <button onclick="addToCart('Camiseta Deportiva', 15)">Agregar al carrito</button>
    </div>

    <div class="product">
      <img src="https://via.placeholder.com/150" alt="Pantalón Deportivo">
      <h2>Pantalón Deportivo</h2>
      <p>$25.00</p>
      <button onclick="addToCart('Pantalón Deportivo', 25)">Agregar al carrito</button>
    </div>

    <div class="product">
      <img src="https://via.placeholder.com/150" alt="Chaqueta Deportiva">
      <h2>Chaqueta Deportiva</h2>
      <p>$40.00</p>
      <button onclick="addToCart('Chaqueta Deportiva', 40)">Agregar al carrito</button>
    </div>
  </section>

  <section class="cart">
    <h2>🛒 Carrito</h2>
    <ul id="cart-list"></ul>
    <p>Total: $<span id="total">0</span></p>
  </section>

  <script src="script.js"></script>
</body>
</html>
