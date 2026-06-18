[gemini-code-1781766906766.html](https://github.com/user-attachments/files/29081833/gemini-code-1781766906766.html)
# test<!DOCTYPE html>
<html lang="ka">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>2026 წლის ფეხბურთის შიდა ჩემპიონატი</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Georgian:wght@400;600;700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --orange: #FF6B00;
    --orange-dark: #E05500;
    --orange-light: #FF8C33;
    --blue: #1E6FD9;
    --blue-dark: #1557B0;
    --white: #FFFFFF;
    --off-white: #FFF8F2;
    --teal: #4ECDC4;
    --dark: #1A1A2E;
    --gray: #F5F5F5;
    --text-dark: #1A1A2E;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Noto Sans Georgian', sans-serif;
    background: var(--off-white);
    color: var(--text-dark);
    overflow-x: hidden;
  }

  .hero {
    background: var(--orange);
    background-image: radial-gradient(ellipse at top right, #FF9A3C 0%, #FF6B00 40%, #E05500 100%);
    padding: 0;
    position: relative;
    overflow: hidden;
    min-height: 220px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 300px; height: 300px;
    border-radius: 50%;
    background: rgba(255,255,255,0.07);
  }
  .hero::after {
    content: '';
    position: absolute;
    bottom: -80px; left: -40px;
    width: 250px; height: 250px;
    border-radius: 50%;
    background: rgba(255,255,255,0.05);
  }
  .hero-inner {
    position: relative;
    z-index: 2;
    padding: 48px 24px 40px;
  }
  .brand-logo {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    margin-bottom: 20px;
  }
  .brand-logo svg { width: 36px; height: 36px; }
  .brand-name {
    font-size: 22px;
    font-weight: 900;
    color: white;
    letter-spacing: 2px;
    text-transform: uppercase;
  }
  .hero-title {
    font-size: clamp(26px, 5vw, 48px);
    font-weight: 900;
    color: white;
    text-shadow: 3px 3px 0 var(--blue-dark), 0 0 40px rgba(0,0,0,0.3);
    line-height: 1.1;
    -webkit-text-stroke: 1px rgba(0,0,0,0.15);
  }
  .hero-subtitle {
    margin-top: 14px;
    font-size: 15px;
    font-weight: 600;
    color: rgba(255,255,255,0.9);
    letter-spacing: 1px;
    background: rgba(30,111,217,0.7);
    display: inline-block;
    padding: 5px 18px;
    border-radius: 20px;
  }
  .hero-balls {
    position: absolute;
    font-size: 80px;
    opacity: 0.08;
    top: 10px; left: 20px;
    user-select: none;
  }
  .hero-balls2 {
    position: absolute;
    font-size: 60px;
    opacity: 0.06;
    bottom: 5px; right: 30px;
    user-select: none;
  }

  .tab-bar {
    background: var(--blue);
    display: flex;
    justify-content: center;
    overflow-x: auto;
    scrollbar-width: none;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 4px 12px rgba(0,0,0,0.2);
  }
  .tab-bar::-webkit-scrollbar { display: none; }
  .tab-btn {
    padding: 14px 22px;
    color: rgba(255,255,255,0.75);
    font-size: 13px;
    font-weight: 700;
    font-family: 'Noto Sans Georgian', sans-serif;
    cursor: pointer;
    border: none;
    background: none;
    white-space: nowrap;
    transition: all 0.2s;
    border-bottom: 3px solid transparent;
  }
  .tab-btn:hover { color: white; background: rgba(255,255,255,0.1); }
  .tab-btn.active {
    color: white;
    border-bottom: 3px solid var(--orange);
    background: rgba(255,255,255,0.1);
  }

  .section { display: none; padding: 24px 16px 40px; max-width: 1000px; margin: 0 auto; }
  .section.active { display: block; }

  .section-title {
    font-size: 22px;
    font-weight: 900;
    color: var(--orange);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 10px;
    border-left: 5px solid var(--orange);
    padding-left: 12px;
  }

  .groups-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 16px;
    margin-bottom: 24px;
  }
  .group-card {
    background: white;
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 4px 20px rgba(255,107,0,0.1);
    border: 2px solid transparent;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .group-card:hover { transform: translateY(-3px); box-shadow: 0 8px 30px rgba(255,107,0,0.2); }
  .group-header {
    background: var(--orange);
    padding: 12px 18px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .group-header.blue { background: var(--blue); }
  .group-header.teal { background: #0891B2; }
  .group-label {
    font-size: 20px;
    font-weight: 900;
    color: white;
  }
  .group-region {
    font-size: 11px;
    color: rgba(255,255,255,0.85);
    font-weight: 600;
    background: rgba(0,0,0,0.2);
    padding: 3px 10px;
    border-radius: 20px;
  }

  .players-table-wrap { overflow-x: auto; }
  table { width: 100%; border-collapse: collapse; background: white; font-size: 13px; }
  thead tr { background: #f9f9f9; color: var(--dark); border-bottom: 2px solid #eee; }
  thead th { padding: 10px 12px; text-align: left; font-weight: 800; white-space: nowrap; font-size: 12px; }
  tbody tr { border-bottom: 1px solid #f0f0f0; transition: background 0.15s; }
  tbody tr:last-child { border-bottom: none; }
  tbody tr:hover { background: #FFF8F2; }
  tbody td { padding: 10px 12px; vertical-align: middle; font-weight: 600; color: #444; }
  
  .team-badge {
    display: inline-block;
    font-weight: 800;
    font-size: 12px;
    padding: 3px 10px;
    border-radius: 10px;
    background: var(--orange);
    color: white;
    white-space: nowrap;
  }
  .team-badge.blue { background: var(--blue); }
  .team-badge.teal { background: #0891B2; }
  .goal-count {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 22px;
    height: 22px;
    border-radius: 50%;
    background: #FFF0E5;
    color: var(--orange);
    font-size: 11px;
    font-weight: 800;
  }
  td.goal-count-cell { text-align: center; }

  footer {
    background: var(--orange);
    color: white;
    text-align: center;
    padding: 20px;
    font-size: 13px;
    font-weight: 600;
    margin-top: 40px;
  }
  footer span { opacity: 0.8; }
</style>
<script>
  function showTab(tabId, btn) {
    document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
    document.getElementById(tabId).classList.add('active');
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
  }
</script>
</head>
<body>

<div class="hero">
  <div class="hero-balls">⚽</div>
  <div class="hero-balls2">⚽</div>
  <div class="hero-inner">
    <div class="brand-logo">
      <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="50" cy="50" r="45" fill="rgba(255,255,255,0.2)" stroke="white" stroke-width="3"/>
        <path d="M30 35 Q50 20 70 35 Q80 50 70 65 Q50 80 30 65 Q20 50 30 35Z" fill="rgba(255,255,255,0.3)" stroke="white" stroke-width="2"/>
        <path d="M40 42 L60 42 M50 32 L50 68 M35 55 L65 55" stroke="white" stroke-width="2.5" stroke-linecap="round"/>
      </svg>
      <span class="brand-name">ზუმერი</span>
    </div>
    <div class="hero-title">2026 წლის ფეხბურთის<br>შიდა ჩემპიონატი</div>
    <div class="hero-subtitle">⚽ ივნისი – ივლისი 2026 &nbsp;|&nbsp; 3 ჯგუფი &nbsp;|&nbsp; 13 გუნდი</div>
  </div>
</div>

<div class="tab-bar">
  <button class="tab-btn active" onclick="showTab('groups', this)">🏆 ქულათა ცხრილი</button>
  <button class="tab-btn" onclick="showTab('stats', this)">⚽ გოლების სტატისტიკა</button>
</div>

<div class="section active" id="groups">
  <h2 class="section-title">🏆 ჯგუფური ეტაპის შედეგები</h2>
  
  <div class="groups-grid">
    <div class="group-card">
      <div class="group-header">
        <span class="group-label">ჯგუფი A</span>
        <span class="group-region">აღმოსავლეთი</span>
      </div>
      <div class="players-table-wrap">
        <table>
          <thead>
            <tr>
              <th>გუნდი</th>
              <th>თ</th>
              <th>მ</th>
              <th>ფ</th>
              <th>წ</th>
              <th>გატ/გაშ</th>
              <th>სხვ</th>
              <th>ქულა</th>
            </tr>
          </thead>
          <tbody>
            <tr><td>OFA</td><td>1</td><td>1</td><td>0</td><td>0</td><td>9 - 0</td><td>9</td><td>3</td></tr>
            <tr><td>Blue Lock</td><td>1</td><td>1</td><td>0</td><td>0</td><td>11 - 3</td><td>8</td><td>3</td></tr>
            <tr><td>Phoenix</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0 - 0</td><td>0</td><td>0</td></tr>
            <tr><td>ბოლო სეზონი</td><td>1</td><td>0</td><td>0</td><td>1</td><td>3 - 11</td><td>-8</td><td>0</td></tr>
            <tr><td>ონლაინი</td><td>1</td><td>0</td><td>0</td><td>1</td><td>0 - 9</td><td>-9</td><td>0</td></tr>
          </tbody>
        </table>
      </div>
    </div>

    <div class="group-card">
      <div class="group-header blue">
        <span class="group-label">ჯგუფი B</span>
        <span class="group-region">აღმოსავლეთი</span>
      </div>
      <div class="players-table-wrap">
        <table>
          <thead>
            <tr>
              <th>გუნდი</th>
              <th>თ</th>
              <th>მ</th>
              <th>ფ</th>
              <th>წ</th>
              <th>გატ/გაშ</th>
              <th>სხვ</th>
              <th>ქულა</th>
            </tr>
          </thead>
          <tbody>
            <tr><td>იმპულსი</td><td>1</td><td>1</td><td>0</td><td>0</td><td>5 - 1</td><td>4</td><td>3</td></tr>
            <tr><td>Midnight Hummer</td><td>1</td><td>0</td><td>1</td><td>0</td><td>0 - 0</td><td>0</td><td>1</td></tr>
            <tr><td>Black Stone</td><td>1</td><td>0</td><td>1</td><td>0</td><td>0 - 0</td><td>0</td><td>1</td></tr>
            <tr><td>QSANI</td><td>1</td><td>0</td><td>0</td><td>1</td><td>1 - 5</td><td>-4</td><td>0</td></tr>
          </tbody>
        </table>
      </div>
    </div>

    <div class="group-card">
      <div class="group-header teal">
        <span class="group-label">ჯგუფი C</span>
        <span class="group-region">დასავლეთი</span>
      </div>
      <div class="players-table-wrap">
        <table>
          <thead>
            <tr>
              <th>გუნდი</th>
              <th>თ</th>
              <th>მ</th>
              <th>ფ</th>
              <th>წ</th>
              <th>გატ/გაშ</th>
              <th>სხვ</th>
              <th>ქულა</th>
            </tr>
          </thead>
          <tbody>
            <tr><td>ზუმერელი BMW შნიკები</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0 - 0</td><td>0</td><td>0</td></tr>
            <tr><td>SHŌRI-DAN</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0 - 0</td><td>0</td><td>0</td></tr>
            <tr><td>FC 404 Team</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0 - 0</td><td>0</td><td>0</td></tr>
            <tr><td>ენერჯაიზერები 2032</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0 - 0</td><td>0</td><td>0</td></tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</div>

<div class="section" id="stats">
  <h2 class="section-title">⚽ გატანილი გოლების ანალიტიკა</h2>
  
  <div class="players-table-wrap" style="background: white; border-radius: 12px; box-shadow: 0 4px 20px rgba(0,0,0,0.08);">
    <table>
      <thead style="background: var(--orange); color: white;">
        <tr>
          <th style="color: white;">ავტორი</th>
          <th style="color: white; text-align: center;">გოლები</th>
          <th style="color: white;">გუნდი</th>
          <th style="color: white;">ფილიალი / დეპარტამენტი</th>
          <th style="color: white;">თარიღი</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>ლუკა აბრამაშვილი</td>
          <td class="goal-count-cell"><span class="goal-count">2</span></td>
          <td><span class="team-badge">იმპულსი</span></td>
          <td>თბილისი მოლი</td>
          <td>16.06.2026</td>
        </tr>
        <tr>
          <td>გიორგი პაიჭაძე</td>
          <td class="goal-count-cell"><span class="goal-count">1</span></td>
          <td><span class="team-badge">იმპულსი</span></td>
          <td>თბილისი მოლი</td>
          <td>16.06.2026</td>
        </tr>
        <tr>
          <td>ლუკა მჭედლიშვილი</td>
          <td class="goal-count-cell"><span class="goal-count">2</span></td>
          <td><span class="team-badge">იმპულსი</span></td>
          <td>თბილისი მოლი</td>
          <td>16.06.2026</td>
        </tr>
        <tr>
          <td>საბა ტაგანაშვილი</td>
          <td class="goal-count-cell"><span class="goal-count">1</span></td>
          <td><span class="team-badge blue">QSANI</span></td>
          <td>საბითუმო ქსანი</td>
          <td>16.06.2026</td>
        </tr>
        <tr>
          <td>გიორგი ხიზანიშვილი</td>
          <td class="goal-count-cell"><span class="goal-count">4</span></td>
          <td><span class="team-badge teal">OFA</span></td>
          <td>ოფისი</td>
          <td>17.06.2026</td>
        </tr>
        <tr>
          <td>გიორგი კიკნაძე</td>
          <td class="goal-count-cell"><span class="goal-count">3</span></td>
          <td><span class="team-badge teal">OFA</span></td>
          <td>ოფისი</td>
          <td>17.06.2026</td>
        </tr>
        <tr>
          <td>მათე დიდია</td>
          <td class="goal-count-cell"><span class="goal-count">1</span></td>
          <td><span class="team-badge teal">OFA</span></td>
          <td>ოფისი</td>
          <td>17.06.2026</td>
        </tr>
        <tr>
          <td>თენგო გიგილაშვილი</td>
          <td class="goal-count-cell"><span class="goal-count">1</span></td>
          <td><span class="team-badge teal">OFA</span></td>
          <td>ოფისი</td>
          <td>17.06.2026</td>
        </tr>
        <tr>
          <td>ნიკოლოზ მინდაძე</td>
          <td class="goal-count-cell"><span class="goal-count">4</span></td>
          <td><span class="team-badge blue">Blue Lock</span></td>
          <td>ისთ ფოინთი</td>
          <td>17.06.2026</td>
        </tr>
        <tr>
          <td>დემეტრე გრიგოლია</td>
          <td class="goal-count-cell"><span class="goal-count">5</span></td>
          <td><span class="team-badge blue">Blue Lock</span></td>
          <td>ისთ ფოინთი</td>
          <td>17.06.2026</td>
        </tr>
        <tr>
          <td>ნიკოლოზ ირემაშვილი</td>
          <td class="goal-count-cell"><span class="goal-count">1</span></td>
          <td><span class="team-badge blue">Blue Lock</span></td>
          <td>ისთ ფოინთი</td>
          <td>17.06.2026</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<footer>
  <strong>2026 წლის ფეხბურთის შიდა ჩემპიონატი</strong><br>
  <span>ზუმერი &nbsp;•&nbsp; ივნისი – ივლისი 2026 &nbsp;•&nbsp; 13 გუნდი</span>
</footer>

</body>
</html>
