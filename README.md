<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="icon" href="./assets/img/logo-site.png">
    <title>Namora comigo?</title>
    <link rel="stylesheet" href="./assets//css/app.css" />
    <script src="./assets/js/app.js" defer></script>
  </head>
  <body>
    <div class="background-1"></div>
    <div class="background-2"></div>
    <div class="background-3">
      <div class="cta">
        <button class="btn" id="yes">
          <span class="btn-text-one">Sim</span>
          <span class="btn-text-two">Eita! 💕</span>
        </button>
        <button class="btn no">
          <span class="btn-text-one">Não</span>
          <span class="btn-text-two">😅</span>
        </button>
      </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
  </body>
</html>

@import url("https://fonts.googleapis.com/css?family=Montserrat&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Montserrat", sans-serif;
  font-weight: bold;
}
:root {
  --main-color: #fd052f;
  --body-color: #020202;
  --text-primary-color: #fff;
  --hover-color: #252323;
}
body {
  display: flex;
  flex-direction: column;
  background-color: var(--body-color);
  height: auto;
  width: 100%;
}
.background-1 {
  height: 100vh;
  width: 100%;
  background: center / cover no-repeat url("../img/background-1.png");
}
.background-2 {
  height: 100vh;
  width: 100%;
  background: center / cover no-repeat url("../img/background-2.png");
  background-attachment: fixed;
}
.background-3 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100%;
  background: center / cover no-repeat url("../img/background-3.png");
}
.cta {
  gap: 20px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.btn {
  width: 140px;
  height: 50px;
  background: linear-gradient(to top, #fd052e53, #fd052e75, #fd052f);
  color: var(--text-primary-color);
  border-radius: 50px;
  border: none;
  outline: none;
  cursor: pointer;
  position: relative;
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5);
  overflow: hidden;
}
.btn span {
  font-size: 1.2rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: top 0.5s;
}
.btn-text-one {
  position: absolute;
  width: 100%;
  top: 50%;
  left: 0;
  transform: translateY(-50%);
}
.btn-text-two {
  position: absolute;
  width: 100%;
  top: 150%;
  left: 0;
  transform: translateY(-50%);
}
.btn:hover {
  background: #fff;
  color: var(--main-color);
}
.btn:hover .btn-text-one {
  top: -100%;
}
.btn:hover .btn-text-two {
  top: 50%;
}
::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar-thumb {
  background-color: var(--main-color);
  border-radius: 20px;
}
::-webkit-scrollbar-track {
  background: transparent;
}
::selection {
  background-color: var(--main-color);

var btn = document.querySelector(".no");
var position = 0;
var isAnimating = false;

btn.addEventListener("click", function() {
    if (!isAnimating) {
        isAnimating = true;
        position = position === 0 ? 150 : 0;
        btn.style.transform = `translate(0px, ${position}px)`;
        btn.style.transition = "all 0.2s ease";

        setTimeout(function() {
            isAnimating = false;
        }, 200);
    }
});

btn.addEventListener("mouseover", function() {
    if (!isAnimating) {
        isAnimating = true;
        position = position === 0 ? 150 : 0;
        btn.style.transform = `translate(0px, ${position}px)`;
        btn.style.transition = "all 0.2s ease";

        setTimeout(function() {
            isAnimating = false;
        }, 200);
    }
});

const sim = document.getElementById('yes');

sim.addEventListener("click", () => {

let timerInterval
Swal.fire({
  title: 'Obrigado 😍',
  html: 'Prometo lhe fazer feliz. 💘',
  timer: 2000,
  timerProgressBar: true,
  didOpen: () => {
    Swal.showLoading()
    const b = Swal.getHtmlContainer().querySelector('b')
    timerInterval = setInterval(() => {
      b.textContent = Swal.getTimerLeft()
    }, 100)
  },
  willClose: () => {
    clearInterval(timerInterval)
  }
}).then((result) => {
  if (result.dismiss === Swal.DismissReason.timer) {
    console.log('I was closed by the timer')
  }
})
});
<!DOCTYPE html>
 <html lang="pt-BR">
 <head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="styles.css">
  <title>Casa comigo?</title>
 </head>
 <header>
  <div class="cabeçalho">
   <h3>Não aceito "não" como resposta 😔</h3>
  </div>
</header>
<body>
  <h1>Você aceita casar comigo?</h1>
  <div class="yes-or-no">
  <button class="yes" onclick="tanks()">Sim :)</button>
  <button class="no" onclick="not()">Não :(</button>
  </div>
</body>
<script src="script.js"></script>
</html>
<!DOCTYPE html>
 <html lang="pt-BR">
 <head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="styles.css">
  <title>Casa comigo?</title>
 </head>
 <header>
  <div class="cabeçalho">
   <h3>Não aceito "não" como resposta 😔</h3>
  </div>
</header>
<body>
  <h1>Você aceita casar comigo?</h1>
  <div class="yes-or-no">
  <button class="yes" onclick="tanks()">Sim :)</button>
  <button class="no" onclick="not()">Não :(</button>
  </div>
</body>
<script src="script.js"></script>
</html>

