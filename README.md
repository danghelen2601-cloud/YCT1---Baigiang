# YCT1-Unit1
Hướng dẫn Trẻ em VN học tiếng Trung qua giáo trình YCT 
[Bai_01_NiHao (1).html](https://github.com/user-attachments/files/29433847/Bai_01_NiHao.1.html)
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bài 1: 你好! (Hello!) - YCT1</title>
<script src="https://cdn.jsdelivr.net/npm/hanzi-writer@3.7.0/dist/hanzi-writer.min.js"></script>
<style>
:root{
  --pink:#FF6FA5;
  --orange:#FFA94D;
  --yellow:#FFD93D;
  --green:#4ECDC4;
  --blue:#5B9BFF;
  --purple:#A06CD5;
  --bg:#FFF8EC;
  --card:#ffffff;
  --ink:#3A2E54;
}
*{box-sizing:border-box;}
body{
  margin:0;
  font-family:'Segoe UI', 'Comic Sans MS', sans-serif;
  background:linear-gradient(180deg,#FFF3D6 0%,#FFF8EC 200px);
  color:var(--ink);
}
.header{
  background:linear-gradient(120deg,var(--pink),var(--purple));
  color:white;
  padding:22px 20px 60px;
  text-align:center;
  border-radius:0 0 40% 40% / 0 0 60px 60px;
  position:relative;
}
.header h1{
  font-size:2.2em;
  margin:0 0 6px;
  text-shadow:2px 2px 0 rgba(0,0,0,.15);
}
.header .hanzi-big{font-size:1.6em;}
.header p{margin:4px 0 0;opacity:.95;}
.teacher-card{
  max-width:480px;
  margin:-38px auto 0;
  background:white;
  color:var(--ink);
  border-radius:18px;
  padding:14px 20px;
  box-shadow:0 8px 22px rgba(160,108,213,.25);
  display:flex;
  align-items:center;
  gap:14px;
  font-size:.92em;
  position:relative;
  z-index:5;
}
.teacher-card .avatar{
  width:52px;height:52px;border-radius:50%;
  background:linear-gradient(135deg,var(--yellow),var(--orange));
  display:flex;align-items:center;justify-content:center;
  font-size:1.6em;flex-shrink:0;
}
.teacher-card b{color:var(--purple);}
.tabs{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
  justify-content:center;
  padding:18px 10px 6px;
  position:sticky;
  top:0;
  background:var(--bg);
  z-index:50;
}
.tab-btn{
  border:none;
  padding:10px 16px;
  border-radius:999px;
  font-weight:700;
  font-size:.9em;
  cursor:pointer;
  background:#fff;
  color:var(--ink);
  box-shadow:0 3px 0 rgba(0,0,0,.08);
  transition:.15s;
}
.tab-btn.active{
  background:var(--green);
  color:white;
  transform:translateY(-2px);
}
.tab-btn:hover{transform:translateY(-2px);}
.panel{display:none;max-width:920px;margin:0 auto;padding:16px 18px 60px;}
.panel.active{display:block;animation:fadein .3s;}
@keyframes fadein{from{opacity:0;transform:translateY(8px);}to{opacity:1;transform:translateY(0);}}
.section-title{
  display:inline-block;
  background:var(--orange);
  color:white;
  padding:6px 18px;
  border-radius:999px;
  font-weight:800;
  margin:18px 0 12px;
}
.card{
  background:var(--card);
  border-radius:18px;
  padding:16px 18px;
  margin-bottom:16px;
  box-shadow:0 4px 16px rgba(0,0,0,.07);
}
.key-sentence{
  background:#FFF1F6;
  border:2px dashed var(--pink);
  border-radius:16px;
  padding:14px 18px;
  margin:10px 0;
  font-size:1.15em;
}
.key-sentence .py{color:#999;font-size:.7em;display:block;}
.vocab-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(150px,1fr));gap:14px;}
.vocab-card{
  background:white;border-radius:16px;padding:14px;text-align:center;
  box-shadow:0 3px 10px rgba(0,0,0,.08);border:2px solid #FFE2EE;
}
.vocab-card .hz{font-size:2.4em;color:var(--purple);font-weight:700;}
.vocab-card .py{color:var(--pink);font-weight:700;}
.vocab-card .mean{font-size:.85em;color:#666;margin:4px 0 8px;}
.btn-mini{
  border:none;border-radius:999px;padding:6px 10px;margin:2px;
  font-size:.78em;font-weight:700;cursor:pointer;color:white;
}
.btn-audio{background:var(--blue);}
.btn-write{background:var(--green);}
.writer-modal{
  display:none;position:fixed;inset:0;background:rgba(0,0,0,.5);
  align-items:center;justify-content:center;z-index:999;
}
.writer-modal.show{display:flex;}
.writer-box{background:white;border-radius:20px;padding:20px;text-align:center;max-width:420px;}
.writer-box svg, .writer-box div#writer-target{margin:10px auto;}
.close-x{float:right;cursor:pointer;font-weight:900;color:var(--pink);font-size:1.3em;}
.numbers-row{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;}
.num-bubble{
  width:62px;height:62px;border-radius:50%;display:flex;flex-direction:column;
  align-items:center;justify-content:center;color:white;font-weight:800;cursor:pointer;
  box-shadow:0 4px 8px rgba(0,0,0,.15);
}
.dialogue-box{display:flex;gap:12px;align-items:flex-start;margin-bottom:14px;}
.bubble{
  background:#EAF7FF;border-radius:14px;padding:10px 14px;position:relative;flex:1;
}
.speaker{
  width:36px;height:36px;border-radius:50%;background:var(--purple);color:white;
  display:flex;align-items:center;justify-content:center;font-weight:800;flex-shrink:0;
}
.game-area{background:#fff;border-radius:18px;padding:16px;box-shadow:0 4px 14px rgba(0,0,0,.07);margin-bottom:18px;}
.match-pairs{display:flex;justify-content:space-between;gap:30px;flex-wrap:wrap;}
.match-col{display:flex;flex-direction:column;gap:10px;}
.match-item{
  background:var(--yellow);border-radius:10px;padding:8px 14px;cursor:pointer;font-weight:700;
  text-align:center;user-select:none;
}
.match-item.selected{outline:3px solid var(--blue);}
.match-item.correct{background:var(--green);color:white;}
.match-item.wrong{background:#ff6b6b;color:white;}
.quiz-q{margin-bottom:20px;padding:14px;background:#FFF7F0;border-radius:14px;}
.quiz-opt{
  display:block;width:100%;text-align:left;background:white;border:2px solid #eee;
  border-radius:10px;padding:10px 14px;margin:6px 0;cursor:pointer;font-size:1em;
}
.quiz-opt.sel{border-color:var(--blue);background:#EAF3FF;}
.quiz-opt.correct{border-color:var(--green);background:#E6FBF6;}
.quiz-opt.wrong{border-color:#ff6b6b;background:#FFEAEA;}
.btn-main{
  background:var(--pink);color:white;border:none;border-radius:999px;
  padding:12px 26px;font-weight:800;font-size:1em;cursor:pointer;box-shadow:0 4px 0 #c94f80;
}
.btn-main:active{transform:translateY(2px);box-shadow:none;}
.score-box{
  background:linear-gradient(120deg,var(--yellow),var(--orange));
  border-radius:18px;padding:18px;text-align:center;font-size:1.2em;font-weight:800;color:white;
  margin:14px 0;display:none;
}
.form-row{display:flex;gap:12px;flex-wrap:wrap;margin-bottom:16px;}
.form-row input{
  flex:1;min-width:160px;padding:10px 14px;border-radius:10px;border:2px solid #FFD0E2;font-size:1em;
}
.exercise-block{background:white;border-radius:16px;padding:16px;margin-bottom:16px;box-shadow:0 3px 10px rgba(0,0,0,.06);}
.exercise-block h4{margin-top:0;color:var(--purple);}
.fill-blank input{
  border:none;border-bottom:3px solid var(--pink);width:70px;text-align:center;font-size:1em;
  background:transparent;
}
.coloring-cell{
  width:40px;height:40px;display:inline-flex;align-items:center;justify-content:center;
  border:2px solid #ddd;border-radius:8px;margin:3px;cursor:pointer;font-weight:700;
}
footer{text-align:center;padding:24px;color:#aa9;font-size:.85em;}
.order-item{
  background:#fff;border:2px solid var(--blue);border-radius:10px;padding:8px 12px;margin:6px 0;
  cursor:grab;font-weight:700;
}
@media(max-width:600px){
  .header h1{font-size:1.6em;}
  .teacher-card{font-size:.8em;}
}
</style>
</head>
<body>

<div class="header">
  <div class="hanzi-big">你好！</div>
  <h1>Bài 1: Hello!</h1>
  <p>YCT1 · Standard Course · Sách giáo khoa & Sách bài tập</p>
</div>

<div class="teacher-card">
  <div class="avatar">👩‍🏫</div>
  <div>
    <b>Teacher Helen</b><br>
    📧 danghelen2601@gmail.com &nbsp;|&nbsp; 💬 Zalo: 0823365755
  </div>
</div>

<div class="tabs" id="tabs">
  <button class="tab-btn active" data-tab="khoidong">🌤️ Khởi động</button>
  <button class="tab-btn" data-tab="tumoi">🔤 Từ mới</button>
  <button class="tab-btn" data-tab="ontap">📝 Ôn tập</button>
  <button class="tab-btn" data-tab="nguphap">📘 Ngữ pháp</button>
  <button class="tab-btn" data-tab="hoithoai">💬 Hội thoại</button>
  <button class="tab-btn" data-tab="games">🎮 Games</button>
  <button class="tab-btn" data-tab="tracnghiem">❓ Trắc nghiệm</button>
  <button class="tab-btn" data-tab="baitap">✏️ Bài tập</button>
  <button class="tab-btn" data-tab="tongket">📊 Tổng kết</button>
</div>

<!-- ===================== KHỞI ĐỘNG ===================== -->
<div class="panel active" id="khoidong">
  <div class="card">
    <div class="section-title">Cùng khám phá!</div>
    <p>Các bạn nhỏ ơi, hôm nay chúng ta sẽ học cách <b>chào hỏi bằng tiếng Trung</b> và đếm số từ 1 đến 10 nhé! 🎉</p>
    <p>Trước khi vào bài, hãy trả lời câu hỏi sau:</p>
    <p style="font-size:1.1em">👉 Khi gặp bạn mới, con thường nói gì để chào? Hãy thử đoán xem tiếng Trung sẽ nói thế nào!</p>
  </div>
  <div class="card">
    <div class="section-title">Khởi động bằng số đếm</div>
    <p>Chạm vào từng số để nghe cách đọc nhé!</p>
    <div class="numbers-row" id="warmupNumbers"></div>
  </div>
  <div class="card">
    <div class="section-title">Trò chơi ngón tay 🖐️</div>
    <p>Giơ đúng số ngón tay theo số được đọc lên — nhờ thầy/cô hoặc bố mẹ kiểm tra giúp con!</p>
  </div>
</div>

<!-- ===================== TỪ MỚI ===================== -->
<div class="panel" id="tumoi">
  <div class="card">
    <div class="section-title">Câu mẫu (Key sentences)</div>
    <div class="key-sentence">
      <span class="py">Nǐ hǎo!</span>
      你好！ <span style="color:#888">— Xin chào!</span>
      <button class="btn-mini btn-audio" onclick="speak('你好')">🔊 Nghe</button>
    </div>
    <div class="key-sentence">
      <span class="py">Zàijiàn!</span>
      再见！ <span style="color:#888">— Tạm biệt!</span>
      <button class="btn-mini btn-audio" onclick="speak('再见')">🔊 Nghe</button>
    </div>
  </div>

  <div class="section-title">Từ vựng</div>
  <div class="vocab-grid" id="vocabGrid"></div>

  <div class="section-title">Số đếm 1-10</div>
  <div class="vocab-grid" id="numberGrid"></div>
</div>

<!-- writer modal -->
<div class="writer-modal" id="writerModal">
  <div class="writer-box">
    <span class="close-x" onclick="closeWriter()">✕</span>
    <h3 id="writerTitle">Xem nét chữ</h3>
    <div id="writer-target" style="display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin:10px auto;"></div>
    <button class="btn-main" onclick="replayWriter()">▶️ Xem lại nét chữ</button>
  </div>
</div>

<!-- ===================== ÔN TẬP ===================== -->
<div class="panel" id="ontap">
  <div class="card">
    <div class="section-title">Tổng hợp kiến thức Bài 1</div>
    <ul style="font-size:1.05em;line-height:1.8">
      <li>你好！(Nǐ hǎo) – Xin chào!</li>
      <li>再见！(Zàijiàn) – Tạm biệt!</li>
      <li>老师好！(Lǎoshī hǎo) – Chào cô/thầy!</li>
      <li>Số đếm: 一 二 三 四 五 六 七 八 九 十 (yī èr sān sì wǔ liù qī bā jiǔ shí)</li>
    </ul>
  </div>
  <div class="card">
    <div class="section-title">Bài hát: 你好 (Nǐ hǎo)</div>
    <p>Nǐ hǎo, nǐ hǎo, nǐ hǎo, nǐ hǎo.<br>你好，你好，你好，你好。<br>
    Nǐ hǎo ma? Nǐ hǎo ma?<br>你好吗？你好吗？<br>
    Wǒ hěn hǎo, zàijiàn. Wǒ hěn hǎo, zàijiàn.<br>我很好，再见。我很好，再见。<br>
    Zàijiàn, zàijiàn.<br>再见，再见。</p>
    <button class="btn-main" onclick="speak('你好，你好，你好，你好。你好吗？你好吗？我很好，再见。我很好，再见。再见，再见。')">🔊 Nghe hát</button>
  </div>
</div>

<!-- ===================== NGỮ PHÁP ===================== -->
<div class="panel" id="nguphap">
  <div class="card">
    <div class="section-title">Cấu trúc chào hỏi</div>
    <p><b>[Đối tượng] + 好 (hǎo)</b> dùng để chào một người cụ thể, lịch sự hơn so với chỉ nói "你好".</p>
    <table style="width:100%;border-collapse:collapse;text-align:left">
      <tr style="background:#FFE9F2"><th style="padding:8px">Cấu trúc</th><th>Ví dụ</th><th>Nghĩa</th></tr>
      <tr><td style="padding:8px">你 + 好</td><td>你好！</td><td>Chào bạn!</td></tr>
      <tr><td style="padding:8px">老师 + 好</td><td>老师好！</td><td>Chào cô/thầy!</td></tr>
    </table>
    <p style="margin-top:14px">👉 Khi nói lời tạm biệt, ta dùng <b>再见 (zàijiàn)</b> cho mọi đối tượng, không cần thêm chủ ngữ phía trước.</p>
  </div>
  <div class="card">
    <div class="section-title">Mẹo nhỏ</div>
    <p>Trong tiếng Trung, danh từ chỉ người + 好 luôn là cách chào trang trọng. Hãy thử thay 老师 bằng tên một người bạn để chào nhé: <i>(tên bạn) + 好!</i></p>
  </div>
</div>

<!-- ===================== HỘI THOẠI ===================== -->
<div class="panel" id="hoithoai">
  <div class="card">
    <div class="section-title">Hội thoại 1: Gặp bạn</div>
    <div class="dialogue-box"><div class="speaker">A</div><div class="bubble">Nǐ hǎo! 你好！ <button class="btn-mini btn-audio" onclick="speak('你好')">🔊</button></div></div>
    <div class="dialogue-box"><div class="speaker">B</div><div class="bubble">Nǐ hǎo! 你好！ <button class="btn-mini btn-audio" onclick="speak('你好')">🔊</button></div></div>
  </div>
  <div class="card">
    <div class="section-title">Hội thoại 2: Gặp cô giáo</div>
    <div class="dialogue-box"><div class="speaker">HS</div><div class="bubble">Lǎoshī hǎo! 老师好！ <button class="btn-mini btn-audio" onclick="speak('老师好')">🔊</button></div></div>
    <div class="dialogue-box"><div class="speaker">GV</div><div class="bubble">Nǐ hǎo! 你好！ <button class="btn-mini btn-audio" onclick="speak('你好')">🔊</button></div></div>
  </div>
  <div class="card">
    <div class="section-title">Hội thoại 3 &amp; 4: Lời tạm biệt</div>
    <div class="dialogue-box"><div class="speaker">A</div><div class="bubble">Zàijiàn! 再见！ <button class="btn-mini btn-audio" onclick="speak('再见')">🔊</button></div></div>
    <div class="dialogue-box"><div class="speaker">B</div><div class="bubble">Zàijiàn! 再见！ <button class="btn-mini btn-audio" onclick="speak('再见')">🔊</button></div></div>
  </div>
  <div class="card">
    <p>🎲 <b>Trò chơi "Truyền hoa":</b> Bắt nhịp trống/nhạc và truyền một vật nhỏ (bông hoa giấy). Khi nhạc dừng, ai đang cầm vật đó sẽ chào bạn bên cạnh theo một trong các hội thoại trên!</p>
  </div>
</div>

<!-- ===================== GAMES ===================== -->
<div class="panel" id="games">
  <div class="game-area">
    <div class="section-title">🎯 Game 1: Nối Pinyin với Hán tự</div>
    <p>Bấm chọn 1 ô bên trái rồi 1 ô bên phải tương ứng.</p>
    <div class="match-pairs">
      <div class="match-col" id="matchLeft"></div>
      <div class="match-col" id="matchRight"></div>
    </div>
    <p id="matchResult" style="font-weight:700;color:var(--green);"></p>
  </div>

  <div class="game-area">
    <div class="section-title">🃏 Game 2: Lật thẻ trí nhớ (Hán tự ↔ Nghĩa)</div>
    <div id="memoryGrid" style="display:grid;grid-template-columns:repeat(4,1fr);gap:8px;max-width:480px;"></div>
    <p id="memoryResult" style="font-weight:700;color:var(--green);"></p>
  </div>
</div>

<!-- ===================== TRẮC NGHIỆM ===================== -->
<div class="panel" id="tracnghiem">
  <div class="card">
    <div class="section-title">Trắc nghiệm nhanh</div>
    <div id="quizArea"></div>
    <button class="btn-main" onclick="submitQuiz()">Nộp trắc nghiệm</button>
    <div class="score-box" id="quizScoreBox"></div>
  </div>
</div>

<!-- ===================== BÀI TẬP ===================== -->
<div class="panel" id="baitap">
  <div class="card">
    <div class="section-title">Thông tin học sinh</div>
    <div class="form-row">
      <input type="text" id="stuName" placeholder="Họ và tên học sinh">
      <input type="text" id="stuClass" placeholder="Lớp">
    </div>
  </div>

  <div class="exercise-block">
    <h4>Câu 1-10 (Theo sách bài tập). Nối số với hình chấm tương ứng</h4>
    <p>一(1) hai(2) ba(3)... Chọn đáp án đúng cho mỗi số:</p>
    <div id="ex1"></div>
  </div>

  <div class="exercise-block">
    <h4>Câu 11. Điền từ thích hợp vào câu chào</h4>
    <p class="fill-blank">_____, 你好。 (Gợi ý: chào bạn cùng lớp tên Mai) → <input type="text" id="fillBlank1" placeholder="Mai"></p>
  </div>

  <div class="exercise-block">
    <h4>Câu 12. Sắp xếp lại hội thoại cho đúng thứ tự</h4>
    <p>Kéo để sắp xếp (hoặc đánh số 1-2 vào ô bên dưới theo đúng trình tự hội thoại "gặp và tạm biệt"):</p>
    <select id="order1"><option value="">-- Chọn câu nói trước --</option><option>你好！</option><option>再见！</option></select>
    <select id="order2"><option value="">-- Chọn câu nói sau --</option><option>你好！</option><option>再见！</option></select>
  </div>

  <div class="exercise-block">
    <h4>Câu 13 (Nâng cao). Chọn cách chào đúng ngữ cảnh</h4>
    <p>Khi gặp cô giáo vào buổi sáng, con nên nói:</p>
    <div id="ex13"></div>
  </div>

  <div class="exercise-block">
    <h4>Câu 14 (Nâng cao). Viết lại số 7 và số 9 bằng chữ Hán</h4>
    <div class="form-row">
      <input type="text" id="hz7" placeholder="Số 7 (chữ Hán)">
      <input type="text" id="hz9" placeholder="Số 9 (chữ Hán)">
    </div>
  </div>

  <button class="btn-main" onclick="gradeHomework()">✅ Chấm điểm bài tập</button>
  <div class="score-box" id="hwScoreBox"></div>

  <div class="card" style="margin-top:18px;">
    <div class="section-title">Nộp bài cho giáo viên</div>
    <p>Sau khi chấm điểm, bấm nút dưới để gửi kết quả tới Teacher Helen.</p>
    <button class="btn-main" id="submitBtn" onclick="submitHomework()">📤 Nộp bài</button>
    <p id="submitMsg" style="color:var(--purple);font-weight:700;"></p>
  </div>
</div>

<!-- ===================== TỔNG KẾT ===================== -->
<div class="panel" id="tongket">
  <div class="card">
    <div class="section-title">📊 Bảng tổng kết lớp - Bài 1</div>
    <p>Bảng dưới đây tổng hợp kết quả nộp bài của học sinh, lấy trực tiếp từ Google Sheet. Mỗi học sinh chỉ tính kết quả nộp <b>gần nhất</b>.</p>
    <button class="btn-main" onclick="loadSummary()">🔄 Làm mới dữ liệu</button>
    <p id="summaryStatus" style="color:#888;font-size:.9em;margin-top:8px;"></p>
    <div style="overflow-x:auto;margin-top:14px;">
      <table id="summaryTable" style="width:100%;border-collapse:collapse;text-align:left;font-size:.95em;">
        <thead>
          <tr style="background:#FFE9F2">
            <th style="padding:10px">Họ và tên</th>
            <th style="padding:10px">Lớp</th>
            <th style="padding:10px">Tổng điểm</th>
            <th style="padding:10px">Tình trạng</th>
          </tr>
        </thead>
        <tbody id="summaryBody"></tbody>
      </table>
    </div>
  </div>
</div>

<!-- Hidden Google Form submission (no redirect, no popup for students) -->
<iframe name="hiddenFormFrame" id="hiddenFormFrame" style="display:none;"></iframe>
<form id="gformSubmit"
      action="https://docs.google.com/forms/d/e/1FAIpQLSfRnIDDllzVVfpFSnlJ-GbOCa5xOVSrV9wUe_52DeVqIJg_-Q/formResponse"
      method="POST" target="hiddenFormFrame" style="display:none;">
  <input type="text" name="entry.1335503732" id="gf_hoten">
  <input type="text" name="entry.1057150645" id="gf_lop">
  <input type="text" name="entry.718079156" id="gf_bai">
  <input type="text" name="entry.1055085790" id="gf_diem">
  <input type="text" name="entry.208972816" id="gf_tinhtrang">
</form>

<footer>YCT1 · Bài 1: 你好! · Thiết kế dành cho học sinh cấp 1 - cấp 2 · Liên hệ Teacher Helen: danghelen2601@gmail.com / Zalo 0823365755</footer>

<script>
/* ---------- DATA ---------- */
const vocab = [
  {hz:'你', py:'nǐ', mean:'bạn (ngôi 2)'},
  {hz:'好', py:'hǎo', mean:'tốt, khỏe'},
  {hz:'老师', py:'lǎoshī', mean:'thầy/cô giáo'},
  {hz:'再见', py:'zàijiàn', mean:'tạm biệt'}
];
const numbers = [
  {hz:'一',py:'yī',mean:'1'},{hz:'二',py:'èr',mean:'2'},{hz:'三',py:'sān',mean:'3'},
  {hz:'四',py:'sì',mean:'4'},{hz:'五',py:'wǔ',mean:'5'},{hz:'六',py:'liù',mean:'6'},
  {hz:'七',py:'qī',mean:'7'},{hz:'八',py:'bā',mean:'8'},{hz:'九',py:'jiǔ',mean:'9'},{hz:'十',py:'shí',mean:'10'}
];
const colors=['#FF6FA5','#FFA94D','#4ECDC4','#5B9BFF','#A06CD5','#FFD93D'];

/* ---------- TABS ---------- */
document.querySelectorAll('.tab-btn').forEach(btn=>{
  btn.addEventListener('click',()=>{
    document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
    document.querySelectorAll('.panel').forEach(p=>p.classList.remove('active'));
    btn.classList.add('active');
    document.getElementById(btn.dataset.tab).classList.add('active');
  });
});

/* ---------- AUDIO (Web Speech API) ---------- */
function speak(text){
  if(!('speechSynthesis' in window)){alert('Thiết bị không hỗ trợ phát âm.');return;}
  const u = new SpeechSynthesisUtterance(text);
  u.lang='zh-CN'; u.rate=0.8;
  speechSynthesis.cancel();
  speechSynthesis.speak(u);
}

/* ---------- HANZI WRITER ---------- */
let currentWriters=[], currentChar='';
function openWriter(word){
  currentChar=word;
  document.getElementById('writerTitle').textContent='Nét chữ: '+word;
  document.getElementById('writerModal').classList.add('show');
  const target=document.getElementById('writer-target');
  target.innerHTML='<div style="padding:40px 0;color:#999;font-size:.85em;">⏳ Đang tải nét chữ...</div>';
  currentWriters=[];

  if(typeof HanziWriter === 'undefined'){
    target.innerHTML = `<div style="font-size:4em;color:var(--purple);padding:20px 0;">${word}</div>
      <div style="color:#e06;font-size:.8em;">Không tải được thư viện nét chữ (kiểm tra kết nối Internet).</div>`;
    return;
  }

  target.innerHTML='';
  const chars = Array.from(word); // tách từng chữ Hán, hỗ trợ từ nhiều chữ
  const boxSize = chars.length > 1 ? 130 : 200;

  chars.forEach((ch, idx)=>{
    const wrap = document.createElement('div');
    wrap.style.textAlign='center';
    const box = document.createElement('div');
    box.id = 'writer-char-' + idx;
    box.style.width = boxSize+'px';
    box.style.height = boxSize+'px';
    box.style.background = '#FAFAFA';
    box.style.borderRadius = '14px';
    wrap.appendChild(box);
    const label = document.createElement('div');
    label.style.fontSize = '.75em';
    label.style.color = '#999';
    label.textContent = ch;
    wrap.appendChild(label);
    target.appendChild(wrap);

    try{
      const writer = HanziWriter.create(box.id, ch, {
        width: boxSize, height: boxSize, padding: 8,
        strokeAnimationSpeed: 1, delayBetweenStrokes: 300,
        showOutline: true,
        showCharacter: false,
        onLoadCharDataError: function(){
          box.innerHTML = `<div style="font-size:2.5em;color:var(--purple);padding:14px 0;">${ch}</div>`;
          box.style.background = 'transparent';
        }
      });
      currentWriters.push(writer);
      writer.animateCharacter();
    }catch(e){
      box.innerHTML = `<div style="font-size:2.5em;color:var(--purple);padding:14px 0;">${ch}</div>`;
    }
  });
}
function replayWriter(){
  if(currentWriters.length){
    currentWriters.forEach(w => w.animateCharacter());
  } else if(currentChar){
    openWriter(currentChar);
  }
}
function closeWriter(){ document.getElementById('writerModal').classList.remove('show'); }

/* ---------- RENDER VOCAB ---------- */
function renderVocabGrid(list, el){
  const grid=document.getElementById(el);
  list.forEach(v=>{
    const div=document.createElement('div');
    div.className='vocab-card';
    div.innerHTML=`<div class="hz">${v.hz}</div><div class="py">${v.py}</div><div class="mean">${v.mean}</div>
    <button class="btn-mini btn-audio" onclick="speak('${v.hz}')">🔊 Phát âm</button>
    <button class="btn-mini btn-write" onclick="openWriter('${v.hz}')">✍️ Nét chữ</button>`;
    grid.appendChild(div);
  });
}
renderVocabGrid(vocab,'vocabGrid');
renderVocabGrid(numbers,'numberGrid');

/* warm up numbers */
const wu=document.getElementById('warmupNumbers');
numbers.forEach((n,i)=>{
  const b=document.createElement('div');
  b.className='num-bubble';
  b.style.background=colors[i%colors.length];
  b.innerHTML=`<div>${n.mean}</div><div style="font-size:.7em">${n.hz}</div>`;
  b.onclick=()=>speak(n.hz);
  wu.appendChild(b);
});

/* ---------- GAME 1: MATCHING ---------- */
const matchData = vocab.concat(numbers.slice(0,4));
let shuffledRight = [...matchData].sort(()=>Math.random()-0.5);
let selLeft=null, selRight=null, matchedCount=0;
function renderMatch(){
  const L=document.getElementById('matchLeft'), R=document.getElementById('matchRight');
  L.innerHTML=''; R.innerHTML='';
  matchData.forEach((v,i)=>{
    const d=document.createElement('div');
    d.className='match-item'; d.textContent=v.py; d.dataset.idx=i;
    d.onclick=()=>selectMatch('left',d,i);
    L.appendChild(d);
  });
  shuffledRight.forEach((v)=>{
    const d=document.createElement('div');
    d.className='match-item'; d.textContent=v.hz;
    d.dataset.idx=matchData.indexOf(v);
    d.onclick=()=>selectMatch('right',d,matchData.indexOf(v));
    R.appendChild(d);
  });
}
function selectMatch(side,el,idx){
  if(el.classList.contains('correct'))return;
  if(side==='left'){ if(selLeft) selLeft.classList.remove('selected'); selLeft=el; el.classList.add('selected'); }
  else { if(selRight) selRight.classList.remove('selected'); selRight=el; el.classList.add('selected'); }
  if(selLeft && selRight){
    if(selLeft.dataset.idx===selRight.dataset.idx){
      selLeft.classList.add('correct'); selRight.classList.add('correct');
      selLeft.classList.remove('selected'); selRight.classList.remove('selected');
      matchedCount++;
      document.getElementById('matchResult').textContent = matchedCount===matchData.length ? '🎉 Hoàn thành! Con đã nối đúng tất cả!' : `Đã nối đúng ${matchedCount}/${matchData.length}`;
    } else {
      selLeft.classList.add('wrong'); selRight.classList.add('wrong');
      setTimeout(()=>{selLeft.classList.remove('wrong','selected');selRight.classList.remove('wrong','selected');},500);
    }
    selLeft=null; selRight=null;
  }
}
renderMatch();

/* ---------- GAME 2: MEMORY ---------- */
let memCards=[];
vocab.forEach(v=>{ memCards.push({key:v.hz+v.py,display:v.hz}); memCards.push({key:v.hz+v.py,display:v.mean}); });
memCards = memCards.sort(()=>Math.random()-0.5);
let flipped=[], lockBoard=false, memMatched=0;
function renderMemory(){
  const grid=document.getElementById('memoryGrid');
  grid.innerHTML='';
  memCards.forEach((c,i)=>{
    const d=document.createElement('div');
    d.style.cssText='height:60px;background:var(--blue);color:white;display:flex;align-items:center;justify-content:center;border-radius:10px;cursor:pointer;font-weight:700;font-size:.85em;text-align:center;padding:4px;';
    d.textContent='❓';
    d.dataset.idx=i; d.dataset.flipped='0';
    d.onclick=()=>flipCard(d,c);
    grid.appendChild(d);
  });
}
function flipCard(el,c){
  if(lockBoard||el.dataset.flipped==='1')return;
  el.textContent=c.display; el.style.background='white'; el.style.color='var(--ink)'; el.style.border='2px solid var(--purple)';
  el.dataset.flipped='1';
  flipped.push({el,c});
  if(flipped.length===2){
    lockBoard=true;
    if(flipped[0].c.key===flipped[1].c.key){
      flipped.forEach(f=>{f.el.style.background='var(--green)';f.el.style.color='white';});
      memMatched++;
      document.getElementById('memoryResult').textContent = memMatched===vocab.length ? '🎉 Con đã lật đúng hết các thẻ!' : `Đã ghép đúng ${memMatched}/${vocab.length} cặp`;
      flipped=[]; lockBoard=false;
    } else {
      setTimeout(()=>{
        flipped.forEach(f=>{f.el.textContent='❓'; f.el.style.background='var(--blue)'; f.el.style.color='white'; f.el.dataset.flipped='0';});
        flipped=[]; lockBoard=false;
      },700);
    }
  }
}
renderMemory();

/* ---------- TRẮC NGHIỆM ---------- */
const quizQuestions=[
  {q:'"你好" có nghĩa là gì?',opts:['Tạm biệt','Xin chào','Cảm ơn','Xin lỗi'],ans:1},
  {q:'"再见" được dùng khi nào?',opts:['Khi gặp nhau','Khi chia tay','Khi ăn cơm','Khi ngủ'],ans:1},
  {q:'Số "五" đọc là gì?',opts:['sān','wǔ','qī','jiǔ'],ans:1},
  {q:'Cách chào cô giáo đúng nhất là?',opts:['你好','老师好','再见','谢谢'],ans:1},
  {q:'Số "十" có nghĩa là số mấy?',opts:['7','8','9','10'],ans:3}
];
let quizAnswers={};
function renderQuiz(){
  const area=document.getElementById('quizArea');
  quizQuestions.forEach((q,qi)=>{
    const div=document.createElement('div');
    div.className='quiz-q';
    div.innerHTML=`<b>Câu ${qi+1}:</b> ${q.q}`;
    q.opts.forEach((o,oi)=>{
      const b=document.createElement('button');
      b.className='quiz-opt'; b.textContent=o;
      b.onclick=()=>{ quizAnswers[qi]=oi;
        div.querySelectorAll('.quiz-opt').forEach(x=>x.classList.remove('sel'));
        b.classList.add('sel');
      };
      div.appendChild(b);
    });
    area.appendChild(div);
  });
}
renderQuiz();
function submitQuiz(){
  let correct=0;
  quizQuestions.forEach((q,qi)=>{ if(quizAnswers[qi]===q.ans) correct++; });
  const score=Math.round(correct/quizQuestions.length*100);
  const box=document.getElementById('quizScoreBox');
  box.style.display='block';
  box.textContent = `Điểm của con: ${score}/100 — ${score>=60?'Đạt ✅':'Chưa đạt, cố lên nhé! 💪'}`;
}

/* ---------- BÀI TẬP (graded, scored /100) ---------- */
// Câu 1-10: number matching mini multiple choice
const ex1Data=[
  {n:'一',ans:'1'},{n:'二',ans:'2'},{n:'三',ans:'3'},{n:'四',ans:'4'},{n:'五',ans:'5'},
  {n:'六',ans:'6'},{n:'七',ans:'7'},{n:'八',ans:'8'},{n:'九',ans:'9'},{n:'十',ans:'10'}
];
const ex1Container=document.getElementById('ex1');
ex1Data.forEach((item,i)=>{
  const row=document.createElement('div');
  row.style.margin='6px 0';
  row.innerHTML=`<b>${item.n}</b> = <select id="ex1_${i}">
    <option value="">--</option>
    ${[...Array(10)].map((_,k)=>`<option value="${k+1}">${k+1}</option>`).join('')}
  </select>`;
  ex1Container.appendChild(row);
});

const ex13Container=document.getElementById('ex13');
['你好','再见','老师好','谢谢'].forEach(opt=>{
  const lbl=document.createElement('label');
  lbl.style.display='block'; lbl.style.margin='4px 0';
  lbl.innerHTML=`<input type="radio" name="ex13" value="${opt}"> ${opt}`;
  ex13Container.appendChild(lbl);
});

let hwScore=0;
function gradeHomework(){
  let totalQuestions = ex1Data.length + 1 /*fill*/ + 1 /*order*/ + 1 /*ex13*/ + 2 /*hz7,hz9*/;
  let pointsEach = 100/totalQuestions;
  let score=0;

  ex1Data.forEach((item,i)=>{
    const sel=document.getElementById('ex1_'+i).value;
    if(sel===item.ans) score+=pointsEach;
  });

  if(document.getElementById('fillBlank1').value.trim().length>0) score+=pointsEach; // accept any name filled in

  const o1=document.getElementById('order1').value, o2=document.getElementById('order2').value;
  if(o1==='你好！' && o2==='再见！') score+=pointsEach;

  const ex13sel=document.querySelector('input[name="ex13"]:checked');
  if(ex13sel && ex13sel.value==='老师好') score+=pointsEach;

  if(document.getElementById('hz7').value.trim()==='七') score+=pointsEach;
  if(document.getElementById('hz9').value.trim()==='九') score+=pointsEach;

  hwScore=Math.round(score);
  const box=document.getElementById('hwScoreBox');
  box.style.display='block';
  box.textContent = `Điểm bài tập: ${hwScore}/100 — ${hwScore>=60?'Đạt ✅':'Chưa đạt, con xem lại bài nhé! 💪'}`;
}

function submitHomework(){
  const name=document.getElementById('stuName').value.trim();
  const cls=document.getElementById('stuClass').value.trim();
  if(!name||!cls){ alert('Vui lòng điền đầy đủ Họ tên và Lớp trước khi nộp bài.'); return; }
  if(document.getElementById('hwScoreBox').style.display!=='block'){
    alert('Vui lòng bấm "Chấm điểm bài tập" trước khi nộp bài.'); return;
  }
  const tinhtrang = hwScore>=60 ? 'Đạt' : 'Không đạt';

  // Gửi dữ liệu vào Google Form bằng 2 cách song song để tăng độ tin cậy
  document.getElementById('gf_hoten').value = name;
  document.getElementById('gf_lop').value = cls;
  document.getElementById('gf_bai').value = 'Bài 1 - 你好!';
  document.getElementById('gf_diem').value = hwScore;
  document.getElementById('gf_tinhtrang').value = tinhtrang;

  // Cách 1: submit form ẩn qua iframe
  document.getElementById('gformSubmit').submit();

  // Cách 2: fetch trực tiếp (dự phòng, không cần đợi phản hồi vì no-cors)
  const fd = new URLSearchParams();
  fd.append('entry.1335503732', name);
  fd.append('entry.1057150645', cls);
  fd.append('entry.718079156', 'Bài 1 - 你好!');
  fd.append('entry.1055085790', hwScore);
  fd.append('entry.208972816', tinhtrang);
  fetch('https://docs.google.com/forms/d/e/1FAIpQLSfRnIDDllzVVfpFSnlJ-GbOCa5xOVSrV9wUe_52DeVqIJg_-Q/formResponse', {
    method:'POST', mode:'no-cors', body: fd
  }).catch(()=>{ /* no-cors nên luôn coi như đã gửi, lỗi ở đây không quan trọng */ });

  document.getElementById('submitMsg').innerHTML =
    `✅ Đã nộp bài thành công! Kết quả của <b>${name} - Lớp ${cls}</b>: <b>${hwScore}/100</b> (${tinhtrang}).<br>
     Cô giáo sẽ thấy kết quả của con trong bảng <b>Tổng kết</b>. Nếu cần, con cũng có thể liên hệ Teacher Helen qua Zalo: <b>0823365755</b>.`;
}

/* ---------- TỔNG KẾT (đọc Google Sheet đã publish dạng CSV) ---------- */
const SUMMARY_CSV_URL = 'https://docs.google.com/spreadsheets/d/e/2PACX-1vTbzQSk2VzxykyqxFjQ3Eyz2xPTe2tePsGUpMWlpiyX2ybP5Vj9CRu4uFq4B99MQEKjLWnVw0pugy9u/pub?output=csv';

function parseCSV(text){
  // Simple CSV parser hỗ trợ dấu phẩy trong ngoặc kép
  const rows=[];
  let row=[], field='', inQuotes=false;
  for(let i=0;i<text.length;i++){
    const c=text[i];
    if(inQuotes){
      if(c==='"'){ if(text[i+1]==='"'){field+='"';i++;} else inQuotes=false; }
      else field+=c;
    } else {
      if(c==='"') inQuotes=true;
      else if(c===','){ row.push(field); field=''; }
      else if(c==='\n'){ row.push(field); rows.push(row); row=[]; field=''; }
      else if(c==='\r'){ /* skip */ }
      else field+=c;
    }
  }
  if(field.length || row.length){ row.push(field); rows.push(row); }
  return rows;
}

async function loadSummary(){
  const status=document.getElementById('summaryStatus');
  const body=document.getElementById('summaryBody');
  status.textContent='⏳ Đang tải dữ liệu...';
  body.innerHTML='';
  try{
    const res = await fetch(SUMMARY_CSV_URL + '&t=' + Date.now());
    if(!res.ok) throw new Error('HTTP '+res.status);
    const text = await res.text();
    const rows = parseCSV(text).filter(r=>r.length>1 && r.some(c=>c.trim()!==''));
    if(rows.length<2){ status.textContent='Chưa có học sinh nào nộp bài.'; return; }

    const header = rows[0].map(h=>h.trim().toLowerCase());
    const idxHoten = header.findIndex(h=>h.includes('ho_ten')||h.includes('họ'));
    const idxLop = header.findIndex(h=>h.includes('lop')||h.includes('lớp'));
    const idxDiem = header.findIndex(h=>h.includes('diem')||h.includes('điểm'));
    const idxTinhtrang = header.findIndex(h=>h.includes('tinh_trang')||h.includes('tình'));

    // Giữ lại bản nộp gần nhất của mỗi học sinh (theo Họ tên + Lớp)
    const latest = {};
    for(let i=1;i<rows.length;i++){
      const r=rows[i];
      const hoten=(r[idxHoten]||'').trim();
      const lop=(r[idxLop]||'').trim();
      if(!hoten||!lop) continue;
      const key=hoten+'|||'+lop;
      latest[key] = { hoten, lop, diem:(r[idxDiem]||'').trim(), tinhtrang:(r[idxTinhtrang]||'').trim() };
    }

    const list = Object.values(latest).sort((a,b)=> a.lop.localeCompare(b.lop) || a.hoten.localeCompare(b.hoten));
    list.forEach(item=>{
      const tr=document.createElement('tr');
      tr.style.borderBottom='1px solid #f0e0ea';
      const dat = item.tinhtrang==='Đạt';
      tr.innerHTML = `<td style="padding:8px">${item.hoten}</td>
        <td style="padding:8px">${item.lop}</td>
        <td style="padding:8px;font-weight:700">${item.diem}</td>
        <td style="padding:8px;font-weight:700;color:${dat?'#2bb673':'#e0556b'}">${item.tinhtrang==='Đạt'?'✅ Đạt':'❌ Không đạt'}</td>`;
      body.appendChild(tr);
    });
    status.textContent = `Cập nhật lúc ${new Date().toLocaleTimeString('vi-VN')} · Tổng số học sinh đã nộp: ${list.length}`;
  }catch(e){
    status.innerHTML = `⚠️ Không tải được dữ liệu (${e.message}). Kiểm tra: Sheet đã "Publish to web" dạng CSV chưa, hoặc thử bấm "Làm mới dữ liệu" lại.`;
  }
}
// Tự tải dữ liệu khi mở tab Tổng kết
document.querySelector('[data-tab="tongket"]').addEventListener('click', loadSummary);
</script>
</body>
</html>
