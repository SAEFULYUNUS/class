<html lang="en">
  
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons+Sharp" rel="stylesheet" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />
    <title>Pesan Dariku Untukmu &#128157</title>
    <style>@import url(https://fonts.googleapis.com/css?family=Ubuntu); @import url(https://fonts.googleapis.com/css?family=Handlee); * { padding: 0; margin: 0; font-family: "Ubuntu", sans-serif; } body { background: #eed9af; } .copyright { text-decoration: none; position: fixed; bottom: 10px; left: calc(50vw - 85px); width: 170px; display: flex; justify-content: space-around; align-items: center; color: white; z-index: 99; opacity: 0.4; } .bg { position: absolute; height: 100%; width: 100%; background-size: cover; background-position: center; filter: brightness(0.5); } .content { color: white; height: 100%; text-align: center; display: flex; justify-content: center; align-items: center; align-content: center; position: relative; z-index: 2; } .card { background: rgba(0, 0, 0, 0.5); padding: 35px 40px; border-radius: 20px; } .content img.surat { margin: 25px auto; animation: animasi1 1s ease infinite; height: 90px; cursor: pointer; } @keyframes animasi1 { 0% { transform: scale(1.03); } 50% { transform: scale(1); } 100% { transform: scale(1.03); } } @keyframes animasi2 { 0% { transform: translateY(0); } 50% { transform: translateY(5px); } 100% { transform: translateY(0); } } .content2 { position: fixed; z-index: 3; top: 0; height: 100%; width: 100%; background: rgba(0, 0, 0, 0.575); display: none; } .content2 .wa { text-align: center; display: none; } .content2 .wa button { background-image: linear-gradient(to top left, #ff009d, #ff004c); padding: 7px 20px; margin: 50px auto; border-radius: 10px; font-size: 1.1rem; font-weight: 600; color: white; border: 2px solid white; animation: animasi2 1s ease infinite; } .paper { position: relative; width: 80%; max-width: 800px; min-width: 360px; height: 480px; margin: 0 auto; margin-top: 60px; background: #fafafa; border-radius: 10px; box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1); overflow: hidden; } .paper:before { content: ""; position: absolute; top: 0; bottom: 0; left: 0; width: 40px; background: radial-gradient(#575450 6px, transparent 7px) repeat-y; background-size: 30px 30px; border-right: 3px solid #d44147; box-sizing: border-box; } .paper-content { position: absolute; top: 30px; right: 0; bottom: 30px; left: 40px; background: linear-gradient(transparent, transparent 28px, #91d1d3 28px); background-size: 30px 30px; } .paper-content textarea { width: 100%; max-width: 100%; height: 100%; max-height: 100%; line-height: 30px; padding: 0 10px; border: 0; outline: 0; background: transparent; color: rgb(0, 0, 0); font-family: "Handlee", cursive; font-weight: bold; font-size: 17px; box-sizing: border-box; z-index: 1; } </style>
  </head>
  <body>

    <audio autoplay type="audio" loop="" class="audio"></audio>
    <div class="bg"></div>

    <div class="content animate__animated animate__bounceInDown">
      <div class="card">
        <div>
          <h3>Ada pesan buat kamu</h3>
        </div>
        <img onclick="tampil()" class="surat" src="https://subscribe.naisid.repl.co/mail.png" alt="MAIL" />
        <p>Tekan untuk membuka</p>
      </div>
    </div>
    <div class="content2">
      <div class="paper animate__animated animate__bounceIn" id="content2">
        <div class="paper-content">
          <textarea class="pesan" disabled></textarea>
        </div>
      </div>
      <div class="wa animate__animated animate__fadeInUp">
        <button onclick="balasWA()">Balas Pesan</button>
      </div>
    </div>
    <a href="https://jeluga.com/" class="copyright" ><p class="cr"><i class="material-icons-sharp cr-logo"> copyright </i></p> <p class="cpr">Jeluga</p></a >
    <script>
      
      var musik = "Musik satu.mp3";
      var background = "Foto satu.jpg"; 
      var ucapanSurat = "Kalau kamu tanya berapa kali kamu datang ke pikiranku, jujur aja cuma sekali. Sekali tapi nggak pergi-pergi.";
      var pesanWhatsapp = "Bisa aja kamu🤭"

    </script>
    <script>var audio = document.querySelector(".audio"); var bg = document.querySelector(".bg"); var isiSurat = document.querySelector(".pesan"); audio.src = musik; bg.style = "background-image: url('" + background + "')"; function tampil() { document.querySelector(".card").style = "transition: 0.5s all ease;transform: scale(0);opacity: 0;"; audio.play(); setTimeout(typeWriter, 1000); setTimeout(function () { document.querySelector(".content2").style.display = "block"; }, 400); } var i = 0; var speed = 100; isiSurat.value = ""; function typeWriter() { if (i < ucapanSurat.length) { isiSurat.value += ucapanSurat.charAt(i); i++; setTimeout(typeWriter, speed); } else { document.querySelector(".wa").style.display = "block"; } } var content = document.querySelector(".content"); var cpr = document.querySelector(".cpr").innerHTML; if (cpr != "Jeluga") { content.style.display = "none"; }function balasWA(){window.open("https://api.whatsapp.com/send?text=" + pesanWhatsapp, "_blank");}</script>
  </body>
</html>
