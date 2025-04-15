<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Avalon</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">

  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
    }

    .video-bg {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      z-index: -1;
    }

    .bg-overlay {
      background-color: rgba(255, 255, 255, 0.3); /* Reducido a 0.3 para más transparencia */
      backdrop-filter: blur(4px);
    }

    .img-container {
      position: relative;
      width: 100%;
      padding-top: 130%;
      overflow: hidden;
      border-radius: 0.5rem;
    }

    .img-container img {
      position: absolute;
      top: 0;
      left: 0;
      transition: opacity 0.3s ease-in-out;
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .img-container img.atras {
      opacity: 0;
    }

    .img-container:hover img.frente {
      opacity: 0;
    }

    .img-container:hover img.atras {
      opacity: 1;
    }
  </style>
</head>
<body class="text-gray-900">
  <!-- Video de fondo -->
  <video autoplay muted loop class="video-bg">
    <source src="videoavalon-fondo.mp4 - copia.mp4" type="video/mp4">
    Tu navegador no soporta la reproducción de video.
  </video>

  <!-- Contenido principal con fondo translúcido -->
  <div class="bg-overlay">

    <!-- Encabezado -->
    <header class="bg-white shadow-md p-4">
      <div class="max-w-6xl mx-auto flex justify-between items-center">
        <h1 class="text-2xl font-bold">Avalon</h1>
        <nav class="flex items-center space-x-4">
          <a href="#" class="hover:text-blue-600">Inicio</a>
          <a href="#productos" class="hover:text-blue-600">Productos</a>
          <a href="#contacto" class="hover:text-blue-600">Contacto</a>
          <a href="#carrito" class="hover:text-blue-600 font-semibold">🛒 Carrito (<span id="carrito-contador">0</span>)</a>
        </nav>
      </div>
    </header>

    <!-- Banner -->
    <section class="bg-blue-100 text-center py-12 bg-opacity-80">
      <h2 class="text-4xl font-bold mb-2">¡Nuevas playeras disponibles!</h2>
      <p class="text-lg">Envíos a todo México - Paga en línea con seguridad</p>
      <p class="text-lg">Inspirada en lo místico, lo épico y lo exclusivo, cada prenda está hecha para quienes no siguen tendencias, las imponen.<br>
        Bienvenido a un estilo de vida donde la actitud es ley y lo ordinario no tiene lugar.<br>
        "Live the Avalon way."
      </p>
    </section>

    <!-- Productos -->
    <section id="productos" class="max-w-6xl mx-auto py-10">
      <h2 class="text-3xl font-bold text-center mb-6">Catálogo de productos</h2>
      <div id="productos-container" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
        <!-- Los productos se agregan con JS -->
      </div>
    </section>

    <!-- Carrito -->
    <section id="carrito" class="max-w-6xl mx-auto py-10">
      <h2 class="text-3xl font-bold text-center mb-6">Tu Carrito</h2>
      <div id="carrito-container" class="bg-white p-6 rounded-lg shadow-md">
        <p id="carrito-vacio" class="text-center text-gray-600">Tu carrito está vacío.</p>
      </div>
      <div class="text-center mt-6">
        <button onclick="realizarPago()" class="bg-green-600 text-white px-6 py-2 rounded hover:bg-green-700">Realizar Pago</button>
      </div>
    </section>

    <!-- Contacto -->
    <section id="contacto" class="bg-white py-10">
      <div class="max-w-4xl mx-auto text-center">
        <h2 class="text-3xl font-bold mb-4">Contáctanos</h2>
        <p class="mb-4">¿Tienes dudas o pedidos personalizados?</p>
        <p>📞 Celular: +56 3911 4559</p>
        <p>📞 Celular: +52 3318 6076 73</p>
        <p>📧 Correo: tienda@avalon.mx</p>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white text-center p-4">
      © 2025 Tienda Avalon - Todos los derechos reservados
    </footer>

  </div>

  <!-- Scripts -->
  <script>
    const productos = [
      { id: 1, nombre: "Playera Negra Estampada", frente: "playera1-frente.jpg.jpg", atras: "playera1-atras.jpg.jpg", precio: 799 },
      { id: 2, nombre: "Playera Blanca Logo", frente: "playera2-frente.jpg.jpg", atras: "playera2-atras.jpg.jpg", precio: 799 },
      { id: 3, nombre: "Playera Oversize Edición", frente: "playera6-frente.jpg.jpg", atras: "playera6-atras.jpg.jpg", precio: 799 },
      { id: 4, nombre: "Playera Avalon Street", frente: "playera4-frente.jpg.jpg", atras: "playera4-atras.jpg.jpg", precio: 799 },
      { id: 5, nombre: "Playera Arte Runas", frente: "playera5-frente.jpg.jpg", atras: "playera5-atras.jpg.jpg", precio: 799 },
      { id: 6, nombre: "Playera Estandarte Avalon", frente: "playera3-frente.jpg.jpg", atras: "playera3-atras.jpg.jpg", precio: 799 },
      { id: 7, nombre: "Playera Guerreros del Norte", frente: "playera7-frente.jpg", atras: "playera7-atras.jpg", precio: 799 },
      { id: 8, nombre: "Playera Espada Legendaria", frente: "playera8-frente.jpg", atras: "playera8-atras.jpg", precio: 799 },
      { id: 9, nombre: "Playera Emblema Mágico", frente: "playera9-frente.jpg", atras: "playera9-atras.jpg", precio: 799 },
      { id: 10, nombre: "Playera Mística Avalon", frente: "playera10-frente.jpg", atras: "playera10-atras.jpg", precio: 799 },
      { id: 11, nombre: "Playera Dragón Celestial", frente: "playera11-frente.jpg.jpg", atras: "playera11-atras.jpg.jpg", precio: 799 },
      { id: 12, nombre: "Playera Espíritu del Bosque", frente: "playera12-frente.jpg.jpg", atras: "playera12-atras.jpg.jpg", precio: 799 },
      { id: 13, nombre: "Playera Sello del Rey", frente: "playera13-frente.jpg.jpg", atras: "playera13-atras.jpg.jpg", precio: 799 },
      { id: 14, nombre: "Playera Círculo Arcano", frente: "playera14-frente.jpg.jpg", atras: "playera14-atras.jpg.jpg", precio: 799 },
      { id: 15, nombre: "Playera Legado de Avalon", frente: "playera15-frente.jpg.jpg", atras: "playera15-atras.jpg.jpg", precio: 799 },
      { id: 16, nombre: "Playera Reino Olvidado", frente: "playera16-frente.jpg.jpg", atras: "playera16-atras.jpg.jpg", precio: 799 }
    ];

    const carrito = [];
    const productosContainer = document.getElementById("productos-container");
    const carritoContainer = document.getElementById("carrito-container");
    const contadorCarrito = document.getElementById("carrito-contador");
    const carritoVacio = document.getElementById("carrito-vacio");

    function renderProductos() {
      productosContainer.innerHTML = "";
      productos.forEach(prod => {
        productosContainer.innerHTML += `
          <div class="bg-white p-4 shadow-md rounded-lg">
            <div class="img-container mb-4">
              <img src="${prod.frente}" alt="Frente" class="frente">
              <img src="${prod.atras}" alt="Atrás" class="atras">
            </div>
            <h3 class="text-xl font-semibold">${prod.nombre}</h3>
            <p class="text-gray-700">$${prod.precio} MXN</p>
            <button onclick="mostrarTallas(${prod.id})" class="mt-2 ml-2 bg-gray-500 text-white px-4 py-2 rounded hover:bg-gray-700">Info Tallas</button>
            <div id="tallas-${prod.id}" class="hidden mt-2 text-sm text-gray-700">
              <label for="talla-${prod.id}">Selecciona una talla:</label>
              <select id="talla-${prod.id}" class="mt-1 p-2">
                <option value="XS">XS</option>
                <option value="S">S</option>
                <option value="M">M</option>
                <option value="L">L</option>
                <option value="XL">XL</option>
              </select>
              <button onclick="agregarAlCarritoConTalla(${prod.id})" class="mt-2 bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">Agregar al carrito</button>
            </div>
          </div>
        `;
      });
    }

    function agregarAlCarritoConTalla(id) {
      const tallaSeleccionada = document.getElementById(`talla-${id}`).value;
      const producto = productos.find(p => p.id === id);
      carrito.push({ ...producto, talla: tallaSeleccionada });
      actualizarCarrito();
    }

    function eliminarDelCarrito(index) {
      carrito.splice(index, 1);
      actualizarCarrito();
    }

    function actualizarCarrito() {
      carritoContainer.innerHTML = "";
      if (carrito.length === 0) {
        carritoContainer.innerHTML = `<p id="carrito-vacio" class="text-center text-gray-600">Tu carrito está vacío.</p>`;
      } else {
        carrito.forEach((prod, index) => {
          carritoContainer.innerHTML += `
            <div class="flex justify-between items-center border-b py-2">
              <p>${prod.nombre} - Talla: ${prod.talla} - $${prod.precio} MXN</p>
              <button onclick="eliminarDelCarrito(${index})" class="text-red-600 hover:underline">❌</button>
            </div>
          `;
        });
      }
      contadorCarrito.innerText = carrito.length;
    }

    function realizarPago() {
      if (carrito.length === 0) {
        alert("Tu carrito está vacío.");
        return;
      }
      alert("Procesando pago... (aquí iría la integración con la pasarela de pago)");
    }

    function mostrarTallas(id) {
      const tallaDiv = document.getElementById(`tallas-${id}`);
      tallaDiv.classList.toggle("hidden");
    }

    renderProductos();
  </script>
</body>
</html>
