<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bigman Holdings — Fixed Version</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@300;400;500;600;700&family=Space+Mono:wght@400;700&display=swap');
:root{--bg:#07080f;--surface:#0e0f1a;--surface2:#141523;--border:#252840;--gold:#c8973a;--gold2:#e8b84b;--gold-soft:rgba(200,151,58,.13);--text:#e6e8f2;--muted:#6b7280;--red:#ef4444;--green:#22c55e}
*{box-sizing:border-box;margin:0;padding:0}html,body{height:100%;overflow:hidden}body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text)}
#login-screen{position:fixed;inset:0;z-index:9999;background:radial-gradient(ellipse at 30% 50%,#1c1506 0%,#07080f 70%);display:flex;align-items:center;justify-content:center}
.lw{display:flex;gap:56px;align-items:center;max-width:920px;width:100%;padding:40px}
.lb-logo{font-family:'Playfair Display',serif;font-size:50px;font-weight:900;background:linear-gradient(135deg,var(--gold),var(--gold2));-webkit-background-clip:text;-webkit-text-fill-color:transparent;line-height:1;margin-bottom:6px}
.lb-sub{font-size:11px;color:var(--muted);letter-spacing:4px;text-transform:uppercase;margin-bottom:22px}
.lb-desc{font-size:13px;color:var(--muted);line-height:1.8;border-left:2px solid var(--gold);padding-left:14px;margin-bottom:22px}
.lb-divs{display:flex;flex-direction:column;gap:7px}.lb-div{display:flex;align-items:center;gap:9px;font-size:12px;color:var(--muted)}.lb-dot{width:6px;height:6px;border-radius:50%;flex-shrink:0}
.lbox{width:460px;background:var(--surface);border:1px solid var(--border);border-radius:18px;padding:32px;box-shadow:0 24px 80px rgba(0,0,0,.6)}
.lbox-t{font-size:18px;font-weight:700;margin-bottom:4px;font-family:'Playfair Display',serif}
.lg-field{margin-bottom:16px}.lg-label{display:block;font-size:11px;font-weight:700;color:var(--gold);text-transform:uppercase;letter-spacing:1px;margin-bottom:7px}
.lg-input{width:100%;padding:14px 16px;background:var(--surface2);border:2px solid var(--border);border-radius:8px;color:var(--text);font-size:15px;outline:none}
.lg-input:focus{border-color:var(--gold)}
.lg-btn{width:100%;padding:14px;border-radius:8px;background:linear-gradient(135deg,var(--gold),var(--gold2));border:none;color:#000;font-weight:700;cursor:pointer;font-size:16px;margin-top:4px}
.qk-btn{padding:8px 10px;background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.1);border-radius:8px;cursor:pointer;font-size:12px;font-weight:600;color:var(--text);transition:all .2s;display:flex;flex-direction:column;gap:2px}
.qk-btn:hover{border-color:var(--gold);color:var(--gold')}
.lerr{text-align:center;font-size:11px;color:var(--red);min-height:16px;margin-top:10px}
#app{display:none;flex-direction:column;height:100vh}
.topbar{height:52px;background:var(--surface);border-bottom:1px solid var(--border);display:flex;align-items:center;padding:0 16px}
.tb-logo{font-family:'Playfair Display',serif;font-size:17px;font-weight:900;color:var(--gold')}
.tb-nav{display:flex;gap:2px;margin-left:20px}
.tn{padding:5px 11px;border-radius:8px;border:none;background:transparent;color:var(--muted);cursor:pointer;font-size:12px}
.tn.active{background:var(--gold-soft);color:var(--gold')}
.tb-right{margin-left:auto;display:flex;align-items:center;gap:9px}
.tb-user{display:flex;align-items:center;gap:7px;padding:4px 9px;background:var(--surface2);border:1px solid var(--border);border-radius:8px;cursor:pointer}
.tb-av{width:22px;height:22px;border-radius:50%;background:linear-gradient(135deg,var(--gold),var(--gold2));display:flex;align-items:center;justify-content:center;font-size:9px;font-weight:700;color:#000}
.screen{display:none;flex:1;overflow-y:auto;padding:22px}
.screen.active{display:flex}
.card{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:16px}
.mo{position:fixed;inset:0;background:rgba(0,0,0,.78);display:flex;align-items:center;justify-content:center;z-index:2000;opacity:0;pointer-events:none}
.mo.open{opacity:1;pointer-events:all}
.md{background:var(--surface);border:1px solid var(--border);border-radius:18px;padding:26px;width:400px;transform:scale(.96)}
.mo.open .md{transform:scale(1)}
.mh{display:flex;justify-content:space-between;margin-bottom:20px}
.mc{background:none;border:none;color:var(--muted);cursor:pointer;font-size:18px}
.btn{padding:7px 14px;border-radius:8px;border:none;cursor:pointer;font-weight:600}
.btn-g{background:linear-gradient(135deg,var(--gold),var(--gold2));color:#000}
.btn-o{background:transparent;border:1px solid var(--border);color:var(--muted')}
.flex{display:flex}.g2{gap:8px}.f1{flex:1}
</style>
</head>
<body>

<div id="login-screen">
  <div class="lw">
    <div style="flex:1">
      <div class="lb-logo">BIGMAN<br>HOLDINGS</div>
      <div class="lb-sub">Enterprise Management System</div>
      <div class="lb-desc">Built exclusively for Sebastian Mwakalobo — CEO<br>Complete management for all five divisions.</div>
    </div>
    <div class="lbox">
      <div class="lbox-t">Welcome Back</div>
      <div style="font-size:12px;color:var(--muted);margin-bottom:22px">Sign in to access the dashboard</div>

      <div class="lg-field">
        <label class="lg-label">Your Name</label>
        <input type="text" id="login-name" class="lg-input" placeholder="e.g. Sebastian" autocomplete="off">
      </div>

      <div class="lg-field">
        <label class="lg-label">PIN</label>
        <input type="password" id="login-pin" class="lg-input" placeholder="Enter 4-digit PIN" maxlength="4" inputmode="numeric">
      </div>

      <button class="lg-btn" onclick="doLogin()">Sign In →</button>
      <div class="lerr" id="lerr"></div>

      <div style="margin-top:20px;padding-top:16px;border-top:1px solid var(--border)">
        <div style="font-size:10px;color:var(--muted);margin-bottom:8px">QUICK LOGIN</div>
        <div style="display:grid;grid-template-columns:1fr 1fr;gap:6px">
          <div class="qk-btn" onclick="quickFill('Sebastian Mwakalobo','1234')">Sebastian <span>Admin</span></div>
          <div class="qk-btn" onclick="quickFill('Amina Rajabu','2222')">Amina <span>Manager</span></div>
          <div class="qk-btn" onclick="quickFill('Joseph Cashier','7777')">Joseph <span>Cashier</span></div>
          <div class="qk-btn" onclick="quickFill('Mary Bookkeeper','8888')">Mary <span>Accounts</span></div>
        </div>
      </div>
    </div>
  </div>
</div>

<div id="app">
  <div class="topbar">
    <div class="tb-logo">BIGMAN</div>
    <div class="tb-nav">
       <button class="tn active" onclick="showScreen('dash')">Dashboard</button>
       <button class="tn" onclick="showScreen('staff')">Staff</button>
    </div>
    <div class="tb-right">
       <div class="tb-user" onclick="openModal('m-logout')">
         <div class="tb-av" id="av">S</div>
         <div><div id="nm" style="font-size:11px;font-weight:600">User</div></div>
       </div>
    </div>
  </div>
  
  <div class="screen active" id="s-dash">
     <h1 style="font-size:22px;margin-bottom:10px">Dashboard</h1>
     <p style="color:var(--muted)">Welcome to Bigman Holdings. The system is now active.</p>
     <div style="margin-top:20px" class="card">
        <div style="font-size:11px;color:var(--muted);text-transform:uppercase;margin-bottom:5px">Total Staff</div>
        <div style="font-size:24px;font-weight:700;color:var(--gold)" id="staff-count">0</div>
     </div>
  </div>
  
  <div class="screen" id="s-staff">
     <h1 style="font-size:22px;margin-bottom:10px">Staff List</h1>
     <div id="staff-list"></div>
  </div>
</div>

<!-- Logout Modal -->
<div class="mo" id="m-logout">
  <div class="md">
    <div class="mh">
      <div style="font-size:19px;font-weight:700">User Menu</div>
      <button class="mc" onclick="closeModal('m-logout')">✕</button>
    </div>
    <div style="text-align:center;margin-bottom:20px">
       <div class="tb-av" style="width:50px;height:50px;margin:0 auto 10px;font-size:20px" id="av-big">S</div>
       <div id="nm-big" style="font-weight:700">User</div>
    </div>
    <button class="btn btn-g" style="width:100%" onclick="doLogout()">🚪 Logout</button>
  </div>
</div>

<script>
// ==========================================================
// BIGMAN HOLDINGS - FIXED LOGIN LOGIC
// ==========================================================

// 1. DEFAULT DATA (HARDCODED)
const DEF_EMP = [
  {id:'e1', name:'Sebastian Mwakalobo', pin:'1234', role:'Admin'},
  {id:'e2', name:'Amina Rajabu', pin:'2222', role:'Manager'},
  {id:'e3', name:'Hassan Mwamba', pin:'3333', role:'Manager'},
  {id:'e4', name:'Grace Kimani', pin:'4444', role:'Manager'},
  {id:'e5', name:'Peter Mushi', pin:'5555', role:'Manager'},
  {id:'e6', name:'Fatuma Ally', pin:'6666', role:'Manager'},
  {id:'e7', name:'Joseph Cashier', pin:'7777', role:'Cashier'},
  {id:'e8', name:'Mary Bookkeeper', pin:'8888', role:'Accountant'}
];

// 2. STORAGE KEY CHANGED TO FORCE RESET
const KEY = 'bigman_v4_final'; 

let DB = { emp: [] };
let CU = null;

// 3. LOAD OR INIT DATABASE
function initDB(){
  const stored = localStorage.getItem(KEY);
  if(stored){
     try {
       const parsed = JSON.parse(stored);
       // If valid data
       if(parsed.emp && parsed.emp.length > 0) {
          DB = parsed;
          console.log("Database loaded from storage.");
          return;
       }
     } catch(e) { console.log("Error parsing, resetting."); }
  }
  
  // If we are here, data is missing or corrupt. FORCE RESET.
  console.log("Initializing fresh database...");
  DB.emp = JSON.parse(JSON.stringify(DEF_EMP));
  saveDB();
}

function saveDB(){
   localStorage.setItem(KEY, JSON.stringify(DB));
}

// 4. LOGIN LOGIC
function quickFill(name, pin){
   document.getElementById('login-name').value = name;
   document.getElementById('login-pin').value = pin;
   document.getElementById('lerr').innerText = '';
}

function doLogin(){
   const nameVal = document.getElementById('login-name').value.trim().toLowerCase();
   const pinVal  = document.getElementById('login-pin').value.trim();
   
   if(!nameVal || !pinVal){
       document.getElementById('lerr').innerText = "Please enter name and PIN.";
       return;
   }

   // Find user (Flexible matching)
   const emp = DB.emp.find(e => {
       const en = e.name.toLowerCase();
       // Match full name OR first name OR last name
       return en === nameVal || en.split(' ')[0] === nameVal || en.includes(nameVal);
   });

   if(!emp){
       document.getElementById('lerr').innerText = "Name not found. Try 'Sebastian'";
       return;
   }

   if(emp.pin !== pinVal){
       document.getElementById('lerr').innerText = "Wrong PIN.";
       return;
   }

   // SUCCESS
   CU = emp;
   document.getElementById('login-screen').style.display = 'none';
   document.getElementById('app').style.display = 'flex';
   
   // Update UI
   document.getElementById('av').innerText = CU.name.charAt(0);
   document.getElementById('nm').innerText = CU.name;
   document.getElementById('av-big').innerText = CU.name.charAt(0);
   document.getElementById('nm-big').innerText = CU.name;
   
   renderDash();
}

function doLogout(){
   CU = null;
   document.getElementById('app').style.display = 'none';
   document.getElementById('login-screen').style.display = 'flex';
   closeModal('m-logout');
   document.getElementById('login-pin').value = '';
}

// 5. UI HELPERS
function openModal(id){ document.getElementById(id).classList.add('open'); }
function closeModal(id){ document.getElementById(id).classList.remove('open'); }
function showScreen(id){ 
   document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
   document.getElementById('s-'+id).classList.add('active');
   document.querySelectorAll('.tn').forEach(b => b.classList.remove('active'));
   event.target.classList.add('active');
}

function renderDash(){
   document.getElementById('staff-count').innerText = DB.emp.length;
   let html = '<div style="display:grid;grid-template-columns:1fr 1fr;gap:10px">';
   DB.emp.forEach(e => {
      html += `<div class="card" style="padding:10px">
         <div style="font-weight:700">${e.name}</div>
         <div style="font-size:11px;color:var(--muted)">${e.role}</div>
      </div>`;
   });
   html += '</div>';
   document.getElementById('staff-list').innerHTML = html;
}

// 6. START APP
initDB();

</script>
</body>
</html>
