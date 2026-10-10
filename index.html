<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Lamp Login</title>
<style>
:root{box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
html,body{height:100%;margin:0}
body{background:#16191a;font-family:"Segoe UI",system-ui,-apple-system,Arial,sans-serif;color:#fff;overflow:hidden;user-select:none;-webkit-user-select:none}
.scene{position:relative;height:100%;display:flex;align-items:center;justify-content:center;gap:6vw;padding:20px;
 background:radial-gradient(ellipse at 30% 50%,#16191a 0%,#16191a 100%);transition:background 1s}
body.on .scene{background:radial-gradient(ellipse at 35% 50%,#4a4631 0%,#2a2b24 35%,#17191a 75%)}
.lamp-wrap{position:relative;width:280px;height:420px;flex:none}
.glow{position:absolute;left:50%;top:70px;width:420px;height:300px;transform:translateX(-50%);
 background:radial-gradient(ellipse,rgba(255,236,160,.55),rgba(255,236,160,0) 65%);opacity:0;transition:opacity .8s;pointer-events:none}
body.on .glow{opacity:1}
.shade{position:absolute;left:50%;top:60px;width:290px;height:110px;transform:translateX(-50%);
 background:#555;border-radius:145px 145px 0 0 / 110px 110px 0 0;transition:all .8s}
.shade::after{content:"";position:absolute;left:0;right:0;bottom:-6px;height:14px;background:inherit;border-radius:50%}
body.on .shade{background:#fff;box-shadow:0 0 40px 12px rgba(255,240,170,.6),0 0 110px 30px rgba(255,225,130,.35)}
.pole{position:absolute;left:50%;top:170px;width:32px;height:250px;margin-left:-16px;background:#d6d3ca;transition:background .8s}
.base{position:absolute;left:50%;bottom:-8px;width:165px;height:26px;margin-left:-82px;background:#d6d3ca;border-radius:13px}
body:not(.on) .pole,body:not(.on) .base{background:#6b6a66}
.rope{position:absolute;left:calc(50% + 62px);top:172px;width:3px;background:#555;height:120px;transform-origin:top;touch-action:none}
.knob{position:absolute;left:50%;bottom:-13px;width:26px;height:26px;margin-left:-12px;border-radius:50%;background:#d9a273;cursor:grab;touch-action:none}
.rope.drag .knob{cursor:grabbing}
.rope::before{content:"";position:absolute;left:-18px;right:-18px;top:0;bottom:-30px}
.hint{position:absolute;left:50%;bottom:-40px;transform:translateX(-50%);font-size:13px;color:#8d8a7a;white-space:nowrap;transition:opacity .4s}
body.on .hint{opacity:0}

.card{width:min(420px,88vw);padding:42px 32px 36px;border-radius:34px;
 background:linear-gradient(135deg,rgba(255,255,255,.12),rgba(255,255,255,.04));
 border:1px solid rgba(255,255,255,.14);backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px);
 box-shadow:0 30px 60px rgba(0,0,0,.45);opacity:0;transform:translateX(30px) scale(.96);pointer-events:none;
 transition:opacity .7s .15s,transform .7s .15s;flex:none}
body.on .card{opacity:1;transform:none;pointer-events:auto}
h1{margin:0 0 28px;text-align:center;font-size:32px;font-weight:700}
label{display:block;margin:0 0 8px 8px;font-size:17px;color:rgba(255,255,255,.45)}
input{width:100%;height:60px;border-radius:20px;border:1px solid transparent;background:rgba(255,255,255,.1);
 color:#fff;font-size:20px;padding:0 28px;margin-bottom:26px;outline:none;font-family:inherit;transition:border-color .2s,background .2s}
input:focus{border-color:#c9a06b;background:rgba(255,255,255,.14)}
input{-webkit-user-select:text;user-select:text;-webkit-touch-callout:default}
button.sign{width:100%;height:60px;border:0;border-radius:20px;font-size:21px;font-weight:700;color:#1a1a1a;cursor:pointer;margin-top:6px;
 background:linear-gradient(115deg,#b8962e 0%,#f4e58c 28%,#a8851f 52%,#f6ea9a 75%,#c9a43a 100%);transition:transform .15s,filter .15s}
button.sign:hover{filter:brightness(1.08)}button.sign:active{transform:scale(.98)}
.msg{text-align:center;margin-top:16px;font-size:15px;min-height:20px;color:#f4e58c}

@media(max-width:760px){
 .scene{flex-direction:column;gap:30px;justify-content:flex-start;padding-top:20px}
 .lamp-wrap{transform:scale(.62);transform-origin:top center;height:420px;width:280px;margin-bottom:-150px}
 .card{padding:30px 22px}
 h1{font-size:28px;margin-bottom:18px}
 input{height:52px;margin-bottom:18px}button.sign{height:52px}
}
</style>
</head>
<body>
<div class="scene">
  <div class="lamp-wrap">
    <div class="glow"></div>
    <div class="shade"></div>
    <div class="pole"></div><div class="base"></div>
    <div class="rope" id="rope"><div class="knob"></div></div>
    <div class="hint">Pull the rope ↓</div>
  </div>

  <div class="card">
    <h1>Welcome</h1>
    <label for="u">Username</label>
    <input id="u" type="text" autocomplete="username" placeholder="Username">
    <label for="p">Password</label>
    <input id="p" type="password" autocomplete="current-password" placeholder="Password">
    <button class="sign" id="go">Sign In</button>
    <div class="msg" id="msg"></div>
  </div>
</div>
<script>
const rope=document.getElementById('rope'),body=document.body,base=120;
let startY=0,dragging=false,pull=0,moved=false;
function setLen(d){rope.style.height=(base+d)+'px'}
function toggle(){body.classList.toggle('on')}
rope.addEventListener('pointerdown',e=>{dragging=true;moved=false;startY=e.clientY;rope.classList.add('drag');rope.setPointerCapture(e.pointerId);rope.style.transition='none'});
rope.addEventListener('pointermove',e=>{if(!dragging)return;pull=Math.max(0,Math.min(70,e.clientY-startY));if(pull>3)moved=true;setLen(pull)});
function end(){if(!dragging)return;dragging=false;rope.classList.remove('drag');
  const fire=pull>35||(!moved&&pull===0&&false);
  rope.style.transition='height .35s cubic-bezier(.3,1.8,.5,1)';setLen(0);
  if(fire)toggle();pull=0}
rope.addEventListener('pointerup',end);rope.addEventListener('pointercancel',end);
rope.addEventListener('click',e=>{if(!moved){setLen(40);setTimeout(()=>{rope.style.transition='height .35s cubic-bezier(.3,1.8,.5,1)';setLen(0)},120);toggle()}});
document.getElementById('go').addEventListener('click',()=>{
  const u=document.getElementById('u').value.trim(),p=document.getElementById('p').value;
  const m=document.getElementById('msg');
  if(!u||!p){m.textContent='Please enter username and password';return}
  if(u.toLowerCase()==='priyansh jain'&&p==='pj_08'){m.style.color='#9be59b';m.textContent='Welcome, Priyansh Jain ✓';setTimeout(()=>{window.location.href='sign-in.html'},600)}
  else{m.style.color='#ff9b8a';m.textContent='Incorrect username or password'}
});
['u','p'].forEach(id=>document.getElementById(id).addEventListener('keydown',e=>{if(e.key==='Enter')document.getElementById('go').click()}));
</script>
</body>
</html>
