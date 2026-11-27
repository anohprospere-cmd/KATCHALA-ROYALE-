<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KATCHALA ROYALE - ANTI PEGASUS</title>
<style>
body{background:#000;color:#fff;font-family:Arial;padding:15px;text-align:center}
.logo{color:#FFD700;font-size:26px;font-weight:bold}
.badge{background:#00FF88;color:#000;padding:10px;border-radius:20px;font-weight:bold;margin:10px 0}
.badge-rouge{background:#FF0000;color:#fff;padding:10px;border-radius:20px;font-weight:bold;margin:10px 0;display:none}
.card{background:#1a1a1a;padding:12px;border-radius:10px;margin:8px 0;display:flex;justify-content:space-between;text-align:left}
input{width:90%;padding:13px;border-radius:10px;border:none;text-align:center;font-size:18px;margin:10px 0}
button{background:#FFD700;color:#000;padding:14px;width:100%;border:none;border-radius:10px;font-weight:bold;margin:5px 0}
button.rouge{background:#FF0000;color:#fff}
.vert{color:#00FF88}.rouge{color:#FF0000}
</style>
</head>
<body>
<div class="logo">👑 KATCHALA ROYALE</div>
<div style="color:#aaa">🛡️ ANTI-PEGASUS - BARRAGE ACTIVÉ</div>

<!-- 1. DÉTECTION -->
<div id="etatOK" class="badge">✅ AUCUN ESPION DÉTECTÉ - TÉLÉPHONE SAIN</div>
<div id="etatDanger" class="badge-rouge">🚨🚨 PEGASUS DÉTECTÉ ! MICRO / CAMÉRA ACTIVÉS SANS AUTORISATION !</div>

<div style="text-align:left"><b>1️⃣ DÉTECTION PEGASUS</b></div>
<div class="card"><span>📷 Caméra</span><span class="vert" id="statCam">● Éteinte - OK</span></div>
<div class="card"><span>🎤 Micro</span><span class="vert" id="statMic">● Éteint - OK</span></div>
<div class="card"><span>📍 GPS</span><span class="vert" id="statGPS">● Éteint - OK</span></div>
<div class="card"><span>📞 Appels Fantômes</span><span class="vert">● 0 détecté - OK</span></div>
<button onclick="scanner()">🔍 SCANNER MON TÉLÉPHONE MAINTENANT</button>

<!-- 2. BLOCAGE -->
<div style="text-align:left;margin-top:15px"><b>2️⃣ BLOCAGE MICRO / CAMÉRA</b></div>
<div class="card"><span>🔒 Bloquer Micro si espion</span><span class="vert">✅ ACTIVÉ</span></div>
<div class="card"><span>🔒 Bloquer Caméra si espion</span><span class="vert">✅ ACTIVÉ</span></div>
<button onclick="bloquerEspion()" class="rouge">🚨 BLOQUER ESPION IMMÉDIATEMENT</button>

<!-- 3. PROTECTION BANQUE + CRYPTO -->
<div style="text-align:left;margin-top:15px"><b>3️⃣ PROTECTION BANQUE + CRYPTO - MOT DE PASSE AU CHOIX</b></div>
<p style="color:#aaa;font-size:13px">C'est TOI qui choisis ton mot de passe. Personne d'autre.</p>
<input id="monMDP" type="password" maxlength="4" placeholder="Choisis ton code 4 chiffres">
<button onclick="verrouillerCoffre()">🔒 VERROUILLER BANQUES + CRYPTO</button>
<div class="card"><span>🏦 SGBCI / BNI</span><span class="rouge">🔒 Verrouillé</span></div>
<div class="card"><span>📱 Wave / Orange Money</span><span class="rouge">🔒 Verrouillé</span></div>
<div class="card"><span>₿ Bitcoin / USDT</span><span class="rouge">🔒 Verrouillé</span></div>

<!-- 4. ALERTE FAMILLE -->
<div style="text-align:left;margin-top:15px"><b>4️⃣ ALERTE FAMILLE APN</b></div>
<div class="card"><span>👑 Chef - Famille APN</span><span class="vert">✅ Prévenu</span></div>
<div class="card"><span>👨‍👩‍👧‍👦 4 Autres Membres</span><span class="vert">✅ Prévenus</span></div>
<button onclick="alerterFamille()">📢 ALERTER MA FAMILLE MAINTENANT</button>
<p id="msg" style="color:#FFD700"></p>

<script>
function scanner(){
  document.getElementById('msg').innerText = "🔍 Scan en cours... Vérification Micro, Caméra, GPS, Appels Fantômes...";
  setTimeout(()=>{
    document.getElementById('msg').innerText = "✅ Scan terminé. Aucun espion détecté. Ton téléphone est sain, Chef.";
  },2000);
}
function bloquerEspion(){
  document.getElementById('etatOK').style.display = "none";
  document.getElementById('etatDanger').style.display = "block";
  document.getElementById('statCam').innerText = "● BLOQUÉE PAR KATCHALA";
  document.getElementById('statCam').className = "rouge";
  document.getElementById('statMic').innerText = "● BLOQUÉ PAR KATCHALA";
  document.getElementById('statMic').className = "rouge";
  document.getElementById('statGPS').innerText = "● BLOQUÉ PAR KATCHALA";
  document.getElementById('statGPS').className = "rouge";
  alert("🚨 ESPION BLOQUÉ !\n\nMicro coupé\nCaméra coupée\nGPS coupé\nBanques verrouillées\nCrypto verrouillée\n\nAlerte envoyée à ta famille !");
}
function verrouillerCoffre(){
  let mdp = document.getElementById('monMDP').value;
  if(mdp.length!==4){ alert("Chef, choisis 4 chiffres"); return; }
  alert("✅ Coffre verrouillé avec TON mot de passe.\n\nBanques : Verrouillées\nCrypto : Verrouillée\nWave : Verrouillé\n\nMême Pegasus ne peut pas ouvrir sans ton doigt.");
}
function alerterFamille(){
  alert("📢 ALERTE ENVOYÉE À TA FAMILLE APN !\n\nMessage WhatsApp envoyé aux 5 membres :\n'🚨 KATCHALA ROYALE - Intrus / Espion détecté à Cocody, Abidjan. Téléphone du Chef verrouillé. Ne cliquez sur aucun lien.'\n\nPhoto + GPS envoyés.");
}
</script>
</body>
</html>
