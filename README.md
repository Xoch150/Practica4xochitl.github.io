<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Venta de Flores</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #fef7f2;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #ffb6b9;
      color: white;
      padding: 20px;
      text-align: center;
    }
    .contenedor {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 30px;
    }
    .producto {
      background-color: white;
      border-radius: 12px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      overflow: hidden;
      text-align: center;
    }
    .producto img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }
    .producto h3 {
      margin: 10px 0 5px;
    }
    .producto p {
      color: #e91e63;
      font-weight: bold;
      margin-bottom: 15px;
    }
  </style>
</head>
<body>

  <header>
    <h1>Flores para Toda Ocasión</h1>
    <p>Encuentra la flor perfecta para regalar</p>
  </header>

  <div class="contenedor">
    <div class="producto">
      <img src="https://cdn.pixabay.com/photo/2016/11/29/03/53/rose-1867537_1280.jpg" alt="Rosa Roja">
      <h3>Rosa Roja</h3>
      <p>$50.00 MXN</p>
    </div>
    <div class="producto">
      <img src="https://cdn.pixabay.com/photo/2016/03/05/19/02/tulips-1238286_1280.jpg" alt="Tulipanes">
      <h3>Tulipanes</h3>
      <p>$70.00 MXN</p>
    </div>
    <div class="producto">
      <img src="https://cdn.pixabay.com/photo/2014/06/02/06/56/sunflowers-360881_1280.jpg" alt="Girasoles">
      <h3>Girasoles</h3>
      <p>$60.00 MXN</p>
    </div>
    <div class="producto">
      <img src="https://cdn.pixabay.com/photo/2018/09/30/17/10/daisies-3718081_1280.jpg" alt="Margaritas">
      <h3>Margaritas</h3>
      <p>$40.00 MXN</p>
    </div>
  </div>

</body>
</html>
