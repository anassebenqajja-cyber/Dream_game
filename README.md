<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Dream games</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@400;500;600&family=Lalezar&family=Space+Mono:wght@400;700&display=swap">
<style id="app-css">
/* Layout: cartridge shelf. Brand bar, compact hero, search + platform filter, grid of cartridge cards. An owner-only side sheet adds games and publishes. */
:root{
  --bg:#E8EEF2;
  --surface:#F6F9FB;
  --ink:#10222B;
  --muted:#4A626D;
  --line:#C3D2DA;
  --cart:#D3DDE4;
  --cart-deep:#BCCAD3;
  --accent:#C2410C;
  --accent-ink:#FFFFFF;
  --accent2:#0B6F82;
  --pin:#B8921F;
  --danger:#B42318;
  --font-display:'Lalezar','Tajawal',system-ui,sans-serif;
  --font-body:'IBM Plex Sans Arabic','Tajawal',system-ui,sans-serif;
  --font-mono:'Space Mono',ui-monospace,Menlo,monospace;
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    --bg:#0B161C;
    --surface:#12212A;
    --ink:#E7F0F4;
    --muted:#9FB5BF;
    --line:#24404C;
    --cart:#1A2E39;
    --cart-deep:#0F1D25;
    --accent:#FF8A4C;
    --accent-ink:#1C0C03;
    --accent2:#56D3E6;
    --pin:#E2BC4F;
    --danger:#FF8F87;
    color-scheme:dark;
  }
}
:root[data-theme="dark"]{
  --bg:#0B161C;
  --surface:#12212A;
  --ink:#E7F0F4;
  --muted:#9FB5BF;
  --line:#24404C;
  --cart:#1A2E39;
  --cart-deep:#0F1D25;
  --accent:#FF8A4C;
  --accent-ink:#1C0C03;
  --accent2:#56D3E6;
  --pin:#E2BC4F;
  --danger:#FF8F87;
  color-scheme:dark;
}

*{box-sizing:border-box}
body{background:var(--bg);color:var(--ink);font-family:var(--font-body);font-size:16px;line-height:1.6;-webkit-text-size-adjust:100%}
:focus-visible{outline:3px solid var(--accent2);outline-offset:2px}
.sr{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0 0 0 0);white-space:nowrap}

.shell{padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));padding-block:20px 56px}
.wrap{max-width:1080px;margin:0 auto}

.top{display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap}
.brand{display:flex;align-items:center;gap:10px;font-family:var(--font-display);font-size:1.75rem;line-height:1;min-width:0}
.brand span{overflow-wrap:anywhere}
.logo{flex:none;height:64px;width:auto;max-width:none;display:block}
.l-body{fill:var(--accent)}
.l-label{fill:var(--bg)}
.l-pins{stroke:var(--bg);stroke-width:2;fill:none}

.btn{display:inline-flex;align-items:center;justify-content:center;gap:8px;min-height:44px;padding:10px 18px;border-radius:8px;border:1px solid transparent;font:inherit;font-weight:600;line-height:1.2;cursor:pointer;text-decoration:none}
.btn-primary{background:var(--accent);color:var(--accent-ink)}
.btn-primary:hover{filter:brightness(1.08)}
.btn-primary:disabled{background:var(--cart-deep);color:var(--muted);cursor:not-allowed;filter:none}
.btn-ghost{background:transparent;color:var(--ink);border-color:var(--line)}
.btn-ghost:hover{background:var(--surface)}
.btn-armed{background:var(--danger);color:var(--accent-ink);border-color:var(--danger)}

.hero{margin-top:26px;padding:34px clamp(16px,4vw,40px);border-radius:18px;background-color:var(--surface);background-image:radial-gradient(var(--line) 1.2px,transparent 1.4px);background-size:16px 16px;display:grid;gap:14px;justify-items:start}
.stat{margin:0;font-family:var(--font-mono);font-size:.78rem;letter-spacing:.04em;color:var(--muted)}
.hero h1{margin:0;font-family:var(--font-display);font-weight:400;font-size:clamp(2.4rem,8vw,4.4rem);line-height:1.08;text-wrap:balance;overflow-wrap:anywhere}
.lead{margin:0;max-width:52ch;color:var(--muted)}

.bar{display:flex;gap:12px;align-items:center;flex-wrap:wrap;margin-top:28px}
.search{flex:1 1 240px;min-width:0}
.chips{display:flex;gap:8px;flex-wrap:wrap}
.chip{border:1px solid var(--line);background:transparent;color:var(--ink);padding:8px 16px;border-radius:999px;font:inherit;font-size:.92rem;min-height:40px;cursor:pointer}
.chip[aria-pressed="true"]{background:var(--ink);color:var(--bg);border-color:var(--ink)}

input,textarea,select{font:inherit;color:var(--ink);background:var(--bg);border:1px solid var(--line);border-radius:8px;padding:10px 12px;min-height:44px;width:100%;min-width:0}
textarea{resize:vertical}
input::placeholder,textarea::placeholder{color:var(--muted)}

.notice{margin:16px 0 0;padding:10px 14px;border-radius:8px;background:var(--surface);color:var(--muted);font-size:.9rem}
.empty{margin:28px 0;color:var(--muted);text-align:center}

.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(min(100%,250px),1fr));gap:22px;margin-top:20px}
.cart{position:relative;display:flex;flex-direction:column;min-width:0;background:var(--cart);padding:22px 14px 0;clip-path:polygon(0 16px,16px 0,calc(100% - 16px) 0,100% 16px,100% 100%,0 100%);transition:transform .2s ease;animation:rise .45s ease backwards;animation-delay:calc(var(--i,0) * 50ms)}
.cart:hover{transform:translateY(-4px)}
.cart::before{content:"";position:absolute;top:9px;left:50%;translate:-50% 0;width:38%;height:4px;border-radius:2px;background:var(--cart-deep)}
@keyframes rise{from{transform:translateY(12px)}to{transform:none}}

.label{position:relative;border-radius:8px;overflow:hidden;aspect-ratio:4/3;max-width:100%;background:var(--cart-deep);box-shadow:inset 0 0 0 2px rgba(0,0,0,.08)}
.cover{display:block;width:100%;height:100%;object-fit:cover}
.art{position:relative;width:100%;height:100%;display:grid;place-items:center}
.art b{position:relative;z-index:1;font-family:var(--font-display);font-weight:400;font-size:6rem;line-height:1;color:rgba(255,255,255,.92);text-shadow:0 3px 0 rgba(0,0,0,.2)}
.art::after{content:"";position:absolute;inset:0;background-image:linear-gradient(rgba(255,255,255,.07) 1px,transparent 1px),linear-gradient(90deg,rgba(255,255,255,.07) 1px,transparent 1px);background-size:12px 12px}
.tag{position:absolute;top:8px;inset-inline-start:8px;z-index:2;padding:3px 9px;border-radius:4px;background:rgba(8,18,24,.8);color:#fff;font-size:.74rem;font-weight:500}
.tag-sample{inset-inline-start:auto;inset-inline-end:8px;background:rgba(255,255,255,.92);color:#10222B}

.cb{display:flex;flex-direction:column;gap:8px;flex:1;padding:14px 2px 14px}
.cb h3{margin:0;font-family:var(--font-display);font-weight:400;font-size:1.5rem;line-height:1.15;overflow-wrap:anywhere}
.meta{display:flex;flex-wrap:wrap;gap:4px 12px;margin:0;font-family:var(--font-mono);font-size:.74rem;color:var(--muted)}
.desc{margin:0;color:var(--muted);font-size:.93rem;display:-webkit-box;-webkit-line-clamp:3;line-clamp:3;-webkit-box-orient:vertical;overflow:hidden;overflow-wrap:anywhere}
.get{margin-top:auto;width:100%}
.pins{height:14px;margin:0 14px;background:repeating-linear-gradient(90deg,var(--pin) 0 5px,transparent 5px 10px);opacity:.9}

.toast{position:fixed;left:0;right:0;bottom:env(safe-area-inset-bottom,0px);display:flex;justify-content:center;padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));padding-bottom:16px;pointer-events:none;z-index:50}
.toast span{background:var(--ink);color:var(--bg);padding:10px 16px;border-radius:10px;font-size:.95rem;max-width:100%}

dialog.sheet{position:fixed;inset:0;margin:0 auto;width:min(640px,100%);max-width:100%;height:100dvh;max-height:100dvh;padding:env(safe-area-inset-top,0px) 0 env(safe-area-inset-bottom,0px);border:0;background:var(--surface);color:var(--ink)}
dialog.sheet::backdrop{background:rgba(5,12,16,.62)}
.sheet-in{height:100%;overflow-y:auto;padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));padding-block:16px 0}
.sheet-head{display:flex;align-items:center;justify-content:space-between;gap:12px}
.sheet-head h2{margin:0;font-family:var(--font-display);font-weight:400;font-size:1.8rem}
.block{display:grid;gap:14px;margin-top:22px;padding-top:18px;border-top:1px solid var(--line)}
.block h3{margin:0;font-size:1rem;font-weight:600}
.field{display:grid;gap:6px;min-width:0}
.field label{font-size:.9rem;font-weight:500}
.two{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.seg{display:flex;gap:8px;flex-wrap:wrap}
.hint{margin:0;font-size:.82rem;color:var(--muted)}
.err{margin:0;color:var(--danger);font-weight:500}
.prev{width:120px;aspect-ratio:4/3;object-fit:cover;border-radius:8px;border:1px solid var(--line)}
.row{display:flex;align-items:center;gap:12px;padding:10px;border:1px solid var(--line);border-radius:10px;min-width:0}
.row + .row{margin-top:8px}
.thumb{flex:none;width:52px;height:40px;border-radius:6px;overflow:hidden;background:var(--cart-deep)}
.thumb img{width:100%;height:100%;object-fit:cover;display:block}
.rinfo{flex:1;min-width:0;display:grid}
.rinfo b{overflow-wrap:anywhere}
.rinfo span{font-size:.8rem;color:var(--muted)}
.muted{margin:0;color:var(--muted)}
.sheet-foot{position:sticky;bottom:0;display:grid;gap:10px;margin-top:22px;padding:14px 0 16px;background:var(--surface);border-top:1px solid var(--line)}
.meter{height:8px;border-radius:99px;background:var(--cart);overflow:hidden}
.meter i{display:block;height:100%;width:0;background:var(--accent2)}
.meter.warn i{background:var(--danger)}
.foot-line{display:flex;justify-content:space-between;gap:12px;flex-wrap:wrap;font-size:.85rem;color:var(--muted)}
.status{margin:0;min-height:1.4em;font-size:.9rem}

@media (prefers-reduced-motion: reduce){
  .cart{animation:none;transition:none}
}
</style>
<div id="app" dir="rtl" lang="ar"></div>
<script type="application/json" id="site-data">{"site":{"name":"Dream games","tagline":"حمّل ألعابي وجرّبها"},"games":[]}</script>
<script id="app-js">
/* APP_MARK_v1 */
(function(){
'use strict';
var S='<'+'script', E='<'+'/script>';
var RESET=':root{color-scheme:light;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}body{margin:0;font:14px system-ui,sans-serif}img{max-width:100%}[hidden]{display:none!important}';
var FONTS='https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@400;500;600&family=Lalezar&family=Space+Mono:wght@400;700&display=swap';
var MAX_FILE=6*1024*1024, MAX_DOC=15*1024*1024;
var PLATFORMS={web:'ويب',android:'أندرويد',windows:'ويندوز',other:'أخرى'};

function $(s){return document.querySelector(s)}
function esc(s){return String(s==null?'':s).replace(/[&<>"']/g,function(c){return {'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]})}
function hash(s){var h=2166136261;for(var i=0;i<s.length;i++){h^=s.charCodeAt(i);h=Math.imul(h,16777619)}return h>>>0}
function artBg(seed){var h=hash(seed),a=h%360,b=(a+40+((h>>8)%60))%360;return 'background:linear-gradient(135deg,hsl('+a+' 62% 34%),hsl('+b+' 70% 24%))'}
function first(t){return Array.from(String(t||'').trim())[0]||'؟'}
function fmtSize(n){if(!n)return '';if(n<1048576)return Math.max(1,Math.round(n/1024))+' KB';return (n/1048576).toFixed(n<10485760?1:0)+' MB'}
var dateFmt=null;
try{dateFmt=new Intl.DateTimeFormat('ar-u-nu-latn',{year:'numeric',month:'short',day:'numeric'})}catch(e){}
function fmtDate(iso){try{return dateFmt?dateFmt.format(new Date(iso)):''}catch(e){return ''}}

var state=null;
try{state=JSON.parse($('#site-data').textContent)}catch(e){}
if(!state||!Array.isArray(state.games)){state={site:{name:'Dream games',tagline:'حمّل ألعابي وجرّبها'},games:[]}}
if(!state.site){state.site={name:'Dream games',tagline:'حمّل ألعابي وجرّبها'}}
var payloads={};
document.querySelectorAll('script.payload').forEach(function(el){payloads[el.getAttribute('data-id')]=el.textContent.trim()});

var SAMPLES=[
  {id:'s1',title:'سباق الصحراء',desc:'سباق سريع بين الكثبان الرملية. اجمع الوقود وتجنّب الصخور قبل أن ينتهي الوقت.',version:'1.0',platform:'web',kind:'file',fileSize:820000,sample:true},
  {id:'s2',title:'حارس البرج',desc:'دافع عن البرج من موجات الأعداء وطوّر أسلحتك بين كل جولة.',version:'0.8',platform:'android',kind:'file',fileSize:14200000,sample:true},
  {id:'s3',title:'قفزة النجوم',desc:'لعبة منصات هادئة تقفز فيها بين الكواكب وتجمع النجوم.',version:'1.2',platform:'windows',kind:'file',fileSize:38000000,sample:true}
];

var LOGO='<img class="logo" src="data:image/webp;base64,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
