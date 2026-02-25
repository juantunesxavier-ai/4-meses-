# 4-meses-
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>4 Meses 💖</title>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  background: radial-gradient(circle at bottom, #1a0026 0%, #000000 70%);
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  overflow:hidden;
  font-family:Arial, sans-serif;
  text-align:center;
  color:white;
  cursor:pointer;
}

.mensagem{
  position:absolute;
  top:8%;
  width:90%;
  max-width:700px;
  font-size:20px;
  opacity:0;
  transition:1s;
  line-height:1.6;
}

/* 🌸 Flor */
.flower{
  position:relative;
  width:120px;
  height:120px;
  margin-top:120px;
  transition:0.8s;
}

.flower__leaf{
  position:absolute;
  width:60px;
  height:60px;
  background:#ff4da6;
  border-radius:50%;
}

.flower__leaf--1{ top:0; left:30px;}
.flower__leaf--2{ top:30px; left:0;}
.flower__leaf--3{ top:30px; right:0;}
.flower__leaf--4{ bottom:0; left:30px;}

.flower__center{
  position:absolute;
  width:40px;
  height:40px;
  background:white;
  border-radius:50%;
  top:40px;
  left:40px;
}

/* 🌟 Crescer */
.grow{
  animation: growFlower 1.5s forwards;
}

@keyframes growFlower{
  0%{ transform:scale(1); }
  100%{ transform:scale(1.8); }
}

/* 🌫 Sumir */
.hide{
  animation: hideFlower 1s forwards;
}

@keyframes hideFlower{
  0%{ opacity:1; transform:scale(1.8); }
  100%{ opacity:0; transform:scale(0); }
}

.show-message{
  opacity:1;
}

/* 💖 Corações */
.heart{
  position:absolute;
  bottom:50%;
  font-size:20px;
  animation: explode 3s ease-out forwards, brilho 1s infinite alternate;
  filter: drop-shadow(0 0 8px #ff4da6);
}

/* ✨ brilho pulsando */
@keyframes brilho{
  0%{
    filter: drop-shadow(0 0 5px #ff4da6);
  }
  100%{
    filter: drop-shadow(0 0 20px #ff99cc);
  }
}

@keyframes explode{
  0%{
    transform:translate(0,0) scale(1);
    opacity:1;
  }
  100%{
    transform:translate(var(--x), var(--y)) scale(0.5);
    opacity:0;
  }
}
</style>
</head>

<body>

<div class="mensagem">
💖 Feliz 4 meses amor 💖<br><br>

Obrigada por sempre estar ao meu lado,  
me apoiando e me amando.  
Eu espero poder retribuir sempre da melhor forma.  
Eu te amo neném 💗<br><br>

4 meses ao seu lado são os melhores 4 meses da minha vida.  
Ao seu lado tudo é mágico, tudo é único e perfeito.  
Eu te amo muito meu amor.  
Que essa data possa se repetir por muitos meses e anos,  
se Deus nos abençoar — e Ele vai. ❤️<br><br>

Obrigada por tanto, meu amor!  
Espero que goste kkk 😅  
Lembrando que não entendo nada disso,  
é só pra mostrar o quão especial você é pra mim, neném 💞
</div>

<div class="flower" id="flower">
  <div class="flower__leaf flower__leaf--1"></div>
  <div class="flower__leaf flower__leaf--2"></div>
  <div class="flower__leaf flower__leaf--3"></div>
  <div class="flower__leaf flower__leaf--4"></div>
  <div class="flower__center"></div>
</div>

<script>
document.body.addEventListener("click", function(){

  const flower = document.getElementById("flower");
  const mensagem = document.querySelector(".mensagem");

  flower.classList.add("grow");

  setTimeout(() => {
    flower.classList.add("hide");

    // 💥 Explodir em corações
    for(let i=0; i<35; i++){
      let heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "💖";

      let x = (Math.random()*600 - 300) + "px";
      let y = (Math.random()*600 - 300) + "px";

      heart.style.setProperty('--x', x);
      heart.style.setProperty('--y', y);
      heart.style.left = "50%";
      heart.style.top = "50%";

      document.body.appendChild(heart);

      setTimeout(()=>{ heart.remove(); },3000);
    }

  }, 1500);

  setTimeout(() => {
    mensagem.classList.add("show-message");
  }, 2500);

});
</script>

</body>
</html>
