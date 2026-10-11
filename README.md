<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ILM Academy — 21st Century Instructional Leadership</title>
<style>
:root{
  --primary:#1a365d;--primary-light:#2b6cb0;--accent:#ed8936;
  --success:#38a169;--danger:#e53e3e;--gold:#d69e2e;--purple:#6b46c1;
  --text:#2d3748;--text-light:#718096;--bg:#f7fafc;--white:#fff;
  --border:#e2e8f0;--shadow:0 4px 6px rgba(0,0,0,.07);
  --shadow-lg:0 10px 25px rgba(0,0,0,.1);--radius:12px;--radius-sm:6px;
}
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,sans-serif;
  color:var(--text);background:var(--bg);line-height:1.6;-webkit-font-smoothing:antialiased}
a{color:var(--primary-light);text-decoration:none;cursor:pointer}
a:hover{text-decoration:underline}
.hidden{display:none!important}
.btn{display:inline-block;padding:14px 28px;border-radius:var(--radius-sm);
  font-weight:600;font-size:15px;cursor:pointer;transition:all .2s;border:none;
  text-align:center;font-family:inherit;background:var(--primary-light);color:#fff}
.btn:hover{background:var(--primary);transform:translateY(-2px);box-shadow:var(--shadow-lg)}
.btn-secondary{background:var(--accent)}
.btn-secondary:hover{background:#dd6b20}
.btn-outline{background:transparent;border:2px solid var(--primary-light);color:var(--primary-light)}
.btn-outline:hover{background:var(--primary-light);color:#fff}
.btn-gold{background:var(--gold)}
.btn-gold:hover{background:#b7791f}
.btn-success{background:var(--success)}
.btn-danger{background:var(--danger)}
.btn-full{width:100%}
.btn-sm{padding:6px 12px;font-size:13px;border-radius:4px}
.btn-row{display:flex;gap:8px;flex-wrap:wrap}

.topnav{background:#fff;box-shadow:var(--shadow);position:sticky;top:0;z-index:100}
.topnav-inner{display:flex;justify-content:space-between;align-items:center;
  padding:16px 20px;max-width:1200px;margin:0 auto;flex-wrap:wrap;gap:12px}
.logo{font-size:22px;font-weight:700;color:var(--primary);cursor:pointer;white-space:nowrap}
.nav-links{display:flex;gap:18px;align-items:center;flex-wrap:wrap;font-size:14px}
.nav-links a{color:var(--text);font-weight:500}
.nav-links a:hover{color:var(--primary-light);text-decoration:none}
.nav-links a.active{color:var(--primary-light);font-weight:700}

.hero{background:linear-gradient(135deg,var(--primary) 0%,var(--primary-light) 100%);
  color:#fff;padding:70px 20px;text-align:center;position:relative;overflow:hidden}
.hero h1{font-size:clamp(28px,5vw,46px);line-height:1.15;margin-bottom:18px;font-weight:700}
.hero .subtitle{font-size:17px;opacity:.92;margin-bottom:32px;max-width:720px;
  margin-left:auto;margin-right:auto}
.hero-badge{display:inline-block;background:rgba(255,255,255,.15);padding:8px 18px;
  border-radius:20px;font-size:13px;font-weight:600;margin-bottom:20px;
  border:1px solid rgba(255,255,255,.3)}
.trust-badges{display:flex;gap:22px;justify-content:center;flex-wrap:wrap;
  font-size:13px;opacity:.9;margin-top:28px}

section{padding:56px 20px}
section h2{text-align:center;font-size:30px;margin-bottom:14px;color:var(--primary)}
.section-sub{text-align:center;color:var(--text-light);max-width:660px;
  margin:0 auto 36px;font-size:15px}
.container{max-width:1100px;margin:0 auto}

.grid{display:grid;gap:22px}
.grid-2{grid-template-columns:repeat(auto-fit,minmax(280px,1fr))}
.grid-3{grid-template-columns:repeat(auto-fit,minmax(260px,1fr))}
.grid-4{grid-template-columns:repeat(auto-fit,minmax(220px,1fr))}

.card{background:#fff;padding:26px;border-radius:var(--radius);
  box-shadow:var(--shadow);transition:transform .2s,box-shadow .2s}
.card:hover{transform:translateY(-3px);box-shadow:var(--shadow-lg)}
.card h3{font-size:17px;margin-bottom:10px;color:var(--primary)}
.card p{color:var(--text-light);font-size:14px}

.pillar-diagram{background:#fff;padding:36px 20px;border-radius:var(--radius);
  box-shadow:var(--shadow);margin-bottom:36px;text-align:center}
.pillar-core{display:inline-block;background:var(--primary);color:#fff;
  padding:14px 28px;border-radius:10px;font-weight:700;font-size:15px;margin-bottom:24px}
.pillar-arrow{font-size:20px;color:var(--primary-light);margin-bottom:16px}
.pillar-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
  gap:16px;max-width:900px;margin:0 auto}
.pillar-box{background:linear-gradient(135deg,#ebf8ff 0%,#e6fffa 100%);
  border:2px solid var(--primary-light);border-radius:10px;padding:18px 14px;
  transition:transform .2s}
.pillar-box:hover{transform:translateY(-4px)}
.pillar-box .p-icon{font-size:32px;display:block;margin-bottom:8px}
.pillar-box h4{font-size:14px;color:var(--primary);font-weight:700}
.pillar-box p{font-size:12px;color:var(--text-light);margin-top:6px}

.problem-card{text-align:center}
.problem-card .icon{font-size:36px;margin-bottom:12px;display:block}

.module-num{font-size:40px;font-weight:700;color:var(--border);line-height:1;margin-bottom:8px}
.module-card ul{list-style:none;margin-top:14px}
.module-card ul li{padding:5px 0 5px 22px;position:relative;font-size:14px;color:var(--text)}
.module-card ul li::before{content:'✓';position:absolute;left:0;color:var(--success);font-weight:700}

.pricing-card{text-align:center;display:flex;flex-direction:column;position:relative}
.pricing-card.featured{border:3px solid var(--accent);transform:scale(1.02)}
.pricing-badge{position:absolute;top:-14px;left:50%;transform:translateX(-50%);
  background:var(--accent);color:#fff;padding:6px 16px;border-radius:20px;
  font-size:12px;font-weight:700;text-transform:uppercase;white-space:nowrap}
.price{font-size:36px;font-weight:700;color:var(--primary);margin:14px 0}
.pricing-card ul{list-style:none;text-align:left;margin:16px 0 24px;flex-grow:1}
.pricing-card ul li{padding:8px 0;border-bottom:1px solid var(--border);font-size:14px}
.pricing-card ul li:last-child{border-bottom:none}

.form-group{margin-bottom:18px}
.form-group label{display:block;margin-bottom:6px;font-weight:600;font-size:14px}
.form-group input,.form-group select,.form-group textarea{
  width:100%;padding:12px 16px;border:1px solid var(--border);
  border-radius:var(--radius-sm);font-size:15px;font-family:inherit;background:#fff}
.form-group input:focus,.form-group textarea:focus{outline:none;
  border-color:var(--primary-light);box-shadow:0 0 0 3px rgba(43,108,176,.1)}
.form-group textarea{min-height:100px;resize:vertical}
.form-group small{color:var(--text-light);font-size:12px;display:block;margin-top:4px}

.auth-page{min-height:calc(100vh - 70px);display:flex;align-items:center;
  justify-content:center;padding:40px 20px;
  background:linear-gradient(135deg,var(--primary) 0%,var(--primary-light) 100%)}
.auth-card{background:#fff;padding:44px 36px;border-radius:var(--radius);
  box-shadow:var(--shadow-lg);max-width:440px;width:100%}
.auth-card h1{font-size:26px;margin-bottom:6px;text-align:center}
.auth-card .auth-sub{text-align:center;color:var(--text-light);margin-bottom:26px}
.auth-footer{text-align:center;margin-top:20px;padding-top:20px;
  border-top:1px solid var(--border);color:var(--text-light);font-size:14px}

.dash{display:grid;grid-template-columns:250px 1fr;min-height:calc(100vh - 70px)}
.sidebar{background:var(--primary);color:#fff;padding:22px 14px}
.sidebar-nav{display:flex;flex-direction:column;gap:4px}
.sidebar-nav a{color:rgba(255,255,255,.85);padding:11px 14px;
  border-radius:var(--radius-sm);font-weight:500;font-size:14px;cursor:pointer;display:block}
.sidebar-nav a:hover,.sidebar-nav a.active{background:rgba(255,255,255,.12);
  color:#fff;text-decoration:none}
.sidebar-nav a.done{opacity:.75}
.sidebar-nav .section-label{padding:14px 14px 6px;font-size:11px;
  color:rgba(255,255,255,.5);text-transform:uppercase;letter-spacing:1px}
.dash-main{padding:30px;background:var(--bg);overflow-x:auto}
.dash-header{margin-bottom:26px}
.dash-header h1{font-size:25px;margin-bottom:4px}
.dash-header p{color:var(--text-light);font-size:14px}

.progress-card{background:#fff;padding:28px;border-radius:var(--radius);
  box-shadow:var(--shadow);display:flex;align-items:center;gap:30px;
  margin-bottom:26px;flex-wrap:wrap}
.progress-ring{position:relative;width:120px;height:120px;flex-shrink:0}
.progress-ring svg{transform:rotate(-90deg);width:100%;height:100%}
.ring-bg{fill:none;stroke:var(--border);stroke-width:3}
.ring-fill{fill:none;stroke:var(--primary-light);stroke-width:3;
  stroke-linecap:round;transition:stroke-dasharray .5s ease}
.ring-text{position:absolute;inset:0;display:flex;flex-direction:column;
  align-items:center;justify-content:center}
.ring-text strong{font-size:26px;color:var(--primary)}
.ring-text span{font-size:11px;color:var(--text-light);text-transform:uppercase}
.progress-info h3{margin-bottom:6px;color:var(--primary);font-size:18px}
.progress-info p{color:var(--text-light);font-size:14px;margin-bottom:4px}
.progress-info .next{color:var(--primary-light);font-weight:600;font-size:13px}

.module-row{background:#fff;padding:18px;border-radius:var(--radius);
  box-shadow:var(--shadow);margin-bottom:14px;display:flex;
  align-items:center;gap:18px;flex-wrap:wrap}
.module-row .num{width:52px;height:52px;background:var(--primary);color:#fff;
  border-radius:12px;display:flex;align-items:center;justify-content:center;
  font-size:22px;font-weight:700;flex-shrink:0}
.module-row.done .num{background:var(--success)}
.module-row .info{flex:1;min-width:200px}
.module-row .info h4{font-size:15px;margin-bottom:4px;color:var(--primary)}
.module-row .info p{font-size:13px;color:var(--text-light)}
.progress-bar{background:var(--border);height:8px;border-radius:4px;
  overflow:hidden;margin-top:8px;width:100%;max-width:280px}
.progress-fill{background:var(--primary-light);height:100%;transition:width .4s ease}

.admin-tabs{display:flex;gap:4px;border-bottom:2px solid var(--border);
  margin-bottom:22px;overflow-x:auto}
.tab{padding:11px 18px;background:none;border:none;font-size:14px;
  font-weight:600;cursor:pointer;color:var(--text-light);
  border-bottom:3px solid transparent;margin-bottom:-2px;white-space:nowrap}
.tab.active{color:var(--primary-light);border-bottom-color:var(--primary-light)}
.tab-content{display:none}
.tab-content.active{display:block}
.table-wrap{overflow-x:auto;background:#fff;border-radius:var(--radius);
  box-shadow:var(--shadow)}
table{width:100%;border-collapse:collapse;font-size:13px}
th,td{padding:12px 14px;text-align:left;border-bottom:1px solid var(--border)}
th{background:var(--bg);font-weight:600;color:var(--text-light);
  text-transform:uppercase;font-size:11px;letter-spacing:.5px}
tr:last-child td{border-bottom:none}
.empty-row{text-align:center;color:var(--text-light);padding:40px!important;font-style:italic}

.badge{display:inline-block;padding:3px 10px;border-radius:12px;
  font-size:11px;font-weight:600;background:var(--bg);color:var(--primary)}
.badge-success{background:#c6f6d5;color:#22543d}
.badge-gold{background:#fef3c7;color:#92400e}
code{background:var(--bg);padding:3px 8px;border-radius:4px;
  font-family:'Courier New',monospace;font-size:12px;color:var(--primary)}

.stat{background:#fff;padding:22px;border-radius:var(--radius);box-shadow:var(--shadow)}
.stat span{color:var(--text-light);font-size:13px;display:block;margin-bottom:6px}
.stat strong{font-size:26px;color:var(--primary);display:block}

.toast{position:fixed;top:20px;right:20px;padding:14px 22px;
  border-radius:var(--radius-sm);color:#fff;font-weight:500;z-index:9999;
  animation:slideIn .3s ease;box-shadow:var(--shadow-lg);max-width:340px;font-size:14px}
.toast-error{background:var(--danger)}
.toast-success{background:var(--success)}
.toast-info{background:var(--primary-light)}
@keyframes slideIn{from{transform:translateX(120%);opacity:0}to{transform:translateX(0);opacity:1}}

.lesson-view{background:#fff;border-radius:var(--radius);
  box-shadow:var(--shadow);padding:30px;margin-bottom:22px}
.lesson-view h2{color:var(--primary);margin-bottom:8px;font-size:23px;text-align:left}
.lesson-view .lesson-meta{color:var(--text-light);font-size:13px;margin-bottom:20px}
.content-block{margin-bottom:24px}
.content-block h3{color:var(--primary);margin-bottom:10px;font-size:17px}
.content-block h4{color:var(--primary-light);margin:14px 0 8px;font-size:15px}
.content-block ul,.content-block ol{padding-left:22px;margin:10px 0}
.content-block li{margin-bottom:6px}
.content-block p{margin-bottom:10px}
.content-block blockquote{border-left:4px solid var(--accent);
  background:#fffaf0;padding:14px 18px;margin:14px 0;border-radius:var(--radius-sm);
  font-style:italic;color:var(--primary);font-size:14px}

.resource-link{display:flex;align-items:flex-start;gap:12px;padding:14px 16px;
  background:var(--bg);border-radius:var(--radius-sm);margin-bottom:10px;
  border-left:4px solid var(--primary-light);transition:all .2s}
.resource-link:hover{background:#edf2f7;text-decoration:none;transform:translateX(3px)}
.resource-link .res-icon{font-size:20px;flex-shrink:0}
.resource-link .res-info strong{display:block;color:var(--primary);font-size:14px}
.resource-link .res-info small{color:var(--text-light);font-size:12px;display:block;margin-top:2px}
.res-badge{display:inline-block;font-size:10px;padding:2px 8px;
  border-radius:10px;margin-top:6px;font-weight:600}

.exercise-box{background:#fffaf0;border-left:4px solid var(--accent);
  padding:20px;border-radius:var(--radius-sm);margin:20px 0}
.exercise-box h3{color:var(--accent);margin-bottom:10px;font-size:16px}
.framework-tag{display:inline-block;background:#feebc8;color:#7b341e;
  padding:3px 10px;border-radius:10px;font-size:11px;font-weight:600;
  margin-bottom:10px;text-transform:uppercase;letter-spacing:.5px}
.lesson-actions{display:flex;gap:12px;margin-top:24px;flex-wrap:wrap}

.certificate{background:#fff;border:8px double var(--primary);padding:44px 36px;
  border-radius:var(--radius);text-align:center;box-shadow:var(--shadow-lg);
  max-width:780px;margin:0 auto;font-family:Georgia,serif}
.certificate .cert-logo{font-size:18px;font-weight:700;color:var(--primary);
  letter-spacing:2px;margin-bottom:22px}
.certificate h2{font-size:28px;color:var(--primary);margin-bottom:18px;text-align:center}
.certificate .cert-name{font-size:32px;color:var(--primary-light);
  font-style:italic;margin:22px 0;border-bottom:2px solid var(--border);padding-bottom:12px}
.certificate .cert-text{font-size:14px;color:var(--text);margin:18px 0;line-height:1.7}
.certificate .cert-meta{display:flex;justify-content:space-around;
  margin-top:36px;padding-top:18px;border-top:1px solid var(--border);
  font-size:11px;color:var(--text-light);flex-wrap:wrap;gap:20px}
.cert-sig{border-top:1px solid var(--text);padding-top:6px;min-width:140px;display:inline-block}

.payment-layout{display:grid;grid-template-columns:1fr 1fr;gap:26px;
  max-width:980px;margin:0 auto}
@media(max-width:800px){.payment-layout{grid-template-columns:1fr}}
.pay-box{background:#fff;padding:28px;border-radius:var(--radius);box-shadow:var(--shadow)}
.pay-box h3{margin-bottom:16px;color:var(--primary)}
.summary-row{display:flex;justify-content:space-between;padding:10px 0;
  border-bottom:1px solid var(--border);font-size:14px}
.summary-row:last-child{border-bottom:none;font-weight:700;color:var(--primary);
  font-size:16px;padding-top:14px}
.pay-steps{background:#f0fff4;border-left:4px solid var(--success);
  padding:14px;border-radius:var(--radius-sm);margin-bottom:18px}
.pay-steps ol{margin-left:20px;font-size:14px}
.pay-steps li{margin-bottom:6px}
.pay-steps .hl{background:#fefcbf;padding:2px 6px;border-radius:3px;
  font-weight:700;color:var(--primary)}

.step-list{list-style:none;counter-reset:step}
.step-list li{counter-increment:step;position:relative;padding:14px 0 14px 46px;
  border-bottom:1px solid var(--border);font-size:14px}
.step-list li:last-child{border-bottom:none}
.step-list li::before{content:counter(step);position:absolute;left:0;top:14px;
  width:30px;height:30px;background:var(--primary-light);color:#fff;
  border-radius:50%;display:flex;align-items:center;justify-content:center;
  font-weight:700;font-size:14px}

.framework-table{width:100%;border-collapse:collapse;background:#fff;
  border-radius:var(--radius);overflow:hidden;box-shadow:var(--shadow);
  font-size:14px;margin:20px 0}
.framework-table th{background:var(--primary);color:#fff;padding:14px 16px;
  text-align:left;font-weight:600;font-size:13px;text-transform:uppercase;
  letter-spacing:.5px}
.framework-table td{padding:14px 16px;border-bottom:1px solid var(--border);
  vertical-align:top}
.framework-table tr:last-child td{border-bottom:none}
.framework-table tr:hover td{background:#f7fafc}
.framework-table .domain{font-weight:700;color:var(--primary)}

.filter-bar{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;margin-bottom:28px}
.filter-btn{padding:8px 18px;border:2px solid var(--border);background:#fff;
  border-radius:20px;font-weight:600;font-size:13px;cursor:pointer;
  transition:all .2s;color:var(--text);font-family:inherit}
.filter-btn:hover{border-color:var(--primary-light);color:var(--primary-light)}
.filter-btn.active{background:var(--primary-light);color:#fff;border-color:var(--primary-light)}

.resource-card{background:#fff;padding:22px;border-radius:var(--radius);
  box-shadow:var(--shadow);display:flex;flex-direction:column;
  border-top:4px solid var(--primary-light);transition:transform .2s}
.resource-card:hover{transform:translateY(-3px);box-shadow:var(--shadow-lg)}
.resource-card.harvard{border-top-color:#a41e22}
.resource-card.ascd{border-top-color:#005eb8}
.resource-card.book{border-top-color:var(--gold)}
.resource-card.toolkit{border-top-color:var(--accent)}
.resource-type{display:inline-block;font-size:10px;font-weight:700;
  text-transform:uppercase;letter-spacing:1px;color:var(--text-light);margin-bottom:8px}
.resource-card h3{font-size:15px;color:var(--primary);margin-bottom:6px;line-height:1.35}
.resource-card .author{font-size:12px;color:var(--text-light);font-style:italic;margin-bottom:10px}
.resource-card p{font-size:13px;color:var(--text);margin-bottom:16px;flex-grow:1}
.resource-card .res-link{display:inline-flex;align-items:center;gap:6px;
  font-weight:600;font-size:13px;color:var(--primary-light);margin-top:auto}

.cta-strip{background:linear-gradient(135deg,var(--primary) 0%,var(--primary-light) 100%);
  color:#fff;text-align:center;padding:50px 20px;border-radius:var(--radius);
  max-width:980px;margin:40px auto}
.cta-strip h2{color:#fff;margin-bottom:10px}
.cta-strip p{opacity:.92;margin-bottom:22px;max-width:580px;margin-left:auto;
  margin-right:auto;font-size:15px}

footer{background:var(--primary);color:rgba(255,255,255,.85);padding:36px 20px;
  font-size:14px;margin-top:50px}
.footer-cols{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:28px;max-width:1000px;margin:0 auto 26px;text-align:left}
.footer-cols h4{color:#fff;margin-bottom:12px;font-size:15px}
.footer-cols p,.footer-cols a{font-size:13px;display:block;margin-bottom:6px;color:#fff}
.footer-bottom{text-align:center;opacity:.6;font-size:12px;padding-top:18px;
  border-top:1px solid rgba(255,255,255,.15);max-width:1000px;margin:0 auto}

@media(max-width:768px){
  .dash{grid-template-columns:1fr}
  .sidebar{padding:14px}
  .sidebar-nav{flex-direction:row;overflow-x:auto;gap:6px}
  .sidebar-nav a{white-space:nowrap;padding:10px 14px}
  .sidebar-nav .section-label{display:none}
  .dash-main{padding:18px}
  .nav-links{gap:12px;font-size:13px}
  .hero{padding:50px 20px}
  .progress-card{justify-content:center;text-align:center}
  section{padding:38px 16px}
  .auth-card{padding:32px 24px}
  .certificate{padding:28px 18px}
  .certificate .cert-name{font-size:24px}
  .certificate h2{font-size:20px}
  .framework-table{font-size:12px}
  .framework-table th,.framework-table td{padding:10px}
}
@media print{
  .topnav,footer,.lesson-actions,.sidebar,.btn-row{display:none!important}
  body{background:#fff}
  .certificate{box-shadow:none;border-width:4px}
}
</style>
</head>
<body>

<nav class="topnav">
  <div class="topnav-inner">
    <div class="logo" onclick="go('home')">🎓 ILM Academy</div>
    <div class="nav-links">
      <a data-nav="home" onclick="go('home')">Home</a>
      <a data-nav="framework" onclick="go('framework')">Framework</a>
      <a data-nav="resources" onclick="go('resources')">Resources</a>
      <a data-nav="toolkit" onclick="go('toolkit')">Toolkit</a>
      <a data-nav="home" onclick="go('home');setTimeout(function(){scrollToId('pricing')},150)">Pricing</a>
      <a id="navAuth" onclick="go('login')">Login</a>
      <a id="navDash" class="hidden" onclick="go('dashboard')">Dashboard</a>
      <a id="navAdmin" class="hidden" onclick="go('admin')">Admin</a>
      <a id="navLogout" class="hidden" onclick="logout()">Logout</a>
    </div>
  </div>
</nav>

<main id="app"></main>

<footer>
  <div class="footer-cols">
    <div>
      <h4>🎓 ILM Academy</h4>
      <p>Empowering School Leaders for the 21st Century</p>
      <p style="margin-top:10px;font-size:12px;opacity:.7">Aligned with Harvard GSE & ASCD standards</p>
    </div>
    <div>
      <h4>Contact</h4>
      <p>📱 Mobile Money: <strong>0917106325</strong></p>
      <p>📧 admin@ilmacademy.com</p>
    </div>
    <div>
      <h4>Explore</h4>
      <a onclick="go('home')">Home</a>
      <a onclick="go('framework')">Framework</a>
      <a onclick="go('resources')">Resource Library</a>
      <a onclick="go('toolkit')">Toolkit</a>
    </div>
    <div>
      <h4>Certification Pathways</h4>
      <a href="https://www.gse.harvard.edu/professional-education/certificate/instructional-leadership-certificate-ilc" target="_blank" rel="noopener">Harvard GSE ILC</a>
      <a href="https://www.ascd.org/instructional-leader-certification" target="_blank" rel="noopener">ASCD Certification</a>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2025 ILM Academy. All Rights Reserved. · Priced in Ethiopian Birr (ETB)</p>
  </div>
</footer>

<script>
/* ============================================================
   ILM ACADEMY v6.0 — FINAL
   Pricing: Birr 50 / 150 / 500
   Payment: 0917106325
   ============================================================ */

const CONFIG = {
  paymentNumber: '0917106325',
  currency: 'ETB',
  currencyLabel: 'Birr',
  adminEmail: 'admin@ilmacademy.com'
};

const PACKAGES = {
  basic:   { name: 'Self-Paced', price: 50 },
  premium: { name: 'Premium',    price: 150 },
  school:  { name: 'School Team',price: 500 }
};

const COURSE = {
  title: 'The 21st Century Instructional Leadership Masterclass',
  modules: [
    {
      number: 1,
      title: 'The 21st Century Paradigm: From Manager to Catalyst of Learning',
      description: 'Understanding the four core pillars of 21st-century instructional leadership and establishing your personal vision.',
      lessons: [
        {
          id: '1-1', title: 'Executive Summary & Core Definition', duration: 15,
          content: `
            <div class="content-block">
              <h3>🎯 Learning Objectives</h3>
              <ul>
                <li>Understand the shift from administrative manager to catalyst of learning</li>
                <li>Identify the forces reshaping 21st-century education</li>
                <li>Articulate a personal definition of instructional leadership</li>
              </ul>
            </div>
            <div class="content-block">
              <h3>📖 Core Content</h3>
              <blockquote>
                <strong>Instructional Leadership in the 21st Century</strong> shifts the role of educational leaders from traditional administrative managers to <strong>catalysts of learning, innovation, and continuous growth</strong>.
              </blockquote>
              <p>In today's dynamic educational landscape—marked by rapid digital transformation, artificial intelligence, diverse learning needs, and shifting global competencies—instructional leaders must cultivate adaptive learning environments.</p>
              <p>They align <strong>curriculum, assessment, technology, and pedagogical practices</strong> to maximize both educator effectiveness and learner outcomes.</p>
              <h4>The Forces Reshaping Education</h4>
              <ul>
                <li><strong>Digital transformation</strong> — every classroom is now a digital learning environment</li>
                <li><strong>Artificial intelligence</strong> — reshaping assessment, personalization, and workload</li>
                <li><strong>Diverse learning needs</strong> — inclusive education is no longer optional</li>
                <li><strong>Global competencies</strong> — critical thinking, creativity, collaboration, communication</li>
              </ul>
            </div>
            <div class="exercise-box">
              <span class="framework-tag">Reflection</span>
              <h3>✍️ Exercise: Define Your Role</h3>
              <p>In 3-5 sentences, write your own definition of 21st-century instructional leadership. How is it different from what you were trained to do?</p>
              <textarea id="ex-1-1" placeholder="My definition..." style="width:100%;margin-top:10px;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:120px"></textarea>
              <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('1-1')">Save Response</button>
            </div>
            <div class="content-block">
              <h3>📚 Essential Resources</h3>
              <a class="resource-link" href="https://www.wallacefoundation.org/" target="_blank" rel="noopener">
                <span class="res-icon">📄</span>
                <span class="res-info"><strong>Wallace Foundation: School Leadership Library</strong>
                <small>Empirical research on how principal leadership affects student outcomes</small>
                <span class="res-badge badge">Research</span></span>
              </a>
              <a class="resource-link" href="https://www.ascd.org/" target="_blank" rel="noopener">
                <span class="res-icon">📄</span>
                <span class="res-info"><strong>ASCD Learning Hub</strong>
                <small>Practitioner articles on 21st-century instructional leadership</small>
                <span class="res-badge badge">Articles</span></span>
              </a>
              <a class="resource-link" href="https://www.futurelearn.com/courses/instructional-leadership" target="_blank" rel="noopener">
                <span class="res-icon">🎓</span>
                <span class="res-info"><strong>British Council: Exploring Instructional Leadership</strong>
                <small>Free 3-week online course on instructional leadership</small>
                <span class="res-badge badge">Free Course</span></span>
              </a>
            </div>
          `
        },
        {
          id: '1-2', title: 'The Four Pillars of 21st Century Leadership', duration: 20,
          content: `
            <div class="content-block">
              <h3>🎯 Learning Objectives</h3>
              <ul>
                <li>Identify the four pillars of 21st-century instructional leadership</li>
                <li>Self-assess your current strength in each pillar</li>
              </ul>
            </div>
            <div class="content-block">
              <h3>📖 The Four Pillars</h3>
              <div class="pillar-diagram" style="margin:20px 0">
                <div class="pillar-core">21st Century Instructional Leadership Core</div>
                <div class="pillar-arrow">↓</div>
                <div class="pillar-grid">
                  <div class="pillar-box"><span class="p-icon">🔭</span><h4>Vision & Tech</h4><p>Future-ready curriculum & digital integration</p></div>
                  <div class="pillar-box"><span class="p-icon">📊</span><h4>Data & AI</h4><p>Evidence-based decisions & formative culture</p></div>
                  <div class="pillar-box"><span class="p-icon">🎯</span><h4>Professional Coaching</h4><p>Observation, feedback & PLCs</p></div>
                  <div class="pillar-box"><span class="p-icon">⚖️</span><h4>Equity & Culture</h4><p>Inclusive, culturally responsive learning</p></div>
                </div>
              </div>
              <h4>A. Visionary & Technology-Enhanced Leadership</h4>
              <ul>
                <li><strong>Digital & AI Integration:</strong> Strategically integrating technology, digital tools, and emerging AI frameworks to enhance engagement, streamline assessments, and personalize learning pathways.</li>
                <li><strong>Future-Ready Curriculum:</strong> Promoting 21st-century skills—critical thinking, creativity, collaboration, communication, and digital literacy—across all content areas.</li>
              </ul>
              <h4>B. Data-Informed & Results-Based Decision Making</h4>
              <ul>
                <li><strong>Formative Assessment Culture:</strong> Shifting focus from purely summative evaluations to continuous, real-time diagnostic and formative assessments.</li>
                <li><strong>Evidence-Based Practice:</strong> Utilizing data tools (e.g., KoboToolbox, dashboards, student growth metrics) to identify learning gaps, target interventions, and measure instructional impact.</li>
              </ul>
              <h4>C. Instructional Coaching & Continuous Capacity Building</h4>
              <ul>
                <li><strong>Observation & Rapid Feedback:</strong> Implementing short, frequent walkthroughs followed by actionable, growth-oriented feedback cycles (e.g., <em>Leverage Leadership</em> frameworks).</li>
                <li><strong>Professional Learning Communities (PLCs):</strong> Fostering collaborative teacher teams that continuously reflect on practice, analyze student work, and share effective strategies.</li>
              </ul>
              <h4>D. Inclusive, Culturally Responsive & Equitable Learning</h4>
              <ul>
                <li><strong>Universal Design & Access:</strong> Ensuring all learners—including vulnerable, accelerated, or struggling students—have equitable access to high-quality instruction.</li>
                <li><strong>Indigenous & Contextualized Knowledge:</strong> Respecting local languages, mother-tongue instruction, and community values alongside global best practices.</li>
              </ul>
            </div>
            <div class="exercise-box">
              <span class="framework-tag">Framework: 4 Pillars</span>
              <h3>✍️ Exercise: Self-Assessment</h3>
              <p>Rate yourself (1-5) on each of the four pillars. Which is your strongest? Which needs the most growth?</p>
              <textarea id="ex-1-2" placeholder="Vision & Tech: __/5&#10;Data & AI: __/5&#10;Coaching: __/5&#10;Equity: __/5" style="width:100%;margin-top:10px;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:140px"></textarea>
              <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('1-2')">Save Response</button>
            </div>
            <div class="content-block">
              <h3>📚 Essential Resources</h3>
              <a class="resource-link" href="https://youtu.be/N31xGilA3cl" target="_blank" rel="noopener">
                <span class="res-icon">🎥</span>
                <span class="res-info"><strong>Instructional Leadership: What It Is & Why It Matters</strong>
                <small>5-minute video on the core of instructional leadership</small>
                <span class="res-badge badge">Video</span></span>
              </a>
              <a class="resource-link" href="https://k-12leadership.org/tools/5-dimensions-of-teaching-and-learning" target="_blank" rel="noopener">
                <span class="res-icon">🧰</span>
                <span class="res-info"><strong>5 Dimensions of Teaching and Learning</strong>
                <small>Research-backed observation framework</small>
                <span class="res-badge badge">Toolkit</span></span>
              </a>
            </div>
          `
        },
        {
          id: '1-3', title: 'Core Functions & Responsibilities', duration: 16,
          content: `
            <div class="content-block">
              <h3>📖 Core Functions Table</h3>
              <table class="framework-table">
                <thead><tr><th>Leadership Domain</th><th>Key Strategic Action</th><th>Impact on Learning</th></tr></thead>
                <tbody>
                  <tr><td class="domain">Defining the Mission</td><td>Establishing clear, measurable, and shared goals for student growth and school climate.</td><td>Aligns staff focus on shared educational priorities.</td></tr>
                  <tr><td class="domain">Managing Curriculum & Instruction</td><td>Aligning standards, learning materials, and modern pedagogical methodologies.</td><td>Guarantees rigor, relevance, and consistency across classrooms.</td></tr>
                  <tr><td class="domain">Coaching & Mentoring Teachers</td><td>Facilitating peer observations, modeling lessons, and running targeted professional development.</td><td>Elevates teaching quality and retains high-performing educators.</td></tr>
                  <tr><td class="domain">Monitoring & Evaluation</td><td>Conducting systematic reviews of learning outcomes using clear logical frameworks and MEAL systems.</td><td>Ensures accountability and real-time project/school adjustments.</td></tr>
                </tbody>
              </table>
            </div>
            <div class="exercise-box">
              <span class="framework-tag">Framework: 4 Domains</span>
              <h3>✍️ Exercise: Audit Your Practice</h3>
              <p>For each domain, note ONE thing you do well and ONE thing you need to strengthen.</p>
              <textarea id="ex-1-3" placeholder="Mission — Do well / Strengthen: ..." style="width:100%;margin-top:10px;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:180px"></textarea>
              <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('1-3')">Save Response</button>
            </div>
          `
        },
        {
          id: '1-4', title: 'Key Takeaways for Practice', duration: 12,
          content: `
            <div class="content-block">
              <h3>📖 Key Takeaways</h3>
              <blockquote><strong>The Principal/Leader as the Primary Learner:</strong> Effective instructional leaders do not simply manage instruction; they actively participate in learning, remaining current on new pedagogical research, technology, and leadership frameworks.</blockquote>
              <ul>
                <li><strong>Shift from Compliance to Growth:</strong> Observations should empower teachers, encouraging calculated innovation rather than enforcing rigid compliance.</li>
                <li><strong>Actionable Next Steps:</strong> Every classroom visit should result in one clear, high-leverage bite-sized action step for the teacher to implement immediately.</li>
              </ul>
            </div>
            <div class="exercise-box">
              <span class="framework-tag">Commitment</span>
              <h3>✍️ Exercise: One Next Step</h3>
              <p>What is ONE specific action you will take in the next 7 days?</p>
              <textarea id="ex-1-4" placeholder="In the next 7 days I will..." style="width:100%;margin-top:10px;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:100px"></textarea>
              <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('1-4')">Save Response</button>
            </div>
          `
        },
        { id: '1-5', title: 'Module 1 Quiz', duration: 10, content: `<div class="content-block"><h3>📝 Knowledge Check</h3></div><div id="quiz-1"></div>` }
      ]
    },
    {
      number: 2,
      title: 'Building a Culture of Collaboration and Trust',
      description: 'Creating psychological safety and collaborative structures necessary for teachers to grow.',
      lessons: [
        { id: '2-1', title: 'Culture & Trust: The Foundation', duration: 16,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <p>Amy Edmondson defines psychological safety as "a belief that one will not be punished or humiliated for speaking up with ideas, questions, concerns, or mistakes."</p>
            <h4>The Four Components</h4>
            <ul><li><strong>Trust:</strong> Predictability and reliability</li><li><strong>Respect:</strong> Valuing expertise</li><li><strong>Vulnerability:</strong> Admitting what you don't know</li><li><strong>Consistency:</strong> Walking the talk</li></ul>
            <p>Jim Knight's <em>Unmistakable Impact</em>: trust built through <strong>7 Partnership Principles</strong>—equality, choice, voice, reflection, dialogue, praxis, reciprocity.</p>
          </div>
          <div class="exercise-box"><span class="framework-tag">Framework: Knight</span><h3>✍️ Trust Audit</h3>
            <textarea id="ex-2-1" placeholder="Trust audit..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:120px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('2-1')">Save Response</button>
          </div>
          <div class="content-block"><h3>📚 Essential Resources</h3>
            <a class="resource-link" href="https://www.youtube.com/watch?v=LhoLuui9gX8" target="_blank" rel="noopener">
              <span class="res-icon">🎥</span>
              <span class="res-info"><strong>Amy Edmondson: Psychological Safety</strong>
              <small>12-minute TED-style talk on building safe teams</small>
              <span class="res-badge badge">Video</span></span>
            </a>
            <a class="resource-link" href="https://www.goodreads.com/shelf/show/instructional-leadership" target="_blank" rel="noopener">
              <span class="res-icon">📕</span>
              <span class="res-info"><strong>Unmistakable Impact — Jim Knight</strong>
              <small>Partnership approach to instructional coaching</small>
              <span class="res-badge badge">Book</span></span>
            </a>
          </div>` },
        { id: '2-2', title: 'Collective Efficacy & PLCs', duration: 15,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <p>Collective teacher efficacy has an effect size of <strong>1.57</strong> (Hattie, 2018).</p>
            <p>DuFour & Marzano's <em>Leaders of Learning</em>: PLCs structured around 4 questions:</p>
            <ol><li>What do we want students to learn?</li><li>How will we know if they've learned it?</li><li>What will we do if they haven't?</li><li>What will we do if they already have?</li></ol>
          </div>
          <div class="exercise-box"><span class="framework-tag">DuFour PLC</span><h3>✍️ PLC Startup Kit</h3>
            <textarea id="ex-2-2" placeholder="Meeting 1: ..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:150px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('2-2')">Save Response</button>
          </div>
          <div class="content-block"><h3>📚 Essential Resources</h3>
            <a class="resource-link" href="https://archive.org/details/collaborativetea0000unse" target="_blank" rel="noopener">
              <span class="res-icon">🎥</span>
              <span class="res-info"><strong>Collaborative Teams in PLCs at Work</strong>
              <small>30-minute video showing real PLC team meetings</small>
              <span class="res-badge badge">Video</span></span>
            </a>
            <a class="resource-link" href="https://www.edutopia.org/article/building-collective-efficacy-schools" target="_blank" rel="noopener">
              <span class="res-icon">📄</span>
              <span class="res-info"><strong>Building Collective Efficacy in Schools</strong>
              <small>Practical strategies from Edutopia</small>
              <span class="res-badge badge">Article</span></span>
            </a>
          </div>` },
        { id: '2-3', title: 'Difficult Conversations with SBI', duration: 18,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <p><strong>SBI Framework:</strong> Situation — Behavior — Impact. Separates person from behavior.</p>
            <h4>Common Sources of Resistance</h4>
            <ul><li><strong>Fear:</strong> Change means loss of competence</li><li><strong>Workload:</strong> Added burden</li><li><strong>Distrust:</strong> Past broken promises</li><li><strong>Belief:</strong> Philosophical disagreement</li></ul>
          </div>
          <div class="exercise-box"><span class="framework-tag">Framework: SBI</span><h3>✍️ Practice SBI</h3>
            <textarea id="ex-2-3" placeholder="Situation: ..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:140px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('2-3')">Save Response</button>
          </div>` },
        { id: '2-4', title: 'Module 2 Quiz', duration: 8, content: `<div class="content-block"><h3>📝 Knowledge Check</h3></div><div id="quiz-2"></div>` }
      ]
    },
    {
      number: 3,
      title: 'Data & AI-Informed Instruction',
      description: 'Using formative data, digital tools, and AI frameworks to drive instructional decisions.',
      lessons: [
        { id: '3-1', title: 'Formative Assessment Culture', duration: 14,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <p>Shift from summative to continuous, real-time diagnostic and formative assessments.</p>
            <h4>The Data Pyramid</h4>
            <ul><li><strong>Formative (most actionable):</strong> Exit tickets, quick checks, student work</li><li><strong>Interim:</strong> Unit tests, benchmarks</li><li><strong>Summative:</strong> End-of-year exams</li><li><strong>Perceptual:</strong> Surveys, focus groups</li></ul>
            <p><em>Leverage Leadership 2.0</em> describes weekly data meetings.</p>
          </div>
          <div class="exercise-box"><span class="framework-tag">Bambrick-Santoyo</span><h3>✍️ Data Source Audit</h3>
            <textarea id="ex-3-1" placeholder="Data audit..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:150px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('3-1')">Save Response</button>
          </div>
          <div class="content-block"><h3>📚 Essential Resources</h3>
            <a class="resource-link" href="https://www.khanacademy.org/teacher-tools" target="_blank" rel="noopener">
              <span class="res-icon">🎥</span>
              <span class="res-info"><strong>Khan Academy: Using Data to Inform Instruction</strong>
              <small>Video on real-time progress monitoring</small>
              <span class="res-badge badge">Video</span></span>
            </a>
            <a class="resource-link" href="https://www.goodreads.com/shelf/show/instructional-leadership" target="_blank" rel="noopener">
              <span class="res-icon">📕</span>
              <span class="res-info"><strong>Leverage Leadership 2.0 — Bambrick-Santoyo</strong>
              <small>Weekly observation-feedback cycles and data-driven instruction</small>
              <span class="res-badge badge">Book</span></span>
            </a>
          </div>` },
        { id: '3-2', title: 'Evidence-Based Practice & Digital Tools', duration: 16,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <h4>Digital Tools for Data-Informed Leadership</h4>
            <ul><li><strong>KoboToolbox:</strong> Free, open-source data collection</li><li><strong>Dashboards:</strong> Real-time visualization</li><li><strong>Growth Metrics:</strong> Value-added models</li><li><strong>MEAL:</strong> Monitoring, Evaluation, Accountability, Learning</li></ul>
            <h4>NSRF Protocol</h4>
            <ol><li><strong>Predict</strong></li><li><strong>Observe</strong></li><li><strong>Infer</strong></li></ol>
          </div>
          <div class="exercise-box"><span class="framework-tag">NSRF · KoboToolbox</span><h3>✍️ Design a Data Tool</h3>
            <textarea id="ex-3-2" placeholder="Question 1: ..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:160px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('3-2')">Save Response</button>
          </div>
          <div class="content-block"><h3>📚 Essential Resources</h3>
            <a class="resource-link" href="https://www.kobotoolbox.org/" target="_blank" rel="noopener">
              <span class="res-icon">🛠️</span>
              <span class="res-info"><strong>KoboToolbox — Free Data Collection</strong>
              <small>Open-source tool for classroom walkthroughs and surveys</small>
              <span class="res-badge badge">Tool</span></span>
            </a>
            <a class="resource-link" href="https://www.nsrfharmony.org/" target="_blank" rel="noopener">
              <span class="res-icon">📄</span>
              <span class="res-info"><strong>NSRF Data-Driven Dialogue Protocols</strong>
              <small>Predict-Observe-Infer structure for team data meetings</small>
              <span class="res-badge badge">Protocol</span></span>
            </a>
          </div>` },
        { id: '3-3', title: 'AI in Instructional Leadership', duration: 14,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <h4>The AI Integration Framework</h4>
            <ul><li><strong>Assess:</strong> What problem?</li><li><strong>Align:</strong> Supports vision?</li><li><strong>Equity:</strong> Who benefits/excluded?</li><li><strong>Privacy:</strong> Data protection compliant?</li><li><strong>Human Oversight:</strong> AI assists, teachers decide</li></ul>
            <h4>Practical Uses</h4>
            <ul><li>Drafting observation feedback</li><li>Analyzing survey responses</li><li>Differentiated lesson ideas</li><li>Translating communications</li></ul>
          </div>
          <div class="exercise-box"><span class="framework-tag">5-Point AI Rubric</span><h3>✍️ Evaluate an AI Tool</h3>
            <textarea id="ex-3-3" placeholder="Tool: ..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:180px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('3-3')">Save Response</button>
          </div>` },
        { id: '3-4', title: 'Module 3 Quiz', duration: 8, content: `<div class="content-block"><h3>📝 Knowledge Check</h3></div><div id="quiz-3"></div>` }
      ]
    },
    {
      number: 4,
      title: 'Coaching, Feedback & Capacity Building',
      description: 'Moving from evaluation to effective, growth-oriented coaching using GROW, SBI, and Leverage Leadership cycles.',
      lessons: [
        { id: '4-1', title: 'Evaluation vs. Coaching', duration: 15,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <p>Evaluation: "Is this teacher meeting the standard?" Coaching: "How can this teacher grow?"</p>
            <ul><li><strong>Evaluation:</strong> Leader-driven, judgment-focused, episodic</li><li><strong>Coaching:</strong> Teacher-driven, growth-focused, ongoing</li></ul>
            <p>Knight's <strong>7 Partnership Principles</strong>: Equality, Choice, Voice, Reflection, Dialogue, Praxis, Reciprocity.</p>
          </div>
          <div class="exercise-box"><span class="framework-tag">Knight</span><h3>✍️ Time Audit</h3>
            <textarea id="ex-4-1" placeholder="Current split..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:120px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('4-1')">Save Response</button>
          </div>
          <div class="content-block"><h3>📚 Essential Resources</h3>
            <a class="resource-link" href="https://www.opportunityculture.org/category/videos/" target="_blank" rel="noopener">
              <span class="res-icon">🎥</span>
              <span class="res-info"><strong>Instructional Leadership & Excellence Video Series</strong>
              <small>Short videos on coaching, feedback, and modeling</small>
              <span class="res-badge badge">Video</span></span>
            </a>
          </div>` },
        { id: '4-2', title: 'The GROW Model', duration: 18,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <ul><li><strong>G — Goal</strong></li><li><strong>R — Reality</strong></li><li><strong>O — Options</strong></li><li><strong>W — Will</strong></li></ul>
            <h4>Powerful Questions</h4>
            <ul><li>"What have you already tried?"</li><li>"What would success look like?"</li><li>"What support do you need?"</li></ul>
          </div>
          <div class="exercise-box"><span class="framework-tag">GROW (Whitmore)</span><h3>✍️ Coaching Script</h3>
            <textarea id="ex-4-2" placeholder="Goal: ..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:200px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('4-2')">Save Response</button>
          </div>
          <div class="content-block"><h3>📚 Essential Resources</h3>
            <a class="resource-link" href="https://www.youtube.com/watch?v=xNLRo3jWPcg" target="_blank" rel="noopener">
              <span class="res-icon">🎥</span>
              <span class="res-info"><strong>Coaching and the GROW Model</strong>
              <small>Video explaining the GROW coaching framework</small>
              <span class="res-badge badge">Video</span></span>
            </a>
            <a class="resource-link" href="https://www.edutopia.org/article/instructional-coaching-guide" target="_blank" rel="noopener">
              <span class="res-icon">📄</span>
              <span class="res-info"><strong>Instructional Coaching: A Guide</strong>
              <small>Practical overview from Edutopia</small>
              <span class="res-badge badge">Article</span></span>
            </a>
          </div>` },
        { id: '4-3', title: 'Rapid Feedback Cycles', duration: 14,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <p>Bambrick-Santoyo's <em>Leverage Leadership 2.0</em>:</p>
            <ol><li><strong>Weekly observation</strong> (10-15 minutes)</li><li><strong>Immediate feedback</strong> (within 24 hours)</li><li><strong>One bite-sized action step</strong></li><li><strong>Follow-up observation</strong></li></ol>
            <p>The magic is in the <strong>frequency</strong>, not the length.</p>
          </div>
          <div class="exercise-box"><span class="framework-tag">Leverage Leadership</span><h3>✍️ Design Your Feedback Cycle</h3>
            <textarea id="ex-4-3" placeholder="Observation day..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:140px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('4-3')">Save Response</button>
          </div>
          <div class="content-block"><h3>📚 Essential Resources</h3>
            <a class="resource-link" href="https://www.wiley.com/en-gb/shop/general-introductory-education/leverage-leadership-3.0-a-practical-guide-to-building-exceptional-schools-p-9781394324439" target="_blank" rel="noopener">
              <span class="res-icon">📕</span>
              <span class="res-info"><strong>Leverage Leadership 3.0</strong>
              <small>Bambrick-Santoyo's updated framework with AI-enhanced tools</small>
              <span class="res-badge badge">Book</span></span>
            </a>
          </div>` },
        { id: '4-4', title: 'Module 4 Quiz', duration: 8, content: `<div class="content-block"><h3>📝 Knowledge Check</h3></div><div id="quiz-4"></div>` }
      ]
    },
    {
      number: 5,
      title: 'Equity, Culture & Culturally Responsive Leadership',
      description: 'Ensuring all learners have equitable access, respecting local knowledge and community values.',
      lessons: [
        { id: '5-1', title: 'Universal Design & Equitable Access', duration: 15,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <p>Equity is not equality. Equality gives everyone the same; equity gives everyone what they need.</p>
            <h4>UDL Principles</h4>
            <ul><li><strong>Multiple means of Engagement:</strong> Why learn?</li><li><strong>Multiple means of Representation:</strong> What learn?</li><li><strong>Multiple means of Action & Expression:</strong> How learn?</li></ul>
          </div>
          <div class="exercise-box"><span class="framework-tag">UDL</span><h3>✍️ Equity Audit</h3>
            <textarea id="ex-5-1" placeholder="Group: ..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:140px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('5-1')">Save Response</button>
          </div>
          <div class="content-block"><h3>📚 Essential Resources</h3>
            <a class="resource-link" href="https://www.edutopia.org/blog/5-minute-film-festival-culturally-responsive-teaching" target="_blank" rel="noopener">
              <span class="res-icon">🎥</span>
              <span class="res-info"><strong>5-Minute Film Festival: Culturally Responsive Teaching</strong>
              <small>Playlist of videos introducing culturally responsive teaching</small>
              <span class="res-badge badge">Video</span></span>
            </a>
          </div>` },
        { id: '5-2', title: 'Indigenous & Contextualized Knowledge', duration: 14,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <ul><li><strong>Mother-tongue instruction:</strong> Children learn best in first language</li><li><strong>Community values:</strong> Reflect local aspirations</li><li><strong>Indigenous knowledge:</strong> Traditional ecological knowledge, oral histories</li><li><strong>Contextualized assessment:</strong> Meaningful in cultural/linguistic context</li></ul>
          </div>
          <div class="exercise-box"><span class="framework-tag">Cultural Bridge</span><h3>✍️ Context Mapping</h3>
            <textarea id="ex-5-2" placeholder="Local knowledge: ..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:140px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('5-2')">Save Response</button>
          </div>` },
        { id: '5-3', title: 'Digital Equity', duration: 12,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <ul><li><strong>Access:</strong> Devices and internet</li><li><strong>Skills:</strong> Effective use</li><li><strong>Use:</strong> Creation vs. consumption</li><li><strong>Support:</strong> Adults who help</li></ul>
          </div>
          <div class="exercise-box"><span class="framework-tag">4-D Equity</span><h3>✍️ Digital Equity Plan</h3>
            <textarea id="ex-5-3" placeholder="Weakest dimension..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:120px"></textarea>
            <button class="btn btn-sm" style="margin-top:10px" onclick="saveExercise('5-3')">Save Response</button>
          </div>` },
        { id: '5-4', title: 'Module 5 Quiz', duration: 8, content: `<div class="content-block"><h3>📝 Knowledge Check</h3></div><div id="quiz-5"></div>` }
      ]
    },
    {
      number: 6,
      title: 'Capstone: Your 90-Day Instructional Leadership Action Plan',
      description: 'Synthesizing all learning into a practical, measurable action plan for your school.',
      lessons: [
        { id: '6-1', title: 'From Learning to Leading', duration: 10,
          content: `<div class="content-block"><h3>📖 Core Content</h3>
            <p>You've explored the four pillars, four domains, coaching, data, AI, and equity. Now it's time to lead.</p>
            <p>A 90-day plan is long enough to see real progress but short enough to maintain urgency.</p>
          </div>` },
        { id: '6-2', title: 'Capstone Submission', duration: 30,
          content: `
            <div class="content-block"><h3>📝 Complete Your Capstone</h3>
            <p>Fill in all five sections below.</p></div>
            <div class="exercise-box"><h3>Section 1: Your Vision</h3>
              <textarea id="cap-1" placeholder="My leadership vision..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:80px"></textarea></div>
            <div class="exercise-box"><h3>Section 2: Goals (2-3)</h3>
              <textarea id="cap-2" placeholder="Goal 1: ..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:120px"></textarea></div>
            <div class="exercise-box"><h3>Section 3: Actions</h3>
              <textarea id="cap-3" placeholder="Weeks 1-2: ..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:150px"></textarea></div>
            <div class="exercise-box"><h3>Section 4: Metrics</h3>
              <textarea id="cap-4" placeholder="How I'll measure..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:100px"></textarea></div>
            <div class="exercise-box"><h3>Section 5: Support Needed</h3>
              <textarea id="cap-5" placeholder="Resources..." style="width:100%;padding:12px;border:1px solid var(--border);border-radius:6px;font-family:inherit;min-height:100px"></textarea></div>
            <button class="btn btn-full" onclick="submitCapstone()">Submit Capstone Project</button>
          ` }
      ]
    }
  ]
};

const QUIZZES = {
  '1': [
    { q: 'How many core pillars define 21st-century instructional leadership?', options: ['2','3','4','5'], correct: 2 },
    { q: 'Which pillar includes AI integration?', options: ['Equity','Vision & Tech','Coaching','Data'], correct: 1 },
    { q: 'The leader\'s key mindset shift?', options: ['Teaching to managing','Compliance to growth','Data to intuition','Vision to control'], correct: 1 }
  ],
  '2': [
    { q: 'Collective teacher efficacy effect size?', options: ['0.42','0.84','1.57','0.27'], correct: 2 },
    { q: 'SBI stands for:', options: ['School Board Initiative','Situation-Behavior-Impact','Student Behavior Index','Strategic Budget'], correct: 1 },
    { q: 'Who wrote "Unmistakable Impact"?', options: ['Bambrick-Santoyo','Jim Knight','DuFour','Woolfolk'], correct: 1 }
  ],
  '3': [
    { q: 'Which is most actionable data?', options: ['Summative','Formative','Standardized','Historic'], correct: 1 },
    { q: 'NSRF phase 1?', options: ['Predict','Observe','Infer','Act'], correct: 0 },
    { q: 'KoboToolbox is:', options: ['AI chatbot','Free open-source data collection tool','Testing platform','Curriculum'], correct: 1 }
  ],
  '4': [
    { q: 'Coaching differs from evaluation by being:', options: ['Leader-driven','Growth-focused','Documented','Episodic'], correct: 1 },
    { q: 'GROW stands for:', options: ['Goal-Reality-Options-Will','Great-Real-Optimal-Working','Grow-Review-Outcome-Win','Goal-Reach-Outcome-Work'], correct: 0 },
    { q: 'Leverage Leadership recommends feedback every:', options: ['Year','Month','Week','Term'], correct: 2 }
  ],
  '5': [
    { q: 'UDL stands for:', options: ['Universal Design for Learning','Unified District Leadership','Urban Development Law','None'], correct: 0 },
    { q: 'Digital divide includes:', options: ['Device access only','Access, skills, use, support','Internet speed only','Training only'], correct: 1 },
    { q: 'Mother-tongue instruction matters because:', options: ['Easier','Children learn best in first language','Cheaper','Required'], correct: 1 }
  ]
};

const RESOURCES = [
  { type:'certification', title:'Harvard GSE — Instructional Leadership Certificate (ILC)', author:'Harvard Graduate School of Education',
    description:'Four-course professional sequence covering teacher coaching, mentoring, teacher team development, and instructional alignment.',
    url:'https://www.gse.harvard.edu/professional-education/certificate/instructional-leadership-certificate-ilc' },
  { type:'certification', title:'ASCD Instructional Leader Certification', author:'ASCD',
    description:'Competency-based professional credential centered on data-driven decision making, curriculum improvement, teacher observation, and coaching.',
    url:'https://www.ascd.org/instructional-leader-certification' },
  { type:'certification', title:'British Council: Exploring Instructional Leadership', author:'FutureLearn / British Council',
    description:'Free 3-week online course exploring how instructional leadership techniques can motivate staff, engage students, and transform teaching and learning.',
    url:'https://www.futurelearn.com/courses/instructional-leadership' },
  { type:'certification', title:'Principles of Educational Leadership & Management', author:'Coursera',
    description:'Comprehensive university module analyzing shared leadership, staff coaching, and institutional decision-making.',
    url:'https://www.classcentral.com/subject/educational-leadership' },
  { type:'book', title:'Leverage Leadership 2.0', author:'Paul Bambrick-Santoyo',
    description:'Core handbook covering weekly observation-feedback cycles, data-driven instruction, school culture, and leadership team development.',
    url:'https://www.goodreads.com/shelf/show/instructional-leadership' },
  { type:'book', title:'Instructional Leadership: A Research-Based Guide', author:'Anita Woolfolk & Wayne K. Hoy',
    description:'Academic textbook bridging cognitive learning theory, motivation, and school-wide instructional strategies.',
    url:'https://www.pearson.com/en-us/subject-catalog/p/Woolfolk-Instructional-Leadership-A-Research-Based-Guide-to-Learning-in-Schools-RENTAL-EDITION-5th-Edition/P200000002044' },
  { type:'book', title:'Unmistakable Impact: A Partnership Approach', author:'Jim Knight',
    description:'Practical framework for instructional coaching, collaborative improvement, and implementation science.',
    url:'https://www.goodreads.com/shelf/show/instructional-leadership' },
  { type:'book', title:'Leaders of Learning', author:'Richard DuFour & Robert J. Marzano',
    description:'Aligning Professional Learning Communities (PLCs) with systemic instructional leadership.',
    url:'https://www.goodreads.com/shelf/show/instructional-leadership' },
  { type:'article', title:'ASCD Learning Hub & Articles', author:'ASCD',
    description:'Open-access repository of practitioner articles on observation tools, formative assessment, and teacher growth models.',
    url:'https://www.ascd.org/' },
  { type:'article', title:'Wallace Foundation School Leadership Library', author:'Wallace Foundation',
    description:'Free empirical research reports and field toolkits on principal instructional leadership.',
    url:'https://www.wallacefoundation.org/' },
  { type:'article', title:'Instructional Leadership Frameworks (ACRL)', author:'CRL News',
    description:'Academic analysis detailing core functions: defining mission, managing curriculum, monitoring instruction.',
    url:'https://crln.acrl.org/index.php/crlnews/article/view/23725/31114' },
  { type:'toolkit', title:'Danielson Framework for Teaching', author:'Charlotte Danielson',
    description:'Standardized observation and feedback rubric covering Planning, Classroom Environment, Instruction, Professional Responsibilities.',
    url:'https://www.danielsongroup.org/framework/' },
  { type:'toolkit', title:'Marzano Focused Teacher Evaluation Model', author:'Robert Marzano',
    description:'Research-based teacher evaluation framework organized around standards-based planning and instruction.',
    url:'https://www.marzanoresources.com/' },
  { type:'toolkit', title:'NSRF Data-Driven Dialogue Protocols', author:'National School Reform Faculty',
    description:'Structured guides for analyzing assessment data—Predict, Observe, Infer.',
    url:'https://www.nsrfharmony.org/' },
  { type:'toolkit', title:'KoboToolbox — Free Data Collection', author:'KoboToolbox / Harvard Humanitarian Initiative',
    description:'Open-source tool for classroom walkthroughs and family surveys—works offline, syncs later.',
    url:'https://www.kobotoolbox.org/' }
];

const DB = {
  get: function(k, d) { try { var v = localStorage.getItem('ilm_' + k); return v ? JSON.parse(v) : (d || null); } catch(e) { return d || null; } },
  set: function(k, v) { try { localStorage.setItem('ilm_' + k, JSON.stringify(v)); } catch(e) {} },
  remove: function(k) { localStorage.removeItem('ilm_' + k); },
  push: function(k, item) { var a = DB.get(k, []); a.push(item); DB.set(k, a); return item; }
};

(function seed() {
  if (!DB.get('admin_seeded')) {
    var users = DB.get('users', []);
    users.push({
      id: 1, full_name: 'Administrator', email: 'admin@ilmacademy.com',
      password: 'admin123', role: 'admin', package: 'admin',
      created_at: new Date().toISOString()
    });
    DB.set('users', users);
    DB.set('admin_seeded', true);
  }
})();

var STATE = {
  user: DB.get('currentUser'),
  route: 'home',
  selectedPackage: null,
  currentLesson: null,
  resourceFilter: 'all'
};

function go(route, params) {
  params = params || {};
  STATE.route = route;
  for (var k in params) STATE[k] = params[k];
  window.scrollTo(0, 0);
  renderNav();
  render();
}

function renderNav() {
  var u = STATE.user;
  var show = function(id, on) {
    var el = document.getElementById(id);
    if (el) el.classList.toggle('hidden', !on);
  };
  show('navAuth', !u);
  show('navDash', !!u && u.role !== 'admin');
  show('navAdmin', !!u && u.role === 'admin');
  show('navLogout', !!u);
  document.querySelectorAll('.nav-links a').forEach(function(a) {
    a.classList.toggle('active', a.dataset.nav === STATE.route);
  });
}

function render() {
  var app = document.getElementById('app');
  var html = '';
  switch (STATE.route) {
    case 'home':        html = renderHome(); break;
    case 'framework':   html = renderFramework(); break;
    case 'resources':   html = renderResources(); break;
    case 'toolkit':     html = renderToolkit(); break;
    case 'login':       html = renderLogin(); break;
    case 'payment':     html = renderPayment(); break;
    case 'thankyou':    html = renderThankYou(); break;
    case 'dashboard':   html = STATE.user ? renderDashboard() : renderLogin(); break;
    case 'lesson':      html = STATE.user ? renderLesson() : renderLogin(); break;
    case 'certificate': html = STATE.user ? renderCertificate() : renderLogin(); break;
    case 'admin':       html = (STATE.user && STATE.user.role === 'admin') ? renderAdmin() : renderLogin(); break;
    default:            html = renderHome();
  }
  app.innerHTML = html;
  if (STATE.route === 'admin') bindAdminTabs();
  if (STATE.route === 'lesson') loadLessonQuiz();
}

function renderHome() {
  return `
  <div class="hero">
    <div class="hero-badge">🎓 Aligned with Harvard GSE & ASCD Standards</div>
    <h1>Become the Instructional Leader Your School Needs</h1>
    <p class="subtitle">An 8-week masterclass built around the four pillars of 21st-century instructional leadership: Vision & Tech, Data & AI, Coaching, and Equity.</p>
    <div class="btn-row" style="justify-content:center">
      <button class="btn btn-secondary" onclick="go('home');setTimeout(function(){scrollToId('pricing')},150)">Enroll Now</button>
      <button class="btn btn-outline" style="color:#fff;border-color:#fff" onclick="go('framework')">View Framework</button>
    </div>
    <div class="trust-badges">
      <span>✓ 4-Pillar Framework</span>
      <span>✓ 30+ Curated Resources</span>
      <span>✓ Certificate of Completion</span>
      <span>✓ From Birr 50</span>
    </div>
  </div>

  <section>
    <h2>Is This You?</h2>
    <div class="grid grid-4">
      <div class="card problem-card"><span class="icon">😰</span><h3>Overwhelmed</h3><p>Drowning in admin tasks, no time for instructional leadership.</p></div>
      <div class="card problem-card"><span class="icon">📊</span><h3>Data-Rich, Insight-Poor</h3><p>Data everywhere, no time to turn it into action.</p></div>
      <div class="card problem-card"><span class="icon">👥</span><h3>Teacher Resistance</h3><p>Feedback isn't landing—teachers see you as evaluator, not coach.</p></div>
      <div class="card problem-card"><span class="icon">🤖</span><h3>AI Anxiety</h3><p>AI is transforming education and you don't know where to start.</p></div>
    </div>
  </section>

  <section style="background:#fff">
    <h2>Built on the 4 Pillars</h2>
    <p class="section-sub">Every module maps to one of the four pillars. Grounded in Harvard GSE, ASCD, Robinson, Hattie, DuFour, Marzano, and Knight.</p>
    <div class="pillar-diagram">
      <div class="pillar-core">21st Century Instructional Leadership Core</div>
      <div class="pillar-arrow">↓</div>
      <div class="pillar-grid">
        <div class="pillar-box"><span class="p-icon">🔭</span><h4>Vision & Tech</h4><p>Future-ready curriculum & digital integration</p></div>
        <div class="pillar-box"><span class="p-icon">📊</span><h4>Data & AI</h4><p>Evidence-based decisions & formative culture</p></div>
        <div class="pillar-box"><span class="p-icon">🎯</span><h4>Coaching</h4><p>Observation, feedback & PLCs</p></div>
        <div class="pillar-box"><span class="p-icon">⚖️</span><h4>Equity & Culture</h4><p>Inclusive, culturally responsive learning</p></div>
      </div>
    </div>
  </section>

  <section id="curriculum">
    <h2>Your 8-Week Journey</h2>
    <p class="section-sub">Six modules. Each includes lessons, exercises, quizzes, and curated external resources.</p>
    <div class="grid grid-3">
      ${COURSE.modules.map(m => `
        <div class="card module-card">
          <div class="module-num">${String(m.number).padStart(2,'0')}</div>
          <h3>${m.title}</h3>
          <p>${m.description}</p>
          <ul>${m.lessons.slice(0,3).map(l => `<li>${l.title}</li>`).join('')}</ul>
        </div>
      `).join('')}
    </div>
  </section>

  <section id="pricing" style="background:#fff">
    <h2>Invest in Your Leadership</h2>
    <p class="section-sub">Affordable pricing in Ethiopian Birr. All plans include lifetime access.</p>
    <div class="grid grid-3">
      <div class="card pricing-card">
        <h3>Self-Paced</h3>
        <div class="price">Birr 50</div>
        <ul>
          <li>✓ All 6 Modules</li>
          <li>✓ Full Resource Library</li>
          <li>✓ Certificate of Completion</li>
          <li>✓ 6 Months Access</li>
        </ul>
        <button class="btn btn-full" onclick="startPayment('basic')">Enroll Now</button>
      </div>
      <div class="card pricing-card featured">
        <div class="pricing-badge">Most Popular</div>
        <h3>Premium</h3>
        <div class="price">Birr 150</div>
        <ul>
          <li>✓ Everything in Self-Paced</li>
          <li>✓ Weekly Live Q&A</li>
          <li>✓ 1-on-1 Coaching Call</li>
          <li>✓ Capstone Feedback</li>
          <li>✓ Harvard/ASCD Pathway Guide</li>
          <li>✓ Lifetime Access</li>
        </ul>
        <button class="btn btn-full" onclick="startPayment('premium')">Enroll Now</button>
      </div>
      <div class="card pricing-card">
        <h3>School Team</h3>
        <div class="price">Birr 500</div>
        <ul>
          <li>✓ Up to 5 Leaders</li>
          <li>✓ All Premium Features</li>
          <li>✓ Private Cohort</li>
          <li>✓ Custom Case Studies</li>
          <li>✓ On-Site Workshop (Optional)</li>
        </ul>
        <button class="btn btn-full" onclick="startPayment('school')">Enroll Now</button>
      </div>
    </div>
  </section>
  `;
}

function renderFramework() {
  return `
  <section>
    <div class="container">
      <h2>21st Century Instructional Leadership Framework</h2>
      <p class="section-sub">The complete framework underpinning this masterclass.</p>
      <div class="pillar-diagram">
        <div class="pillar-core">21st Century Instructional Leadership Core</div>
        <div class="pillar-arrow">↓</div>
        <div class="pillar-grid">
          <div class="pillar-box"><span class="p-icon">🔭</span><h4>Vision & Tech</h4><p>Future-ready curriculum & digital/AI integration</p></div>
          <div class="pillar-box"><span class="p-icon">📊</span><h4>Data & AI</h4><p>Formative culture & evidence-based practice</p></div>
          <div class="pillar-box"><span class="p-icon">🎯</span><h4>Professional Coaching</h4><p>Observation, feedback & PLCs</p></div>
          <div class="pillar-box"><span class="p-icon">⚖️</span><h4>Equity & Culture</h4><p>Inclusive, culturally responsive learning</p></div>
        </div>
      </div>

      <div class="card" style="margin-bottom:24px">
        <h3>1. Executive Summary & Core Definition</h3>
        <p><strong>Instructional Leadership in the 21st Century</strong> shifts the role of educational leaders from traditional administrative managers to <strong>catalysts of learning, innovation, and continuous growth</strong>.</p>
        <p style="margin-top:10px">In today's dynamic educational landscape—marked by rapid digital transformation, artificial intelligence, diverse learning needs, and shifting global competencies—instructional leaders must cultivate adaptive learning environments.</p>
      </div>

      <h3 style="color:var(--primary);margin:30px 0 14px;font-size:22px">2. Key Pillars</h3>
      <div class="grid grid-2">
        <div class="card">
          <h3>🔭 A. Visionary & Technology-Enhanced Leadership</h3>
          <p><strong>Digital & AI Integration:</strong> Strategically integrating technology, digital tools, and emerging AI frameworks to enhance engagement, streamline assessments, and personalize learning pathways.</p>
          <p style="margin-top:10px"><strong>Future-Ready Curriculum:</strong> Promoting 21st-century skills—critical thinking, creativity, collaboration, communication, and digital literacy.</p>
        </div>
        <div class="card">
          <h3>📊 B. Data-Informed & Results-Based Decision Making</h3>
          <p><strong>Formative Assessment Culture:</strong> Shifting focus from purely summative evaluations to continuous, real-time diagnostic and formative assessments.</p>
          <p style="margin-top:10px"><strong>Evidence-Based Practice:</strong> Utilizing data tools (KoboToolbox, dashboards, student growth metrics) to identify learning gaps.</p>
        </div>
        <div class="card">
          <h3>🎯 C. Instructional Coaching & Continuous Capacity Building</h3>
          <p><strong>Observation & Rapid Feedback:</strong> Short, frequent walkthroughs followed by actionable, growth-oriented feedback cycles.</p>
          <p style="margin-top:10px"><strong>PLCs:</strong> Fostering collaborative teacher teams that continuously reflect on practice.</p>
        </div>
        <div class="card">
          <h3>⚖️ D. Inclusive, Culturally Responsive & Equitable Learning</h3>
          <p><strong>Universal Design & Access:</strong> Ensuring all learners have equitable access to high-quality instruction.</p>
          <p style="margin-top:10px"><strong>Indigenous & Contextualized Knowledge:</strong> Respecting local languages, mother-tongue instruction, and community values.</p>
        </div>
      </div>

      <h3 style="color:var(--primary);margin:40px 0 14px;font-size:22px">3. Core Functions</h3>
      <table class="framework-table">
        <thead><tr><th>Leadership Domain</th><th>Key Strategic Action</th><th>Impact on Learning</th></tr></thead>
        <tbody>
          <tr><td class="domain">Defining the Mission</td><td>Establishing clear, measurable, and shared goals.</td><td>Aligns staff focus on shared priorities.</td></tr>
          <tr><td class="domain">Managing Curriculum & Instruction</td><td>Aligning standards, learning materials, and pedagogy.</td><td>Guarantees rigor, relevance, consistency.</td></tr>
          <tr><td class="domain">Coaching & Mentoring Teachers</td><td>Facilitating peer observations and targeted professional development.</td><td>Elevates teaching quality and retention.</td></tr>
          <tr><td class="domain">Monitoring & Evaluation</td><td>Systematic reviews using logical frameworks and MEAL systems.</td><td>Ensures accountability and real-time adjustment.</td></tr>
        </tbody>
      </table>

      <h3 style="color:var(--primary);margin:40px 0 14px;font-size:22px">4. Key Takeaways</h3>
      <div class="card">
        <blockquote style="border-left:4px solid var(--accent);background:#fffaf0;padding:16px 20px;border-radius:6px;font-style:italic;color:var(--primary);margin-bottom:16px">
          <strong>The Principal/Leader as the Primary Learner:</strong> Effective instructional leaders do not simply manage instruction; they actively participate in learning.
        </blockquote>
        <ul style="padding-left:20px">
          <li style="margin-bottom:8px"><strong>Shift from Compliance to Growth:</strong> Observations should empower teachers.</li>
          <li><strong>Actionable Next Steps:</strong> Every classroom visit should result in one clear, high-leverage bite-sized action step.</li>
        </ul>
      </div>
    </div>
  </section>`;
}

function renderResources() {
  var filter = STATE.resourceFilter || 'all';
  var filtered = filter === 'all' ? RESOURCES : RESOURCES.filter(function(r) { return r.type === filter; });
  return `
  <section>
    <div class="container">
      <h2>📚 Resource Library</h2>
      <p class="section-sub">Curated collection of the world's best instructional leadership resources.</p>
      <div class="filter-bar">
        <button class="filter-btn ${filter==='all'?'active':''}" onclick="filterResources('all')">All (${RESOURCES.length})</button>
        <button class="filter-btn ${filter==='certification'?'active':''}" onclick="filterResources('certification')">🎓 Certifications</button>
        <button class="filter-btn ${filter==='book'?'active':''}" onclick="filterResources('book')">📕 Books</button>
        <button class="filter-btn ${filter==='article'?'active':''}" onclick="filterResources('article')">📄 Research</button>
        <button class="filter-btn ${filter==='toolkit'?'active':''}" onclick="filterResources('toolkit')">🧰 Toolkits</button>
      </div>
      <div class="grid grid-3">
        ${filtered.map(function(r) {
          return '<div class="resource-card ' + r.type + '">' +
            '<span class="resource-type">' + r.type + '</span>' +
            '<h3>' + r.title + '</h3>' +
            '<p class="author">' + r.author + '</p>' +
            '<p>' + r.description + '</p>' +
            '<a class="res-link" href="' + r.url + '" target="_blank" rel="noopener">' +
              (r.type === 'book' ? 'View Book →' : r.type === 'certification' ? 'View Program →' : r.type === 'toolkit' ? 'Access Toolkit →' : 'Read More →') +
            '</a></div>';
        }).join('')}
      </div>
    </div>
  </section>`;
}

function filterResources(type) { STATE.resourceFilter = type; render(); }

function renderToolkit() {
  var toolkits = RESOURCES.filter(function(r) { return r.type === 'toolkit'; });
  return `
  <section>
    <div class="container">
      <h2>🧰 Instructional Leadership Toolkit</h2>
      <p class="section-sub">Frameworks and protocols used in real schools for observation, feedback, and data analysis.</p>
      <div class="grid grid-3">
        ${toolkits.map(function(t) {
          return '<div class="resource-card toolkit">' +
            '<span class="resource-type">Toolkit</span>' +
            '<h3>' + t.title + '</h3>' +
            '<p class="author">' + t.author + '</p>' +
            '<p>' + t.description + '</p>' +
            '<a class="res-link" href="' + t.url + '" target="_blank" rel="noopener">Access Framework →</a>' +
            '</div>';
        }).join('')}
      </div>
      <div class="card" style="max-width:900px;margin:40px auto 0">
        <h3>How to Use These Tools</h3>
        <ol class="step-list" style="margin-top:14px">
          <li><strong>Choose your observation framework</strong> — Danielson (4 domains) or Marzano (60 elements).</li>
          <li><strong>Adopt NSRF Data-Driven Dialogue</strong> for team data meetings.</li>
          <li><strong>Align feedback to Leverage Leadership</strong> — weekly, not annual.</li>
          <li><strong>Ground coaching in Knight's Partnership Principles.</strong></li>
          <li><strong>Deploy KoboToolbox</strong> for walkthroughs and surveys.</li>
          <li><strong>Map to ASCD or Harvard GSE certification</strong> for advanced credentials.</li>
        </ol>
      </div>
    </div>
  </section>`;
}

function renderLogin() {
  return `
  <div class="auth-page">
    <div class="auth-card">
      <h1>Welcome Back</h1>
      <p class="auth-sub">Log in to continue your leadership journey</p>
      <form onsubmit="handleLogin(event)">
        <div class="form-group"><label>Email Address</label>
          <input type="email" name="email" required placeholder="you@example.com"></div>
        <div class="form-group"><label>Password</label>
          <input type="password" name="password" required placeholder="••••••••"></div>
        <button type="submit" class="btn btn-full">Log In</button>
      </form>
      <div class="auth-footer">
        <p>Don't have an account? <a onclick="go('home');setTimeout(function(){scrollToId('pricing')},150)">Enroll Now</a></p>
        <p style="margin-top:8px;font-size:12px;color:#a0aec0">Admin demo: admin@ilmacademy.com / admin123</p>
      </div>
    </div>
  </div>`;
}

function handleLogin(e) {
  e.preventDefault();
  var fd = new FormData(e.target);
  var email = (fd.get('email') || '').toLowerCase().trim();
  var pass = fd.get('password') || '';
  var users = DB.get('users', []);
  var user = users.find(function(u) { return u.email.toLowerCase() === email && u.password === pass; });
  if (!user) { toast('error', 'Invalid email or password'); return; }
  STATE.user = user;
  DB.set('currentUser', user);
  toast('success', 'Welcome back, ' + user.full_name + '!');
  go(user.role === 'admin' ? 'admin' : 'dashboard');
}

function logout() {
  STATE.user = null;
  DB.remove('currentUser');
  toast('info', 'Logged out');
  go('home');
}

function startPayment(pkg) {
  STATE.selectedPackage = pkg;
  go('payment', { selectedPackage: pkg });
}

function renderPayment() {
  var pkg = STATE.selectedPackage || 'premium';
  var info = PACKAGES[pkg];
  return `
  <section style="min-height:70vh">
    <div class="container">
      <h2>Complete Your Enrollment</h2>
      <p class="section-sub">You're one step away from transforming your leadership</p>
      <div class="payment-layout">
        <div><div class="pay-box">
          <h3>Order Summary</h3>
          <div class="summary-row"><span>Course</span><span>Instructional Leadership Masterclass</span></div>
          <div class="summary-row"><span>Package</span><span>${info.name}</span></div>
          <div class="summary-row"><span>Total</span><span>Birr ${info.price.toLocaleString()}</span></div>
        </div></div>
        <div><div class="pay-box">
          <h3>Payment Instructions</h3>
          <div class="pay-steps"><ol>
            <li>Open Telebirr / M-Pesa Ethiopia / CBE Birr</li>
            <li>Select "Send Money"</li>
            <li>Enter number: <span class="hl">${CONFIG.paymentNumber}</span></li>
            <li>Enter amount: <span class="hl">Birr ${info.price.toLocaleString()}</span></li>
            <li>Use your <strong>full name</strong> as reference</li>
            <li>Complete the transaction</li>
            <li>Fill the form below</li>
          </ol></div>
          <form onsubmit="handlePaymentSubmit(event)">
            <input type="hidden" name="package" value="${pkg}">
            <div class="form-group"><label>Full Name *</label><input type="text" name="full_name" required></div>
            <div class="form-group"><label>Email Address *</label><input type="email" name="email" required></div>
            <div class="form-group"><label>Phone Number *</label><input type="tel" name="phone" required></div>
            <div class="form-group"><label>Transaction Code *</label><input type="text" name="transaction_code" required placeholder="e.g. QWE123456"></div>
            <div class="form-group"><label>Password (for your account) *</label><input type="password" name="password" required minlength="6"></div>
            <button type="submit" class="btn btn-full">Submit Payment Confirmation</button>
          </form>
        </div></div>
      </div>
    </div>
  </section>`;
}

function handlePaymentSubmit(e) {
  e.preventDefault();
  var fd = new FormData(e.target);
  var pkg = fd.get('package');
  var email = (fd.get('email') || '').toLowerCase().trim();
  var users = DB.get('users', []);
  if (users.find(function(u) { return u.email.toLowerCase() === email; })) {
    toast('error', 'This email is already registered. Please log in.');
    return;
  }
  DB.push('enrollments', {
    id: Date.now(),
    full_name: fd.get('full_name'),
    email: email,
    phone: fd.get('phone'),
    password: fd.get('password'),
    transaction_code: fd.get('transaction_code'),
    package_type: pkg,
    amount: PACKAGES[pkg].price,
    status: 'pending',
    created_at: new Date().toISOString()
  });
  toast('success', 'Payment submitted! Await admin verification.');
  setTimeout(function() { go('thankyou'); }, 800);
}

function renderThankYou() {
  return `
  <section style="text-align:center;padding:80px 20px">
    <div style="font-size:72px;margin-bottom:20px">🎉</div>
    <h2>Thank You!</h2>
    <p style="max-width:600px;margin:0 auto 30px;color:var(--text-light)">
      Your payment has been submitted for verification. Our team will review within 24 hours.</p>
    <div class="pay-box" style="max-width:500px;margin:0 auto;text-align:left">
      <h3>What Happens Next</h3>
      <ol class="step-list">
        <li>We verify your payment to ${CONFIG.paymentNumber}</li>
        <li>You receive login credentials by email</li>
        <li>Log in and start learning immediately</li>
      </ol>
    </div>
    <button class="btn" style="margin-top:24px" onclick="go('home')">Back to Home</button>
  </section>`;
}

function renderDashboard() {
  var u = STATE.user;
  var progress = getProgress();
  var pct = progress.total ? Math.round((progress.completed / progress.total) * 100) : 0;
  return `
  <div class="dash">
    <aside class="sidebar">
      <nav class="sidebar-nav">
        <a class="active" onclick="go('dashboard')">📊 Dashboard</a>
        <a onclick="go('framework')">🏛️ Framework</a>
        <a onclick="go('resources')">📚 Resources</a>
        <a onclick="go('toolkit')">🧰 Toolkit</a>
        <a onclick="go('certificate')">🏆 Certificate</a>
        <a onclick="logout()">🚪 Logout</a>
      </nav>
    </aside>
    <main class="dash-main">
      <div class="dash-header">
        <h1>Welcome back, ${u.full_name.split(' ')[0]}! 👋</h1>
        <p>Package: <strong>${(PACKAGES[u.package] && PACKAGES[u.package].name) || 'Premium'}</strong></p>
      </div>
      <div class="progress-card">
        <div class="progress-ring">
          <svg viewBox="0 0 36 36">
            <path class="ring-bg" d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831"/>
            <path class="ring-fill" stroke-dasharray="${pct}, 100" d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831"/>
          </svg>
          <div class="ring-text"><strong>${pct}%</strong><span>Complete</span></div>
        </div>
        <div class="progress-info">
          <h3>Course Progress</h3>
          <p>${progress.completed} of ${progress.total} lessons completed</p>
          <p class="next">Next: ${progress.next}</p>
        </div>
      </div>
      <h2 style="font-size:19px;margin-bottom:14px">📚 Course Modules</h2>
      ${COURSE.modules.map(function(m) {
        var done = m.lessons.filter(function(l) { return isLessonComplete(l.id); }).length;
        var total = m.lessons.length;
        var mpct = Math.round((done/total)*100);
        return '<div class="module-row ' + (done === total ? 'done' : '') + '">' +
          '<div class="num">' + (done === total ? '✓' : m.number) + '</div>' +
          '<div class="info">' +
            '<h4>' + m.title + '</h4>' +
            '<p>' + done + '/' + total + ' lessons · ' + mpct + '% complete</p>' +
            '<div class="progress-bar"><div class="progress-fill" style="width:' + mpct + '%"></div></div>' +
          '</div>' +
          '<button class="btn btn-sm" onclick="openLesson(\'' + m.lessons[0].id + '\')">' +
            (done === total ? 'Review' : done === 0 ? 'Start' : 'Continue') + ' →' +
          '</button></div>';
      }).join('')}
    </main>
  </div>`;
}

function openLesson(lessonId) { go('lesson', { currentLesson: lessonId }); }

function findLesson(id) {
  for (var i = 0; i < COURSE.modules.length; i++) {
    var m = COURSE.modules[i];
    for (var j = 0; j < m.lessons.length; j++) {
      if (m.lessons[j].id === id) return { module: m, lesson: m.lessons[j] };
    }
  }
  return null;
}

function renderLesson() {
  var found = findLesson(STATE.currentLesson);
  if (!found) return '<section><div class="container"><p>Lesson not found.</p></div></section>';
  var m = found.module;
  var lesson = found.lesson;
  var isComplete = isLessonComplete(lesson.id);
  var allLessons = [];
  COURSE.modules.forEach(function(mm) { mm.lessons.forEach(function(ll) { allLessons.push(ll); }); });
  var idx = -1;
  for (var i = 0; i < allLessons.length; i++) { if (allLessons[i].id === lesson.id) { idx = i; break; } }
  var prev = idx > 0 ? allLessons[idx-1] : null;
  var next = idx < allLessons.length - 1 ? allLessons[idx+1] : null;

  return `
  <div class="dash">
    <aside class="sidebar">
      <nav class="sidebar-nav">
        <a onclick="go('dashboard')">← Dashboard</a>
        <div class="section-label">Module ${m.number}</div>
        ${m.lessons.map(function(l) {
          return '<a class="' + (l.id === lesson.id ? 'active' : '') + ' ' + (isLessonComplete(l.id) ? 'done' : '') + '" onclick="openLesson(\'' + l.id + '\')">' +
            (isLessonComplete(l.id) ? '✓' : '○') + ' ' + l.title + '</a>';
        }).join('')}
      </nav>
    </aside>
    <main class="dash-main">
      <div class="lesson-view">
        <p class="lesson-meta">Module ${m.number} · Lesson ${m.lessons.indexOf(lesson)+1} of ${m.lessons.length} · ${lesson.duration} min</p>
        <h2>${lesson.title}</h2>
        <div style="margin-top:22px">${lesson.content}</div>
        <div class="lesson-actions">
          ${prev ? '<button class="btn btn-outline btn-sm" onclick="openLesson(\'' + prev.id + '\')">← Previous</button>' : ''}
          ${isComplete
            ? '<button class="btn btn-success btn-sm">✓ Completed</button>'
            : '<button class="btn btn-sm" onclick="markComplete(\'' + lesson.id + '\')">Mark Complete</button>'}
          ${next ? '<button class="btn btn-sm" onclick="openLesson(\'' + next.id + '\')">Next →</button>'
                 : '<button class="btn btn-secondary btn-sm" onclick="go(\'certificate\')">🏆 View Certificate</button>'}
        </div>
      </div>
    </main>
  </div>`;
}

function markComplete(id) {
  var completed = DB.get('completed_lessons', []);
  if (completed.indexOf(id) === -1) {
    completed.push(id);
    DB.set('completed_lessons', completed);
    toast('success', 'Lesson completed! ✓');
    render();
  }
}

function isLessonComplete(id) {
  return DB.get('completed_lessons', []).indexOf(id) !== -1;
}

function getProgress() {
  var total = 0;
  COURSE.modules.forEach(function(m) { total += m.lessons.length; });
  var completed = DB.get('completed_lessons', []).length;
  var next = 'Start Module 1';
  for (var i = 0; i < COURSE.modules.length; i++) {
    var m = COURSE.modules[i];
    for (var j = 0; j < m.lessons.length; j++) {
      if (!isLessonComplete(m.lessons[j].id)) {
        next = m.title + ' → ' + m.lessons[j].title;
        return { total: total, completed: completed, next: next };
      }
    }
  }
  return { total: total, completed: completed, next: next };
}

function saveExercise(id) {
  var el = document.getElementById('ex-' + id);
  if (!el) return;
  var exercises = DB.get('exercises', {});
  exercises[id] = el.value;
  DB.set('exercises', exercises);
  toast('success', 'Response saved ✓');
}

function submitCapstone() {
  var data = {};
  for (var i = 1; i <= 5; i++) {
    var el = document.getElementById('cap-' + i);
    if (el) data['section_' + i] = el.value;
  }
  var allFilled = true;
  for (var k in data) { if (!data[k].trim()) allFilled = false; }
  if (!allFilled) { toast('error', 'Please fill all sections'); return; }
  var obj = {};
  for (var k2 in data) obj[k2] = data[k2];
  obj.submitted_at = new Date().toISOString();
  DB.set('capstone_' + STATE.user.id, obj);
  ['6-1','6-2','6-3'].forEach(function(id) {
    var completed = DB.get('completed_lessons', []);
    if (completed.indexOf(id) === -1) completed.push(id);
    DB.set('completed_lessons', completed);
  });
  toast('success', '🎉 Capstone submitted! Certificate unlocked.');
  go('certificate');
}

function loadLessonQuiz() {
  var found = findLesson(STATE.currentLesson);
  if (!found) return;
  var quizEl = document.getElementById('quiz-' + found.module.number);
  if (!quizEl) return;
  var questions = QUIZZES[found.module.number];
  if (!questions) return;
  var html = '<form onsubmit="handleQuiz(event,' + found.module.number + ')">';
  questions.forEach(function(q, i) {
    html += '<div style="margin-bottom:18px;padding:16px;background:#fff;border-radius:8px;box-shadow:var(--shadow)">';
    html += '<p style="font-weight:600;margin-bottom:12px">' + (i+1) + '. ' + q.q + '</p>';
    q.options.forEach(function(opt, j) {
      html += '<label style="display:block;padding:10px 12px;border:1px solid var(--border);border-radius:6px;margin-bottom:8px;cursor:pointer">';
      html += '<input type="radio" name="q' + i + '" value="' + j + '" required> ' + opt;
      html += '</label>';
    });
    html += '</div>';
  });
  html += '<button type="submit" class="btn">Submit Quiz</button></form>';
  quizEl.innerHTML = html;
}

function handleQuiz(e, moduleNum) {
  e.preventDefault();
  var fd = new FormData(e.target);
  var questions = QUIZZES[moduleNum];
  var correct = 0;
  questions.forEach(function(q, i) {
    if (parseInt(fd.get('q' + i)) === q.correct) correct++;
  });
  var pct = Math.round((correct / questions.length) * 100);
  if (pct >= 80) {
    toast('success', '🎉 Score: ' + pct + '%! You passed.');
    markComplete(STATE.currentLesson);
  } else {
    toast('error', 'Score: ' + pct + '%. You need 80% to pass. Try again.');
  }
}

function renderCertificate() {
  var u = STATE.user;
  var progress = getProgress();
  var pct = progress.total ? Math.round((progress.completed / progress.total) * 100) : 0;
  var date = new Date().toLocaleDateString('en-US', { year:'numeric', month:'long', day:'numeric' });
  var certNum = 'ILM-' + new Date().getFullYear() + '-' + String(u.id).slice(-6);
  if (pct < 100) {
    return '<section style="text-align:center;padding:80px 20px">' +
      '<div style="font-size:72px;margin-bottom:20px">🔒</div>' +
      '<h2>Certificate Locked</h2>' +
      '<p style="max-width:500px;margin:0 auto 20px;color:var(--text-light)">Complete all ' + progress.total + ' lessons to unlock. You\'re at ' + pct + '%.</p>' +
      '<div class="progress-bar" style="max-width:400px;margin:0 auto 22px"><div class="progress-fill" style="width:' + pct + '%"></div></div>' +
      '<button class="btn" onclick="go(\'dashboard\')">Continue Learning →</button></section>';
  }
  return `
  <section style="padding:40px 20px">
    <div class="container">
      <div style="text-align:center;margin-bottom:22px">
        <h2>🏆 Congratulations!</h2>
        <p style="color:var(--text-light)">Your certificate is ready. Print or save as PDF.</p>
        <div class="btn-row" style="justify-content:center;margin-top:12px">
          <button class="btn" onclick="window.print()">🖨️ Print / Save as PDF</button>
          <button class="btn btn-outline" onclick="go('resources')">📚 Continue Learning</button>
        </div>
      </div>
      <div class="certificate">
        <div class="cert-logo">🎓 ILM ACADEMY</div>
        <h2>CERTIFICATE OF COMPLETION</h2>
        <p class="cert-text">This certificate is proudly presented to</p>
        <div class="cert-name">${u.full_name}</div>
        <p class="cert-text">
          for successfully completing the<br>
          <strong>21st Century Instructional Leadership Masterclass</strong><br>
          An 8-week comprehensive program for school leaders<br>
          <em style="font-size:12px;color:var(--text-light)">Aligned with Harvard GSE and ASCD instructional leadership standards</em>
        </p>
        <div class="cert-meta">
          <div><div class="cert-sig"></div><p>Lead Instructor</p></div>
          <div><p style="font-size:11px">Issued ${date}<br>Certificate No: ${certNum}</p></div>
          <div><div class="cert-sig"></div><p>Program Director</p></div>
        </div>
      </div>
      <div class="cta-strip">
        <h2>What's Next?</h2>
        <p>Advance your credentials with Harvard GSE or ASCD certification.</p>
        <div class="btn-row" style="justify-content:center">
          <a class="btn btn-gold" href="https://www.gse.harvard.edu/professional-education/certificate/instructional-leadership-certificate-ilc" target="_blank" rel="noopener">Harvard GSE ILC →</a>
          <a class="btn btn-secondary" href="https://www.ascd.org/instructional-leader-certification" target="_blank" rel="noopener">ASCD Certification →</a>
        </div>
      </div>
    </div>
  </section>`;
}

function renderAdmin() {
  var enrollments = DB.get('enrollments', []);
  var pending = enrollments.filter(function(e) { return e.status === 'pending'; });
  var confirmed = enrollments.filter(function(e) { return e.status === 'confirmed'; });
  var totalRevenue = 0;
  confirmed.forEach(function(e) { totalRevenue += e.amount || 0; });
  var monthRevenue = 0;
  var now = new Date();
  confirmed.forEach(function(e) {
    var d = new Date(e.confirmed_at || e.created_at);
    if (d.getMonth() === now.getMonth() && d.getFullYear() === now.getFullYear()) {
      monthRevenue += e.amount || 0;
    }
  });
  return `
  <div class="dash">
    <aside class="sidebar">
      <nav class="sidebar-nav">
        <a class="active">📊 Admin Panel</a>
        <a onclick="go('home')">🏠 View Site</a>
        <a onclick="logout()">🚪 Logout</a>
      </nav>
    </aside>
    <main class="dash-main">
      <div class="dash-header">
        <h1>🎓 Admin Dashboard</h1>
        <p>Payments received at <strong>${CONFIG.paymentNumber}</strong> · Currency: <strong>Birr (ETB)</strong></p>
      </div>
      <div class="grid grid-4" style="margin-bottom:26px">
        <div class="stat"><span>Total Revenue</span><strong>Birr ${totalRevenue.toLocaleString()}</strong></div>
        <div class="stat"><span>Confirmed</span><strong>${confirmed.length}</strong></div>
        <div class="stat"><span>Pending</span><strong>${pending.length}</strong></div>
        <div class="stat"><span>This Month</span><strong>Birr ${monthRevenue.toLocaleString()}</strong></div>
      </div>
      <div class="admin-tabs">
        <button class="tab active" data-tab="pending">Pending (${pending.length})</button>
        <button class="tab" data-tab="confirmed">Confirmed (${confirmed.length})</button>
      </div>
      <div class="tab-content active" id="tab-pending">
        <div class="table-wrap"><table>
          <thead><tr><th>ID</th><th>Name</th><th>Email</th><th>Phone</th><th>Package</th><th>Amount</th><th>Transaction</th><th>Actions</th></tr></thead>
          <tbody>
            ${pending.length === 0 ? '<tr><td colspan="8" class="empty-row">No pending enrollments</td></tr>'
              : pending.map(function(p) {
                return '<tr>' +
                  '<td>#' + String(p.id).slice(-6) + '</td>' +
                  '<td>' + p.full_name + '</td><td>' + p.email + '</td><td>' + p.phone + '</td>' +
                  '<td><span class="badge">' + p.package_type + '</span></td>' +
                  '<td><strong>Birr ' + p.amount.toLocaleString() + '</strong></td>' +
                  '<td><code>' + p.transaction_code + '</code></td>' +
                  '<td><div class="btn-row">' +
                    '<button class="btn btn-success btn-sm" onclick="approveEnrollment(' + p.id + ')">✓</button>' +
                    '<button class="btn btn-danger btn-sm" onclick="rejectEnrollment(' + p.id + ')">✗</button>' +
                  '</div></td></tr>';
              }).join('')}
          </tbody>
        </table></div>
      </div>
      <div class="tab-content" id="tab-confirmed">
        <div class="table-wrap"><table>
          <thead><tr><th>ID</th><th>Name</th><th>Email</th><th>Package</th><th>Amount</th><th>Confirmed</th></tr></thead>
          <tbody>
            ${confirmed.length === 0 ? '<tr><td colspan="6" class="empty-row">No confirmed enrollments yet</td></tr>'
              : confirmed.map(function(p) {
                return '<tr>' +
                  '<td>#' + String(p.id).slice(-6) + '</td>' +
                  '<td>' + p.full_name + '</td><td>' + p.email + '</td>' +
                  '<td><span class="badge badge-success">' + p.package_type + '</span></td>' +
                  '<td><strong>Birr ' + p.amount.toLocaleString() + '</strong></td>' +
                  '<td>' + new Date(p.confirmed_at || p.created_at).toLocaleDateString() + '</td></tr>';
              }).join('')}
          </tbody>
        </table></div>
      </div>
    </main>
  </div>`;
}

function bindAdminTabs() {
  document.querySelectorAll('.tab').forEach(function(tab) {
    tab.addEventListener('click', function() {
      document.querySelectorAll('.tab').forEach(function(t) { t.classList.remove('active'); });
      document.querySelectorAll('.tab-content').forEach(function(c) { c.classList.remove('active'); });
      tab.classList.add('active');
      var el = document.getElementById('tab-' + tab.dataset.tab);
      if (el) el.classList.add('active');
    });
  });
}

function approveEnrollment(id) {
  if (!confirm('Approve this enrollment?')) return;
  var enrollments = DB.get('enrollments', []);
  var e = null;
  for (var i = 0; i < enrollments.length; i++) { if (enrollments[i].id === id) { e = enrollments[i]; break; } }
  if (!e) return;
  e.status = 'confirmed';
  e.confirmed_at = new Date().toISOString();
  DB.set('enrollments', enrollments);
  var users = DB.get('users', []);
  var exists = false;
  for (var j = 0; j < users.length; j++) { if (users[j].email.toLowerCase() === e.email.toLowerCase()) { exists = true; break; } }
  if (!exists) {
    users.push({
      id: Date.now(), full_name: e.full_name, email: e.email, phone: e.phone,
      password: e.password, role: 'student', package: e.package_type,
      confirmed: true, created_at: new Date().toISOString()
    });
    DB.set('users', users);
  }
  toast('success', '✅ Approved! ' + e.full_name + ' can now log in.');
  render();
}

function rejectEnrollment(id) {
  var reason = prompt('Reason for rejection:');
  if (reason === null) return;
  var enrollments = DB.get('enrollments', []);
  for (var i = 0; i < enrollments.length; i++) {
    if (enrollments[i].id === id) {
      enrollments[i].status = 'rejected';
      enrollments[i].rejection_reason = reason;
      break;
    }
  }
  DB.set('enrollments', enrollments);
  toast('info', 'Enrollment rejected.');
  render();
}

function scrollToId(id) {
  var el = document.getElementById(id);
  if (el) el.scrollIntoView({ behavior: 'smooth', block: 'start' });
}

function toast(type, message) {
  var div = document.createElement('div');
  div.className = 'toast toast-' + type;
  div.textContent = message;
  document.body.appendChild(div);
  setTimeout(function() { if (div.parentNode) div.parentNode.removeChild(div); }, 3500);
}

renderNav();
render();
</script>
</body>
</html>
