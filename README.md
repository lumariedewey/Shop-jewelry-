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
</section>

</body>
</html>

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

<script src="script.js"></script>
</body>
</html>

<section class="carrito">
    <h2>Carrito de Compras</h2>
    <div id="lista-carrito"></div>
    <h3>Total: $<span id="total"></span></h3>
    <button onclick="vaciarCarrito()">Vaciar Carrito</button>
</section>

<script>
    let carrito = JSON.parse(localStorage.getItem("carrito")) || [];

    function mostrarCarrito() {
        let listaCarrito = document.getElementById("lista-carrito");
        let total = 0;
        listaCarrito.innerHTML = "";

        carrito.forEach((producto, index) => {
            total += producto.precio;
            listaCarrito.innerHTML += `<p>${producto.nombre} - $${producto.precio} <button onclick="eliminarProducto(${index})">X</button></p>`;
        });

        document.getElementById("total").innerText = total;
        document.getElementById("cart-count").innerText = carrito.length;
    }

    function eliminarProducto(index) {
        carrito.splice(index, 1);
        localStorage.setItem("carrito", JSON.stringify(carrito));
        mostrarCarrito();
    }

    function vaciarCarrito() {
        carrito = [];
        localStorage.setItem("carrito", JSON.stringify(carrito));
        mostrarCarrito();
    }

    document.addEventListener("DOMContentLoaded", mostrarCarrito);
</script>

</body>
</html>