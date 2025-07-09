<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Computación Cuántica - La Revolución del Siglo XXI</title>
    <style>
        :root {
            --primary: #140e1df5; /* Morado más claro */
            --secondary: #80146e7a; /* Morado secundario más claro */
            --accent: #f7258441;
            --light: #45529100;
            --dark: #212529;
            --gray: #546879;
            --success: #4cc9f0;
            --team-card-border: #ee75d42d; /* Color para el borde de las tarjetas de equipo */
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #c7bebe; /* Fondo gris claro para el cuerpo */
            color: var(--dark); /* Texto oscuro para el cuerpo */
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white; /* Texto blanco en el encabezado */
            padding: 2rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            position: relative;
            z-index: 2;
        }
        
        .quantum-particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            opacity: 0.3;
        }
        
        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background-color: white;
            border-radius: 50%;
            animation: float 15s infinite linear;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) translateX(0);
                opacity: 0;
            }
            50% {
                opacity: 1;
            }
            100% {
                transform: translateY(-500px) translateX(200px);
                opacity: 0;
            }
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            font-weight: 800;
        }
        
        .tagline {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            font-weight: 300;
        }
        
        .header-image { /* Nuevo estilo para la imagen del encabezado */
            max-width: 300px;
            height: auto;
            border-radius: 10px;
            margin-bottom: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white; /* Texto blanco en botones */
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            margin: 0.5rem;
        }
        
        .btn:hover {
            background-color: #d91a6d65;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid white; /* Borde blanco en botones outline */
            color: white; /* Texto blanco en botones outline */
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
        }
        
        nav {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 2rem;
        }
        
        .logo {
            font-weight: bold;
            font-size: 1.5rem;
            color: var(--primary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark); /* Texto oscuro en enlaces de navegación */
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            bottom: -5px;
            left: 0;
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
        }
        
        h2::after {
            content: '';
            position: absolute;
            width: 50%;
            height: 4px;
            background-color: var(--accent);
            bottom: -10px;
            left: 0;
            border-radius: 2px;
        }
        
        h3 {
            font-size: 1.8rem;
            margin: 2rem 0 1rem;
            color: var(--secondary);
        }
        
        p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }
        
        .highlight {
            background-color: rgba(247, 37, 133, 0.1);
            padding: 2rem;
            border-radius: 10px;
            margin: 2rem 0;
            border-left: 4px solid var(--accent);
        }
        
        .quote {
            font-style: italic;
            font-size: 1.2rem;
            color: var(--gray);
            padding: 1.5rem;
            border-left: 4px solid var(--secondary);
            margin: 2rem 0;
            background-color: rgba(114, 9, 183, 0.05);
        }
        
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 2rem 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            overflow: hidden;
        }
        
        .comparison-table th, .comparison-table td {
            padding: 1.2rem;
            text-align: left;
            border-bottom: 1px solid #ddd;
            color: var(--dark); /* Texto oscuro en celdas de tabla */
        }
        
        .comparison-table th {
            background-color: var(--primary);
            color: white; /* Texto blanco en encabezados de tabla */
            font-weight: bold;
        }
        
        .comparison-table tr:nth-child(even) {
            background-color: #f8f9fa;
        }
        
        .comparison-table tr:hover {
            background-color: rgba(58, 12, 163, 0.1);
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            color: var(--dark); /* Texto oscuro en tarjetas de características */
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .feature-card h4 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--secondary);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .sector-card {
            background-color: white;
            border-radius: 10px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border-left: 4px solid var(--success);
            color: var(--dark); /* Texto oscuro en tarjetas de sector */
        }
        
        .sector-card h4 {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .sector-card h4::before {
            content: '✓';
            margin-right: 0.5rem;
            color: var(--success);
            font-weight: bold;
        }
        
        .timeline {
            position: relative;
            max-width: 1200px;
            margin: 3rem auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 6px;
            background-color: var(--secondary);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
            border-radius: 3px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            background-color: rgb(231, 220, 220);
            border: 4px solid var(--accent);
            border-radius: 50%;
            top: 15px;
            z-index: 1;
        }
        
        .left {
            left: 0;
        }
        
        .right {
            left: 50%;
        }
        
        .left::after {
            right: -12px;
        }
        
        .right::after {
            left: -12px;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            color: var(--dark); /* Texto oscuro en contenido de línea de tiempo */
        }
        
        .timeline-content h4 {
            margin-bottom: 0.5rem;
            color: var(--primary);
        }
        
        .resources-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }
        
        .resource-card {
            background-color: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
            color: var(--dark); /* Texto oscuro en tarjetas de recursos */
        }
        
        .resource-card:hover {
            transform: translateY(-5px);
        }
        
        .resource-card h4 {
            margin-bottom: 1rem;
            color: var(--secondary);
        }
        
        .resource-link {
            display: inline-block;
            margin-top: 1rem;
            color: var(--accent);
            font-weight: bold;
            text-decoration: none;
        }
        
        .resource-link:hover {
            text-decoration: underline;
        }
        
        .contact-section { /* Nuevo estilo para la sección de contáctanos */
            background-color: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
            color: var(--dark);
        }

        .contact-section h2 {
            margin-bottom: 1rem;
        }

        .contact-section p {
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }

        .contact-section a {
            color: var(--primary);
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
        }

        .contact-section a:hover {
            text-decoration: underline;
        }
        
        footer {
            background-color: var(--dark);
            color: white; /* Texto blanco en el pie de página */
            padding: 3rem 2rem;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            text-align: left;
        }
        
        .footer-column h4 {
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
            color: var(--light); /* Títulos de columna del footer en color claro */
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: var(--gray); /* Enlaces del footer en color gris */
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            color: white; /* Iconos sociales en blanco */
            font-size: 1.5rem;
        }
        
        .copyright {
            margin-top: 3rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray); /* Texto de copyright en color gris */
            text-align: center; /* Alineación central para el texto del copyright */
        }

        /* Estilos para las imágenes en las secciones */
        .section-image {
            width: 100%;
            max-width: 600px; /* Limita el ancho máximo de las imágenes */
            height: auto;
            border-radius: 10px;
            margin: 2rem auto; /* Centra la imagen y añade margen */
            display: block; /* Para que margin: auto funcione */
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        /* Estilos para la sección de Integrantes */
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
            justify-content: center; /* Centrar las tarjetas */
        }

        .team-card {
            background-color: white;
            border-radius: 15px;
            padding: 2rem;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            border: 2px solid var(--team-card-border); /* Borde de color secundario */
            color: var(--dark); /* Texto oscuro en tarjetas de equipo */
        }

        .team-card:hover {
            transform: translateY(-12px) scale(1.02);
            box-shadow: 0 18px 35px rgba(0, 0, 0, 0.2);
        }

        .team-card img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 1.5rem;
            border: 4px solid var(--accent); /* Borde de acento */
            box-shadow: 0 0 0 6px rgba(247, 37, 133, 0.2);
        }

        .team-card h4 {
            font-size: 1.6rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
            font-weight: 600;
        }

        .team-card p {
            font-size: 1.1rem;
            color: var(--gray); /* Color gris para el rol */
            margin-bottom: 0;
        }

        /* Estilos para la sección de Puntos Clave */
        .key-points-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }

        .key-point-card {
            background-color: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border-left: 4px solid var(--primary); /* Borde primario */
            color: var(--dark); /* Texto oscuro */
        }

        .key-point-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }

        .key-point-card h4 {
            font-size: 1.4rem;
            margin-bottom: 1rem;
            color: var(--secondary);
            display: flex;
            align-items: center;
        }

        .key-point-card h4::before {
            content: '•'; /* Un bullet point simple */
            font-size: 2rem;
            line-height: 1;
            margin-right: 0.8rem;
            color: var(--accent);
            font-weight: bold;
        }
        
        /* Media Queries */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .nav-links {
                display: none;
                flex-direction: column;
                width: 100%;
                background-color: white;
                position: absolute;
                top: 100%;
                left: 0;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
                padding: 1rem 0;
            }

            .nav-links.active { /* Clase para mostrar el menú móvil */
                display: flex;
            }
            
            .nav-links li {
                margin: 0.5rem 0;
                text-align: center;
            }

            .nav-links a {
                padding: 0.5rem 1rem;
                display: block;
            }
            
            .hamburger {
                display: block;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item::after {
                left: 18px;
            }
            
            .left::after, .right::after {
                left: 18px;
            }
            
            .right {
                left: 0;
            }

            .team-grid, .key-points-grid {
                grid-template-columns: 1fr; /* Una columna en móviles */
            }
        }
        
        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        section {
            animation: fadeIn 0.8s ease-out;
        }
        
        .feature-card, .team-card, .resource-card, .sector-card, .key-point-card {
            animation: fadeIn 0.8s ease-out;
            animation-fill-mode: both;
        }
        
        .feature-card:nth-child(1) { animation-delay: 0.1s; }
        .feature-card:nth-child(2) { animation-delay: 0.3s; }
        .feature-card:nth-child(3) { animation-delay: 0.5s; }
        .feature-card:nth-child(4) { animation-delay: 0.7s; }

        .key-point-card:nth-child(1) { animation-delay: 0.1s; }
        .key-point-card:nth-child(2) { animation-delay: 0.3s; }
        .key-point-card:nth-child(3) { animation-delay: 0.5s; }
        .key-point-card:nth-child(4) { animation-delay: 0.7s; }

        .team-card:nth-child(1) { animation-delay: 0.1s; }
        .team-card:nth-child(2) { animation-delay: 0.3s; }
        .team-card:nth-child(3) { animation-delay: 0.5s; }
        .team-card:nth-child(4) { animation-delay: 0.7s; }
    </style>
</head>
<body>
    <header>
        <div class="quantum-particles" id="quantumParticles"></div>
        <div class="header-content">
            <h1>Computación Cuántica</h1>
            <p class="tagline">La Revolución Tecnológica del Siglo XXI</p>
            <div class="header-buttons">
                <a href="#que-es" class="btn">Explorar</a>
                <a href="#contactanos" class="btn btn-outline">Contáctanos</a> <!-- Botón "Contáctanos" en el header -->
            </div>
        </div>
    </header>
    
    <nav>
        <div class="nav-container">
            <div class="logo">Quantum<span style="color: var(--accent);">Tech</span></div>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#que-es">¿Qué es?</a></li>
                <li><a href="#puntos-clave">Puntos Clave</a></li>
                <li><a href="#aplicaciones">Aplicaciones</a></li>
                <li><a href="#ciberseguridad">Ciberseguridad</a></li>
                <li><a href="#futuro">Futuro</a></li>
                <li><a href="#integrantes">Integrantes</a></li>
                <li><a href="#contactanos">Contáctanos</a></li> <!-- Enlace "Contáctanos" en la navegación principal -->
            </ul>
            <div class="hamburger">☰</div>
        </div>
    </nav>
    
    <section id="inicio">
        <h2>Bienvenidos a la Era Cuántica</h2>
        <p>La <strong>computación cuántica</strong> no es solo una evolución tecnológica, es un <strong>cambio de paradigma</strong> que promete revolucionar cómo procesamos información, resolvemos problemas complejos y aceleramos descubrimientos científicos.</p>
        
        <div class="highlight">
            <h3>¿Por qué es importante?</h3>
            <ul>
                <li><strong>Potencial exponencial</strong>: Resuelve problemas que las computadoras clásicas no pueden abordar, desde el diseño de nuevos fármacos hasta la optimización de sistemas globales.</li>
                <li><strong>Nuevos horizontes</strong>: Permite simulaciones moleculares, cifrado indescifrable y avances en inteligencia artificial.</li>
                <li><strong>Más allá de la Ley de Moore</strong>: Mientras los chips clásicos se acercan a sus límites físicos, la computación cuántica ofrece un camino hacia el futuro.</li>
            </ul>
        </div>
        
        <div class="quote">
            "La computación cuántica no es solo más rápida, es radicalmente diferente."
        </div>

        <!-- YouTube Video Embed -->
        <div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; margin-top: 2rem; border-radius: 10px; overflow: hidden; box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);">
            <iframe 
                src="https://www.youtube.com/embed/mnwU98tIMBY" 
                frameborder="0" 
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                allowfullscreen 
                style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border-radius: 10px;">
            </iframe>
        </div>
    </section>
    
    <section id="que-es">
        <h2>¿Qué es la Computación Cuántica?</h2>
        
        <h3>Diferencias Clave: Clásica vs. Cuántica</h3>
        <table class="comparison-table">
            <tr>
                <th>Computación Clásica</th>
                <th>Computación Cuántica</th>
            </tr>
            <tr>
                <td>Usa <strong>bits</strong> (0 ó 1)</td>
                <td>Usa <strong>qubits</strong> (0, 1 o ambos a la vez)</td>
            </tr>
            <tr>
                <td>Opera con puertas lógicas booleanas</td>
                <td>Opera con matrices cuánticas (Hadamard, CNOT)</td>
            </tr>
            <tr>
                <td>Procesamiento secuencial</td>
                <td><strong>Superposición</strong>: Cálculos en paralelo</td>
            </tr>
        </table>
        
        <h3>Los Pilares de la Computación Cuántica</h3>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">⚡</div>
                <h4>Superposición</h4>
                <p>Un qubit puede estar en <strong>0, 1 o ambos estados simultáneamente</strong> (como una moneda girando en el aire). Ejemplo: 30 qubits pueden representar <strong>2³⁰ = 1,073,741,824 estados a la vez</strong>.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🔗</div>
                <h4>Entrelazamiento Cuántico</h4>
                <p>Dos qubits entrelazados están <strong>correlacionados instantáneamente</strong>, sin importar la distancia. Clave para <strong>criptografía cuántica</strong> y algoritmos optimizados.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🌀</div>
                <h4>Interferencia Cuántica</h4>
                <p>Refuerza resultados correctos y cancela los incorrectos, mejorando la eficiencia de los algoritmos.</p>
            </div>
        </div>
        
        <div class="quote">
            "Las puertas cuánticas no siguen el Álgebra de Boole, sino el álgebra lineal matricial."
        </div>
    </section>

    <section id="puntos-clave">
        <h2>Puntos Clave a Saber</h2>
        <p>Aquí te presentamos los aspectos más importantes a comprender sobre la computación cuántica.</p>
        <div class="key-points-grid">
            <div class="key-point-card">
                <h4>No es un reemplazo directo</h4>
                <p>La computación cuántica no reemplazará a las computadoras clásicas. Es una tecnología complementaria diseñada para resolver tipos específicos de problemas extremadamente complejos.</p>
            </div>
            <div class="key-point-card">
                <h4>El "Invierno Cuántico"</h4>
                <p>Existe la posibilidad de un "invierno cuántico" si las expectativas superan los avances reales, lo que podría llevar a una disminución de la inversión y el interés. La investigación es clave.</p>
            </div>
            <div class="key-point-card">
                <h4>Impacto en la Ciberseguridad</h4>
                <p>La computación cuántica representa una amenaza para los métodos de cifrado actuales (como RSA). Es crucial desarrollar y migrar a la criptografía post-cuántica.</p>
            </div>
            <div class="key-point-card">
                <h4>Potencial Transformador</h4>
                <p>A pesar de los desafíos, su potencial para revolucionar campos como la medicina, la ciencia de materiales, la inteligencia artificial y la logística es inmenso.</p>
            </div>
            <div class="key-point-card">
                <h4>Fase de Investigación y Desarrollo</h4>
                <p>Actualmente, la computación cuántica se encuentra en una etapa temprana de investigación y desarrollo. Los ordenadores cuánticos actuales son ruidosos y propensos a errores, pero mejoran rápidamente.</p>
            </div>
            <div class="key-point-card">
                <h4>Accesibilidad en la Nube</h4>
                <p>Grandes empresas como IBM y Microsoft ofrecen acceso a procesadores cuánticos a través de la nube, permitiendo a investigadores y desarrolladores experimentar con esta tecnología.</p>
            </div>
        </div>
    </section>
    
    <section id="aplicaciones">
        <h2>Aplicaciones en la Industria</h2>
        
        <h3>Problemas que la Computación Cuántica Puede Resolver</h3>
        <ul>
            <li><strong>Optimización</strong>: Rutas logísticas, gestión de energía</li>
            <li><strong>Simulación</strong>: Moléculas para nuevos fármacos</li>
            <li><strong>Machine Learning</strong>: Entrenamiento acelerado de IA</li>
        </ul>
        
        <h3>Sectores Clave</h3>
        <div class="sector-card">
            <h4>Salud y Ciencias</h4>
            <ul>
                <li>Diseño de fármacos (ej: COVID-19)</li>
                <li>Medicina personalizada (análisis de ADN)</li>
                <li>Simulación de procesos moleculares</li>
            </ul>
        </div>
        
        <div class="sector-card">
            <h4>Finanzas</h4>
            <ul>
                <li>Detección de fraudes</li>
                <li>Optimización de carteras de inversión</li>
                <li>Análisis de riesgos</li>
            </ul>
            <p><em>JP Morgan, Goldman Sachs ya están explorando estas aplicaciones</em></p>
        </div>
        
        <div class="sector-card">
            <h4>Logística y Energía</h4>
            <ul>
                <li>Optimización de rutas (Amazon, DHL)</li>
                <li>Redes eléctricas inteligentes</li>
                <li>Gestión de inventarios</li>
            </ul>
        </div>
        
        <div class="sector-card">
            <h4>IA y Automoción</h4>
            <ul>
                <li>Coches autónomos más seguros</li>
                <li>Redes neuronales cuánticas</li>
                <li>Procesamiento de lenguaje natural</li>
            </ul>
        </div>
        
        <div class="quote">
            "Empresas como IBM, Google y Microsoft ya están desarrollando soluciones cuánticas para estos sectores."
        </div>
    </section>
    
    <section id="ciberseguridad">
        <h2>Ciberseguridad en la Era Cuántica</h2>
        
        <h3>Amenazas Cuánticas</h3>
        <div class="highlight">
            <p><strong>🔓 Algoritmo de Shor</strong>: Puede romper el cifrado RSA y ECC en segundos.</p>
            <p><strong>⚠ "Guarda Ahora, Descifra Después" (SNDL)</strong>: Hackers almacenan datos cifrados hoy para descifrarlos mañana.</p>
        </div>
        
        <h3>Soluciones Cuánticas</h3>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">🛡️</div>
                <h4>Criptografía Post-Cuántica (PQC)</h4>
                <p>Algoritmos basados en <strong>retículos (NTRU)</strong> e <strong>isogenias (SIDH)</strong> resistentes a ataques cuánticos.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🔑</div>
                <h4>Distribución Cuántica de Claves (QKD)</h4>
                <p>Método de comunicación intrínsecamente seguro basado en principios cuánticos. <strong>Proyecto MADRID-Q</strong> y <strong>LuxQuanta</strong> lideran su desarrollo en España.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">💾</div>
                <h4>Chip Majorana 1 (Microsoft)</h4>
                <p>Qubits topológicos más estables para criptografía segura y autenticación cuántica.</p>
            </div>
        </div>
        
        <div class="quote">
            "Infraestructuras críticas (bancos, gobiernos) deben migrar ya a criptografía post-cuántica."
        </div>
    </section>
    
    <section id="futuro">
        <h2>Desafíos y Futuro</h2>
        
        <h3>Retos Actuales</h3>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">❌</div>
                <h4>Decoherencia Cuántica</h4>
                <p>Los qubits son frágiles (requieren -273°C y aislamiento extremo).</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">❌</div>
                <h4>Escalabilidad</h4>
                <p>Hoy solo hay chips de decenas de qubits (IBM Eagle: 127 qubits).</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">❌</div>
                <h4>Software</h4>
                <p>Falta de herramientas maduras (Qiskit, Cirq están en desarrollo).</p>
            </div>
        </div>
        
        <h3>Perspectivas Futuras</h3>
        <div class="timeline">
            <div class="timeline-item left">
                <div class="timeline-content">
                    <h4>2023-2025</h4>
                    <p>Avances en corrección de errores. Primeros algoritmos prácticos en optimización.</p>
                </div>
            </div>
            <div class="timeline-item right">
                <div class="timeline-content">
                    <h4>2025-2030</h4>
                    <p>Ordenadores cuánticos tolerantes a fallos. Mercado de $100 mil millones.</p>
                </div>
            </div>
            <div class="timeline-item left">
                <div class="timeline-content">
                    <h4>2030+</h4>
                    <p>Computación cuántica universal. Posible "invierno cuántico" si no se cumplen expectativas.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section id="integrantes">
        <h2>Autores</h2>
        <p>Conoce a los miembros clave detrás de la iniciativa computación cuántica.</p>
        <div class="team-grid">
            <div class="team-card">
                <img src="jerson.jpeg"
                <h4>Jerson Arcos Durand</h4>
                <p>Líder de Proyecto</p>
            </div>
            <div class="team-card">
                <img src="Samanta.jpeg"
                <h4>Samantha Galindo Mujica</h4>
                <p>Investigadora Cuántica</p>
            </div>
            <div class="team-card">
                <img src="Noemi.jpeg"
                <h4>Noemi Merari Altamirano Orosco</h4>
                <p>Desarrollador de Software Cuántico</p>
            </div>
            <div class="team-card">
                <img src="Sinai.jpeg"
                <h4>Sinai Altamirano Orosco</h4>
                <p>Especialista en Ciberseguridad Cuántica</p>
            </div>
        </div>
    </section>

    <section id="recursos">
        <h2>Más información</h2>
        <div class="resources-grid">
            <div class="resource-card">
                <h4>Computing</h4>
                <p>Qué es la computación cuántica y para qué sirve, y qué son los ordenadores cuánticos, son interrogantes que surgen ante el protagonismo que está adquiriendo esta tecnología.</p>
                <a href="https://www.computing.es/informes/computacion-cuantica-que-es-y-como-funciona/" class="resource-link" target="_blank">Visitar →</a>
            </div>
            
            <div class="resource-card">
                <h4>Principios de la computación cuántica</h4>
                <p>Leyes físicas que imponían algunas limitaciones al proceso de cómputo.</p>
                <a href="https://enginyeriainformatica.cat/wp-content/uploads/2016/05/PRINCIPIOS-FUNDAMENTALES-DE-COMPUTACI%C3%93N-CU%C3%81NTICA.pdf" class="resource-link" target="_blank">Visitar →</a>
            </div>
    
            </div>
        </div>
    </section>
    
    <section id="contactanos" class="contact-section">
        <h2>Contáctanos</h2>
        <p>Puedes enviarnos un correo electrónico a:</p>
        <p><a href="mailto:018100111k@uandina.edu.pe">018100111k@uandina.edu.pe</a></p>
        <p><a href="mailto:017200419h@uandina.edu.pe">017200419h@uandina.edu.pe</a></p>
        <p><a href="mailto:019200457e@uandina.edu.pe">019200457e@uandina.edu.pe</a></p>
    </section>
        
        <div class="copyright">
            <p>Linfokillers-Cenfoti-UAC</p>
            <P>AUXILIO</P>
            <p>Cusco-Perú</p>
            <P>2025
        </div>
    </footer>
    
    <script>
        // Smooth scrolling para enlaces
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Menú hamburguesa para móviles
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');
        
        hamburger.addEventListener('click', () => {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
        
        // Cerrar menú al hacer clic en un enlace (móviles)
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                if (window.innerWidth <= 768) {
                    navLinks.style.display = 'none';
                }
            });
        });
    </script>
</body>
</html>
