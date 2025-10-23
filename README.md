<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Masque Hollow Bleach animé</title>
  <style>
    body {
      background: linear-gradient(135deg, #222, #444);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .mask-container {
      animation: reveal 2s ease-in-out forwards;
      opacity: 0;
      transform: scale(0.7);
    }
    @keyframes reveal {
      0% { opacity: 0; transform: scale(0.7) rotate(-30deg);}
      70% { opacity: 1; transform: scale(1.05) rotate(10deg);}
      100% { opacity: 1; transform: scale(1) rotate(0deg);}
    }
    .hollow-mask {
      width: 280px;
      height: 360px;
      position: relative;
    }
    /* Visage */
    .face {
      background: #fff;
      border-radius: 50% 50% 45% 45% / 60% 60% 80% 80%;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      box-shadow: 0 0 25px 5px #fff8;
      border: 3px solid #222;
      overflow: hidden;
    }
    /* Œil gauche rouge */
    .eye-left {
      position: absolute;
      left: 55px;
      top: 100px;
      width: 65px;
      height: 38px;
      background: #b00;
      border-radius: 50% 60% 60% 50% / 70% 70% 80% 80%;
      box-shadow: 0 0 12px 2px #b008;
      z-index: 2;
      transform: rotate(-9deg);
      animation: eye-blink 4s infinite;
    }
    /* Éclats noirs autour de l’œil */
    .eye-mark {
      position: absolute;
      background: #222;
      border-radius: 60% 40% 40% 60% / 60% 40% 70% 30%;
      opacity: 0.6;
      z-index: 3;
    }
    .eye-mark1 { left: 32px; top: 95px; width: 40px; height: 18px; transform: rotate(-12deg);}
    .eye-mark2 { left: 38px; top: 126px; width: 32px; height: 18px; transform: rotate(-6deg);}
    .eye-mark3 { left: 45px; top: 154px; width: 24px; height: 16px; transform: rotate(4deg);}
    /* Bande rouge centrale */
    .center-stripe {
      position: absolute;
      left: 120px;
      top: 40px;
      width: 45px;
      height: 280px;
      background: repeating-linear-gradient(
        160deg,
        #b00 0 22px,
        #fff 22px 32px
      );
      opacity: 0.7;
      border-radius: 60% 50% 40% 50% / 70% 70% 80% 80%;
      z-index: 2;
      animation: stripe-wave 2.5s infinite alternate;
    }
    @keyframes stripe-wave {
      0% { opacity: 0.8; left: 120px;}
      100% { opacity: 0.55; left: 115px;}
    }
    @keyframes eye-blink {
      0%, 92% { background: #b00; }
      95% { background: #900; }
      98% { background: #fff; }
      100% { background: #b00;}
    }
    /* Fissures rouges */
    .crack {
      position: absolute;
      background: #b00;
      border-radius: 30px;
      opacity: 0.45;
      z-index: 5;
    }
    .crack1 { left: 170px; top: 92px; width: 18px; height: 75px; transform: rotate(-24deg);}
    .crack2 { left: 175px; top: 190px; width: 14px; height: 55px; transform: rotate(-18deg);}
    .crack3 { left: 140px; top: 230px; width: 12px; height: 40px; transform: rotate(-9deg);}
    /* Ombre bas */
    .shadow {
      position: absolute;
      left: 70px;
      bottom: 10px;
      width: 140px;
      height: 40px;
      background: radial-gradient(ellipse at center, #2228 30%, transparent 100%);
      opacity: 0.6;
      z-index: 10;
    }
  </style>
</head>
<body>
  <div class="mask-container">
    <div class="hollow-mask">
      <div class="face"></div>
      <div class="eye-left"></div>
      <div class="eye-mark eye-mark1"></div>
      <div class="eye-mark eye-mark2"></div>
      <div class="eye-mark eye-mark3"></div>
      <div class="center-stripe"></div>
      <div class="crack crack1"></div>
      <div class="crack crack2"></div>
      <div class="crack crack3"></div>
      <div class="shadow"></div>
    </div>
  </div>
</body>
</html># README
