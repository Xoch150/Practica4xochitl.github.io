# Practica4xochitl.github.io
Xochitl López Román
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SportStep - Tienda de Tenis Deportivos</title>
    <style>
        /* Estilos generales */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
        }
        
        /* Header */
        header {
            background-color: #000;
            color: white;
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
            color: #fff;
        }
        
        .logo span {
            color: #ff6b00;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #ff6b00;
        }
        
        /* Hero Section */
        .hero {
            background-image: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 500px;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
        }
        
        .hero-content h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero-content p {
            font-size: 20px;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: #ff6b00;
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #e05d00;
        }
        
        /* Featured Products */
        .section-title {
            text-align: center;
            margin: 60px 0 40px;
            font-size: 36px;
        }
        
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }
        
        .product-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
        }
        
        .product-img {
            height: 250px;
            overflow: hidden;
        }
        
        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .product-card:hover .product-img img {
            transform: scale(1.1);
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-info h3 {
            font-size: 20px;
            margin-bottom: 10px;
        }
        
        .product-info p {
            color: #666;
            margin-bottom: 15px;
        }
        
        .price {
            font-size: 22px;
            font-weight: bold;
            color: #ff6b00;
            margin-bottom: 15px;
        }
        
        /* Categories */
        .categories {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 60px;
        }
        
        .category-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            width: 200px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .category-card:hover {
            transform: translateY(-5px);
        }
        
        .category-img {
            height: 150px;
            overflow: hidden;
        }
        
        .category-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .category-info {
            padding: 15px;
        }
        
        .category-info h3 {
            font-size: 18px;
        }
        
        /* Payment Methods */
        .payment-methods {
            background-color: #fff;
            padding: 60px 0;
            margin-bottom: 60px;
        }
        
        .payment-content {
            text-align: center;
        }
        
        .payment-icons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 30px;
        }
        
        .payment-icon {
            font-size: 40px;
            color: #555;
        }
        
        /* Testimonials */
        .testimonials {
            margin-bottom: 60px;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
            color: #555;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 15px;
        }
        
        .author-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .author-info h4 {
            font-size: 18px;
            margin-bottom: 5px;
        }
        
        .author-info p {
            color: #777;
            font-size: 14px;
        }
        
        /* Footer */
        footer {
            background-color: #222;
            color: white;
            padding: 60px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 20px;
            margin-bottom: 20px;
            color: #ff6b00;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            color: white;
            font-size: 20px;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: #ff6b00;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #bbb;
            font-size: 14px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero {
                height: 400px;
            }
            
            .hero-content h1 {
                font-size: 36px;
            }
            
            .hero-content p {
                font-size: 18px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">Sport<span>Step</span></div>
                <nav>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#productos">Productos</a></li>
                        <li><a href="#categorias">Categorías</a></li>
                        <li><a href="#pagos">Métodos de Pago</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="container">
            <div class="hero-content">
                <h1>Los Mejores Tenis Deportivos</h1>
                <p>Encuentra el par perfecto para tu estilo y rendimiento</p>
                <a href="#productos" class="btn">Ver Colección</a>
            </div>
        </div>
    </section>
    
    <!-- Featured Products -->
    <section class="container" id="productos">
        <h2 class="section-title">Productos Destacados</h2>
        <div class="products">
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1600269452121-4f2416e55c28?ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80" alt="Tenis Running Pro">
                </div>
                <div class="product-info">
                    <h3>Running Pro X</h3>
                    <p>Tenis de alto rendimiento para corredores</p>
                    <div class="price">$1,299.00</div>
                    <a href="#" class="btn">Comprar Ahora</a>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1600185365483-26d7a4cc7519?ixlib=rb-1.2.1&auto=format&fit=crop&w=1025&q=80" alt="Tenis Basketball Elite">
                </div>
                <div class="product-info">
                    <h3>Basketball Elite</h3>
                    <p>Diseñados para máximo soporte en la cancha</p>
                    <div class="price">$1,499.00</div>
                    <a href="#" class="btn">Comprar Ahora</a>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1543508282-6319a3e2621f?ixlib=rb-1.2.1&auto=format&fit=crop&w=658&q=80" alt="Tenis Casual Street">
                </div>
                <div class="product-info">
                    <h3>Casual Street</h3>
                    <p>Estilo urbano con máxima comodidad</p>
                    <div class="price">$999.00</div>
                    <a href="#" class="btn">Comprar Ahora</a>
                </div>
            </div>
            
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1605348532760-6753d2c38ed8?ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80" alt="Tenis Trail Adventure">
                </div>
                <div class="product-info">
                    <h3>Trail Adventure</h3>
                    <p>Perfectos para senderismo y terrenos difíciles</p>
                    <div class="price">$1,199.00</div>
                    <a href="#" class="btn">Comprar Ahora</a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Categories -->
    <section class="container" id="categorias">
        <h2 class="section-title">Nuestras Categorías</h2>
        <div class="categories">
            <div class="category-card">
                <div class="category-img">
                    <img src="https://images.unsplash.com/photo-1460353581641-37baddab0fa2?ixlib=rb-1.2.1&auto=format&fit=crop&w=1351&q=80" alt="Running">
                </div>
                <div class="category-info">
                    <h3>Running</h3>
                </div>
            </div>
            
            <div class="category-card">
                <div class="category-img">
                    <img src="https://images.unsplash.com/photo-1600269452121-4f2416e55c28?ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80" alt="Basketball">
                </div>
                <div class="category-info">
                    <h3>Basketball</h3>
                </div>
            </div>
            
            <div class="category-card">
                <div class="category-img">
                    <img src="https://images.unsplash.com/photo-1542272604-787c3835535d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1226&q=80" alt="Fútbol">
                </div>
                <div class="category-info">
                    <h3>Fútbol</h3>
                </div>
            </div>
            
            <div class="category-card">
                <div class="category-img">
                    <img src="https://images.unsplash.com/photo-1543508282-6319a3e2621f?ixlib=rb-1.2.1&auto=format&fit=crop&w=658&q=80" alt="Casual">
                </div>
                <div class="category-info">
                    <h3>Casual</h3>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Payment Methods -->
    <section class="payment-methods" id="pagos">
        <div class="container">
            <div class="payment-content">
                <h2 class="section-title">Métodos de Pago</h2>
                <p>Aceptamos todas las formas de pago para tu comodidad</p>
                <div class="payment-icons">
                    <div class="payment-icon">
                        <i class="fab fa-cc-visa"></i>
                    </div>
                    <div class="payment-icon">
                        <i class="fab fa-cc-mastercard"></i>
                    </div>
                    <div class="payment-icon">
                        <i class="fab fa-cc-amex"></i>
                    </div>
                    <div class="payment-icon">
                        <i class="fab fa-cc-paypal"></i>
                    </div>
                    <div class="payment-icon">
                        <i class="fas fa-money-bill-wave"></i>
                    </div>
                    <div class="payment-icon">
                        <i class="fas fa-university"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Testimonials -->
    <section class="testimonials container">
        <h2 class="section-title">Lo que dicen nuestros clientes</h2>
        <div class="testimonial-grid">
            <div class="testimonial-card">
                <div class="testimonial-text">
                    "Los tenis Running Pro X son increíbles. Los he usado para dos maratones y el soporte es perfecto. ¡Los recomiendo totalmente!"
                </div>
                <div class="testimonial-author">
                    <div class="author-img">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Carlos M.">
                    </div>
                    <div class="author-info">
                        <h4>Carlos M.</h4>
                        <p>Corredor profesional</p>
                    </div>
                </div>
            </div>
            
            <div class="testimonial-card">
                <div class="testimonial-text">
                    "Compré los Casual Street y son los tenis más cómodos que he tenido. Además, recibo muchos cumplidos por su estilo."
                </div>
                <div class="testimonial-author">
                    <div class="author-img">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Ana L.">
                    </div>
                    <div class="author-info">
                        <h4>Ana L.</h4>
                        <p>Estudiante</p>
                    </div>
                </div>
            </div>
            
            <div class="testimonial-card">
                <div class="testimonial-text">
                    "Excelente servicio al cliente y entrega rápida. Los tenis de basketball superaron mis expectativas en calidad y durabilidad."
                </div>
                <div class="testimonial-author">
                    <div class="author-img">
                        <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Javier R.">
                    </div>
                    <div class="author-info">
                        <h4>Javier R.</h4>
                        <p>Jugador de basketball</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer id="contacto">
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>SportStep</h3>
                    <p>Tu tienda de confianza para tenis deportivos de alta calidad.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Enlaces Rápidos</h3>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#productos">Productos</a></li>
                        <li><a href="#categorias">Categorías</a></li>
                        <li><a href="#pagos">Métodos de Pago</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Contacto</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> Av. Principal 123, CDMX</li>
                        <li><i class="fas fa-phone"></i> +52 55 1234 5678</li>
                        <li><i class="fas fa-envelope"></i> info@sportstep.com</li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Horario</h3>
                    <ul>
                        <li>Lunes - Viernes: 9am - 8pm</li>
                        <li>Sábado: 10am - 6pm</li>
                        <li>Domingo: 11am - 4pm</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 SportStep. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>
</body>
</html>
