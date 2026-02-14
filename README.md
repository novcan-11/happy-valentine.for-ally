<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Happy Valentine Sayang 💖</title>

<style>
body {
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #ff9ecf, #ff4f81);
    font-family: 'Poppins', sans-serif;
    text-align: center;
    overflow: hidden;
    color: white;
}

.container {
    margin-top: 100px;
}

h1 {
    font-size: 40px;
    animation: fadeIn 2s ease-in-out;
}

button {
    background: white;
    color: #ff4f81;
    border: none;
    padding: 20px 40px;
    font-size: 24px;
    border-radius: 50px;
    cursor: pointer;
    margin-top: 30px;
    transition: 0.3s;
}

button:hover {
    transform: scale(1.1);
    background: #ffe6f2;
}

.surat {
    display: none;
    margin-top: 40px;
    font-size: 20px;
    width: 80%;
    margin-left: auto;
    margin-right: auto;
    animation: fadeIn 2s ease-in-out;
}

.heart {
    position: fixed;
    color: white;
    animation: fall 5s linear infinite;
}

@keyframes fall {
    0% { top: -10%; opacity: 1; }
    100% { top: 110%; opacity: 0; }
}

@keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
}
</style>
</head>

<body>

<div class="container">
    <h1>Happy Valentine Sayangku 💖</h1>
    <p>Aku punya sesuatu buat kamu...</p>
    <button onclick="bukaSurat()">💗 Buka Cinta Aku 💗</button>

    <div class="surat" id="surat">
        <p>
        Untuk kamu yang paling aku sayang 💞<br><br>
        Terima kasih sudah hadir dalam hidup aku.<br>
        Kamu itu alasan aku senyum setiap hari 😘<br><br>
        Semoga kita selalu bersama,<br>
        penuh cinta, tawa, dan kebahagiaan 💖<br><br>
        I Love You So Much ❤️
        </p>
    </div>
</div>

<script>
function bukaSurat() {
    document.getElementById("surat").style.display = "block";
    buatHati();
}

function buatHati() {
    setInterval(function() {
        let heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = Math.random() * 30 + 20 + "px";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 5000);
    }, 300);
}
</script>

</body>
</html>
