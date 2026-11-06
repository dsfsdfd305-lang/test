<!DOCTYPE html>
<html lang="az">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Tutorize Free – pulsuz test generatoru</title>
<script src="https://cdn.tailwindcss.com/3.4.17"></script>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@600;800&family=Manrope:wght@400;600;700&display=swap" rel="stylesheet">
<script>tailwind.config={darkMode:'class'}</script>
<style>
:root{box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);--bg:#f3f1ff;--card:#fff;--ink:#16173d;--mut:#5d6090;--line:#e1ddfa;--ac:#6d4aff;--ac2:#00b8a9;--ac3:#ffb020;--ac4:#ff4d6d}
:root[data-theme="dark"]{--bg:#0d0e2b;--card:#171946;--ink:#f0f0ff;--mut:#a9acdf;--line:#2c2f6e}
html{scroll-padding-top:90px;scroll-behavior:smooth}
body{margin:0;color:var(--ink);font-family:'Manrope',system-ui,sans-serif;background:radial-gradient(900px 500px at 10% -5%,rgba(109,74,255,.18),transparent),radial-gradient(800px 500px at 100% 10%,rgba(0,184,169,.16),transparent),var(--bg);transition:background .3s}
h1,h2,h3,.dsp{font-family:'Bricolage Grotesque','Manrope',sans-serif}
.card{background:var(--card);border:1px solid var(--line);border-radius:22px;box-shadow:0 8px 30px rgba(60,40,160,.07)}
.mut{color:var(--mut)}
nav.top{position:sticky;top:env(safe-area-inset-top,0px);z-index:40;margin:10px auto 0;max-width:72rem;border-radius:20px;background:color-mix(in srgb,var(--card) 80%,transparent);backdrop-filter:blur(14px);border:1px solid var(--line)}
nav a{font-weight:700;padding:.45rem .8rem;border-radius:10px;color:var(--mut);text-decoration:none;transition:.2s}
nav a:hover{background:rgba(109,74,255,.12);color:var(--ac)}
select,input.f{background:var(--card);color:var(--ink);border:1.5px solid var(--line);border-radius:14px;padding:.75rem .9rem;width:100%;outline:none;transition:.2s;font:inherit}
select:focus,input.f:focus,.btn:focus-visible,.tab:focus-visible{border-color:var(--ac);box-shadow:0 0 0 3px rgba(109,74,255,.28)}
input[type=checkbox]{accent-color:var(--ac);width:16px;height:16px}
.btn{position:relative;overflow:hidden;border-radius:14px;padding:.7rem 1.15rem;font-weight:800;color:#fff;background:linear-gradient(135deg,#6d4aff,#8b6bff);cursor:pointer;border:0;transition:transform .15s,box-shadow .2s;box-shadow:0 6px 16px rgba(109,74,255,.3);font:inherit}
.btn:hover{transform:translateY(-2px)}.btn:active{transform:scale(.96)}
.btn.teal{background:linear-gradient(135deg,#00b8a9,#27d3c3)}.btn.amber{background:linear-gradient(135deg,#ffb020,#ffcf5a);color:#2b1b00}.btn.green{background:linear-gradient(135deg,#16a34a,#34d27b)}.btn.red{background:linear-gradient(135deg,#e11d48,#fb7185)}.btn.ghost{background:transparent;color:var(--ink);border:1.5px solid var(--line);box-shadow:none}
.tab{flex:1;padding:.55rem .6rem;border-radius:14px;font-weight:800;color:var(--mut);background:transparent;border:0;cursor:pointer;font:inherit;font-weight:800}
.tab.on{background:var(--card);color:var(--ac);box-shadow:0 4px 12px rgba(60,40,160,.12)}
.rip{position:absolute;border-radius:50%;background:rgba(255,255,255,.55);transform:scale(0);animation:rip .6s ease-out;pointer-events:none}
@keyframes rip{to{transform:scale(4);opacity:0}}
.fade{opacity:0;transform:translateY(10px);animation:fi .5s ease forwards}
@keyframes fi{to{opacity:1;transform:none}}
.hero{background:radial-gradient(circle at 15% 10%,#8b6bff,transparent 50%),radial-gradient(circle at 90% 90%,#00b8a9,transparent 45%),linear-gradient(135deg,#2b1c9a,#5b3df0);color:#fff;border-radius:32px;position:relative;overflow:hidden}
.blob{position:absolute;border-radius:50%;opacity:.5;animation:fl 7s ease-in-out infinite}
@keyframes fl{50%{transform:translateY(-22px) rotate(8deg)}}
.mini{position:absolute;background:rgba(255,255,255,.15);border:1px solid rgba(255,255,255,.3);backdrop-filter:blur(8px);border-radius:16px;padding:.6rem .9rem;font-weight:800;animation:fl 6s ease-in-out infinite}
.tile{border:0;border-radius:24px;padding:1.1rem;color:#fff;text-align:left;cursor:pointer;position:relative;overflow:hidden;transition:transform .25s,box-shadow .25s;box-shadow:0 10px 24px rgba(0,0,0,.14);min-height:120px}
.tile:hover{transform:translateY(-6px) rotate(-1deg);box-shadow:0 16px 30px rgba(0,0,0,.22)}
.tile .em{font-size:2.4rem;display:block;transition:transform .3s}.tile:hover .em{transform:scale(1.2) rotate(8deg)}
.tile.on{outline:4px solid var(--ink);outline-offset:3px}
.tile::after{content:"";position:absolute;right:-20px;bottom:-30px;width:90px;height:90px;border-radius:50%;background:rgba(255,255,255,.18)}
.q{position:relative;overflow:hidden;transition:transform .3s,border-color .3s}
.q::after{content:"";position:absolute;inset:0;pointer-events:none;opacity:0;background:repeating-linear-gradient(135deg,rgba(109,74,255,.11) 0 6px,transparent 6px 14px);transition:opacity .35s}
.q:hover::after{opacity:1;animation:hatch 1.2s linear infinite}.q:hover{transform:translateY(-3px);border-color:var(--ac)}
@keyframes hatch{to{background-position:40px 40px}}
.opt{display:flex;gap:.6rem;align-items:center;padding:.5rem .7rem;border-radius:12px;border:1.5px solid var(--line);margin-top:.4rem;cursor:pointer;transition:.2s}
.opt:hover{background:rgba(109,74,255,.09)}
.opt.ok{background:rgba(22,163,74,.16);border-color:#16a34a}
.opt.bad{background:rgba(225,29,72,.14);border-color:#e11d48}
.opt.sel{border-color:var(--ac);background:rgba(109,74,255,.14)}
.chip{display:inline-block;padding:.15rem .65rem;border-radius:99px;font-size:.75rem;font-weight:800}
.bar{height:14px;border-radius:99px;transition:width 1s cubic-bezier(.2,.8,.2,1);width:0}
#toasts{position:fixed;right:1rem;bottom:calc(1rem + env(safe-area-inset-bottom,0px));z-index:70;display:flex;flex-direction:column;gap:.5rem}
.toast{background:#16a34a;color:#fff;padding:.8rem 1.1rem;border-radius:14px;font-weight:800;box-shadow:0 10px 30px rgba(0,0,0,.25);animation:tin .4s ease,tout .4s ease 2.8s forwards}
@keyframes tin{from{transform:translateX(120%);opacity:0}}@keyframes tout{to{transform:translateX(120%);opacity:0}}
#modal{position:fixed;inset:0;background:rgba(10,10,40,.65);z-index:60;display:none;align-items:flex-start;justify-content:center;padding:1rem;overflow:auto}
#modal.on{display:flex}
#modal #mbox{width:100%;max-width:42rem}
@media(max-width:640px){
 html,body{overflow-x:hidden}
 body{font-size:15px}
 nav.top{margin:6px 8px 0;border-radius:16px;padding:.5rem .6rem;gap:.4rem}
 nav.top .dsp{font-size:1.1rem}
 nav.top .btn{padding:.5rem .6rem;font-size:13px;min-height:40px;box-shadow:none}
 .btn{min-height:44px;padding:.7rem .9rem}
 .card{border-radius:18px}
 .hero{border-radius:24px}
 .mini{display:none}
 select,input.f{font-size:16px;min-height:46px;padding:.7rem .8rem}
 .tab{min-height:42px;font-size:14px}
 .tile{min-height:104px;padding:.9rem}
 .tile .em{font-size:2rem}
 .tile:hover,.q:hover,.btn:hover{transform:none}
 .opt{padding:.7rem .8rem;font-size:15px}
 .opt input{width:18px;height:18px;flex-shrink:0}
 .chip{white-space:normal;text-align:center}
 table{font-size:13px}
 #toasts{left:1rem;right:1rem}
 .toast{text-align:center}
 #modal{padding:0}
 #modal #mbox{max-width:none;width:100%;min-height:100vh;margin:0;border-radius:0;border:0;box-shadow:none;padding:1rem 1rem 2rem}
 #modal #mbox .btn.ghost{flex-shrink:0}
 #authbox .card{margin-top:1rem}
 #v-student .flex,#v-teacher .flex{gap:.5rem}
}
@media(prefers-reduced-motion:reduce){*{animation-duration:.01ms!important;transition-duration:.01ms!important}}
@media print{body *{visibility:hidden}#cards,#cards *{visibility:visible}#cards{position:absolute;left:0;top:0;width:100%}.q::after{display:none}}
</style>
</head>
<body>
<nav class="top px-4 py-2 flex items-center justify-between gap-2 flex-wrap">
  <a href="#" data-go="h" class="dsp text-xl font-extrabold flex items-center gap-2" style="text-decoration:none;color:var(--ink)"><span class="inline-grid place-items-center w-9 h-9 rounded-xl text-white" style="background:linear-gradient(135deg,#6d4aff,#00b8a9)">T</span><span>Tutorize</span><span class="chip" style="background:var(--ac2);color:#fff">Free</span></a>
  <div class="flex gap-2 items-center flex-wrap"><button class="btn ghost !px-3 !py-2" data-go="t">👩‍🏫 Müəllim</button><button class="btn ghost !px-3 !py-2" data-go="s">🎒 Şagird</button><button id="lo" class="btn amber !px-3 !py-2 hidden">Çıxış</button><button id="snd" class="btn ghost !px-3 !py-2" aria-label="Səs">🔊</button><button id="theme" class="btn ghost !px-3 !py-2" aria-label="Rejim">🌙</button></div>
</nav>

<main class="max-w-6xl mx-auto px-4 pb-16">

<div id="v-home">
<section class="hero mt-5 p-7 md:p-12 min-h-[300px]">
  <div class="blob w-44 h-44 bg-amber-300 -right-10 -top-10"></div>
  <div class="blob w-24 h-24 bg-rose-400 right-44 bottom-6" style="animation-delay:-2s"></div>
  <div class="mini hidden md:block right-20 top-24">2x + 6 = 14 → x = 4</div>
  <div class="relative max-w-xl">
    <span class="chip" style="background:rgba(255,255,255,.2)">100% pulsuz · abunəlik yoxdur</span>
    <h1 class="text-4xl md:text-6xl font-extrabold leading-tight mt-3">Test və summativ iki dəqiqəyə hazırdır</h1>
    <p class="mt-4 text-lg opacity-90">Müəllim özəl kodla qeydiyyatdan keçir, testi yaradır və nəticələri izləyir. Şagird isə hesab yaradır, testi həll edir və səhvlərinə baxır.</p>
  </div>
</section>
<div class="grid md:grid-cols-2 gap-5 mt-6">
  <div class="card p-6"><div class="text-4xl">👩‍🏫</div><h2 class="text-2xl font-extrabold mt-2">Müəllim paneli</h2><p class="mut mt-1">Özəl giriş kodu ilə qeydiyyatdan keçin, test yaradın və sinif nəticələrini görün.</p><button class="btn mt-4" data-go="t">Müəllim girişi</button></div>
  <div class="card p-6"><div class="text-4xl">🎒</div><h2 class="text-2xl font-extrabold mt-2">Şagird paneli</h2><p class="mut mt-1">Hesab yaradın, müəllimin verdiyi test kodunu yazın və cavablarınızın təhlilinə baxın.</p><button class="btn teal mt-4" data-go="s">Şagird girişi</button></div>
</div>
</div>

<section id="v-auth" class="hidden"><div id="authbox"></div></section>

<div id="v-teacher" class="hidden">
  <div class="card p-4 mt-5 flex flex-wrap items-center justify-between gap-3">
    <div><b class="dsp text-lg" id="tw"></b><div class="mut text-sm">Müəllim paneli · yalnız siz görürsünüz</div></div>
    <div class="flex flex-wrap items-center gap-2"><span class="chip" style="background:rgba(109,74,255,.15);color:var(--ac)">Müəllim kodunuz: <b id="tcode"></b></span><button class="btn ghost !px-3 !py-2" id="tcp">Kodu kopyala</button></div>
  </div>
<section id="fenler" class="mt-10">
  <h2 class="text-3xl font-extrabold">Fənni seçin</h2>
  <p class="mut mt-1">Bir fənnə toxunun, qalanını biz hazırlayaq.</p>
  <div id="tiles" class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-4 mt-5"></div>
</section>

<section id="params" class="card p-6 mt-8">
  <h2 class="text-2xl font-extrabold">Parametrlər</h2>
  <div class="grid md:grid-cols-4 gap-4 mt-4">
    <label class="text-sm font-bold">Sinif<select id="grade" class="mt-1"></select></label>
    <label class="text-sm font-bold">Fənn<select id="subj" class="mt-1"><option value="">Fənni seçin</option></select></label>
    <label class="text-sm font-bold">Mövzu<select id="topic" class="mt-1" disabled><option value="">Əvvəl fənni seçin</option></select></label>
    <label class="text-sm font-bold">Sual sayı<select id="cnt" class="mt-1"><option>4</option><option>6</option><option selected>8</option><option>10</option><option>12</option></select></label>
  </div>
  <div id="ready" class="hidden mt-5 flex flex-wrap items-center gap-3"><span class="chip" style="background:rgba(109,74,255,.15);color:var(--ac)" id="sel"></span><button class="btn" id="gen">Test yarat</button></div>
</section>

<section id="out" class="hidden mt-8">
  <div class="card p-6"><h2 class="text-2xl font-extrabold">Bal qrupları</h2><p class="mut mt-1">Suallar çətinliyə görə avtomatik bölünür.</p><div id="groups" class="grid sm:grid-cols-4 gap-3 mt-4"></div></div>
  <div class="flex flex-wrap items-center justify-between gap-3 mt-8">
    <h2 class="text-2xl font-extrabold">Test kartları</h2>
    <div class="flex flex-wrap gap-2"><button class="btn teal" id="key">Cavab açarı</button><button class="btn" id="pdf">PDF yüklə</button><button class="btn green" id="wa">WhatsApp-da göndər</button><button class="btn amber" id="stu">Şagird rejimi</button><button class="btn red" id="delt">Testi sil</button></div>
  </div>
  <div id="cards" class="grid md:grid-cols-2 gap-4 mt-4"></div>
  <div class="card p-6 mt-8">
    <h2 class="text-2xl font-extrabold">Şagirdlərə göndəriləcək link</h2>
    <p class="mut text-sm mt-1">Şagirdlər hesab yaradıb bu linki açsalar, test birbaşa açılacaq.</p>
    <div class="flex flex-wrap gap-2 items-center mt-3"><input id="link" readonly class="f max-w-xl"><button class="btn ghost" id="copy">Kopyala</button></div>
    <h2 class="text-2xl font-extrabold mt-8">Sinfin nəticələri</h2>
    <p class="mut mt-1" id="note"></p>
    <div class="flex flex-wrap gap-3 mt-4" id="stats"></div>
    <h3 class="font-bold mt-6">Sinif üzrə nəticə</h3><div id="cls" class="mt-2 space-y-3"></div>
    <h3 class="font-bold mt-6">Mövzu üzrə nəticə (%)</h3><div id="chart" class="mt-2 space-y-3"></div>
    <h3 class="font-bold mt-6">Şagirdlər</h3><div id="tbl" class="overflow-x-auto mt-2"></div>
    <h3 class="font-bold mt-6">Nəticə kodu əlavə et</h3>
    <p class="mut text-sm">Şagird testi başqa cihazda həll edibsə, onun göndərdiyi nəticə kodunu bura yapışdırın.</p>
    <div class="flex flex-wrap gap-2 mt-2"><input id="rcode" class="f max-w-xl" placeholder="r.eyJ..."><button class="btn teal" id="radd">Əlavə et</button></div>
  </div>
</section>
</div>

<div id="v-student" class="hidden">
  <div class="card p-6 mt-8 flex flex-wrap justify-between gap-4 items-center">
    <div><h2 class="text-2xl font-extrabold" id="sh"></h2><p class="mut" id="si"></p></div>
    <div class="flex flex-wrap gap-2" id="sstat"></div>
  </div>
  <div class="card p-6 mt-6">
    <h3 class="font-bold">Test kodu və ya linki</h3>
    <p class="mut text-sm mt-1">Müəllim sizə kod və ya link göndərib. Kodu yazıb testi başlayın.</p>
    <div class="flex flex-wrap gap-2 mt-3"><input id="code" class="f max-w-md" placeholder="Məsələn: t-7-0-1-6-AB12CD"><button class="btn teal" id="go">Testi başla</button></div>
    <p id="cerr" class="text-sm mt-2 font-bold" style="color:var(--ac4)"></p>
  </div>
  <div class="card p-6 mt-6"><h2 class="text-xl font-extrabold">Mənim nəticələrim</h2><p class="mut text-sm mt-1">Hər testin altında “Bax” düyməsi ilə səhv və düz cavablarınızı görə bilərsiniz.</p><div id="hist" class="mt-3 space-y-2"></div></div>
</div>

</main>

<div id="modal"><div class="card p-6 my-6" id="mbox"></div></div>
<div id="toasts"></div>

<script>
const $=s=>document.querySelector(s);
const S=(e,c,t,q)=>({e,c,t,q:q.map(x=>[x[0],x[1],x[2].split('|'),x[3],x[4]])});
const TEACHER_CODES=["MUE-4K7P-2X9","MUE-9TQ2-HM6","MUE-3RZ8-LW1","MUE-6NB5-QD4","MUE-8JF1-VS7","MUE-2GC9-TK3","MUE-5WH6-PR8","MUE-1XD7-YN2"];
const DB={
"Riyaziyyat":S("➗",["#6d4aff","#9b7bff"],["Kəsrlər","Tənliklər","Həndəsə"],[
[0,"3/4 + 1/4 = ?","1|4/8|3/8|1/2",0,"Məxrəc eynidir: (3+1)/4 = 1."],
[0,"2/3 kəsrinin 12-si neçədir?","6|8|9|10",1,"12 · 2/3 = 8."],
[0,"1/2 + 1/3 = ?","2/5|5/6|1/5|2/6",1,"3/6 + 2/6 = 5/6."],
[0,"3/5 kəsrinin 20-si neçədir?","8|10|12|15",2,"20 · 3/5 = 12."],
[1,"2x + 6 = 14 olarsa, x = ?","3|4|5|10",1,"2x = 8, x = 4."],
[1,"3x − 5 = 16 olarsa, x = ?","5|6|7|8",2,"3x = 21, x = 7."],
[1,"5x = 35 olarsa, x = ?","5|6|7|8",2,"x = 35 : 5 = 7."],
[1,"x/4 = 3 olarsa, x = ?","7|10|12|14",2,"x = 3 · 4 = 12."],
[2,"Tərəfləri 5 və 8 sm olan düzbucaqlının sahəsi?","13 sm²|26 sm²|40 sm²|45 sm²",2,"S = 5 · 8 = 40."],
[2,"Üçbucağın daxili bucaqları cəmi?","90°|180°|270°|360°",1,"Cəm 180°-dir."],
[2,"Kvadratın tərəfi 6 sm-dirsə, perimetri?","12 sm|24 sm|36 sm|18 sm",1,"P = 4 · 6 = 24 sm."],
[2,"Dördbucaqlının daxili bucaqları cəmi?","180°|270°|360°|400°",2,"Cəm 360°-dir."]]),
"Azərbaycan dili":S("📖",["#ff4d6d","#ff8fa3"],["Fonetika","Leksika","Qrammatika"],[
[0,"“Kitab” sözündə neçə sait var?","0|1|2|3",2,"i və a saitdir."],
[0,"Hansı səs saitdir?","b|k|a|r",2,"a sait səsdir."],
[0,"“Məktəb” sözündə neçə hece var?","1|2|3|4",1,"Mək-təb: 2 hece."],
[0,"Hansı səs samitdir?","a|o|e|s",3,"s samit səsdir."],
[1,"“Yaxşı” sözünün antonimi?","Gözəl|Pis|Böyük|Tez",1,"Əks mənalı söz: pis."],
[1,"“Cəsur” sözünün sinonimi?","Qorxaq|İgid|Tənbəl|Yavaş",1,"Yaxın mənalı söz: igid."],
[1,"“Böyük” sözünün antonimi?","Uca|Kiçik|Geniş|Ağır",1,"Əks mənalı söz: kiçik."],
[1,"“Sevinc” sözünün sinonimi?","Kədər|Qəm|Şadlıq|Qorxu",2,"Yaxın mənalı söz: şadlıq."],
[2,"İsim hansı suallara cavab verir?","kim? nə?|necə?|neçə?|nə edir?",0,"İsim “kim? nə?” sualına cavab verir."],
[2,"Feil hansı suala cavab verir?","kim?|necə?|nə edir?|harada?",2,"Feil işi bildirir."],
[2,"Sifət hansı suallara cavab verir?","kim?|hansı?|nə edir?|harada?",1,"Sifət “hansı?” sualına cavab verir."],
[2,"Zərf hansı suala cavab verir?","necə?|kim?|nə?|hara?",0,"Zərf “necə?” sualına cavab verir."]]),
"Fizika":S("⚡",["#0ea5e9","#4cc9f0"],["Hərəkət","Qüvvə","İş və enerji"],[
[0,"Sürət düsturu?","v = s/t|v = s·t|v = t/s|v = s+t",0,"Sürət = yol / zaman."],
[0,"2 saata 120 km gedənin sürəti?","40 km/s|60 km/s|80 km/s|240 km/s",1,"120 : 2 = 60."],
[0,"Yolun düsturu?","s = v·t|s = v/t|s = t/v|s = v+t",0,"Yol = sürət · zaman."],
[0,"40 km/s sürətlə 3 saat gedən yol?","80 km|120 km|13 km|160 km",1,"s = 40 · 3 = 120 km."],
[1,"Qüvvənin vahidi?","Coul|Nyuton|Vatt|Paskal",1,"Qüvvə Nyutonla ölçülür."],
[1,"m = 2 kq, a = 3 m/s² olarsa F = ?","5 N|6 N|1,5 N|9 N",1,"F = m·a = 6 N."],
[1,"Sürtünmə qüvvəsi hansı istiqamətdə yönəlir?","Hərəkətə qarşı|Hərəkətlə eyni|Yanlara|Yuxarıya",0,"Sürtünmə hərəkətə əks istiqamətdədir."],
[1,"m = 5 kq üçün ağırlıq qüvvəsi (g = 10 m/s²)?","5 N|15 N|50 N|500 N",2,"F = m·g = 50 N."],
[2,"İşin vahidi?","Coul|Nyuton|Vatt|Metr",0,"İş Coulla ölçülür."],
[2,"Gücün vahidi?","Vatt|Coul|Nyuton|Kq",0,"Güc Vattla ölçülür."],
[2,"Enerjinin vahidi?","Coul|Nyuton|Vatt|Paskal",0,"Enerji Coulla ölçülür."],
[2,"Kinetik enerji düsturu?","mv²/2|mv|mgh|ma",0,"Ek = mv²/2."]]),
"Biologiya":S("🧬",["#16a34a","#4ade80"],["Hüceyrə","Bitkilər","İnsan"],[
[0,"Hüceyrənin enerji stansiyası?","Nüvə|Mitoxondri|Ribosom|Vakuol",1,"Mitoxondriyada tənəffüs gedir."],
[0,"Yalnız bitki hüceyrəsində olan quruluş?","Nüvə|Hüceyrə divarı|Sitoplazma|Membran",1,"Hüceyrə divarı bitkiyə xasdır."],
[0,"Hüceyrənin idarəedici mərkəzi?","Nüvə|Membran|Vakuol|Ribosom",0,"Nüvədə genetik məlumat var."],
[0,"Hüceyrə membranının əsas funksiyası?","Enerji istehsalı|Maddələrin keçməsinə nəzarət|Zülal sintezi|Fotosintez",1,"Membran maddələrin keçidini tənzimləyir."],
[1,"Fotosintez harada gedir?","Xloroplast|Mitoxondri|Nüvə|Lizosom",0,"Xloroplastda xlorofil işığı udur."],
[1,"Fotosintezdə bitki hansı qazı udur?","Oksigen|Azot|Karbon qazı|Hidrogen",2,"CO₂ və sudan qlükoza və O₂ əmələ gəlir."],
[1,"Suyu yuxarı daşıyan toxuma?","Floema|Ksilema|Stoma|Epidermis",1,"Ksilema suyu yuxarı daşıyır."],
[1,"Stomaların əsas vəzifəsi?","Qaz mübadiləsi|Qidalanma|Ayrılma|Böyümə",0,"Stomalar vasitəsilə CO₂ və O₂ mübadiləsi olur."],
[2,"İnsan ürəyi neçə kameradan ibarətdir?","2|3|4|5",2,"2 qulaqcıq, 2 mədəcik."],
[2,"Qanı bədənə hansı orqan vurur?","Ağciyər|Ürək|Qaraciyər|Böyrək",1,"Ürək nasos kimi işləyir."],
[2,"Qanın qırmızı rəngini hansı maddə verir?","Hemoqlobin|Leykosit|Plazma|Trombosit",0,"Hemoqlobin oksigeni daşıyır."],
[2,"Ağciyərlərdən qana hansı qaz keçir?","Azot|Oksigen|Helium|Hidrogen",1,"Oksigen qana keçir."]]),
"Kimya":S("⚗️",["#f97316","#fdba74"],["Maddə","Elementlər","Reaksiyalar"],[
[0,"Suyun formulu?","H₂O|CO₂|O₂|NaCl",0,"2 hidrogen + 1 oksigen."],
[0,"Hansı sadə maddədir?","Su|Oksigen|Duz|Şəkər",1,"O₂ yalnız oksigendən ibarətdir."],
[0,"Karbon qazının formulu?","CO|CO₂|C₂O|CH₄",1,"Bir karbon, iki oksigen."],
[0,"Metanın formulu?","CH₄|C₂H₆|NH₃|H₂S",0,"Metan CH₄-dür."],
[1,"Natriumun simvolu?","N|Na|Ni|S",1,"Natrium — Na."],
[1,"Hidrogenin sıra nömrəsi?","1|2|8|11",0,"Hidrogen 1-ci elementdir."],
[1,"Oksigenin simvolu?","O|Ox|Og|Os",0,"Oksigen — O."],
[1,"Karbonun sıra nömrəsi?","4|6|8|12",1,"Karbon 6-cı elementdir."],
[2,"Yanma üçün hansı qaz lazımdır?","Azot|Oksigen|Helium|Neon",1,"Yanma oksigenlə gedir."],
[2,"Turşu lakmusu hansı rəngə boyayır?","Qırmızı|Mavi|Yaşıl|Sarı",0,"Turşuda lakmus qırmızı olur."],
[2,"Sadə duz (NaCl) hansı elementlərdən ibarətdir?","Na və Cl|Na və O|K və Cl|Ca və Cl",0,"Natrium və xlor."],
[2,"Qələvidə lakmus hansı rəngə boyanır?","Qırmızı|Mavi|Sarı|Yaşıl",1,"Qələvidə lakmus mavi olur."]]),
"Tarix":S("🏛️",["#b45309","#f0b45c"],["Qədim dünya","Orta əsrlər","Azərbaycan"],[
[0,"Qədim Misir hökmdarları necə adlanırdı?","Sultan|Fironlar|İmperator|Xan",1,"Fironlar."],
[0,"Ehramlar nə üçün tikilirdi?","Qala|Qəbir|Bazar|Məktəb",1,"Fironların məqbərələridir."],
[0,"Piramidalar hansı ölkədə yerləşir?","Hindistan|Misir|Çin|Yunanıstan",1,"Misir."],
[0,"Qədim Yunanıstanın məşhur şəhər dövlətləri?","Afina və Sparta|Roma və Venesiya|Bağdad və Kair|Dehli və Pekin",0,"Afina və Sparta məşhur idi."],
[1,"Orta əsrdə torpaq sahibləri?","Feodal|Tacir|Kahin|Əsgər",0,"Feodallar torpağa sahib idi."],
[1,"İpək yolu nə ilə məşhur idi?","Ticarət|Dəniz döyüşü|Əkinçilik|Tikinti",0,"Şərqi Qərblə bağlayan ticarət yolu idi."],
[1,"Müqəddəs yürüşlər nə üçün təşkil olunurdu?","Müqəddəs torpaqlar|Ticarət yolu|Əkin sahələri|Dənizlərin tapılması",0,"Səlib yürüşləri Qüdsə yönəlmişdi."],
[1,"Orta əsrdə Bizans kilsəsinin mərkəzi?","Roma|Konstantinopol|Qahirə|Bağdad",1,"Konstantinopol Bizans kilsəsinin mərkəzi idi."],
[2,"ADR neçənci ildə yaranıb?","1828|1918|1991|1945",1,"28 may 1918."],
[2,"Azərbaycanın paytaxtı?","Gəncə|Bakı|Şəki|Sumqayıt",1,"Bakı."],
[2,"Azərbaycan bayrağında neçə rəng var?","2|3|4|5",1,"Göy, qırmızı və yaşıl: üç rəng."],
[2,"Novruz bayramı hansı ayda qeyd olunur?","Mart|Aprel|Yanvar|İyun",0,"Novruz martın 21-də qeyd olunur."]]),
"Coğrafiya":S("🌍",["#0d9488","#5eead4"],["Yer","İqlim","Azərbaycan"],[
[0,"Ən böyük okean?","Atlantik|Sakit|Hind|Şimal Buzlu",1,"Sakit okean."],
[0,"Yerin təbii peyki?","Mars|Ay|Venera|Yupiter",1,"Ay."],
[0,"Ən böyük materik?","Afrika|Avropa|Asiya|Amerika",2,"Asiya ən böyük materikdir."],
[0,"Yer kürəsinin ən hündür dağı?","Everest|Elbrus|Kilimancaro|Alp",0,"Everest dünyanın ən hündür dağıdır."],
[1,"Ekvator ətrafında iqlim?","Soyuq|İsti|Mülayim|Quru-soyuq",1,"Günəş şüaları dik düşür."],
[1,"Yağış nədən əmələ gəlir?","Buxarlanma və kondensasiya|Külək|Zəlzələ|Vulkan",0,"Su buxarlanıb buludlaşır."],
[1,"Qütblərdə iqlim necədir?","İsti|Çox soyuq|Mülayim|Tropik",1,"Qütblər çox soyuqdur."],
[1,"Dəniz suyu niyə şordur?","Duzların həll olması|Buzlaşma|Külək|Vulkan",0,"Çaylar dənizə duz daşıyır."],
[2,"Azərbaycanın əsas uzun çayı?","Kür|Samur|Qanıx|Qusar",0,"Kür."],
[2,"Xəzər dənizi Azərbaycanın hansı tərəfindədir?","Şimal|Şərq|Qərb|Cənub",1,"Şərq."],
[2,"Azərbaycanın ən yüksək dağı?","Bazardüzü|Şahdağ|Kəpəz|Təfəkçi",0,"Bazardüzü ölkənin ən yüksək zirvəsidir."],
[2,"Lənkəran hansı bölgədə yerləşir?","Qarabağ|Talış|Şirvan|Mil",1,"Lənkəran Talış bölgəsindədir."]]),
"İngilis dili":S("🔤",["#7c3aed","#c4b5fd"],["Qrammatika","Lüğət","Zamanlar"],[
[0,"She ___ a teacher.","am|is|are|be",1,"“She” ilə “is”."],
[0,"They ___ happy.","is|am|are|be",2,"“They” ilə “are”."],
[0,"We ___ students.","am|is|are|be",2,"“We” ilə “are”."],
[0,"It ___ a cat.","am|is|are|be",1,"“It” ilə “is”."],
[1,"“Apple” sözünün tərcüməsi?","Alma|Armud|Üzüm|Nar",0,"Apple — alma."],
[1,"“Book” sözünün tərcüməsi?","Qələm|Kitab|Dəftər|Çanta",1,"Book — kitab."],
[1,"“House” sözünün tərcüməsi?","Ev|Məktəb|Bağ|Maşın",0,"House — ev."],
[1,"“Water” sözünün tərcüməsi?","Od|Hava|Su|Torpaq",2,"Water — su."],
[2,"I ___ football yesterday.","play|plays|played|playing",2,"Keçmiş zaman: played."],
[2,"He ___ to school every day.","go|goes|going|gone",1,"3-cü şəxs: goes."],
[2,"She ___ TV now.","watches|watched|is watching|watch",2,"İndi baş verən: is watching."],
[2,"They ___ dinner tomorrow.","cook|will cook|cooked|cooking",1,"Gələcək zaman: will cook."]]),
"İnformatika":S("💻",["#2563eb","#7aa7ff"],["Kompüter","Alqoritm","İnternet"],[
[0,"Kompüterin “beyni”?","Monitor|Prosessor|Siçan|Printer",1,"Prosessor."],
[0,"Giriş qurğusu hansıdır?","Monitor|Klaviatura|Dinamik|Printer",1,"Klaviatura."],
[0,"Çıxış qurğusu hansıdır?","Klaviatura|Siçan|Monitor|Skaner",2,"Monitor məlumatı göstərir."],
[0,"Yaddaş qurğusu hansıdır?","RAM|Monitor|Siçan|Printer",0,"RAM müvəqqəti yaddaşdır."],
[1,"Alqoritm nədir?","Proqram dili|Addım-addım təlimat|Kompüter növü|Şəbəkə",1,"Həll addımları ardıcıllığı."],
[1,"Şərt yoxlayan əmr?","if|print|loop|end",0,"if şərtə görə qərar verir."],
[1,"Dövr (loop) nə üçündür?","Təkrarlama|Fayl silmək|Şəkil çəkmək|Səs yazmaq",0,"Dövr əmrləri təkrar icra edir."],
[1,"Dəyişən (variable) nədir?","Məlumat saxlayan ad|Kompüter növü|Şəbəkə|Printer",0,"Dəyişən məlumatı saxlayır."],
[2,"WWW nə deməkdir?","World Wide Web|Web Win Work|World Web Wire|We Want Web",0,"Qlobal veb."],
[2,"Brauzer nə üçündür?","Veb səhifə açmaq|Mətn çap etmək|Fayl silmək|Səs yazmaq",0,"İnternet səhifələrini göstərir."],
[2,"URL nəyi göstərir?","Veb ünvanı|Kompüterin sürəti|Fayl ölçüsü|Printer modeli",0,"URL — veb ünvanıdır."],
[2,"E-poçt nə üçündür?","Elektron məktub göndərmək|Şəkil çəkmək|Oyun oynamaq|Mətn çap etmək",0,"E-poçt elektron məktubdur."]])
};
const NM=Object.keys(DB),LV=[["Asan",1,"#16a34a"],["Orta",2,"#f59e0b"],["Çətin",3,"#e11d48"]];
const GR_LBL=['Çox zəif','Zəif','Orta','Yaxşı','Güclü'],GR_COL=['#e11d48','#e11d48','#f59e0b','#16a34a','#16a34a'];

let test=[],curCode='',showKey=false,AC,mute=false,cur='home',authRole='t',authMode='login',pend=null,pendNote='';
let test_=null;

function snd(k){if(mute)return;try{AC=AC||new(window.AudioContext||window.webkitAudioContext)();const P={tick:[[660,.05]],pop:[[520,.06],[780,.07]],ok:[[523,.1],[659,.1],[784,.2]],bad:[[330,.12],[247,.22]],gen:[[440,.08],[587,.08],[880,.16]]}[k];let t=AC.currentTime;P.forEach(([f,d])=>{const o=AC.createOscillator(),g=AC.createGain();o.frequency.value=f;g.gain.setValueAtTime(.12,t);g.gain.exponentialRampToValueAtTime(.001,t+d);o.connect(g);g.connect(AC.destination);o.start(t);o.stop(t+d);t+=d*.8})}catch(e){}}
const esc=x=>String(x).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const mem={},st={get(k,d){try{const v=localStorage.getItem(k);return v==null?(k in mem?mem[k]:d):JSON.parse(v)}catch(e){return k in mem?mem[k]:d}},set(k,v){try{if(v===null)localStorage.removeItem(k);else localStorage.setItem(k,JSON.stringify(v))}catch(e){mem[k]=v}}};
function toast(m){snd('ok');const d=document.createElement('div');d.className='toast';d.textContent='✔ '+m;$('#toasts').appendChild(d);setTimeout(()=>d.remove(),3300)}

/* ---------- hesablar və sessiya ---------- */
async function H(u,x){try{const h=await crypto.subtle.digest('SHA-256',new TextEncoder().encode('tz:'+u+':'+x));return[...new Uint8Array(h)].map(b=>b.toString(16).padStart(2,'0')).join('')}catch(e){return'p:'+btoa(unescape(encodeURIComponent(u+':'+x)))}}
const A=()=>st.get('tz_acc',[]);
const saveA=a=>st.set('tz_acc',a);
const used=()=>st.get('tz_used',{});
function rnd(n){const c='ABCDEFGHJKLMNPQRSTUVWXYZ23456789';return Array.from({length:n},()=>c[Math.floor(Math.random()*c.length)]).join('')}
function newTid(){let t;do{t=rnd(6)}while(A().some(a=>a.tid===t));return t}
function who(){const s=st.get('tz_ses',null);if(!s)return null;return A().find(x=>x.r===s.r&&x.u===s.u)||null}
let me=who();
function mine(){return me&&me.r==='s'?st.get('tz_r',[]).filter(r=>r.su===me.u):[]}
function strength(p){let s=0;if(p.length>=6)s++;if(p.length>=10&&/\d/.test(p)&&/[A-Za-zƏəÖöÜüĞğŞşÇçİı]/.test(p))s++;if(/[^A-Za-z0-9ƏəÖöÜüĞğŞşÇçİı]/.test(p))s++;if(p.length>=14)s++;return Math.min(s,4)}
function meter(p){const el=$('#fmeter');if(!el)return;if(!p){el.innerHTML='';return}const s=strength(p);el.innerHTML=`<div class="rounded-full" style="background:var(--line);height:8px"><div style="height:8px;width:${(s+1)*20}%;background:${GR_COL[s]};border-radius:99px;transition:.3s"></div></div><p class="text-xs mt-1" style="color:${GR_COL[s]}">Şifrənin gücü: ${GR_LBL[s]}</p>`}

/* ---------- naviqasiya ---------- */
function show(v,r,m){
 if(v==='teacher'&&!(me&&me.r==='t')){v='auth';r='t';m='login'}
 if(v==='student'&&!(me&&me.r==='s')){v='auth';r='s';m='login'}
 cur=v;
 if(v==='auth')renderAuth(r||authRole,m||'login');
 ['home','auth','teacher','student'].forEach(x=>$('#v-'+x).classList.toggle('hidden',x!==v));
 $('#lo').classList.toggle('hidden',!me);
 if(v==='teacher'){$('#tw').textContent='Salam, '+me.n;$('#tcode').textContent=me.tid;restoreT()}
 if(v==='student')sPanel();
 scrollTo(0,0)}
document.addEventListener('click',e=>{const g=e.target.closest('[data-go]');if(!g)return;e.preventDefault();const k=g.dataset.go;show(k==='t'?'teacher':k==='s'?'student':'home')});
$('#lo').onclick=()=>{st.set('tz_ses',null);me=null;test=[];curCode='';pend=null;toast('Çıxış edildi');show('home')};
$('#tcp').onclick=()=>{try{navigator.clipboard.writeText(me.tid)}catch(e){}toast('Müəllim kodu kopyalandı')};

/* ---------- giriş və qeydiyyat ---------- */
function fld(id,label,type,ac,val,ph){return `<label class="block mt-3 text-sm font-bold">${label}<input id="${id}" type="${type}" class="f mt-1" autocomplete="${ac}" value="${esc(val)}" placeholder="${esc(ph)}"></label>`}
function renderAuth(r,m){
 authRole=r;authMode=m;
 const T=r==='t',isL=m==='login';
 const gradeOpts=Array.from({length:11},(_,i)=>`<option value="${i+1}"${i==6?' selected':''}>${i+1}-ci sinif</option>`).join('');
 let f='';
 if(isL){
  f+=fld('fu','İstifadəçi adı','text','username',st.get('tz_lastu',''),'məs. ali_k');
  f+=fld('fp','Şifrə','password','current-password','','Şifrənizi yazın');
  f+=`<div class="flex flex-wrap justify-between gap-2 items-center mt-3 text-sm"><label class="flex items-center gap-2"><input type="checkbox" id="fshow"> Şifrəni göstər</label><label class="flex items-center gap-2"><input type="checkbox" id="frem" checked> Adımı yadda saxla</label></div>`;
 }else{
  if(T)f+=fld('fcode','Müəllim giriş kodu','text','off','','MUE-XXXX-XXX');
  f+=fld('fn','Ad və soyad','text','name','','Məs. Əli Həsənov');
  f+=fld('fu','İstifadəçi adı','text','username','','3–20 simvol, məs. ali_k');
  if(!T)f+=`<div class="grid grid-cols-2 gap-3 mt-3"><label class="text-sm font-bold">Sinif<select id="fg" class="mt-1">${gradeOpts}</select></label><label class="text-sm font-bold">Hərf (könüllü)<input id="fl" class="f mt-1" maxlength="1" placeholder="A"></label></div>`;
  f+=fld('fp','Şifrə','password','new-password','','ən azı 6 simvol');
  f+=`<div id="fmeter" class="mt-2"></div>`;
  f+=fld('fp2','Şifrəni təkrar yazın','password','new-password','','');
  f+=`<label class="flex items-center gap-2 mt-3 text-sm"><input type="checkbox" id="fshow"> Şifrəni göstər</label>`;
 }
 const hint=T?(isL?'Hesabınıza daxil olun.':'Müəllim giriş kodunuzu daxil edib hesab yaradın. Hər kod yalnız bir dəfə istifadə olunur.'):(isL?'İstifadəçi adı və şifrənizlə daxil olun. Sinif və ad yazmağa ehtiyac yoxdur.':'Qeydiyyatdan keçdikdən sonra istənilən test kodunu həll edə bilərsiniz.');
 const tabs=`<div class="flex gap-2 mt-4 p-1 rounded-2xl" style="background:var(--bg)"><button type="button" class="tab ${isL?'on':''}" data-m="login">Daxil ol</button><button type="button" class="tab ${!isL?'on':''}" data-m="signup">Qeydiyyat</button></div>`;
 const note=pendNote?`<p class="text-sm mt-3 p-3 rounded-xl" style="background:rgba(0,184,169,.14)">${pendNote}</p>`:'';
 $('#authbox').innerHTML=`<div class="card p-6 max-w-md mx-auto mt-8"><div class="text-4xl">${T?'👩‍🏫':'🎒'}</div><h2 class="text-2xl font-extrabold mt-2">${T?'Müəllim':'Şagird'} ${isL?'girişi':'qeydiyyatı'}</h2><p class="mut text-sm mt-1">${hint}</p>${note}${tabs}<form id="aform" class="mt-2">${f}<p id="aerr" class="text-sm mt-3 font-bold" style="color:var(--ac4)"></p><button class="btn ${T?'':'teal'} w-full mt-4" type="submit">${isL?'Daxil ol':'Hesab yarat'}</button></form></div>`;
 document.querySelectorAll('#authbox .tab').forEach(b=>b.onclick=()=>renderAuth(r,b.dataset.m));
 $('#aform').onsubmit=authSubmit;
 $('#fshow').onchange=e=>{['#fp','#fp2'].forEach(s=>{const x=$(s);if(x)x.type=e.target.checked?'text':'password'})};
 if(!isL)$('#fp').oninput=e=>meter(e.target.value);
 const first=$(isL?'#fu':(T?'#fcode':'#fn'));if(first&&!first.value)first.focus();
}
function loginAs(a){
 st.set('tz_ses',{r:a.r,u:a.u});me=a;test=[];curCode='';
 if(a.r==='s'&&pend){const c=pend;pend=null;pendNote='';toast('Xoş gəldiniz, '+a.n);show('student');$('#code').value=c;startCode(c);return}
 pendNote='';toast('Xoş gəldiniz, '+a.n);
 show(a.r==='t'?'teacher':'student')}
async function authSubmit(e){
 e.preventDefault();
 const err=$('#aerr');err.textContent='';
 const u=($('#fu').value||'').trim().toLowerCase(),p=$('#fp').value||'';
 if(authMode==='login'){
  if(!u||!p){snd('bad');err.textContent='İstifadəçi adı və şifrəni yazın.';return}
  const a=A().find(x=>x.r===authRole&&x.u===u);
  if(!a){snd('bad');err.textContent='Bu adda hesab tapılmadı. Qeydiyyatdan keçin.';return}
  if(a.h!==await H(u,p)){snd('bad');err.textContent='Şifrə səhvdir.';return}
  st.set('tz_lastu',$('#frem').checked?u:'');
  loginAs(a);return;
 }
 const name=($('#fn').value||'').trim(),p2=$('#fp2').value||'';
 if(name.length<3){snd('bad');err.textContent='Ad və soyadı tam yazın.';return}
 if(!/^[\p{L}\d_.]{3,20}$/u.test(u)){snd('bad');err.textContent='İstifadəçi adı 3–20 simvol olmalıdır: hərf, rəqəm, _ və ya nöqtə.';return}
 if(p.length<6){snd('bad');err.textContent='Şifrə ən azı 6 simvol olmalıdır.';return}
 if(p!==p2){snd('bad');err.textContent='Şifrələr eyni deyil.';return}
 if(A().some(x=>x.u===u)){snd('bad');err.textContent='Bu istifadəçi adı artıq tutulub. Başqa ad seçin.';return}
 const h=await H(u,p);
 if(authRole==='t'){
  const code=($('#fcode').value||'').trim().toUpperCase();
  if(!TEACHER_CODES.includes(code)){snd('bad');err.textContent='Müəllim giriş kodu yanlışdır.';return}
  if(used()[code]){snd('bad');err.textContent='Bu kod artıq istifadə olunub.';return}
  const acc={r:'t',u,n:name,h,tid:newTid(),code,ts:Date.now()};
  saveA([...A(),acc]);
  const us=used();us[code]=u;st.set('tz_used',us);
  loginAs(acc);
 }else{
  const g=$('#fg').value,l=($('#fl').value||'').trim().toUpperCase().slice(0,1);
  const acc={r:'s',u,n:name,h,g,cl:g+l,ts:Date.now()};
  saveA([...A(),acc]);
  loginAs(acc);
 }
}

/* ---------- müəllim paneli ---------- */
const tkey=()=>'tz_last:'+me.u;
function restoreT(){
 if(!me||me.r!=='t')return;
 if(test.length&&curCode.endsWith('-'+me.tid))return;
 const z=st.get(tkey(),null),p=z&&parse(z.c);
 if(p){test=mk(p.sn,p.ti,p.n);curCode=p.code;render()}
 else{test=[];curCode='';$('#out').classList.add('hidden')}
}
function pick(n){$('#subj').value=n;const t=$('#topic');t.disabled=false;t.innerHTML=DB[n].t.map(x=>`<option>${x}</option>`).join('');document.querySelectorAll('.tile').forEach(b=>b.classList.toggle('on',b.dataset.n===n));chk()}
function chk(){const ok=$('#subj').value&&$('#topic').value;$('#ready').classList.toggle('hidden',!ok);if(ok)$('#sel').textContent=`${$('#grade').value}-ci sinif · ${$('#subj').value} · ${$('#topic').value}`}
function mk(sn,ti,n){const s=DB[sn],pool=[...s.q.filter(q=>q[0]===ti),...s.q.filter(q=>q[0]!==ti)].slice(0,n);return pool.map((q,i)=>({t:s.t[q[0]],q:q[1],o:q[2],a:q[3],e:q[4],lv:i<Math.ceil(n*.4)?0:i<Math.ceil(n*.8)?1:2}))}
function build(){const sn=$('#subj').value;test=mk(sn,Math.max(0,DB[sn].t.indexOf($('#topic').value)),+$('#cnt').value)}
const code=()=>`t-${$('#grade').value}-${NM.indexOf($('#subj').value)}-${DB[$('#subj').value].t.indexOf($('#topic').value)}-${$('#cnt').value}-${me.tid}`;
function parse(c){
 const m=/^t-(\d+)-(\d+)-(\d+)-(\d+)-([A-Za-z0-9]{6})$/i.exec((c||'').trim());
 if(!m)return null;
 const g=+m[1],si=+m[2],ti=+m[3],n=+m[4],sn=NM[si];
 if(!sn||!DB[sn].t[ti]||![4,6,8,10,12].includes(n)||g<1||g>11)return null;
 const tid=m[5].toUpperCase();
 return{code:`t-${g}-${si}-${ti}-${n}-${tid}`,g:String(g),sn,ti,n,tid}}
const enc=r=>'r.'+btoa(unescape(encodeURIComponent(JSON.stringify({c:r.c,cl:r.cl,n:r.n,a:r.a,s:r.s}))));

function render(){
 $('#out').classList.remove('hidden');
 const tot=test.reduce((a,q)=>a+LV[q.lv][1],0);
 $('#groups').innerHTML=LV.map((l,i)=>{const c=test.filter(q=>q.lv===i).length;return `<div class="card p-4 fade" style="border-left:6px solid ${l[2]}"><div class="mut text-sm">${l[0]}</div><div class="dsp text-2xl font-extrabold">${c} sual</div><div class="text-sm">hər biri ${l[1]} bal = ${c*l[1]} bal</div></div>`}).join('')+`<div class="card p-4 fade" style="background:var(--ac);color:#fff"><div class="text-sm opacity-80">Cəmi</div><div class="dsp text-2xl font-extrabold">${tot} bal</div></div>`;
 $('#cards').innerHTML=test.map((q,i)=>`<article class="card q p-5 fade" style="animation-delay:${i*70}ms"><div class="flex justify-between items-center mb-2"><span class="chip" style="background:${LV[q.lv][2]};color:#fff">${LV[q.lv][0]} · ${LV[q.lv][1]} bal</span><span class="mut text-sm">${q.t}</span></div><h3 class="font-bold text-lg">${i+1}. ${esc(q.q)}</h3>${q.o.map((o,j)=>`<div class="opt${showKey&&j===q.a?' ok':''}"><b>${'ABCD'[j]}</b> ${esc(o)}</div>`).join('')}<div class="${showKey?'':'hidden'} mt-3 text-sm"><b>Cavab: ${'ABCD'[q.a]}.</b> <span class="mut">${esc(q.e)}</span></div></article>`).join('');
 $('#link').value=location.href.split('#')[0]+'#'+curCode;stats();
}
function rows(){const m={};st.get('tz_r',[]).filter(r=>r.c===curCode&&r.a.length===test.length).forEach(r=>m[(r.su||r.n)+'|'+(r.cl||'')]=r);return Object.values(m)}
const sc=r=>[...r.a].filter(x=>x==='1').length,PC=r=>Math.round(sc(r)/test.length*100);
const clr=p=>p<50?'#e11d48':p<75?'#f59e0b':'#16a34a';
const B=(l,p)=>`<div><div class="flex justify-between text-sm font-bold"><span>${esc(l)}</span><span>${p}%</span></div><div class="rounded-full" style="background:var(--line)"><div class="bar" data-w="${p}" style="background:${clr(p)}"></div></div></div>`;
function stats(){
 const R=rows(),n=R.length,T=[...new Set(test.map(q=>q.t))];
 const avg=n?Math.round(R.reduce((a,r)=>a+PC(r),0)/n):null;
 const tp=T.map(t=>{let a=0,b=0;test.forEach((q,i)=>{if(q.t===t)R.forEach(r=>{b++;if(r.a[i]==='1')a++})});return[t,b?Math.round(a/b*100):null]}).filter(x=>x[1]!==null);
 const G={};R.forEach(r=>(G[r.cl||'-']=G[r.cl||'-']||[]).push(r));
 const cl=Object.entries(G).sort().map(([c,a])=>{const av=Math.round(a.reduce((x,r)=>x+PC(r),0)/a.length),pass=Math.round(a.filter(r=>PC(r)>=50).length/a.length*100);return[`${c} sinfi · ${a.length} şagird · keçmə ${pass}%`,av]});
 const weak=[...tp].sort((a,b)=>a[1]-b[1])[0];
 $('#note').textContent=n?`Bu test üzrə ${n} şagirdin real nəticəsi hesablanıb.`:'Hələ nəticə yoxdur. Şagird testi həll edəndə və ya nəticə kodu əlavə olunanda burada görünəcək.';
 $('#stats').innerHTML=[['Şagird',n,'--ac'],['Siniflər',cl.length,'--ac3'],['Orta nəticə',avg===null?'-':avg+'%','--ac2'],['Zəif mövzu',weak?weak[0]:'-','--ac4']].map(x=>`<div class="card p-4 min-w-[150px]" style="border-top:5px solid var(${x[2]})"><div class="mut text-sm">${x[0]}</div><div class="dsp text-xl font-extrabold">${esc(x[1])}</div></div>`).join('');
 $('#cls').innerHTML=cl.length?cl.map(x=>B(x[0],x[1])).join(''):'<p class="mut text-sm">-</p>';
 $('#chart').innerHTML=tp.length?tp.map(x=>B(x[0],x[1])).join(''):'<p class="mut text-sm">-</p>';
 $('#tbl').innerHTML=n?`<table class="w-full text-sm"><thead><tr class="mut text-left"><th class="py-1">Şagird</th><th>Sinif</th><th>Düz</th><th>%</th></tr></thead><tbody>${R.map(r=>`<tr style="border-top:1px solid var(--line)"><td class="py-2">${esc(r.n)}</td><td>${esc(r.cl||'-')}</td><td>${sc(r)}/${test.length}</td><td><b>${PC(r)}%</b></td></tr>`).join('')}</tbody></table>`:'<p class="mut text-sm">-</p>';
 setTimeout(()=>document.querySelectorAll('.bar').forEach(b=>b.style.width=b.dataset.w+'%'),50);
}
$('#grade').innerHTML=Array.from({length:11},(_,i)=>`<option value="${i+1}"${i==6?' selected':''}>${i+1}-ci sinif</option>`).join('');
$('#subj').innerHTML+=NM.map(n=>`<option>${n}</option>`).join('');
$('#tiles').innerHTML=NM.map((n,i)=>`<button class="tile fade" style="background:linear-gradient(135deg,${DB[n].c[0]},${DB[n].c[1]});animation-delay:${i*50}ms" data-n="${n}"><span class="em">${DB[n].e}</span><b class="dsp text-lg block mt-2">${n}</b><span class="text-sm opacity-90">${DB[n].t.length} mövzu</span></button>`).join('');
document.querySelectorAll('.tile').forEach(b=>b.onclick=()=>{pick(b.dataset.n);$('#params').scrollIntoView()});
$('#subj').onchange=e=>e.target.value&&pick(e.target.value);
['#grade','#topic','#cnt'].forEach(s=>$(s).onchange=chk);
$('#gen').onclick=()=>{showKey=false;build();curCode=code();st.set(tkey(),{c:curCode});render();snd('gen');$('#out').scrollIntoView()};
$('#delt').onclick=()=>{if(!confirm('Bu testi silmək istəyirsiniz? Şagird nəticələri qalacaq.'))return;st.set(tkey(),null);test=[];curCode='';$('#out').classList.add('hidden');toast('Test silindi')};
$('#key').onclick=()=>{showKey=!showKey;render()};
$('#pdf').onclick=()=>{showKey=true;render();toast('PDF hazırdır: çap pəncərəsində “PDF kimi saxla” seçin');setTimeout(()=>{try{window.print()}catch(e){}},800)};
$('#wa').onclick=()=>{const t=`Salam! Testi həll edin (qeydiyyat tələb olunur, hesab yaradın):\n${$('#link').value}`;try{window.open('https://wa.me/?text='+encodeURIComponent(t),'_blank')}catch(e){}toast('WhatsApp paylaşımı açıldı')};
$('#copy').onclick=()=>{try{navigator.clipboard.writeText($('#link').value)}catch(e){$('#link').select()}toast('Link kopyalandı')};
$('#stu').onclick=()=>{const p=parse(curCode);if(p)openStu(test,curCode,true,p)};
$('#radd').onclick=()=>{try{const r=JSON.parse(decodeURIComponent(escape(atob($('#rcode').value.trim().replace(/^r\./,'')))));const p=parse(r.c);if(!p||!r.n||typeof r.a!=='string'||!/^[01]+$/.test(r.a)||r.a.length!==p.n)throw 0;const rs=st.get('tz_r',[]);rs.push({c:p.code,tc:p.tid,cl:String(r.cl||'').slice(0,3),n:String(r.n).slice(0,60),a:r.a,s:Array.isArray(r.s)?r.s:null,su:null,ts:Date.now()});st.set('tz_r',rs);$('#rcode').value='';$('#rcode').style.borderColor='';stats();toast(p.code===curCode?'Nəticə əlavə olundu':'Saxlandı, lakin başqa testə aiddir')}catch(e){snd('bad');$('#rcode').style.borderColor='#e11d48'}};

/* ---------- şagird paneli ---------- */
function sPanel(){
 $('#sh').textContent='Salam, '+me.n;
 $('#si').textContent=`${me.u} · ${me.cl} sinfi`;
 const rs=mine().slice().reverse();
 const pcts=rs.map(r=>Math.round([...r.a].filter(x=>x==='1').length/r.a.length*100));
 const avg=pcts.length?Math.round(pcts.reduce((a,b)=>a+b,0)/pcts.length)+'%':'-';
 $('#sstat').innerHTML=[['Test sayı',rs.length],['Orta nəticə',avg]].map(x=>`<div class="card p-3 px-4" style="border-top:4px solid var(--ac2)"><div class="mut text-xs">${x[0]}</div><div class="dsp text-lg font-extrabold">${x[1]}</div></div>`).join('');
 $('#hist').innerHTML=rs.length?rs.map(r=>{const p=parse(r.c);if(!p)return'';const n=r.a.length,k=[...r.a].filter(x=>x==='1').length;return`<div class="flex flex-wrap justify-between items-center gap-3 p-3 rounded-xl" style="border:1px solid var(--line)"><span><b>${DB[p.sn].t[p.ti]}</b> <span class="mut text-sm">${p.sn} · ${new Date(r.ts).toLocaleDateString('az-AZ')}</span></span><span class="flex gap-2 items-center"><span class="chip" style="background:var(--ac2);color:#fff">${k}/${n} · ${Math.round(k/n*100)}%</span><button class="btn ghost !px-3 !py-2" data-rev="${r.ts}">Bax</button></span></div>`}).join(''):'<p class="mut">Hələ test həll etməmisiniz.</p>';
}
$('#hist').onclick=e=>{const b=e.target.closest('[data-rev]');if(!b)return;const rec=mine().find(r=>String(r.ts)===b.dataset.rev);if(rec)review(rec)};
$('#go').onclick=()=>startCode($('#code').value);
function startCode(c){const p=parse(c);if(!p){snd('bad');$('#cerr').textContent='Kod yanlışdır. Müəllimin göndərdiyi kodu və ya linki yazın (məs. t-7-0-1-6-AB12CD).';return}$('#cerr').textContent='';openStu(mk(p.sn,p.ti,p.n),p.code,false,p)}

/* ---------- test həlli və nəticə ---------- */
function openStu(t,cd,prev,p){
 const m=$('#mbox');
 m.innerHTML=`<div class="flex justify-between items-center gap-3"><div><h2 class="text-2xl font-extrabold">${p.sn} testi</h2><p class="mut text-sm">${DB[p.sn].t[p.ti]} · ${p.g}-ci sinif səviyyəsi</p></div><button class="btn ghost" onclick="closeM()">Bağla</button></div><p class="mut mt-2">${prev?'Önizləmə rejimi: nəticə yadda saxlanmır.':'Şagird: <b>'+esc(me.n)+'</b> · '+esc(me.cl)+' sinfi'}</p>
 <div class="flex justify-between text-sm font-bold mt-4"><span id="prg">0 / ${t.length} cavablandırılıb</span></div><div class="rounded-full mt-1" style="background:var(--line);height:10px"><div id="pbar" class="rounded-full" style="height:10px;width:0;background:var(--ac);transition:.3s"></div></div>`+
 t.map((q,i)=>`<div class="mt-5"><b>${i+1}. ${esc(q.q)}</b>${q.o.map((o,j)=>`<label class="opt"><input type="radio" name="q${i}" value="${j}"> ${esc(o)}</label>`).join('')}</div>`).join('')+
 `<button class="btn green mt-6" id="sub">Cavabları göndər</button><div id="sr"></div>`;
 m.querySelectorAll('.opt input').forEach(r=>r.onchange=()=>{snd('pop');m.querySelectorAll(`input[name="${r.name}"]`).forEach(x=>x.parentElement.classList.toggle('sel',x.checked));const done=t.filter((q,i)=>m.querySelector(`input[name="q${i}"]:checked`)).length;$('#prg').textContent=`${done} / ${t.length} cavablandırılıb`;$('#pbar').style.width=Math.round(done/t.length*100)+'%'});
 $('#modal').classList.add('on');
 $('#sub').onclick=()=>{
  const sel=t.map((q,i)=>{const c=m.querySelector(`input[name="q${i}"]:checked`);return c?+c.value:-1});
  const a=t.map((q,i)=>sel[i]===q.a),k=a.filter(Boolean).length,pc=Math.round(k/t.length*100);
  const rec={c:cd,tc:p.tid,cl:me?me.cl||'':'',n:me?me.n:'Önizləmə',su:me&&me.r==='s'?me.u:null,a:a.map(x=>+x).join(''),s:sel,ts:Date.now()};
  let rc='';
  if(!prev){const rs=st.get('tz_r',[]);rs.push(rec);st.set('tz_r',rs);rc=enc(rec)}
  $('#sub').remove();snd(k*2>=t.length?'ok':'bad');
  $('#sr').innerHTML=`<div class="card p-5 mt-5 fade" style="border-left:6px solid var(--ac2)"><div class="dsp text-3xl font-extrabold">${k} / ${t.length} düz cavab · ${pc}%</div><p class="mut">${k*2>=t.length?'Əla nəticə!':'Səhv cavablarınızı təhlil edin və mövzunu təkrarlayın.'}</p>
   <div class="flex flex-wrap gap-2 mt-3"><button class="btn" id="rev">Cavabları gör</button>${prev?'':''}</div>
   ${rc?`<p class="text-sm mt-4"><b>Nəticə kodu</b> (müəllim başqa cihazdadırsa ona göndərin):</p><div class="flex flex-wrap gap-2 mt-1"><input id="rc" readonly class="f max-w-md" value="${rc}"><button class="btn ghost" id="rcc">Kopyala</button><button class="btn green" id="rcw">WhatsApp</button></div>`:''}</div>`;
  $('#rev').onclick=()=>review(rec);
  if(rc){$('#rcc').onclick=()=>{try{navigator.clipboard.writeText(rc)}catch(e){$('#rc').select()}toast('Kod kopyalandı')};$('#rcw').onclick=()=>{try{window.open('https://wa.me/?text='+encodeURIComponent('Nəticə kodum:\n'+rc),'_blank')}catch(e){}}}
 };
}
function review(rec){
 const p=parse(rec.c);if(!p)return;
 const qs=mk(p.sn,p.ti,p.n),s=Array.isArray(rec.s)?rec.s:null,k=[...rec.a].filter(x=>x==='1').length;
 const body=qs.map((q,i)=>{
  const ok=rec.a[i]==='1',ch=s?s[i]:-1;
  return `<div class="mt-5 p-4 rounded-2xl" style="border:1.5px solid ${ok?'#16a34a':'#e11d48'}"><div class="flex justify-between gap-2 items-start"><b>${i+1}. ${esc(q.q)}</b><span class="chip" style="background:${ok?'#16a34a':'#e11d48'};color:#fff;white-space:nowrap">${ok?'Düz':'Səhv'}</span></div>`+
   q.o.map((o,j)=>{const cls=j===q.a?'ok':(j===ch&&!ok?'bad':'');return `<div class="opt ${cls}"><b>${'ABCD'[j]}</b> ${esc(o)}${j===ch?' <span class="mut text-xs">(sizin cavab)</span>':''}</div>`}).join('')+
   (!ok&&ch<0?'<p class="text-xs mut mt-2">Bu sualda cavab verilməyib.</p>':'')+
   `<p class="text-sm mt-2"><b>İzah:</b> <span class="mut">${esc(q.e)}</span></p></div>`;
 }).join('');
 $('#mbox').innerHTML=`<div class="flex justify-between items-center gap-3"><div><h2 class="text-2xl font-extrabold">Cavabların təhlili</h2><p class="mut text-sm">${p.sn} · ${DB[p.sn].t[p.ti]} · ${k} / ${qs.length} düz</p></div><button class="btn ghost" onclick="closeM()">Bağla</button></div>`+
  (s?'':'<p class="mut text-sm mt-4">Bu nəticədə hansı variantın seçildiyi saxlanmayıb (köhnə kod).</p>')+body;
 $('#modal').classList.add('on');
}
function closeM(){$('#modal').classList.remove('on');if(cur==='student')sPanel()}

/* ---------- qeydiyyat bağlantısı və başlanğıc ---------- */
function route(){
 const m=/^#(t-\d+-\d+-\d+-\d+-[A-Za-z0-9]{6})$/i.exec(location.hash);
 if(!m)return;
 if(me&&me.r==='s'){show('student');$('#code').value=m[1];startCode(m[1])}
 else{pend=m[1];pendNote='Test linki tapıldı. Daxil olun və ya qeydiyyatdan keçin, sonra test avtomatik açılacaq.';show('auth','s','login')}
}
addEventListener('keydown',e=>{if(e.key==='Escape'&&$('#modal').classList.contains('on'))closeM()});
$('#modal').addEventListener('click',e=>{if(e.target.id==='modal')closeM()});
$('#snd').onclick=()=>{mute=!mute;$('#snd').textContent=mute?'🔇':'🔊';if(!mute)snd('pop')};
let dark=matchMedia('(prefers-color-scheme: dark)').matches;
function setTheme(){document.documentElement.dataset.theme=dark?'dark':'light';document.documentElement.classList.toggle('dark',dark);$('#theme').textContent=dark?'☀️':'🌙'}
setTheme();$('#theme').onclick=()=>{dark=!dark;setTheme()};
document.addEventListener('click',e=>{const b=e.target.closest('.btn,.tile');if(!b)return;if(b.id!=='gen')snd('tick');if(b.classList.contains('btn')){const r=b.getBoundingClientRect(),s=Math.max(r.width,r.height),d=document.createElement('span');d.className='rip';d.style.cssText=`width:${s}px;height:${s}px;left:${e.clientX-r.left-s/2}px;top:${e.clientY-r.top-s/2}px`;b.appendChild(d);setTimeout(()=>d.remove(),600)}});
document.querySelectorAll('select').forEach(s=>s.addEventListener('change',()=>snd('pop')));

if(location.hash){route()}
else if(me){show(me.r==='t'?'teacher':'student')}
else{show('home')}
addEventListener('hashchange',route);
</script>
</body>
</html>
