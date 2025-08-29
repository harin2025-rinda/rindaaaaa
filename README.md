[index.html.html](https://github.com/user-attachments/files/22035454/index.html.html)
<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>비밀번호 입력 시 사진 표시</title>
  <style>
    body { font-family: Arial, sans-serif; display:flex; justify-content:center; align-items:center; min-height:100vh; background:#f4f4f4; margin:0; }
    .container { background:white; padding:20px; border-radius:10px; box-shadow:0 2px 10px rgba(0,0,0,0.1); max-width:600px; width:100%; text-align:center; }
    input[type="text"] { padding:10px; font-size:16px; border:1px solid #ccc; border-radius:5px; width:70%; }
    button { padding:10px 20px; font-size:16px; border:none; border-radius:5px; background:#007bff; color:white; cursor:pointer; }
    button:hover { background:#0056b3; }
    .hint { font-size:13px; color:#666; margin-top:8px; }
    .error { color:red; display:none; margin-top:10px; }
    .imgBox { display:none; margin-top:20px; }
    .imgBox img { max-width:100%; height:auto; border-radius:10px; }
    .row { display:flex; gap:10px; justify-content:center; align-items:center; flex-wrap:wrap; }
  </style>
</head>
<body>
  <div class="container">
    <h2>🔓 암호입력</h2>
    <form id="pwForm" autocomplete="off">
      <div class="row">
        <input id="pw" type="text" inputmode="latin" placeholder="풀어보세유" aria-label="암호" required />
        <button id="showBtn" type="submit">보기</button>
      </div>
    </form>
    <p class="hint"><code></code></p>
    <p id="err" class="error" role="alert">암호가 올바르지 않습니다.</p>

    <div id="imgBox" class="imgBox" aria-live="polite">
      <img id="secretImg" alt="비밀 이미지" />
    </div>
    <p style="font-size:12px; color:#666; margin-top:20px;"> 젊은제자들 </p>
  </div>

  <script>
    const PASSWORD = "youngnam2025"; // 암호 (보이는 텍스트 입력)
    const IMAGE_URL = "https://i.imgur.com/bh4AeHv.jpeg"; // Imgur 링크

    const form = document.getElementById("pwForm");
    const pwInput = document.getElementById("pw");
    const err = document.getElementById("err");
    const imgBox = document.getElementById("imgBox");
    const secretImg = document.getElementById("secretImg");

    function reveal() {
      err.style.display = "none";
      imgBox.style.display = "block";
      if (!secretImg.getAttribute("src")) {
        secretImg.setAttribute("src", IMAGE_URL);
      }
      // 보기 이후에도 수정 가능하도록 disabled는 제거
    }

    form.addEventListener("submit", (e) => {
      e.preventDefault();
      const value = (pwInput.value || "").trim();
      if (value === PASSWORD) {
        reveal();
      } else {
        err.style.display = "block";
        form.animate([
          { transform: "translateX(0)" },
          { transform: "translateX(-6px)" },
          { transform: "translateX(6px)" },
          { transform: "translateX(0)" }
        ], { duration: 160, iterations: 1 });
        pwInput.focus();
        pwInput.select();
      }
    });

    // 엔터로 제출
    pwInput.addEventListener("keydown", (e) => {
      if (e.key === "Enter") {
        form.requestSubmit();
      }
    });
  </script>
</body>
</html>
