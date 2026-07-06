<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no, viewport-fit=cover">
<meta name="theme-color" content="#0F1412">
<title>Ledger</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=IBM+Plex+Mono:wght@400;500&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0F1412;
    --surface:#171E1A;
    --surface-2:#1F2924;
    --text:#EDEFEA;
    --muted:#8A9691;
    --divider:#2A342E;
    --save:#4FBA82;
    --save-dim:#2E4B3B;
    --spend:#C4674A;
    --spend-dim:#4A2E27;
  }
  *{box-sizing:border-box; -webkit-tap-highlight-color:transparent;}
  html,body{margin:0; height:100%; background:var(--bg); color:var(--text); font-family:'Inter',sans-serif; overflow:hidden;}
  #app{height:100vh; height:100dvh; display:flex; flex-direction:column; max-width:480px; margin:0 auto; position:relative;}

  .screen{position:absolute; inset:0; display:flex; flex-direction:column; opacity:0; pointer-events:none; transition:opacity .22s ease; padding:env(safe-area-inset-top) 0 env(safe-area-inset-bottom) 0;}
  .screen.active{opacity:1; pointer-events:auto;}

  /* ---------- HOME ---------- */
  #home{justify-content:center; gap:16px; padding:24px;}
  .home-title{font-family:'Fraunces',serif; font-size:22px; font-weight:500; color:var(--muted); text-align:left; margin:0 4px 8px; letter-spacing:.2px;}
  .panel{
    background:var(--surface); border:1px solid var(--divider); border-radius:20px;
    padding:26px 22px; display:flex; flex-direction:column; gap:6px;
    cursor:pointer; transition:border-color .15s, transform .1s;
  }
  .panel:active{transform:scale(.98);}
  .panel-label{font-size:14px; color:var(--muted); text-transform:uppercase; letter-spacing:1.5px;}
  .panel-amount{font-family:'Fraunces',serif; font-size:36px; font-weight:500;}
  #panel-card{border-color:var(--spend-dim);}
  #panel-saved{border-color:var(--save-dim);}
  #panel-card .panel-amount{color:var(--text);}
  #panel-saved .panel-amount{color:var(--save);}

  /* ---------- SUBPAGE HEADER ---------- */
  .topbar{display:flex; align-items:center; justify-content:space-between; padding:18px 20px 6px;}
  .back{font-size:22px; color:var(--muted); background:none; border:none; padding:6px; cursor:pointer;}
  .topbar-title{font-size:13px; letter-spacing:2px; text-transform:uppercase; color:var(--muted);}
  .gear{font-size:18px; color:var(--muted); background:none; border:none; padding:6px; cursor:pointer;}

  .balance-block{text-align:center; padding:18px 20px 10px;}
  .balance-caption{font-size:12px; color:var(--muted); text-transform:uppercase; letter-spacing:1.5px; margin-bottom:6px;}
  .balance-number{font-family:'Fraunces',serif; font-size:52px; font-weight:500; line-height:1; display:inline-flex; align-items:baseline; gap:6px;}
  .balance-input{
    font-family:'Fraunces',serif; font-size:52px; font-weight:500; background:none; border:none; color:var(--save);
    text-align:center; width:220px; outline:none; border-bottom:1px solid var(--save);
  }
  #card-balance{color:var(--text);}
  #saved-balance{color:var(--save);}

  .edit-pencil{font-size:14px; color:var(--muted); margin-left:6px; cursor:pointer; vertical-align:middle;}

  /* ---------- AUTO SETTINGS ---------- */
  .auto-panel{
    margin:6px 20px 0; background:var(--surface); border:1px solid var(--divider); border-radius:14px;
    padding:0; overflow:hidden; max-height:0; transition:max-height .25s ease;
  }
  .auto-panel.open{max-height:220px;}
  .auto-panel-inner{padding:16px 18px;}
  .row{display:flex; align-items:center; justify-content:space-between; margin-bottom:12px;}
  .row:last-child{margin-bottom:0;}
  .row label{font-size:13px; color:var(--muted);}
  .row input[type=number]{
    background:var(--surface-2); border:1px solid var(--divider); border-radius:8px; color:var(--text);
    font-family:'IBM Plex Mono',monospace; font-size:15px; padding:8px 10px; width:110px; text-align:right; outline:none;
  }
  .switch{position:relative; width:42px; height:24px; background:var(--surface-2); border-radius:20px; border:1px solid var(--divider); cursor:pointer; transition:background .15s;}
  .switch.on{background:var(--save-dim); border-color:var(--save);}
  .switch::after{content:''; position:absolute; top:2px; left:2px; width:18px; height:18px; border-radius:50%; background:var(--muted); transition:transform .15s, background .15s;}
  .switch.on::after{transform:translateX(18px); background:var(--save);}
  .auto-hint{font-size:11px; color:var(--muted); margin-top:2px; line-height:1.4;}

  /* ---------- LEDGER (expenses) ---------- */
  .ledger-wrap{flex:1; overflow-y:auto; margin-top:10px; padding:0 20px 90px;}
  .ledger-caption{font-size:12px; color:var(--muted); text-transform:uppercase; letter-spacing:1.5px; margin:14px 0 8px;}
  .ledger{background:var(--surface); border:1px solid var(--divider); border-radius:16px; overflow:hidden;}
  .ledger-empty{padding:26px 18px; text-align:center; color:var(--muted); font-size:13px;}
  .ledger-row{display:flex; align-items:center; justify-content:space-between; padding:14px 16px; border-bottom:1px dashed var(--divider);}
  .ledger-row:last-child{border-bottom:none;}
  .ledger-name{font-size:14px;}
  .ledger-date{font-size:11px; color:var(--muted); margin-top:2px;}
  .ledger-amount{font-family:'IBM Plex Mono',monospace; font-size:15px; color:var(--spend);}
  .ledger-del{background:none; border:none; color:var(--muted); font-size:16px; padding:0 0 0 12px; cursor:pointer;}

  /* ---------- ADD BAR ---------- */
  .add-bar{position:absolute; bottom:0; left:0; right:0; padding:12px 20px calc(16px + env(safe-area-inset-bottom)); background:linear-gradient(to top, var(--bg) 60%, transparent);}
  .add-btn{
    width:100%; padding:14px; border-radius:14px; border:none; background:var(--text); color:var(--bg);
    font-family:'Inter',sans-serif; font-weight:600; font-size:15px; cursor:pointer;
  }
  .add-btn:active{opacity:.85;}

  /* ---------- MODAL ---------- */
  .modal-backdrop{position:fixed; inset:0; background:rgba(0,0,0,.55); display:none; align-items:flex-end; justify-content:center; z-index:20;}
  .modal-backdrop.show{display:flex;}
  .modal{width:100%; max-width:480px; background:var(--surface); border-radius:20px 20px 0 0; padding:22px 20px calc(22px + env(safe-area-inset-bottom));}
  .modal-title{font-family:'Fraunces',serif; font-size:19px; margin:0 0 16px;}
  .field{margin-bottom:14px;}
  .field label{display:block; font-size:12px; color:var(--muted); text-transform:uppercase; letter-spacing:1px; margin-bottom:6px;}
  .field input{width:100%; background:var(--surface-2); border:1px solid var(--divider); border-radius:10px; color:var(--text); font-family:'Inter',sans-serif; font-size:15px; padding:12px; outline:none;}
  .field input[type=number]{font-family:'IBM Plex Mono',monospace;}
  .modal-actions{display:flex; gap:10px; margin-top:6px;}
  .modal-actions button{flex:1; padding:13px; border-radius:12px; border:none; font-weight:600; font-size:14px; cursor:pointer;}
  .btn-cancel{background:var(--surface-2); color:var(--muted);}
  .btn-confirm{background:var(--spend); color:#1a1a1a;}
  #saved-edit-confirm{background:var(--save);}

  .cat-grid{display:flex; flex-wrap:wrap; gap:8px;}
  .cat-chip{
    display:flex; align-items:center; gap:6px; background:var(--surface-2); border:1px solid var(--divider);
    border-radius:20px; padding:8px 12px; font-size:13px; color:var(--text); cursor:pointer; transition:border-color .15s, background .15s;
  }
  .cat-chip .cat-icon{font-size:15px; line-height:1;}
  .cat-chip.selected{background:var(--spend-dim); border-color:var(--spend); color:var(--text);}
  .ledger-icon{margin-right:8px; font-size:15px;}

  ::-webkit-scrollbar{display:none;}
</style>
</head>
<body>
<div id="app">

  <!-- HOME -->
  <div class="screen active" id="home">
    <div class="home-title">Overview</div>
    <div class="panel" id="panel-card" onclick="go('card')">
      <div class="panel-label">Card</div>
      <div class="panel-amount" id="home-card-amt">0 DZD</div>
    </div>
    <div class="panel" id="panel-saved" onclick="go('saved')">
      <div class="panel-label">Saved</div>
      <div class="panel-amount" id="home-saved-amt">0 DZD</div>
    </div>
  </div>

  <!-- CARD SCREEN -->
  <div class="screen" id="card">
    <div class="topbar">
      <button class="back" onclick="go('home')">‹</button>
      <div class="topbar-title">Card</div>
      <button class="gear" onclick="toggleAuto('card')">⚙</button>
    </div>
    <div class="balance-block">
      <div class="balance-caption">Left after expenses</div>
      <div class="balance-number" id="card-balance">0 DZD</div>
    </div>
    <div class="auto-panel" id="card-auto-panel">
      <div class="auto-panel-inner">
        <div class="row">
          <label>Auto-add monthly income</label>
          <div class="switch" id="card-auto-switch" onclick="flipSwitch('card')"></div>
        </div>
        <div class="row">
          <label>Amount</label>
          <input type="number" id="card-auto-amount" placeholder="0" inputmode="decimal">
        </div>
        <div class="row">
          <label>Day of month</label>
          <input type="number" id="card-auto-day" placeholder="1" min="1" max="31" inputmode="numeric" style="width:70px;">
        </div>
        <div class="row" style="margin-bottom:4px;">
          <button class="add-btn" style="padding:10px; font-size:13px;" onclick="saveAuto('card')">Save</button>
        </div>
        <div class="auto-hint">Added once per calendar month, on or after the day you set above, the first time you open the app that month.</div>
      </div>
    </div>
    <div class="ledger-wrap">
      <div class="ledger-caption">Expenses</div>
      <div class="ledger" id="expense-list"></div>
    </div>
    <div class="add-bar" style="display:flex; gap:10px;">
      <button class="add-btn" style="flex:1; background:var(--save); color:#0F1412;" onclick="openModal('income')">Add amount</button>
      <button class="add-btn" style="flex:1;" onclick="openModal('expense')">Add expense</button>
    </div>
  </div>

  <!-- SAVED SCREEN -->
  <div class="screen" id="saved">
    <div class="topbar">
      <button class="back" onclick="go('home')">‹</button>
      <div class="topbar-title">Saved</div>
      <button class="gear" onclick="toggleAuto('saved')">⚙</button>
    </div>
    <div class="balance-block">
      <div class="balance-caption">Total saved</div>
      <div id="saved-display">
        <span class="balance-number" id="saved-balance">0 DZD</span>
        <span class="edit-pencil" onclick="startEditSaved()">✎</span>
      </div>
    </div>
    <div class="auto-panel" id="saved-auto-panel">
      <div class="auto-panel-inner">
        <div class="row">
          <label>Auto-add monthly</label>
          <div class="switch" id="saved-auto-switch" onclick="flipSwitch('saved')"></div>
        </div>
        <div class="row">
          <label>Amount</label>
          <input type="number" id="saved-auto-amount" placeholder="0" inputmode="decimal">
        </div>
        <div class="row">
          <label>Day of month</label>
          <input type="number" id="saved-auto-day" placeholder="1" min="1" max="31" inputmode="numeric" style="width:70px;">
        </div>
        <div class="row" style="margin-bottom:4px;">
          <button class="add-btn" style="padding:10px; font-size:13px;" onclick="saveAuto('saved')">Save</button>
        </div>
        <div class="auto-hint">Added once per calendar month, on or after the day you set above, the first time you open the app that month.</div>
      </div>
    </div>
  </div>

</div>

<!-- ADD EXPENSE MODAL -->
<div class="modal-backdrop" id="modal-backdrop">
  <div class="modal">
    <div class="modal-title" id="modal-title">Add expense</div>
    <div class="field" id="exp-category-field">
      <label>Category</label>
      <div class="cat-grid" id="exp-category-grid"></div>
    </div>
    <div class="field" id="exp-name-field"><label>Name</label><input type="text" id="exp-name" placeholder="Groceries"></div>
    <div class="field"><label>Amount</label><input type="number" id="exp-amount" placeholder="0" inputmode="decimal"></div>
    <div class="modal-actions">
      <button class="btn-cancel" onclick="closeModal()">Cancel</button>
      <button class="btn-confirm" id="modal-confirm-btn" onclick="confirmModal()">Add</button>
    </div>
  </div>
</div>

<script>
const KEY = 'ledgerAppData';

function defaultData(){
  return {
    card:{ balance:0, income:{ amount:0, enabled:false, lastApplied:null, day:1 }, expenses:[] },
    saved:{ balance:0, auto:{ amount:0, enabled:false, lastApplied:null, day:1 } }
  };
}

function load(){
  try{
    const raw = localStorage.getItem(KEY);
    if(!raw) return defaultData();
    const d = JSON.parse(raw);
    const def = defaultData();
    return {
      ...def, ...d,
      card:{ ...def.card, ...d.card, income:{ ...def.card.income, ...(d.card && d.card.income) } },
      saved:{ ...def.saved, ...d.saved, auto:{ ...def.saved.auto, ...(d.saved && d.saved.auto) } }
    };
  }catch(e){ return defaultData(); }
}
function save(){ localStorage.setItem(KEY, JSON.stringify(state)); }

let state = load();

function currentMonthKey(){
  const n = new Date();
  return n.getFullYear()+'-'+String(n.getMonth()+1).padStart(2,'0');
}

function daysInMonth(y,m){ return new Date(y, m+1, 0).getDate(); }

function applyAutomations(){
  const now = new Date();
  const mk = currentMonthKey();
  const today = now.getDate();
  const dim = daysInMonth(now.getFullYear(), now.getMonth());

  const cardDay = Math.min(Math.max(state.card.income.day || 1, 1), dim);
  if(state.card.income.enabled && state.card.income.lastApplied !== mk && state.card.income.amount > 0 && today >= cardDay){
    state.card.balance += Number(state.card.income.amount);
    state.card.income.lastApplied = mk;
  }
  const savedDay = Math.min(Math.max(state.saved.auto.day || 1, 1), dim);
  if(state.saved.auto.enabled && state.saved.auto.lastApplied !== mk && state.saved.auto.amount > 0 && today >= savedDay){
    state.saved.balance += Number(state.saved.auto.amount);
    state.saved.auto.lastApplied = mk;
  }
  save();
}

function fmt(n){
  const v = Number(n)||0;
  return v.toLocaleString(undefined,{minimumFractionDigits: v%1===0?0:2, maximumFractionDigits:2}) + ' DZD';
}

function render(){
  document.getElementById('home-card-amt').textContent = fmt(state.card.balance);
  document.getElementById('home-saved-amt').textContent = fmt(state.saved.balance);
  document.getElementById('card-balance').textContent = fmt(state.card.balance);
  document.getElementById('saved-balance').textContent = fmt(state.saved.balance);

  document.getElementById('card-auto-switch').classList.toggle('on', state.card.income.enabled);
  document.getElementById('card-auto-amount').value = state.card.income.amount || '';
  document.getElementById('card-auto-day').value = state.card.income.day || 1;
  document.getElementById('saved-auto-switch').classList.toggle('on', state.saved.auto.enabled);
  document.getElementById('saved-auto-amount').value = state.saved.auto.amount || '';
  document.getElementById('saved-auto-day').value = state.saved.auto.day || 1;

  const list = document.getElementById('expense-list');
  if(state.card.expenses.length === 0){
    list.innerHTML = '<div class="ledger-empty">No expenses yet.</div>';
  } else {
    list.innerHTML = state.card.expenses.slice().reverse().map(e => `
      <div class="ledger-row">
        <div>
          <div class="ledger-name"><span class="ledger-icon">${e.icon || '📦'}</span>${escapeHtml(e.name)}</div>
          <div class="ledger-date">${e.date}</div>
        </div>
        <div style="display:flex; align-items:center;">
          <div class="ledger-amount">-${fmt(e.amount)}</div>
          <button class="ledger-del" onclick="deleteExpense('${e.id}')">✕</button>
        </div>
      </div>
    `).join('');
  }
}

function escapeHtml(s){
  const d = document.createElement('div'); d.textContent = s; return d.innerHTML;
}

function go(screen){
  document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
  document.getElementById(screen).classList.add('active');
}

function toggleAuto(which){
  const panel = document.getElementById(which+'-auto-panel');
  panel.classList.toggle('open');
}
function flipSwitch(which){
  const el = document.getElementById(which+'-auto-switch');
  el.classList.toggle('on');
}
function saveAuto(which){
  const enabled = document.getElementById(which+'-auto-switch').classList.contains('on');
  const amountEl = document.getElementById(which+'-auto-amount');
  const amount = parseFloat(amountEl.value) || 0;
  const dayEl = document.getElementById(which+'-auto-day');
  const day = Math.min(31, Math.max(1, parseInt(dayEl.value) || 1));
  if(which === 'card'){
    state.card.income.enabled = enabled;
    state.card.income.amount = amount;
    state.card.income.day = day;
  } else {
    state.saved.auto.enabled = enabled;
    state.saved.auto.amount = amount;
    state.saved.auto.day = day;
  }
  save(); render();
  document.getElementById(which+'-auto-panel').classList.remove('open');
}

const CATEGORIES = [
  { icon:'🛒', label:'Groceries' },
  { icon:'🍽️', label:'Dining' },
  { icon:'🚗', label:'Transport' },
  { icon:'🧾', label:'Bills' },
  { icon:'🏠', label:'Rent' },
  { icon:'🛍️', label:'Shopping' },
  { icon:'🏥', label:'Health' },
  { icon:'🎬', label:'Entertainment' },
  { icon:'📶', label:'Phone/Internet' },
  { icon:'✈️', label:'Travel' },
  { icon:'🎁', label:'Gift' },
  { icon:'📦', label:'Other' }
];
let selectedCategory = null;

function renderCategoryGrid(){
  const grid = document.getElementById('exp-category-grid');
  grid.innerHTML = CATEGORIES.map(c => `
    <div class="cat-chip" data-label="${c.label}" onclick="pickCategory('${c.icon}','${c.label}')">
      <span class="cat-icon">${c.icon}</span><span>${c.label}</span>
    </div>
  `).join('');
}
function pickCategory(icon, label){
  selectedCategory = icon;
  document.getElementById('exp-name').value = label;
  document.querySelectorAll('#exp-category-grid .cat-chip').forEach(chip => {
    chip.classList.toggle('selected', chip.getAttribute('data-label') === label);
  });
}

let modalMode = 'expense';
function openModal(mode){
  modalMode = mode;
  selectedCategory = null;
  document.getElementById('exp-name').value = '';
  document.getElementById('exp-amount').value = '';
  const nameField = document.getElementById('exp-name-field');
  const catField = document.getElementById('exp-category-field');
  const title = document.getElementById('modal-title');
  const confirmBtn = document.getElementById('modal-confirm-btn');
  if(mode === 'income'){
    nameField.style.display = 'none';
    catField.style.display = 'none';
    title.textContent = 'Add amount';
    confirmBtn.style.background = 'var(--save)';
    confirmBtn.style.color = '#0F1412';
  } else {
    nameField.style.display = '';
    catField.style.display = '';
    renderCategoryGrid();
    title.textContent = 'Add expense';
    confirmBtn.style.background = 'var(--spend)';
    confirmBtn.style.color = '#1a1a1a';
  }
  document.getElementById('modal-backdrop').classList.add('show');
}
function closeModal(){ document.getElementById('modal-backdrop').classList.remove('show'); }
function confirmModal(){
  const amount = parseFloat(document.getElementById('exp-amount').value) || 0;
  if(amount <= 0){ closeModal(); return; }
  if(modalMode === 'income'){
    state.card.balance += amount;
  } else {
    const name = document.getElementById('exp-name').value.trim() || 'Expense';
    const icon = selectedCategory || '📦';
    const today = new Date();
    const dateStr = t
