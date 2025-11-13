<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title> https:// windows.ni.34.389992.$%7229.+/×^&</title>
<style>
body {
    margin:0;
    font-family:'Arial',sans-serif;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background: linear-gradient(-45deg, #ff9a9e, #fad0c4, #fbc2eb, #a18cd1);
    background-size:400% 400%;
    animation: gradientBG 20s ease infinite;
}
@keyframes gradientBG {
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
}

/* Login Modal */
#loginModal {
    background: rgba(255,255,255,0.95);
    z-index:5;
    display:flex;
    flex-direction:column;
    align-items:center;
    padding:40px;
    border-radius:25px;
    box-shadow:0 0 30px rgba(0,0,0,0.3);
}

#loginModal input {
    padding:12px;
    margin:10px 0;
    border-radius:10px;
    border:2px solid #ff69b4;
    width:220px;
    text-align:center;
}

#loginModal input::placeholder {
    color:#ff1493;
    font-weight:bold;
}

#loginModal label {
    margin-top:15px;
    padding:12px 25px;
    border-radius:15px;
    background: linear-gradient(45deg,#ff69b4,#ff1493);
    color:white;
    font-weight:bold;
    cursor:pointer;
    transition:0.3s;
}
#loginModal label:hover { transform: scale(1.05); }

/* Buttons Container */
#buttonsContainer {
    display:none;
    flex-direction:column;
    align-items:center;
    gap:15px;
}

.romanticButton {
    padding:15px 30px;
    font-size:1.2em;
    border-radius:15px;
    cursor:pointer;
    border:3px solid;
    background:linear-gradient(135deg,#ffe0f0,#ffb6c1);
    color:#fff;
    box-shadow:0 0 15px rgba(255,255,255,0.6);
    transition:0.3s;
}
.romanticButton:hover { transform:scale(1.1); }

#logoutBtn {
    margin-top:20px;
    padding:10px 25px;
    font-size:1em;
    border-radius:10px;
    cursor:pointer;
    background:#ff4d4d;
    color:white;
    border:none;
}

/* Modal general */
.modal {
    position:fixed;
    top:0; left:0; right:0; bottom:0;
    display:flex;
    justify-content:center;
    align-items:center;
    background: rgba(0,0,0,0.5);
    visibility:hidden;
    opacity:0;
    transition:0.5s;
    z-index:5;
}

.modal.active {
    visibility:visible;
    opacity:1;
}

.modalContent {
    background: linear-gradient(135deg,#ffb6c1,#ff69b4);
    padding:40px;
    border-radius:25px;
    display:flex;
    flex-direction:column;
    align-items:center;
    box-shadow:0 0 30px rgba(255,255,255,0.6);
}

.modalContent input {
    padding:12px;
    margin:10px 0;
    border-radius:10px;
    border:2px solid #fff;
    text-align:center;
}

.modalContent label {
    margin-top:15px;
    padding:12px 25px;
    border-radius:15px;
    background: #ff1493;
    color:white;
    font-weight:bold;
    cursor:pointer;
    margin-bottom:10px;
}

#closeBtn {
    background:#ff69b4;
    color:white;
}

/* BESO Floating */
.besoEmoji {
    font-size:2em;
    position:absolute;
    animation: floatBeso 3s infinite;
}

@keyframes floatBeso {
    0% { transform: translateY(0) scale(1);}
    50% { transform: translateY(-50px) scale(1.2);}
    100% { transform: translateY(0) scale(1);}
}

/* ABRAZO */
#abrazosContainer {
    position:relative;
    width:100%;
    height:100%;
}

.abrazoEmoji {
    font-size:2em;
    position:absolute;
    animation: pulse 2s infinite;
}

@keyframes pulse {
    0%{transform:scale(1);}
    50%{transform:scale(1.2);}
    100%{transform:scale(1);}
}

/* CARTA */
#letter {
    font-size:1.5em;
    background: rgba(255,255,255,0.9);
    padding:20px;
    border-radius:15px;
    text-align:center;
    display:none;
}

/* ROSA */
#rosa {
    font-size:6em;
    display:none;
    opacity:0;
    transition:2s;
}

/* SECRETO SCREEN */
#secretScreen {
    display:none;
    background: linear-gradient(-45deg, #ff9a9e, #fad0c4, #fbc2eb);
    flex-direction:column;
    gap:20px;
    align-items:center;
    justify-content:center;
    position:absolute;
    top:0; left:0; right:0; bottom:0;
}

#secretScreen h1 {
    color:#fff;
    font-size:3em;
    text-align:center;
}

#secretScreen button {
    padding:15px 40px;
    border:none;
    border-radius:15px;
    font-size:1.5em;
    cursor:pointer;
    transition:0.3s;
}

#yesBtn { background:#ff1493; color:#fff; position:relative; }
#noBtn { background:#ff69b4; color:#fff; position:absolute; top:50%; left:50%; transform:translate(-50%,-50%); }
</style>
</head>
<body>

<!-- Login Modal -->
<div id="loginModal">
    <h2>Login Romántico</h2>
    <input type="text" id="username" placeholder="Nombre de usuario">
    <input type="password" id="password" placeholder="Password">
    <label onclick="login()">Entrar 💖</label>
</div>

<!-- Buttons -->
<div id="buttonsContainer">
    <button class="romanticButton" onclick="openBeso()">💋BESO🔥</button>
    <button class="romanticButton" onclick="openAbrazo()">🤗Abrazo💫</button>
    <button class="romanticButton" onclick="openCarta()">💌Carta💖</button>
    <button class="romanticButton" onclick="openRosa()">🌹Rosa💖</button>
    <button class="romanticButton" onclick="openSecret()">⛓️Secreto🔒⛓️</button>
    <label id="logoutBtn" onclick="logout()">Cerrar sesión</label>
</div>

<!-- BESO Modal -->
<div id="besoModal" class="modal">
    <div class="modalContent" id="besoContent">
        <h2>BESOS PARA VOS 💋</h2>
        <label onclick="closeBeso()">Cerrar ❌</label>
    </div>
</div>

<!-- ABRAZO Modal -->
<div id="abrazoModal" class="modal">
    <div class="modalContent" id="abrazoContent">
        <h2>Un gran abrazo para vos 🤗💖</h2>
        <div id="abrazosContainer"></div>
        <label onclick="closeAbrazo()">Cerrar ❌</label>
    </div>
</div>

<!-- CARTA Modal -->
<div id="cartaModal" class="modal">
    <div class="modalContent">
        <div id="letter"></div>
        <label onclick="closeCarta()">Cerrar ❌</label>
    </div>
</div>

<!-- ROSA Modal -->
<div id="rosaModal" class="modal">
    <div class="modalContent">
        <div id="rosa">🌹</div>
        <label onclick="closeRosa()">Cerrar ❌</label>
    </div>
</div>

<!-- Secret Modal -->
<div id="secretModal" class="modal">
    <div class="modalContent">
        <h2>Ingresar Contraseña 💖</h2>
        <input type="password" id="secretPass" placeholder="Contraseña">
        <label onclick="checkSecret()">Aceptar ✅</label>
        <label id="closeBtn" onclick="closeSecret()">Cerrar ❌</label>
    </div>
</div>

<!-- Secret Screen -->
<div id="secretScreen">
    <h1>¿Quieres ser mi novia?</h1>
    <button id="yesBtn">Sí 💖</button>
    <button id="noBtn">No 💔</button>
    <audio id="music" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    </audio>
</div>

<script>
// Login
const messages = [
    "Ups! 😜 Intenta de nuevo",
    "No fue, pero sigue intentándolo 💖",
    "Usuario incorrecto! 😏",
    "Casi, inténtalo otra vez 😍",
    "Error 💔, pero no te rindas!"
];
function login() {
    const user = document.getElementById('username').value;
    const pass = document.getElementById('password').value;
    if(user === 'Jendry' && pass === '1234') {
        document.getElementById('loginModal').style.display='none';
        document.getElementById('buttonsContainer').style.display='flex';
    } else {
        alert(messages[Math.floor(Math.random()*messages.length)]);
    }
}

// Logout
function logout() {
    document.getElementById('loginModal').style.display='flex';
    document.getElementById('buttonsContainer').style.display='none';
    hideAllModals();
    document.getElementById('username').value='';
    document.getElementById('password').value='';
    document.getElementById('music').pause();
}

// Hide all modals
function hideAllModals() {
    const modals = document.querySelectorAll('.modal');
    modals.forEach(m=> m.classList.remove('active'));
    document.getElementById('secretScreen').style.display='none';
    document.getElementById('letter').style.display='none';
    document.getElementById('rosa').style.display='none';
    document.getElementById('abrazosContainer').innerHTML='';
}

// BESO
function openBeso() {
    document.getElementById('besoModal').classList.add('active');
}
function closeBeso() { document.getElementById('besoModal').classList.remove('active'); }

// ABRAZO
function openAbrazo() {
    document.getElementById('abrazoModal').classList.add('active');
    const container = document.getElementById('abrazosContainer');
    for(let i=0;i<15;i++){
        const e = document.createElement('div');
        e.className='abrazoEmoji';
        e.innerText=['💕','♥','🤗'][Math.floor(Math.random()*3)];
        e.style.left=Math.random()*80+'%';
        e.style.top=Math.random()*80+'%';
        container.appendChild(e);
    }
}
function closeAbrazo() { document.getElementById('abrazoModal').classList.remove('active'); }

// CARTA
function openCarta() {
    document.getElementById('cartaModal').classList.add('active');
    const lines = [
        "Hola hermosa 🌸, desde que te conocí por mi primo...",
        "No he dejado de pensar en vos 💖...",
        "Cada día me doy cuenta de lo mucho que te quiero 😘",
        "Con todo mi corazón, David P."
    ];
    const letter = document.getElementById('letter');
    letter.style.display='block';
    letter.innerHTML='';
    let i=0;
    function writeLine() {
        if(i<lines.length){
            let p=document.createElement('p');
            letter.appendChild(p);
            let j=0;
            function typeChar() {
                if(j<lines[i].length){
                    p.innerHTML += lines[i][j];
                    j++;
                    setTimeout(typeChar,50);
                } else { i++; setTimeout(writeLine,500);}
            }
            typeChar();
        }
    }
    writeLine();
}
function closeCarta() { document.getElementById('cartaModal').classList.remove('active'); }

// ROSA
function openRosa() {
    document.getElementById('rosaModal').classList.add('active');
    const rosa = document.getElementById('rosa');
    rosa.style.opacity=0;
    setTimeout(()=>rosa.style.opacity=1,50);
}
function closeRosa() { document.getElementById('rosaModal').classList.remove('active'); }

// SECRETO
function openSecret() { document.getElementById('secretModal').classList.add('active'); }
function closeSecret() { document.getElementById('secretModal').classList.remove('active'); }
function checkSecret() {
    const pass = document.getElementById('secretPass').value;
    if(pass === '1234') {
        closeSecret();
        document.getElementById('buttonsContainer').style.display='none';
        document.getElementById('secretScreen').style.display='flex';
        document.getElementById('music').play();
        randomNoBtn();
    } else {
        alert("Contraseña incorrecta 😘");
    }
}

// Botón No se mueve
function randomNoBtn() {
    const btn = document.getElementById('noBtn');
    btn.onmouseover = function() {
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 50);
        btn.style.left = x+'px';
        btn.style.top = y+'px';
    }
}
</script>
</body>
</html>
