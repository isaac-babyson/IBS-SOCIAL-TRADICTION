# IBS-SOCIAL-TRADICTION
<input id="rPass" type="password" placeholder="Mot de passe">
<div style="position:relative;margin:8px 0;">
  <input id="rPhone" placeholder="0840981930" style="width:100%;padding:12px;border-radius:8px;border:1px solid #dddfe2;">
</div>

<div style="position:relative;margin:8px 0;">
  <input id="rPass" type="text" placeholder="Mot de passe visible" style="width:100%;padding:12px 40px 12px 12px;border-radius:8px;border:1px solid #dddfe2;background:#fff8e1;">
  <span onclick="togglePass()" style="position:absolute;right:10px;top:50%;transform:translateY(-50%);cursor:pointer;font-size:18px;">👁️</span>
</div>

<div style="position:relative;margin:8px 0;">
  <input id="rPass2" type="text" placeholder="Confirme mot de passe (visible)" style="width:100%;padding:12px 40px 12px 12px;border-radius:8px;border:1px solid #dddfe2;background:#fff8e1;">
</div>
<p id="passError" style="color:red;font-size:11px;display:none;">Les mots de passe ne correspondent pas</p>
function togglePass(){
  let p1=document.getElementById('rPass');
  let p2=document.getElementById('rPass2');
  let type = p1.type === 'password' ? 'text' : 'password';
  p1.type = type;
  p2.type = type;
}

function createUser(){
 let n=document.getElementById('rName').value.trim();
 let ph=document.getElementById('rPhone').value.trim();
 let pw=document.getElementById('rPass').value.trim();
 let pw2=document.getElementById('rPass2').value.trim();
 
 if(!n||!ph||!pw||!pw2) return alert('Remplis tout les champs');
 
 if(pw !== pw2){
   document.getElementById('passError').style.display='block';
   return alert('Mot de passe différent - regarde bien, il est visible comme le numéro');
 }
 document.getElementById('passError').style.display='none';

 if(pw.length < 4) return alert('Mot de passe trop court - minimum 4 caractères');

 user={name:n,phone:ph,password:pw,verified:ph==='0840981930'};
 followers=ph==='0840981930'?15000:0;
 localStorage.setItem('ibs_user',JSON.stringify(user));
 localStorage.setItem('ibs_followers',followers);
 init();
}
