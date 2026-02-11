<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Valentine's Day Rio ❤️</title>
<style>
    body {
        margin: 0;
        padding: 0;
        background: linear-gradient(135deg, #ff9a9e, #fad0c4);
        font-family: 'Comic Sans MS', cursive, sans-serif;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }

    .card {
        background: white;
        padding: 30px;
        border-radius: 20px;
        box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        text-align: center;
        max-width: 340px;
        animation: fadeIn 2s ease-in-out;
        z-index: 2;
    }

    h1 {
        color: #ff4d6d;
        margin-bottom: 10px;
    }

    p {
        color: #444;
        font-size: 15px;
        line-height: 1.5;
    }

    .heart {
        position: absolute;
        color: #ff4d6d;
        font-size: 20px;
        animation: floatUp 6s linear infinite;
    }

    @keyframes floatUp {
        0% { transform: translateY(100vh) scale(1); opacity: 1; }
        100% { transform: translateY(-10vh) scale(1.5); opacity: 0; }
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: scale(0.8); }
        to { opacity: 1; transform: scale(1); }
    }

    button {
        margin-top: 15px;
        padding: 10px 15px;
        border: none;
        border-radius: 15px;
        background-color: #ff4d6d;
        color: white;
        font-size: 14px;
        cursor: pointer;
    }

    button:hover {
        background-color: #e63956;
    }
</style>
</head>
<body>

<div class="card">
    <h1>Happy Valentine's Day Rio 💖</h1>
    <p>
        I love you so much, much more than I can express. Even though we are so far from each other, 
        I can still see the care you have for me. I want to meet you, hug you tight, and never let go.  
        You are amazing and the most handsome boy. Thank you so much for being a part of my life 😘😘
    </p>
    <button onclick="showLove()">Click for a surprise 💌</button>
</div>

<script>
    function showLove() {
        alert("I love you so much, much more than I can express ❤️");
    }

    function createHeart() {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "❤";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = (Math.random() * 20 + 10) + "px";
        heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 6000);
    }

    setInterval(createHeart, 300);
</script>

</body>
</html>
