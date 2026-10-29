<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>IBS TRADUCTION V3</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<style>
:root{--bg:#fff;--bg2:#f0f2f5;--card:#fff;--blue:#0866ff;--text:#050505;--border:#dddfe2;--green:#1faa59;}
*{margin:0;padding:0;box-sizing:border-box;font-family:system-ui;}
body{background:var(--bg2);color:var(--text);padding-bottom:75px;}
header.top{background:var(--card);display:flex;align-items:center;justify-content:space-between;padding:6px 10px;position:sticky;top:0;z-index:200;border-bottom:1px solid var(--border);}
.logo{display:flex;align-items:center;gap:8px;}
.logo img{width:42px;height:42px;border-radius:50%;border:2px solid #ffcc00;}
.logo b{font-size:19px;line-height:1;} .logo b span{color:var(--blue);}
.top-btns{display:flex;gap:8px;} .top-btns button{width:38px;height:38px;border-radius:50%;border:none;background:var(--bg2);font-size:18px;cursor:pointer;}
.nav2{background:var(--card);display:flex;justify-content:space-around;padding:5px 0;border-bottom:1px solid var(--border);position:sticky;top:54px;z-index:199;}
.nav2 button{border:none;background:none;font-size:20px;padding:6px 14px;border-radius:10px;position:relative;cursor:pointer;} .nav2 button.active{color:var(--blue);background:var(--bg2);}
.badge{position:absolute;top:-2px;right:2px;background:#e41e3f;color:#fff;font-size:10px;padding:1px 5px;border-radius:10px;font-weight:900;}
.hist{display:flex;gap:8px;padding:8px;background:var(--card);border-bottom:1px solid var(--border);position:sticky;top:92px;z-index:198;}
.hist button{padding:5px 12px;border-radius:20px;border:1px solid var(--border);background:var(--bg2);cursor:pointer;font-weight:700;}
#app{max-width:620px;margin:0 auto;}
.card{background:var(--card);margin:8px;border-radius:10px;padding:12px;box-shadow:0 1px 2px rgba(0,0,0,.1);}
.hidden{display:none!important;}
#create{position:fixed;inset:0;background:#fff;z-index:9999;display:flex;align-items:center;justify-content:center;padding:20px;overflow-y:auto;}
.form{width:100%;max-width:380px;background:var(--card);padding:20px;border-radius:12px;box-shadow:0 10px 30px rgba(0,0,0,.2);}
.input-wrap{position:relative;margin:8px 0;}
.input-wrap input{width:100%;padding:12px 40px 12px 12px;border-radius:8px;border:1px solid var(--border);background:#fff;}
.input-wrap input.visible-pass{background:#fff8e1;border:1.5px solid #ffb300;}
.eye{position:absolute;right:10px;top:50%;transform:translateY(-50%);cursor:pointer;font-size:18px;background:var(--bg2);width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center;}
.btn-blue{background:var(--blue);color:white;border:none;padding:12px;width:100%;border-radius:8px;font-weight:900;cursor:pointer;margin-top:10px;}
.bubble{margin:10px;padding:12px;border-radius:18px;max-width:88%;}
.top-bubble{background:#d6e7ff;} .bottom-bubble{background:#d9f2d0;}
.tag{font-size:10px;background:white;border-radius:20px;padding:3px 8px;display:inline-block;margin-top:6px;border:1px solid #ccc;}
.mic-zone{text-align:center;padding:20px;}
.mic{width:92px;height:92px;border-radius:50%;background:var(--green);border:5px solid white;box-shadow:0 6px 20px rgba(0,0,0,.3);color:white;font-size:38px;display:flex;align-items:center;justify-content:center;margin:0 auto;cursor:pointer;}
.mic.active{background:#ff2d2d;transform:scale(1.1);}
.cover{height:210px;background:#ddd;position:relative;border-radius:12px 12px 0 0;overflow:hidden;cursor:pointer;}
.cover img{width:100%;height:100%;object-fit:cover;}
.prof{width:115px;height:115px;border-radius:50%;border:5px solid var(--card);position:absolute;bottom:-45px;left:15px;object-fit:cover;background:#bbb;cursor:pointer;}
.bottom{position:fixed;bottom:0;left:0;right:0;background:var(--card);border-top:1px solid var(--border);display:flex;justify-content:space-around;padding:8px 0;z-index:300;}
.bottom button{border:none;background:none;font-size:20px;cursor:pointer;display:flex;flex-direction:column;align-items:center;color:var(--text);} .bottom button.active{color:var(--blue);} .bottom small{font-size:9px;font-weight:700;margin-top:2px;}
.langs{display:flex;gap:6px;flex-wrap:wrap;justify-content:center;margin:8px 0;}
.langs select{padding:6px 10px;border-radius:20px;border:1px solid var(--border);background:var(--bg2);font-size:12px;}
</style>
</head>
<body>
<div id="create">
<div class="form">
<h2 style="color:var(--blue);">IBS TRADUCTION</h2>
<p style="font-size:11px;margin:8px 0;color:gray;">Badge bleu auto si 0840981930 ou 10000 abonnés - Mot de passe visible pour ne pas se tromper</p>

<div class="input-wrap"><input id="rName" placeholder="Nom complet"></div>
<div class="input-wrap"><input id="rPhone" placeholder="Numéro ex: 0840981930 - visible" type="text"></div>

<div class="input-wrap">
<input id="rPass" type="text" placeholder="Mot de passe - VISIBLE comme numéro" class="visible-pass">
<span class="eye" onclick="togglePass()">👁️</span>
</div>

<div class="input-wrap">
<input id="rPass2" type="text" placeholder="Confirme mot de passe - VISIBLE" class="visible-pass">
<span class="eye" onclick="togglePass()">👁️</span>
</div>

<p id="passError" style="color:red;font-size:11px;display:none;margin-top:4px;">❌ Les mots de passe ne correspondent pas - vérifie, ils sont visibles</p>
<p style="font-size:10px;color:#666;margin-top:6px;">💡 Le mot de passe est visible pour éviter les erreurs. Clique sur 👁️ pour le cacher.</p>

<button class="btn-blue" onclick="createUser()">Créer et Entrer</button>
</div>
</div>

<header class="top">
<div class="logo"><img src="https://i.pravatar.cc/100?img=12"><b>IBS<br><span>TRADUCTION</span></b></div>
<div class="top-btns">
<button onclick="alert('Nouvelle publication')"><i class="fa fa-plus"></i></button>
<button onclick="show('search')"><i class="fa fa-search"></i></button>
<button onclick="show('menu')"><i class="fa fa-bars"></i></button>
</div>
</header>

<div class="nav2">
<button class="active" onclick="show('home')"><i class="fa fa-house"></i><span class="badge">15+</span></button>
<button onclick="show('friends')"><i class="fa fa-user-group"></i><span class="badge">4</span></button>
<button onclick="show('dual')"><i class="fa fa-comment-dots"></i><span class="badge">5</span></button>
<button onclick="show('videos')"><i class="fa fa-tv"></i><span class="badge">15+</span></button>
<button onclick="show('notif')"><i class="fa fa-bell"></i><span class="badge">15+</span></button>
<button onclick="show('shop')"><i class="fa fa-cart-shopping"></i></button>
</div>

<div class="hist">
<button onclick="back()">🔙 Retour</button>
<button onclick="forward()">Suivant 🔜</button>
<span id="pageName" style="margin-left:auto;font-size:11px;color:gray;">Accueil</span>
</div>

<div id="app" class="hidden">
<div id="home" class="page"><div id="feed"></div></div>

<div id="dual" class="page hidden">
<div class="card">
<b><i class="fa fa-language"></i> Conversation Directe 2 personnes - comme photo</b>
<div class="langs"><select id="fromLang"></select><span>→</span><select id="toLang"></select></div>
<div style="text-align:center;margin:6px;"><span style="background:#e6f4ea;color:#0d652d;padding:5px 12px;border-radius:20px;font-size:12px;font-weight:700;"><i class="fa fa-location-dot"></i> MOI - CONGO</span></div>
<div id="chatDual">
<div class="bubble top-bubble"><div>नमस्ते, आपकी उड़ान किस समय है?</div><div style="margin-top:6px;font-size:13px;">Bonjour, à quelle heure est votre vol ?</div><div class="tag">✨ Hindi / Arabe → Français</div></div>
<div class="bubble bottom-bubble"><div>Mon vol est à 16h40. Je cherche la porte.</div><div class="tag">✨ Français → Lingala</div></div>
</div>
<div class="mic-zone">
<div id="micBtn" class="mic" onclick="startMic()"><i class="fa fa-microphone"></i></div>
<p id="micTxt" style="margin-top:10px;font-weight:800;color:var(--blue);">Appuyez pour parler - Traduction directe 1000 langues</p>
<div style="margin-top:10px;display:flex;gap:8px;justify-content:center;">
<button onclick="playLast('from')" style="padding:6px 10px;border-radius:20px;border:1px solid var(--border);background:var(--bg2);font-size:11px;"><i class="fa fa-volume-high"></i> Original</button>
<button onclick="playLast('to')" style="padding:6px 10px;border-radius:20px;border:1px solid var(--border);background:var(--bg2);font-size:11px;"><i class="fa fa-volume-high"></i> Traduction</button>
</div>
</div>
</div>
</div>

<div id="profil" class="page hidden">
<div class="card" style="padding:0;overflow:hidden;">
<div class="cover" onclick="document.getElementById('coverFile').click()"><img id="coverImg" src="https://picsum.photos/800/350?random=11"><input type="file" id="coverFile" class="hidden" accept="image/*" onchange="setCover(this)"><div style="position:absolute;right:10px;bottom:10px;background:rgba(0,0,0,.6);color:white;padding:6px 10px;border-radius:8px;font-size:12px;"><i class="fa fa-camera"></i> Changer couverture</div></div>
<div style="padding:60px 15px 15px;position:relative;">
<img id="profImg" class="prof" src="https://i.pravatar.cc/150?img=5" onclick="document.getElementById('profFile').click()"><input type="file" id="profFile" class="hidden" accept="image/*" onchange="setProf(this)">
<h2 id="uName">Moi <i id="uBadge" class="fa fa-circle-check" style="color:var(--blue);"></i></h2>
<p id="uBio" style="color:gray;font-size:13px;">Créateur IBS - Bukavu</p>
<button class="btn-blue" style="width:auto;padding:6px 14px;margin-top:8px;" onclick="editBio()">Modifier profil / couverture / bio</button>
</div>
</div>
<div class="card"><p>Badge: <span id="fCount">0</span> abonnés - Bleu si 0840981930 ou 10000</p></div>
</div>

<div id="search" class="page hidden"><div class="card"><h3>Rechercher amis</h3></div></div>
<div id="friends" class="page hidden"><div class="card"><h3>Amis</h3></div></div>
<div id="videos" class="page hidden"><div class="card"><h3>Vidéos</h3></div></div>
<div id="notif" class="page hidden"><div class="card"><h3>Notifications</h3></div></div>
<div id="shop" class="page hidden"><div class="card"><h3>Boutique</h3></div></div>
<div id="gnews" class="page hidden"><div class="card"><h3><i class="fa fa-globe"></i> Actualités Google</h3></div></div>
<div id="menu" class="page hidden"><div class="card"><h3>Menu - Tous cliquables</h3></div></div>
</div>

<div class="bottom" id="bottomBar">
<button class="active" onclick="show('home')"><i class="fa fa-house"></i><small>Actualités</small></button>
<button onclick="show('dual')" style="color:#1a9e3e;"><i class="fa fa-comments"></i><small>Direct 2 Pers</small></button>
<button onclick="show('gnews')"><i class="fa fa-earth-americas"></i><small>Google News</small></button>
<button onclick="show('videos')"><i class="fa fa-circle-play"></i><small>Vidéos</small></button>
<button onclick="show('profil')"><i class="fa fa-user"></i><small>Profil</small></button>
</div>

<script>
const LANGS=[["fr","Français"],["en","English"],["ln","Lingala"],["sw","Swahili"],["ar","Arabe"],["hi","Hindi"],["es","Español"],["pt","Português"],["de","Deutsch"],["zh","中文"],["ja","日本語"],["ru","Русский"]];
function fillLangs(){let f=document.getElementById('fromLang'),t=document.getElementById('toLang');LANGS.forEach(l=>{f.innerHTML+=`<option value="${l[0]}">${l[1]}</option>`;t.innerHTML+=`<option value="${l[0]}">${l[1]}</option>`;});f.value='fr';t.value='ln';}
let user=JSON.parse(localStorage.getItem('ibs_user')||'null');
let followers=parseInt(localStorage.getItem('ibs_followers')||'0');
let stack=['home'],idx=0,last={from:'',to:'',fl:'',tl:''};

function togglePass(){
 let p1=document.getElementById('rPass'),p2=document.getElementById('rPass2');
 let newType = p1.type==='password'?'text':'password';
 p1.type=newType; p2.type=newType;
}

function createUser(){
 let n=document.getElementById('rName').value.trim();
 let ph=document.getElementById('rPhone').value.trim();
 let pw=document.getElementById('rPass').value.trim();
 let pw2=document.getElementById('rPass2').value.trim();
 if(!n||!ph||!pw||!pw2){alert('Remplis tout - tout est visible maintenant');return;}
 if(pw!==pw2){document.getElementById('passError').style.display='block';return;}
 if(pw.length<4){alert('Mot de passe trop court - 4 caractères minimum');return;}
 document.getElementById('passError').style.display='none';
 user={name:n,phone:ph,password:pw,verified:ph==='0840981930'};
 followers=ph==='0840981930'?15000:0;
 localStorage.setItem('ibs_user',JSON.stringify(user));
 localStorage.setItem('ibs_followers',followers);
 init();
}

function init(){
 if(!user) return;
 document.getElementById('create').classList.add('hidden');
 document.getElementById('app').classList.remove('hidden');
 document.getElementById('uName').innerHTML=user.name+' <i class="fa fa-circle-check" style="color:#0866ff;"></i>';
 document.getElementById('fCount').innerText=followers;
 if(user.phone!=='0840981930' && followers<10000) document.getElementById('uBadge').style.display='none';
 document.getElementById('feed').innerHTML=`<div class="card"><div style="display:flex;gap:10px;"><img src="https://i.pravatar.cc/40?u=isaac" style="width:40px;border-radius:50%;"><div><b>ISAAC BABYSON GUY ★</b> <i class="fa fa-circle-check" style="color:var(--blue)"></i><br><small>ADMIN VÉRIFIÉ DIRECT</small></div></div><p style="margin-top:10px;">Bienvenue IBS TRADUCTION 1000+ langues - Logo en haut comme demandé</p></div>`;
 fillLangs();
}
function show(id){document.querySelectorAll('.page').forEach(p=>p.classList.add('hidden'));document.getElementById(id).classList.remove('hidden');if(stack[idx]!==id){stack=stack.slice(0,idx+1);stack.push(id);idx++;}document.getElementById('pageName').innerText=id;}
function showNoHist(id){document.querySelectorAll('.page').forEach(p=>p.classList.add('hidden'));document.getElementById(id).classList.remove('hidden');document.getElementById('pageName').innerText=id;}
function back(){if(idx>0){idx--;showNoHist(stack[idx]);}}
function forward(){if(idx<stack.length-1){idx++;showNoHist(stack[idx]);}}
function setCover(inp){if(inp.files[0]){let r=new FileReader();r.onload=e=>document.getElementById('coverImg').src=e.target.result;r.readAsDataURL(inp.files[0]);}}
function setProf(inp){if(inp.files[0]){let r=new FileReader();r.onload=e=>document.getElementById('profImg').src=e.target.result;r.readAsDataURL(inp.files[0]);}}
function editBio(){let b=prompt('Nouvelle bio:');if(b)document.getElementById('uBio').innerText=b;}
let recog=null,listening=false;
function startMic(){
 let btn=document.getElementById('micBtn'),txt=document.getElementById('micTxt');
 if(!('webkitSpeechRecognition' in window||'SpeechRecognition' in window)){alert('Utilise Chrome');return;}
 if(listening){recog.stop();return;}
 const SR=window.SpeechRecognition||window.webkitSpeechRecognition;recog=new SR();
 let fl=document.getElementById('fromLang').value;recog.lang=fl==='ln'?'fr-FR':fl==='sw'?'sw-KE':fl==='hi'?'hi-IN':fl==='ar'?'ar-SA':fl==='en'?'en-US':'fr-FR';
 recog.onstart=()=>{listening=true;btn.classList.add('active');txt.innerText='Écoute... Parlez maintenant';};
 recog.onend=()=>{listening=false;btn.classList.remove('active');txt.innerText='Appuyez pour parler - Traduction directe';};
 recog.onresult=async(e)=>{
   let text=e.results[0][0].transcript;let tl=document.getElementById('toLang').value;
   try{
     let res=await fetch(`https://api.mymemory.translated.net/get?q=${encodeURIComponent(text)}&langpair=${fl}|${tl}`);
     let data=await res.json();let trad=data.responseData.translatedText||text;
     last={from:text,to:trad,fl:fl,tl:tl};
     let div=document.getElementById('chatDual');div.innerHTML+=`<div class="bubble bottom-bubble"><div><b>${text}</b></div><div>→ ${trad}</div><div class="tag">✨ ${fl} → ${tl} | Direct</div></div>`;
     speak(trad,tl);
   }catch{alert('Capté: '+text);}
 };
 recog.start();
}
function speak(t,lang){let u=new SpeechSynthesisUtterance(t);u.lang=lang==='ln'?'fr-FR':lang==='sw'?'sw-KE':lang==='hi'?'hi-IN':lang==='ar'?'ar-SA':lang==='en'?'en-US':'fr-FR';speechSynthesis.speak(u);}
function playLast(type){if(!last.from){alert('Parle d\'abord');return;}if(type==='from')speak(last.from,last.fl);else speak(last.to,last.tl);}
init();
</script>
</body>
</html>
