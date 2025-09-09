
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content=
  "width=device-width, initial-scale=1.0">
  <title>Personalización del Universo V2.5</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: url('img/fondo.jpg') no-repeat center center fixed;
      background-size: cover;
      padding: 20px;
      margin: 0;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      overflow: auto;
    }

    .watermark {
      position: absolute;
      bottom: 10px;
      left: 50%;
      transform: translateX(-50%);
      color: rgba(255, 255, 255, 0.7);
      font-size: 1.2em;
      font-weight: bold;
      text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
      z-index: 0;
    }

    .form-container {
      background: linear-gradient(135deg, rgba(11, 27, 59, 0.9), rgba(42, 10, 92, 0.9));
      padding: 40px;
      max-width: 90%;
      width: 450px;
      margin: 20px auto;
      border-radius: 25px;
      box-shadow: 0 15px 40px rgba(0, 0, 0, 0.5);
      position: relative;
      z-index: 1;
      backdrop-filter: blur(8px);
      color: #e6e6ff;
      animation: fadeIn 1s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h2 {
      text-align: center;
      color: #b300ff;
      font-size: 2em;
      margin-bottom: 25px;
      text-shadow: 0 2px 6px rgba(0, 0, 0, 0.6);
      font-weight: 700;
    }

    .intro-message {
      text-align: center;
      color: #e6e6ff;
      font-size: 1.1em;
      font-style: italic;
      margin-bottom: 25px;
      text-shadow: 0 1px 3px rgba(0, 0, 0, 0.5);
    }

    .section-title {
      color: #ffffff;
      font-size: 1.2em;
      font-weight: bold;
      margin-top: 20px;
      margin-bottom: 10px;
      text-shadow: 0 1px 3px rgba(0, 0, 0, 0.5);
      padding: 12px;
      background: rgba(255, 255, 255, 0.08);
      border-radius: 10px;
      box-shadow: 0 3px 6px rgba(0, 0, 0, 0.4);
    }

    label {
      display: block;
      margin-top: 15px;
      font-weight: bold;
      color: #e6e6ff;
      font-size: 1.1em;
    }

    .input-container, .button-container {
      display: flex;
      align-items: center;
      gap: 10px;
      flex-wrap: wrap;
      padding: 15px;
      margin-bottom: 10px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
    }

    .input-container:nth-child(odd), .button-container:nth-child(odd) {
      background: rgba(255, 255, 255, 0.12);
    }

    .input-container:nth-child(even), .button-container:nth-child(even) {
      background: rgba(255, 255, 255, 0.18);
    }

    input, button {
      width: 100%;
      padding: 14px;
      margin-top: 8px;
      border-radius: 12px;
      border: none;
      box-sizing: border-box;
      font-size: 1em;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    input {
      background: rgba(255, 255, 255, 0.15);
      color: #e6e6ff;
      box-shadow: inset 0 2px 5px rgba(0, 0, 0, 0.3);
    }

    input::placeholder {
      color: rgba(230, 230, 255, 0.7);
      opacity: 1;
    }

    input:focus {
      outline: none;
      transform: scale(1.02);
      box-shadow: 0 0 10px rgba(179, 0, 255, 0.6);
    }

    button {
      background: linear-gradient(45deg, #c0c0c0, #b300ff);
      color: white;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s ease, transform 0.2s ease;
    }

    button:hover {
      background: linear-gradient(45deg, #a8a8a8, #9900e6);
      transform: scale(1.05);
    }

    .success, .error {
      margin-top: 15px;
      font-weight: bold;
      text-align: center;
      font-size: 1.1em;
      padding: 12px;
      border-radius: 10px;
      opacity: 1;
      transition: opacity 0.5s ease;
    }

    .success {
      color: #00ff85;
      background: rgba(0, 255, 133, 0.25);
    }

    .error {
      color: #b300ff;
      background: rgba(179, 0, 255, 0.25);
    }

    .link-container {
      margin-top: 20px;
      text-align: center;
    }

    .link-message {
      color: #e6e6ff;
      font-size: 1em;
      margin-bottom: 15px;
      font-style: italic;
      background: rgba(179, 0, 255, 0.25);
      border: 2px solid #b300ff;
      padding: 15px;
      border-radius: 12px;
      text-align: left;
    }

    .link-high, .link-low {
      padding: 15px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
      margin-bottom: 12px;
    }

    .link-high {
      background: linear-gradient(45deg, rgba(179, 0, 255, 0.25), rgba(139, 0, 204, 0.25));
    }

    .link-low {
      background: linear-gradient(45deg, rgba(0, 255, 133, 0.25), rgba(0, 204, 102, 0.25));
    }

    .link-high input, .link-low input {
      width: 100%;
      padding: 12px;
      margin-bottom: 10px;
      background: rgba(255, 255, 255, 0.15);
      color: #e6e6ff;
      font-size: 0.9em;
    }

    .link-high button, .link-low button {
      width: 100%;
      margin: 5px 0;
      font-size: 0.9em;
      background: #25d366;
      color: #fff;
    }

    .link-high button:hover, .link-low button:hover {
      background: #20b35a;
      transform: scale(1.05);
    }

    .show-button {
      width: auto;
      background: linear-gradient(45deg, #c0c0c0, #00ff85);
      padding: 8px 12px;
      font-size: 0.9em;
      border-radius: 10px;
    }

    .show-button:hover {
      background: linear-gradient(45deg, #a8a8a8, #00e07a);
      transform: scale(1.05);
    }

    .photos-container, .phrases-container {
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.5s ease-out;
      margin-top: 15px;
      padding: 15px;
      background: rgba(255, 255, 255, 0.12);
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
    }

    .photos-container.open, .phrases-container.open {
      max-height: 1500px;
    }

    .photos-message, .phrases-message {
      text-align: center;
      color: #e6e6ff;
      font-size: 1em;
      margin: 15px 0;
      font-style: italic;
    }

    .preview-panel, .confirmation-panel, .browser-panel, .support-panel {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 90%;
      max-width: 450px;
      max-height: 80vh;
      box-shadow: 0 15px 40px rgba(0, 0, 0, 0.5);
      border-radius: 20px;
      transition: opacity 0.3s ease, transform 0.3s ease;
      z-index: 1000;
      opacity: 0;
      pointer-events: none;
      backdrop-filter: blur(8px);
      padding: 25px;
      text-align: center;
      overflow-y: auto;
    }

    .preview-panel.open, .confirmation-panel.open, .browser-panel.open, .support-panel.open {
      opacity: 1;
      pointer-events: auto;
      transform: translate(-50%, -50%) scale(1);
    }

    .preview-panel img {
      width: 100%;
      max-height: calc(60vh - 60px);
      object-fit: contain;
      border-radius: 10px;
      margin-top: 10px;
    }

    .preview-panel header, .confirmation-panel header, .browser-panel header, .support-panel header {
      padding: 15px;
      color: white;
      font-size: 1.2em;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-top-left-radius: 20px;
      border-top-right-radius: 20px;
    }

    .preview-panel header button, .confirmation-panel header button, .browser-panel header button, .support-panel header button {
      background: transparent;
      border: none;
      color: white;
      font-size: 1.5em;
      cursor: pointer;
      transition: transform 0.2s ease;
    }

    .preview-panel header button:hover, .confirmation-panel header button:hover, .browser-panel header button:hover, .support-panel header button:hover {
      transform: scale(1.1);
    }

    .confirmation-panel p, .browser-panel p, .support-panel p {
      color: #e6e6ff;
      font-size: 1em;
      margin: 15px 0;
    }

    .confirmation-panel .highlight {
      color: #ffffff;
      font-weight: bold;
    }

    .browser-panel {
      background: linear-gradient(135deg, rgba(0, 51, 102, 0.95), rgba(51, 0, 102, 0.95));
      border: 2px solid #00ff85;
    }

    .browser-panel header {
      background: linear-gradient(45deg, #00ff85, #b300ff);
    }

    .browser-panel .browser-message {
      color: #e6e6ff;
      font-size: 1.1em;
      margin-bottom: 20px;
    }

    .browser-panel .browser-logos {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }

    .browser-panel .browser-logos img {
      width: 60px;
      height: 60px;
      border-radius: 10px;
    }

    .support-panel {
      background: linear-gradient(135deg, rgba(101, 10, 147, 0.95), rgba(50, 5, 73, 0.95));
      border: 2px solid #650A93;
    }

    .support-panel header {
      background: linear-gradient(45deg, #650A93, #A55DC7);
    }

    .support-panel .support-message {
      color: #e6e6ff;
      font-size: 1.1em;
      margin-bottom: 25px;
      font-weight: 600;
    }

    .support-panel .payment-option {
      margin-bottom: 25px;
      padding: 20px;
      border-radius: 15px;
      background: linear-gradient(45deg, rgba(255, 255, 255, 0.15), rgba(255, 255, 255, 0.05));
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
      transition: transform 0.2s ease;
    }

    .support-panel .payment-option:hover {
      transform: scale(1.02);
    }

    .support-panel .payment-option h3 {
      color: #ffffff;
      font-size: 1.2em;
      margin-bottom: 12px;
      text-shadow: 0 1px 3px rgba(0, 0, 0, 0.5);
    }

    .support-panel .payment-option .logo-container {
      display: flex;
      justify-content: center;
      margin-top: 15px;
    }

    .support-panel .payment-option .logo-container img {
      width: 140px;
      height: auto;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

    .support-panel button {
      background: linear-gradient(45deg, #650A93, #A55DC7);
      margin-top: 10px;
      font-size: 1.1em;
      padding: 15px;
      border-radius: 15px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
      transition: background 0.3s ease, transform 0.2s ease;
    }

    .support-panel button:hover {
      background: linear-gradient(45deg, #A55DC7, #650A93);
      transform: scale(1.05);
    }

    @media (max-width: 600px) {
      .form-container {
        padding: 25px;
        width: 100%;
      }

      h2 {
        font-size: 1.7em;
      }

      .intro-message, .section-title {
        font-size: 1em;
      }

      input, button {
        font-size: 0.9em;
        padding: 12px;
      }

      .show-button {
        padding: 6px 10px;
        font-size: 0.8em;
      }

      .link-high button, .link-low button {
        width: 100%;
        margin: 5px 0;
      }

      .preview-panel, .confirmation-panel, .browser-panel, .support-panel {
        width: 95%;
        max-height: 85vh;
        padding: 20px;
      }

      .watermark {
        font-size: 1em;
      }

      .photos-container.open, .phrases-container.open {
        max-height: 3000px;
      }

      .browser-panel .browser-logos {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
</head>
<body>
  <div class="browser-panel" id="browserPanel">
    <header>
      Aviso Importante <button onclick=
      "cerrarBrowserPanel()">×</button>
    </header>
    <p class="browser-message">⚠️ <b>Aviso:</b> Si estás abriendo
    este enlace desde el navegador de TikTok en tu celular, y si
    note deja subir tus fotos. Para solucionar eso, abre este
    enlace en otro navegador como <b>Google Chrome</b>,
    <b>Microsoft Edge</b> u otros...</p>
    <div class="browser-logos"><img src=
    "https://www.google.com/chrome/static/images/chrome-logo.svg"
    alt="Chrome Logo"> <img src=
    "https://www.microsoft.com/edge/static/images/edge-logo.svg"
    alt="Edge Logo"></div>
  </div>
  <div class="support-panel" id="supportPanel">
    <header>
      Apoyo al Creador <button onclick=
      "cerrarSupportPanel()">×</button>
    </header>
    <p class="support-message">Estos proyectos son totalmente
    gratis, no tiene anuncios y no cobro por pasarte el link o el
    código, todo te lo doy sin costo 🙌. Pero si valoras el
    esfuerzo, puedes apoyar al creador con una donación voluntaria
    (no es obligatorio, pero se agradece mucho el gesto).</p>
    <div class="payment-option">
      <h3>Si eres de Perú 🇵🇪 - Usa Yape</h3><button onclick=
      "abrirYapeImage()">Invitar dulce con Yape</button>
      <div class="logo-container"><img src=
      "https://upload.wikimedia.org/wikipedia/commons/0/08/Icono_de_la_aplicaci%C3%B3n_Yape.png"
      alt="Yape Logo"></div>
    </div>
    <div class="payment-option">
      <h3>Para donaciones internacionales - Usa
      PayPal</h3><button onclick="abrirPayPal()">Donar con
      PayPal</button>
      <div class="logo-container"><img src=
      "https://upload.wikimedia.org/wikipedia/commons/b/b5/PayPal.svg"
      alt="PayPal Logo"></div>
    </div>
  </div>
  <div class="form-container">
    <h2>🌌 Personalización del Universo V2.5</h2>
    <p class="intro-message">Crea tu propio universo con frases y
    fotos que orbitarán tu planeta. ¡Usa los botones para explorar
    las opciones!</p>
    <div class="input-container">
      <div style="flex: 1;">
        <label>🆔 Crear tu ID:</label> <input type="text" id=
        "usuario" placeholder="Ej: ➪𝐁𝐞𝐫𝐌𝐚𝐭_𝐌𝐨𝐝𝐬𖤍">
      </div><button class="show-button" onclick=
      "mostrarGuia('usuario')">Guía</button>
    </div>
    <div class="input-container">
      <div style="flex: 1;">
        <label>🌍 Nombre en el Planeta:</label> <input type="text"
        id="nombrePlaneta" placeholder="Ej: ➪𝐁𝐞𝐫𝐌𝐚𝐭_𝐌𝐨𝐝𝐬𖤍">
      </div><button class="show-button" onclick=
      "mostrarGuia('nombrePlaneta')">Guía</button>
    </div>
    <div class="section-title">
      🌟 Frases Girando
    </div>
    <div class="button-container">
      <button onclick="togglePhrasesContainer()">Desplegar
      Frases</button> <button class="show-button" onclick=
      "mostrarGuia('fraseGirando')">Guía</button>
    </div>
    <div class="phrases-container" id="phrasesContainer">
      <div class="phrases-message">
        Solo necesitas una frase, ¡pero puedes agregar hasta 5!
      </div><label>🌟 Frase o Palabra Girando 1:</label>
      <input type="text" id="fraseGirando1" placeholder=
      "Ej: Te amo"> <label>🌟 Frase o Palabra Girando 2:</label>
      <input type="text" id="fraseGirando2" placeholder=
      "Ej: Siempre juntos"> <label>🌟 Frase o Palabra Girando
      3:</label> <input type="text" id="fraseGirando3" placeholder=
      "Ej: Mi amor"> <label>🌟 Frase o Palabra Girando 4:</label>
      <input type="text" id="fraseGirando4" placeholder=
      "Ej: Eres mi todo"> <label>🌟 Frase o Palabra Girando
      5:</label> <input type="text" id="fraseGirando5" placeholder=
      "Ej: Para siempre">
    </div>
    <div class="section-title">
      📸 Fotos Girando
    </div>
    <div class="button-container">
      <button onclick="togglePhotosContainer()">Desplegar
      Fotos</button> <button class="show-button" onclick=
      "mostrarGuia('fotoGirando')">Guía</button>
    </div>
    <div class="phrases-container" id="photosContainer">
      <div class="phrases-message">
        Solo necesitas una foto, ¡pero puedes agregar hasta 10!
      </div><label>📸 Foto para Girar 1:</label> <input type="file"
      id="fotoGirando1" accept="image/*"> <label>📸 Foto para Girar
      2:</label> <input type="file" id="fotoGirando2" accept=
      "image/*"> <label>📸 Foto para Girar 3:</label> <input type=
      "file" id="fotoGirando3" accept="image/*"> <label>📸 Foto para
      Girar 4:</label> <input type="file" id="fotoGirando4" accept=
      "image/*"> <label>📸 Foto para Girar 5:</label> <input type=
      "file" id="fotoGirando5" accept="image/*"> <label>📸 Foto para
      Girar 6:</label> <input type="file" id="fotoGirando6" accept=
      "image/*"> <label>📸 Foto para Girar 7:</label> <input type=
      "file" id="fotoGirando7" accept="image/*"> <label>📸 Foto para
      Girar 8:</label> <input type="file" id="fotoGirando8" accept=
      "image/*"> <label>📸 Foto para Girar 9:</label> <input type=
      "file" id="fotoGirando9" accept="image/*"> <label>📸 Foto para
      Girar 10:</label> <input type="file" id="fotoGirando10"
      accept="image/*">
    </div>
    <div class="input-container">
      <div style="flex: 1;">
        <label>💫 Foto de la Estrella Fugaz:</label>
      </div><button class="show-button" onclick=
      "mostrarGuia('estrellaFugaz')">Guía</button>
    </div><input type="file" id="estrellaFugaz" accept="image/*">
    <button onclick="guardarInformacion()">Guardar
    Información</button> <button onclick=
    "abrirSupportPanel()">Apoyar al creador</button>
    <div id="mensaje"></div>
    <div class="link-container" id="linkContainer" style=
    "display: none;">
      <div class="link-message">
        ⚠️ <b>Aviso Importante:</b><br>
        <br>
        👉 <b>Elige el enlace según tu dispositivo:</b><br>
        <br>
        💻 <b>PC / Celulares de Gama Alta</b><br>
        <div class="link-high">
          <input type="text" id="linkGeneradoHigh" readonly>
          <button onclick="compartirWhatsapp('high')">💬 Compartir
          WhatsApp (💻 PC / 🔝 Gama Alta)</button>
        </div><br>
        📱 <b>Celulares de Gama Baja</b><br>
        <div class="link-low">
          <input type="text" id="linkGeneradoLow" readonly>
          <button onclick="compartirWhatsapp('low')">💬 Compartir
          WhatsApp (📱 Gama Baja)</button>
        </div>
      </div>
    </div>
  </div>
  <div class="preview-panel" id="previewPanel">
  <header>
    Guía de la plantilla <button onclick="cerrarPanel()">×</button>
  </header><img id="previewImage" src="" alt=
  "Guía de la plantilla"></div>
  <div class="confirmation-panel" id="confirmationPanel">
    <header>
      Información Guardada <button onclick=
      "cerrarConfirmationPanel()">×</button>
    </header>
    <p id="confirmationMessage"></p>
  </div>
  <div class="watermark">
    Sígueme en TikTok: @bermat_mods
  </div>
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

   
    window.onload = function() {
      document.getElementById("browserPanel").classList.add("open");
    };


    window.togglePhotosContainer = function() {
      const photosContainer = document.getElementById("photosContainer");
      photosContainer.classList.toggle("open");
    };

    window.togglePhrasesContainer = function() {
      const phrasesContainer = document.getElementById("phrasesContainer");
      phrasesContainer.classList.toggle("open");
    };

    window.guardarInformacion = async function() {
      const usuario = document.getElementById("usuario").value.trim().toLowerCase();
      const nombrePlaneta = document.getElementById("nombrePlaneta").value.trim();
      const estrellaFugazInput = document.getElementById("estrellaFugaz");
      const frasesGirandoInputs = [
        document.getElementById("fraseGirando1"),
        document.getElementById("fraseGirando2"),
        document.getElementById("fraseGirando3"),
        document.getElementById("fraseGirando4"),
        document.getElementById("fraseGirando5")
      ];
      const fotosGirandoInputs = [
        document.getElementById("fotoGirando1"),
        document.getElementById("fotoGirando2"),
        document.getElementById("fotoGirando3"),
        document.getElementById("fotoGirando4"),
        document.getElementById("fotoGirando5"),
        document.getElementById("fotoGirando6"),
        document.getElementById("fotoGirando7"),
        document.getElementById("fotoGirando8"),
        document.getElementById("fotoGirando9"),
        document.getElementById("fotoGirando10")
      ];
      const mensaje = document.getElementById("mensaje");
      const linkContainer = document.getElementById("linkContainer");
      const linkGeneradoHigh = document.getElementById("linkGeneradoHigh");
      const linkGeneradoLow = document.getElementById("linkGeneradoLow");
      const confirmationPanel = document.getElementById("confirmationPanel");
      const confirmationMessage = document.getElementById("confirmationMessage");

   
   
      let errores = [];
      if (!usuario) errores.push("ID");
      if (!nombrePlaneta) errores.push("Nombre en el Planeta");
      if (!estrellaFugazInput.files[0]) errores.push("Foto de la Estrella Fugaz");

      const frasesCargadas = frasesGirandoInputs.filter(input => input.value.trim());
      if (frasesCargadas.length === 0) errores.push("al menos una Frase o Palabra Girando");

      const fotosCargadas = fotosGirandoInputs.filter(input => input.files[0]);
      if (fotosCargadas.length === 0) errores.push("al menos una Foto para Girar");

      if (errores.length > 0) {
        mensaje.innerHTML = `<div class="error">❌ Por favor completa los siguientes campos: ${errores.join(", ")}. Tu información se guardará solo por 8 horas y luego se eliminará para mayor privacidad.</div>`;
        setTimeout(() => {
          mensaje.style.opacity = '0';
        }, 5000);
        mensaje.style.opacity = '1';
        return;
      }

      mensaje.innerHTML = "<div class='success'>⏳ Verificando usuario...</div>";
      mensaje.style.opacity = '1';

      try {
        const snapshot = await get(ref(database, "usuarios/" + usuario));
        if (snapshot.exists()) {
          mensaje.innerHTML = "<div class='error'>❌ El nombre de usuario ya está en uso. Elige otro. Tu información se guardará solo por 8 horas y luego se eliminará para mayor privacidad.</div>";
          setTimeout(() => {
            mensaje.style.opacity = '0';
          }, 5000);
          mensaje.style.opacity = '1';
          return;
        }

        mensaje.innerHTML = "<div class='success'>⏳ Comprimiendo y guardando imágenes...</div>";

        const fotosGirando = [];
        for (let input of fotosCargadas) {
          const imagen = await comprimirImagen(input.files[0]);
          fotosGirando.push(imagen);
        }

        const estrellaFugaz = await comprimirImagen(estrellaFugazInput.files[0]);

        const frasesGirando = frasesCargadas.map(input => input.value.trim());

        const datos = {
          nombrePlaneta,
          frasesGirando,
          fotosGirando,
          estrellaFugaz,
          timestamp: Date.now()
        };
        await set(ref(database, "usuarios/" + usuario), datos);

        confirmationMessage.innerHTML = `✅ ¡Información guardada exitosamente!<br>Tu ID es: <span class="highlight">${usuario}</span><br>Tu ling ya se genero correctamente, ya puedes compartirlo atu pareja o amiga ...<br><small>Tu información se guardará solo por 8 horas y luego se eliminará para mayor privacidad.</small>`;
        confirmationPanel.classList.add("open");

        
        const linkHigh = `https://bermatmods.github.io/Espacio-BerMat/?id=${usuario}`;
        const linkLow = `https://bermatmods.github.io/Espacio-BerMat-movil-/?id=${usuario}`;
        linkGeneradoHigh.value = linkHigh;
        linkGeneradoLow.value = linkLow;
        linkContainer.style.display = "block";

        setTimeout(async () => {
          try {
            await set(ref(database, "usuarios/" + usuario), null);
            console.log(`Datos del usuario ${usuario} eliminados después de 8 horas.`);
          } catch (error) {
            console.error("Error al eliminar datos:", error);
          }
        }, 28800000);

      } catch (error) {
        console.error("Error al guardar:", error);
        mensaje.innerHTML = "<div class='error'>❌ Error al guardar: " + error.message + ". Por favor, intenta de nuevo. Tu información se guardará solo por 8 horas y luego se eliminará para mayor privacidad.</div>";
        setTimeout(() => {
          mensaje.style.opacity = '0';
        }, 5000);
        mensaje.style.opacity = '1';
      }
    };

    async function comprimirImagen(file) {
      return new Promise((resolve, reject) => {
        const reader = new FileReader();
        reader.onload = function (event) {
          const img = new Image();
          img.src = event.target.result;
          img.onload = function () {
            const canvas = document.createElement("canvas");
            const ctx = canvas.getContext("2d");
            const maxWidth = 800;
            const maxHeight = 800;
            let width = img.width;
            let height = img.height;

            if (width > height) {
              if (width > maxWidth) {
                height = Math.round((height * maxWidth) / width);
                width = maxWidth;
              }
            } else {
              if (height > maxHeight) {
                width = Math.round((width * maxHeight) / height);
                height = maxHeight;
              }
            }

            canvas.width = width;
            canvas.height = height;
            ctx.drawImage(img, 0, 0, width, height);

            const dataUrl = canvas.toDataURL("image/jpeg", 0.7);
            resolve(dataUrl);
          };
          img.onerror = reject;
        };
        reader.onerror = reject;
        reader.readAsDataURL(file);
      });
    }

    window.compartirWhatsapp = function(type) {
      const link = type === 'high' 
        ? document.getElementById("linkGeneradoHigh").value 
        : document.getElementById("linkGeneradoLow").value;

      const usuario = document.getElementById("usuario").value.trim().toLowerCase();

      const texto = 
  `
  ━━━━━━━━━━━━━━━━━━━
  ✨ Mira el universo que preparé para ti ✨
  🔗 Enlace: ${link}  


  `;

      const whatsappURL = `https://wa.me/?text=${encodeURIComponent(texto)}`;
      window.open(whatsappURL, "_blank");
    };

    window.mostrarGuia = function(campo) {
      const previewPanel = document.getElementById("previewPanel");
      const previewImage = document.getElementById("previewImage");
      let imagenSrc = '';

      switch (campo) {
        case 'usuario':
          imagenSrc = 'img/1.jpg';
          break;
        case 'nombrePlaneta':
          imagenSrc = 'img/2.jpg';
          break;
        case 'fraseGirando':
          imagenSrc = 'img/3.jpg';
          break;
        case 'fotoGirando':
          imagenSrc = 'img/4.jpg';
          break;
        case 'estrellaFugaz':
          imagenSrc = 'img/5.jpg';
          break;
      }

      previewImage.src = imagenSrc;
      previewPanel.classList.add("open");
    };

    window.cerrarPanel = function() {
      document.getElementById("previewPanel").classList.remove("open");
    };

    window.cerrarConfirmationPanel = function() {
      document.getElementById("confirmationPanel").classList.remove("open");
    };

    window.cerrarBrowserPanel = function() {
      document.getElementById("browserPanel").classList.remove("open");
      document.getElementById("supportPanel").classList.add("open");
    };

    window.cerrarSupportPanel = function() {
      document.getElementById("supportPanel").classList.remove("open");
    };

    window.abrirSupportPanel = function() {
      document.getElementById("supportPanel").classList.add("open");
    };

    window.abrirYapeImage = function() {
      window.open('img/yape.jpg', '_blank');
    };

    window.abrirPayPal = function() {
      window.open('https://paypal.me/tonyhxp', '_blank');
    };
  </script>
</body>
</html>
