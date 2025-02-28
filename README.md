<!DOCTYPE html>
<html>

<head>
    <title>Raffaelo Sanzio</title>
    <style>
        body {
            background-color: #f2f2f2;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            animation: fadeIn 1s ease-in-out;
            text-align: center;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }

            to {
                opacity: 1;
            }
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, red, purple);
            /* Gradiente rojo y púrpura */
            opacity: 0.5;
            animation: slideIn 5s linear infinite;
        }

        @keyframes slideIn {
            0% {
                transform: translateX(-100%);
            }

            100% {
                transform: translateX(100%);
            }
        }

        h1 {
            font-size: 36px;
            margin-bottom: 10px;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0% {
                transform: scale(1);
            }

            50% {
                transform: scale(1.1);
            }

            100% {
                transform: scale(1);
            }
        }

        p {
            font-size: 18px;
            line-height: 1.5;
            margin-bottom: 20px;
            animation: slideInLeft 1s ease-in-out;
        }

        @keyframes slideInLeft {
            from {
                transform: translateX(-100%);
                opacity: 0;
            }

            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        img {
            width: 500px;
            height: auto;
            margin: 20px auto;
            display: block;
            animation: zoomIn 1s ease-in-out;
            border: 5px solid transparent;
            border-image: linear-gradient(to right, red, purple, blue, green, yellow, orange, red);
            border-image-slice: 1;
            animation: borderAnimation 5s linear infinite;
        }

        @keyframes borderAnimation {
            0% {
                border-image-source: linear-gradient(to right, red, purple, blue, green, yellow, orange, red);
            }

            25% {
                border-image-source: linear-gradient(to right, purple, blue, green, yellow, orange, red, purple);
            }

            50% {
                border-image-source: linear-gradient(to right, blue, green, yellow, orange, red, purple, blue);
            }

            75% {
                border-image-source: linear-gradient(to right, green, yellow, orange, red, purple, blue, green);
            }

            100% {
                border-image-source: linear-gradient(to right, red, purple, blue, green, yellow, orange, red);
            }
        }

        @keyframes zoomIn {
            from {
                transform: scale(0);
                opacity: 0;
            }

            to {
                transform: scale(1);
                opacity: 1;
            }
        }

        ul {
            list-style: none;
            padding: 0;
        }

        li {
            margin-bottom: 10px;
            animation: fadeIn 1s ease-in-out;
        }

        a {
            color: #333;
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
            color: #007bff;
        }

        footer {
            background-color: #333;
            color: #fff;
            padding: 10px;
            text-align: center;
            position: fixed;
            bottom: 0;
            width: 100%;
            animation: slideInUp 1s ease-in-out;
        }

        @keyframes slideInUp {
            from {
                transform: translateY(100%);
                opacity: 0;
            }

            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        #resumen-obras {
            display: none;
            background-color: #fff;
            padding: 20px;
            margin: 20px auto;
            width: 80%;
            border: 1px solid #ccc;
            text-align: left;
        }
    </style>
    <script>
        function mostrarResumen() {
            var resumen = document.getElementById("resumen-obras");
            if (resumen.style.display === "none") {
                resumen.style.display = "block";
            } else {
                resumen.style.display = "none";
            }
        }
    </script>
</head>

<body>
    <header>
        <h1>Raffaelo Sanzio</h1>
        <p>Creado por Danny Guillen</p>
    </header>
    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <img src="https://artsdot.com/ADC/Art-ImgScreen-4.nsf/O/A-7YKFUW/$FILE/Raphael-raffaello-sanzio-da-urbino-portrait-of-agnolo-doni.Jpg" alt="Raffaelo Sanzio">
                <p>Raffaello Sanzio (1483-1520), también conocido como Rafael, fue un pintor y arquitecto italiano del
                    Alto Renacimiento. Es considerado uno de los grandes maestros del arte occidental y es famoso por
                    sus pinturas de Madonnas, retratos y escenas mitológicas y religiosas.</p>
                <p>Raffaelo nació en Urbino, Italia, y comenzó su carrera artística bajo la tutela de su padre, Giovanni
                    Santi. A los diecisiete años, se trasladó a Florencia, donde estudió con Pietro Perugino y se vio
                    influenciado por las obras de Leonardo da Vinci y Miguel Ángel. En 1508, fue llamado a Roma por el
                    papa Julio II para decorar las estancias del Vaticano, lo que le convirtió en uno de los artistas
                    más importantes de su época.</p>
                <p>Raffaelo murió en Roma en 1520, a la edad de 37 años. Su obra ha tenido una gran influencia en el
                    arte occidental y sigue siendo admirada hoy en día.</p>
            </div>
            <div class="col-md-6">
                <h2>Obras destacadas</h2>
                <ul>
                    <li><a href="https://es.wikipedia.org/wiki/La_Escuela_de_Atenas">La Escuela de Atenas</a></li>
                    <li><a href="https://es.wikipedia.org/wiki/La_Virgen_del_Pez">La Virgen del Pez</a></li>
                    <li><a href="https://es.wikipedia.org/wiki/La_Virgen_del_Silla">La Virgen del Silla</a></li>
                    <li><a href="https://es.wikipedia.org/wiki/La_Transfiguración">La Transfiguración</a></li>
                    <li><a href="https://es.wikipedia.org/wiki/La_Virgen_de_Alba">La Virgen de Alba</a></li>
                </ul>
                <button onclick="mostrarResumen()">Mostrar resumen de obras</button>
                <div id="resumen-obras">
                    <h3>Resumen de obras de Raffaelo Sanzio</h3>
                    <p>Raffaello Sanzio, conocido como Rafael, fue un prolífico artista del Alto Renacimiento cuyas
                        obras abarcan una amplia gama de temas y estilos. Aquí tienes un resumen de sus principales
                        áreas de producción:</p>
                    <p><strong>Pinturas religiosas:</strong></p>
                    <ul>
                        <ul>
                            <li>Madonnas: Rafael es famoso por sus numerosas representaciones de la Virgen María con el
                                Niño Jesús. Estas obras, como "La Virgen del Gran Duque", "La Virgen Sixtina" y "La
                                Bella Jardinera", destacan por su belleza idealizada, armonía y serenidad.</li>
                            <li>Otras obras religiosas: Rafael también creó importantes pinturas religiosas como "La
                                Transfiguración", una obra maestra que muestra la dualidad de la naturaleza de Cristo, y
                                numerosas escenas bíblicas para las estancias del Vaticano.</li>
                        </ul>
                        <p><strong>Pinturas de historia y mitología:</strong></p>
                        <ul>
                            <li>Estancias de Rafael: Sus frescos en las estancias del Vaticano, como "La Escuela de
                                Atenas" y "El Parnaso", son obras maestras del Renacimiento que representan la
                                filosofía, la teología, la poesía y la justicia.</li>
                            <li>Otras obras mitológicas: Rafael también pintó temas mitológicos como "El triunfo de
                                Galatea".</li>
                        </ul>
                        <p><strong>Retratos:</strong></p>
                        <ul>
                            <li>Rafael fue un retratista muy solicitado, y sus obras capturan la personalidad y la
                                dignidad de sus modelos. Algunos de sus retratos más famosos incluyen "Retrato de
                                Baltasar Castiglione", "Retrato del cardenal" y "Retrato de Julio II".</li>
                        </ul>
                        <p><strong>Características generales de su obra:</strong></p>
                        <ul>
                            <li>Rafael es conocido por su dominio del dibujo, su uso armonioso del color y su capacidad
                                para crear composiciones equilibradas y elegantes.</li>
                            <li>Sus obras reflejan los ideales del Alto Renacimiento, como la belleza, la armonía y la
                                proporción.</li>
                            <li>Rafael tuvo una gran influencia en generaciones posteriores de artistas, y su estilo ha
                                sido admirado y emulado durante siglos.</li>
                        </ul>
                </div>
            </div>
        </div>
    </div>
