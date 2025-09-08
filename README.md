
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>🌌 Personalización del Universo V2.5 - By ➪𝐁𝐞𝐫𝐌𝐚𝐭_𝐌𝐨𝐝𝐬𖤍</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=Poppins:wght@400;500;600&display=swap" rel="stylesheet">
  <style>
    /* === FONDO Y BASE === */
    body {
      font-family: 'Poppins', sans-serif;
      background: #000 url('img/fondo.jpg') no-repeat center center fixed;
      background-size: cover;
      color: #fff;
      margin: 0;
      padding: 20px;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      overflow: auto;
      cursor: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAAzElEQVRYR+2T2w6CMBBE/e8/vU8XFiIIiqIfYDAzc86F0Hx44GZaJ+2jTQDn4Dycj/NxPs7H+Tgf5+N8nI/zcT7Ox/k4H+fjfJyP83E+zsclzMc16vv2928KZvMJn7P9jgIAaI10B9wCyABcADeAFeAEOAE2gBPABnACPAAvgBfgDfgAPoAv4Af4An4Dfw=='), auto;
    }

    /* === MARCA DE AGUA BRILLANTE === */
    .watermark {
      position: fixed;
      bottom: 15px;
      left: 50%;
      transform: translateX(-50%) scale(1);
      font-size: 1.4em;
      font-weight: bold;
      color: #FFD700;
      text-shadow: 0 0 10px #FFD700, 0 0 20px #FFD700, 0 0 30px #FFA500;
      z-index: 1000;
      background: rgba(0, 0, 0, 0.6);
      padding: 10px 25px;
      border-radius: 20px;
      border: 1px solid #FFD700;
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
      animation: pulse 2.5s infinite alternate, float 3s ease-in-out infinite;
      letter-spacing: 2px;
      font-family: 'Orbitron', sans-serif;
    }

    @keyframes pulse {
      0% { opacity: 0.8; text-shadow: 0 0 10px #FFD700; }
      100% { opacity: 1; text-shadow: 0 0 20px #FFD700, 0 0 30px #FFA500; }
    }

    @keyframes float {
      0%, 100% { transform: translateX(-50%) translateY(0); }
      50% { transform: translateX(-50%) translateY(-5px); }
    }

    /* === CONTENEDOR PRINCIPAL - NEGRO CON BORDES DORADOS BRILLANTES === */
    .form-container {
      background: radial-gradient(circle at center, #0a0a0a, #000) url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="none" stroke="%23FFD700" stroke-width="0.5" stroke-opacity="0.2"/></svg>') repeat;
      padding: 45px;
      max-width: 90%;
      width: 500px;
      margin: 40px auto;
      border-radius: 30px;
      box-shadow: 
        0 0 30px rgba(255, 215, 0, 0.3),
        0 0 60px rgba(255, 165, 0, 0.15) inset;
      position: relative;
      z-index: 1;
      backdrop-filter: blur(10px);
      border: 2px solid #FFD700;
      overflow: hidden;
      animation: fadeIn 1.2s ease-out;
    }

    .form-container::before {
      content: '';
      position: absolute;
      top: -10px; left: -10px; right: -10px; bottom: -10px;
      background: linear-gradient(45deg, transparent, #FFD700, transparent, #FFA500);
      background-size: 400% 400%;
      z-index: -1;
      border-radius: 35px;
      animation: shimmer 6s ease-in-out infinite;
      pointer-events: none;
    }

    @keyframes shimmer {
      0%, 100% { opacity: 0.3; }
      50% { opacity: 0.7; }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h2 {
      text-align: center;
      color: #FFD700;
      font-family: 'Orbitron', sans-serif;
      font-size: 2.4em;
      margin-bottom: 20px;
      text-shadow: 0 0 15px #FFD700, 0 0 25px #FFA500;
      letter-spacing: 2px;
      animation: glow 2s ease-in-out infinite alternate;
    }

    @keyframes glow {
      from { text-shadow: 0 0 10px #FFD700; }
      to { text-shadow: 0 0 20px #FFD700, 0 0 30px #FFA500; }
    }

    .intro-message {
      text-align: center;
      color: #fff;
      font-size: 1.15em;
      font-style: italic;
      margin-bottom: 25px;
      text-shadow: 0 0 8px rgba(255, 215, 0, 0.4);
    }

    .section-title {
      color: #FFD700;
      font-size: 1.4em;
      font-weight: bold;
      margin: 30px 0 15px;
      padding: 15px;
      text-align: center;
      background: rgba(255, 215, 0, 0.1);
      border-radius: 14px;
      box-shadow: 0 0 15px rgba(255, 215, 0, 0.2);
      border: 1px solid #FFD700;
      letter-spacing: 1px;
      font-family: 'Orbitron', sans-serif;
      animation: floatLine 3s ease-in-out infinite;
    }

    @keyframes floatLine {
      0%, 100% { box-shadow: 0 0 15px rgba(255, 215, 0, 0.2); }
      50% { box-shadow: 0 0 25px rgba(255, 215, 0, 0.4); }
    }

    label {
      display: block;
      margin-top: 18px;
      font-weight: 600;
      color: #FFD700;
      font-size: 1.1em;
      text-shadow: 0 0 5px rgba(255, 215, 0, 0.3);
    }

    .input-container, .button-container {
      display: flex;
      align-items: center;
      gap: 12px;
      flex-wrap: wrap;
      padding: 14px;
      margin-bottom: 14px;
      border-radius: 16px;
      box-shadow: 0 0 12px rgba(255, 215, 0, 0.15);
      border: 1px solid rgba(255, 215, 0, 0.2);
      transition: transform 0.3s ease;
    }

    .input-container:hover, .button-container:hover {
      transform: translateY(-3px);
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.3);
    }

    input {
      width: 100%;
      padding: 15px;
      margin-top: 8px;
      border-radius: 14px;
      border: 2px solid #FFD700;
      background: rgba(0, 0, 0, 0.4);
      color: #fff;
      font-size: 1em;
      box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.5);
      transition: all 0.3s ease;
    }

    input:focus {
      outline: none;
      border-color: #FFA500;
      box-shadow: 0 0 0 3px rgba(255, 215, 0, 0.3), inset 0 2px 8px rgba(0, 0, 0, 0.6);
      transform: scale(1.03);
    }

    input::placeholder {
      color: rgba(255, 215, 0, 0.5);
    }

    button {
      background: linear-gradient(45deg, #FFD700, #FFA500);
      color: #000;
      font-weight: bold;
      cursor: pointer;
      padding: 15px;
      border: none;
      border-radius: 14px;
      font-size: 1.05em;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.4);
      transition: all 0.3s ease;
      text-shadow: 0 1px 2px rgba(0, 0, 0, 0.5);
    }

    button:hover {
      background: linear-gradient(45deg, #FFA500, #FFD700);
      transform: scale(1.08) rotate(1deg);
      box-shadow: 0 8px 20px rgba(255, 215, 0, 0.5);
    }

    .show-button {
      background: linear-gradient(45deg, #00ff85, #00cc66) !important;
      color: #000 !important;
      font-size: 0.95em !important;
      padding: 10px 14px !important;
      width: auto !important;
    }

    .show-button:hover {
      background: linear-gradient(45deg, #00cc66, #00ff85) !important;
    }

    /* === MENSAJES === */
    .success, .error {
      margin-top: 20px;
      padding: 16px;
      border-radius: 14px;
      text-align: center;
      font-weight: bold;
      animation: fadeIn 0.5s ease;
      border: 1px solid rgba(255, 215, 0, 0.3);
    }

    .success {
      color: #00ff85;
      background: rgba(0, 255, 133, 0.15);
    }

    .error {
      color: #FFD700;
      background: rgba(255, 215, 0, 0.1);
    }

    /* === LINKS === */
    .link-container {
      margin-top: 30px;
      text-align: center;
    }

    .link-message {
      background: rgba(0, 0, 0, 0.6);
      border: 2px solid #FFD700;
      border-radius: 16px;
      padding: 20px;
      color: #fff;
      font-size: 1.05em;
      line-height: 1.7;
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.2);
    }

    .link-high input {
      background: rgba(255, 215, 0, 0.1);
      color: #FFD700;
      border: 1px solid #FFD700;
      font-weight: bold;
    }

    .link-high button {
      background: #00ff85;
      color: #000;
    }

    .link-high button:hover {
      background: #00cc66;
    }

    /* === CONTENEDORES OCULTOS === */
    .photos-container, .phrases-container {
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.7s ease-out;
      margin-top: 15px;
      padding: 16px;
      background: rgba(255, 215, 0, 0.05);
      border-radius: 14px;
      border: 1px solid rgba(255, 215, 0, 0.1);
    }

    .photos-container.open, .phrases-container.open {
      max-height: 3000px;
    }

    .phrases-message {
      text-align: center;
      color: #aaa;
      font-size: 1em;
      margin: 15px 0;
      font-style: italic;
    }

    /* === PANEL DE YAPE === */
    .support-panel {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) scale(0.9);
      width: 90%;
      max-width: 450px;
      max-height: 80vh;
      background: #000;
      border: 2px solid #FFD700;
      border-radius: 25px;
      box-shadow: 0 0 40px rgba(255, 215, 0, 0.4);
      z-index: 1000;
      opacity: 0;
      pointer-events: none;
      transition: all 0.4s ease;
      padding: 30px;
      overflow-y: auto;
    }

    .support-panel.open {
      opacity: 1;
      pointer-events: auto;
      transform: translate(-50%, -50%) scale(1);
    }

    .support-panel header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: linear-gradient(45deg, #FFD700, #FFA500);
      color: #000;
      font-weight: bold;
      padding: 16px 20px;
      border-radius: 20px 20px 0 0;
      font-size: 1.3em;
      font-family: 'Orbitron', sans-serif;
    }

    .support-panel header button {
      background: transparent;
      border: none;
      font-size: 1.4em;
      cursor: pointer;
      color: #000;
    }

    .support-panel header button:hover {
      transform: rotate(90deg);
    }

    .support-panel .support-message {
      color: #fff;
      font-size: 1.15em;
      margin: 25px 0;
      line-height: 1.7;
      text-shadow: 0 0 5px rgba(255, 215, 0, 0.3);
    }

    .payment-option {
      background: rgba(255, 215, 0, 0.1);
      padding: 25px;
      border-radius: 18px;
      margin-bottom: 25px;
      border: 1px solid rgba(255, 215, 0, 0.2);
      box-shadow: 0 0 15px rgba(255, 215, 0, 0.1);
      transition: transform 0.3s ease;
    }

    .payment-option:hover {
      transform: scale(1.03);
      box-shadow: 0 0 25px rgba(255, 215, 0, 0.2);
    }

    .payment-option h3 {
      color: #FFD700;
      font-size: 1.3em;
      margin-bottom: 15px;
      text-shadow: 0 0 8px rgba(255, 215, 0, 0.4);
      font-family: 'Orbitron', sans-serif;
    }

    .yape-number {
      font-family: 'Orbitron', monospace;
      font-size: 1.8em;
      color: #FFD700;
      margin: 15px 0;
      text-shadow: 0 0 10px #FFD700;
    }

    .logo-container {
      display: flex;
      justify-content: center;
      margin-top: 15px;
    }

    .logo-container img {
      width: 160px;
      border-radius: 14px;
      box-shadow: 0 5px 20px rgba(0, 0, 0, 0.5);
    }

    .support-panel button {
      background: linear-gradient(45deg, #FFD700, #FFA500);
      color: #000;
      font-size: 1.15em;
      padding: 16px;
      border: none;
      border-radius: 16px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.4);
      margin-top: 10px;
    }

    .support-panel button:hover {
      transform: scale(1.08);
      box-shadow: 0 8px 25px rgba(255, 215, 0, 0.6);
    }

    /* === ANIMACIONES DE EMOJIS 🧑‍💻 === */
    .emoji {
      position: fixed;
      font-size: 2em;
      pointer-events: none;
      z-index: 9999;
      animation: floatEmoji 1.5s ease-out forwards;
      opacity: 0;
    }

    @keyframes floatEmoji {
      0% { transform: translate(0, 0) rotate(0deg); opacity: 1; }
      100% { transform: translate(var(--tx), var(--ty)) rotate(360deg); opacity: 0; }
    }

    @media (max-width: 600px) {
      .form-container { width: 95%; padding: 30px; }
      h2 { font-size: 2em; }
      .watermark { font-size: 1.1em; }
    }
  </style>
</head>
<body>

  <!-- === PANEL DE APOYO (SÓLO YAPE) === -->
  <div class="support-panel" id="supportPanel">
    <header>✨ Apoya a BerMatMods<button onclick="cerrarSupportPanel()">×</button></header>
    <p class="support-message">
      Este proyecto es 100% gratuito y sin anuncios. Si te gusta, puedes apoyarme con un gesto. ¡Cualquier ayuda es bienvenida! 🙌
    </p>
    <div class="payment-option">
      <h3>🇵🇪 Yape – ¡Gracias por tu apoyo!</h3>
      <div class="yape-number">930569195</div>
      <p style="color:#aaa;font-size:0.95em;">📱 Copia el número o escanea el código</p>
      <div class="logo-container">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/08/Icono_de_la_aplicaci%C3%B3n_Yape.png" alt="Yape Logo">
      </div>
      <button onclick="copiarYape()">📋 Copiar Número</button>
    </div>
  </div>

  <!-- === FORMULARIO PRINCIPAL === -->
  <div class="form-container">
    <h2>🌌 UNIVERSO V2.5</h2>
    <p class="intro-message">Crea tu propio universo con frases y fotos que orbitarán tu planeta. ¡Totalmente personalizable!</p>

    <div class="input-container">
      <div style="flex: 1;">
        <label>🆔 Crea tu ID:</label>
        <input type="text" id="usuario" placeholder="Ej: miuniverso123">
      </div>
      <button class="show-button" onclick="mostrarGuia('usuario')">Guía</button>
    </div>

    <div class="input-container">
      <div style="flex: 1;">
        <label>🌍 Nombre en el Planeta:</label>
        <input type="text" id="nombrePlaneta" placeholder="Ej: Luna">
      </div>
      <button class="show-button" onclick="mostrarGuia('nombrePlaneta')">Guía</button>
    </div>

    <div class="section-title">🌟 Frases Girando</div>
    <div class="button-container">
      <button onclick="togglePhrasesContainer()">Desplegar Frases</button>
      <button class="show-button" onclick="mostrarGuia('fraseGirando')">Guía</button>
    </div>
    <div class="phrases-container" id="phrasesContainer">
      <div class="phrases-message">Solo necesitas una frase, ¡pero puedes agregar hasta 5!</div>
      <label>🌟 Frase 1:</label><input type="text" id="fraseGirando1" placeholder="Ej: Te amo">
      <label>🌟 Frase 2:</label><input type="text" id="fraseGirando2" placeholder="Ej: Siempre juntos">
      <label>🌟 Frase 3:</label><input type="text" id="fraseGirando3" placeholder="Ej: Mi amor">
      <label>🌟 Frase 4:</label><input type="text" id="fraseGirando4" placeholder="Ej: Eres mi todo">
      <label>🌟 Frase 5:</label><input type="text" id="fraseGirando5" placeholder="Ej: Para siempre">
    </div>

    <div class="section-title">📸 Fotos Girando</div>
    <div class="button-container">
      <button onclick="togglePhotosContainer()">Desplegar Fotos</button>
      <button class="show-button" onclick="mostrarGuia('fotoGirando')">Guía</button>
    </div>
    <div class="phrases-container" id="photosContainer">
      <div class="phrases-message">Solo necesitas una foto, ¡pero puedes agregar hasta 10!</div>
      <label>📸 Foto 1:</label><input type="file" id="fotoGirando1" accept="image/*">
      <label>📸 Foto 2:</label><input type="file" id="fotoGirando2" accept="image/*">
      <label>📸 Foto 3:</label><input type="file" id="fotoGirando3" accept="image/*">
      <label>📸 Foto 4:</label><input type="file" id="fotoGirando4" accept="image/*">
      <label>📸 Foto 5:</label><input type="file" id="fotoGirando5" accept="image/*">
      <label>📸 Foto 6:</label><input type="file" id="fotoGirando6" accept="image/*">
      <label>📸 Foto 7:</label><input type="file" id="fotoGirando7" accept="image/*">
      <label>📸 Foto 8:</label><input type="file" id="fotoGirando8" accept="image/*">
      <label>📸 Foto 9:</label><input type="file" id="fotoGirando9" accept="image/*">
      <label>📸 Foto 10:</label><input type="file" id="fotoGirando10" accept="image/*">
    </div>

    <div class="input-container">
      <div style="flex: 1;">
        <label>💫 Foto de la Estrella Fugaz:</label>
      </div>
      <button class="show-button" onclick="mostrarGuia('estrellaFugaz')">Guía</button>
    </div>
    <input type="file" id="estrellaFugaz" accept="image/*">

    <button onclick="guardarInformacion()">Guardar Información</button>
    <button onclick="abrirSupportPanel()">💖 Apoyar al Creador</button>

    <div id="mensaje"></div>

    <div class="link-container" id="linkContainer" style="display: none;">
      <div class="link-message">
        <strong>📌 Elige tu enlace:</strong><br><br>
        💻 <strong>PC / Gama Alta</strong>
        <div class="link-high">
          <input type="text" id="linkGeneradoHigh" readonly>
          <button onclick="compartirWhatsapp('high')">💬 Compartir (💻 Alta)</button>
        </div>
        <br>
        📱 <strong>Gama Baja</strong>
        <div class="link-low">
          <input type="text" id="linkGeneradoLow" readonly>
          <button onclick="compartirWhatsapp('low')">💬 Compartir (📱 Baja)</button>
        </div>
      </div>
    </div>
  </div>

  <!-- === MARCA DE AGUA FINAL === -->
  <div class="watermark">By ➪𝐁𝐞𝐫𝐌𝐚𝐭_𝐌𝐨𝐝𝐬𖤍</div>

  <!-- === SCRIPTS === -->
  <script type="module">
    import { initializeApp } from 'https://www.gstatic.com/firebasejs/9.22.2/firebase-app.js';
    import { getDatabase, ref, set, get } from 'https://www.gstatic.com/firebasejs/9.22.2/firebase-database.js';

    const firebaseConfig = {
      apiKey: "AIzaSyDpOr0m4RL00yNfXZRSPTpLdM3oGNNnxlc",
      authDomain: "universo-dfd68.firebaseapp.com",
      databaseURL: "https://universo-dfd68-default-rtdb.firebaseio.com",
      projectId: "universo-dfd68",
      storageBucket: "universo-dfd68.firebasestorage.app",
      messagingSenderId: "854783882661",
      appId: "1:854783882661:web:6588b7701cf4614b99e44c",
      measurementId: "G-ZQXQ3RBE48"
    };

    const app = initializeApp(firebaseConfig);
    const database = getDatabase(app);

    // === FUNCIONES ===
    window.onload = () => {
      console.log("%cCreado con 💻 por BerMatMods", "color: #FFD700; font-size: 18px; font-weight: bold; text-shadow: 0 0 5px #FFA500;");
    };

    window.abrirSupportPanel = () => {
      document.getElementById("supportPanel").classList.add("open");
      crearExplosionEmojis();
    };

    window.cerrarSupportPanel = () => {
      document.getElementById("supportPanel").classList.remove("open");
    };

    window.togglePhotosContainer = () => {
      document.getElementById("photosContainer").classList.toggle("open");
    };

    window.togglePhrasesContainer = () => {
      document.getElementById("phrasesContainer").classList.toggle("open");
    };

    window.mostrarGuia = (tipo) => {
      alert("Guía: " + tipo);
    };

    window.guardarInformacion = () => {
      const usuario = document.getElementById("usuario").value.trim().toLowerCase();
      const mensajeDiv = document.getElementById("mensaje");

      if (!usuario) {
        mensajeDiv.innerHTML = '<div class="error">⚠️ Por favor, crea un ID.</div>';
        return;
      }

      // Simulación de guardado
      setTimeout(() => {
        const linkHigh = `https://tu-dominio.com/universo/${usuario}?v=high`;
        const linkLow = `https://tu-dominio.com/universo/${usuario}?v=low`;

        document.getElementById("linkGeneradoHigh").value = linkHigh;
        document.getElementById("linkGeneradoLow").value = linkLow;
        document.getElementById("linkContainer").style.display = "block";

        mensajeDiv.innerHTML = '<div class="success">✅ ¡Información guardada! 🚀</div>';
        crearExplosionEmojis();
      }, 800);
    };

    window.compartirWhatsapp = (tipo) => {
      const link = document.getElementById(`linkGenerado${tipo.charAt(0).toUpperCase() + tipo.slice(1)}`).value;
      if (link) {
        const mensaje = encodeURIComponent(`¡Mira mi universo personalizado! 🌌 ${link}`);
        window.open(`https://wa.me/?text=${mensaje}`, '_blank');
        crearExplosionEmojis();
      }
    };

    window.copiarYape = () => {
      navigator.clipboard.writeText("930569195").then(() => {
        alert("✅ Número de Yape copiado: 930569195");
        crearExplosionEmojis();
      });
    };

    // === EXPLOSIÓN DE EMOJIS 🧑‍💻 ===
    function crearExplosionEmojis() {
      const emojis = ['🧑‍💻', '✨', '🚀', '🔥', '💫', '🌟', '🎉'];
      for (let i = 0; i < 15; i++) {
        const emoji = document.createElement('div');
        emoji.classList.add('emoji');
        emoji.innerText = emojis[Math.floor(Math.random() * emojis.length)];
        
        const x = Math.random() * window.innerWidth;
        const y = Math.random() * window.innerHeight;
        
        emoji.style.left = `${x}px`;
        emoji.style.top = `${y}px`;
        
        const tx = (Math.random() - 0.5) * 300;
        const ty = (Math.random() - 0.5) * 300;
        emoji.style.setProperty('--tx', `${tx}px`);
        emoji.style.setProperty('--ty', `${ty}px`);
        
        document.body.appendChild(emoji);
        
        setTimeout(() => emoji.remove(), 1500);
      }
    }

    // Pulsación en cualquier parte genera emojis
    document.body.addEventListener('click', (e) => {
      if (e.target.tagName !== 'INPUT' && e.target.tagName !== 'TEXTAREA') {
        crearExplosionEmojis();
      }
    });
  </script>

</body>
</html>
