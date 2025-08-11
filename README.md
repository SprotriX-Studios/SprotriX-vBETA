<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SprotriX BETA - Plataforma musical</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    body {
      margin: 0; font-family: 'Montserrat', sans-serif;
      background: #0a0a0a;
      color: #ddd;
      display: flex; flex-direction: column; min-height: 100vh;
    }
    header {
      background: linear-gradient(90deg, #4b0082, #8a2be2, #00ffff);
      padding: 1rem 2rem;
      color: #fff;
      font-weight: 700;
      font-size: 1.5rem;
      text-align: center;
      user-select: none;
    }
    nav {
      display: flex;
      background: #110044;
      box-shadow: 0 2px 8px #330088aa;
      overflow-x: auto;
    }
    nav button.nav-btn {
      flex: none;
      background: transparent;
      border: none;
      color: #aaa;
      padding: 0.8rem 1.2rem;
      cursor: pointer;
      font-weight: 600;
      transition: color 0.3s ease;
    }
    nav button.nav-btn.active,
    nav button.nav-btn:hover {
      color: #00ffff;
      text-shadow: 0 0 8px #00ffff;
    }
    main {
      flex-grow: 1;
      padding: 2rem;
      background: #121021;
      max-width: 900px;
      margin: 0 auto;
    }
    section {
      display: none;
      animation: fadeIn 0.6s ease forwards;
    }
    section.active {
      display: block;
    }
    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(8px);}
      to {opacity: 1; transform: translateY(0);}
    }
    h2 {
      color: #8a2be2;
      border-bottom: 2px solid #00ffff;
      padding-bottom: 0.3rem;
      margin-bottom: 1rem;
    }
    p {
      line-height: 1.5;
      color: #ccc;
    }
    ul {
      list-style: none;
      padding-left: 0;
    }
    ul li {
      margin-bottom: 0.8rem;
      font-weight: 600;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #330088;
      padding-bottom: 0.4rem;
    }
    button.apuntate,
    button.reclamar,
    button.copy-link {
      background: linear-gradient(45deg, #8a2be2, #00ffff);
      border: none;
      color: #000;
      font-weight: 700;
      cursor: pointer;
      padding: 0.3rem 0.7rem;
      border-radius: 4px;
      transition: background 0.3s ease;
    }
    button.apuntate:hover,
    button.reclamar:hover,
    button.copy-link:hover {
      background: #00ffff;
      color: #111;
      text-shadow: 0 0 4px #4b0082;
    }
    form label {
      display: block;
      margin-bottom: 0.5rem;
      font-weight: 600;
    }
    form input[type="text"],
    form input[type="file"] {
      width: 100%;
      padding: 0.4rem;
      margin-bottom: 1rem;
      border-radius: 4px;
      border: none;
      font-size: 1rem;
    }
    form button {
      background: #8a2be2;
      border: none;
      padding: 0.6rem 1.2rem;
      color: #fff;
      font-weight: 700;
      cursor: pointer;
      border-radius: 4px;
      transition: background 0.3s ease;
    }
    form button:hover {
      background: #00ffff;
      color: #000;
      text-shadow: 0 0 6px #4b0082;
    }
    footer {
      background: #110044;
      color: #555;
      text-align: center;
      padding: 1rem 0;
      font-size: 0.9rem;
      user-select: none;
    }
    /* Scrollbar nav */
    nav::-webkit-scrollbar {
      height: 6px;
    }
    nav::-webkit-scrollbar-thumb {
      background: #4b0082cc;
      border-radius: 10px;
    }
    nav::-webkit-scrollbar-track {
      background: transparent;
    }
  </style>
</head>
<body>

<header>
  SprotriX - Plataforma Musical BETA
</header>

<nav>
  <button class="nav-btn active" data-target="inicio">Inicio</button>
  <button class="nav-btn" data-target="descargas">Descargas</button>
  <button class="nav-btn" data-target="subir-cancion">Subir Canción</button>
  <button class="nav-btn" data-target="a-escuchar">A Escuchar</button>
  <button class="nav-btn" data-target="listas">Listas</button>
  <button class="nav-btn" data-target="premios">Premios</button>
  <button class="nav-btn" data-target="estudio">Estudio</button>
  <button class="nav-btn" data-target="albumes-top">Álbumes Top</button>
  <button class="nav-btn" data-target="ganadores">Ganadores</button>
  <button class="nav-btn" data-target="noticias">Noticias SprotriX</button>
  <button class="nav-btn" data-target="enlace-app">Enlace App vBETA</button>
</nav>

<main>
  <!-- INICIO -->
  <section id="inicio" class="active">
    <h2>Bienvenido a la BETA de SprotriX</h2>
    <p>Esta es una versión preliminar de la plataforma musical. Muchas funciones están limitadas o no disponibles.</p>
  </section>

  <!-- DESCARGAS -->
  <section id="descargas">
    <h2>Instalaciones y Apps Hermanas</h2>
    <ul>
      <li>Gestiona tus premios <button class="apuntate">Descargar</button></li>
      <li>SprotriX Studio for Artist <button class="apuntate">Descargar</button></li>
      <li>Estudio musical SprotriX <button class="apuntate">Descargar</button></li>
      <li>Spotify <button class="apuntate">Descargar</button></li>
    </ul>
    <p><em>Nota: Spotify ya no se puede descargar, no es un fallo, es pasá de moda.</em></p>
  </section>

  <!-- SUBIR CANCIÓN -->
  <section id="subir-cancion">
    <h2>Subir Canción</h2>
    <form id="upload-form">
      <label for="song-title">Título de la canción:</label>
      <input type="text" id="song-title" name="song-title" required />
      <label for="song-file">Archivo de audio:</label>
      <input type="file" id="song-file" name="song-file" accept="audio/*" required />
      <button type="submit">Subir</button>
    </form>
    <p><em>Función no disponible en esta BETA.</em></p>
  </section>

  <!-- A ESCUCHAR -->
  <section id="a-escuchar">
    <h2>A Escuchar</h2>
    <p>Explora las canciones más populares próximamente...</p>
    <p><em>Esta función está en desarrollo.</em></p>
  </section>

  <!-- LISTAS -->
  <section id="listas">
    <h2>Listas</h2>
    <p>No hay listas disponibles en esta BETA.</p>
  </section>

  <!-- PREMIOS -->
  <section id="premios">
    <h2>Premios SprotriX</h2>
    <ul>
      <li>Beats Awards <button class="apuntate">Apúntate</button></li>
      <li>Duo Awards <button class="apuntate">Apúntate</button></li>
      <li>Bands Win Awards <button class="apuntate">Apúntate</button></li>
      <li>Freestyle Awards <button class="apuntate">Apúntate</button></li>
      <li>Traps Awards <button class="apuntate">Apúntate</button></li>
      <li>Emergents Awards <button class="apuntate">Apúntate</button></li>
      <li>Funny Awards <button class="apuntate">Apúntate</button></li>
      <li>Productors Awards <button class="apuntate">Apúntate</button></li>
      <li>Cantada del Año <button class="apuntate">Apúntate</button></li>
      <li>Premios Pacos <button class="apuntate">Apúntate</button></li>
      <li>Mierdaza Awards <button class="apuntate">Apúntate</button></li>
      <li>Agost Awards <button class="apuntate">Apúntate</button></li>
      <li>Podcast Awards <button class="apuntate">Apúntate</button></li>
      <li>Oyents Awards <button class="apuntate">Apúntate</button></li>
      <li>Disco de Coro <button class="reclamar">Reclamar</button></li>
      <li>Disco de Casino Podcatero <button class="reclamar">Reclamar</button></li>
    </ul>
    <p><em>En la versión normal, para reclamar premios debes tener suficientes escuchas.</em></p>
  </section>

  <!-- ESTUDIO -->
  <section id="estudio">
    <h2>Estudio de Producción Musical</h2>
    <p>Espacio dedicado para producir, mezclar y crear tu música con tecnología avanzada.</p>
    <p><em>Función no disponible en esta BETA.</em></p>
  </section>

  <!-- ÁLBUMES TOP -->
  <section id="albumes-top">
    <h2>Álbumes Top del Mes</h2>
    <p>No hay ningún álbum por el momento.</p>
  </section>

  <!-- GANADORES -->
  <section id="ganadores">
    <h2>Ganadores</h2>
    <p>No hay ganadores aún, esta sección estará disponible pronto.</p>
  </section>

  <!-- NOTICIAS -->
  <section id="noticias">
    <h2>Noticias SprotriX</h2>
    <p>Esta sección mostrará noticias relevantes en la versión final.</p>
    <p><em>Actualmente en desarrollo.</em></p>
  </section>

  <!-- ENLACE APP VBETA -->
  <section id="enlace-app">
    <h2>Enlace para descargar la App vBETA</h2>
    <p>Descarga la versión BETA para Android y Apple desde el siguiente enlace:</p>
    <button class="copy-link">Copiar enlace de la BETA</button>
    <p id="copy-msg" style="margin-top: 1rem; color: #00ffff; font-weight: 700;"></p>
  </section>
</main>

<footer>
  &copy; 2025 SprotriX - Plataforma musical &bull; Versión BETA
</footer>

<script>
  // Navegación entre secciones
  const buttons = document.querySelectorAll('nav button.nav-btn');
  const sections = document.querySelectorAll('main section');

  buttons.forEach(button => {
    button.addEventListener('click', () => {
      buttons.forEach(btn => btn.classList.remove('active'));
      sections.forEach(sec => sec.classList.remove('active'));
      button.classList.add('active');
      const target = button.getAttribute('data-target');
      document.getElementById(target).classList.add('active');
      // Limpiar mensajes de copiar enlace
      if (target !== 'enlace-app') {
        document.getElementById('copy-msg').textContent = '';
      }
    });
  });

  // Botones Apúntate muestran alerta no disponible
  const apuntateButtons = document.querySelectorAll('button.apuntate');
  apuntateButtons.forEach(btn => {
    btn.addEventListener('click', () => {
      alert('No disponible en la BETA');
    });
  });

  // Botones Reclamar premios "Disco de Coro" y "Disco de Casino Podcatero"
  const reclamarButtons = document.querySelectorAll('button.reclamar');
  reclamarButtons.forEach(btn => {
    btn.addEventListener('click', () => {
      alert('No puedes subir música en la BETA, por lo tanto no puedes obtener escuchas ni este premio, lo sentimos.');
    });
  });

  // Form subir canción: no sube, solo alerta
  const uploadForm = document.getElementById('upload-form');
  uploadForm.addEventListener('submit', (e) => {
    e.preventDefault();
    alert('Subida de canción no disponible en la BETA');
  });

  // Botón copiar enlace app vBETA
  const copyLinkBtn = document.querySelector('button.copy-link');
  copyLinkBtn.addEventListener('click', () => {
    const url = window.location.href;
    navigator.clipboard.writeText(url).then(() => {
      const msg = document.getElementById('copy-msg');
      msg.textContent = 'Enlace copiado al portapapeles.';
      setTimeout(() => { msg.textContent = ''; }, 4000);
    }).catch(() => {
      alert('No se pudo copiar el enlace automáticamente, por favor cópialo manualmente.');
    });
  });

  // Descargas: botón descarga para apps hermanas y Spotify
  const descargaBtns = document.querySelectorAll('#descargas button.apuntate');
  descargaBtns.forEach((btn, i) => {
    btn.addEventListener('click', () => {
      const appName = btn.parentElement.textContent.trim().replace('Descargar', '');
      if (appName.toLowerCase().includes('spotify')) {
        alert('Esta app ya no se puede descargar, no es un fallo, es pasá de moda.');
      } else {
        alert(`La descarga de "${appName.trim()}" no está disponible en esta BETA.`);
      }
    });
  });
</script>

</body>
</html> 
