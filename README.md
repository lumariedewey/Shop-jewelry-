# Lumarie's Shop Jewelry
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Joyería Elegante</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>Joyería Elegante</h1>
    <nav>
        <a href="index.html">Inicio</a>
        <a href="productos.html">Productos</a>
        <a href="carrito.html">Carrito (<span id="cart-count">0</span>)</a>
    </nav>
</header>

<section class="hero">
    <h2>Descubre la Elegancia en Cada Detalle</h2>
    <p>Las mejores joyas para cada ocasión.</p>
    <a href="productos.html" class="btn">Ver Productos</a>
</section>

</body>
</html>

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Productos - Joyería Elegante</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<section class="productos">
    <h2>Nuestras Joyas</h2>
    <div class="lista-productos">
        <div class="producto">
            <img src="img/anillo.jpg" alt="Anillo de Oro">
            <h3>Anillo de Oro</h3>
            <p>$120</p>
            <button onclick="agregarAlCarrito('Anillo de Oro', 120)">Añadir al carrito</button>
        </div>
        <div class="producto">
            <img src="img/collar.jpg" alt="Collar de Plata">
            <h3>Collar de Plata</h3>
            <p>$90</p>
            <button onclick="agregarAlCarrito('Collar de Plata', 90)">Añadir al carrito</button>
        </div>
    </div>
</section>
</body>
</html>

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carrito - Joyería Elegante</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<section class="carrito">
    <h2>Carrito de Compras</h2>
    <div id="lista-carrito"></div>
    <h3>Total: $<span id="total"></span></h3>
    <button onclick="vaciarCarrito()">Vaciar Carrito</button>
</section>

</body>
</html>