
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
    <h2>🔒 암호입력</h2>
    <form id="pwForm" autocomplete="off">
      <div class="row">
        <input id="pw" type="text" inputmode="latin" placeholder="풀어보세유" aria-label="암호" required />
        <button id="showBtn" type="submit">보기</button>
      </div>
    </form>
    <p class="hint"></p>
    <p id="err" class="error" role="alert">암호가 올바르지 않습니다.</p>

    <div id="imgBox" class="imgBox" aria-live="polite">
      <img id="secretImg" alt="비밀 이미지" />
      <p style="font-size:16px; font-weight:bold; margin-bottom:10px;">🙏 기도제목</p>
      <p style="font-size:12px; font-weight:bold; margin-bottom:10px;">
      🌟장찬주🌟<br>
1. 학교 개학이 벌써 다가오는데 두려워말고 주님과 함께 있다는 생각으로 학교 생활하기<br>
2. 어깨가 아픈데 치료와 운동하면서 회복되길<br>
3. 모든 해야할 일을 책임감을 가지며 완수하길<br>
4. 가족의 평안과 화평이 언제나 이어지길<br>

🌟이주원🌟<br>
1. 날마다 주님과 동행하며 주님 부르신 그 곳을 향하여 계속 걸어가기<br>
2. 매일의 삶 속에서 나를 향하신 주님의 뜻과 계획을 알아가기<br>
3. 영남제일선교팀이 하나님 나라를 이뤄가는 성실한 일꾼으로 각자의 삶을 살아내는 것<br>

🌟성은서🌟<br>
1. 개강 후, 매일 아침 일찍 일어나 말씀을 묵상하고 기도하는 습관이 들었으면 좋겠습니다<br>
2. 말씀묵상과 기도할 때 기쁨으로 나라가면 좋겠습니다.<br>
3. 집중하는 것이 어렵습니다(공부,책읽기 할때) 기면증 증상이 치유되길 바랍니다<br>

🌟유하린🌟<br>
1. 요즘 회사에 일이많고 사람때문에 많이 지치는데 내 감정을 잘지키고 내가 성숙해 질 수 있는 계기가 되기를<br>
2. 한해가 끝나가는데 쉬고 싶은 마음리 너무너무 간절합니다. 주님은혜안에서 남은 한해를 잘 마무리하고 내년도 잘 이끌어주시기를<br>
3. 주님 사랑 듬뿍누리는~~한해 보내기를<br>

🌟임도언🌟<br>
1. 선교를 향한 마음과 선교지와 아이들을 위한 마음이 계속 이어질 수 있도록 그곳을 위해 중보하며 살 수 있도록 <br>

🌟김지홍🌟<br>
1. 강철 체력을 주세요.<br>
2. 하는 일 모두 잘되길<br>

🌟이재성🌟<br>
1. 선교 잘 마치게 해 주셔서 감사합니다.<br>
9월부터 시적되는 제자학교, 리더모임도 이끌어 주시고 진행되고 있는 제자훈련도 중도포기자 없이 완주 할수있게 해주세요.<br>
2. 하나님을 더욱 사랑하고 경외하는 자 되기를<br>
3. 영육강건 성령충만하길<br>
4. 선교지와 교회를 위해 중보하는 자 되기를<br>

🌟박준혁🌟<br>
1. 나의 이 순간을 그저 흘러보내며 시간을 보내는 것이 아닌 주님의 마음을 구하며 주님리 기뻐하시는 일꾼이 되기<br>
2. 국내선교 때 받은 은혜들을 가득 안고 살아가기<br>
3. 공동체의 소중함과 감사함을 더욱 더 느끼기<br>

🌟문선민🌟<br>
1. 제자훈련 완주하기<br>
2. 새로운 일즐 앞에서 마음 지키기<br>
3. 서른 시작 잘하게 믿음 잘 다지기<br>

🌟이원준🌟<br>
1. 삶의 우선순위를 하나님께 두기를<br>
2. 이직을 준비하는 모든 과정에 함께하여 주시길<br>
3. 선교의 은혜를 잊지 않고 간직하며 살아낼 수 있기를<br>

🌟이예림🌟<br>
1. 주님이 예비하신 곳(취업)이 제가 가고싶어 하는 곳이 되길, 그 곳에 가기에 준비되어 주님께 감사 올려드리는 자가 되길<br>
2. 남은 마지막 학기(학업), 끝까지 주님께서 허락하신 곳에서 열심히 해나가길<br>
3. 지혜롭고 겸손한 자가 되길<br>

🌟박의진🌟<br>
1. 회사 면접을 이곳 저곳 보고있는 중입니다.<br>
하나님의 인도하심 따라 부르심 있는 곳으로 가길 원합니다.<br>
2. 이사 준비를 하고 있습니다.<br>
이후의 계획도 모두 주님께 맡겨드리기 원합니다.<br>
3. 기도의 사람으로 세워지길 기도합니다.<br>
기도가 필요한 곳, 곳곳에 기도의 씨앗을 뿌릴 수 있은자가 되길 기도합니다.<br>

🌟장성은🌟<br>
1. 하나님만 사랑하게 하시고, 보내신 곳에서 빛의 자녀로 살아가게 하소서<br>
2. 나의 죄와 상처 연약함을 하나님 말씀 앞에서 비춰보며 고침받고 하시고 깨끗한 그릇되길 소망하며 쓰임받게 하소서<br>
3. 캄보디아에서의 시간이 날 향한 하나님의 계획을 발견하고 비전이 구제화되게 하소서<br>
      </p>
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
