<div class="mensagem">Obrigado por ter conhecido você</div>

<!-- Música de fundo: Arctic Monkeys - 505 -->
<iframe style="display:none;" src="https://www.youtube.com/embed/qU9mHegkTc4?autoplay=1&loop=1&playlist=qU9mHegkTc4" frameborder="0" allow="autoplay" allowfullscreen></iframe>
body {
  margin: 0;
  background: #fff0f5;
  overflow: hidden;
  height: 100vh;
  position: relative;
  font-family: 'Segoe UI', sans-serif;
}

.mensagem {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 2em;
  color: #d63384;
  font-weight: bold;
  text-shadow: 2px 2px #fff;
  animation: fadeIn 3s ease-in-out;
  z-index: 10;
}

@keyframes fadeIn {
  0% { opacity: 0; transform: translate(-50%, -60%); }
  100% { opacity: 1; transform: translate(-50%, -50%); }
}

.heart, .kitty {
  position: absolute;
  top: 100%;
  animation: float 6s linear infinite;
}

.heart {
  width: 20px;
  height: 20px;
  background-color: red;
  transform: rotate(-45deg);
  opacity: 0.8;
}

.heart::before,
.heart::after {
  content: "";
  width: 20px;
  height: 20px;
  background-color: inherit;
  border-radius: 50%;
  position: absolute;
}

.heart::before {
  top: -10px;
  left: 0;
}

.heart::after {
  left: 10px;
  top: 0;
}

.kitty {
  width: 40px;
  height: 40px;
  background-image: url('https://upload.wikimedia.org/wikipedia/en/0/05/Hello_Kitty_character_portrait.png');
  background-size: contain;
  background-repeat: no-repeat;
}

@keyframes float {
  0% {
    transform: translateY(0) scale(1);
    opacity: 1;
  }
  100% {
    transform: translateY(-120vh) scale(1.5);
    opacity: 0;
  }
}
