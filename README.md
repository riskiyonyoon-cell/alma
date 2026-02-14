<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Alma 🤍</title>

<style>
*{
  box-sizing:border-box;
  font-family:'Poppins',sans-serif;
}

body{
  margin:0;
  height:100vh;
  background:linear-gradient(180deg,#eef6ff,#ffffff);
  display:flex;
  justify-content:center;
  align-items:center;
}

.phone{
  width:360px;
  max-width:95%;
  background:#fff;
  border-radius:26px;
  padding:22px;
  box-shadow:0 20px 40px rgba(0,0,0,.18);
  display:flex;
  flex-direction:column;
  justify-content:space-between;
  animation:fade .8s ease;
}

@keyframes fade{
  from{opacity:0;transform:translateY(12px);}
  to{opacity:1;transform:translateY(0);}
}

h1{
  text-align:center;
  color:#3182ce;
  margin-bottom:12px;
}

#text{
  flex:1;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  font-size:14.5px;
  line-height:1.7;
  color:#2a4365;
  padding:8px;
  transition:opacity .4s ease;
}

img{
  width:100%;
  border-radius:18px;
  margin-top:14px;
  display:none;
  box-shadow:0 12px 25px rgba(0,0,0,.2);
}

.photo-text{
  text-align:center;
  font-size:13px;
  color:#4a6fa5;
  margin-top:6px;
  display:none;
}

button{
  width:100%;
  padding:14px;
  border:none;
  border-radius:14px;
  font-size:15px;
  margin-top:10px;
  cursor:pointer;
}

#next{
  background:#3182ce;
  color:#fff;
}

#dm{
  display:none;
  background:linear-gradient(45deg,#2b6cb0,#63b3ed);
  color:white;
}
</style>
</head>

<body>

<!-- 🎧 MUSIK -->
<audio autoplay loop>
  <source src="https://www.bensound.com/bensound-music/bensound-slowmotion.mp3">
</audio>

<div class="phone">
  <div>
    <h1>🤍 For Alma 🤍</h1>
    <div id="text"></div>

    <!-- FOTO DI AKHIR -->
    <img id="photo" src="https://i.pinimg.com/736x/23/45/dd/2345ddcd59d4b54bef646dd25eadec36.jpg" alt="foto kenangan">
    <div id="photoText" class="photo-text">
      butut tapi satu 🤍
    </div>
  </div>

  <div>
    <button id="next">Lanjut ➜</button>
    <button id="dm" onclick="goDM()">Balas aku 🤍</button>
  </div>
</div>

<script>
const texts=[
  "Hai Alma 🤍",
  "Aku mikir mau mulai dari mana.",
  "Karena kita tuh… banyak banget samanya.",
  "Sama-sama butut.",
  "Sama-sama sial.",
  "Sama-sama sering ketawa di kondisi nggak jelas.",
  "Kamu itu tipe temen yang ngebullynya blak-blakan.",
  "Kadang jahat.",
  "Kadang nusuk.",
  "Kadang bikin aku mikir: ini temen apa musuh 😭",
  "Tapi anehnya…",
  "aku nggak pergi.",
  "Karena kamu lucu.",
  "Dan jujur.",
  "Dan real.",
  "Makasih ya.",
  "Udah temenan sama aku sejauh ini.",
  "butut tapi satu 🤍"
];

let i=0;
const textEl=document.getElementById("text");
const nextBtn=document.getElementById("next");
const photo=document.getElementById("photo");
const photoText=document.getElementById("photoText");
const dmBtn=document.getElementById("dm");

textEl.innerHTML=texts[0];

nextBtn.onclick=()=>{
  i++;
  textEl.style.opacity=0;

  setTimeout(()=>{
    if(i<texts.length){
      textEl.innerHTML=texts[i];
      textEl.style.opacity=1;
    }else{
      nextBtn.style.display="none";
      photo.style.display="block";
      photoText.style.display="block";
      dmBtn.style.display="block";
      textEl.innerHTML="Kalau kamu baca ini sambil ngakak,<br>ya berarti ini kamu 🤍";
      textEl.style.opacity=1;
    }
  },300);
};

function goDM(){
  const msg=encodeURIComponent(
    "aku udah baca 🤍\n" +
    "iya aku jahat dan blak-blakan 😭\n" +
    "makasih udah temenan 🤍"
  );

  window.open(
    "https://www.instagram.com/direct/new/?username=drugstprn&text="+msg,
    "_blank"
  );
}
</script>

</body>
</html>
