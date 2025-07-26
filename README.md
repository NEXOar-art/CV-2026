



<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Currículum Vitae de Gastón Roberto Giménez - Operador de Planta">
    <meta name="keywords" content="Gastón Giménez, operador de planta, operador de reactores, Power BI, producción industrial">
    <meta name="author" content="Gastón Roberto Giménez">
    <title>Gastón Roberto Giménez - CV</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
    <style>
        body {
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 50%, #1a2526 100%);
            color: #ffffff;
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
            animation: gradientFlow 20s ease-in-out infinite;
            background-size: 200% 200%;
            transition: color 0.3s ease;
        }
        @keyframes gradientFlow {
            0% { background-position: 0% 0%; }
            50% { background-position: 100% 100%; }
            100% { background-position: 0% 0%; }
        }
        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, rgba(52, 152, 219, 0.2) 0%, transparent 70%);
            z-index: 0;
        }
        .twinkle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: rgba(52, 152, 219, 0.8);
            border-radius: 50%;
            animation: twinkle 2s infinite ease-in-out;
        }
        @keyframes twinkle {
            0% { opacity: 0; }
            50% { opacity: 0.8; }
            100% { opacity: 0; }
        }
        .section-hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        .parallax-bg {
            background-attachment: fixed;
            background-size: cover;
            background-position: center;
        }
         .highlight-text {
            background: linear-gradient(90deg, #3498db, #2980b9);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .section {
            padding: 4rem 2rem;
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.6s ease-out;
            position: relative;
            z-index: 1;
        }
        .section.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .timeline-item {
            position: relative;
            padding-left: 2.5rem;
            margin-bottom: 2rem;
        }
        .timeline-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 4px;
            background: #3498db;
        }
        .timeline-item .dot {
            position: absolute;
            left: -8px;
            top: 0;
            width: 16px;
            height: 16px;
            background: #3498db;
            border-radius: 50%;
        }
        .card {
            background: #1a2526;
            border-radius: 1rem;
            padding: 1.5rem;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.5), 0 0 5px rgba(52, 152, 219, 0.2) inset;
            transform: perspective(500px) translateZ(0);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card:hover {
            transform: perspective(500px) translateZ(10px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.7), 0 0 8px rgba(52, 152, 219, 0.3) inset;
        }
        .whatsapp-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 0.75rem;
            border-radius: 50%;
            background-color: #3498db;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .whatsapp-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 0 15px rgba(52, 152, 219, 0.5);
        }
        .whatsapp-logo {
            width: 32px;
            height: 32px;
        }
        @media (max-width: 768px) {
            .section-hero {
                min-height: 80vh;
                text-align: center;
            }
            .section {
                padding: 2rem 1rem;
            }
            .text-5xl {
                font-size: 2.5rem;
            }
            .text-7xl {
                font-size: 3.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Twinkle Effect -->
    <script>
        function createTwinkles(count) {
            for (let i = 0; i < count; i++) {
                const twinkle = document.createElement('div');
                twinkle.className = 'twinkle';
                twinkle.style.left = `${Math.random() * 100}vw`;
                twinkle.style.top = `${Math.random() * 100}vh`;
                twinkle.style.animationDelay = `${Math.random() * 2}s`;
                document.body.appendChild(twinkle);
            }
        }
        createTwinkles(50);

        // Dynamic text color adjustment based on background
        function adjustTextColor() {
            const body = document.body;
            const computeStyle = getComputedStyle(body);
            const bgColor = computeStyle.backgroundColor;
            const rgb = bgColor.match(/\d+/g).map(Number);
            const brightness = (rgb[0] * 299 + rgb[1] * 587 + rgb[2] * 114) / 1000;
            if (brightness > 128) {
                body.style.color = '#333333'; // Dark gray for bright backgrounds like blue
                document.querySelectorAll('.text-gray-300, .text-gray-400').forEach(el => {
                    el.style.color = '#444444'; // Adjust subtext colors
                });
            } else {
                body.style.color = '#ffffff'; // White for dark backgrounds
                document.querySelectorAll('.text-gray-300, .text-gray-400').forEach(el => {
                    el.style.color = '#aaaaaa'; // Adjust subtext colors
                });
            }
        }
        setInterval(adjustTextColor, 100); // Check every 100ms
        adjustTextColor(); // Initial call
    </script>

    <!-- Hero Section -->
    <section class="section-hero parallax-bg">
        <div class="container mx-auto px-4 z-10 flex items-center gap-6">
            <img src="IMGCV/FOTO NUEVA.png" alt="Profile Picture" class="w-24 h-24 rounded-full object-cover">
            <div>
                <h1 class="text-5xl md:text-7xl font-bold highlight-text mb-4">Gastón Roberto Giménez</h1>
                <p class="text-2xl md:text-3xl text-gray-300 mb-6">Operador de Planta</p>
                <p class="text-lg text-gray-400 max-w-2xl">Profesional con experiencia en producción industrial, impulsando la eficiencia operativa y la innovación en entornos dinámicos.</p>
                <a href="https://api.whatsapp.com/send?phone=+543834689137&text=%C2%A1Hola%20....Quiero%20informaci%C3%B3n%20de%20tu%20Perfil%20Gast%C3%B3n!" target="_blank" class="mt-6 whatsapp-btn">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp Logo" class="whatsapp-logo">
                </a>
            </div>
        </div>
    </section>

    <!-- Resumen Laboral -->
    <section id="resumen" class="section bg-gray-900">
        <div class="container mx-auto px-4">
            <h2 class="text-4xl font-bold text-blue-400 mb-6">Resumen Laboral</h2>
            <div class="card">
                <p class="text-lg text-gray-300 leading-relaxed">
                    Más de 15 años de experiencia en producción industrial, trabajando en empresas líderes como Cervecería y Maltería Quilmes, Papelera del Plata (Softly) y Cabot Argentina. En Cabot, como Operador de Planta y Reactores, logré un rendimiento del 98% en la producción de negro de humo mediante controles de calidad y operación eficiente en sistemas DeltaV. Mi enfoque en la productividad, resolución de problemas y adaptabilidad me permite destacar en entornos de alta exigencia.
                </p>
            </div>
        </div>
    </section>

    <!-- Experiencia Laboral -->
    <section id="experiencia" class="section bg-gray-800">
        <div class="container mx-auto px-4">
            <h2 class="text-4xl font-bold text-blue-400 mb-6">Experiencia Laboral</h2>
            <div class="timeline-item">
                <div class="dot"></div>
                <h3 class="text-xl font-semibold text-white">Operador de Planta y Operador de Reactores - Cabot Argentina</h3>
                <p class="text-gray-400">2000 - 2013</p>
                <p class="text-gray-300">Optimización de procesos productivos, logrando un rendimiento del 92% en la producción de negro de humo mediante controles de calidad y operación eficiente en control distribuido DeltaV.</p>
            </div>
            <div class="timeline-item">
                <div class="dot"></div>
                <h3 class="text-xl font-semibold text-white">Operador de Planta - Papelera del Plata (Softly)</h3>
                <p class="text-gray-400">1999 - 2000</p>
                <p class="text-gray-300">Gestión de líneas de producción, garantizando cumplimiento de normativas y estándares de seguridad.</p>
            </div>
            <div class="timeline-item">
                <div class="dot"></div>
                <h3 class="text-xl font-semibold text-white">Operador - Cervecería y Maltería Quilmes</h3>
                <p class="text-gray-400">1995 - 1998</p>
                <p class="text-gray-300">Operación de maquinaria industrial alimenticia y mantenimiento preventivo, contribuyendo a la continuidad operativa en líneas de transporte en sector envasado.</p>
            </div>
        </div>
    </section>

    <!-- Educación -->
    <section id="educacion" class="section bg-gray-900">
        <div class="container mx-auto px-4">
            <h2 class="text-4xl font-bold text-blue-400 mb-6">Educación</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class="card">
                    <h3 class="text-xl font-semibold text-white">Lic. en Comercio Internacional</h3>
                    <p class="text-gray-400">Universidad de Luján | 2019 - 2022</p>
                </div>
                <div class="card">
                    <h3 class="text-xl font-semibold text-white">Técnico Químico</h3>
                    <p class="text-gray-400">Técnica Luciano Reyes | 1989 - 1995</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Habilidades -->
    <section id="habilidades" class="section bg-gray-800">
        <div class="container mx-auto px-4">
            <h2 class="text-4xl font-bold text-blue-400 mb-6">Habilidades</h2>
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
                <div class="card text-center">
                    <p class="text-white">Paquete Office</p>
                </div>
                <div class="card text-center">
                    <p class="text-white">Python Básico</p>
                </div>
                <div class="card text-center">
                    <p class="text-white">Google Colab</p>
                </div>
                <div class="card text-center">
                    <p class="text-white">Visual Studio Code</p>
                </div>
                <div class="card text-center">
                    <p class="text-white">Power BI</p>
                </div>
                <div class="card text-center">
                    <p class="text-white">Canva</p>
                </div>
                <div class="card text-center">
                    <p class="text-white">Foguista</p>
                </div>
                <div class="card text-center">
                    <p class="text-white">Operador DeltaV EMERSON</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Certificaciones -->
    <section id="certificaciones" class="section bg-gray-900">
        <div class="container mx-auto px-4">
            <h2 class="text-4xl font-bold text-blue-400 mb-6">Certificaciones</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class="card">
                    <p class="text-lg text-gray-300">Data Analytics | CoderHouse | 2022</p>
                </div>
                <div class="card">
                    <p class="text-lg text-gray-300">Data Science | CoderHouse | 2023</p>
                </div>
                <div class="card">
                    <p class="text-lg text-gray-300">Visualización de Datos | Coursera | 2023</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Idiomas -->
    <section id="idiomas" class="section bg-gray-800">
        <div class="container mx-auto px-4">
            <h2 class="text-4xl font-bold text-blue-400 mb-6">Idiomas</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class="card">
                    <p class="text-lg text-gray-300">Español: Nativo</p>
                </div>
                <div class="card">
                    <p class="text-lg text-gray-300">Inglés: Básico</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contacto -->
    <section id="contact" class="section bg-gray-900">
        <div class="container mx-auto px-4">
            <h2 class="text-4xl font-bold text-blue-400 mb-6">Contacto</h2>
            <div class="card">
                <p class="text-lg text-gray-300">Conecta conmigo para oportunidades laborales o colaboraciones:</p>
                <p class="text-lg text-gray-400 mt-4">Email: gaston.gimenez@example.com</p>
                <p class="text-lg text-gray-400 mt-2">LinkedIn: <a href="https://linkedin.com/in/gastongimenez" target="_blank" class="text-blue-400 hover:underline">linkedin.com/in/gastongimenez</a></p>
                <a href="https://linkedin.com/in/gastongimenez" target="_blank" class="mt-4 inline-block bg-blue-400 text-white font-semibold py-3 px-6 rounded-full hover:bg-blue-300 transition">Visitar Perfil de LinkedIn</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black py-6 text-center text-gray-400">
        <p>© 2025 Gastón Roberto Giménez. Todos los derechos reservados.</p>
        <p class="mt-2">
            <a href="#" class="text-blue-400 hover:underline">Política de Privacidad</a> | 
            <a href="#" class="text-blue-400 hover:underline">Política de Cookies</a> | 
            <a href="#" class="text-blue-400 hover:underline">Aviso Legal</a>
        </p>
    </footer>

    <script>
        // Animaciones con GSAP y ScrollTrigger
        gsap.registerPlugin(ScrollTrigger);

        gsap.utils.toArray(".section").forEach((section) => {
            gsap.to(section, {
                scrollTrigger: {
                    trigger: section,
                    start: "top 80%",
                    toggleActions: "play none none none",
                },
                opacity: 1,
                y: 0,
                duration: 0.6,
            });
        });

        gsap.utils.toArray(".card").forEach((card) => {
            gsap.to(card, {
                scrollTrigger: {
                    trigger: card,
                    start: "top 90%",
                    toggleActions: "play none none none",
                },
                scale: 1.02,
                duration: 0.3,
                ease: "power1.out"
            });
        });

        // Parallax effect
        window.addEventListener("scroll", () => {
            const hero = document.querySelector(".section-hero");
            const scrollPosition = window.pageYOffset;
            hero.style.backgroundPositionY = `${scrollPosition * 0.5}px`;
        });

        // Dynamic text color adjustment based on background
        function adjustTextColor() {
            const body = document.body;
            const computeStyle = getComputedStyle(body);
            const bgColor = computeStyle.backgroundColor;
            const rgb = bgColor.match(/\d+/g).map(Number);
            const brightness = (rgb[0] * 299 + rgb[1] * 587 + rgb[2] * 114) / 1000;
            if (brightness > 128) {
                body.style.color = '#333333'; // Dark gray for bright backgrounds like blue
                document.querySelectorAll('.text-gray-300, .text-gray-400').forEach(el => {
                    el.style.color = '#444444'; // Adjust subtext colors
                });
            } else {
                body.style.color = '#ffffff'; // White for dark backgrounds
                document.querySelectorAll('.text-gray-300, .text-gray-400').forEach(el => {
                    el.style.color = '#aaaaaa'; // Adjust subtext colors
                });
            }
        }
        setInterval(adjustTextColor, 100); // Check every 100ms
        adjustTextColor(); // Initial call
    </script>
</body>
</html>
