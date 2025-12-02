<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Café Cafecito | Tributos & Películas</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Schibsted+Grotesk:wght@400;500;700;800&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
  <style>
    :root {
      --hueso: #F8EDD6;
      --cafe-claro: #B35643;
      --verde: #7AA985;
      --negro: #050505;
      --blanco: #FFFFFF;
      --acento: #E8B796;
    }
    body {
      font-family: 'Inter', sans-serif;
      background-color: var(--hueso);
      color: var(--negro);
      margin: 0;
      line-height: 1.6;
    }
    h1, h2, h3, h4, .logo {
      font-family: 'Schibsted Grotesk', sans-serif;
      font-weight: 700;
      letter-spacing: -0.3px;
      color: var(--negro);
    }
    .logo {
      font-size: 1.8rem;
      font-weight: 800;
      color: var(--cafe-claro);
    }
    .site-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.5rem 3rem;
      background-color: var(--blanco);
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    }
    .main-nav a {
      margin-left: 2rem;
      color: var(--negro);
      text-decoration: none;
      font-weight: 500;
      font-family: 'Schibsted Grotesk', sans-serif;
      font-weight: 500;
    }
    .hero {
      height: 85vh;
      background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)),
                  url('https://images.pexels.com/photos/302902/pexels-photo-302902.jpeg') center/cover;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: var(--blanco);
      margin-top: 80px;
    }
    .hero h1 {
      font-size: 4rem;
      margin-bottom: 1rem;
      color: var(--blanco);
      text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
    }
    .hero p {
      font-size: 1.3rem;
      max-width: 700px;
      margin: 0 auto 2.5rem;
    }
    .seccion-contenedor {
      max-width: 1200px;
      margin: 0 auto;
      padding: 6rem 2rem;
    }
    .titulo-seccion {
      text-align: center;
      margin-bottom: 4rem;
      position: relative;
    }
    .titulo-seccion::after {
      content: '';
      display: block;
      width: 80px;
      height: 4px;
      background-color: var(--acento);
      margin: 1.5rem auto;
    }
    /* --- SECCIÓN 1 nosotros --- */
    .sobre-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 5rem;
      align-items: center;
    }
    /* --- SECCIÓN 2 productos --- */
    .categorias-productos {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 2.5rem;
      text-align: center;
    }
    .categoria-card {
      background: var(--blanco);
      border-radius: 15px;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(0,0,0,0.08);
      transition: transform 0.4s ease;
    }
    .categoria-card:hover {
      transform: translateY(-10px);
    }
    .categoria-img {
      width: 100%;
      height: 220px;
      object-fit: cover;
      border-bottom: 5px solid var(--verde);
    }
    .categoria-card:nth-child(2) .categoria-img { border-bottom-color: var(--cafe-claro); }
    .categoria-card:nth-child(3) .categoria-img { border-bottom-color: var(--acento); }
    .categoria-content {
      padding: 2rem;
    }
    /* --- SECCIÓN 3: evntos --- */
    .eventos-destacados {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
      gap: 3.5rem;
      margin-top: 2rem;
    }
    .evento-principal {
      background: var(--blanco);
      border-radius: 18px;
      overflow: hidden;
      box-shadow: 0 15px 40px rgba(0,0,0,0.1);
    }
    .evento-img {
      width: 100%;
      height: 280px;
      object-fit: cover;
    }
    .evento-content {
      padding: 2.5rem;
    }
    .badge-evento {
      display: inline-block;
      padding: 0.5rem 1.5rem;
      border-radius: 50px;
      font-family: 'Schibsted Grotesk', sans-serif;
      font-weight: 700;
      font-size: 0.9rem;
      margin-bottom: 1.5rem;
    }
    .badge-strokes {
      background-color: var(--negro);
      color: white;
    }
    .badge-shrek {
      background-color: var(--verde);
      color: white;
    }
    .evento-dias {
      background: rgba(0,0,0,0.03);
      border-radius: 12px;
      padding: 2rem;
      margin-top: 1.5rem;
    }
    .evento-dias ul {
      list-style: none;
      padding: 0;
    }
    .evento-dias li {
      padding: 1.2rem;
      border-bottom: 1px dashed #ddd;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .evento-dias li:last-child { border-bottom: none; }
    .fecha-destacada {
      background-color: rgba(183, 86, 67, 0.1);
      border-radius: 8px;
    }
    /* --- SECCIÓN 4: fomrs --- */
    #formulario-reserva {
      background-color: var(--blanco);
      padding: 3.5rem;
      border-radius: 15px;
      max-width: 750px;
      margin: 0 auto;
      box-shadow: 0 15px 35px rgba(0,0,0,0.08);
    }
    .btn-principal {
      background-color: var(--cafe-claro);
      color: white;
      border: none;
      padding: 1.2rem 3rem;
      border-radius: 50px;
      font-family: 'Schibsted Grotesk', sans-serif;
      font-weight: 700;
      font-size: 1.1rem;
      cursor: pointer;
      transition: all 0.3s;
      display: inline-block;
      text-decoration: none;
    }
    .btn-principal:hover {
      background-color: var(--negro);
      transform: translateY(-3px);
      box-shadow: 0 7px 15px rgba(0,0,0,0.2);
    }
  
    @media (max-width: 1100px) {
      .categorias-productos {
        grid-template-columns: 1fr;
        max-width: 500px;
        margin: 0 auto;
      }
      .eventos-destacados {
        grid-template-columns: 1fr;
      }
    }
    @media (max-width: 768px) {
      .hero h1 { font-size: 2.8rem; }
      .sobre-grid { grid-template-columns: 1fr; gap: 3rem; }
      .site-header { padding: 1rem; flex-direction: column; }
      .main-nav a { margin: 0 0.8rem; }
      .seccion-contenedor { padding: 4rem 1.5rem; }
    }
  </style>
</head>
<body>
  <!-- HEADER -->
  <header class="site-header">
       <img src="images/Asset 1.svg" alt="Café Cafecito" style="height: 50px;"> </div>
    <nav class="main-nav">
      <a href="#sobre-nosotros"><strong>Sobre nosotros</strong></a>
      <a href="#productos"><strong>Productos</strong></a>
      <a href="#eventos"><strong>Eventos</strong></a>
      <a href="#reserva"><strong>Reservar</strong></a>
    </nav>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div>
      
      <h1>CAFÉ, ROCK &amp; CINE</h1>
      <p>El lugar donde tu taza se llena de<strong> buena música</strong>, <strong>cine de culto</strong> y <strong>sabores</strong> que son lo <em><strong>más top</strong></em>.</p>
      <a href="#reserva" class="btn-principal">Reservar mi experiencia</a>
    </div>
  </section>

  <!-- SECCIÓN 1: nosotros-->
<section id="sobre-nosotros" class="seccion-contenedor">
    <h2 class="titulo-seccion">¿QUÉ ES CAFÉ CAFECITO?</h2>
    <div class="sobre-grid">
      <div>
        <p>No somos una cafetería cualquiera. Somos el <strong>punto de encuentro</strong> para quienes buscan algo más: una <strong>experiencia única</strong>.</p>
        <p>Nuestro proyecto nace de tres obsesiones: el <strong>café de especialidad</strong> impecable, la <strong>música que nos mueve&nbsp;</strong> &nbsp;y el <strong>cine que nos une.</strong> </p>
        <p>Cada detalle, desde el grano hasta el sonido, está elegido para que te sientas parte de algo distinto. Bienvenido a tu nuevo rincón.</p>
      </div>
      <div>
        <img src="https://images.pexels.com/photos/32416013/pexels-photo-32416013.jpeg" alt="Ambiente interior de Café Cafecito" style="width:100%; border-radius:15px; box-shadow: 0 20px 40px rgba(0,0,0,0.15);">
      </div>
    </div>
  </section>

  <!-- SECCIÓN 2: productos -->
<section id="productos" class="seccion-contenedor" style="background-color:rgba(255,255,255,0.5);">
    <h2 class="titulo-seccion">NUESTRA <strong><em>CARTA</em></strong></h2>
  <p style="text-align:center; max-width:700px; margin:0 auto 4rem; font-size:1.1rem;">Diseñada para disfrutar solo, en pareja o con amigos. Todo es real, nada es simulado.</p>

    <div class="categorias-productos">
      <!-- CATEGORÍA 1: cafes  -->
      <div class="categoria-card">
        <img src="https://images.pexels.com/photos/894695/pexels-photo-894695.jpeg" alt="Variedad de cafés especiales" class="categoria-img">
        <div class="categoria-content">
          <h3>EL CAFÉ ES LO PRIMERO</h3>
          <p><strong>De especialidad.</strong> Desde un espresso balanceado hasta un frappé de origen único. También creamos tizanas, cold brew y bebidas únicas para los aventureros.</p>
        </div>
      </div>

      <!-- CATEGORÍA 2: hamburgueass -->
      <div class="categoria-card">
        <img src="https://images.pexels.com/photos/3219483/pexels-photo-3219483.jpeg" class="categoria-img">
        <div class="categoria-content">
          <h3>PARA LLEVAR AL LADO SALADO</h3>
          <p><strong>Hamburguesas artesanales</strong> con carne 100% de res, pollo crispy o nuestra opción vegana. <strong>Chapatas</strong> recién horneadas y snacks para compartir. Ideal para aguantar un maratón.</p>
        </div>
      </div>

      <!-- CATEGORÍA 3: vegis -->
      <div class="categoria-card">
        <img src="https://images.pexels.com/photos/1143754/pexels-photo-1143754.jpeg" alt="Bowl vegetariano colorido" class="categoria-img">
        <div class="categoria-content">
          <h3>LO VEGI (Y LO NO TAN VEGI)</h3>
          <p>Una <strong>sección dedicada</strong>: bowls vegetarianos, wraps veganos, hamburguesas de lenteja y quinoa, y opciones sin lactosa. Porque todos merecen disfrutar.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- SECCIÓN 3: eventos -->
  <section id="eventos" class="seccion-contenedor">
    <h2 class="titulo-seccion">EVENTOS <em>DICIEMBRE</em> 2025</h2>
    <p style="text-align:center; margin-bottom:3rem; font-size:1.1rem;">Dos planes, muchas fechas.<em> <strong>Elige la tuya</strong></em>.</p>

    <div class="eventos-destacados">
      <!-- EVENTO 1 -->
      <div class="evento-principal">
        <img src="images/the-strokes-logo.jpg" class="evento-img">
        <div class="evento-content">
          <span class="badge-evento badge-strokes">MÚSICA EN VIVO</span>
          <h3 style="font-size: 2.2rem; margin-bottom: 0.5rem;">TRIBUTO: THE STROKES</h3>
          <p style="font-size: 1.1rem; color: var(--cafe-claro); margin-bottom: 1rem;">Por "Los Monos Articos" · 8:00 PM · $120</p>
          <p>Revive la energía del garage rock revival con la banda tributo más auténtica. Cada noche dedicada a lo mejor de The Strokes.</p>
          
          <div class="evento-dias">
            <p style="font-weight: 700; margin-bottom: 1rem;">📅 3 noches especiales:</p>
            <ul>
              <li class="fecha-destacada">
                <span><strong>Jueves 11 Dic</strong></span>
                <span>Grandes éxitos</span>
              </li>
              <li>
                <span><strong>Viernes 12 Dic</strong></span>
                <span>Grandes éxitos</span>
              </li>
              <li>
                <span><strong>Sábado 13 Dic</strong></span>
                <span>Grandes éxitos</span>
              </li>
            </ul>
          </div>
          
          <div style="text-align:center; margin-top: 2.5rem;">
            <a href="#reserva" class="btn-principal" style="background: var(--negro);">Reservar para The Strokes</a>
          </div>
        </div>
      </div>

      <!-- EVENTO 2 -->
      <div class="evento-principal">
        <img src="images/sherk.jpg" class="evento-img">
        <div class="evento-content">
          <span class="badge-evento badge-shrek">CINE ENTRETENIDO</span>
          <h3 style="font-size: 2.2rem; margin-bottom: 0.5rem;">MARATÓN SHREK 1, 2 & 3</h3>
          <p style="font-size: 1.1rem; color: var(--verde); margin-bottom: 1rem;">Tardes de cine ogro · 4:00 PM · Entrada gratis con consumo mínimo ($60)</p>
          <p>Porque las capas tienen significado y los burros hablan. Un plan perfecto para reír, recordar y disfrutar del cine que nos hizo creer en los cuentos... al revés.</p>
          
          <div class="evento-dias">
            <p style="font-weight: 700; margin-bottom: 1rem;">🎬 Proyecciones por día:</p>
            <ul>
              <li class="fecha-destacada">
                <span><strong>Jueves 18 Dic</strong></span>
                <span>Shrek 1 (doblada)</span>
              </li>
              <li>
                <span><strong>Viernes 19 Dic</strong></span>
                <span>Shrek 2 (doblada)</span>
              </li>
              <li>
                <span><strong>Sábado 20 Dic</strong></span>
                <span>Shrek 3 (doblada)</span>
              </li>
            </ul>
          </div>
          
          <div style="text-align:center; margin-top: 2.5rem;">
            <a href="#reserva" class="btn-principal" style="background: var(--verde);">Reservar para Shrek</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- SECCIÓN 4: reserva -->
  <section id="reserva" class="seccion-contenedor" style="padding-top: 0;">
    <div id="formulario-reserva">
      <h2 class="titulo-seccion" style="margin-top: 0;">RESERVA TU EXPERIENCIA</h2>
      <p style="text-align:center; margin-bottom: 2.5rem; font-size: 1.1rem;">Elige evento, fecha y cuántos serán. Te confirmaremos vía email.</p>

      <form id="formReserva" action="https://script.google.com/macros/s/YOUR_SCRIPT_ID/exec" method="POST">
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 2rem; margin-bottom: 2rem;">
          <div>
            <label for="nombre" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Nombre completo *</label>
            <input type="text" id="nombre" name="nombre" required style="width: 100%; padding: 1rem; border-radius: 10px; border: 1px solid #ddd; font-family: 'Inter', sans-serif;">
          </div>
          <div>
            <label for="email" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Correo electrónico *</label>
            <input type="email" id="email" name="email" required style="width: 100%; padding: 1rem; border-radius: 10px; border: 1px solid #ddd; font-family: 'Inter', sans-serif;">
          </div>
        </div>

        <div style="margin-bottom: 2rem;">
          <label for="evento_interes" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Evento de interés *</label>
          <select id="evento_interes" name="evento_interes" required style="width: 100%; padding: 1rem; border-radius: 10px; border: 1px solid #ddd; font-family: 'Inter', sans-serif;">
            <option value="" disabled selected>Selecciona el evento que te late</option>
            <option value="strokes_jueves">The Strokes - Jueves 11 Dic</option>
            <option value="strokes_viernes">The Strokes - Viernes 12 Dic</option>
            <option value="strokes_sabado">The Strokes - Sábado 13 Dic</option>
            <option value="shrek_jueves">Shrek 1 - Jueves 18 Dic</option>
            <option value="shrek_viernes">Shrek 2 - Viernes 19 Dic</option>
            <option value="shrek_sabado">Shrek 3 + Trivia - Sábado 20 Dic</option>
          </select>
        </div>

        <div style="margin-bottom: 2.5rem;">
          <label for="comentarios" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Comentarios  o peticiones especiales</label>
          <textarea id="comentarios" name="comentarios" rows="4" placeholder="Ej: Somos 4 personas, una es vegana. ¡Nos encanta Shrek!" style="width: 100%; padding: 1rem; border-radius: 10px; border: 1px solid #ddd; font-family: 'Inter', sans-serif;"></textarea>
        </div>

        <button type="submit" class="btn-principal" style="width: 100%; font-size: 1.2rem; padding: 1.5rem;">
          ENVIAR RESERVA →
        </button>
      </form>
      <p id="mensaje-confirmacion" style="text-align:center; margin-top: 1.5rem; display:none; color: var(--verde); font-weight: 700; font-family: 'Schibsted Grotesk', sans-serif; font-size: 1.1rem;">
        ✅ ¡Listo! Te contactaremos pronto.
      </p>
    </div>
  </section>

  <!-- FOOTER -->
<footer style="background: var(--negro); color: var(--hueso); padding: 4rem 2rem; text-align: center;">
        <div style="margin-bottom: 2rem;">
     
      <img src="images/Asset 2.svg" alt="Café Cafecito" style="height: 50px;"></div> 
    </div>
    <p style="margin-bottom: 0.5rem;"><strong>&nbsp;</strong> &nbsp;Av. Juarez, #123. Puebla, Puebla.</p>
    <p style="margin-bottom: 2rem;">📞 Teléfono : 22 1234 5678 | 📧 cafecafecito@gmail.com</p>
    <p style="margin-top: 3rem; opacity: 0.7; font-size: 0.9rem;">© 2025 Café Cafecito.</p>
  </footer>

<script>
       document.getElementById('formReserva').addEventListener('submit', function(e) {
      e.preventDefault();
      document.getElementById('mensaje-confirmacion').style.display = 'block';
      setTimeout(() => {
        document.getElementById('mensaje-confirmacion').style.display = 'none';
      }, 5000);
      this.reset();
     
    });
  </script>
</body>
</html>
