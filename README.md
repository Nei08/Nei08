<!doctype html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Esneider de la Hoz · Melma Ice × Kannde</title>
<meta name="description" content="Portafolio de Esneider de la Hoz: creador de Melma Ice y Kannde.">
<style>
:root{--gold:#f5c84a;--gold2:#fff2b8;--ink:#e8eaf0;--bg:#10131c}
*{box-sizing:border-box}
html,body{margin:0;background:var(--bg);color:var(--ink);font:16px/1.5 system-ui,-apple-system,"Segoe UI",sans-serif;overflow-x:hidden}
#bg{position:fixed;inset:0;z-index:0}
#bg::after{content:"";position:absolute;inset:0;background:linear-gradient(180deg,#10131ccc,#10131c66 40%,#10131ccc)}
#feathers{position:fixed;inset:0;z-index:1;pointer-events:none}
main{position:relative;z-index:2}
.hero{padding:9vh 20px 2vh;text-align:center}
.hero h1{margin:0;font-size:clamp(34px,7vw,76px);line-height:1.05;letter-spacing:-.02em;
  background:linear-gradient(100deg,var(--gold2),var(--gold) 40%,#c8901e 70%,var(--gold2));background-size:200% 100%;
  -webkit-background-clip:text;background-clip:text;color:transparent;animation:shine 6s linear infinite}
.hero p{margin:14px auto 0;max-width:620px;color:#c9cedb;font-size:clamp(15px,2.2vw,19px)}
.hero .hint{margin-top:18px;font-size:13px;color:var(--gold);opacity:.85;animation:pulse 2.4s ease-in-out infinite}
@keyframes shine{to{background-position:-200% 0}}
@keyframes pulse{50%{opacity:.35}}
#stage{position:relative;height:min(72vh,620px);margin:0 auto;max-width:1100px;touch-action:none}
.orb{position:absolute;left:0;top:0;width:clamp(170px,26vw,290px);aspect-ratio:1;border-radius:50%;overflow:hidden;cursor:grab;
  will-change:transform;user-select:none;-webkit-user-select:none;touch-action:none;
  box-shadow:0 0 0 3px #ffffff33,0 0 40px 6px #f5c84a44,0 24px 50px #0008;transition:box-shadow .25s}
.orb:hover{box-shadow:0 0 0 3px var(--gold),0 0 60px 14px #f5c84a77,0 24px 50px #0008}
.orb.grab{cursor:grabbing}
.orb img{width:100%;height:100%;object-fit:cover;display:block;pointer-events:none;-webkit-user-drag:none}
.orb.bear img{animation:bob 3.2s ease-in-out infinite}
.orb.face img{animation:wiggle 2.6s ease-in-out infinite}
@keyframes bob{50%{transform:scale(1.07) translateY(-3%)}}
@keyframes wiggle{0%,100%{transform:rotate(-4deg) scale(1.02)}50%{transform:rotate(5deg) scale(1.1)}}
.tag{position:absolute;left:0;top:0;z-index:3;pointer-events:none;padding:5px 12px;border-radius:99px;font-weight:700;font-size:13px;
  background:#10131ccc;border:1px solid #f5c84a88;color:var(--gold2);white-space:nowrap;will-change:transform;backdrop-filter:blur(4px)}
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:20px;max-width:1000px;margin:6vh auto 0;padding:0 20px}
.card{padding:26px;border-radius:20px;background:#161a26cc;border:1px solid #ffffff1a;backdrop-filter:blur(8px);transition:transform .3s,border-color .3s}
.card.pop{transform:scale(1.04);border-color:var(--gold)}
.card h2{margin:0 0 6px;font-size:24px;color:var(--gold2)}
.card .k{font-size:12px;letter-spacing:.14em;text-transform:uppercase;color:var(--gold)}
.card.melma{border-top:4px solid #2a509c}.card.kannde{border-top:4px solid #ff1f66}
footer{text-align:center;padding:7vh 20px 6vh;color:#9aa1b3}
footer a{color:var(--gold);text-decoration:none;border-bottom:1px dashed #f5c84a88;margin:0 8px}
footer a:hover{color:var(--gold2)}
@media (prefers-reduced-motion:reduce){.hero h1,.orb img,.hero .hint{animation:none}}
</style>
</head>
<body>
<div id="bg"></div>
<canvas id="feathers"></canvas>
<main>
  <section class="hero">
    <h1>Esneider de la Hoz</h1>
    <p>Emprendedor y desarrollador front-end. Creo ecosistemas digitales y conceptos de hardware. Fundador de <b>Melma Ice</b> y <b>Kannde</b>.</p>
    <div class="hint">✦ arrastra, lanza y choca los logos · toca para soltar plumas ✦</div>
  </section>

  <section id="stage" aria-label="Mis empresas">
    <div class="orb bear" data-card="melma" role="img" aria-label="Logo de Melma Ice"><img src="assets/melma-ice.jpg" alt="Melma Ice" draggable="false"></div>
    <div class="orb face" data-card="kannde" role="img" aria-label="Logo de Kannde"><img src="assets/kannde.jpg" alt="Kannde" draggable="false"></div>
    <div class="tag">Melma Ice</div>
    <div class="tag">Kannde</div>
  </section>

  <section class="cards">
    <article class="card melma" id="melma">
      <div class="k">Empresa 01</div>
      <h2>Melma Ice 🐻‍❄️</h2>
      <p>Marca fría, sólida y con carácter. Identidad, producto y ecosistema digital en construcción.</p>
    </article>
    <article class="card kannde" id="kannde">
      <div class="k">Empresa 02</div>
      <h2>Kannde 😋</h2>
      <p>Marca divertida, vibrante y con sabor. Experiencias digitales que se sienten vivas.</p>
    </article>
  </section>

  <footer>
    <a href="https://github.com/nei08">GitHub</a>·<a href="mailto:delahozz027@gmail.com">Contacto</a>
  </footer>
</main>

<script src="assets/melmafx-bg.js"></script>
<script>
/* ---------- Fondo MelmaFX (caída dorada, sin ángel) ---------- */
(function(){
  const host=document.getElementById('bg');let t;
  const mount=()=>MelmaFX.mount(host,'caida-dorada',{w:innerWidth,h:innerHeight});
  mount();
  addEventListener('resize',()=>{clearTimeout(t);t=setTimeout(mount,200)});
})();

/* ---------- Plumas doradas interactivas ---------- */
const FE=(function(){
  const cv=document.getElementById('feathers'),cx=cv.getContext('2d');
  let W,H,D;
  const reduce=matchMedia('(prefers-reduced-motion: reduce)').matches;
  function fit(){D=Math.min(2,devicePixelRatio||1);W=innerWidth;H=innerHeight;cv.width=W*D;cv.height=H*D;cx.setTransform(D,0,0,D,0,0)}
  fit();addEventListener('resize',fit);
  // sprite de pluma dorada
  const sp=document.createElement('canvas');sp.width=64;sp.height=192;
  (function(){const c=sp.getContext('2d');c.scale(4,4);
    const g=c.createLinearGradient(0,0,16,48);['#fff2b8','#f5c84a','#c8901e','#8a5a10'].forEach((s,i)=>g.addColorStop(i/3,s));
    c.fillStyle=g;c.beginPath();c.moveTo(8,1);c.bezierCurveTo(16,10,15,34,8,46);c.bezierCurveTo(1,34,0,10,8,1);c.fill();
    c.strokeStyle='#fff4c866';c.lineWidth=.8;
    for(let i=0;i<9;i++){c.beginPath();c.moveTo(8,6+4.5*i);c.lineTo(i%2?14:2,2+4.5*i);c.stroke()}
    c.strokeStyle='#7a4a0e';c.lineWidth=1;c.beginPath();c.moveTo(8,2);c.quadraticCurveTo(9,26,8,47);c.stroke()})();
  const list=[];const N=reduce?14:Math.round(Math.min(46,Math.max(22,W/32)));
  const mk=(top)=>({x:Math.random()*W,y:top?-60-Math.random()*H:Math.random()*H,vx:0,vy:.5+Math.random()*1.1,
    r:Math.random()*6.28,vr:(Math.random()-.5)*.03,ph:Math.random()*6.28,fs:.02+Math.random()*.03,
    s:14+Math.random()*20,sw:.4+Math.random()*.8,burst:false,a:.55+Math.random()*.45});
  for(let i=0;i<N;i++)list.push(mk(false));
  const m={x:-999,y:-999};
  addEventListener('pointermove',e=>{m.x=e.clientX;m.y=e.clientY},{passive:true});
  function burst(x,y,n=14){for(let i=0;i<n;i++){const a=-Math.PI/2+(Math.random()-.5)*2.6,v=3+Math.random()*6;
    const f=mk(false);f.x=x;f.y=y;f.vx=Math.cos(a)*v;f.vy=Math.sin(a)*v;f.burst=true;f.s=16+Math.random()*22;list.push(f)}}
  function frame(){
    cx.clearRect(0,0,W,H);
    for(let i=list.length-1;i>=0;i--){const f=list[i];
      f.ph+=f.fs;
      const dx=f.x-m.x,dy=f.y-m.y,d2=dx*dx+dy*dy;
      if(d2<14000){const d=Math.sqrt(d2)||1,p=(1-d/118)*1.4;f.vx+=dx/d*p;f.vy+=dy/d*p*.6}
      f.vx*=.97;
      f.vy+= (f.burst?.12:0);                       // gravedad suave en las que explotan
      const fall=f.burst?0:(.5+.5*Math.abs(Math.sin(f.ph*.5)))*.9; // planeo
      f.x+=f.vx+Math.sin(f.ph)*f.sw;f.y+=f.vy*(f.burst?1:.55)+fall*.5;
      if(!f.burst&&f.vy>1.2)f.vy*=.99;
      f.r+=f.vr+f.vx*.004;
      if(f.burst&&f.vy>2&&f.y>H*.1){f.burst=false;f.vx*=.3;f.vy=.7+Math.random()}
      if(f.y>H+60||f.x<-80||f.x>W+80){ if(i<N&&!f.burst||list.length<=N){Object.assign(f,mk(true))}else list.splice(i,1);continue}
      cx.save();cx.translate(f.x,f.y);cx.rotate(f.r);
      cx.scale(.8*Math.cos(f.ph*1.7)+.2,1);          // giro 3D
      cx.globalAlpha=f.a;
      cx.shadowColor='#f0a820aa';cx.shadowBlur=8;
      cx.drawImage(sp,-f.s/3,-f.s,f.s*.66,f.s*2);
      cx.restore()}
    requestAnimationFrame(frame)}
  requestAnimationFrame(frame);
  return {burst};
})();

/* ---------- Logos arrastrables con inercia y choques ---------- */
(function(){
  const stage=document.getElementById('stage');
  const els=[...stage.querySelectorAll('.orb')],tags=[...stage.querySelectorAll('.tag')];
  const o=els.map((el,i)=>({el,tag:tags[i],x:0,y:0,vx:(i?-1:1)*1.4,vy:(i?1:-1)*1,r:0,drag:false,lx:0,ly:0,moved:0}));
  let W=0,H=0;
  function size(){W=stage.clientWidth;H=stage.clientHeight;
    o.forEach((b,i)=>{b.r=b.el.offsetWidth/2;if(!b.ready){b.x=W*(i?.72:.28);b.y=H*.5;b.ready=true}
      b.x=Math.min(Math.max(b.x,b.r),W-b.r);b.y=Math.min(Math.max(b.y,b.r),H-b.r)})}
  size();addEventListener('resize',size);
  o.forEach(b=>{
    const el=b.el;
    el.addEventListener('pointerdown',e=>{el.setPointerCapture(e.pointerId);b.drag=true;b.moved=0;el.classList.add('grab');
      const r=stage.getBoundingClientRect();b.ox=e.clientX-r.left-b.x;b.oy=e.clientY-r.top-b.y;b.lx=e.clientX;b.ly=e.clientY;b.vx=b.vy=0;e.preventDefault()});
    el.addEventListener('pointermove',e=>{if(!b.drag)return;
      const r=stage.getBoundingClientRect();
      const nx=e.clientX-r.left-b.ox,ny=e.clientY-r.top-b.oy;
      b.vx=(e.clientX-b.lx)*.9;b.vy=(e.clientY-b.ly)*.9;b.moved+=Math.abs(e.clientX-b.lx)+Math.abs(e.clientY-b.ly);
      b.lx=e.clientX;b.ly=e.clientY;
      b.x=Math.min(Math.max(nx,b.r),W-b.r);b.y=Math.min(Math.max(ny,b.r),H-b.r)});
    const up=e=>{if(!b.drag)return;b.drag=false;el.classList.remove('grab');
      if(b.moved<8){const r=el.getBoundingClientRect();FE.burst(r.left+r.width/2,r.top+r.height/2,22);
        const c=document.getElementById(el.dataset.card);c.classList.add('pop');setTimeout(()=>c.classList.remove('pop'),700);}};
    el.addEventListener('pointerup',up);el.addEventListener('pointercancel',up);
  });
  function step(){
    o.forEach(b=>{if(b.drag)return;
      b.x+=b.vx;b.y+=b.vy;b.vx*=.992;b.vy*=.992;
      const sp=Math.hypot(b.vx,b.vy);if(sp<.9){const k=.9/(sp||1);b.vx=(b.vx||Math.random()-.5)*k;b.vy=(b.vy||Math.random()-.5)*k} // nunca se detienen
      if(b.x<b.r){b.x=b.r;b.vx=Math.abs(b.vx)}if(b.x>W-b.r){b.x=W-b.r;b.vx=-Math.abs(b.vx)}
      if(b.y<b.r){b.y=b.r;b.vy=Math.abs(b.vy)}if(b.y>H-b.r){b.y=H-b.r;b.vy=-Math.abs(b.vy)}});
    // choque entre ambos
    const [a,c]=o,dx=c.x-a.x,dy=c.y-a.y,d=Math.hypot(dx,dy),min=a.r+c.r;
    if(d<min&&d>0){const nx=dx/d,ny=dy/d,ov=min-d;
      if(!a.drag){a.x-=nx*ov/2;a.y-=ny*ov/2}if(!c.drag){c.x+=nx*ov/2;c.y+=ny*ov/2}
      const rv=(c.vx-a.vx)*nx+(c.vy-a.vy)*ny;
      if(rv<0){const j=-rv*1.05;if(!a.drag){a.vx-=j*nx;a.vy-=j*ny}if(!c.drag){c.vx+=j*nx;c.vy+=j*ny}
        if(-rv>2.5)FE.burst(stage.getBoundingClientRect().left+(a.x+c.x)/2,stage.getBoundingClientRect().top+(a.y+c.y)/2,8)}}
    o.forEach(b=>{b.el.style.transform=`translate(${b.x-b.r}px,${b.y-b.r}px) rotate(${Math.max(-10,Math.min(10,b.vx*1.5))}deg)`;
      b.tag.style.transform=`translate(${b.x-b.tag.offsetWidth/2}px,${b.y+b.r+8}px)`});
    requestAnimationFrame(step)}
  requestAnimationFrame(step);
})();
</script>
</body>
</html>
