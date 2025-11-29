<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Question for You ❤️</title>
<style>
  html, body {
    height: 100%;
    margin: 0;
    padding: 0;
    overflow: hidden;
  }
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Arial, sans-serif;
    text-align: center;
    background: #ffe4ec;
    box-sizing: border-box;
  }
  .frame {
    display: inline-block;
    border: 5px solid #ff69b4;
    border-radius: 15px;
    padding: 20px;
    background: white;
  }
  img {
    max-width: 300px;
    max-height: 300px;
    width: auto;
    height: auto;
    transition: all 0.3s ease;
  }
  .btn {
    font-size: 18px;
    padding: 10px 20px;
    margin: 10px;
    cursor: pointer;
    border: none;
    border-radius: 8px;
    transition: 0.3s;
  }
  .yes { background-color: #ff69b4; color: white; }
  .no { background-color: #ccc; }
  .love {
    background-color: red;
    color: white;
    font-size: 30px !important;
    padding: 20px 40px;
  }
  .message-box {
    border: 3px dashed #ff69b4;
    padding: 15px;
    margin-top: 20px;
    font-size: 20px;
    background: #fff0f6;
  }
</style>
</head>
<body>

<div class="frame" id="mainFrame">
  <h1 id="question">คุณรักเค้าไหม? 💖</h1>
  <img id="gif" src="https://media.tenor.com/76BaX0eo304AAAAj/kitty-kitty-heart.gif" alt="cute gif">
  <div id="btnContainer"></div>
</div>

<script>
  const gif = document.getElementById('gif');
  const question = document.getElementById('question');
  const btnContainer = document.getElementById('btnContainer');
  let yesBtnSize = 18;
  let noCount = 0;

  // แก้ตรงนี้เพื่อเปลี่ยนรูปเมื่อกด no
  let gifs = ["https://media.tenor.com/76BaX0eo304AAAAj/kitty-kitty-heart.gif", 
    "https://media1.tenor.com/m/wVAjxnPa81IAAAAd/cat-cat-gif.gif",
    "https://media1.tenor.com/m/f6ts3WWJa-8AAAAC/funny-cats-funny.gif",
    "https://media1.tenor.com/m/kEZzd8WrRpAAAAAC/peach-peach-and-goma.gif",
    "https://media.tenor.com/C35t4Pf5GlgAAAAi/peach-and-goma-cute.gif",
    "https://media1.tenor.com/m/troWhJKIjZsAAAAC/hey-cat.gif"
  ]

  function initButtons() {
    btnContainer.innerHTML = `
      <button class="btn yes" id="yesBtn">Yes 💕</button>
      <button class="btn no" id="noBtn">No 😢</button>
    `;
    const yesBtn = document.getElementById('yesBtn');
    const noBtn = document.getElementById('noBtn');

    yesBtn.addEventListener('click', () => yesClick(yesBtn));
    noBtn.addEventListener('click', () => noClick(yesBtn, noBtn));
  }

  function resetPage() {
    noCount = 0;
    yesBtnSize = 18;
    question.textContent = "รักพี่มั้ยคับ? 💖";
    // แก้ตรงนี้เพื่อเปลี่ยนรูปหน้าแรก
    gif.src = "https://media.tenor.com/76BaX0eo304AAAAj/kitty-kitty-heart.gif";
    initButtons();
  }

  function yesClick(yesBtn) {
    // แก้ตรงนี้เพื่อเปลี่ยนรูปเมื่อกด yes
    gif.src = "https://media.giphy.com/media/3oriO0OEd9QIDdllqo/giphy.gif";
    question.textContent = "เย่ เค้าก็รักเธอเหมือนกัน 💗";
    btnContainer.innerHTML = `<button class="btn" id="homeBtn">Home 🏠</button>`;
    document.getElementById('homeBtn').addEventListener('click', resetPage);
  }

  function noClick(yesBtn, noBtn) {
    yesBtnSize += 10;
    yesBtn.style.fontSize = yesBtnSize + 'px';
    noCount++;
    gif.src = gifs[noCount]
    if (noCount >= 5) {
      noBtn.remove();
      yesBtn.textContent = "Love ❤️";
      yesBtn.classList.add('love');
      yesBtn.onclick = () => {
        // แก้ตรงนี้เพื่อเปลี่ยนรูปเมื่อกด love
        gif.src = "https://media1.tenor.com/m/qR1sGRNmfqsAAAAC/besito-catlove.gif";
        question.innerHTML = `<div class="message-box">รักเหมือนกันนนอิอิ 💞</div>`;
        btnContainer.innerHTML = `<button class="btn" id="homeBtn">Home 🏠</button>`;
        document.getElementById('homeBtn').addEventListener('click', resetPage);
      };
    }
  }

  resetPage();
</script>

</body>
</html>
