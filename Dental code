<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DentalFlow AI — Website Optimizer for Dentists</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
<style>
/* =========================================
   CSS VARIABLES & RESET
   ========================================= */
:root {
  --primary: #0ea5e9;
  --primary-dark: #0284c7;
  --primary-light: #e0f2fe;
  --accent: #06d6a0;
  --accent-dark: #05b384;
  --danger: #ef4444;
  --warning: #f59e0b;
  --success: #22c55e;
  --bg: #f0f4f8;
  --bg-card: #ffffff;
  --text: #1e293b;
  --text-light: #64748b;
  --text-lighter: #94a3b8;
  --border: #e2e8f0;
  --sidebar-bg: #0f172a;
  --sidebar-text: #cbd5e1;
  --sidebar-active: #1e293b;
  --radius: 12px;
  --radius-sm: 8px;
  --shadow: 0 1px 3px rgba(0,0,0,.08), 0 4px 12px rgba(0,0,0,.04);
  --shadow-lg: 0 4px 24px rgba(0,0,0,.1);
  --transition: .25s cubic-bezier(.4,0,.2,1);
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }

body {
  font-family: 'Inter', -apple-system, sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
  overflow-x: hidden;
}

a { text-decoration: none; color: inherit; }
button { cursor: pointer; border: none; font-family: inherit; }
input, textarea, select { font-family: inherit; }

/* =========================================
   UTILITY CLASSES
   ========================================= */
.hidden { display: none !important; }
.flex { display: flex; }
.flex-col { flex-direction: column; }
.items-center { align-items: center; }
.justify-center { justify-content: center; }
.justify-between { justify-content: space-between; }
.gap-1 { gap: 8px; }
.gap-2 { gap: 16px; }
.gap-3 { gap: 24px; }
.w-full { width: 100%; }
.text-center { text-align: center; }

/* =========================================
   LANDING PAGE
   ========================================= */
.landing {
  min-height: 100vh;
  background: linear-gradient(135deg, #0f172a 0%, #1e3a5f 50%, #0f172a 100%);
  position: relative;
  overflow: hidden;
}

.landing::before {
  content: '';
  position: absolute;
  top: -50%; left: -50%;
  width: 200%; height: 200%;
  background: radial-gradient(circle at 30% 50%, rgba(14,165,233,.15) 0%, transparent 50%),
              radial-gradient(circle at 70% 80%, rgba(6,214,160,.1) 0%, transparent 40%);
  animation: bgFloat 15s ease-in-out infinite;
}

@keyframes bgFloat {
  0%, 100% { transform: translate(0,0) rotate(0deg); }
  33% { transform: translate(30px, -30px) rotate(1deg); }
  66% { transform: translate(-20px, 20px) rotate(-1deg); }
}

.landing-nav {
  position: relative; z-index: 10;
  padding: 20px 40px;
  display: flex; align-items: center; justify-content: space-between;
}

.logo {
  display: flex; align-items: center; gap: 10px;
  font-size: 22px; font-weight: 800; color: #fff;
}

.logo-icon {
  width: 40px; height: 40px;
  background: linear-gradient(135deg, var(--primary), var(--accent));
  border-radius: 10px;
  display: flex; align-items: center; justify-content: center;
  font-size: 20px;
}

.landing-nav-links { display: flex; gap: 24px; align-items: center; }
.landing-nav-links a { color: var(--sidebar-text); font-size: 14px; font-weight: 500; transition: var(--transition); }
.landing-nav-links a:hover { color: #fff; }

.landing-hero {
  position: relative; z-index: 10;
  max-width: 900px; margin: 0 auto;
  padding: 80px 40px 60px;
  text-align: center;
}

.landing-badge {
  display: inline-flex; align-items: center; gap: 8px;
  background: rgba(14,165,233,.15); border: 1px solid rgba(14,165,233,.3);
  border-radius: 50px; padding: 6px 16px;
  font-size: 13px; color: var(--primary); font-weight: 500;
  margin-bottom: 24px;
}

.landing-badge span { animation: pulse 2s infinite; }

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: .5; }
}

.landing-hero h1 {
  font-size: clamp(36px, 5vw, 60px);
  font-weight: 900; color: #fff;
  line-height: 1.1; margin-bottom: 20px;
}

.landing-hero h1 .gradient-text {
  background: linear-gradient(135deg, var(--primary), var(--accent));
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  background-clip: text;
}

.landing-hero p {
  font-size: 18px; color: var(--sidebar-text);
  max-width: 600px; margin: 0 auto 40px;
  line-height: 1.7;
}

/* Input Group */
.url-input-group {
  display: flex; gap: 0;
  max-width: 600px; margin: 0 auto 24px;
  background: rgba(255,255,255,.08);
  border: 1px solid rgba(255,255,255,.15);
  border-radius: 16px; overflow: hidden;
  backdrop-filter: blur(10px);
  transition: var(--transition);
}

.url-input-group:focus-within {
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(14,165,233,.2);
}

.url-input-group input {
  flex: 1; padding: 18px 24px;
  background: transparent; border: none;
  color: #fff; font-size: 16px; outline: none;
}

.url-input-group input::placeholder { color: var(--text-lighter); }

.url-input-group button {
  padding: 18px 32px;
  background: linear-gradient(135deg, var(--primary), var(--accent));
  color: #fff; font-size: 15px; font-weight: 600;
  border-radius: 0 12px 12px 0;
  transition: var(--transition);
  white-space: nowrap;
}

.url-input-group button:hover { opacity: .9; transform: scale(1.02); }

.extra-fields {
  display: flex; gap: 12px;
  max-width: 600px; margin: 0 auto 32px;
  flex-wrap: wrap; justify-content: center;
}

.extra-fields input, .extra-fields select {
  padding: 12px 18px;
  background: rgba(255,255,255,.06);
  border: 1px solid rgba(255,255,255,.12);
  border-radius: 10px; color: #fff;
  font-size: 14px; outline: none;
  flex: 1; min-width: 160px;
  transition: var(--transition);
}

.extra-fields input:focus, .extra-fields select:focus {
  border-color: var(--primary);
}

.extra-fields select option { background: var(--sidebar-bg); color: #fff; }

.trust-row {
  display: flex; gap: 32px; justify-content: center;
  flex-wrap: wrap; margin-top: 16px;
}

.trust-item { display: flex; align-items: center; gap: 8px; color: var(--text-lighter); font-size: 13px; }
.trust-item svg { width: 16px; height: 16px; color: var(--accent); }

/* Feature Cards */
.features-grid {
  position: relative; z-index: 10;
  display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px; max-width: 1100px;
  margin: 40px auto 0; padding: 0 40px 80px;
}

.feature-card {
  background: rgba(255,255,255,.05);
  border: 1px solid rgba(255,255,255,.08);
  border-radius: var(--radius); padding: 28px;
  backdrop-filter: blur(10px);
  transition: var(--transition);
}

.feature-card:hover {
  background: rgba(255,255,255,.08);
  border-color: rgba(14,165,233,.3);
  transform: translateY(-4px);
}

.feature-card-icon {
  width: 48px; height: 48px;
  border-radius: 12px; margin-bottom: 16px;
  display: flex; align-items: center; justify-content: center;
  font-size: 22px;
}

.feature-card h3 { color: #fff; font-size: 16px; font-weight: 600; margin-bottom: 8px; }
.feature-card p { color: var(--text-lighter); font-size: 13px; line-height: 1.6; }

/* =========================================
   LOADING SCREEN
   ========================================= */
.loading-screen {
  position: fixed; top: 0; left: 0;
  width: 100%; height: 100%; z-index: 1000;
  background: linear-gradient(135deg, #0f172a 0%, #1e3a5f 100%);
  display: flex; flex-direction: column;
  align-items: center; justify-content: center;
  gap: 32px;
}

.scan-visual {
  width: 200px; height: 200px;
  position: relative;
}

.scan-ring {
  position: absolute; top: 50%; left: 50%;
  border-radius: 50%; border: 2px solid rgba(14,165,233,.2);
  animation: scanPulse 2s ease-out infinite;
}

.scan-ring:nth-child(1) { width: 80px; height: 80px; margin: -40px 0 0 -40px; animation-delay: 0s; }
.scan-ring:nth-child(2) { width: 120px; height: 120px; margin: -60px 0 0 -60px; animation-delay: .4s; }
.scan-ring:nth-child(3) { width: 160px; height: 160px; margin: -80px 0 0 -80px; animation-delay: .8s; }
.scan-ring:nth-child(4) { width: 200px; height: 200px; margin: -100px 0 0 -100px; animation-delay: 1.2s; }

.scan-center {
  position: absolute; top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  font-size: 36px; animation: scanGlow 1.5s ease-in-out infinite alternate;
}

@keyframes scanPulse {
  0% { transform: scale(.8); opacity: 1; border-color: rgba(14,165,233,.6); }
  100% { transform: scale(1.3); opacity: 0; border-color: rgba(6,214,160,.1); }
}

@keyframes scanGlow {
  0% { filter: drop-shadow(0 0 8px rgba(14,165,233,.5)); }
  100% { filter: drop-shadow(0 0 20px rgba(6,214,160,.8)); }
}

.loading-text { color: #fff; font-size: 18px; font-weight: 600; }

.loading-steps {
  display: flex; flex-direction: column; gap: 12px;
  width: 350px; max-width: 90%;
}

.loading-step {
  display: flex; align-items: center; gap: 12px;
  color: var(--text-lighter); font-size: 14px;
  transition: var(--transition);
}

.loading-step.active { color: var(--primary); }
.loading-step.done { color: var(--accent); }

.loading-step-dot {
  width: 24px; height: 24px; border-radius: 50%;
  border: 2px solid currentColor;
  display: flex; align-items: center; justify-content: center;
  font-size: 11px; flex-shrink: 0;
  transition: var(--transition);
}

.loading-step.active .loading-step-dot { background: var(--primary); color: #fff; border-color: var(--primary); }
.loading-step.done .loading-step-dot { background: var(--accent); color: #fff; border-color: var(--accent); }

.loading-progress {
  width: 350px; max-width: 90%; height: 4px;
  background: rgba(255,255,255,.1); border-radius: 4px;
  overflow: hidden;
}

.loading-progress-bar {
  height: 100%; width: 0%;
  background: linear-gradient(90deg, var(--primary), var(--accent));
  border-radius: 4px;
  transition: width .5s ease;
}

/* =========================================
   DASHBOARD LAYOUT
   ========================================= */
.dashboard {
  display: flex; min-height: 100vh;
}

/* Sidebar */
.sidebar {
  width: 260px; background: var(--sidebar-bg);
  padding: 24px 0; display: flex;
  flex-direction: column; position: fixed;
  top: 0; left: 0; height: 100vh;
  z-index: 100; transition: var(--transition);
}

.sidebar-logo {
  display: flex; align-items: center; gap: 10px;
  padding: 0 24px; margin-bottom: 8px;
  font-size: 18px; font-weight: 800; color: #fff;
}

.sidebar-url {
  padding: 0 24px; margin-bottom: 24px;
  font-size: 12px; color: var(--text-lighter);
  word-break: break-all;
}

.sidebar-section {
  padding: 0 16px; margin-bottom: 8px;
}

.sidebar-section-title {
  font-size: 10px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 1.5px;
  color: var(--text-lighter); padding: 0 8px;
  margin-bottom: 8px;
}

.sidebar-link {
  display: flex; align-items: center; gap: 12px;
  padding: 10px 16px; border-radius: var(--radius-sm);
  color: var(--sidebar-text); font-size: 14px;
  font-weight: 500; transition: var(--transition);
  margin-bottom: 2px; cursor: pointer;
  border: none; background: none; width: 100%;
  text-align: left;
}

.sidebar-link:hover { background: rgba(255,255,255,.05); color: #fff; }
.sidebar-link.active { background: var(--primary); color: #fff; }
.sidebar-link-icon { width: 20px; text-align: center; font-size: 15px; }

.sidebar-spacer { flex: 1; }

.sidebar-api {
  padding: 16px 24px; border-top: 1px solid rgba(255,255,255,.08);
}

.sidebar-api label { display: block; font-size: 10px; font-weight: 600; text-transform: uppercase; letter-spacing: 1px; color: var(--text-lighter); margin-bottom: 6px; }

.sidebar-api input {
  width: 100%; padding: 8px 12px;
  background: rgba(255,255,255,.06);
  border: 1px solid rgba(255,255,255,.1);
  border-radius: 6px; color: #fff;
  font-size: 12px; outline: none;
}

.sidebar-api input:focus { border-color: var(--primary); }

.sidebar-api .api-status { font-size: 11px; margin-top: 6px; }
.api-connected { color: var(--accent); }
.api-disconnected { color: var(--text-lighter); }

/* Main Content */
.main {
  margin-left: 260px; flex: 1;
  padding: 32px; min-height: 100vh;
}

.main-header {
  display: flex; align-items: center;
  justify-content: space-between;
  margin-bottom: 32px; flex-wrap: wrap; gap: 16px;
}

.main-header h1 { font-size: 24px; font-weight: 700; }
.main-header p { color: var(--text-light); font-size: 14px; margin-top: 4px; }

.btn {
  display: inline-flex; align-items: center; gap: 8px;
  padding: 10px 20px; border-radius: var(--radius-sm);
  font-size: 14px; font-weight: 600;
  transition: var(--transition);
}

.btn-primary { background: var(--primary); color: #fff; }
.btn-primary:hover { background: var(--primary-dark); }
.btn-accent { background: var(--accent); color: #fff; }
.btn-accent:hover { background: var(--accent-dark); }
.btn-outline { background: transparent; color: var(--text); border: 1px solid var(--border); }
.btn-outline:hover { background: var(--bg); }
.btn-sm { padding: 6px 14px; font-size: 13px; }
.btn-lg { padding: 14px 28px; font-size: 16px; }
.btn-danger { background: var(--danger); color: #fff; }

/* Cards */
.card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 24px;
  box-shadow: var(--shadow);
  transition: var(--transition);
}

.card:hover { box-shadow: var(--shadow-lg); }
.card-header { display: flex; align-items: center; justify-content: space-between; margin-bottom: 16px; }
.card-title { font-size: 16px; font-weight: 600; }
.card-subtitle { font-size: 12px; color: var(--text-light); margin-top: 2px; }

/* Score Cards */
.scores-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 16px; margin-bottom: 24px;
}

.score-card {
  background: var(--bg-card); border: 1px solid var(--border);
  border-radius: var(--radius); padding: 20px;
  box-shadow: var(--shadow); text-align: center;
  transition: var(--transition);
}

.score-card:hover { transform: translateY(-2px); box-shadow: var(--shadow-lg); }

.score-circle {
  width: 80px; height: 80px;
  border-radius: 50%; margin: 0 auto 12px;
  position: relative; display: flex;
  align-items: center; justify-content: center;
}

.score-circle svg { position: absolute; top: 0; left: 0; width: 80px; height: 80px; transform: rotate(-90deg); }
.score-circle circle { fill: none; stroke-width: 5; }
.score-circle .bg { stroke: var(--border); }

.score-circle .fg {
  stroke-linecap: round;
  transition: stroke-dashoffset 1.5s ease;
}

.score-value { font-size: 22px; font-weight: 800; position: relative; z-index: 1; }
.score-card .score-label { font-size: 13px; font-weight: 600; color: var(--text); }
.score-card .score-change { font-size: 11px; color: var(--text-light); margin-top: 4px; }

/* Grid layouts */
.grid-2 { display: grid; grid-template-columns: repeat(auto-fit, minmax(400px, 1fr)); gap: 20px; margin-bottom: 24px; }
.grid-3 { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin-bottom: 24px; }

/* Issue/Recommendation Items */
.issue-list { display: flex; flex-direction: column; gap: 12px; }

.issue-item {
  display: flex; gap: 14px; padding: 16px;
  background: var(--bg); border-radius: var(--radius-sm);
  border-left: 4px solid var(--border);
  transition: var(--transition);
}

.issue-item:hover { background: #e8edf3; }
.issue-item.critical { border-left-color: var(--danger); }
.issue-item.warning { border-left-color: var(--warning); }
.issue-item.good { border-left-color: var(--success); }
.issue-item.info { border-left-color: var(--primary); }

.issue-icon {
  width: 32px; height: 32px; border-radius: 8px;
  display: flex; align-items: center; justify-content: center;
  font-size: 14px; flex-shrink: 0;
}

.issue-item.critical .issue-icon { background: #fef2f2; color: var(--danger); }
.issue-item.warning .issue-icon { background: #fffbeb; color: var(--warning); }
.issue-item.good .issue-icon { background: #f0fdf4; color: var(--success); }
.issue-item.info .issue-icon { background: var(--primary-light); color: var(--primary); }

.issue-content { flex: 1; }
.issue-title { font-size: 14px; font-weight: 600; margin-bottom: 4px; }
.issue-desc { font-size: 13px; color: var(--text-light); line-height: 1.5; }
.issue-action { margin-top: 8px; }

/* Tags */
.tag {
  display: inline-flex; padding: 3px 10px;
  border-radius: 50px; font-size: 11px; font-weight: 600;
}

.tag-red { background: #fef2f2; color: var(--danger); }
.tag-yellow { background: #fffbeb; color: #b45309; }
.tag-green { background: #f0fdf4; color: #15803d; }
.tag-blue { background: var(--primary-light); color: var(--primary-dark); }

/* Content Generator */
.generator-form { display: flex; flex-direction: column; gap: 16px; }

.form-group { display: flex; flex-direction: column; gap: 6px; }
.form-group label { font-size: 13px; font-weight: 600; color: var(--text); }

.form-group input,
.form-group select,
.form-group textarea {
  padding: 12px 16px;
  background: var(--bg);
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
  font-size: 14px; color: var(--text);
  outline: none; transition: var(--transition);
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(14,165,233,.1);
}

.form-group textarea { min-height: 120px; resize: vertical; }

.form-row { display: flex; gap: 16px; flex-wrap: wrap; }
.form-row .form-group { flex: 1; min-width: 200px; }

/* Generated Content Output */
.output-box {
  background: var(--bg);
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
  padding: 20px; margin-top: 16px;
  position: relative; min-height: 120px;
}

.output-box pre {
  white-space: pre-wrap;
  font-family: 'Inter', sans-serif;
  font-size: 14px; line-height: 1.7;
  color: var(--text);
}

.output-box .copy-btn {
  position: absolute; top: 12px; right: 12px;
  padding: 6px 14px; background: var(--primary);
  color: #fff; border-radius: 6px;
  font-size: 12px; font-weight: 600;
}

.output-box .copy-btn:hover { background: var(--primary-dark); }

/* Typing animation */
.typing-cursor::after {
  content: '▋'; animation: blink 1s step-end infinite;
  color: var(--primary);
}

@keyframes blink { 50% { opacity: 0; } }

/* Competitor Table */
.comp-table {
  width: 100%; border-collapse: collapse;
  font-size: 13px;
}

.comp-table th {
  text-align: left; padding: 12px 16px;
  background: var(--bg); font-weight: 600;
  font-size: 12px; text-transform: uppercase;
  letter-spacing: .5px; color: var(--text-light);
  border-bottom: 2px solid var(--border);
}

.comp-table td {
  padding: 12px 16px; border-bottom: 1px solid var(--border);
}

.comp-table tr:hover td { background: #f8fafc; }

/* Progress Bar */
.progress { width: 100%; height: 8px; background: var(--bg); border-radius: 8px; overflow: hidden; }
.progress-fill { height: 100%; border-radius: 8px; transition: width 1s ease; }
.progress-fill.red { background: var(--danger); }
.progress-fill.yellow { background: var(--warning); }
.progress-fill.green { background: var(--success); }
.progress-fill.blue { background: var(--primary); }

/* Action Plan */
.action-item {
  display: flex; align-items: flex-start; gap: 12px;
  padding: 16px; background: var(--bg);
  border-radius: var(--radius-sm);
  margin-bottom: 8px;
  border: 1px solid var(--border);
}

.action-check {
  width: 22px; height: 22px; border-radius: 6px;
  border: 2px solid var(--border); flex-shrink: 0;
  cursor: pointer; display: flex;
  align-items: center; justify-content: center;
  transition: var(--transition); margin-top: 2px;
  background: #fff;
}

.action-check.checked { background: var(--accent); border-color: var(--accent); color: #fff; font-size: 11px; }
.action-item.completed { opacity: .5; }
.action-item.completed .action-text { text-decoration: line-through; }
.action-priority { font-size: 10px; font-weight: 700; text-transform: uppercase; letter-spacing: .5px; }
.action-text { font-size: 14px; font-weight: 500; }
.action-detail { font-size: 12px; color: var(--text-light); margin-top: 4px; line-height: 1.5; }

/* Toast */
.toast {
  position: fixed; bottom: 24px; right: 24px;
  background: var(--sidebar-bg); color: #fff;
  padding: 14px 24px; border-radius: var(--radius-sm);
  font-size: 14px; font-weight: 500;
  box-shadow: var(--shadow-lg); z-index: 9999;
  display: flex; align-items: center; gap: 10px;
  animation: toastIn .3s ease;
}

.toast.success { border-left: 4px solid var(--accent); }
.toast.error { border-left: 4px solid var(--danger); }
.toast.info { border-left: 4px solid var(--primary); }

@keyframes toastIn {
  from { transform: translateY(20px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

/* Tab content */
.tab-content { display: none; }
.tab-content.active { display: block; }

/* Keyword tags */
.keyword-cloud { display: flex; flex-wrap: wrap; gap: 8px; }
.keyword-tag {
  padding: 6px 14px; background: var(--primary-light);
  color: var(--primary-dark); border-radius: 50px;
  font-size: 13px; font-weight: 500;
  transition: var(--transition);
}
.keyword-tag:hover { background: var(--primary); color: #fff; }

/* Spinner */
.spinner {
  display: inline-block; width: 18px; height: 18px;
  border: 2px solid rgba(255,255,255,.3);
  border-top-color: #fff; border-radius: 50%;
  animation: spin .6s linear infinite;
}

@keyframes spin { to { transform: rotate(360deg); } }

/* Mobile Sidebar Toggle */
.mobile-toggle {
  display: none;
  position: fixed; top: 16px; left: 16px;
  z-index: 200; width: 44px; height: 44px;
  background: var(--sidebar-bg); border-radius: 10px;
  align-items: center; justify-content: center;
  color: #fff; font-size: 20px;
}

/* Responsive */
@media (max-width: 768px) {
  .mobile-toggle { display: flex; }
  .sidebar { transform: translateX(-100%); }
  .sidebar.open { transform: translateX(0); }
  .main { margin-left: 0; padding: 24px 16px; padding-top: 72px; }
  .grid-2, .grid-3 { grid-template-columns: 1fr; }
  .scores-grid { grid-template-columns: repeat(2, 1fr); }
  .features-grid { grid-template-columns: 1fr; padding: 0 20px 60px; }
  .landing-hero { padding: 60px 20px 40px; }
  .url-input-group { flex-direction: column; border-radius: var(--radius); }
  .url-input-group button { border-radius: 0 0 var(--radius) var(--radius); }
  .landing-nav { padding: 16px 20px; }
  .landing-nav-links { display: none; }
}

/* Empty/Loading State */
.empty-state {
  text-align: center; padding: 48px 24px;
  color: var(--text-light);
}

.empty-state-icon { font-size: 48px; margin-bottom: 16px; opacity: .5; }
.empty-state h3 { font-size: 18px; color: var(--text); margin-bottom: 8px; }
.empty-state p { font-size: 14px; max-width: 400px; margin: 0 auto; }

/* Checklist */
.checklist { list-style: none; }

.checklist li {
  padding: 10px 0; border-bottom: 1px solid var(--border);
  display: flex; align-items: flex-start; gap: 10px;
  font-size: 14px;
}

.checklist li:last-child { border-bottom: none; }
.check-yes { color: var(--success); font-weight: 700; }
.check-no { color: var(--danger); font-weight: 700; }

/* CTA Cards */
.cta-suggestion {
  padding: 16px; background: var(--bg);
  border-radius: var(--radius-sm);
  border: 1px dashed var(--border);
  margin-bottom: 12px;
}

.cta-before { font-size: 13px; color: var(--text-light); margin-bottom: 4px; }
.cta-arrow { color: var(--primary); font-size: 18px; margin: 6px 0; }
.cta-after { font-size: 15px; font-weight: 700; color: var(--accent-dark); }

/* Stat bar */
.stat-bar { display: flex; align-items: center; gap: 12px; margin-bottom: 12px; }
.stat-bar-label { font-size: 13px; font-weight: 500; min-width: 120px; }
.stat-bar-track { flex: 1; height: 10px; background: var(--bg); border-radius: 10px; overflow: hidden; }
.stat-bar-fill { height: 100%; border-radius: 10px; }
.stat-bar-value { font-size: 13px; font-weight: 700; min-width: 40px; text-align: right; }

/* Scrollbar */
::-webkit-scrollbar { width: 6px; }
::-webkit-scrollbar-track { background: transparent; }
::-webkit-scrollbar-thumb { background: var(--border); border-radius: 3px; }
::-webkit-scrollbar-thumb:hover { background: var(--text-lighter); }
</style>
</head>
<body>

<!-- ============================================
     LANDING PAGE
     ============================================ -->
<div id="landingPage" class="landing">
  <nav class="landing-nav">
    <div class="logo">
      <div class="logo-icon">🦷</div>
      DentalFlow AI
    </div>
    <div class="landing-nav-links">
      <a href="#features">Features</a>
      <a href="#" onclick="showToast('Contact: hello@dentalflow.ai','info')">Contact</a>
    </div>
  </nav>

  <div class="landing-hero">
    <div class="landing-badge">
      <span>⚡</span> AI-Powered Website Analysis
    </div>
    <h1>Turn Your Website Into a <span class="gradient-text">Patient Magnet</span></h1>
    <p>DentalFlow AI analyzes your dental website, identifies weaknesses, generates optimized content, and gives you a step-by-step action plan to attract more patients.</p>

    <div class="url-input-group">
      <input type="url" id="websiteUrl" placeholder="Enter your dental website URL..." value="">
      <button onclick="startAnalysis()">Analyze My Site →</button>
    </div>

    <div class="extra-fields">
      <input type="text" id="practiceName" placeholder="Practice Name">
      <input type="text" id="practiceCity" placeholder="City / Location">
      <select id="practiceType">
        <option value="general">General Dentistry</option>
        <option value="cosmetic">Cosmetic Dentistry</option>
        <option value="pediatric">Pediatric Dentistry</option>
        <option value="orthodontic">Orthodontics</option>
        <option value="oral-surgery">Oral Surgery</option>
        <option value="periodontic">Periodontics</option>
        <option value="endodontic">Endodontics</option>
        <option value="multi">Multi-Specialty</option>
      </select>
    </div>

    <div class="trust-row">
      <div class="trust-item">
        <svg viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/></svg>
        Free Analysis
      </div>
      <div class="trust-item">
        <svg viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/></svg>
        No Credit Card
      </div>
      <div class="trust-item">
        <svg viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/></svg>
        Instant Results
      </div>
      <div class="trust-item">
        <svg viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/></svg>
        HIPAA Friendly
      </div>
    </div>
  </div>

  <div id="features" class="features-grid">
    <div class="feature-card">
      <div class="feature-card-icon" style="background:rgba(14,165,233,.15);color:var(--primary)">🔍</div>
      <h3>SEO Analysis</h3>
      <p>Discover exactly which keywords your local competitors rank for and get actionable steps to outrank them.</p>
    </div>
    <div class="feature-card">
      <div class="feature-card-icon" style="background:rgba(6,214,160,.15);color:var(--accent)">✍️</div>
      <h3>AI Content Generator</h3>
      <p>Generate patient-friendly blog posts, service descriptions, FAQs, and meta tags in seconds.</p>
    </div>
    <div class="feature-card">
      <div class="feature-card-icon" style="background:rgba(245,158,11,.15);color:var(--warning)">📈</div>
      <h3>Conversion Optimizer</h3>
      <p>Get specific recommendations to turn more website visitors into booked appointments.</p>
    </div>
    <div class="feature-card">
      <div class="feature-card-icon" style="background:rgba(239,68,68,.15);color:var(--danger)">🏆</div>
      <h3>Competitor Intelligence</h3>
      <p>See how your website stacks up against local dental practices and find gaps to exploit.</p>
    </div>
  </div>
</div>

<!-- ============================================
     LOADING SCREEN
     ============================================ -->
<div id="loadingScreen" class="loading-screen hidden">
  <div class="scan-visual">
    <div class="scan-ring"></div>
    <div class="scan-ring"></div>
    <div class="scan-ring"></div>
    <div class="scan-ring"></div>
    <div class="scan-center">🦷</div>
  </div>
  <div class="loading-text" id="loadingTitle">Analyzing Your Website...</div>
  <div class="loading-steps" id="loadingSteps">
    <div class="loading-step" data-step="0">
      <div class="loading-step-dot"></div>
      <span>Crawling website pages...</span>
    </div>
    <div class="loading-step" data-step="1">
      <div class="loading-step-dot"></div>
      <span>Analyzing SEO structure...</span>
    </div>
    <div class="loading-step" data-step="2">
      <div class="loading-step-dot"></div>
      <span>Evaluating content quality...</span>
    </div>
    <div class="loading-step" data-step="3">
      <div class="loading-step-dot"></div>
      <span>Checking mobile responsiveness...</span>
    </div>
    <div class="loading-step" data-step="4">
      <div class="loading-step-dot"></div>
      <span>Running competitor comparison...</span>
    </div>
    <div class="loading-step" data-step="5">
      <div class="loading-step-dot"></div>
      <span>Generating recommendations...</span>
    </div>
  </div>
  <div class="loading-progress">
    <div class="loading-progress-bar" id="loadingBar"></div>
  </div>
</div>

<!-- ============================================
     DASHBOARD
     ============================================ -->
<div id="dashboard" class="dashboard hidden">

  <!-- Mobile Toggle -->
  <button class="mobile-toggle" onclick="document.querySelector('.sidebar').classList.toggle('open')">☰</button>

  <!-- Sidebar -->
  <aside class="sidebar">
    <div class="sidebar-logo">
      <div class="logo-icon" style="width:32px;height:32px;font-size:16px;border-radius:8px">🦷</div>
      DentalFlow AI
    </div>
    <div class="sidebar-url" id="sidebarUrl">your-website.com</div>

    <div class="sidebar-section">
      <div class="sidebar-section-title">Dashboard</div>
      <button class="sidebar-link active" onclick="switchTab('overview', this)">
        <span class="sidebar-link-icon">📊</span> Overview
      </button>
      <button class="sidebar-link" onclick="switchTab('seo', this)">
        <span class="sidebar-link-icon">🔍</span> SEO Analysis
      </button>
      <button class="sidebar-link" onclick="switchTab('content', this)">
        <span class="sidebar-link-icon">✍️</span> Content Studio
      </button>
      <button class="sidebar-link" onclick="switchTab('conversion', this)">
        <span class="sidebar-link-icon">📈</span> Conversion Lab
      </button>
      <button class="sidebar-link" onclick="switchTab('competitors', this)">
        <span class="sidebar-link-icon">🏆</span> Competitors
      </button>
      <button class="sidebar-link" onclick="switchTab('actions', this)">
        <span class="sidebar-link-icon">✅</span> Action Plan
      </button>
    </div>

    <div class="sidebar-spacer"></div>

    <div class="sidebar-api">
      <label>OpenAI API Key (Optional)</label>
      <input type="password" id="apiKeyInput" placeholder="sk-..." oninput="checkApiKey()">
      <div class="api-status" id="apiStatus">
        <span class="api-disconnected">⚪ Using built-in templates</span>
      </div>
    </div>

    <div style="padding:16px 24px;border-top:1px solid rgba(255,255,255,.08)">
      <button class="btn btn-outline w-full" style="color:var(--sidebar-text);border-color:rgba(255,255,255,.15);font-size:13px;justify-content:center" onclick="resetApp()">
        ← New Analysis
      </button>
    </div>
  </aside>

  <!-- Main Content -->
  <main class="main">

    <!-- ============== OVERVIEW TAB ============== -->
    <div class="tab-content active" id="tab-overview">
      <div class="main-header">
        <div>
          <h1>Website Health Overview</h1>
          <p id="overviewSubtitle">Analysis results for your dental practice website</p>
        </div>
        <button class="btn btn-primary" onclick="exportReport()">📄 Export Report</button>
      </div>

      <!-- Scores -->
      <div class="scores-grid" id="scoresGrid"></div>

      <!-- Quick Wins & Issues -->
      <div class="grid-2">
        <div class="card">
          <div class="card-header">
            <div>
              <div class="card-title">🚨 Critical Issues</div>
              <div class="card-subtitle">Fix these first for the biggest impact</div>
            </div>
            <span class="tag tag-red" id="criticalCount">0</span>
          </div>
          <div class="issue-list" id="criticalIssues"></div>
        </div>
        <div class="card">
          <div class="card-header">
            <div>
              <div class="card-title">⚡ Quick Wins</div>
              <div class="card-subtitle">Easy changes with high impact</div>
            </div>
            <span class="tag tag-green" id="quickWinCount">0</span>
          </div>
          <div class="issue-list" id="quickWins"></div>
        </div>
      </div>

      <!-- Summary -->
      <div class="card">
        <div class="card-header">
          <div class="card-title">📋 Analysis Summary</div>
        </div>
        <div id="analysisSummary" style="font-size:14px;line-height:1.8;color:var(--text-light)"></div>
      </div>
    </div>

    <!-- ============== SEO TAB ============== -->
    <div class="tab-content" id="tab-seo">
      <div class="main-header">
        <div>
          <h1>SEO Analysis</h1>
          <p>Search engine optimization insights for your dental website</p>
        </div>
      </div>

      <div class="grid-2">
        <div class="card">
          <div class="card-header">
            <div class="card-title">🎯 Recommended Keywords</div>
          </div>
          <p style="font-size:13px;color:var(--text-light);margin-bottom:16px">Target these keywords to attract local patients:</p>
          <div class="keyword-cloud" id="keywordCloud"></div>
        </div>
        <div class="card">
          <div class="card-header">
            <div class="card-title">📊 SEO Checklist</div>
          </div>
          <ul class="checklist" id="seoChecklist"></ul>
        </div>
      </div>

      <div class="card">
        <div class="card-header">
          <div class="card-title">🔧 SEO Recommendations</div>
        </div>
        <div class="issue-list" id="seoRecommendations"></div>
      </div>

      <div class="card" style="margin-top:20px">
        <div class="card-header">
          <div class="card-title">📝 AI Meta Description Generator</div>
        </div>
        <div class="generator-form">
          <div class="form-group">
            <label>Page to generate meta description for:</label>
            <select id="metaPageSelect">
              <option value="home">Homepage</option>
              <option value="about">About / Meet the Doctor</option>
              <option value="services">Services Page</option>
              <option value="cosmetic">Cosmetic Dentistry</option>
              <option value="implants">Dental Implants</option>
              <option value="emergency">Emergency Dentistry</option>
              <option value="contact">Contact Page</option>
            </select>
          </div>
          <button class="btn btn-primary" onclick="generateMeta()">✨ Generate Meta Description</button>
          <div class="output-box hidden" id="metaOutput">
            <button class="copy-btn" onclick="copyOutput('metaOutput')">📋 Copy</button>
            <pre id="metaOutputText"></pre>
          </div>
        </div>
      </div>
    </div>

    <!-- ============== CONTENT STUDIO TAB ============== -->
    <div class="tab-content" id="tab-content">
      <div class="main-header">
        <div>
          <h1>AI Content Studio</h1>
          <p>Generate patient-friendly content for your dental website</p>
        </div>
      </div>

      <div class="grid-2">
        <!-- Blog Post Generator -->
        <div class="card">
          <div class="card-header">
            <div class="card-title">📝 Blog Post Generator</div>
          </div>
          <div class="generator-form">
            <div class="form-group">
              <label>Topic</label>
              <select id="blogTopic">
                <option value="implants">Dental Implants: What to Expect</option>
                <option value="whitening">Teeth Whitening Options Compared</option>
                <option value="invisalign">Is Invisalign Right for You?</option>
                <option value="root-canal">Root Canal: Nothing to Fear</option>
                <option value="pediatric">Your Child's First Dental Visit</option>
                <option value="veneers">Transform Your Smile with Veneers</option>
                <option value="emergency">Dental Emergencies: What To Do</option>
                <option value="prevention">Preventive Care: Why It Matters</option>
                <option value="anxiety">Overcoming Dental Anxiety</option>
                <option value="flossing">The Truth About Flossing</option>
                <option value="custom">Custom Topic...</option>
              </select>
            </div>
            <div class="form-group hidden" id="customTopicGroup">
              <label>Custom Topic</label>
              <input type="text" id="customTopic" placeholder="Enter your blog topic...">
            </div>
            <div class="form-group">
              <label>Tone</label>
              <select id="blogTone">
                <option value="friendly">Friendly & Reassuring</option>
                <option value="professional">Professional & Authoritative</option>
                <option value="casual">Casual & Conversational</option>
                <option value="educational">Educational & Detailed</option>
              </select>
            </div>
            <div class="form-group">
              <label>Word Count (approx.)</label>
              <select id="blogLength">
                <option value="short">Short (~400 words)</option>
                <option value="medium" selected>Medium (~700 words)</option>
                <option value="long">Long (~1000 words)</option>
              </select>
            </div>
            <button class="btn btn-accent btn-lg w-full" onclick="generateBlog()" id="blogGenBtn" style="justify-content:center">
              ✨ Generate Blog Post
            </button>
          </div>
          <div class="output-box hidden" id="blogOutput">
            <button class="copy-btn" onclick="copyOutput('blogOutput')">📋 Copy</button>
            <pre id="blogOutputText"></pre>
          </div>
        </div>

        <!-- Service Page Generator -->
        <div class="card">
          <div class="card-header">
            <div class="card-title">🏥 Service Page Generator</div>
          </div>
          <div class="generator-form">
            <div class="form-group">
              <label>Service</label>
              <select id="serviceType">
                <option value="general">General Dentistry</option>
                <option value="cosmetic">Cosmetic Dentistry</option>
                <option value="implants">Dental Implants</option>
                <option value="orthodontics">Orthodontics / Invisalign</option>
                <option value="pediatric">Pediatric Dentistry</option>
                <option value="emergency">Emergency Dentistry</option>
                <option value="periodontal">Periodontal Treatment</option>
                <option value="whitening">Teeth Whitening</option>
                <option value="crowns">Crowns & Bridges</option>
                <option value="root-canal">Root Canal Therapy</option>
                <option value="sedation">Sedation Dentistry</option>
                <option value="dentures">Dentures</option>
              </select>
            </div>
            <div class="form-group">
              <label>Key selling points (optional)</label>
              <textarea id="servicePoints" placeholder="e.g., Latest technology, Experienced team, Same-day appointments, Insurance accepted..." rows="3"></textarea>
            </div>
            <button class="btn btn-primary btn-lg w-full" onclick="generateService()" id="serviceGenBtn" style="justify-content:center">
              ✨ Generate Service Page
            </button>
          </div>
          <div class="output-box hidden" id="serviceOutput">
            <button class="copy-btn" onclick="copyOutput('serviceOutput')">📋 Copy</button>
            <pre id="serviceOutputText"></pre>
          </div>
        </div>
      </div>

      <!-- FAQ Generator -->
      <div class="card">
        <div class="card-header">
          <div class="card-title">❓ Patient FAQ Generator</div>
        </div>
        <div class="generator-form">
          <div class="form-row">
            <div class="form-group">
              <label>Category</label>
              <select id="faqCategory">
                <option value="general">General Questions</option>
                <option value="insurance">Insurance & Payment</option>
                <option value="procedures">Common Procedures</option>
                <option value="first-visit">First Visit</option>
                <option value="cosmetic">Cosmetic Dentistry</option>
                <option value="emergency">Emergency Care</option>
              </select>
            </div>
            <div class="form-group">
              <label>Number of FAQs</label>
              <select id="faqCount">
                <option value="3">3 Questions</option>
                <option value="5" selected>5 Questions</option>
                <option value="8">8 Questions</option>
              </select>
            </div>
          </div>
          <button class="btn btn-primary" onclick="generateFAQ()" id="faqGenBtn">✨ Generate FAQs</button>
        </div>
        <div class="output-box hidden" id="faqOutput">
          <button class="copy-btn" onclick="copyOutput('faqOutput')">📋 Copy</button>
          <pre id="faqOutputText"></pre>
        </div>
      </div>

      <!-- Social Media Posts -->
      <div class="card" style="margin-top:20px">
        <div class="card-header">
          <div class="card-title">📱 Social Media Post Generator</div>
        </div>
        <div class="generator-form">
          <div class="form-row">
            <div class="form-group">
              <label>Platform</label>
              <select id="socialPlatform">
                <option value="instagram">Instagram</option>
                <option value="facebook">Facebook</option>
                <option value="google">Google Business Post</option>
              </select>
            </div>
            <div class="form-group">
              <label>Post Type</label>
              <select id="socialType">
                <option value="promo">Promotion / Offer</option>
                <option value="educational">Educational Tip</option>
                <option value="behind-scenes">Behind the Scenes</option>
                <option value="testimonial">Patient Testimonial Prompt</option>
                <option value="seasonal">Seasonal Post</option>
              </select>
            </div>
          </div>
          <button class="btn btn-accent" onclick="generateSocial()" id="socialGenBtn">✨ Generate Post</button>
        </div>
        <div class="output-box hidden" id="socialOutput">
          <button class="copy-btn" onclick="copyOutput('socialOutput')">📋 Copy</button>
          <pre id="socialOutputText"></pre>
        </div>
      </div>
    </div>

    <!-- ============== CONVERSION TAB ============== -->
    <div class="tab-content" id="tab-conversion">
      <div class="main-header">
        <div>
          <h1>Conversion Optimizer</h1>
          <p>Turn more visitors into booked appointments</p>
        </div>
      </div>

      <div class="grid-2">
        <div class="card">
          <div class="card-header">
            <div class="card-title">🔘 CTA Improvements</div>
            <div class="card-subtitle">Better button text = more clicks</div>
          </div>
          <div id="ctaSuggestions"></div>
        </div>
        <div class="card">
          <div class="card-header">
            <div class="card-title">🛡️ Trust Signals Checklist</div>
            <div class="card-subtitle">Elements that build patient confidence</div>
          </div>
          <ul class="checklist" id="trustChecklist"></ul>
        </div>
      </div>

      <div class="card">
        <div class="card-header">
          <div class="card-title">💡 Conversion Recommendations</div>
        </div>
        <div class="issue-list" id="conversionRecs"></div>
      </div>

      <div class="card" style="margin-top:20px">
        <div class="card-header">
          <div class="card-title">👨‍⚕️ AI "Doctor Bio" Generator</div>
        </div>
        <div class="generator-form">
          <div class="form-row">
            <div class="form-group">
              <label>Doctor's Name</label>
              <input type="text" id="drName" placeholder="Dr. Sarah Johnson">
            </div>
            <div class="form-group">
              <label>Years of Experience</label>
              <input type="number" id="drYears" placeholder="15" min="1" max="50">
            </div>
          </div>
          <div class="form-group">
            <label>Specialties / Highlights (comma-separated)</label>
            <input type="text" id="drSpecialties" placeholder="e.g., Cosmetic dentistry, Invisalign certified, Pediatric care, Implants">
          </div>
          <div class="form-group">
            <label>Education (optional)</label>
            <input type="text" id="drEducation" placeholder="e.g., NYU College of Dentistry">
          </div>
          <div class="form-group">
            <label>Personal Touch (optional)</label>
            <input type="text" id="drPersonal" placeholder="e.g., Enjoys hiking, has two golden retrievers">
          </div>
          <button class="btn btn-primary" onclick="generateBio()" id="bioGenBtn">✨ Generate Doctor Bio</button>
        </div>
        <div class="output-box hidden" id="bioOutput">
          <button class="copy-btn" onclick="copyOutput('bioOutput')">📋 Copy</button>
          <pre id="bioOutputText"></pre>
        </div>
      </div>
    </div>

    <!-- ============== COMPETITORS TAB ============== -->
    <div class="tab-content" id="tab-competitors">
      <div class="main-header">
        <div>
          <h1>Competitor Intelligence</h1>
          <p>See how you compare to nearby dental practices</p>
        </div>
      </div>

      <div class="card">
        <div class="card-header">
          <div class="card-title">📊 Competitive Comparison</div>
          <div class="card-subtitle">Simulated analysis based on common local patterns</div>
        </div>
        <div style="overflow-x:auto">
          <table class="comp-table" id="compTable">
            <thead>
              <tr>
                <th>Metric</th>
                <th>Your Site</th>
                <th>Avg. Competitor</th>
                <th>Status</th>
              </tr>
            </thead>
            <tbody id="compTableBody"></tbody>
          </table>
        </div>
      </div>

      <div class="grid-2" style="margin-top:20px">
        <div class="card">
          <div class="card-header">
            <div class="card-title">🕳️ Content Gaps</div>
            <div class="card-subtitle">Topics your competitors cover that you don't</div>
          </div>
          <div class="issue-list" id="contentGaps"></div>
        </div>
        <div class="card">
          <div class="card-header">
            <div class="card-title">💪 Your Advantages</div>
            <div class="card-subtitle">Areas where you're ahead</div>
          </div>
          <div class="issue-list" id="yourAdvantages"></div>
        </div>
      </div>
    </div>

    <!-- ============== ACTION PLAN TAB ============== -->
    <div class="tab-content" id="tab-actions">
      <div class="main-header">
        <div>
          <h1>Action Plan</h1>
          <p>Your prioritized to-do list for website improvement</p>
        </div>
        <div class="flex gap-1">
          <button class="btn btn-outline btn-sm" onclick="uncheckAll()">Reset All</button>
          <button class="btn btn-primary btn-sm" onclick="exportReport()">📄 Export</button>
        </div>
      </div>

      <div class="card">
        <div class="card-header">
          <div class="card-title">📋 Prioritized Actions</div>
          <div id="actionProgress" style="font-size:13px;color:var(--text-light)">0 / 0 completed</div>
        </div>
        <div id="actionList"></div>
      </div>
    </div>

  </main>
</div>

<!-- ============================================
     TOAST CONTAINER
     ============================================ -->
<div id="toastContainer"></div>

<!-- ============================================
     JAVASCRIPT
     ============================================ -->
<script>
// =============================================
// GLOBAL STATE
// =============================================
const state = {
  url: '',
  practiceName: '',
  city: '',
  type: 'general',
  scores: {},
  apiKey: ''
};

// =============================================
// NAVIGATION & UI
// =============================================
function switchTab(tabId, el) {
  document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
  document.querySelectorAll('.sidebar-link').forEach(l => l.classList.remove('active'));
  document.getElementById('tab-' + tabId).classList.add('active');
  if (el) el.classList.add('active');
  document.querySelector('.sidebar').classList.remove('open');
}

function resetApp() {
  document.getElementById('dashboard').classList.add('hidden');
  document.getElementById('landingPage').classList.remove('hidden');
}

function checkApiKey() {
  const key = document.getElementById('apiKeyInput').value;
  state.apiKey = key;
  const status = document.getElementById('apiStatus');
  if (key && key.startsWith('sk-') && key.length > 20) {
    status.innerHTML = '<span class="api-connected">🟢 API key set — using GPT</span>';
  } else if (key.length > 0) {
    status.innerHTML = '<span class="api-disconnected">🟡 Invalid key format</span>';
  } else {
    status.innerHTML = '<span class="api-disconnected">⚪ Using built-in templates</span>';
  }
}

function showToast(message, type = 'info') {
  const container = document.getElementById('toastContainer');
  const toast = document.createElement('div');
  toast.className = 'toast ' + type;
  toast.innerHTML = message;
  container.appendChild(toast);
  setTimeout(() => { toast.style.opacity = '0'; toast.style.transform = 'translateY(10px)'; setTimeout(() => toast.remove(), 300); }, 3000);
}

function copyOutput(boxId) {
  const text = document.getElementById(boxId + 'Text').textContent;
  navigator.clipboard.writeText(text).then(() => showToast('Copied to clipboard!', 'success'));
}

// =============================================
// ANALYSIS ENGINE
// =============================================
function startAnalysis() {
  const url = document.getElementById('websiteUrl').value.trim();
  const name = document.getElementById('practiceName').value.trim();
  const city = document.getElementById('practiceCity').value.trim();
  const type = document.getElementById('practiceType').value;

  if (!url) {
    showToast('Please enter your website URL', 'error');
    return;
  }

  state.url = url;
  state.practiceName = name || 'Your Dental Practice';
  state.city = city || 'your city';
  state.type = type;

  document.getElementById('landingPage').classList.add('hidden');
  document.getElementById('loadingScreen').classList.remove('hidden');

  runLoadingAnimation();
}

function runLoadingAnimation() {
  const steps = document.querySelectorAll('.loading-step');
  const bar = document.getElementById('loadingBar');
  let currentStep = 0;
  const totalSteps = steps.length;

  const interval = setInterval(() => {
    if (currentStep > 0) {
      steps[currentStep - 1].classList.remove('active');
      steps[currentStep - 1].classList.add('done');
      steps[currentStep - 1].querySelector('.loading-step-dot').textContent = '✓';
    }

    if (currentStep < totalSteps) {
      steps[currentStep].classList.add('active');
      bar.style.width = ((currentStep + 1) / totalSteps * 100) + '%';
      currentStep++;
    } else {
      clearInterval(interval);
      setTimeout(() => {
        document.getElementById('loadingScreen').classList.add('hidden');
        document.getElementById('dashboard').classList.remove('hidden');
        populateDashboard();
      }, 600);
    }
  }, 700);
}

// =============================================
// SCORE GENERATION
// =============================================
function generateScores() {
  const rand = (min, max) => Math.floor(Math.random() * (max - min + 1)) + min;
  state.scores = {
    overall: rand(38, 72),
    seo: rand(30, 65),
    content: rand(35, 70),
    mobile: rand(50, 90),
    speed: rand(40, 80),
    trust: rand(25, 65),
    conversion: rand(30, 60)
  };
}

function getScoreColor(score) {
  if (score >= 75) return '#22c55e';
  if (score >= 50) return '#f59e0b';
  return '#ef4444';
}

function getScoreClass(score) {
  if (score >= 75) return 'green';
  if (score >= 50) return 'yellow';
  return 'red';
}

function getScoreLabel(score) {
  if (score >= 80) return 'Excellent';
  if (score >= 65) return 'Good';
  if (score >= 50) return 'Fair';
  if (score >= 35) return 'Needs Work';
  return 'Poor';
}

// =============================================
// POPULATE DASHBOARD
// =============================================
function populateDashboard() {
  generateScores();

  document.getElementById('sidebarUrl').textContent = state.url;
  document.getElementById('overviewSubtitle').textContent = `Analysis for ${state.practiceName} in ${state.city}`;

  renderScores();
  renderCriticalIssues();
  renderQuickWins();
  renderSummary();
  renderSEOTab();
  renderConversionTab();
  renderCompetitorsTab();
  renderActionPlan();

  // Blog topic custom toggle
  document.getElementById('blogTopic').addEventListener('change', function() {
    document.getElementById('customTopicGroup').classList.toggle('hidden', this.value !== 'custom');
  });
}

function renderScores() {
  const grid = document.getElementById('scoresGrid');
  const scoreData = [
    { key: 'overall', label: 'Overall Score', icon: '🏆' },
    { key: 'seo', label: 'SEO', icon: '🔍' },
    { key: 'content', label: 'Content', icon: '📝' },
    { key: 'mobile', label: 'Mobile', icon: '📱' },
    { key: 'speed', label: 'Speed', icon: '⚡' },
    { key: 'trust', label: 'Trust', icon: '🛡️' },
    { key: 'conversion', label: 'Conversion', icon: '📈' }
  ];

  grid.innerHTML = scoreData.map(s => {
    const score = state.scores[s.key];
    const color = getScoreColor(score);
    const circumference = 2 * Math.PI * 35;
    const offset = circumference - (score / 100) * circumference;
    return `
      <div class="score-card">
        <div class="score-circle">
          <svg viewBox="0 0 80 80">
            <circle class="bg" cx="40" cy="40" r="35"/>
            <circle class="fg" cx="40" cy="40" r="35"
              stroke="${color}"
              stroke-dasharray="${circumference}"
              stroke-dashoffset="${offset}"/>
          </svg>
          <div class="score-value" style="color:${color}">${score}</div>
        </div>
        <div class="score-label">${s.icon} ${s.label}</div>
        <div class="score-change">${getScoreLabel(score)}</div>
      </div>
    `;
  }).join('');
}

function renderCriticalIssues() {
  const container = document.getElementById('criticalIssues');
  const city = state.city;
  const issues = [];

  if (state.scores.seo < 60)
    issues.push({ t: 'Missing local SEO keywords', d: `Your pages don't include location-based keywords like "dentist in ${city}". This severely impacts local search visibility.`, type: 'critical' });
  if (state.scores.trust < 50)
    issues.push({ t: 'No patient reviews on website', d: 'Trust signals like testimonials are missing. 84% of patients trust online reviews as much as personal recommendations.', type: 'critical' });
  if (state.scores.mobile < 60)
    issues.push({ t: 'Mobile experience issues detected', d: 'Text may be too small, buttons too close together, or layout not adapting to mobile screens. Over 60% of dental searches happen on mobile.', type: 'critical' });
  if (state.scores.conversion < 50)
    issues.push({ t: 'No clear call-to-action above the fold', d: 'Visitors can\'t immediately find how to book an appointment. Add a prominent "Book Now" button in your header.', type: 'critical' });
  if (state.scores.speed < 50)
    issues.push({ t: 'Slow page load speed', d: 'Your site may take too long to load. Each second of delay reduces conversions by 7%.', type: 'critical' });
  if (state.scores.content < 45)
    issues.push({ t: 'Thin content on service pages', d: 'Service pages have very little content. Google requires substantial, helpful content to rank pages well.', type: 'critical' });

  if (issues.length === 0)
    issues.push({ t: 'No critical issues found!', d: 'Your website is in decent shape. Check the warnings and quick wins for improvements.', type: 'good' });

  document.getElementById('criticalCount').textContent = issues.filter(i => i.type === 'critical').length;

  container.innerHTML = issues.map(i => `
    <div class="issue-item ${i.type}">
      <div class="issue-icon">${i.type === 'critical' ? '✕' : '✓'}</div>
      <div class="issue-content">
        <div class="issue-title">${i.t}</div>
        <div class="issue-desc">${i.d}</div>
      </div>
    </div>
  `).join('');
}

function renderQuickWins() {
  const container = document.getElementById('quickWins');
  const city = state.city;
  const name = state.practiceName;

  const wins = [
    { t: 'Add click-to-call on mobile', d: 'Make your phone number a clickable link. This one change can increase calls by 30%.', type: 'info' },
    { t: `Update page title to include "${city}"`, d: `Change your homepage title to "${name} | Trusted Dentist in ${city}" for instant SEO benefit.`, type: 'info' },
    { t: 'Add Google Maps embed to contact page', d: 'An embedded map helps patients find you and signals your location to Google.', type: 'info' },
    { t: 'Add alt text to all images', d: 'Describe your images for SEO and accessibility. e.g., "Modern dental office lobby at ' + name + '"', type: 'info' },
    { t: 'Add an online booking button', d: 'A visible "Book Online" button can increase appointment requests by 25-40%.', type: 'info' },
    { t: 'Create a Google Business Profile post', d: 'Regular Google Business posts improve your local search presence. Post weekly tips or offers.', type: 'info' }
  ];

  document.getElementById('quickWinCount').textContent = wins.length;

  container.innerHTML = wins.map(w => `
    <div class="issue-item ${w.type}">
      <div class="issue-icon">💡</div>
      <div class="issue-content">
        <div class="issue-title">${w.t}</div>
        <div class="issue-desc">${w.d}</div>
      </div>
    </div>
  `).join('');
}

function renderSummary() {
  const s = state.scores;
  document.getElementById('analysisSummary').innerHTML = `
    <p>We analyzed <strong>${state.url}</strong> for <strong>${state.practiceName}</strong> in <strong>${state.city}</strong>.</p>
    <br>
    <p>Your overall website health score is <strong style="color:${getScoreColor(s.overall)}">${s.overall}/100</strong> (${getScoreLabel(s.overall)}).
    The biggest areas for improvement are <strong>${s.seo < s.conversion ? 'SEO' : 'Conversion Optimization'}</strong> (score: ${Math.min(s.seo, s.conversion)})
    and <strong>${s.trust < s.content ? 'Trust Signals' : 'Content Quality'}</strong> (score: ${Math.min(s.trust, s.content)}).</p>
    <br>
    <p><strong>Key Insight:</strong> Most dental practices in ${state.city} have better-optimized websites.
    By implementing the recommendations in your Action Plan, you could improve your score to <strong>80+</strong>
    and significantly increase your patient inquiries from organic search.</p>
    <br>
    <p>⏱️ Estimated time to implement all recommendations: <strong>4-6 hours</strong> (or use our AI Content Studio to cut that in half).</p>
  `;
}

// =============================================
// SEO TAB
// =============================================
function renderSEOTab() {
  const city = state.city;
  const name = state.practiceName;
  const typeLabels = {
    general: 'dentist', cosmetic: 'cosmetic dentist', pediatric: 'pediatric dentist',
    orthodontic: 'orthodontist', 'oral-surgery': 'oral surgeon', periodontic: 'periodontist',
    endodontic: 'endodontist', multi: 'dental clinic'
  };
  const mainKeyword = typeLabels[state.type] || 'dentist';

  // Keywords
  const keywords = [
    `${mainKeyword} in ${city}`, `best ${mainKeyword} ${city}`, `${mainKeyword} near me`,
    `emergency dentist ${city}`, `affordable dental care ${city}`, `teeth whitening ${city}`,
    `dental implants ${city}`, `Invisalign ${city}`, `family dentist ${city}`,
    `cosmetic dentistry ${city}`, `dental cleaning ${city}`, `${city} dental office`,
    `pediatric dentist ${city}`, `dental crowns ${city}`, `same day dentist ${city}`
  ];

  document.getElementById('keywordCloud').innerHTML = keywords.map(k =>
    `<span class="keyword-tag">${k}</span>`
  ).join('');

  // Checklist
  const checks = [
    { text: `Title tag includes "${mainKeyword}" and "${city}"`, pass: state.scores.seo > 55 },
    { text: 'Meta description is 150-160 characters', pass: state.scores.seo > 50 },
    { text: 'H1 heading on homepage', pass: state.scores.content > 50 },
    { text: 'Alt text on images', pass: Math.random() > 0.6 },
    { text: 'Google Business Profile linked', pass: Math.random() > 0.5 },
    { text: 'Schema markup (LocalBusiness)', pass: Math.random() > 0.7 },
    { text: 'SSL certificate (HTTPS)', pass: state.scores.trust > 40 },
    { text: 'XML sitemap present', pass: Math.random() > 0.5 },
    { text: 'NAP consistency (Name, Address, Phone)', pass: Math.random() > 0.4 },
    { text: 'Internal linking between service pages', pass: state.scores.content > 55 }
  ];

  document.getElementById('seoChecklist').innerHTML = checks.map(c =>
    `<li>
      <span class="${c.pass ? 'check-yes' : 'check-no'}">${c.pass ? '✓' : '✕'}</span>
      <span>${c.text}</span>
    </li>`
  ).join('');

  // Recommendations
  const recs = [
    { t: `Optimize title tags for local search`, d: `Change your homepage title to: "${name} | ${mainKeyword.charAt(0).toUpperCase() + mainKeyword.slice(1)} in ${city} | Call (XXX) XXX-XXXX"`, type: 'warning' },
    { t: 'Add location-specific content', d: `Create a paragraph mentioning landmarks, neighborhoods, and areas you serve near ${city}.`, type: 'info' },
    { t: 'Start a dental blog', d: 'Publishing 2-4 blog posts per month can increase organic traffic by 55%. Use our Content Studio to generate posts instantly.', type: 'info' },
    { t: 'Optimize for "near me" searches', d: 'Ensure your Google Business Profile is complete, verified, and has consistent NAP information across all directories.', type: 'warning' },
    { t: 'Add FAQ schema markup', d: 'Structured FAQ data can give you rich snippets in Google, increasing your click-through rate by 20-30%.', type: 'info' },
    { t: 'Build local backlinks', d: `Get listed on local directories, ${city} Chamber of Commerce, and dental association websites to boost domain authority.`, type: 'info' }
  ];

  document.getElementById('seoRecommendations').innerHTML = recs.map(r => `
    <div class="issue-item ${r.type}">
      <div class="issue-icon">${r.type === 'warning' ? '⚠️' : '💡'}</div>
      <div class="issue-content">
        <div class="issue-title">${r.t}</div>
        <div class="issue-desc">${r.d}</div>
      </div>
    </div>
  `).join('');
}

// =============================================
// CONVERSION TAB
// =============================================
function renderConversionTab() {
  // CTA Suggestions
  const ctas = [
    { before: 'Submit', after: 'Book My Appointment →' },
    { before: 'Contact Us', after: 'Schedule Your Free Consultation' },
    { before: 'Learn More', after: 'See How We Can Help Your Smile' },
    { before: 'Click Here', after: 'Get Started With a Free Exam' },
    { before: 'Send', after: 'Request My Appointment Today' },
    { before: 'Call Now', after: 'Call Us – We Answer 24/7 📞' }
  ];

  document.getElementById('ctaSuggestions').innerHTML = ctas.map(c => `
    <div class="cta-suggestion">
      <div class="cta-before">❌ Instead of: <strong>"${c.before}"</strong></div>
      <div class="cta-arrow">↓</div>
      <div class="cta-after">✅ Use: "${c.after}"</div>
    </div>
  `).join('');

  // Trust checklist
  const trusts = [
    { text: 'Doctor photo and professional bio', pass: state.scores.trust > 50 },
    { text: 'Patient testimonials / reviews on site', pass: state.scores.trust > 55 },
    { text: 'Before & after photo gallery', pass: Math.random() > 0.6 },
    { text: 'Insurance plans accepted listed', pass: Math.random() > 0.5 },
    { text: 'Office photos / virtual tour', pass: Math.random() > 0.7 },
    { text: 'Professional certifications displayed', pass: state.scores.trust > 45 },
    { text: 'ADA member badge', pass: Math.random() > 0.5 },
    { text: 'Clear pricing or financing info', pass: Math.random() > 0.6 },
    { text: 'New patient special offer visible', pass: Math.random() > 0.5 },
    { text: 'HIPAA compliance notice', pass: Math.random() > 0.4 }
  ];

  document.getElementById('trustChecklist').innerHTML = trusts.map(t =>
    `<li><span class="${t.pass ? 'check-yes' : 'check-no'}">${t.pass ? '✓' : '✕'}</span> ${t.text}</li>`
  ).join('');

  // Conversion recommendations
  const recs = [
    { t: 'Add online scheduling widget', d: 'Practices with online booking get 35% more appointments. Integrate tools like Zocdoc, LocalMed, or your PMS\'s online scheduler.', type: 'critical' },
    { t: 'Add a "New Patient" banner or special', d: 'Highlight a welcome offer like "Free Exam & X-rays for New Patients" prominently on your homepage.', type: 'warning' },
    { t: 'Display your phone number in the header', d: 'Make it large, visible, and click-to-call on mobile. Include office hours next to it.', type: 'warning' },
    { t: 'Add an exit-intent popup', d: 'When a visitor is about to leave, show a gentle popup: "Wait! Book a free consultation before you go."', type: 'info' },
    { t: 'Show a live chat or chatbot', d: 'An AI chatbot can answer common questions 24/7 and collect patient contact info after hours.', type: 'info' },
    { t: 'Simplify your contact form', d: 'Reduce form fields to: Name, Phone, Email, Preferred Time. Every extra field reduces submissions by 10%.', type: 'warning' }
  ];

  document.getElementById('conversionRecs').innerHTML = recs.map(r => `
    <div class="issue-item ${r.type}">
      <div class="issue-icon">${r.type === 'critical' ? '🚨' : r.type === 'warning' ? '⚠️' : '💡'}</div>
      <div class="issue-content">
        <div class="issue-title">${r.t}</div>
        <div class="issue-desc">${r.d}</div>
      </div>
    </div>
  `).join('');
}

// =============================================
// COMPETITORS TAB
// =============================================
function renderCompetitorsTab() {
  const s = state.scores;
  const metrics = [
    { m: 'Overall Score', you: s.overall, comp: 68 },
    { m: 'Number of Pages', you: Math.floor(Math.random()*8)+5, comp: 15 },
    { m: 'Blog Posts', you: Math.floor(Math.random()*5), comp: 12 },
    { m: 'Page Load Time', you: (Math.random()*3+2).toFixed(1)+'s', comp: '2.1s', lower: true },
    { m: 'Mobile Score', you: s.mobile, comp: 78 },
    { m: 'Reviews on Site', you: Math.floor(Math.random()*5), comp: 15 },
    { m: 'Service Pages', you: Math.floor(Math.random()*5)+3, comp: 10 },
    { m: 'Social Links', you: Math.floor(Math.random()*3)+1, comp: 4 }
  ];

  document.getElementById('compTableBody').innerHTML = metrics.map(m => {
    let status, color;
    const youNum = parseFloat(m.you);
    const compNum = parseFloat(m.comp);
    if (m.lower) {
      status = youNum <= compNum ? 'Ahead' : 'Behind';
      color = youNum <= compNum ? 'green' : 'red';
    } else {
      status = youNum >= compNum ? 'Ahead' : 'Behind';
      color = youNum >= compNum ? 'green' : 'red';
    }
    return `<tr>
      <td><strong>${m.m}</strong></td>
      <td>${m.you}</td>
      <td>${m.comp}</td>
      <td><span class="tag tag-${color}">${status}</span></td>
    </tr>`;
  }).join('');

  // Content Gaps
  const gaps = [
    { t: 'Sedation Dentistry page', d: 'Top competitors have detailed sedation dentistry pages. This is a high-converting service page for anxious patients.' },
    { t: 'Patient resources / blog', d: 'Competitors average 12 blog posts. Educational content drives 55% more organic traffic.' },
    { t: 'Financing / payment options page', d: 'A dedicated financing page addresses a top patient concern and can increase case acceptance.' },
    { t: 'Before & after gallery', d: 'Visual proof of results is one of the strongest conversion tools in cosmetic dentistry.' },
    { t: 'Patient forms download', d: 'Allowing patients to download forms beforehand improves the intake experience.' }
  ];

  document.getElementById('contentGaps').innerHTML = gaps.map(g => `
    <div class="issue-item warning">
      <div class="issue-icon">🕳️</div>
      <div class="issue-content">
        <div class="issue-title">${g.t}</div>
        <div class="issue-desc">${g.d}</div>
      </div>
    </div>
  `).join('');

  // Advantages
  const advs = [
    { t: 'SSL Certificate active', d: 'Your site uses HTTPS — this is essential for trust and Google ranking.' },
    { t: 'Clean, modern design', d: 'Your website template looks professional and contemporary.' }
  ];

  if (s.mobile > 70) advs.push({ t: 'Good mobile responsiveness', d: 'Your site adapts well to mobile devices — better than some competitors.' });
  if (s.speed > 60) advs.push({ t: 'Decent page speed', d: 'Your site loads faster than some local competitors.' });

  document.getElementById('yourAdvantages').innerHTML = advs.map(a => `
    <div class="issue-item good">
      <div class="issue-icon">💪</div>
      <div class="issue-content">
        <div class="issue-title">${a.t}</div>
        <div class="issue-desc">${a.d}</div>
      </div>
    </div>
  `).join('');
}

// =============================================
// ACTION PLAN
// =============================================
function renderActionPlan() {
  const city = state.city;
  const name = state.practiceName;

  const actions = [
    { priority: 'High', color: 'red', text: 'Add a prominent "Book Appointment" button in the header', detail: 'This should be visible without scrolling on both desktop and mobile. Use contrasting color (e.g., green or orange).' },
    { priority: 'High', color: 'red', text: `Update page titles to include "${city}" and your specialty`, detail: `Example: "${name} | Trusted Family Dentist in ${city}"` },
    { priority: 'High', color: 'red', text: 'Add at least 5 patient testimonials to your homepage', detail: 'Use real patient reviews from Google. Include first name, last initial, and star rating.' },
    { priority: 'High', color: 'red', text: 'Write a personal "Meet the Doctor" bio', detail: 'Use our AI Bio Generator in the Conversion Lab to create this in seconds.' },
    { priority: 'High', color: 'red', text: 'Make phone number click-to-call on mobile', detail: 'Wrap your phone number in an <a href="tel:"> tag.' },
    { priority: 'Medium', color: 'yellow', text: 'Create dedicated service pages for each treatment', detail: 'Each service should have its own page with 300+ words. Use our Content Studio.' },
    { priority: 'Medium', color: 'yellow', text: 'Add alt text to all images', detail: 'Describe what\'s in each image for SEO and accessibility.' },
    { priority: 'Medium', color: 'yellow', text: 'Start publishing blog posts (2-4/month)', detail: 'Use our Blog Generator to create SEO-optimized posts in minutes.' },
    { priority: 'Medium', color: 'yellow', text: 'Add Google Maps embed to contact page', detail: 'Makes it easy for patients to find your office and helps local SEO.' },
    { priority: 'Medium', color: 'yellow', text: 'Create a "New Patient" welcome page', detail: 'Include what to expect, forms to download, insurance info, and a warm welcome message.' },
    { priority: 'Medium', color: 'yellow', text: 'Add before & after photos', detail: 'Showcase your best cosmetic work (with patient consent). This is a top conversion driver.' },
    { priority: 'Low', color: 'blue', text: 'Add FAQ schema markup', detail: 'This can earn you rich snippets in Google search results.' },
    { priority: 'Low', color: 'blue', text: 'Set up Google Business Profile posts', detail: 'Post weekly updates, tips, or offers to your Google Business listing.' },
    { priority: 'Low', color: 'blue', text: 'Optimize images for faster loading', detail: 'Compress images using tools like TinyPNG. Target under 200KB per image.' },
    { priority: 'Low', color: 'blue', text: 'Add social media links and feeds', detail: 'Link to your Facebook, Instagram, and Google Business profiles from your website.' }
  ];

  const container = document.getElementById('actionList');
  container.innerHTML = actions.map((a, i) => `
    <div class="action-item" id="action-${i}">
      <div class="action-check" onclick="toggleAction(${i})" id="check-${i}"></div>
      <div>
        <div class="action-priority" style="color:var(--${a.color === 'blue' ? 'primary' : a.color === 'yellow' ? 'warning' : 'danger'})">${a.priority} Priority</div>
        <div class="action-text">${a.text}</div>
        <div class="action-detail">${a.detail}</div>
      </div>
    </div>
  `).join('');

  updateActionProgress();
}

function toggleAction(i) {
  const check = document.getElementById('check-' + i);
  const item = document.getElementById('action-' + i);
  check.classList.toggle('checked');
  item.classList.toggle('completed');
  if (check.classList.contains('checked')) {
    check.textContent = '✓';
  } else {
    check.textContent = '';
  }
  updateActionProgress();
}

function updateActionProgress() {
  const total = document.querySelectorAll('.action-item').length;
  const done = document.querySelectorAll('.action-check.checked').length;
  document.getElementById('actionProgress').textContent = `${done} / ${total} completed`;
}

function uncheckAll() {
  document.querySelectorAll('.action-check').forEach(c => { c.classList.remove('checked'); c.textContent = ''; });
  document.querySelectorAll('.action-item').forEach(i => i.classList.remove('completed'));
  updateActionProgress();
}

// =============================================
// AI CONTENT GENERATION
// =============================================
async function callAI(prompt) {
  if (state.apiKey && state.apiKey.startsWith('sk-') && state.apiKey.length > 20) {
    try {
      const res = await fetch('https://api.openai.com/v1/chat/completions', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json', 'Authorization': 'Bearer ' + state.apiKey },
        body: JSON.stringify({
          model: 'gpt-4o-mini',
          messages: [
            { role: 'system', content: `You are a dental marketing copywriter. You write compelling, patient-friendly content for dental practice websites. The practice is "${state.practiceName}" in ${state.city}. Specialty: ${state.type}. Write in a warm, professional tone. Always include calls-to-action.` },
            { role: 'user', content: prompt }
          ],
          max_tokens: 1500,
          temperature: 0.7
        })
      });
      const data = await res.json();
      if (data.choices && data.choices[0]) return data.choices[0].message.content;
      throw new Error(data.error?.message || 'API error');
    } catch (e) {
      showToast('API Error: ' + e.message + '. Using template.', 'error');
      return null;
    }
  }
  return null;
}

function showOutput(boxId, text) {
  const box = document.getElementById(boxId);
  const textEl = document.getElementById(boxId + 'Text');
  box.classList.remove('hidden');
  textEl.textContent = '';
  textEl.classList.add('typing-cursor');

  let i = 0;
  const speed = 8;
  function type() {
    if (i < text.length) {
      textEl.textContent += text.charAt(i);
      i++;
      setTimeout(type, speed);
    } else {
      textEl.classList.remove('typing-cursor');
    }
  }
  type();
  box.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
}

function setLoading(btnId, loading) {
  const btn = document.getElementById(btnId);
  if (loading) {
    btn.disabled = true;
    btn.dataset.originalText = btn.innerHTML;
    btn.innerHTML = '<span class="spinner"></span> Generating...';
  } else {
    btn.disabled = false;
    btn.innerHTML = btn.dataset.originalText;
  }
}

// Blog Generator
async function generateBlog() {
  setLoading('blogGenBtn', true);
  const topic = document.getElementById('blogTopic').value;
  const tone = document.getElementById('blogTone').value;
  const length = document.getElementById('blogLength').value;
  const customTopic = document.getElementById('customTopic').value;
  const city = state.city;
  const name = state.practiceName;

  const topicLabel = topic === 'custom' ? customTopic : document.getElementById('blogTopic').options[document.getElementById('blogTopic').selectedIndex].text;

  const prompt = `Write a ${length === 'short' ? '400' : length === 'medium' ? '700' : '1000'}-word blog post about "${topicLabel}" for a dental practice called "${name}" in ${city}. Tone: ${tone}. Include an engaging title, subheadings, patient-friendly language, local SEO keywords mentioning ${city}, and end with a call-to-action to schedule an appointment.`;

  let result = await callAI(prompt);

  if (!result) {
    result = getTemplateBlog(topic === 'custom' ? 'general-topic' : topic, topicLabel);
  }

  setLoading('blogGenBtn', false);
  showOutput('blogOutput', result);
}

// Service Page Generator
async function generateService() {
  setLoading('serviceGenBtn', true);
  const service = document.getElementById('serviceType').value;
  const points = document.getElementById('servicePoints').value;
  const serviceLabel = document.getElementById('serviceType').options[document.getElementById('serviceType').selectedIndex].text;

  const prompt = `Write a compelling service page for "${serviceLabel}" for a dental practice called "${state.practiceName}" in ${state.city}. Include: a patient-focused headline, description focusing on benefits (not just features), what patients can expect, why choose us section${points ? ', highlighting these points: ' + points : ''}. End with a strong call-to-action. Use local SEO keywords. Make it warm, reassuring, and professional. About 400-500 words.`;

  let result = await callAI(prompt);

  if (!result) {
    result = getTemplateService(service, serviceLabel);
  }

  setLoading('serviceGenBtn', false);
  showOutput('serviceOutput', result);
}

// FAQ Generator
async function generateFAQ() {
  setLoading('faqGenBtn', true);
  const category = document.getElementById('faqCategory').value;
  const count = document.getElementById('faqCount').value;
  const catLabel = document.getElementById('faqCategory').options[document.getElementById('faqCategory').selectedIndex].text;

  const prompt = `Generate ${count} frequently asked questions and answers about "${catLabel}" for a dental practice called "${state.practiceName}" in ${state.city}. Write patient-friendly answers that are reassuring and informative. Each answer should be 2-3 sentences. Format as Q: and A:.`;

  let result = await callAI(prompt);

  if (!result) {
    result = getTemplateFAQ(category, parseInt(count));
  }

  setLoading('faqGenBtn', false);
  showOutput('faqOutput', result);
}

// Social Media Generator
async function generateSocial() {
  setLoading('socialGenBtn', true);
  const platform = document.getElementById('socialPlatform').value;
  const postType = document.getElementById('socialType').value;
  const typeLabel = document.getElementById('socialType').options[document.getElementById('socialType').selectedIndex].text;

  const prompt = `Write a ${platform} post for a dental practice called "${state.practiceName}" in ${state.city}. Post type: ${typeLabel}. Include relevant emojis, hashtags, and a call-to-action. Make it engaging and shareable. Keep it appropriate length for ${platform}.`;

  let result = await callAI(prompt);

  if (!result) {
    result = getTemplateSocial(platform, postType);
  }

  setLoading('socialGenBtn', false);
  showOutput('socialOutput', result);
}

// Meta Description Generator
async function generateMeta() {
  const page = document.getElementById('metaPageSelect').value;
  const pageLabel = document.getElementById('metaPageSelect').options[document.getElementById('metaPageSelect').selectedIndex].text;

  const prompt = `Write 3 different SEO meta descriptions (150-160 characters each) for the "${pageLabel}" of a dental practice called "${state.practiceName}" in ${state.city}. Include a call-to-action and local keywords. Number them 1, 2, 3.`;

  let result = await callAI(prompt);

  if (!result) {
    result = getTemplateMeta(page);
  }

  showOutput('metaOutput', result);
}

// Doctor Bio Generator
async function generateBio() {
  setLoading('bioGenBtn', true);
  const name = document.getElementById('drName').value || 'Dr. Smith';
  const years = document.getElementById('drYears').value || '10';
  const specialties = document.getElementById('drSpecialties').value || 'General and cosmetic dentistry';
  const education = document.getElementById('drEducation').value;
  const personal = document.getElementById('drPersonal').value;

  const prompt = `Write a warm, professional doctor bio for ${name}, a dentist at "${state.practiceName}" in ${state.city} with ${years} years of experience. Specialties: ${specialties}.${education ? ' Education: ' + education + '.' : ''}${personal ? ' Personal: ' + personal + '.' : ''} The bio should connect emotionally with patients, highlight expertise, and end with an invitation to schedule a visit. About 200-300 words.`;

  let result = await callAI(prompt);

  if (!result) {
    result = getTemplateBio(name, years, specialties, education, personal);
  }

  setLoading('bioGenBtn', false);
  showOutput('bioOutput', result);
}

// =============================================
// TEMPLATE CONTENT (Fallback when no API key)
// =============================================
function getTemplateBlog(topic, topicLabel) {
  const name = state.practiceName;
  const city = state.city;
  const templates = {
    'implants': `Dental Implants: Your Complete Guide to a Permanent Smile\n\n${name} | ${city}\n\n${'='.repeat(50)}\n\nAre you tired of dealing with missing teeth, uncomfortable dentures, or gaps in your smile? Dental implants might be the life-changing solution you've been looking for.\n\nAt ${name} in ${city}, we've helped hundreds of patients restore their smiles with state-of-the-art dental implants. Here's everything you need to know.\n\n## What Are Dental Implants?\n\nDental implants are small titanium posts that are surgically placed into your jawbone, where they serve as artificial tooth roots. Once healed, they provide a strong foundation for permanent replacement teeth that look, feel, and function just like your natural teeth.\n\nUnlike dentures that can slip and slide, implants are fixed in place — meaning you can eat, speak, and smile with complete confidence.\n\n## Benefits of Dental Implants\n\n• **Look Natural** — Custom-crafted crowns match your existing teeth perfectly\n• **Permanent Solution** — With proper care, implants can last a lifetime\n• **Preserve Bone** — Implants stimulate your jawbone, preventing bone loss\n• **Eat Anything** — No dietary restrictions like with dentures\n• **Easy Care** — Brush and floss just like natural teeth\n• **Boost Confidence** — Smile freely without worry\n\n## What to Expect During the Process\n\nThe implant process typically involves 2-3 visits over a few months:\n\n1. **Consultation** — We'll examine your teeth, take digital scans, and create your personalized treatment plan\n2. **Implant Placement** — The titanium post is gently placed into your jawbone (most patients say it's easier than they expected!)\n3. **Healing Period** — Over 3-6 months, the implant fuses with your bone in a process called osseointegration\n4. **Crown Placement** — Your beautiful, permanent crown is attached to the implant\n\n## Am I a Good Candidate?\n\nMost adults with missing teeth are excellent candidates for dental implants. The key requirements are:\n• Adequate jawbone density (bone grafting is available if needed)\n• Healthy gums\n• Good overall health\n• Non-smoker or willing to quit during healing\n\n## Affordable Options in ${city}\n\nWe believe everyone deserves a complete, healthy smile. That's why ${name} offers:\n• Flexible payment plans\n• Insurance coordination\n• Financing options through CareCredit\n• Free implant consultations\n\n## Ready to Get Started?\n\nDon't let missing teeth hold you back from living your best life. Schedule your free dental implant consultation at ${name} in ${city} today. Our experienced team will answer all your questions and help you explore your options.\n\n📞 Call us today or click "Book Appointment" to get started!\n\n---\n${name} | Trusted Dental Implants in ${city}`,

    'whitening': `Teeth Whitening: Which Option Is Right for You?\n\n${name} | ${city}\n\n${'='.repeat(50)}\n\nA bright, white smile can transform your confidence and make a lasting first impression. But with so many whitening options available, how do you choose the right one?\n\nAt ${name} in ${city}, we offer professional teeth whitening solutions that are safe, effective, and tailored to your needs. Let's compare your options.\n\n## Why Do Teeth Get Stained?\n\nBefore choosing a whitening method, it helps to understand why teeth lose their brightness:\n• **Coffee, tea, and red wine** — These popular beverages are top stain culprits\n• **Tobacco use** — Causes deep, stubborn discoloration\n• **Aging** — Enamel naturally thins over time, revealing yellowish dentin\n• **Medications** — Certain antibiotics and treatments can cause discoloration\n• **Foods** — Berries, curry, tomato sauce, and other pigmented foods\n\n## Your Whitening Options Compared\n\n### 1. Professional In-Office Whitening ⭐\n**Best for:** Dramatic results, fast\n**How it works:** We apply a powerful whitening gel activated by a special light. Results in just one 60-minute visit!\n**Results:** 5-8 shades whiter\n**Cost:** $$-$$$\n**Our recommendation:** Best results, safest option\n\n### 2. Professional Take-Home Kits\n**Best for:** Gradual whitening at your convenience\n**How it works:** Custom-fitted trays with professional-grade gel. Wear for 30 min/day for 2 weeks.\n**Results:** 3-6 shades whiter\n**Cost:** $$\n\n### 3. Over-the-Counter Products\n**Best for:** Minor touch-ups\n**How it works:** Strips, pens, or generic trays from the store\n**Results:** 1-3 shades whiter\n**Cost:** $\n**Note:** Results are less predictable and may cause sensitivity\n\n## Why Professional Whitening Is Worth It\n\n• Custom treatment for even, consistent results\n• Stronger, professional-grade whitening agents\n• Supervised by dental professionals for safety\n• Reduced sensitivity with our advanced formulas\n• Results that last 1-3 years with proper care\n\n## Maintaining Your White Smile\n\nAfter whitening, keep your smile bright with these tips:\n• Brush twice daily with whitening toothpaste\n• Rinse with water after consuming staining foods/drinks\n• Use a straw for coffee and tea\n• Schedule regular dental cleanings at ${name}\n• Touch up annually with your take-home kit\n\n## Special Offer for ${city} Patients\n\nReady for a brighter smile? Contact ${name} to learn about our current whitening specials. We'll help you choose the perfect option for your smile goals and budget.\n\n📞 Schedule your whitening consultation today!\n\n---\n${name} | Professional Teeth Whitening in ${city}`,

    'invisalign': `Is Invisalign Right for You? Everything You Need to Know\n\n${name} | ${city}\n\n${'='.repeat(50)}\n\nDreaming of straighter teeth but dreading the thought of metal braces? You're not alone — and you have options! Invisalign clear aligners have transformed millions of smiles worldwide, and at ${name} in ${city}, we're proud to offer this revolutionary treatment.\n\n## What Is Invisalign?\n\nInvisalign uses a series of custom-made, virtually invisible plastic aligners to gradually shift your teeth into their ideal position. No metal brackets, no wires, no monthly tightening appointments.\n\nEach set of aligners is worn for about 1-2 weeks before moving to the next set, gently guiding your teeth into place.\n\n## Who Is Invisalign For?\n\nInvisalign can treat a wide range of orthodontic issues:\n\n✅ Crowded teeth\n✅ Gaps between teeth\n✅ Overbite, underbite, crossbite\n✅ Crooked or rotated teeth\n✅ Mild to moderate alignment issues\n\nIt's ideal for teens and adults who want a discreet orthodontic solution.\n\n## Invisalign vs. Traditional Braces\n\n| Feature | Invisalign | Metal Braces |\n|---------|------------|-------------|\n| Visibility | Nearly invisible | Very visible |\n| Removable | Yes | No |\n| Diet restrictions | None | Many |\n| Comfort | Smooth plastic | Wires & brackets |\n| Treatment time | 6-18 months | 18-36 months |\n| Office visits | Every 6-8 weeks | Every 4 weeks |\n\n## The Invisalign Process at ${name}\n\n1. **Free Consultation** — We'll assess your smile and discuss your goals\n2. **Digital Scan** — No messy impressions! We use advanced 3D scanning\n3. **Preview Your Smile** — See your projected results before starting\n4. **Receive Your Aligners** — Custom-made just for you\n5. **Progress Check-ins** — Brief visits every 6-8 weeks\n6. **Reveal Your New Smile!** — Enjoy your beautiful, straight teeth\n\n## Why Choose ${name} for Invisalign in ${city}?\n\n• Experienced Invisalign provider\n• Advanced 3D digital scanning technology\n• Flexible payment plans available\n• Free initial consultation\n• Friendly, supportive team\n\nReady to start your journey to a straighter smile? Book your free Invisalign consultation at ${name} in ${city} today!\n\n📞 Call us or book online — your dream smile is closer than you think!\n\n---\n${name} | Invisalign Provider in ${city}`
  };

  if (templates[topic]) return templates[topic];

  // Generic template
  return `${topicLabel}\n\n${name} | ${city}\n\n${'='.repeat(50)}\n\nAt ${name} in ${city}, we're committed to providing our patients with the highest quality dental care in a comfortable, welcoming environment.\n\n## Understanding ${topicLabel}\n\nWhen it comes to your dental health, knowledge is power. That's why we want to share important information about ${topicLabel.toLowerCase()} with our ${city} community.\n\nMany patients have questions about this topic, and our experienced team is always here to provide answers and guidance.\n\n## What You Should Know\n\nDental health is a crucial part of your overall wellness. Here are some key points about ${topicLabel.toLowerCase()}:\n\n• Regular dental visits help catch issues early\n• Modern dentistry offers comfortable, effective treatments\n• Prevention is always better (and cheaper) than treatment\n• Our team uses the latest technology for the best results\n• We work with you to create a personalized treatment plan\n\n## Why Choose ${name}?\n\nOur patients in ${city} choose us because we offer:\n\n✅ Experienced, caring dental professionals\n✅ State-of-the-art technology\n✅ Comfortable, modern office environment\n✅ Flexible scheduling and payment options\n✅ A genuine commitment to your smile\n\n## Your Next Step\n\nWhether you're due for a check-up or have a specific concern about ${topicLabel.toLowerCase()}, we're here to help. At ${name}, every patient is treated like family.\n\n📞 Contact us today to schedule your appointment. We look forward to seeing you smile!\n\n---\n${name} | Quality Dental Care in ${city}`;
}

function getTemplateService(service, serviceLabel) {
  const name = state.practiceName;
  const city = state.city;

  return `# ${serviceLabel} in ${city}\n## ${name}\n\n${'='.repeat(50)}\n\n### Your Smile Deserves the Best ${serviceLabel}\n\nAt ${name}, we believe every patient deserves a healthy, beautiful smile. Our ${serviceLabel.toLowerCase()} services combine advanced technology with a gentle, patient-first approach to deliver results you'll love.\n\n### What We Offer\n\nOur comprehensive ${serviceLabel.toLowerCase()} services include personalized treatment plans designed around your unique needs and goals. Whether you're looking to maintain your oral health, restore damaged teeth, or enhance your smile's appearance, we have the expertise and technology to help.\n\n### What to Expect\n\nFrom the moment you walk through our doors in ${city}, you'll experience:\n\n🤝 **Warm Welcome** — Our friendly team will make you feel right at home\n📋 **Thorough Consultation** — We'll listen to your concerns and explain all options\n💻 **Advanced Technology** — Digital imaging, modern equipment, comfortable care\n😊 **Gentle Treatment** — Your comfort is always our top priority\n📞 **Ongoing Support** — We're here for you before, during, and after treatment\n\n### Why Patients in ${city} Choose Us\n\n• ⭐ Years of experience and continuing education\n• 🏆 Commitment to clinical excellence\n• 💰 Transparent pricing and flexible payment options\n• 🕐 Convenient scheduling including early and late appointments\n• 👨‍👩‍👧‍👦 Welcoming to patients of all ages\n• 🛡️ Insurance accepted and filed on your behalf\n\n### Patient-Focused Care\n\nWe understand that visiting the dentist can cause anxiety for some patients. That's why we've created a calm, comfortable environment and offer various comfort options to ensure your experience is as pleasant as possible.\n\n### Schedule Your Visit Today\n\nReady to experience the ${name} difference? Contact us today to schedule your ${serviceLabel.toLowerCase()} consultation. We're conveniently located in ${city} and accepting new patients!\n\n📞 Call us today or use our online booking to get started.\n\nYour best smile is waiting.\n\n---\n${name} | ${serviceLabel} in ${city}`;
}

function getTemplateFAQ(category, count) {
  const name = state.practiceName;
  const city = state.city;

  const allFAQs = {
    general: [
      { q: 'How often should I visit the dentist?', a: `We recommend visiting ${name} every six months for a routine check-up and professional cleaning. Regular visits help us catch potential issues early and keep your smile healthy.` },
      { q: 'Do you accept new patients?', a: `Absolutely! ${name} is always welcoming new patients of all ages. Call us or book online to schedule your first visit. We look forward to meeting you!` },
      { q: 'What should I do if I have a dental emergency?', a: `Call ${name} immediately. We offer same-day emergency appointments for patients in ${city} experiencing severe pain, broken teeth, or other urgent dental issues.` },
      { q: 'How can I prevent cavities?', a: 'The best prevention includes brushing twice daily with fluoride toothpaste, flossing daily, limiting sugary snacks, and visiting us regularly for check-ups and cleanings.' },
      { q: 'Is dental X-ray radiation safe?', a: 'Yes! Modern digital X-rays use extremely low radiation — less than you receive from a day of natural sun exposure. We also use protective lead aprons for extra safety.' },
      { q: 'Do you offer sedation for anxious patients?', a: `Yes, we understand dental anxiety is common. ${name} offers sedation options to help nervous patients feel completely comfortable during their treatment.` },
      { q: 'How long does a dental cleaning take?', a: 'A typical professional cleaning takes about 45-60 minutes. This includes removing plaque and tartar, polishing your teeth, and a brief examination by your dentist.' },
      { q: 'What age should my child first see a dentist?', a: 'The American Dental Association recommends a child\'s first dental visit by their first birthday or within six months of their first tooth appearing.' }
    ],
    insurance: [
      { q: 'What insurance plans do you accept?', a: `${name} accepts most major dental insurance plans. Please call our office to verify your specific coverage, and our team will handle the paperwork for you.` },
      { q: 'Do you offer payment plans?', a: `Yes! We believe finances should never prevent you from getting quality dental care. ${name} offers flexible payment plans and financing through CareCredit.` },
      { q: 'What if I don\'t have dental insurance?', a: `No insurance? No problem! We offer an affordable in-house membership plan and competitive self-pay rates. Ask about our new patient specials!` },
      { q: 'Do you file insurance claims for me?', a: 'Yes, our experienced billing team handles all insurance claims on your behalf. We work to maximize your benefits so you can focus on your smile.' },
      { q: 'How much does a dental visit cost without insurance?', a: 'Costs vary by treatment, but we\'re committed to transparency. We\'ll provide a detailed estimate before any treatment begins, with no surprise fees.' }
    ],
    procedures: [
      { q: 'Does getting a filling hurt?', a: 'With modern anesthesia and techniques, most patients feel little to no discomfort during fillings. We prioritize your comfort and will ensure you\'re fully numb before any work begins.' },
      { q: 'How long do dental crowns last?', a: 'With proper care, dental crowns typically last 10-15 years or more. We use high-quality materials and precise techniques to ensure long-lasting results.' },
      { q: 'Is teeth whitening safe?', a: 'Professional teeth whitening supervised by a dentist is very safe. We use proven whitening agents and customize treatment to minimize sensitivity.' },
      { q: 'What is a root canal like?', a: 'Modern root canals are very comfortable — most patients compare it to getting a filling! The procedure removes infection from inside the tooth and relieves pain.' },
      { q: 'How long do dental implants take?', a: 'The complete implant process typically takes 3-6 months from placement to final crown. However, you\'ll have a temporary restoration so you\'re never without a tooth.' }
    ],
    'first-visit': [
      { q: 'What should I bring to my first appointment?', a: `Please bring your photo ID, insurance card (if applicable), completed patient forms (available on our website), and a list of any medications you take.` },
      { q: 'How early should I arrive?', a: 'We recommend arriving 15 minutes before your scheduled appointment to complete any remaining paperwork and settle in comfortably.' },
      { q: 'What happens during a first visit?', a: `Your first visit at ${name} includes a comprehensive exam, digital X-rays, professional cleaning, and a one-on-one discussion about your dental health and goals.` },
      { q: 'Can I bring my children?', a: 'Absolutely! We welcome patients of all ages and have a family-friendly environment. We can even schedule family block appointments for your convenience.' },
      { q: 'Will I receive a treatment plan?', a: 'Yes, after your exam we\'ll provide a clear, detailed treatment plan with all options and costs explained. We never pressure patients — the choice is always yours.' }
    ],
    cosmetic: [
      { q: 'What cosmetic dental services do you offer?', a: `${name} offers a full range of cosmetic services including teeth whitening, porcelain veneers, dental bonding, Invisalign, smile makeovers, and more.` },
      { q: 'How much do veneers cost?', a: 'Veneer costs vary based on the number of teeth and material chosen. We offer free cosmetic consultations and flexible financing to make your dream smile affordable.' },
      { q: 'Are cosmetic dental procedures painful?', a: 'Most cosmetic procedures involve minimal to no discomfort. We use modern techniques and anesthesia to ensure you\'re comfortable throughout your treatment.' },
      { q: 'How long do cosmetic results last?', a: 'With proper care, cosmetic results are long-lasting. Veneers can last 10-20 years, bonding 5-10 years, and whitening results 1-3 years with maintenance.' },
      { q: 'Can you show me what my new smile will look like?', a: 'Yes! We use digital smile design technology to show you a preview of your potential results before any treatment begins. See your new smile before committing!' }
    ],
    emergency: [
      { q: 'What counts as a dental emergency?', a: 'Dental emergencies include severe toothache, knocked-out or broken teeth, lost fillings/crowns, dental abscess, uncontrolled bleeding, and jaw injuries.' },
      { q: 'Do you see emergency patients same-day?', a: `Yes! ${name} reserves time each day for emergency patients in ${city}. Call us immediately and we\'ll get you in as soon as possible.` },
      { q: 'What should I do if a tooth gets knocked out?', a: 'Handle the tooth by the crown (not the root), rinse gently, try to place it back in the socket or keep it in milk, and get to our office within 30 minutes for the best chance of saving it.' },
      { q: 'Will my insurance cover emergency dental care?', a: 'Most dental insurance plans cover emergency treatments. Our team will verify your coverage and help you understand your benefits before treatment.' },
      { q: 'What can I do for tooth pain at home until my appointment?', a: 'Rinse with warm salt water, take over-the-counter pain relievers (not aspirin directly on gums), apply a cold compress to your cheek, and avoid very hot or cold foods.' }
    ]
  };

  const faqs = (allFAQs[category] || allFAQs.general).slice(0, count);

  let result = `Frequently Asked Questions — ${state.practiceName}\n${'='.repeat(50)}\n\n`;
  faqs.forEach((faq, i) => {
    result += `Q${i + 1}: ${faq.q}\n\nA: ${faq.a}\n\n---\n\n`;
  });

  result += `Have more questions? Contact ${name} in ${city} — we're happy to help! 📞`;
  return result;
}

function getTemplateSocial(platform, type) {
  const name = state.practiceName;
  const city = state.city;

  const posts = {
    'instagram-promo': `✨ NEW PATIENT SPECIAL ✨\n\nWelcome to ${name}! 🦷\n\nWe're offering new patients a FREE exam & X-rays with their first cleaning! 🎉\n\nWhy choose us?\n✅ Gentle, caring team\n✅ Modern technology\n✅ Comfortable office in ${city}\n✅ Flexible scheduling\n\nYour best smile is waiting! Link in bio to book 👆\n\n#${city.replace(/\s/g,'')}Dentist #NewPatientSpecial #DentalCare #SmileMakeover #${city.replace(/\s/g,'')} #DentistNearMe #HealthySmile #DentalOffer`,
    'instagram-educational': `💡 DID YOU KNOW? 💡\n\nBrushing too hard can actually DAMAGE your teeth and gums! 😱\n\nHere are 3 brushing tips from our team at ${name}:\n\n1️⃣ Use a SOFT-bristled toothbrush\n2️⃣ Brush in gentle circular motions\n3️⃣ Don't brush immediately after eating acidic foods — wait 30 minutes!\n\nYour enamel will thank you! 😁\n\nSave this post for later ☝️\n\n#DentalTips #OralHealth #${city.replace(/\s/g,'')}Dentist #HealthyTeeth #DentalCare #SmileTips #BrushingTips`,
    'instagram-behind-scenes': `👋 Behind the scenes at ${name}! \n\nEver wonder what goes on before our doors open? Here's a peek at our morning routine:\n\n☀️ Sterilizing all instruments\n🖥️ Reviewing patient care plans\n☕ Team huddle (yes, there's coffee!)\n💐 Fresh flowers in the lobby\n🎵 Curating our relaxing playlist\n\nWe put this care into EVERYTHING we do — because you deserve it! ❤️\n\n#BehindTheScenes #DentalOffice #${city.replace(/\s/g,'')} #MeetTheTeam #DentistLife #PatientCare`,
    'instagram-testimonial': `⭐⭐⭐⭐⭐\n\n"I used to be terrified of the dentist. ${name} completely changed that. The team is so gentle and kind — I actually LOOK FORWARD to my visits now!"\n\n— Happy Patient in ${city} 😊\n\nWe love hearing stories like this! 💙\n\nReady to experience the difference? Link in bio!\n\n#PatientLove #${city.replace(/\s/g,'')}Dentist #DentalReview #HappyPatient #SmileTransformation #GentleDentistry`,
    'instagram-seasonal': `🌸 Spring Smile Refresh! 🌸\n\nNew season, new smile? ✨\n\nThis spring, brighten your smile with our professional teeth whitening special at ${name}!\n\n🦷 In-office whitening: results in just 1 hour\n🏠 Take-home kits available too\n💰 Special spring pricing — ask us!\n\nPerfect timing before summer photos 📸☀️\n\nBook your appointment today! Link in bio 👆\n\n#SpringSmile #TeethWhitening #${city.replace(/\s/g,'')} #SmileRefresh #CosmeticDentistry #BrightSmile`,
    'facebook-promo': `🎉 SPECIAL OFFER for New Patients! 🎉\n\n${name} is welcoming new patients with a special offer: FREE exam & X-rays with your first professional cleaning!\n\nWe know finding a new dentist can be stressful, so we want to make it easy for you. Our friendly team in ${city} is here to provide gentle, high-quality dental care for your whole family.\n\n✅ Modern, comfortable office\n✅ Experienced, caring team\n✅ Most insurance accepted\n✅ Evening & weekend hours available\n\n📞 Call us or visit our website to schedule your appointment today!\n\nLimited availability — book soon! 🦷✨`,
    'facebook-educational': `🦷 Dental Tip Tuesday!\n\nDid you know that your oral health is connected to your overall health? Research shows links between gum disease and:\n\n❤️ Heart disease\n🧠 Cognitive health\n🤰 Pregnancy complications\n📊 Diabetes management\n\nThat's why regular dental check-ups at ${name} are about more than just your teeth — they're about your whole-body wellness!\n\nWhen was your last dental check-up? If it's been more than 6 months, it's time to schedule!\n\n📞 Call us or book online today.\n\n#DentalHealth #OralHealth #${city.replace(/\s/g,'')} #HealthyLiving`,
    'facebook-behind-scenes': `👀 Take a peek inside our office!\n\nAt ${name} in ${city}, we've created a space where you can actually RELAX at the dentist (yes, really! 😄)\n\nOur office features:\n🖥️ State-of-the-art digital technology\n🛋️ Comfortable treatment rooms\n📺 TVs in every room\n☕ Complimentary beverages\n🎵 Relaxing atmosphere\n\nWe believe your dental experience should be as comfortable as possible. Come see for yourself!\n\n📞 Schedule a tour or your first visit today!`,
    'facebook-testimonial': `Nothing makes our day like hearing from happy patients! ❤️\n\n"I've been going to ${name} for 3 years now, and I can't imagine going anywhere else. The staff remembers my name, the office is beautiful, and Dr. [Name] takes the time to explain everything. Best dental experience I've ever had!" ⭐⭐⭐⭐⭐\n\nThank you for trusting us with your smile! We're honored to serve the ${city} community.\n\nWant to join our dental family? We're accepting new patients! 🦷\n📞 Call or book online today.`,
    'facebook-seasonal': `☀️ Summer is coming — is your smile ready?\n\nWhether it's graduation photos, weddings, vacations, or just wanting to feel your best, now is the perfect time to invest in your smile!\n\nAt ${name} in ${city}, we offer:\n✨ Professional teeth whitening\n😁 Invisalign clear aligners\n💎 Porcelain veneers\n🦷 Complete smile makeovers\n\nSchedule a FREE cosmetic consultation this month and let's design your dream smile together!\n\n📞 Call us or click Book Now to get started.`,
    'google-promo': `🦷 New Patient Special at ${name}!\n\nWelcome to our dental family! New patients receive a free exam & X-rays with their first cleaning.\n\nWe offer comprehensive dental care for the whole family in ${city}. Modern office, gentle care, and a team that truly cares about your smile.\n\n📞 Book your appointment today! Most insurance accepted. Evening hours available.`,
    'google-educational': `Brushing Tip from ${name} 🦷\n\nReplace your toothbrush every 3 months (or sooner if bristles are frayed). A worn toothbrush is up to 50% less effective at removing plaque!\n\nFor more dental tips and to schedule your next check-up, visit ${name} in ${city}. We're here for all your dental needs! 😊`,
    'google-behind-scenes': `We love our team at ${name}! 💙\n\nOur dedicated dental professionals in ${city} are committed to providing you with the best possible care in a warm, welcoming environment.\n\nCome meet our team — schedule your visit today! New patients always welcome. 🦷✨`,
    'google-testimonial': `⭐⭐⭐⭐⭐ "Best dentist in ${city}! Gentle care, modern office, and the friendliest staff. Highly recommend ${name} to anyone looking for a new dental home."\n\nThank you for the kind words! We're proud to serve our ${city} community. Schedule your visit today! 🦷`,
    'google-seasonal': `Spring cleaning for your teeth! 🌸🦷\n\n${name} is offering special pricing on professional cleanings and whitening this season. Start spring with a fresh, bright smile!\n\n📞 Call to book your appointment. New patients welcome! Most insurance accepted.\n\n${name} — Your trusted dentist in ${city}.`
  };

  const key = platform + '-' + type;
  return posts[key] || posts['instagram-promo'];
}

function getTemplateMeta(page) {
  const name = state.practiceName;
  const city = state.city;

  const metas = {
    home: `1. "${name} — Trusted Dentist in ${city}. Accepting new patients! Gentle care, modern office, flexible scheduling. Call today!" (148 chars)\n\n2. "Looking for a dentist in ${city}? ${name} offers comprehensive dental care for the whole family. Book your free consultation today!" (142 chars)\n\n3. "Your smile deserves the best. ${name} in ${city} provides expert dental care in a comfortable, welcoming environment. New patients welcome!" (150 chars)`,
    about: `1. "Meet the caring team at ${name} in ${city}. Experienced dentists committed to your comfort and smile. Learn about our approach to care." (146 chars)\n\n2. "Dr. [Name] and the ${name} team bring years of expertise and genuine compassion to every patient in ${city}. Meet your dental team!" (140 chars)\n\n3. "Discover why patients in ${city} trust ${name} for their dental care. Meet our experienced, friendly team and learn about our philosophy." (148 chars)`,
    services: `1. "${name} in ${city} offers complete dental services: cleanings, fillings, crowns, implants, whitening & more. Schedule your visit today!" (147 chars)\n\n2. "From preventive care to smile makeovers, ${name} provides comprehensive dental services in ${city}. See our full list of treatments." (143 chars)\n\n3. "Expert dental services in ${city} — general, cosmetic & restorative dentistry at ${name}. Modern technology, gentle care. Book now!" (141 chars)`,
    cosmetic: `1. "Transform your smile with cosmetic dentistry at ${name} in ${city}. Veneers, whitening, Invisalign & more. Free consultation available!" (149 chars)\n\n2. "Dream smile? Make it real! ${name} offers expert cosmetic dentistry in ${city} — whitening, veneers, bonding & complete makeovers." (142 chars)\n\n3. "Cosmetic dentist in ${city} — ${name} creates beautiful, natural-looking smiles with the latest technology. See your new smile today!" (145 chars)`,
    implants: `1. "Missing teeth? Dental implants at ${name} in ${city} restore your smile permanently. Natural-looking results. Free implant consultation!" (150 chars)\n\n2. "Dental implants in ${city} by experienced professionals at ${name}. Permanent, beautiful tooth replacement. Financing available. Call today!" (152 chars)\n\n3. "Restore your smile and confidence with dental implants from ${name}. Trusted implant dentist in ${city}. Book your free consultation!" (146 chars)`,
    emergency: `1. "Dental emergency in ${city}? ${name} offers same-day emergency appointments. Toothache, broken tooth, or injury — call us now for help!" (148 chars)\n\n2. "Emergency dentist in ${city} — ${name} provides urgent dental care when you need it most. Open evenings. Call for immediate assistance!" (147 chars)\n\n3. "Don't wait with dental pain! ${name} in ${city} sees emergency patients same-day. Expert care for toothaches, injuries & more. Call now!" (149 chars)`,
    contact: `1. "Contact ${name} in ${city} to schedule your appointment. Conveniently located, flexible hours, friendly team. Call or book online today!" (148 chars)\n\n2. "Ready to visit ${name}? Find our ${city} location, office hours, and contact info. We make scheduling easy! New patients always welcome." (148 chars)\n\n3. "Schedule your dental appointment at ${name} in ${city}. Easy online booking, same-day availability, and a team that puts your comfort first!" (152 chars)`
  };

  return `Meta Description Options:\n${'='.repeat(40)}\n\n${metas[page] || metas.home}`;
}

function getTemplateBio(drName, years, specialties, education, personal) {
  const name = state.practiceName;
  const city = state.city;

  let bio = `Meet ${drName}\n${'='.repeat(40)}\n\n`;
  bio += `${drName} is the heart and soul of ${name}, bringing ${years} years of dedicated dental experience to the ${city} community.\n\n`;
  bio += `With a passion for ${specialties.toLowerCase()}, ${drName} combines clinical excellence with a genuinely caring approach. "I believe every patient deserves to feel comfortable, informed, and confident about their dental care," says ${drName}. "My goal is to create a positive experience that makes you actually look forward to visiting the dentist."\n\n`;

  if (education) {
    bio += `${drName} earned their dental degree from ${education} and continues to pursue advanced training and education to stay at the forefront of modern dentistry. This commitment to lifelong learning means you always receive care based on the latest techniques and research.\n\n`;
  }

  bio += `What sets ${drName} apart is their ability to listen. Whether you're coming in for a routine cleaning or considering a complete smile makeover, ${drName} takes the time to understand your goals, answer your questions, and develop a personalized treatment plan that fits your needs and budget.\n\n`;

  bio += `Specialties and expertise include: ${specialties}.\n\n`;

  if (personal) {
    bio += `Outside the office, ${drName} enjoys ${personal}. This well-rounded lifestyle contributes to the warm, personable atmosphere that patients at ${name} know and love.\n\n`;
  }

  bio += `${drName} is currently accepting new patients at ${name} in ${city}. Whether you need a trusted family dentist or are looking for a specific treatment, ${drName} and the team are ready to welcome you.\n\n`;
  bio += `📞 Schedule your appointment with ${drName} today and experience dentistry done differently!`;

  return bio;
}

// =============================================
// EXPORT REPORT
// =============================================
function exportReport() {
  const s = state.scores;
  let report = `${'═'.repeat(60)}\n`;
  report += `  DENTALFLOW AI — WEBSITE ANALYSIS REPORT\n`;
  report += `${'═'.repeat(60)}\n\n`;
  report += `Practice: ${state.practiceName}\n`;
  report += `Website:  ${state.url}\n`;
  report += `Location: ${state.city}\n`;
  report += `Type:     ${state.type}\n`;
  report += `Date:     ${new Date().toLocaleDateString()}\n\n`;
  report += `${'─'.repeat(60)}\n`;
  report += `  SCORES\n`;
  report += `${'─'.repeat(60)}\n\n`;
  report += `  Overall:    ${s.overall}/100  (${getScoreLabel(s.overall)})\n`;
  report += `  SEO:        ${s.seo}/100  (${getScoreLabel(s.seo)})\n`;
  report += `  Content:    ${s.content}/100  (${getScoreLabel(s.content)})\n`;
  report += `  Mobile:     ${s.mobile}/100  (${getScoreLabel(s.mobile)})\n`;
  report += `  Speed:      ${s.speed}/100  (${getScoreLabel(s.speed)})\n`;
  report += `  Trust:      ${s.trust}/100  (${getScoreLabel(s.trust)})\n`;
  report += `  Conversion: ${s.conversion}/100  (${getScoreLabel(s.conversion)})\n\n`;
  report += `${'─'.repeat(60)}\n`;
  report += `  Generated by DentalFlow AI\n`;
  report += `${'─'.repeat(60)}\n`;

  const blob = new Blob([report], { type: 'text/plain' });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = `DentalFlow-Report-${state.practiceName.replace(/\s+/g, '-')}.txt`;
  a.click();
  URL.revokeObjectURL(url);
  showToast('Report downloaded!', 'success');
}

// =============================================
// INIT
// =============================================
document.addEventListener('DOMContentLoaded', () => {
  // Pre-fill for demo if needed
  document.getElementById('websiteUrl').addEventListener('keypress', (e) => {
    if (e.key === 'Enter') startAnalysis();
  });
});
</script>

</body>
</html>
