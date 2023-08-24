# projeto

<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500&display=swap"
      rel="stylesheet"
    />
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>DevLinks</title> 
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div id="container">
      <div id="profile">
        <img
          src="./assets/Foto de perfil 1.png"
          alt="Foto de Mayk Brito sorrindo, usando oculos e camisa preta, barba e fundo amarelo"
        />
        <p>João Vitor</p>
      </div>
  
      <div id="switch" onclick="toggleMode()">
        <button>
        </button>
        <span></span>
      </div>
<br>
      <ul>
        <li>
          <a href="https://www.instagram.com/instajao04/" target="_blank">Veja meu Instagram</a>
        </li>

        <li>
          <a
            href="https://www.linkedin.com/in/jo%C3%A3o-vitor-b81846270/"
            target="_blank"
            >Veja meu linkedin</a
          >
        </li>

        <li>
          <a href="https://github.com/jaosousa04" target="_blank"
            >Veja meu GitHub</a
          >
        </li>

        <li>
          <a>Veja meu portifolior</a
          >
        </li>
      </ul>
      <div id="social-links">
        <a href="https://github.com/jaosousa04" target="_blank">
          <ion-icon name="logo-github"></ion-icon>
        </a>

        <a href="https://www.instagram.com/instajao04/" target="_blank">
          <ion-icon name="logo-instagram"></ion-icon>
        </a>

        <a href="https://www.linkedin.com/in/jo%C3%A3o-vitor-sousa-ferreira-b81846270/" target="_blank">
          <ion-icon name="logo-linkedin"></ion-icon>
        </a>
      </div>

      <footer>
        Feito com ♥ </a>
    </div>
    <script
      type="module"
      src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"
    ></script>
    <script
      nomodule
      src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"
    ></script>

    <script src="./assets/script.js"></script>
  </body>
</html>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --text-color: White;
  --bg-url: url(./assets/bg-mobile.jpg);
  --stroke-color: rgba(255, 255, 255, 0.5);
  --surface-color: rgba(255, 255, 255, 0.05);
  --surface-color-hover: rgba(0, 0, 0, 0.02);
  --highlight-color: rgba(255, 255, 255, 0.2);
  --switch-bg-url: url(./assets/moon-star.svg);
}

.light {
  --text-color: black;
  --bg-url: url(./assets/bg-mobile-light.jpg);
  --stroke-color: rgba(0, 0, 0, 0.5);
  --surface-color: rgba(0, 0, 0, 0.05);
  --surface-color-hover: rgba(0, 0, 0, 0.02);
  --highlight-color: rgba(0, 0, 0, 0.1);
  --switch-bg-url: url(./assets/sun.svg);
}

body {
  background: var(--bg-url) no-repeat top center/cover;
}

body * {
  font-family: "Inter", sans-serif;
  color: var(--text-color);
}

#container {
  width: 360px;
  margin: 56px auto 0px;
  padding: 0 24px;
}

#profile {
  text-align: center;
  padding: 24px;
}

#profile img {
  width: 112px;
}

#profile p {
  font-weight: 500;
  line-height: 24px;
  margin-top: 8px;
}

#switch {
  position: relative;
  width: 64px;

  margin: 4px auto;
}

#switch button {
  width: 32px;
  height: 32px;
  background: white var(--switch-bg-url) no-repeat center;
  border: 0;
  border-radius: 50%;

  position: absolute;
  top: 50%;
  left: 0;
  z-index: 1;
  transform: translateY(-50%);
}

.light #switch button {
  right: 0;
  left: initial;s
}

#switch span {
  display: block;
  width: 64px;
  height: 24px;
  background: var(--surface-color);
  border: 1px solid var(--stroke-color);
  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);
  border-radius: 9999px;
}

/* links */
ul {
  list-style: none;
  /* abaixo é como damos espaço entre os botoções */
  display: flex;
  flex-direction: column;
  gap: 16px;
}

ul li a {
  display: flex; /* Cria botão, o display Flex */
  align-items: center;
  justify-content: center;

  padding: 16px 24px;

  background: var(--surface-color);
  border: 1px solid var(--stroke-color);
  border-radius: 8px;

  /* RGBA significa Red - Green - Blue e Alpha(Significa transparencia)
eles vão do 0 a 255, 0 o mais escuro possivel e 255 o mais claro possivel */

  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);

  text-decoration: none;
  font-weight: 500;

  transition: background all 0.2s;
}

/* Abaixo deixa o botão marcado quando passamos o mouse sobre ele */
ul li a:hover {
  background: var(--surface-color-hover);
  border: 1.5px solid var(--text-color);
}

/* Tamanhos e espaço dos icones */
#social-links {
  display: flex;
  justify-content: center;

  padding: 24px 0;

  font-size: 24px;
}

#social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 16px;

  transition: background 0.2s;
  border-radius: 50%;
}

#social-links a:hover {
  background: var(--highlight-color);
}

footer {
  padding: 24px 0;
  text-align: center;
  font-size: 14px;
}

function toggleMode() {
  const html = document.documentElement
  html.classList.toggle("light")

  // pegar a tag img
  const img = document.querySelector("#profile img")

  // substituir a imagem
  if (html.classList.contains("light")) {
    //se tiver sem light mode, adicionar a imagem light
    img.setAttribute("src", "./assets/Foto de perfil 02 1.png")
  } else {
    //se tiver sem light mode, manter a imagem normal
    img.setAttribute("src", "./assets/Foto de perfil 1.png")
  }
}
