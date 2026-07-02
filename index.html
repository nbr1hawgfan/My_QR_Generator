<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>QR Forge</title>
<meta name="description" content="Turn a link, note, or contact into a QR code and save it to your device.">
<meta name="theme-color" content="#EEF0F3">
<link rel="manifest" href="manifest.json">
<link rel="icon" href="icon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" href="icon-192.png">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#EEF0F3;
    --surface:#FFFFFF;
    --surface-raised:#F5F6F8;
    --line:#D9DCE1;
    --line-soft:#E3E5E9;
    --ink:#12151C;
    --ink-dim:#4B5560;
    --ink-faint:#8A8F98;
    --amber:#B4790E;
    --amber-dim:#E4C48C;
    --green:#1F7A4D;
    --radius:12px;
    --sans:'Inter', system-ui, sans-serif;
    --display:'Space Grotesk', system-ui, sans-serif;
  }
  *{box-sizing:border-box;}
  html,body{margin:0;padding:0;}
  body{
    background:var(--bg);
    color:var(--ink);
    font-family:var(--sans);
    min-height:100vh;
    display:flex;
    justify-content:center;
    padding:44px 20px 64px;
  }
  .wrap{width:100%;max-width:460px;}

  header{margin-bottom:24px;}
  h1{
    font-family:var(--display);
    font-weight:600;
    font-size:26px;
    margin:0 0 6px;
    letter-spacing:-0.01em;
  }
  header p{
    margin:0;
    color:var(--ink-dim);
    font-size:14px;
    line-height:1.55;
    max-width:42ch;
  }

  .tabs{
    display:flex;
    gap:6px;
    background:var(--surface-raised);
    border:1px solid var(--line);
    border-radius:10px;
    padding:4px;
    margin-bottom:16px;
  }
  .tab{
    flex:1;
    text-align:center;
    padding:9px 8px;
    font-size:12.5px;
    font-weight:500;
    font-family:var(--sans);
    color:var(--ink-dim);
    background:transparent;
    border:none;
    border-radius:7px;
    cursor:pointer;
  }
  .tab.active{
    background:var(--surface);
    color:var(--ink);
    box-shadow:0 1px 2px rgba(18,21,28,.08);
  }

  .card{
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:var(--radius);
    padding:20px;
    margin-bottom:16px;
  }
  .panel{display:none;}
  .panel.active{display:block;}

  label.field-label{
    display:block;
    font-size:12px;
    font-weight:500;
    color:var(--ink-dim);
    margin-bottom:6px;
  }

  textarea, input[type=text], input[type=tel], input[type=email], input[type=url]{
    width:100%;
    background:var(--bg);
    border:1px solid var(--line);
    border-radius:9px;
    color:var(--ink);
    font-family:var(--sans);
    font-size:14px;
    line-height:1.5;
    padding:10px 12px;
    outline:none;
  }
  textarea{resize:vertical;min-height:88px;}
  textarea::placeholder, input::placeholder{color:var(--ink-faint);}
  textarea:focus, input:focus{border-color:var(--amber-dim);}

  .field{margin-bottom:14px;}
  .field:last-child{margin-bottom:0;}
  .field-hint{font-size:11.5px;color:var(--ink-faint);margin-top:6px;line-height:1.5;}

  .row{display:flex;gap:12px;margin-top:14px;}
  .row > div{flex:1;}
  .row.fields{margin-top:0;margin-bottom:14px;}

  select, input[type=color]{
    width:100%;
    background:var(--bg);
    border:1px solid var(--line);
    border-radius:9px;
    color:var(--ink);
    font-family:var(--sans);
    font-size:13px;
    padding:9px 10px;
    outline:none;
  }
  input[type=color]{padding:4px;height:38px;cursor:pointer;}
  select:focus{border-color:var(--amber-dim);}
  select:disabled{opacity:.5;}

  .char-count{
    text-align:right;
    font-size:11.5px;
    color:var(--ink-faint);
    margin-top:6px;
  }
  .char-count.warn{color:var(--amber);}

  .options-card{margin-top:0;}

  .logo-row{
    display:flex;
    align-items:center;
    gap:12px;
    margin-top:14px;
  }
  .logo-preview{
    width:38px;height:38px;
    border-radius:8px;
    border:1px solid var(--line);
    background:var(--bg);
    display:flex;
    align-items:center;
    justify-content:center;
    overflow:hidden;
    flex-shrink:0;
  }
  .logo-preview img{width:100%;height:100%;object-fit:contain;}
  .logo-preview svg{width:16px;height:16px;color:var(--ink-faint);}
  .logo-controls{flex:1;display:flex;gap:8px;}
  .file-btn{
    font-size:12.5px;
    font-weight:500;
    padding:8px 12px;
    border:1px solid var(--line);
    border-radius:8px;
    background:var(--surface-raised);
    color:var(--ink);
    cursor:pointer;
  }
  .file-btn:hover{border-color:var(--ink-faint);}
  input[type=file]{display:none;}

  .viewfinder{
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:var(--radius);
    padding:28px;
    display:flex;
    align-items:center;
    justify-content:center;
    margin-bottom:16px;
    min-height:280px;
  }

  #qr-stage{
    position:relative;
    background:#fff;
    padding:16px;
    border-radius:8px;
    line-height:0;
  }
  #qr-stage img, #qr-stage canvas{display:block;image-rendering:pixelated;}

  .empty-state{
    text-align:center;
    color:var(--ink-faint);
    font-size:13px;
    max-width:230px;
    line-height:1.6;
  }
  .empty-state strong{
    display:block;
    font-size:13px;
    color:var(--ink-dim);
    font-weight:500;
    margin-bottom:4px;
  }

  .actions{display:flex;gap:10px;}
  button{
    font-family:var(--sans);
    font-size:13.5px;
    font-weight:500;
    border-radius:9px;
    border:1px solid var(--line);
    background:var(--surface-raised);
    color:var(--ink);
    padding:12px 14px;
    cursor:pointer;
    flex:1;
    display:flex;
    align-items:center;
    justify-content:center;
    gap:8px;
    transition:transform .08s ease, border-color .15s ease;
  }
  button:hover{border-color:var(--ink-faint);}
  button:active{transform:scale(.98);}
  button:disabled{opacity:.4;cursor:not-allowed;}
  button.primary{
    background:var(--ink);
    border-color:var(--ink);
    color:var(--surface);
  }
  button.primary:hover{background:#252B35;}
  button svg{width:15px;height:15px;flex-shrink:0;}

  .toast{
    position:fixed;
    bottom:24px;
    left:50%;
    transform:translateX(-50%) translateY(12px);
    background:var(--surface-raised);
    border:1px solid var(--line);
    color:var(--ink);
    font-size:13px;
    padding:10px 16px;
    border-radius:10px;
    opacity:0;
    pointer-events:none;
    transition:opacity .2s ease, transform .2s ease;
    display:flex;
    align-items:center;
    gap:8px;
  }
  .toast.on{opacity:1;transform:translateX(-50%) translateY(0);}
  .toast .dot{width:6px;height:6px;border-radius:50%;background:var(--green);}

  .history{margin-top:16px;}
  .history-head{
    display:flex;
    align-items:center;
    justify-content:space-between;
    margin-bottom:10px;
  }
  .history-head span{font-size:12px;font-weight:500;color:var(--ink-dim);}
  .history-clear{
    background:none;border:none;color:var(--ink-faint);
    font-size:11.5px;cursor:pointer;padding:0;flex:none;
  }
  .history-clear:hover{color:var(--ink-dim);}
  .history-list{display:flex;flex-direction:column;gap:6px;}
  .history-item{
    display:flex;
    align-items:center;
    gap:10px;
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:9px;
    padding:9px 10px;
  }
  .history-item .htype{
    font-size:10px;
    font-weight:600;
    letter-spacing:.04em;
    text-transform:uppercase;
    color:var(--ink-faint);
    background:var(--surface-raised);
    border-radius:5px;
    padding:3px 6px;
    flex-shrink:0;
  }
  .history-item .hlabel{
    flex:1;
    font-size:12.5px;
    color:var(--ink);
    white-space:nowrap;
    overflow:hidden;
    text-overflow:ellipsis;
  }
  .history-item button{
    flex:none;
    padding:6px 8px;
    border:none;
    background:none;
    color:var(--ink-faint);
  }
  .history-item button:hover{color:var(--ink);}
  .history-empty{
    font-size:12.5px;
    color:var(--ink-faint);
    padding:4px 2px;
  }

  .batch-grid{
    display:grid;
    grid-template-columns:repeat(auto-fill, minmax(128px, 1fr));
    gap:12px;
    margin-top:16px;
  }
  .batch-cell{
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:10px;
    padding:8px;
    text-align:center;
  }
  .batch-cell .qrbox{
    background:#fff;
    border-radius:6px;
    padding:6px;
    display:inline-block;
    line-height:0;
  }
  .batch-cell .caption{
    margin-top:8px;
    font-size:11.5px;
    color:var(--ink-dim);
    line-height:1.4;
    word-break:break-word;
  }

  footer{
    text-align:center;
    color:var(--ink-faint);
    font-size:12px;
    margin-top:22px;
    line-height:1.7;
  }

  @media (max-width:400px){
    .row{flex-direction:column;}
  }

  @media print{
    body{background:#fff;padding:0;}
    header, .tabs, .card, .viewfinder, .actions, .history, footer, .no-print{display:none !important;}
    .batch-print{display:block !important;}
    .batch-grid{margin-top:0;}
    .batch-cell{break-inside:avoid;border-color:#ccc;}
  }
</style>
</head>
<body>
<div class="wrap">

  <header>
    <h1>QR Forge</h1>
    <p>Create a QR code for a link, a note, a contact, or a whole batch of labels &mdash; then save or print it.</p>
  </header>

  <div class="tabs">
    <button class="tab active" id="tabText" type="button">Link or text</button>
    <button class="tab" id="tabContact" type="button">Contact card</button>
    <button class="tab" id="tabBatch" type="button">Batch labels</button>
  </div>

  <div class="card panel active" id="panelText">
    <label class="field-label" for="content">Content</label>
    <textarea id="content" placeholder="https://example.com or any text" maxlength="1200"></textarea>
    <div class="char-count" id="charCount">0 / 1200</div>
  </div>

  <div class="card panel" id="panelContact">
    <div class="row fields">
      <div>
        <label class="field-label" for="cFirst">First name</label>
        <input type="text" id="cFirst" placeholder="Jane">
      </div>
      <div>
        <label class="field-label" for="cLast">Last name</label>
        <input type="text" id="cLast" placeholder="Doe">
      </div>
    </div>
    <div class="field">
      <label class="field-label" for="cOrg">Company</label>
      <input type="text" id="cOrg" placeholder="Logistics Warehouse Inc.">
    </div>
    <div class="field">
      <label class="field-label" for="cTitle">Job title</label>
      <input type="text" id="cTitle" placeholder="Operations Manager">
    </div>
    <div class="row fields">
      <div>
        <label class="field-label" for="cPhone">Phone</label>
        <input type="tel" id="cPhone" placeholder="(555) 123-4567">
      </div>
      <div>
        <label class="field-label" for="cPhoneMobile">Mobile</label>
        <input type="tel" id="cPhoneMobile" placeholder="(555) 987-6543">
      </div>
    </div>
    <div class="field">
      <label class="field-label" for="cEmail">Email</label>
      <input type="email" id="cEmail" placeholder="jane@company.com">
    </div>
    <div class="field">
      <label class="field-label" for="cUrl">Website</label>
      <input type="url" id="cUrl" placeholder="https://company.com">
    </div>
    <div class="field">
      <label class="field-label" for="cAddress">Address</label>
      <input type="text" id="cAddress" placeholder="123 Main St, Fort Smith, AR 72901">
    </div>
  </div>

  <div class="card panel" id="panelBatch">
    <label class="field-label" for="batchInput">Items, one per line</label>
    <textarea id="batchInput" style="min-height:130px" placeholder="Bay A12&#10;Bay A13 | https://example.com/bay/a13&#10;Forklift 07"></textarea>
    <div class="field-hint">Each line becomes one QR code. Add <code>Label | content</code> to set a custom caption &mdash; otherwise the line itself is used as both the code and the caption.</div>
    <button id="generateBatchBtn" class="primary" style="margin-top:14px;width:100%;">Generate sheet</button>
  </div>

  <div class="card options-card" id="singleOptions">
    <div class="row" style="margin-top:0;">
      <div>
        <label class="field-label" for="size">Size</label>
        <select id="size">
          <option value="200">Small &mdash; 200px</option>
          <option value="320" selected>Medium &mdash; 320px</option>
          <option value="480">Large &mdash; 480px</option>
          <option value="640">Extra large &mdash; 640px</option>
        </select>
      </div>
      <div>
        <label class="field-label" for="ecl">Error correction</label>
        <select id="ecl">
          <option value="L">Low</option>
          <option value="M" selected>Medium</option>
          <option value="Q">Quartile</option>
          <option value="H">High</option>
        </select>
      </div>
    </div>

    <div class="row">
      <div>
        <label class="field-label" for="fg">Mark color</label>
        <input type="color" id="fg" value="#12151C">
      </div>
      <div>
        <label class="field-label" for="bg">Background</label>
        <input type="color" id="bg" value="#ffffff">
      </div>
    </div>

    <label class="field-label" style="margin-top:14px;">Logo</label>
    <div class="logo-row">
      <div class="logo-preview" id="logoPreview">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><path d="M21 15l-5-5L5 21"/></svg>
      </div>
      <div class="logo-controls">
        <label class="file-btn" for="logoInput">Upload logo</label>
        <input type="file" id="logoInput" accept="image/*">
        <button type="button" id="removeLogoBtn" style="display:none;flex:none;padding:8px 12px;">Remove</button>
      </div>
    </div>
    <div class="field-hint" id="logoHint" style="display:none;">Error correction was set to High so the code still scans with a logo over it.</div>
  </div>

  <div class="viewfinder no-print" id="singleViewfinder">
    <div id="qr-stage"></div>
    <div class="empty-state" id="emptyState">
      <strong>Nothing to show yet</strong>
      Fill in the fields above and your code will appear here.
    </div>
  </div>

  <div class="actions no-print" id="singleActions">
    <button id="downloadBtn" class="primary" disabled>
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
      Download PNG
    </button>
    <button id="clearBtn">Clear</button>
  </div>

  <div class="batch-print" id="batchOutput" style="display:none;">
    <div class="batch-grid" id="batchGrid"></div>
    <div class="actions no-print" style="margin-top:16px;">
      <button id="printBatchBtn" class="primary">Print sheet</button>
      <button id="clearBatchBtn">Clear</button>
    </div>
  </div>

  <div class="history no-print" id="historySection">
    <div class="history-head">
      <span>Recent codes</span>
      <button class="history-clear" id="clearHistoryBtn" type="button">Clear all</button>
    </div>
    <div class="history-list" id="historyList"></div>
  </div>

  <footer class="no-print">
    Generated entirely on this device &mdash; nothing entered here is sent anywhere.
  </footer>
</div>

<div class="toast" id="toast"><span class="dot"></span><span id="toastMsg">Saved</span></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
<script>
(function(){
  const tabText = document.getElementById('tabText');
  const tabContact = document.getElementById('tabContact');
  const tabBatch = document.getElementById('tabBatch');
  const panelText = document.getElementById('panelText');
  const panelContact = document.getElementById('panelContact');
  const panelBatch = document.getElementById('panelBatch');
  const singleOptions = document.getElementById('singleOptions');
  const singleViewfinder = document.getElementById('singleViewfinder');
  const singleActions = document.getElementById('singleActions');
  const batchOutput = document.getElementById('batchOutput');

  const contentEl = document.getElementById('content');
  const charCount = document.getElementById('charCount');

  const contactFields = ['cFirst','cLast','cOrg','cTitle','cPhone','cPhoneMobile','cEmail','cUrl','cAddress']
    .reduce((acc, id) => { acc[id] = document.getElementById(id); return acc; }, {});

  const sizeEl = document.getElementById('size');
  const eclEl = document.getElementById('ecl');
  const fgEl = document.getElementById('fg');
  const bgEl = document.getElementById('bg');
  const stage = document.getElementById('qr-stage');
  const emptyState = document.getElementById('emptyState');
  const downloadBtn = document.getElementById('downloadBtn');
  const clearBtn = document.getElementById('clearBtn');
  const toast = document.getElementById('toast');
  const toastMsg = document.getElementById('toastMsg');

  const logoInput = document.getElementById('logoInput');
  const logoPreview = document.getElementById('logoPreview');
  const removeLogoBtn = document.getElementById('removeLogoBtn');
  const logoHint = document.getElementById('logoHint');

  const batchInput = document.getElementById('batchInput');
  const generateBatchBtn = document.getElementById('generateBatchBtn');
  const batchGrid = document.getElementById('batchGrid');
  const printBatchBtn = document.getElementById('printBatchBtn');
  const clearBatchBtn = document.getElementById('clearBatchBtn');

  const historyList = document.getElementById('historyList');
  const clearHistoryBtn = document.getElementById('clearHistoryBtn');

  const ECL_MAP = { L: QRCode.CorrectLevel.L, M: QRCode.CorrectLevel.M, Q: QRCode.CorrectLevel.Q, H: QRCode.CorrectLevel.H };
  const HISTORY_KEY = 'qrforge_history';
  const HISTORY_MAX = 12;

  let mode = 'text';
  let debounceTimer = null;
  let logoImage = null;
  let eclBeforeLogo = 'M';

  function escapeVCard(value){
    return String(value || '').replace(/([,;\\])/g, '\\$1');
  }

  function buildVCard(fields){
    const first = fields.cFirst.trim();
    const last = fields.cLast.trim();
    const org = fields.cOrg.trim();
    const title = fields.cTitle.trim();
    const phone = fields.cPhone.trim();
    const mobile = fields.cPhoneMobile.trim();
    const email = fields.cEmail.trim();
    const url = fields.cUrl.trim();
    const address = fields.cAddress.trim();

    const fullName = [first, last].filter(Boolean).join(' ');
    if (!fullName && !org && !phone && !mobile && !email) return '';

    const lines = ['BEGIN:VCARD', 'VERSION:3.0'];
    lines.push('N:' + escapeVCard(last) + ';' + escapeVCard(first) + ';;;');
    lines.push('FN:' + escapeVCard(fullName || org));
    if (org) lines.push('ORG:' + escapeVCard(org));
    if (title) lines.push('TITLE:' + escapeVCard(title));
    if (phone) lines.push('TEL;TYPE=WORK,VOICE:' + escapeVCard(phone));
    if (mobile) lines.push('TEL;TYPE=CELL:' + escapeVCard(mobile));
    if (email) lines.push('EMAIL:' + escapeVCard(email));
    if (url) lines.push('URL:' + escapeVCard(url));
    if (address) lines.push('ADR;TYPE=WORK:;;' + escapeVCard(address) + ';;;;');
    lines.push('END:VCARD');
    return lines.join('\n');
  }

  function currentContactFieldValues(){
    return Object.keys(contactFields).reduce((acc, key) => {
      acc[key] = contactFields[key].value;
      return acc;
    }, {});
  }

  function setMode(next){
    mode = next;
    tabText.classList.toggle('active', mode === 'text');
    tabContact.classList.toggle('active', mode === 'contact');
    tabBatch.classList.toggle('active', mode === 'batch');
    panelText.classList.toggle('active', mode === 'text');
    panelContact.classList.toggle('active', mode === 'contact');
    panelBatch.classList.toggle('active', mode === 'batch');

    const isBatch = mode === 'batch';
    singleOptions.style.display = isBatch ? 'none' : 'block';
    singleViewfinder.style.display = isBatch ? 'none' : 'flex';
    singleActions.style.display = isBatch ? 'none' : 'flex';
    batchOutput.style.display = isBatch && batchGrid.children.length ? 'block' : 'none';

    if (!isBatch) generate();
  }

  tabText.addEventListener('click', () => setMode('text'));
  tabContact.addEventListener('click', () => setMode('contact'));
  tabBatch.addEventListener('click', () => setMode('batch'));

  function showToast(msg){
    toastMsg.textContent = msg;
    toast.classList.add('on');
    setTimeout(() => toast.classList.remove('on'), 1800);
  }

  function getPayload(){
    if (mode === 'text') return contentEl.value.trim();
    if (mode === 'contact') return buildVCard(currentContactFieldValues());
    return '';
  }

  function drawLogo(canvas){
    if (!logoImage) return;
    const ctx = canvas.getContext('2d');
    const size = canvas.width;
    const logoSize = Math.round(size * 0.22);
    const pad = Math.round(logoSize * 0.16);
    const boxSize = logoSize + pad * 2;
    const x = (size - boxSize) / 2;
    const y = (size - boxSize) / 2;
    ctx.fillStyle = '#ffffff';
    const r = 8;
    ctx.beginPath();
    ctx.moveTo(x + r, y);
    ctx.arcTo(x + boxSize, y, x + boxSize, y + boxSize, r);
    ctx.arcTo(x + boxSize, y + boxSize, x, y + boxSize, r);
    ctx.arcTo(x, y + boxSize, x, y, r);
    ctx.arcTo(x, y, x + boxSize, y, r);
    ctx.closePath();
    ctx.fill();
    ctx.drawImage(logoImage, x + pad, y + pad, logoSize, logoSize);
  }

  function generate(){
    if (mode === 'text'){
      charCount.textContent = contentEl.value.length + ' / 1200';
      charCount.classList.toggle('warn', contentEl.value.length > 1000);
    }

    const text = getPayload();
    stage.innerHTML = '';

    if (!text){
      emptyState.style.display = 'block';
      stage.style.display = 'none';
      downloadBtn.disabled = true;
      return;
    }

    emptyState.style.display = 'none';
    stage.style.display = 'block';

    const size = parseInt(sizeEl.value, 10);
    new QRCode(stage, {
      text: text,
      width: size,
      height: size,
      colorDark: fgEl.value,
      colorLight: bgEl.value,
      correctLevel: ECL_MAP[eclEl.value]
    });

    const canvas = stage.querySelector('canvas');
    if (canvas) drawLogo(canvas);

    downloadBtn.disabled = false;
  }

  function scheduleGenerate(){
    clearTimeout(debounceTimer);
    debounceTimer = setTimeout(generate, 250);
  }

  contentEl.addEventListener('input', scheduleGenerate);
  Object.values(contactFields).forEach((el) => el.addEventListener('input', scheduleGenerate));
  sizeEl.addEventListener('change', generate);
  eclEl.addEventListener('change', generate);
  fgEl.addEventListener('input', scheduleGenerate);
  bgEl.addEventListener('input', scheduleGenerate);

  clearBtn.addEventListener('click', () => {
    if (mode === 'text'){
      contentEl.value = '';
      contentEl.focus();
    } else {
      Object.values(contactFields).forEach((el) => { el.value = ''; });
      contactFields.cFirst.focus();
    }
    generate();
  });

  logoInput.addEventListener('change', () => {
    const file = logoInput.files && logoInput.files[0];
    if (!file) return;
    const reader = new FileReader();
    reader.onload = (e) => {
      const img = new Image();
      img.onload = () => {
        logoImage = img;
        logoPreview.innerHTML = '';
        const previewImg = document.createElement('img');
        previewImg.src = e.target.result;
        logoPreview.appendChild(previewImg);
        removeLogoBtn.style.display = 'block';
        logoHint.style.display = 'block';
        eclBeforeLogo = eclEl.value;
        eclEl.value = 'H';
        eclEl.disabled = true;
        generate();
      };
      img.src = e.target.result;
    };
    reader.readAsDataURL(file);
  });

  removeLogoBtn.addEventListener('click', () => {
    logoImage = null;
    logoInput.value = '';
    logoPreview.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><path d="M21 15l-5-5L5 21"/></svg>';
    removeLogoBtn.style.display = 'none';
    logoHint.style.display = 'none';
    eclEl.disabled = false;
    eclEl.value = eclBeforeLogo;
    generate();
  });

  downloadBtn.addEventListener('click', () => {
    const canvas = stage.querySelector('canvas');
    if (!canvas) return;
    const link = document.createElement('a');
    const stamp = new Date().toISOString().slice(0,19).replace(/[:T]/g,'-');
    const prefix = mode === 'contact' ? 'contact-qr-' : 'qr-code-';
    link.download = prefix + stamp + '.png';
    link.href = canvas.toDataURL('image/png');
    link.click();
    showToast('Saved to your device');
    saveToHistory();
  });

  function saveToHistory(){
    const text = getPayload();
    if (!text) return;
    let label = '';
    if (mode === 'text'){
      label = contentEl.value.trim().slice(0, 60);
    } else {
      const f = currentContactFieldValues();
      label = [f.cFirst, f.cLast].filter(Boolean).join(' ') || f.cOrg || 'Contact';
    }
    const entry = {
      id: Date.now() + '-' + Math.random().toString(36).slice(2, 7),
      mode: mode,
      label: label,
      data: mode === 'contact' ? currentContactFieldValues() : { content: contentEl.value },
      ts: Date.now()
    };
    let history = [];
    try { history = JSON.parse(localStorage.getItem(HISTORY_KEY)) || []; } catch (e) { history = []; }
    history.unshift(entry);
    history = history.slice(0, HISTORY_MAX);
    try { localStorage.setItem(HISTORY_KEY, JSON.stringify(history)); } catch (e) {}
    renderHistory();
  }

  function loadHistory(){
    try { return JSON.parse(localStorage.getItem(HISTORY_KEY)) || []; } catch (e) { return []; }
  }

  function renderHistory(){
    const history = loadHistory();
    historyList.innerHTML = '';
    if (!history.length){
      historyList.innerHTML = '<div class="history-empty">Codes you download will show up here for quick reuse.</div>';
      return;
    }
    history.forEach((entry) => {
      const row = document.createElement('div');
      row.className = 'history-item';

      const typeTag = document.createElement('span');
      typeTag.className = 'htype';
      typeTag.textContent = entry.mode === 'contact' ? 'Contact' : 'Text';
      row.appendChild(typeTag);

      const labelSpan = document.createElement('span');
      labelSpan.className = 'hlabel';
      labelSpan.textContent = entry.label || '(untitled)';
      row.appendChild(labelSpan);

      const restoreBtn = document.createElement('button');
      restoreBtn.type = 'button';
      restoreBtn.title = 'Load this code';
      restoreBtn.innerHTML = '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="1 4 1 10 7 10"/><path d="M3.51 15a9 9 0 1 0 2.13-9.36L1 10"/></svg>';
      restoreBtn.addEventListener('click', () => restoreHistory(entry));
      row.appendChild(restoreBtn);

      const deleteBtn = document.createElement('button');
      deleteBtn.type = 'button';
      deleteBtn.title = 'Remove';
      deleteBtn.innerHTML = '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg>';
      deleteBtn.addEventListener('click', () => deleteHistoryItem(entry.id));
      row.appendChild(deleteBtn);

      historyList.appendChild(row);
    });
  }

  function restoreHistory(entry){
    if (entry.mode === 'contact'){
      setMode('contact');
      Object.keys(contactFields).forEach((key) => {
        contactFields[key].value = (entry.data && entry.data[key]) || '';
      });
    } else {
      setMode('text');
      contentEl.value = (entry.data && entry.data.content) || '';
    }
    generate();
    showToast('Code loaded');
  }

  function deleteHistoryItem(id){
    const history = loadHistory().filter((e) => e.id !== id);
    try { localStorage.setItem(HISTORY_KEY, JSON.stringify(history)); } catch (e) {}
    renderHistory();
  }

  clearHistoryBtn.addEventListener('click', () => {
    try { localStorage.removeItem(HISTORY_KEY); } catch (e) {}
    renderHistory();
  });

  function parseBatchLine(line){
    const pipeIndex = line.indexOf('|');
    if (pipeIndex > -1){
      const label = line.slice(0, pipeIndex).trim();
      const content = line.slice(pipeIndex + 1).trim();
      if (label && content) return { label, content };
    }
    return { label: line.trim(), content: line.trim() };
  }

  function generateBatch(){
    const lines = batchInput.value.split('\n').map((l) => l.trim()).filter(Boolean);
    batchGrid.innerHTML = '';
    if (!lines.length){
      batchOutput.style.display = 'none';
      return;
    }
    lines.forEach((line) => {
      const { label, content } = parseBatchLine(line);
      const cell = document.createElement('div');
      cell.className = 'batch-cell';
      const qrbox = document.createElement('div');
      qrbox.className = 'qrbox';
      cell.appendChild(qrbox);
      const caption = document.createElement('div');
      caption.className = 'caption';
      caption.textContent = label;
      cell.appendChild(caption);
      batchGrid.appendChild(cell);
      new QRCode(qrbox, {
        text: content,
        width: 100,
        height: 100,
        colorDark: '#12151C',
        colorLight: '#ffffff',
        correctLevel: QRCode.CorrectLevel.M
      });
    });
    batchOutput.style.display = 'block';
    showToast(lines.length + ' code' + (lines.length === 1 ? '' : 's') + ' generated');
  }

  generateBatchBtn.addEventListener('click', generateBatch);
  printBatchBtn.addEventListener('click', () => window.print());
  clearBatchBtn.addEventListener('click', () => {
    batchInput.value = '';
    batchGrid.innerHTML = '';
    batchOutput.style.display = 'none';
  });

  if ('serviceWorker' in navigator){
    window.addEventListener('load', () => {
      navigator.serviceWorker.register('sw.js').catch(() => {});
    });
  }

  renderHistory();
  generate();
})();
</script>
</body>
</html>
