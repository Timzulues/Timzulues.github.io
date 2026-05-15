<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>苍穹 ⋅ 磐石 — 纪律仪表盘</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=DM+Serif+Display&family=DM+Sans:wght@300;400;500;700&family=Fraunces:ital,wght@0,300;0,400;0,500;0,600;1,400&family=Manrope:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,500;0,600;1,400&family=Karla:wght@300;400;500;600&family=Caveat:wght@400;500;600&family=Quicksand:wght@400;500;600&family=Inter:wght@300;400;500;600&family=Noto+Serif+SC:wght@400;500;600&family=Noto+Sans+SC:wght@300;400;500&family=ZCOOL+XiaoWei&display=swap" rel="stylesheet">

<style>
/* ═══════════════════════════════════════════
   主题系统：每日轮换
   ═══════════════════════════════════════════ */

/* 🌅 主题1：晨光 Dawn */
[data-theme="dawn"] {
  --bg: #fdf6ee;
  --bg-soft: #faedd6;
  --bg-card: rgba(255, 251, 245, 0.7);
  --bg-card-hover: rgba(255, 251, 245, 0.95);
  --primary: #d97757;
  --primary-soft: #f4a880;
  --secondary: #c4915c;
  --accent: #a67563;
  --text: #4a3528;
  --text-soft: #8b6b5a;
  --text-dim: #b89c8a;
  --border: rgba(217, 119, 87, 0.2);
  --border-strong: rgba(217, 119, 87, 0.5);
  --success: #8b9d6f;
  --warn: #d9a557;
  --danger: #c25450;
  --font-display: 'Cormorant Garamond', 'Noto Serif SC', serif;
  --font-body: 'Inter', 'Noto Sans SC', sans-serif;
  --font-num: 'Cormorant Garamond', serif;
  --layout: 'centered';
}

/* 🍂 主题2：秋日 Amber */
[data-theme="amber"] {
  --bg: #f5ebd9;
  --bg-soft: #ead7ba;
  --bg-card: rgba(255, 247, 233, 0.6);
  --bg-card-hover: rgba(255, 247, 233, 0.85);
  --primary: #b8530a;
  --primary-soft: #d97a3a;
  --secondary: #6b3410;
  --accent: #8c4a1c;
  --text: #3d2510;
  --text-soft: #7a5230;
  --text-dim: #a88860;
  --border: rgba(184, 83, 10, 0.18);
  --border-strong: rgba(184, 83, 10, 0.45);
  --success: #5c7a3a;
  --warn: #b88010;
  --danger: #a83824;
  --font-display: 'DM Serif Display', 'Noto Serif SC', serif;
  --font-body: 'DM Sans', 'Noto Sans SC', sans-serif;
  --font-num: 'DM Serif Display', serif;
  --layout: 'magazine';
}

/* 🪷 主题3：莲池 Lotus */
[data-theme="lotus"] {
  --bg: #f9f0f0;
  --bg-soft: #f3e3e6;
  --bg-card: rgba(255, 250, 250, 0.7);
  --bg-card-hover: rgba(255, 250, 250, 0.95);
  --primary: #c97b89;
  --primary-soft: #e0a4ae;
  --secondary: #7d9577;
  --accent: #b8909d;
  --text: #3d2a30;
  --text-soft: #745560;
  --text-dim: #a89098;
  --border: rgba(201, 123, 137, 0.2);
  --border-strong: rgba(201, 123, 137, 0.5);
  --success: #7d9577;
  --warn: #d9a557;
  --danger: #b85060;
  --font-display: 'Fraunces', 'Noto Serif SC', serif;
  --font-body: 'Manrope', 'Noto Sans SC', sans-serif;
  --font-num: 'Fraunces', serif;
  --layout: 'cards';
}

/* 🌙 主题4：月白 Moonlit */
[data-theme="moonlit"] {
  --bg: #e8eef2;
  --bg-soft: #d8e1e8;
  --bg-card: rgba(248, 251, 253, 0.6);
  --bg-card-hover: rgba(248, 251, 253, 0.9);
  --primary: #5a7a9e;
  --primary-soft: #88a3bf;
  --secondary: #8e8b86;
  --accent: #6b8aa8;
  --text: #2a3a48;
  --text-soft: #5a6b7a;
  --text-dim: #98a5b3;
  --border: rgba(90, 122, 158, 0.18);
  --border-strong: rgba(90, 122, 158, 0.45);
  --success: #6b8e75;
  --warn: #c4a460;
  --danger: #a85968;
  --font-display: 'Playfair Display', 'Noto Serif SC', serif;
  --font-body: 'Karla', 'Noto Sans SC', sans-serif;
  --font-num: 'Playfair Display', serif;
  --layout: 'timeline';
}

/* 🍑 主题5：桃染 Peach */
[data-theme="peach"] {
  --bg: #fff5ec;
  --bg-soft: #ffe8d6;
  --bg-card: rgba(255, 252, 248, 0.7);
  --bg-card-hover: rgba(255, 252, 248, 0.95);
  --primary: #e88b6a;
  --primary-soft: #f4b298;
  --secondary: #d4a574;
  --accent: #cc7755;
  --text: #4a3325;
  --text-soft: #8a6a52;
  --text-dim: #c4a594;
  --border: rgba(232, 139, 106, 0.2);
  --border-strong: rgba(232, 139, 106, 0.5);
  --success: #8da872;
  --warn: #d9a557;
  --danger: #c25460;
  --font-display: 'Caveat', cursive;
  --font-body: 'Quicksand', 'Noto Sans SC', sans-serif;
  --font-num: 'Quicksand', sans-serif;
  --layout: 'journal';
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--font-body);
  min-height: 100vh;
  transition: background 0.6s ease, color 0.6s ease;
  font-weight: 400;
  line-height: 1.6;
}

/* ═══════════════════════════════════════════
   背景纹理（每个主题不同）
   ═══════════════════════════════════════════ */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  z-index: -2;
  pointer-events: none;
  transition: all 0.6s ease;
}

[data-theme="dawn"] body::before,
body[data-theme="dawn"]::before {
  background: 
    radial-gradient(ellipse at 20% 0%, rgba(244, 168, 128, 0.25), transparent 50%),
    radial-gradient(ellipse at 80% 100%, rgba(217, 165, 87, 0.15), transparent 50%);
}

[data-theme="amber"] body::before,
body[data-theme="amber"]::before {
  background: 
    radial-gradient(ellipse at 30% 20%, rgba(184, 83, 10, 0.08), transparent 60%),
    radial-gradient(ellipse at 70% 80%, rgba(140, 74, 28, 0.06), transparent 60%);
}

[data-theme="lotus"] body::before,
body[data-theme="lotus"]::before {
  background: 
    radial-gradient(ellipse at 15% 30%, rgba(201, 123, 137, 0.15), transparent 50%),
    radial-gradient(ellipse at 85% 70%, rgba(125, 149, 119, 0.12), transparent 50%);
}

[data-theme="moonlit"] body::before,
body[data-theme="moonlit"]::before {
  background: 
    radial-gradient(ellipse at 25% 10%, rgba(136, 163, 191, 0.2), transparent 55%),
    radial-gradient(ellipse at 75% 90%, rgba(142, 139, 134, 0.12), transparent 50%);
}

[data-theme="peach"] body::before,
body[data-theme="peach"]::before {
  background: 
    radial-gradient(ellipse at 30% 20%, rgba(244, 178, 152, 0.25), transparent 55%),
    radial-gradient(ellipse at 75% 80%, rgba(212, 165, 116, 0.15), transparent 50%);
}

.container {
  max-width: 1280px;
  margin: 0 auto;
  padding: 48px 32px 100px;
  position: relative;
  z-index: 2;
}

/* ═══════════════════════════════════════════
   头部
   ═══════════════════════════════════════════ */
.header {
  margin-bottom: 64px;
  text-align: center;
  animation: fadeInDown 0.8s ease-out;
}

@keyframes fadeInDown {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}

.theme-tag {
  display: inline-block;
  font-family: var(--font-body);
  font-size: 11px;
  letter-spacing: 0.4em;
  color: var(--text-dim);
  text-transform: uppercase;
  padding: 6px 18px;
  border: 1px solid var(--border);
  border-radius: 100px;
  margin-bottom: 24px;
  background: var(--bg-card);
  backdrop-filter: blur(8px);
}

h1.title {
  font-family: var(--font-display);
  font-weight: 400;
  font-size: clamp(48px, 7vw, 84px);
  line-height: 0.95;
  letter-spacing: -0.02em;
  color: var(--text);
  margin-bottom: 8px;
}

[data-theme="peach"] h1.title {
  font-weight: 500;
}

h1.title {
  font-family: 'ZCOOL XiaoWei', var(--font-display) !important;
  letter-spacing: 0.05em;
}

h1.title .divider {
  color: var(--primary);
  margin: 0 16px;
  font-style: italic;
  opacity: 0.7;
}

.subtitle {
  font-family: var(--font-display);
  font-style: italic;
  font-size: clamp(16px, 2vw, 20px);
  color: var(--text-soft);
  margin-top: 16px;
  font-weight: 300;
}

[data-theme="peach"] .subtitle {
  font-style: normal;
  font-weight: 500;
  font-size: clamp(20px, 2.5vw, 26px);
}

/* ═══════════════════════════════════════════
   每日晨语
   ═══════════════════════════════════════════ */
.daily-phrase {
  position: relative;
  margin: 48px auto;
  max-width: 720px;
  padding: 32px 40px;
  text-align: center;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 4px;
  backdrop-filter: blur(10px);
  animation: phraseFadeIn 1.2s ease-out 0.3s both;
}

@keyframes phraseFadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.daily-phrase::before,
.daily-phrase::after {
  content: '';
  position: absolute;
  width: 40px;
  height: 1px;
  background: var(--primary);
  top: 50%;
  opacity: 0.4;
}

.daily-phrase::before {
  left: -20px;
}

.daily-phrase::after {
  right: -20px;
}

[data-theme="lotus"] .daily-phrase,
[data-theme="moonlit"] .daily-phrase {
  border-radius: 20px;
}

[data-theme="peach"] .daily-phrase {
  border-radius: 0;
  border-style: dashed;
  transform: rotate(-0.5deg);
}

.phrase-quote-mark {
  font-family: var(--font-display);
  font-size: 48px;
  color: var(--primary);
  opacity: 0.3;
  line-height: 1;
  margin-bottom: -16px;
}

.phrase-text {
  font-family: var(--font-display);
  font-style: italic;
  font-size: clamp(18px, 2.2vw, 22px);
  color: var(--text);
  font-weight: 400;
  line-height: 1.5;
  letter-spacing: 0.01em;
}

[data-theme="peach"] .phrase-text {
  font-style: normal;
  font-size: clamp(22px, 2.6vw, 28px);
}

.phrase-author {
  display: block;
  margin-top: 16px;
  font-family: var(--font-body);
  font-size: 12px;
  letter-spacing: 0.3em;
  color: var(--text-dim);
  text-transform: uppercase;
  font-style: normal;
}

/* ═══════════════════════════════════════════
   日期 + 时钟 + 主题切换
   ═══════════════════════════════════════════ */
.top-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 32px;
  padding: 16px 0;
  border-bottom: 1px solid var(--border);
  flex-wrap: wrap;
  gap: 16px;
}

.date-block {
  font-family: var(--font-display);
  font-size: 16px;
  color: var(--text-soft);
}

.date-block .day {
  font-size: 28px;
  color: var(--text);
  font-weight: 500;
  margin-right: 8px;
}

.date-block .full {
  font-size: 14px;
  color: var(--text-dim);
  letter-spacing: 0.1em;
  margin-left: 12px;
}

.theme-switcher {
  display: flex;
  gap: 8px;
  align-items: center;
}

.theme-switcher .label {
  font-size: 11px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-dim);
  margin-right: 8px;
}

.theme-dot {
  width: 22px;
  height: 22px;
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.3s ease;
  border: 2px solid transparent;
  position: relative;
}

.theme-dot:hover {
  transform: scale(1.15);
}

.theme-dot.active {
  border-color: var(--text);
  transform: scale(1.1);
}

.theme-dot[data-set="dawn"] { background: linear-gradient(135deg, #f4a880, #d97757); }
.theme-dot[data-set="amber"] { background: linear-gradient(135deg, #d97a3a, #b8530a); }
.theme-dot[data-set="lotus"] { background: linear-gradient(135deg, #e0a4ae, #c97b89); }
.theme-dot[data-set="moonlit"] { background: linear-gradient(135deg, #88a3bf, #5a7a9e); }
.theme-dot[data-set="peach"] { background: linear-gradient(135deg, #f4b298, #e88b6a); }

/* ═══════════════════════════════════════════
   价格输入区
   ═══════════════════════════════════════════ */
.input-section {
  margin: 56px 0;
  animation: sectionFadeIn 1s ease-out 0.5s both;
}

@keyframes sectionFadeIn {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

.section-title {
  font-family: var(--font-display);
  font-size: 14px;
  letter-spacing: 0.3em;
  color: var(--text-soft);
  text-transform: uppercase;
  margin-bottom: 24px;
  text-align: center;
  position: relative;
}

.section-title::before,
.section-title::after {
  content: '';
  position: absolute;
  top: 50%;
  width: 60px;
  height: 1px;
  background: var(--border-strong);
}

.section-title::before { left: calc(50% - 140px); }
.section-title::after { right: calc(50% - 140px); }

.inputs-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 24px;
  max-width: 900px;
  margin: 0 auto;
}

.input-field {
  position: relative;
}

.input-field label {
  display: block;
  font-family: var(--font-body);
  font-size: 11px;
  letter-spacing: 0.25em;
  color: var(--text-soft);
  text-transform: uppercase;
  margin-bottom: 8px;
  font-weight: 500;
}

.input-field input {
  width: 100%;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-bottom: 2px solid var(--border-strong);
  border-radius: 4px;
  padding: 16px 18px;
  font-family: var(--font-num);
  font-size: 28px;
  font-weight: 500;
  color: var(--text);
  outline: none;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  backdrop-filter: blur(8px);
}

[data-theme="lotus"] .input-field input,
[data-theme="peach"] .input-field input {
  border-radius: 12px;
}

.input-field input:focus {
  border-color: var(--primary);
  border-bottom-color: var(--primary);
  background: var(--bg-card-hover);
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.04), 0 0 0 4px rgba(217, 119, 87, 0.08);
}

.input-field input::placeholder {
  color: var(--text-dim);
  font-weight: 300;
}

/* 按钮 */
.btn-update {
  display: block;
  margin: 32px auto 0;
  padding: 16px 56px;
  background: var(--primary);
  color: white;
  border: none;
  border-radius: 100px;
  font-family: var(--font-body);
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
  box-shadow: 0 4px 16px rgba(217, 119, 87, 0.2);
}

[data-theme="peach"] .btn-update {
  border-radius: 12px;
  font-family: var(--font-display);
  font-size: 18px;
  text-transform: none;
  letter-spacing: normal;
}

.btn-update::before {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 0;
  height: 0;
  background: rgba(255,255,255,0.3);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: width 0.6s, height 0.6s;
}

.btn-update:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(217, 119, 87, 0.35);
}

.btn-update:hover::before {
  width: 400px;
  height: 400px;
}

.btn-update:active {
  transform: translateY(0) scale(0.98);
}

.btn-update span {
  position: relative;
  z-index: 1;
}

/* 新高横幅 */
.new-high-banner {
  max-width: 720px;
  margin: 24px auto 0;
  padding: 18px 28px;
  background: var(--success);
  color: white;
  border-radius: 4px;
  text-align: center;
  font-family: var(--font-display);
  font-size: 17px;
  font-style: italic;
  font-weight: 500;
  letter-spacing: 0.02em;
  display: none;
  position: relative;
  overflow: hidden;
}

[data-theme="lotus"] .new-high-banner,
[data-theme="peach"] .new-high-banner {
  border-radius: 16px;
}

.new-high-banner.show {
  display: block;
  animation: bannerSlide 0.5s ease-out;
}

@keyframes bannerSlide {
  from { opacity: 0; transform: translateY(-12px); }
  to { opacity: 1; transform: translateY(0); }
}

.new-high-banner::after {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.25), transparent);
  animation: shimmer 2.5s linear infinite;
}

@keyframes shimmer {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

/* ═══════════════════════════════════════════
   状态总览
   ═══════════════════════════════════════════ */
.overview {
  margin: 64px 0;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 24px;
  animation: sectionFadeIn 1s ease-out 0.7s both;
}

.overview-card {
  text-align: center;
  padding: 28px 20px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 6px;
  backdrop-filter: blur(10px);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

[data-theme="lotus"] .overview-card,
[data-theme="peach"] .overview-card {
  border-radius: 20px;
}

[data-theme="amber"] .overview-card {
  border-radius: 0;
  border-top: 3px solid var(--primary);
}

.overview-card:hover {
  background: var(--bg-card-hover);
  transform: translateY(-4px);
  box-shadow: 0 12px 32px rgba(0,0,0,0.06);
}

.overview-label {
  font-family: var(--font-body);
  font-size: 11px;
  letter-spacing: 0.25em;
  color: var(--text-dim);
  text-transform: uppercase;
  font-weight: 500;
  margin-bottom: 12px;
}

.overview-value {
  font-family: var(--font-num);
  font-size: 32px;
  font-weight: 500;
  color: var(--text);
  line-height: 1;
  transition: color 0.3s;
}

.overview-value.color-primary { color: var(--primary); }
.overview-value.color-success { color: var(--success); }
.overview-value.color-warn { color: var(--warn); }
.overview-value.color-danger { color: var(--danger); }

.overview-sub {
  margin-top: 8px;
  font-size: 12px;
  color: var(--text-soft);
  font-style: italic;
  font-family: var(--font-display);
}

/* ═══════════════════════════════════════════
   今日纪律指令面板
   ═══════════════════════════════════════════ */
.action-panel {
  margin: 48px 0;
  padding: 40px 48px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 8px;
  backdrop-filter: blur(10px);
  position: relative;
  animation: sectionFadeIn 1s ease-out 0.9s both;
}

[data-theme="lotus"] .action-panel,
[data-theme="peach"] .action-panel {
  border-radius: 24px;
}

[data-theme="amber"] .action-panel {
  border-radius: 0;
  border-left: 4px solid var(--primary);
}

.action-panel::before {
  content: '◌';
  position: absolute;
  top: -16px;
  left: 32px;
  font-size: 24px;
  color: var(--primary);
  background: var(--bg);
  padding: 0 12px;
}

.action-label {
  font-family: var(--font-body);
  font-size: 11px;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--primary);
  margin-bottom: 16px;
  font-weight: 600;
}

.action-content {
  font-family: var(--font-display);
  font-size: clamp(16px, 1.8vw, 19px);
  line-height: 1.7;
  color: var(--text);
  font-weight: 400;
}

[data-theme="peach"] .action-content {
  font-family: var(--font-body);
  font-weight: 500;
}

.action-content strong {
  color: var(--primary);
  font-weight: 600;
}

.action-content .num-highlight {
  font-family: var(--font-num);
  font-size: 1.1em;
  color: var(--primary);
  font-weight: 600;
  padding: 0 4px;
  font-style: normal;
}

/* ═══════════════════════════════════════════
   账户分区
   ═══════════════════════════════════════════ */
.account-section {
  margin: 80px 0;
  animation: sectionFadeIn 1s ease-out both;
}

.account-section.mountain { animation-delay: 1.1s; }
.account-section.plain { animation-delay: 1.3s; }

.account-header {
  margin-bottom: 40px;
  text-align: center;
  position: relative;
}

.account-illustration {
  font-family: var(--font-display);
  font-size: clamp(72px, 10vw, 120px);
  font-weight: 400;
  color: var(--text);
  line-height: 0.85;
  letter-spacing: -0.04em;
  margin-bottom: 16px;
  position: relative;
  display: inline-block;
}

.account-illustration::after {
  content: '';
  position: absolute;
  bottom: -8px;
  left: 50%;
  transform: translateX(-50%);
  width: 80px;
  height: 2px;
  background: var(--primary);
  opacity: 0.6;
}

.account-meta {
  font-family: var(--font-display);
  font-style: italic;
  font-size: 16px;
  color: var(--text-soft);
  margin-bottom: 6px;
}

.account-tag {
  display: inline-block;
  margin-top: 12px;
  font-family: var(--font-body);
  font-size: 11px;
  letter-spacing: 0.3em;
  color: var(--text-dim);
  text-transform: uppercase;
}

.account-tag::before { content: '— '; }
.account-tag::after { content: ' —'; }

/* 苍穹 - 山形装饰 */
.mountain-deco {
  display: block;
  margin: 24px auto 0;
  width: 60px;
  height: 30px;
}

.plain-deco {
  display: block;
  margin: 24px auto 0;
  width: 80px;
  height: 14px;
}

/* ═══════════════════════════════════════════
   档位卡片
   ═══════════════════════════════════════════ */
.tiers-grid {
  display: grid;
  gap: 20px;
}

/* 不同主题不同布局 */
[data-theme="dawn"] .tiers-grid,
[data-theme="lotus"] .tiers-grid,
[data-theme="moonlit"] .tiers-grid {
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
}

[data-theme="amber"] .tiers-grid {
  grid-template-columns: 1fr 1fr;
  gap: 1px;
  background: var(--border-strong);
  padding: 1px;
}

[data-theme="amber"] .tier-card {
  border-radius: 0;
  border: none;
}

[data-theme="peach"] .tiers-grid {
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 24px;
}

[data-theme="peach"] .tier-card:nth-child(odd) {
  transform: rotate(-0.8deg);
}

[data-theme="peach"] .tier-card:nth-child(even) {
  transform: rotate(0.6deg);
}

.tier-card {
  padding: 28px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 6px;
  backdrop-filter: blur(8px);
  position: relative;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

[data-theme="lotus"] .tier-card,
[data-theme="peach"] .tier-card {
  border-radius: 20px;
}

.tier-card:hover {
  background: var(--bg-card-hover);
  transform: translateY(-6px);
  box-shadow: 0 16px 40px rgba(0,0,0,0.08);
}

[data-theme="peach"] .tier-card:hover {
  transform: translateY(-6px) rotate(0deg);
}

.tier-card.active {
  border-color: var(--primary);
  border-width: 2px;
  background: var(--bg-card-hover);
  box-shadow: 0 8px 32px rgba(217, 119, 87, 0.2);
}

.tier-card.active::before {
  content: '⬢';
  position: absolute;
  top: 12px;
  right: 12px;
  color: var(--primary);
  font-size: 18px;
  animation: pulse 2s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 0.4; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.15); }
}

.tier-top {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  margin-bottom: 8px;
  padding-bottom: 16px;
  border-bottom: 1px solid var(--border);
}

.tier-num {
  font-family: var(--font-display);
  font-style: italic;
  font-size: 14px;
  letter-spacing: 0.2em;
  color: var(--text-soft);
  text-transform: uppercase;
}

.tier-mode {
  font-family: var(--font-body);
  font-size: 10px;
  padding: 3px 12px;
  border-radius: 100px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  font-weight: 600;
}

.tier-mode.grid {
  background: rgba(125, 149, 119, 0.15);
  color: var(--success);
  border: 1px solid var(--success);
}

.tier-mode.build {
  background: rgba(217, 119, 87, 0.15);
  color: var(--primary);
  border: 1px solid var(--primary);
}

.tier-price {
  font-family: var(--font-num);
  font-size: 52px;
  font-weight: 500;
  color: var(--primary);
  line-height: 1;
  margin: 20px 0 8px;
  transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
}

[data-theme="peach"] .tier-price {
  font-family: var(--font-display);
  font-size: 64px;
}

.tier-drop {
  font-family: var(--font-body);
  font-size: 13px;
  letter-spacing: 0.05em;
  color: var(--danger);
  margin-bottom: 20px;
  font-weight: 500;
}

.tier-row {
  display: flex;
  justify-content: space-between;
  padding: 8px 0;
  font-size: 14px;
  border-bottom: 1px dashed var(--border);
}

.tier-row:last-of-type {
  border-bottom: none;
}

.tier-row .k {
  color: var(--text-soft);
  font-size: 12px;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  font-weight: 500;
}

.tier-row .v {
  font-family: var(--font-num);
  color: var(--text);
  font-weight: 500;
  font-size: 15px;
}

.tier-row .v.success { color: var(--success); }
.tier-row .v.warn { color: var(--warn); }
.tier-row .v.primary { color: var(--primary); }

.sell-section {
  margin-top: 20px;
  padding-top: 16px;
  border-top: 1px solid var(--border);
}

.sell-section h4 {
  font-family: var(--font-display);
  font-style: italic;
  font-size: 13px;
  color: var(--success);
  margin-bottom: 12px;
  font-weight: 500;
  letter-spacing: 0.05em;
}

.sell-section h4::before {
  content: '↗ ';
}

/* ═══════════════════════════════════════════
   配置说明（磐石账户的多元配置）
   ═══════════════════════════════════════════ */
.allocation-bar {
  display: flex;
  height: 50px;
  margin: 32px 0;
  border-radius: 4px;
  overflow: hidden;
  border: 1px solid var(--border);
}

[data-theme="lotus"] .allocation-bar,
[data-theme="peach"] .allocation-bar {
  border-radius: 25px;
}

.alloc-seg {
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-body);
  font-size: 11px;
  letter-spacing: 0.1em;
  font-weight: 600;
  color: white;
  text-transform: uppercase;
  transition: all 0.4s;
  position: relative;
  cursor: pointer;
}

.alloc-seg:hover {
  flex-grow: 1.05;
}

.alloc-seg.tqqq { background: var(--primary); }
.alloc-seg.qqq { background: var(--accent); }
.alloc-seg.boxx { background: var(--secondary); color: white; }
.alloc-seg.cash { background: var(--text-dim); color: white; }

.alloc-legend {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-top: 24px;
}

.alloc-item {
  padding: 20px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 6px;
  backdrop-filter: blur(8px);
  transition: all 0.3s;
}

[data-theme="lotus"] .alloc-item,
[data-theme="peach"] .alloc-item {
  border-radius: 16px;
}

.alloc-item:hover {
  transform: translateY(-2px);
  background: var(--bg-card-hover);
}

.alloc-item .name {
  font-family: var(--font-display);
  font-size: 22px;
  font-weight: 500;
  color: var(--text);
  margin-bottom: 4px;
}

.alloc-item .name .dot {
  display: inline-block;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  margin-right: 8px;
}

.alloc-item .pct {
  font-family: var(--font-num);
  font-size: 32px;
  color: var(--primary);
  font-weight: 500;
  line-height: 1;
  margin: 8px 0;
}

.alloc-item .amt {
  font-family: var(--font-body);
  font-size: 13px;
  color: var(--text-soft);
  letter-spacing: 0.05em;
}

.alloc-item .desc {
  margin-top: 12px;
  font-family: var(--font-display);
  font-style: italic;
  font-size: 13px;
  color: var(--text-soft);
  line-height: 1.5;
}

[data-theme="peach"] .alloc-item .desc {
  font-style: normal;
  font-weight: 500;
}

/* ═══════════════════════════════════════════
   纪律清单
   ═══════════════════════════════════════════ */
.rules-block {
  margin: 40px 0;
  padding: 32px 40px;
  background: var(--bg-soft);
  border-radius: 6px;
  position: relative;
}

[data-theme="lotus"] .rules-block,
[data-theme="peach"] .rules-block {
  border-radius: 20px;
}

[data-theme="amber"] .rules-block {
  border-radius: 0;
  border-left: 3px solid var(--primary);
}

.rules-block h3 {
  font-family: var(--font-display);
  font-weight: 500;
  font-size: 18px;
  color: var(--text);
  margin-bottom: 20px;
  letter-spacing: 0.02em;
}

.rules-block h3::before {
  content: '§ ';
  color: var(--primary);
}

.rules-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.rules-list li {
  padding-left: 28px;
  position: relative;
  font-size: 14px;
  line-height: 1.6;
  color: var(--text-soft);
}

.rules-list li::before {
  content: '◇';
  position: absolute;
  left: 0;
  top: 2px;
  color: var(--primary);
  font-size: 14px;
}

.rules-list li strong {
  color: var(--text);
  font-weight: 600;
}

.rules-list li .pulse {
  font-family: var(--font-num);
  color: var(--primary);
  font-weight: 600;
}

/* ═══════════════════════════════════════════
   历史记录
   ═══════════════════════════════════════════ */
.history-section {
  margin: 48px 0;
}

.history-toggle {
  background: none;
  border: 1px solid var(--border);
  padding: 12px 24px;
  border-radius: 100px;
  font-family: var(--font-body);
  font-size: 12px;
  color: var(--text-soft);
  letter-spacing: 0.2em;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.3s;
  display: block;
  margin: 0 auto;
}

.history-toggle:hover {
  background: var(--bg-card-hover);
  color: var(--primary);
  border-color: var(--primary);
}

.history-list {
  display: none;
  max-width: 720px;
  margin: 24px auto 0;
  padding: 24px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 6px;
  max-height: 320px;
  overflow-y: auto;
}

.history-list.show {
  display: block;
  animation: sectionFadeIn 0.4s ease-out;
}

.history-entry {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0;
  border-bottom: 1px dashed var(--border);
  font-size: 14px;
}

.history-entry:last-child {
  border-bottom: none;
}

.history-entry .date {
  font-family: var(--font-num);
  color: var(--text-soft);
  font-size: 13px;
}

.history-entry .change {
  font-family: var(--font-display);
  font-style: italic;
  color: var(--primary);
  font-size: 14px;
}

/* ═══════════════════════════════════════════
   底部
   ═══════════════════════════════════════════ */
.footer {
  margin-top: 100px;
  padding-top: 40px;
  border-top: 1px solid var(--border);
  text-align: center;
  font-family: var(--font-display);
  font-style: italic;
  color: var(--text-dim);
  font-size: 14px;
  line-height: 1.8;
}

[data-theme="peach"] .footer {
  font-style: normal;
  font-weight: 500;
}

.footer .heart {
  color: var(--primary);
  display: inline-block;
  animation: heartBeat 1.8s ease-in-out infinite;
}

@keyframes heartBeat {
  0%, 100% { transform: scale(1); }
  20% { transform: scale(1.2); }
  40% { transform: scale(1); }
  60% { transform: scale(1.15); }
  80% { transform: scale(1); }
}

/* ═══════════════════════════════════════════
   重置按钮（角落）
   ═══════════════════════════════════════════ */
.reset-btn {
  position: fixed;
  bottom: 24px;
  right: 24px;
  background: var(--bg-card);
  border: 1px solid var(--danger);
  color: var(--danger);
  padding: 10px 20px;
  border-radius: 100px;
  font-family: var(--font-body);
  font-size: 11px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  cursor: pointer;
  z-index: 100;
  backdrop-filter: blur(8px);
  transition: all 0.3s;
  opacity: 0.6;
}

.reset-btn:hover {
  opacity: 1;
  background: var(--danger);
  color: white;
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(194, 84, 80, 0.3);
}

/* ═══════════════════════════════════════════
   响应式
   ═══════════════════════════════════════════ */
@media (max-width: 768px) {
  .container {
    padding: 32px 16px 80px;
  }
  
  .top-bar {
    flex-direction: column;
    align-items: flex-start;
  }
  
  .theme-switcher {
    width: 100%;
    overflow-x: auto;
  }
  
  .action-panel {
    padding: 28px 24px;
  }
  
  [data-theme="amber"] .tiers-grid {
    grid-template-columns: 1fr;
  }
}

/* 数字翻动动画 */
@keyframes numberTick {
  0% { transform: translateY(-100%); opacity: 0; }
  100% { transform: translateY(0); opacity: 1; }
}

.number-animate {
  animation: numberTick 0.5s cubic-bezier(0.4, 0, 0.2, 1);
}

/* 滚动条美化 */
::-webkit-scrollbar {
  width: 8px;
  height: 8px;
}
::-webkit-scrollbar-track {
  background: var(--bg-soft);
}
::-webkit-scrollbar-thumb {
  background: var(--primary-soft);
  border-radius: 4px;
}
::-webkit-scrollbar-thumb:hover {
  background: var(--primary);
}

/* ═══════════════════════════════════════════
   总铁律 — 命令版式
   ═══════════════════════════════════════════ */
.commandments-section {
  margin-top: 80px;
  padding: 48px 0 80px;
}
.commandments-header {
  display: flex;
  align-items: center;
  gap: 24px;
  margin-bottom: 48px;
  justify-content: center;
}
.cmd-line {
  flex: 1;
  max-width: 200px;
  height: 1px;
  background: linear-gradient(to right, transparent, var(--primary));
}
.cmd-line:last-child {
  background: linear-gradient(to left, transparent, var(--primary));
}
.cmd-title {
  font-family: var(--font-display);
  font-size: clamp(16px, 2.2vw, 22px);
  letter-spacing: 0.18em;
  color: var(--text);
  white-space: nowrap;
}
.commandments-grid {
  display: grid;
  gap: 14px;
  max-width: 860px;
  margin: 0 auto;
}
.commandment-card {
  display: flex;
  align-items: flex-start;
  gap: 28px;
  padding: 22px 32px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-left: 3px solid var(--primary);
  border-radius: 4px;
  backdrop-filter: blur(8px);
  transition: all 0.3s ease;
}
.commandment-card:hover {
  background: var(--bg-card-hover);
  border-left-color: var(--accent);
  transform: translateX(5px);
}
.cmd-num {
  font-family: var(--font-num);
  font-size: 28px;
  color: var(--primary);
  opacity: 0.55;
  line-height: 1;
  min-width: 28px;
  text-align: center;
  flex-shrink: 0;
  padding-top: 3px;
}
.cmd-text {
  display: flex;
  flex-direction: column;
  gap: 5px;
}
.cmd-text strong {
  font-family: var(--font-body);
  font-size: 15px;
  font-weight: 600;
  color: var(--text);
}
.cmd-text span {
  font-family: var(--font-body);
  font-size: 13px;
  color: var(--text-soft);
  line-height: 1.6;
}
.cmd-final {
  margin-top: 36px;
  text-align: center;
  font-family: var(--font-display);
  font-style: italic;
  font-size: 14px;
  color: var(--text-dim);
  letter-spacing: 0.08em;
}
/* 自动获取状态 */
.fetch-status {
  text-align: center;
  font-size: 12px;
  letter-spacing: 0.05em;
  color: var(--text-dim);
  margin-bottom: 20px;
  min-height: 18px;
  transition: color 0.3s;
}
.btn-row {
  display: flex;
  gap: 12px;
  justify-content: center;
  flex-wrap: wrap;
}
.btn-fetch {
  background: transparent;
  border: 1px solid var(--border-strong);
  color: var(--text-soft);
  padding: 12px 28px;
  border-radius: 2px;
  font-family: var(--font-body);
  font-size: 13px;
  letter-spacing: 0.1em;
  cursor: pointer;
  transition: all 0.3s ease;
}
.btn-fetch:hover {
  background: var(--bg-soft);
  color: var(--text);
}

</style>
</head>
<body data-theme="dawn">

<div class="container">

  <!-- ═══════════ HEADER ═══════════ -->
  <header class="header">
    <span class="theme-tag" id="theme-tag">Dawn · 晨光</span>
    <h1 class="title">苍穹<span class="divider">/</span>磐石</h1>
    <div class="subtitle">纪律即自由，情绪即敌人。</div>
  </header>

  <!-- ═══════════ 每日晨语 ═══════════ -->
  <div class="daily-phrase">
    <div class="phrase-quote-mark">"</div>
    <div class="phrase-text" id="daily-phrase-text">载入中...</div>
    
  </div>

  <!-- ═══════════ 顶部信息条 ═══════════ -->
  <div class="top-bar">
    <div class="date-block">
      <span class="day" id="date-day">--</span>
      <span id="date-month">--月</span>
      <span class="full" id="date-full">----</span>
    </div>
    <div class="theme-switcher">
      <span class="label">主题</span>
      <div class="theme-dot active" data-set="dawn" title="晨光"></div>
      <div class="theme-dot" data-set="amber" title="秋日"></div>
      <div class="theme-dot" data-set="lotus" title="莲池"></div>
      <div class="theme-dot" data-set="moonlit" title="月白"></div>
      <div class="theme-dot" data-set="peach" title="桃染"></div>
    </div>
  </div>

  <!-- ═══════════ 价格输入 ═══════════ -->
  <section class="input-section">
    <div class="section-title">实时价格</div>
    <div id="fetch-status" class="fetch-status">正在自动获取今日价格...</div>
    <div class="inputs-grid">
      <div class="input-field">
        <label>TQQQ 当前价</label>
        <input type="number" id="tqqq-input" step="0.01" placeholder="76.19">
      </div>
      <div class="input-field">
        <label>QQQ 当前价</label>
        <input type="number" id="qqq-input" step="0.01" placeholder="600.00">
      </div>
      <div class="input-field">
        <label>TQQQ 历史最高</label>
        <input type="number" id="tqqq-high-input" step="0.01" placeholder="77.36">
      </div>
    </div>
    <div class="btn-row">
      <button class="btn-update" onclick="updatePrices()"><span>更新纪律</span></button>
      <button class="btn-fetch" onclick="fetchStockPrices()"><span>↻ 重新获取</span></button>
    </div>
    <div class="new-high-banner" id="new-high-banner">✦ 新高纪录已刷新 ✦ 全部纪律已重新计算 ✦</div>
  </section>

  <!-- ═══════════ 状态总览 ═══════════ -->
  <section class="overview">
    <div class="overview-card">
      <div class="overview-label">当前 TQQQ</div>
      <div class="overview-value color-primary" id="ov-tqqq">$ --</div>
      <div class="overview-sub" id="ov-tqqq-sub">尚未录入</div>
    </div>
    <div class="overview-card">
      <div class="overview-label">历史最高</div>
      <div class="overview-value" id="ov-high">$77.36</div>
      <div class="overview-sub">基准价</div>
    </div>
    <div class="overview-card">
      <div class="overview-label">距最高回撤</div>
      <div class="overview-value color-warn" id="ov-drop">--</div>
      <div class="overview-sub" id="ov-drop-sub">待录入</div>
    </div>
    <div class="overview-card">
      <div class="overview-label">当前阶段</div>
      <div class="overview-value color-success" id="ov-phase" style="font-size: 22px;">观望</div>
      <div class="overview-sub" id="ov-phase-sub">--</div>
    </div>
  </section>

  <!-- ═══════════ 今日纪律指令 ═══════════ -->
  <div class="action-panel">
    <div class="action-label">◌ 今日纪律指令</div>
    <div class="action-content" id="action-content">
      等待价格数据 — 正在自动获取，或请手动输入后点击更新。
    </div>
  </div>

  <!-- ═══════════ 苍穹账户 ═══════════ -->
  <section class="account-section mountain">
    <div class="account-header">
      <div class="account-illustration">苍穹</div>
      <div class="account-meta">爸爸账户 · 完整 TQQQ 四档策略</div>
      <div class="account-tag">$96,000 · 进攻 · 4 Tiers</div>
      <svg class="mountain-deco" viewBox="0 0 60 30">
        <path d="M2 28 L18 8 L28 18 L40 4 L58 28 Z" fill="none" stroke="currentColor" stroke-width="1" opacity="0.4"/>
      </svg>
    </div>

    <div class="tiers-grid" id="mountain-tiers"></div>

    <div class="rules-block">
      <h3>苍穹之纪律</h3>
      <ul class="rules-list">
        <li><strong>仅触发档位1</strong>：网格策略，TQQQ涨到 <span class="pulse" id="m-sell-1">--</span> 全卖</li>
        <li><strong>触发至档位2</strong>：网格策略，平均成本+10%全卖（约 <span class="pulse" id="m-sell-2">--</span>）</li>
        <li><strong>触发至档位3</strong>：建仓型 — 前高 <span class="pulse" id="m-sell-3a">--</span> 卖2/3，<span class="pulse" id="m-sell-3b">--</span> 卖1/3</li>
        <li><strong>触发至档位4</strong>：建仓型 — 前高 <span class="pulse" id="m-sell-4a">--</span> 卖2/3，<span class="pulse" id="m-sell-4b">--</span> 卖1/3</li>
        <li><strong>长熊市备用</strong>：建仓12个月没破前高但盈利+25% → 全卖</li>
        <li><strong>灾难场景</strong>：跌破档位4继续跌 → 装死持有，不止损，等下轮牛市</li>
        <li><strong>突破前高失败</strong>：从局部高点回撤-12% → 触发追踪止损</li>
      </ul>
    </div>
  </section>

  <!-- ═══════════ 磐石账户 ═══════════ -->
  <section class="account-section plain">
    <div class="account-header">
      <div class="account-illustration">磐石</div>
      <div class="account-meta">妈妈账户 · 多元配置 · 风险隔离</div>
      <div class="account-tag">$117,000 · 稳健 · Diversified</div>
      <svg class="plain-deco" viewBox="0 0 80 14">
        <path d="M2 8 Q20 4 40 8 T78 8" fill="none" stroke="currentColor" stroke-width="1" opacity="0.4"/>
        <path d="M2 11 Q20 7 40 11 T78 11" fill="none" stroke="currentColor" stroke-width="1" opacity="0.25"/>
      </svg>
    </div>

    <!-- 配置可视化 -->
    <div class="allocation-bar">
      <div class="alloc-seg tqqq" style="flex: 35;" title="TQQQ 35%">TQQQ 35%</div>
      <div class="alloc-seg qqq" style="flex: 30;" title="QQQ 30%">QQQ 30%</div>
      <div class="alloc-seg boxx" style="flex: 25;" title="BOXX 25%">BOXX 25%</div>
      <div class="alloc-seg cash" style="flex: 10;" title="现金 10%">现金</div>
    </div>

    <div class="alloc-legend">
      <div class="alloc-item">
        <div class="name"><span class="dot" style="background: var(--primary);"></span>TQQQ 部分</div>
        <div class="pct">35%</div>
        <div class="amt">$40,950 · 杠杆主仓</div>
        <div class="desc">仅触发档位1+档位2，涨10%全卖。<br>绝不参与档位3/4建仓型。</div>
      </div>
      <div class="alloc-item">
        <div class="name"><span class="dot" style="background: var(--accent);"></span>QQQ 核心</div>
        <div class="pct">30%</div>
        <div class="amt">$35,100 · 无杠杆指数</div>
        <div class="desc">回调 -5/-10/-15% 分三批买入。<br>长期持有，无追踪止损。</div>
      </div>
      <div class="alloc-item">
        <div class="name"><span class="dot" style="background: var(--secondary);"></span>BOXX 现金</div>
        <div class="pct">25%</div>
        <div class="amt">$29,250 · 类现金</div>
        <div class="desc">立即配置，吃约4-5%国债收益。<br>延税结构利于长期持有。</div>
      </div>
      <div class="alloc-item">
        <div class="name"><span class="dot" style="background: var(--text-dim);"></span>应急流动性</div>
        <div class="pct">10%</div>
        <div class="amt">$11,700 · SGOV/BIL</div>
        <div class="desc">短期国债ETF储备。<br>妈妈应急取用渠道。</div>
      </div>
    </div>

    <!-- 磐石的TQQQ档位 -->
    <div style="margin-top: 48px;">
      <div class="section-title" style="text-align: left;">磐石 · TQQQ 部分档位</div>
      <div class="tiers-grid" id="plain-tiers"></div>
    </div>

    <!-- 磐石的QQQ档位 -->
    <div style="margin-top: 48px;">
      <div class="section-title" style="text-align: left;">磐石 · QQQ 核心档位</div>
      <div class="tiers-grid" id="plain-qqq-tiers"></div>
    </div>

    <div class="rules-block">
      <h3>磐石之纪律</h3>
      <ul class="rules-list">
        <li><strong>TQQQ 部分</strong>：仅档位1和档位2，涨10%全卖（网格型）</li>
        <li><strong>QQQ 核心</strong>：回调-5%/-10%/-15%分三批，长期持有</li>
        <li><strong>BOXX 立即配置</strong>，应急金立即配置 SGOV/BIL</li>
        <li><strong>铁律一</strong>：TQQQ部分绝不升级到档位3/4</li>
        <li><strong>铁律二</strong>：BOXX绝不挪用补TQQQ</li>
        <li><strong>铁律三</strong>：妈妈可能要用的钱，永远保守优先</li>
      </ul>
    </div>
  </section>

  <!-- ═══════════ 历史记录 ═══════════ -->
  <section class="history-section">
    <button class="history-toggle" onclick="toggleHistory()">▼ 查看历史记录</button>
    <div class="history-list" id="history-list"></div>
  </section>

  <!-- ═══════════ 总铁律 ═══════════ -->
  <section class="commandments-section">
    <div class="commandments-header">
      <div class="cmd-line"></div>
      <span class="cmd-title">不可违反之总铁律</span>
      <div class="cmd-line"></div>
    </div>
    <div class="commandments-grid">
      <div class="commandment-card">
        <span class="cmd-num">Ⅰ</span>
        <div class="cmd-text">
          <strong>绝不在TQQQ创新高时加仓</strong>
          <span>本策略是反向逻辑，越涨越观望，越跌越执行。</span>
        </div>
      </div>
      <div class="commandment-card">
        <span class="cmd-num">Ⅱ</span>
        <div class="cmd-text">
          <strong>触发档位3时，策略性质从网格转为建仓</strong>
          <span>不同的市场深度，对应不同的应对方式。不可混淆。</span>
        </div>
      </div>
      <div class="commandment-card">
        <span class="cmd-num">Ⅲ</span>
        <div class="cmd-text">
          <strong>纪律机械执行，不许主观判断</strong>
          <span>"我感觉再等等"是散户死亡的起点。规则说什么，就做什么。</span>
        </div>
      </div>
      <div class="commandment-card">
        <span class="cmd-num">Ⅳ</span>
        <div class="cmd-text">
          <strong>两账户独立核算，苍穹与磐石永不交叉</strong>
          <span>资金与策略完全隔离，任何跨账户调配都是违律。</span>
        </div>
      </div>
      <div class="commandment-card">
        <span class="cmd-num">Ⅴ</span>
        <div class="cmd-text">
          <strong>$213,000 是家庭的信任，不是筹码</strong>
          <span>这不是游戏，不是赌场。每一个决定，背后都是人。</span>
        </div>
      </div>
    </div>
    <div class="cmd-final">— 以上五律，执行时无需理解，只需服从 —</div>
  </section>

  <!-- ═══════════ 底部 ═══════════ -->
  <footer class="footer">
    数据本地存储，不上传云端 · 不构成任何投资建议<br>
    本仪表盘仅供纪律追踪使用，不是持牌投顾 <span class="heart">❤</span>
  </footer>

</div>

<button class="reset-btn" onclick="resetAll()">⟲ 重置数据</button>

<script>
// ═══════════════════════════════════════════════════════════
//                   策略配置
// ═══════════════════════════════════════════════════════════

const CONFIG = {
  mountain: {
    name: '苍穹',
    total: 96000,
    tiers: [
      { id: 1, dropPct: 0.10, allocPct: 0.15, type: 'grid' },
      { id: 2, dropPct: 0.20, allocPct: 0.25, type: 'grid' },
      { id: 3, dropPct: 0.30, allocPct: 0.35, type: 'build' },
      { id: 4, dropPct: 0.40, allocPct: 0.25, type: 'build' }
    ]
  },
  plain_tqqq: {
    name: '磐石 TQQQ',
    total: 40950,
    tiers: [
      { id: 1, dropPct: 0.10, allocPct: 0.35, type: 'grid' },
      { id: 2, dropPct: 0.20, allocPct: 0.65, type: 'grid' }
    ]
  },
  plain_qqq: {
    name: '磐石 QQQ',
    total: 35100,
    tiers: [
      { id: 1, dropPct: 0.05, allocPct: 0.30, type: 'grid' },
      { id: 2, dropPct: 0.10, allocPct: 0.35, type: 'grid' },
      { id: 3, dropPct: 0.15, allocPct: 0.35, type: 'grid' }
    ]
  }
};

const GRID_PREMIUM = 1.10;
const SELL_FIRST = 1.00;
const SELL_SECOND = 1.15;

// ═══════════════════════════════════════════════════════════
//                   每日晨语数据库
// ═══════════════════════════════════════════════════════════

const DAILY_PHRASES = [
  "今天也要好好执行纪律。机械执行，不打折扣。",
  "市场不在乎你的情绪，所以让纪律替你思考。",
  "别太早看盘。盯盘是散户的习惯，不是你的。",
  "记住：90%的散户死在嘴硬上。",
  "买入的勇气不在创新高时，而在所有人恐慌时。",
  "Burry说现在像1999末期。你最好相信他一半。",
  "纪律像猫尾巴：你以为你能控制它，其实是它控制你。",
  "今天不交易，就是最好的交易。",
  "$117,000是妈妈的，$96,000是爸爸的。别忘了这一点。",
  "看见TQQQ涨了想加仓？先想想这是谁的钱，再想想纪律怎么说。",
  "持有比买卖难得多。能熬住-30%的人才能享受+200%。",
  "牛市赚钱不算本事，熊市不亏才是真功夫。",
  "你15岁。时间是你最大的资产，不是钱。",
  "Druckenmiller也在加仓GOOGL，但他保留了现金。",
  "TQQQ最大回撤-81.66%。这个数字配得上你的尊重。",
  "今天的恐惧，是未来的利润。",
  "今天的贪婪，是未来的眼泪。",
  "执行计划，不要解读市场。市场不需要被解读。",
  "没有鼓励，只有规则。规则本身就是最好的保护。",
  "想想特朗普跌54%你还能加仓的自己。那个时刻，才是真正的纪律。",
  "记住存款不是真正的财富，能保住的存款才是。",
  "TQQQ不是股票，是一种心理测试。",
  "下跌时买的勇气，来自上涨时卖出的纪律。",
  "纪律不是限制，是让你睡得着的保险。",
  "如果你今天觉得焦虑，那说明你做对了一半。",
  "策略是骨架，纪律是血肉。两者缺一不可。",
  "真正的保护不是告诉你别担心，而是让你有纪律，不需要担心。",
  "看见账户跌-20%？这是你买入的信号，不是离场的信号。",
  "市场永远在测试你。今天的测试是：你能不能不动？",
  "Burry做空NVDA和QQQ。Druckenmiller加仓GOOGL。世界很复杂。",
  "没有人能替你守住纪律。那是你自己的事。",
  "保守不是胆小。保守是对未来的承诺。",
  "记住妈妈的钱不能输。这不是道德问题，是数学问题。",
  "你今天看了几次仪表盘？少看。多睡。",
  "做错决定不可怕，可怕的是不知道自己为什么做。",
  "今天是五个主题之一。明天换个心情，但纪律不换。",
  "下跌不是惩罚，是机会的另一个名字。",
  "$77.36是数字，但守住它的纪律是品格。",
  "记住：最深的关怀，不是温柔，是规则。",
  "如果今天TQQQ涨疯了，记得把这页关掉，去外面走走。"
];

const NEW_HIGH_PHRASES = [
  "✦ 新高纪录已刷新 ✦ 全部纪律已重新计算 ✦",
  "✦ 山又高了一点点 ✦ 但纪律永远不变 ✦",
  "✦ 又是新高 ✦ 策略基准已自动更新 ✦",
  "✦ 创新高 ✦ 按计划观望，绝不追涨 ✦"
];

// ═══════════════════════════════════════════════════════════
//                   状态管理
// ═══════════════════════════════════════════════════════════

let state = {
  tqqqHigh: 77.36,
  tqqqCurrent: null,
  qqqCurrent: null,
  qqqHigh: null,
  lastUpdated: null,
  history: [],
  customTheme: null // null表示自动按日轮换
};

function loadState() {
  try {
    const saved = localStorage.getItem('main_peak_plain_v7');
    if (saved) {
      const parsed = JSON.parse(saved);
      state = { ...state, ...parsed };
    }
  } catch (e) {
    console.error('Load state failed:', e);
  }
}

function saveState() {
  try {
    localStorage.setItem('main_peak_plain_v7', JSON.stringify(state));
  } catch (e) {
    console.error('Save state failed:', e);
  }
}

// ═══════════════════════════════════════════════════════════
//                   主题轮换（按日期）
// ═══════════════════════════════════════════════════════════

const THEMES = ['dawn', 'amber', 'lotus', 'moonlit', 'peach'];
const THEME_NAMES = {
  dawn: 'Dawn · 晨光',
  amber: 'Amber · 秋日',
  lotus: 'Lotus · 莲池',
  moonlit: 'Moonlit · 月白',
  peach: 'Peach · 桃染'
};

function getThemeOfTheDay() {
  if (state.customTheme) return state.customTheme;
  const today = new Date();
  const dayOfYear = Math.floor((today - new Date(today.getFullYear(), 0, 0)) / 86400000);
  return THEMES[dayOfYear % THEMES.length];
}

function applyTheme(themeKey) {
  document.body.setAttribute('data-theme', themeKey);
  document.getElementById('theme-tag').textContent = THEME_NAMES[themeKey];
  document.querySelectorAll('.theme-dot').forEach(d => {
    d.classList.toggle('active', d.dataset.set === themeKey);
  });
}

function setupThemeSwitcher() {
  document.querySelectorAll('.theme-dot').forEach(dot => {
    dot.addEventListener('click', () => {
      state.customTheme = dot.dataset.set;
      saveState();
      applyTheme(dot.dataset.set);
    });
  });
}

// ═══════════════════════════════════════════════════════════
//                   每日晨语
// ═══════════════════════════════════════════════════════════

function getDailyPhrase() {
  const today = new Date();
  const seed = today.getFullYear() * 1000 + today.getMonth() * 100 + today.getDate();
  return DAILY_PHRASES[seed % DAILY_PHRASES.length];
}

function renderDailyPhrase() {
  document.getElementById('daily-phrase-text').textContent = getDailyPhrase();
}

// ═══════════════════════════════════════════════════════════
//                   日期显示
// ═══════════════════════════════════════════════════════════

function renderDate() {
  const d = new Date();
  const weekdays = ['日', '一', '二', '三', '四', '五', '六'];
  document.getElementById('date-day').textContent = d.getDate();
  document.getElementById('date-month').textContent = (d.getMonth() + 1) + '月';
  document.getElementById('date-full').textContent = `${d.getFullYear()} · 星期${weekdays[d.getDay()]}`;
}

// ═══════════════════════════════════════════════════════════
//                   核心：更新价格 + 强制重算
// ═══════════════════════════════════════════════════════════

function updatePrices() {
  const tqqqInput = document.getElementById('tqqq-input').value.trim();
  const qqqInput = document.getElementById('qqq-input').value.trim();
  const highInput = document.getElementById('tqqq-high-input').value.trim();
  
  const tqqq = tqqqInput === '' ? null : parseFloat(tqqqInput);
  const qqq = qqqInput === '' ? null : parseFloat(qqqInput);
  const inputHigh = highInput === '' ? null : parseFloat(highInput);

  // 至少要有一个有效输入
  if ((tqqq === null || isNaN(tqqq)) && 
      (qqq === null || isNaN(qqq)) && 
      (inputHigh === null || isNaN(inputHigh))) {
    alert('请至少输入一个有效的价格。');
    return;
  }

  const prevHigh = state.tqqqHigh;
  let isNewHigh = false;
  let newHighFinal = prevHigh;

  // 步骤1：处理用户手动输入的高点
  if (inputHigh !== null && !isNaN(inputHigh) && inputHigh > 0) {
    if (Math.abs(inputHigh - prevHigh) > 0.001) {
      newHighFinal = inputHigh;
      isNewHigh = inputHigh > prevHigh;
      state.history.push({
        date: new Date().toISOString(),
        type: 'manual_high',
        from: prevHigh,
        to: inputHigh,
        note: '手动调整最高'
      });
    }
  }

  // 步骤2：处理当前价是否突破最高
  if (tqqq !== null && !isNaN(tqqq) && tqqq > 0) {
    if (tqqq > newHighFinal) {
      state.history.push({
        date: new Date().toISOString(),
        type: 'auto_high',
        from: newHighFinal,
        to: tqqq,
        note: '当前价突破最高'
      });
      newHighFinal = tqqq;
      isNewHigh = true;
    }
    state.tqqqCurrent = tqqq;
  }

  // 步骤3：更新QQQ
  if (qqq !== null && !isNaN(qqq) && qqq > 0) {
    state.qqqCurrent = qqq;
    if (!state.qqqHigh || qqq > state.qqqHigh) {
      state.qqqHigh = qqq;
    }
  }

  // 步骤4：最关键 - 无论如何都强制更新 tqqqHigh 并重算
  state.tqqqHigh = newHighFinal;
  state.lastUpdated = new Date().toISOString();

  saveState();
  
  // 强制全量重渲染（即便高点没变也要重渲染）
  renderAll();

  // 显示新高警报
  if (isNewHigh) {
    const banner = document.getElementById('new-high-banner');
    const phrase = NEW_HIGH_PHRASES[Math.floor(Math.random() * NEW_HIGH_PHRASES.length)];
    banner.textContent = phrase;
    banner.classList.add('show');
    setTimeout(() => banner.classList.remove('show'), 6000);
  }

  // 数字动画
  document.querySelectorAll('.tier-price, .overview-value').forEach(el => {
    el.classList.remove('number-animate');
    void el.offsetWidth;
    el.classList.add('number-animate');
  });
}

// ═══════════════════════════════════════════════════════════
//                   渲染：档位卡片
// ═══════════════════════════════════════════════════════════

function calculateTiers(config, basePrice) {
  let cumCost = 0;
  let cumShares = 0;
  return config.tiers.map(tier => {
    const buyPrice = basePrice * (1 - tier.dropPct);
    const investAmount = config.total * tier.allocPct;
    const shares = investAmount / buyPrice;
    cumCost += investAmount;
    cumShares += shares;
    const avgCost = cumCost / cumShares;
    return { ...tier, buyPrice, investAmount, shares, avgCost, cumCost };
  });
}

function renderTierCards(containerId, config, basePrice, currentPrice, isQQQ = false) {
  const container = document.getElementById(containerId);
  if (!container) return;
  
  const tiers = calculateTiers(config, basePrice);
  container.innerHTML = '';

  tiers.forEach((tier, idx) => {
    const isActive = currentPrice && currentPrice <= tier.buyPrice;
    const card = document.createElement('div');
    card.className = 'tier-card' + (isActive ? ' active' : '');

    let sellInfo = '';
    if (tier.type === 'grid') {
      const gridSell = tier.buyPrice * GRID_PREMIUM;
      const cumulativeSell = tier.avgCost * GRID_PREMIUM;
      sellInfo = `
        <div class="sell-section">
          <h4>卖出条件 · 网格</h4>
          <div class="tier-row">
            <span class="k">单档+10%</span>
            <span class="v success">$${gridSell.toFixed(2)}</span>
          </div>
          ${idx > 0 ? `
          <div class="tier-row">
            <span class="k">累计成本+10%</span>
            <span class="v warn">$${cumulativeSell.toFixed(2)}</span>
          </div>` : ''}
        </div>
      `;
    } else {
      const sellA = basePrice * SELL_FIRST;
      const sellB = basePrice * SELL_SECOND;
      sellInfo = `
        <div class="sell-section">
          <h4>卖出条件 · 建仓</h4>
          <div class="tier-row">
            <span class="k">前高 卖2/3</span>
            <span class="v success">$${sellA.toFixed(2)}</span>
          </div>
          <div class="tier-row">
            <span class="k">前高+15% 卖1/3</span>
            <span class="v success">$${sellB.toFixed(2)}</span>
          </div>
        </div>
      `;
    }

    const ticker = isQQQ ? 'QQQ' : 'TQQQ';

    card.innerHTML = `
      <div class="tier-top">
        <span class="tier-num">${ticker} · 档位 ${tier.id}</span>
        <span class="tier-mode ${tier.type}">${tier.type === 'grid' ? '网格' : '建仓'}</span>
      </div>
      <div class="tier-price">$${tier.buyPrice.toFixed(2)}</div>
      <div class="tier-drop">↓ ${(tier.dropPct * 100).toFixed(0)}% 从 $${basePrice.toFixed(2)}</div>
      <div class="tier-row">
        <span class="k">投入金额</span>
        <span class="v">$${tier.investAmount.toLocaleString('en-US', {maximumFractionDigits: 0})}</span>
      </div>
      <div class="tier-row">
        <span class="k">仓位占比</span>
        <span class="v">${(tier.allocPct * 100).toFixed(0)}%</span>
      </div>
      <div class="tier-row">
        <span class="k">股数</span>
        <span class="v">${tier.shares.toFixed(2)}</span>
      </div>
      <div class="tier-row">
        <span class="k">累计平均成本</span>
        <span class="v primary">$${tier.avgCost.toFixed(2)}</span>
      </div>
      ${sellInfo}
    `;
    container.appendChild(card);
  });
}

// ═══════════════════════════════════════════════════════════
//                   渲染：状态总览 + 指令
// ═══════════════════════════════════════════════════════════

function renderOverview() {
  const high = state.tqqqHigh;
  const current = state.tqqqCurrent;

  document.getElementById('ov-high').textContent = `$${high.toFixed(2)}`;
  
  if (current !== null && !isNaN(current)) {
    document.getElementById('ov-tqqq').textContent = `$${current.toFixed(2)}`;
    
    const dropPct = ((high - current) / high) * 100;
    const dropEl = document.getElementById('ov-drop');
    dropEl.textContent = dropPct >= 0 ? `-${dropPct.toFixed(2)}%` : `+${(-dropPct).toFixed(2)}%`;
    
    const dropSub = document.getElementById('ov-drop-sub');
    if (dropPct < 0) {
      dropEl.className = 'overview-value color-success';
      dropSub.textContent = '已创新高 ☀';
    } else if (dropPct < 5) {
      dropEl.className = 'overview-value color-success';
      dropSub.textContent = '观望区间';
    } else if (dropPct < 15) {
      dropEl.className = 'overview-value color-warn';
      dropSub.textContent = '准备档位1';
    } else if (dropPct < 25) {
      dropEl.className = 'overview-value color-primary';
      dropSub.textContent = '档位区间';
    } else {
      dropEl.className = 'overview-value color-danger';
      dropSub.textContent = '深度回调';
    }

    // 当前TQQQ的对比
    const tqqqEl = document.getElementById('ov-tqqq');
    if (current > high * 0.98) {
      document.getElementById('ov-tqqq-sub').textContent = '接近高点';
    } else {
      document.getElementById('ov-tqqq-sub').textContent = '已录入';
    }
    
    renderActionContent(current, high);
    renderPhase(current, high);
  } else {
    document.getElementById('ov-tqqq').textContent = '$ --';
    document.getElementById('ov-tqqq-sub').textContent = '尚未录入';
    document.getElementById('ov-drop').textContent = '--';
    document.getElementById('ov-drop-sub').textContent = '待录入';
    document.getElementById('ov-phase').textContent = '观望';
    document.getElementById('ov-phase-sub').textContent = '尚未录入';
    document.getElementById('action-content').innerHTML = '等待价格数据 — 正在自动获取，或请手动输入后点击更新。';
  }

  // 卖出纪律计算
  renderSellRules();
}

function renderPhase(current, high) {
  const dropPct = (high - current) / high;
  const phaseEl = document.getElementById('ov-phase');
  const subEl = document.getElementById('ov-phase-sub');

  if (dropPct < 0) {
    phaseEl.textContent = '新高';
    phaseEl.className = 'overview-value color-success';
    subEl.textContent = '不许加仓喔';
  } else if (dropPct < 0.05) {
    phaseEl.textContent = '观望';
    phaseEl.className = 'overview-value color-success';
    subEl.textContent = '保持冷静';
  } else if (dropPct < 0.10) {
    phaseEl.textContent = '档位1准备';
    phaseEl.className = 'overview-value color-warn';
    subEl.textContent = '手指放键盘';
  } else if (dropPct < 0.20) {
    phaseEl.textContent = '档位1已触发';
    phaseEl.className = 'overview-value color-primary';
    subEl.textContent = '开始建仓';
  } else if (dropPct < 0.30) {
    phaseEl.textContent = '档位2已触发';
    phaseEl.className = 'overview-value color-primary';
    subEl.textContent = '累计40%仓位';
  } else if (dropPct < 0.40) {
    phaseEl.textContent = '档位3已触发';
    phaseEl.className = 'overview-value color-danger';
    subEl.textContent = '建仓型启动';
  } else {
    phaseEl.textContent = '档位4已触发';
    phaseEl.className = 'overview-value color-danger';
    subEl.textContent = '满仓装死模式';
  }
}

function renderActionContent(current, high) {
  const dropPct = (high - current) / high;
  const action = document.getElementById('action-content');
  const t1 = high * 0.9;
  const t2 = high * 0.8;
  const t3 = high * 0.7;
  const t4 = high * 0.6;

  if (dropPct < 0) {
    action.innerHTML = `
      TQQQ <span class="num-highlight">$${current.toFixed(2)}</span> 已创新高，基准价已自动更新。<br><br>
      <strong>今日指令</strong>：保持现金，<strong>绝不</strong>追涨加仓。
      账户苍穹持现金或BOXX，账户磐石按计划配置QQQ/BOXX/应急金。
      下一档买入触发：<span class="num-highlight">$${(current * 0.9).toFixed(2)}</span>。
    `;
  } else if (dropPct < 0.05) {
    action.innerHTML = `
      当前 <span class="num-highlight">$${current.toFixed(2)}</span>，距前高仅 -${(dropPct*100).toFixed(1)}%。<br><br>
      <strong>今日指令</strong>：什么都不做。纪律告诉你不在创新高附近加仓。
      下一档触发价 <span class="num-highlight">$${t1.toFixed(2)}</span>，还差 <span class="num-highlight">$${(current - t1).toFixed(2)}</span>。
    `;
  } else if (dropPct < 0.10) {
    action.innerHTML = `
      已回调 -${(dropPct*100).toFixed(1)}%，接近档位1。<br><br>
      <strong>今日指令</strong>：准备执行档位1。
      触发价 <span class="num-highlight">$${t1.toFixed(2)}</span>。<br>
      · 苍穹买入 <span class="num-highlight">$14,400</span>（15%仓位）<br>
      · 磐石TQQQ买入 <span class="num-highlight">$14,333</span>（35%仓位）<br>
      ⚠️ 不许提前下单！纪律是机械执行！
    `;
  } else if (dropPct < 0.20) {
    action.innerHTML = `
      <strong>档位1已触发！</strong> 当前 <span class="num-highlight">$${current.toFixed(2)}</span>。<br><br>
      <strong>苍穹</strong>：已建仓 <span class="num-highlight">$14,400</span>（15%）@ ~$${t1.toFixed(2)}<br>
      <strong>磐石</strong>：已建仓 <span class="num-highlight">$14,333</span>（35%TQQQ预算）<br><br>
      <strong>后续</strong>：反弹至 <span class="num-highlight">$${(t1*1.10).toFixed(2)}</span> → 网格卖出；
      继续跌至 <span class="num-highlight">$${t2.toFixed(2)}</span> → 触发档位2。
    `;
  } else if (dropPct < 0.30) {
    const avg2 = (0.15*t1 + 0.25*t2) / 0.40;
    action.innerHTML = `
      <strong>档位2已触发！</strong> 当前 <span class="num-highlight">$${current.toFixed(2)}</span>。<br><br>
      <strong>苍穹</strong>：再加 <span class="num-highlight">$24,000</span>（累计40%）<br>
      <strong>磐石</strong>：再加 <span class="num-highlight">$26,617</span>（TQQQ部分满仓）<br>
      苍穹平均成本 <span class="num-highlight">$${avg2.toFixed(2)}</span>。<br><br>
      <strong>后续</strong>：反弹至 <span class="num-highlight">$${(avg2*1.10).toFixed(2)}</span> → 全卖；
      继续跌至 <span class="num-highlight">$${t3.toFixed(2)}</span> → 仅苍穹升级至档位3。<br>
      ⚠️ 磐石绝不进入档位3！
    `;
  } else if (dropPct < 0.40) {
    const avg3 = (0.15*t1 + 0.25*t2 + 0.35*t3) / 0.75;
    action.innerHTML = `
      <strong>档位3已触发！策略性质改变为建仓型！</strong><br>
      当前 <span class="num-highlight">$${current.toFixed(2)}</span>。<br><br>
      <strong>苍穹</strong>：再加 <span class="num-highlight">$33,600</span>（累计75%）<br>
      苍穹平均成本 <span class="num-highlight">$${avg3.toFixed(2)}</span>。<br>
      ⛔ 磐石账户不动作！<br><br>
      <strong>后续</strong>：等TQQQ回到前高 <span class="num-highlight">$${high.toFixed(2)}</span> 卖2/3；
      涨至 <span class="num-highlight">$${(high*1.15).toFixed(2)}</span> 卖1/3。<br>
      备用：12个月没破前高+盈利25% → 全卖。
    `;
  } else {
    const avg4 = (0.15*t1 + 0.25*t2 + 0.35*t3 + 0.25*t4) / 1.0;
    action.innerHTML = `
      <strong>档位4已触发！苍穹满仓！</strong><br>
      当前 <span class="num-highlight">$${current.toFixed(2)}</span>。<br><br>
      <strong>苍穹</strong>：再加 <span class="num-highlight">$24,000</span>（累计100%）<br>
      苍穹平均成本 <span class="num-highlight">$${avg4.toFixed(2)}</span>。<br>
      ⛔ 磐石保持冷静！BOXX不许挪用！<br><br>
      <strong>后续</strong>：前高 <span class="num-highlight">$${high.toFixed(2)}</span> 卖2/3；
      <span class="num-highlight">$${(high*1.15).toFixed(2)}</span> 卖1/3。<br>
      继续跌 → 装死持有等下轮牛市。<strong>不止损，不加仓，不卖飞。</strong>
    `;
  }
}

function renderSellRules() {
  const high = state.tqqqHigh;
  const t1 = high * 0.9;
  const t2 = high * 0.8;
  const t3 = high * 0.7;
  const t4 = high * 0.6;
  
  const avg1 = t1;
  const avg2 = (0.15*t1 + 0.25*t2) / 0.40;

  document.getElementById('m-sell-1').textContent = `$${(avg1*1.10).toFixed(2)}`;
  document.getElementById('m-sell-2').textContent = `$${(avg2*1.10).toFixed(2)}`;
  document.getElementById('m-sell-3a').textContent = `$${high.toFixed(2)}`;
  document.getElementById('m-sell-3b').textContent = `$${(high*1.15).toFixed(2)}`;
  document.getElementById('m-sell-4a').textContent = `$${high.toFixed(2)}`;
  document.getElementById('m-sell-4b').textContent = `$${(high*1.15).toFixed(2)}`;
}

// ═══════════════════════════════════════════════════════════
//                   渲染：历史记录
// ═══════════════════════════════════════════════════════════

function renderHistory() {
  const list = document.getElementById('history-list');
  if (!state.history || state.history.length === 0) {
    list.innerHTML = '<div style="text-align: center; padding: 20px; color: var(--text-dim);">暂无历史记录</div>';
    return;
  }
  list.innerHTML = state.history.slice().reverse().slice(0, 50).map(h => {
    const d = new Date(h.date);
    const dateStr = `${d.getMonth()+1}/${d.getDate()} ${d.getHours().toString().padStart(2,'0')}:${d.getMinutes().toString().padStart(2,'0')}`;
    return `
      <div class="history-entry">
        <span class="date">${dateStr}</span>
        <span class="change">${h.note}：$${h.from.toFixed(2)} → $${h.to.toFixed(2)}</span>
      </div>
    `;
  }).join('');
}

function toggleHistory() {
  document.getElementById('history-list').classList.toggle('show');
}

// ═══════════════════════════════════════════════════════════
//                   总渲染
// ═══════════════════════════════════════════════════════════

function renderAll() {
  // 1. 档位卡片（苍穹、磐石TQQQ、磐石QQQ）
  renderTierCards('mountain-tiers', CONFIG.mountain, state.tqqqHigh, state.tqqqCurrent, false);
  renderTierCards('plain-tiers', CONFIG.plain_tqqq, state.tqqqHigh, state.tqqqCurrent, false);
  
  // QQQ卡片使用QQQ的高点
  const qqqHigh = state.qqqHigh || state.qqqCurrent || 600;
  renderTierCards('plain-qqq-tiers', CONFIG.plain_qqq, qqqHigh, state.qqqCurrent, true);
  
  // 2. 状态总览
  renderOverview();
  
  // 3. 历史记录
  renderHistory();
}

// ═══════════════════════════════════════════════════════════
//                   重置
// ═══════════════════════════════════════════════════════════

function resetAll() {
  if (!confirm('确认重置所有数据？此操作不可逆。')) return;
  localStorage.removeItem('main_peak_plain_v7');
  state = {
    tqqqHigh: 77.36,
    tqqqCurrent: null,
    qqqCurrent: null,
    qqqHigh: null,
    lastUpdated: null,
    history: [],
    customTheme: null
  };
  document.getElementById('tqqq-input').value = '';
  document.getElementById('qqq-input').value = '';
  document.getElementById('tqqq-high-input').value = '';
  applyTheme(getThemeOfTheDay());
  renderAll();
}


// ═══════════════════════════════════════════════════════════
//                   自动获取实时股价（Yahoo Finance）
// ═══════════════════════════════════════════════════════════

async function fetchStockPrices() {
  const statusEl = document.getElementById('fetch-status');
  if (!statusEl) return;
  statusEl.textContent = '正在获取实时价格...';
  statusEl.style.color = 'var(--text-dim)';

  try {
    const [tqqqRes, qqqRes] = await Promise.all([
      fetch(`https://query1.finance.yahoo.com/v8/finance/chart/TQQQ?range=1d&interval=1d&_=${Date.now()}`),
      fetch(`https://query1.finance.yahoo.com/v8/finance/chart/QQQ?range=1d&interval=1d&_=${Date.now()}`)
    ]);

    if (!tqqqRes.ok || !qqqRes.ok) throw new Error('HTTP error');

    const [tqqqData, qqqData] = await Promise.all([tqqqRes.json(), qqqRes.json()]);

    const tqqqPrice = tqqqData?.chart?.result?.[0]?.meta?.regularMarketPrice;
    const qqqPrice  = qqqData?.chart?.result?.[0]?.meta?.regularMarketPrice;

    if (!tqqqPrice || !qqqPrice) throw new Error('No price data');

    document.getElementById('tqqq-input').value = tqqqPrice.toFixed(2);
    document.getElementById('qqq-input').value  = qqqPrice.toFixed(2);

    const now = new Date();
    const timeStr = `${now.getHours()}:${now.getMinutes().toString().padStart(2,'0')}`;
    statusEl.textContent = `✓ 已自动获取实时价格 · ${timeStr} · TQQQ $${tqqqPrice.toFixed(2)}  QQQ $${qqqPrice.toFixed(2)}`;
    statusEl.style.color = 'var(--success)';

    // 自动刷新计算
    updatePrices();

  } catch (e) {
    // CORS or network error — graceful fallback
    const isFile = location.protocol === 'file:';
    statusEl.textContent = isFile
      ? '⚠ 本地文件无法直接请求股价（浏览器安全限制）—— 请手动输入，或将文件托管到 GitHub Pages'
      : '⚠ 自动获取失败（网络或市场已关闭），请手动输入价格';
    statusEl.style.color = 'var(--warn)';
  }
}

// ═══════════════════════════════════════════════════════════
//                   初始化
// ═══════════════════════════════════════════════════════════

function init() {
  loadState();
  applyTheme(getThemeOfTheDay());
  setupThemeSwitcher();
  renderDate();
  renderDailyPhrase();
  
  // 填充输入框
  if (state.tqqqCurrent !== null) document.getElementById('tqqq-input').value = state.tqqqCurrent;
  if (state.qqqCurrent !== null) document.getElementById('qqq-input').value = state.qqqCurrent;
  document.getElementById('tqqq-high-input').value = state.tqqqHigh;

  renderAll();

  // 自动获取实时股价
  fetchStockPrices();

  // 回车提交
  ['tqqq-input', 'qqq-input', 'tqqq-high-input'].forEach(id => {
    document.getElementById(id).addEventListener('keydown', e => {
      if (e.key === 'Enter') {
        e.preventDefault();
        updatePrices();
      }
    });
  });
}

document.addEventListener('DOMContentLoaded', init);
</script>
</body>
</html>
