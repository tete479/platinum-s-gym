<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>FITZONE | Tu mejor versión comienza aquí</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background-color: #0b0b0b;
            color: #ffffff;
        }

        /* =========================
           NAVEGACIÓN
        ========================= */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(10px);
        }

        nav {
            max-width: 1200px;
            margin: auto;
            height: 75px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 25px;
        }

        .logo {
            font-size: 28px;
            font-weight: 900;
            letter-spacing: 2px;
            color: #ffffff;
        }

        .logo span {
            color: #ff3b30;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        .nav-links a {
            color: #ffffff;
            text-decoration: none;
            font-size: 15px;
            font-weight: 600;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: #ff3b30;
        }

        .nav-button {
            background: #ff3b30;
            color: white !important;
            padding: 12px 20px;
            border-radius: 5px;
        }

        .nav-button:hover {
            background: #e52d23;
        }

        /* =========================
           HERO
        ========================= */

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 100px 20px 60px;

            background:
                linear-gradient(
                    rgba(0, 0, 0, 0.72),
                    rgba(0, 0, 0, 0.85)
                ),
                url("https://images.unsplash.com/photo-1534438327276-14e5300c3a48?auto=format&fit=crop&w=2000&q=80");

            background-size: cover;
            background-position: center;
        }

        .hero-content {
            max-width: 850px;
        }

        .hero h1 {
            font-size: clamp(45px, 8vw, 90px);
            line-height: 0.95;
            font-weight: 900;
            text-transform: uppercase;
            margin-bottom: 25px;
        }

        .hero h1 span {
            color: #ff3b30;
        }

        .hero p {
            font-size: 20px;
            color: #dddddd;
            max-width: 650px;
            margin: 0 auto 35px;
            line-height: 1.6;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 15px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        .btn-primary {
            background: #ff3b30;
            color: white;
        }

        .btn-primary:hover {
            background: #e52d23;
            transform: translateY(-2px);
        }

        .btn-secondary {
            border: 2px solid white;
            color: white;
        }

        .btn-secondary:hover {
            background: white;
            color: black;
        }

        /* =========================
           SECCIONES GENERALES
        ========================= */

        section {
            padding: 100px 20px;
        }

        .container {
            max-width: 1100px;
            margin: auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 42px;
            text-transform: uppercase;
            margin-bottom: 15px;
        }

        .section-title span {
            color: #ff3b30;
        }

        .section-title p {
            color: #999999;
            max-width: 600px;
            margin: auto;
            line-height: 1.6;
        }

        /* =========================
           NOSOTROS
        ========================= */

        .about {
            background: #111111;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-image {
            min-height: 450px;
            border-radius: 10px;
            background:
                linear-gradient(
                    rgba(0, 0, 0, 0.2),
                    rgba(0, 0, 0, 0.4)
                ),
                url("https://images.unsplash.com/photo-1581009146145-b5ef050c2e1e?auto=format&fit=crop&w=1000&q=80");

            background-size: cover;
            background-position: center;
        }

        .about-text h3 {
            font-size: 35px;
            margin-bottom: 20px;
        }

        .about-text p {
            color: #aaaaaa;
            line-height: 1.8;
            margin-bottom: 20px;
        }

        .features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 30px;
        }

        .feature {
            padding: 20px;
            background: #1a1a1a;
            border-left: 3px solid #ff3b30;
        }

        .feature h4 {
            margin-bottom: 8px;
        }

        .feature p {
            font-size: 14px;
            margin: 0;
        }

        /* =========================
           PLANES
        ========================= */

        .plans {
            background: #0b0b0b;
        }

        .plans-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .plan {
            background: #151515;
            border: 1px solid #292929;
            border-radius: 10px;
            padding: 35px 25px;
            text-align: center;
            transition: 0.3s;
        }

        .plan:hover {
            transform: translateY(-8px);
            border-color: #ff3b30;
        }

        .plan.featured {
            border: 2px solid #ff3b30;
            transform: scale(1.03);
        }

        .plan h3 {
            font-size: 25px;
            margin-bottom: 20px;
        }

        .price {
            font-size: 45px;
            font-weight: 900;
            margin-bottom: 25px;
        }

        .price small {
            font-size: 15px;
            color: #999999;
            font-weight: normal;
        }

        .plan ul {
            list-style: none;
            margin-bottom: 30px;
        }

        .plan li {
            padding: 10px 0;
            border-bottom: 1px solid #292929;
            color: #cccccc;
        }

        /* =========================
           CLASES
        ========================= */

        .classes {
            background: #111111;
        }

        .classes-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .class-card {
            background: #191919;
            padding: 30px;
            border-radius: 8px;
            transition: 0.3s;
        }

        .class-card:hover {
            transform: translateY(-5px);
        }

        .class-icon {
            font-size: 35px;
            margin-bottom: 20px;
        }

        .class-card h3 {
            margin-bottom: 10px;
        }

        .class-card p {
            color: #999999;
            line-height: 1.6;
        }

        /* =========================
           CTA
        ========================= */

        .cta {
            text-align: center;
            background:
                linear-gradient(
                    rgba(255, 59, 48, 0.88),
                    rgba(200, 30, 25, 0.88)
                ),
                url("https://images.unsplash.com/photo-1534438327276-14e5300c3a48?auto=format&fit=crop&w=2000&q=80");

            background-size: cover;
            background-position: center;
        }

        .cta h2 {
            font-size: 50px;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .cta p {
            font-size: 18px;
            margin-bottom: 30px;
        }

        .cta .btn {
            background: white;
            color: #111111;
        }

        /* =========================
           FOOTER
        ========================= */

        footer {
            background: #050505;
            padding: 50px 20px 25px;
        }

        .footer-content {
            max-width: 1100px;
            margin: auto;
            display: grid;
            grid-template-columns: 2fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        footer h3 {
            margin-bottom: 15px;
        }

        footer p,
        footer a {
            color: #888888;
            line-height: 1.8;
            text-decoration: none;
        }

        footer a:hover {
            color: #ff3b30;
        }

        .footer-bottom {
            border-top: 1px solid #222222;
            padding-top: 20px;
            text-align: center;
            color: #666666;
            font-size: 14px;
        }

        /* =========================
           RESPONSIVE
        ========================= */

        @media (max-width: 800px) {

            .nav-links {
                display: none;
            }

            .about-grid {
                grid-template-columns: 1fr;
            }

            .plans-grid {
                grid-template-columns: 1fr;
            }

            .classes-grid {
                grid-template-columns: 1fr;
            }

            .footer-content {
                grid-template-columns: 1fr;
            }

            .plan.featured {
                transform: none;
            }

            .hero h1 {
                font-size: 55px;
            }

            .section-title h2 {
                font-size: 35px;
            }

            .cta h2 {
                font-size: 38px;
            }
        }
    </style>
</head>

<body>

    <!-- =========================
         NAVEGACIÓN
    ========================= -->

    <header>
        <nav>

            <div class="logo">
                FIT<span>ZONE</span>
            </div>

            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#planes">Planes</a></li>
                <li><a href="#clases">Clases</a></li>
                <li><a href="#contacto">Contacto</a></li>
                <li>
                    <a href="#planes" class="nav-button">
                        Inscríbete
                    </a>
                </li>
            </ul>

        </nav>
    </header>


    <!-- =========================
         HERO
    ========================= -->

    <section class="hero" id="inicio">

        <div class="hero-content">

            <h1>
                CONSTRUYE<br>
                TU <span>MEJOR</span><br>
                VERSIÓN
            </h1>

            <p>
                Entrena con propósito, supera tus límites
                y alcanza tus objetivos en un espacio diseñado
                para sacar lo mejor de ti.
            </p>

            <div class="hero-buttons">

                <a href="#planes" class="btn btn-primary">
                    Ver planes
                </a>

                <a href="#nosotros" class="btn btn-secondary">
                    Conócenos
                </a>

            </div>

        </div>

    </section>


    <!-- =========================
         NOSOTROS
    ========================= -->

    <section class="about" id="nosotros">

        <div class="container">

            <div class="about-grid">

                <div class="about-image"></div>

                <div class="about-text">

                    <h3>
                        MÁS QUE UN GIMNASIO
                    </h3>

                    <p>
                        En FITZONE creemos que entrenar no se trata
                        únicamente de levantar pesas. Se trata de
                        disciplina, constancia y de convertirte
                        cada día en una mejor versión de ti mismo.
                    </p>

                    <p>
                        Contamos con instalaciones modernas,
                        entrenadores capacitados y todo lo necesario
                        para ayudarte a alcanzar tus objetivos.
                    </p>

                    <div class="features">

                        <div class="feature">
                            <h4>💪 Equipamiento</h4>
                            <p>
                                Máquinas y equipos para todo tipo
                                de entrenamiento.
                            </p>
                        </div>

                        <div class="feature">
                            <h4>🏆 Entrenadores</h4>
                            <p>
                                Profesionales listos para ayudarte.
                            </p>
                        </div>

                        <div class="feature">
                            <h4>🔥 Ambiente</h4>
                            <p>
                                Energía y motivación en cada entrenamiento.
                            </p>
                        </div>

                        <div class="feature">
                            <h4>⏰ Horarios</h4>
                            <p>
                                Horarios flexibles para adaptarnos a ti.
                            </p>
                        </div>

                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         PLANES
    ========================= -->

    <section class="plans" id="planes">

        <div class="container">

            <div class="section-title">

                <h2>
                    ELIGE TU <span>PLAN</span>
                </h2>

                <p>
                    Encuentra la membresía que mejor se adapte
                    a tus objetivos.
                </p>

            </div>

            <div class="plans-grid">

                <div class="plan">

                    <h3>BÁSICO</h3>

                    <div class="price">
                        $25
                        <small>/mes</small>
                    </div>

                    <ul>
                        <li>Acceso al gimnasio</li>
                        <li>Área de pesas</li>
                        <li>Área cardiovascular</li>
                    </ul>

                    <a href="#contacto" class="btn btn-secondary">
                        Elegir plan
                    </a>

                </div>


                <div class="plan featured">

                    <h3>PREMIUM</h3>

                    <div class="price">
                        $40
                        <small>/mes</small>
                    </div>

                    <ul>
                        <li>Acceso ilimitado</li>
                        <li>Clases grupales</li>
                        <li>Área de pesas</li>
                        <li>Área cardiovascular</li>
                    </ul>

                    <a href="#contacto" class="btn btn-primary">
                        Elegir plan
                    </a>

                </div>


                <div class="plan">

                    <h3>PRO</h3>

                    <div class="price">
                        $60
                        <small>/mes</small>
                    </div>

                    <ul>
                        <li>Acceso ilimitado</li>
                        <li>Clases grupales</li>
                        <li>Entrenador personal</li>
                        <li>Plan personalizado</li>
                    </ul>

                    <a href="#contacto" class="btn btn-secondary">
                        Elegir plan
                    </a>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         CLASES
    ========================= -->

    <section class="classes" id="clases">

        <div class="container">

            <div class="section-title">

                <h2>
                    NUESTRAS <span>CLASES</span>
                </h2>

                <p>
                    Entrena de diferentes maneras y encuentra
                    la actividad que más disfrutes.
                </p>

            </div>


            <div class="classes-grid">

                <div class="class-card">

                    <div class="class-icon">🥊</div>

                    <h3>BOXEO</h3>

                    <p>
                        Mejora tu resistencia, coordinación
                        y condición física.
                    </p>

                </div>


                <div class="class-card">

                    <div class="class-icon">🏋️</div>

                    <h3>FUNCIONAL</h3>

                    <p>
                        Entrenamientos dinámicos para mejorar
                        fuerza y resistencia.
                    </p>

                </div>


                <div class="class-card">

                    <div class="class-icon">🧘</div>

                    <h3>YOGA</h3>

                    <p>
                        Trabaja flexibilidad, movilidad
                        y bienestar mental.
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         CTA
    ========================= -->

    <section class="cta">

        <div class="container">

            <h2>
                ¿LISTO PARA EMPEZAR?
            </h2>

            <p>
                Tu transformación comienza con una decisión.
            </p>

            <a href="#contacto" class="btn">
                QUIERO INSCRIBIRME
            </a>

        </div>

    </section>


    <!-- =========================
         FOOTER
    ========================= -->

    <footer id="contacto">

        <div class="footer-content">

            <div>

                <div class="logo">
                    FIT<span>ZONE</span>
                </div>

                <p>
                    Tu espacio para entrenar, crecer
                    y alcanzar tu mejor versión.
                </p>

            </div>


            <div>

                <h3>Contacto</h3>

                <p>
                    📍 San Pedro Sula, Honduras
                </p>

                <p>
                    📞 +504 0000-0000
                </p>

                <p>
                    ✉️ info@fitzone.com
                </p>

            </div>


            <div>

                <h3>Síguenos</h3>

                <p>
                    <a href="#">Instagram</a>
                </p>

                <p>
                    <a href="#">Facebook</a>
                </p>

                <p>
                    <a href="#">TikTok</a>
                </p>

            </div>

        </div>


        <div class="footer-bottom">

            © 2026 FITZONE. Todos los derechos reservados.

        </div>

    </footer>

</body>
</html>