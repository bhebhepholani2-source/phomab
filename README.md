<!DOCTYPE html>
<html lang="en"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#0e7c86">
<title>Phomab</title>
<style>
:root{--bg:#fff7ec;--card:#fff;--ink:#1d2433;--mut:#5f6577;--pri:#0e7c86;--pri2:#d9f2f4;--line:#eadfce;--acc:#f59e0b;--grad:linear-gradient(135deg,#0e7c86,#6d28d9);--pmb:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='60' height='60'%3E%3Cg font-family='Arial' font-weight='900' font-size='11' fill='%230e7c86' fill-opacity='.22' text-anchor='middle'%3E%3Ctext x='15' y='19' transform='rotate(-20 15 15)'%3EPMB%3C/text%3E%3Ctext x='45' y='49' transform='rotate(-20 45 45)'%3EPMB%3C/text%3E%3C/g%3E%3C/svg%3E");padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root{--bg:#101a1d;--card:#172529;--ink:#e9f1f2;--mut:#9db0b4;--pri:#3dd6d0;--pri2:#12363a;--line:#27403f;--acc:#ffb84d;--pmb:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='60' height='60'%3E%3Cg font-family='Arial' font-weight='900' font-size='11' fill='%233dd6d0' fill-opacity='.2' text-anchor='middle'%3E%3Ctext x='15' y='19' transform='rotate(-20 15 15)'%3EPMB%3C/text%3E%3Ctext x='45' y='49' transform='rotate(-20 45 45)'%3EPMB%3C/text%3E%3C/g%3E%3C/svg%3E")}}
*{box-sizing:border-box}html,body{height:100%;margin:0}
body{background:var(--bg) var(--pmb);color:var(--ink);font:15px/1.4 system-ui,-apple-system,Segoe UI,Roboto,sans-serif;display:flex;flex-direction:column}
header{padding:10px 14px;display:flex;align-items:center;gap:8px;background:var(--grad);color:#fff}
header b{font-size:19px;letter-spacing:.5px}
nav{display:flex;background:var(--card);border-bottom:1px solid var(--line)}
nav button{flex:1;padding:11px 4px;border:0;background:none;color:var(--mut);font:inherit;font-weight:600;border-bottom:3px solid transparent}
nav button.on{color:var(--pri);border-color:var(--acc)}
main{flex:1;overflow-y:auto;padding:12px 14px}
.card{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:12px;margin:8px 0}
.card h4{margin:0 0 3px;font-size:15px}.card p{margin:3px 0;color:var(--mut);font-size:13px}
.card img.ph{width:100%;max-height:190px;object-fit:cover;border-radius:10px;margin-bottom:6px}
label{display:block;margin-top:6px;font-size:12px;color:var(--mut)}
input,select,textarea{width:100%;padding:10px 12px;margin:3px 0;border-radius:10px;border:1px solid var(--line);background:var(--bg);color:var(--ink);font:inherit;min-width:0}
.price{font-weight:700;color:var(--pri)!important}
.row{display:flex;gap:8px;margin-top:8px;flex-wrap:wrap;align-items:center}
.b{min-height:40px;padding:8px 14px;border-radius:10px;border:1px solid transparent;background:var(--grad);color:#fff;font:inherit;font-weight:600;text-decoration:none;display:inline-flex;align-items:center;width:auto}
.b.o{background:none;color:var(--pri);border-color:var(--pri)}
.tag{display:inline-block;font-size:11px;padding:2px 8px;border-radius:99px;background:var(--pri2);color:var(--pri);font-weight:700}
.tag.ok{background:var(--pri);color:#fff}
.mut{color:var(--mut);font-size:13px}.err{color:#c0392b;font-size:13px}
.bub{max-width:86%;padding:8px 12px;border-radius:14px;margin:5px 0;background:var(--card);border:1px solid var(--line);white-space:pre-wrap;overflow-wrap:anywhere}
.bub.me{margin-left:auto;background:var(--grad);color:#fff;border-color:transparent}
.bar{display:none;gap:8px;padding:10px 12px;background:var(--card);border-top:1px solid var(--line)}
.bar input{flex:1;margin:0}
.f{display:grid;grid-template-columns:1fr 1fr;gap:6px}.f input,.f select{margin:0}
a{color:var(--pri);cursor:pointer}
#toast{position:fixed;left:50%;bottom:90px;transform:translateX(-50%);background:var(--ink);color:var(--bg);padding:9px 16px;border-radius:99px;font-size:13px;display:none;z-index:60}
#call{position:fixed;inset:0;background:#000;z-index:70;display:none;flex-direction:column;align-items:center;justify-content:center;gap:10px;padding:12px}
#call video{max-width:100%;max-height:60%;border-radius:12px;background:#111}#call #lv{width:110px}

.chips{display:flex;gap:6px;flex-wrap:wrap}
.chip{min-height:34px;padding:6px 12px;border-radius:99px;background:var(--pri2);color:var(--pri);border:0;font:inherit;font-size:13px;font-weight:600;width:auto}
.chip.on{background:var(--grad);color:#fff}
</style></head><body>
<header><b>Phomab</b><span style="flex:1"></span><button class="b o" id="lg" aria-label="Language" style="color:#fff;border-color:#fff8;min-height:34px;padding:4px 10px"></button><button class="b o" id="hl" style="color:#fff;border-color:#fff8;min-height:34px;padding:4px 10px"></button></header>
<nav><button data-t="home">Home</button><button data-t="post">Post</button><button data-t="chats">Chats</button><button data-t="groups">Groups</button><button data-t="me">Me</button></nav>
<main id="main"></main>
<div class="bar" id="bar"><input id="inp" aria-label="Message"><button class="b o" id="cam" aria-label="Send photo">📷</button><button class="b o" id="off">Offer $</button><button class="b" id="send">Send</button><input type="file" id="pic" accept="image/*" hidden></div>
<div id="toast"></div>
<script type="module">
import{initializeApp}from'https://www.gstatic.com/firebasejs/10.12.2/firebase-app.js';
import{getAuth,onAuthStateChanged,createUserWithEmailAndPassword as signUp,signInWithEmailAndPassword as signIn,signOut,sendEmailVerification,sendPasswordResetEmail,updateProfile}from'https://www.gstatic.com/firebasejs/10.12.2/firebase-auth.js';
import{getFirestore,collection,doc,setDoc,addDoc,getDoc,updateDoc,deleteDoc,query,orderBy,limit,where,onSnapshot,arrayUnion}from'https://www.gstatic.com/firebasejs/10.12.2/firebase-firestore.js';

/* PASTE YOUR FIREBASE WEB APP CONFIG HERE (Project settings > Your apps > Phomab) */
let SV={};try{SV=JSON.parse(localStorage.getItem('pm_cfg')||'{}')}catch(e){}
const CFG={apiKey:SV.apiKey||'PASTE_API_KEY',authDomain:SV.authDomain||(SV.projectId||'pmata-26d51')+'.firebaseapp.com',projectId:SV.projectId||'pmata-26d51',messagingSenderId:SV.messagingSenderId||'PASTE_SENDER_ID',appId:SV.appId||'PASTE_APP_ID'};

const $=s=>document.querySelector(s),esc=s=>String(s??'').replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const TX={en:{home:'Home',post:'Post',chats:'Chats',groups:'Groups',me:'Me',ph:'Type a message',msg:'Message',conf:'Confirm deal',send:'Send',srch:'Search',sp:'Try: 2 roomed house in Nketha under $150'},nd:{home:'Ikhaya',post:'Beka',chats:'Izingxoxo',groups:'Amaqembu',me:'Mina',ph:'Bhala umlayezo',msg:'Umlayezo',conf:'Vuma isivumelwano',send:'Thumela',srch:'Funa',sp:'Zama: indlu eyi-2 e-Nketha ngaphansi kuka-$150'},sn:{home:'Kumba',post:'Isa',chats:'Hurukuro',groups:'Mapoka',me:'Ini',ph:'Nyora meseji',msg:'Meseji',conf:'Bvuma chibvumirano',send:'Tumira',srch:'Tsvaga',sp:'Edza: imba ye2 muNketha pasi pe$150'}};
let LG='en',LOC=null;try{LG=localStorage.getItem('pm_lg')||'en';LOC=JSON.parse(localStorage.getItem('pm_loc'))}catch(e){}
const T=k=>(TX[LG]||TX.en)[k];
const toast=m=>{const t=$('#toast');t.textContent=m;t.style.display='block';clearTimeout(toast.x);toast.x=setTimeout(()=>t.style.display='none',3000)};
const XY={Town:[-20.150,28.580],Nketha:[-20.185,28.510],Luveve:[-20.120,28.500],Entumbane:[-20.135,28.515],Mzilikazi:[-20.140,28.550],Pumula:[-20.190,28.460],'Cowdray Park':[-20.200,28.430],Magwegwe:[-20.130,28.490],Mganwini:[-20.190,28.500],Nkulumane:[-20.190,28.530],Emakhandeni:[-20.165,28.525],Tshabalala:[-20.190,28.550],Njube:[-20.165,28.550],Lobengula:[-20.145,28.545],Sizinda:[-20.185,28.560],Barbourfields:[-20.150,28.560],Makokoba:[-20.160,28.570],Iminyela:[-20.170,28.570],Matshobana:[-20.195,28.510],Gwabalanda:[-20.115,28.510],Hillside:[-20.190,28.620],Kumalo:[-20.170,28.620],Famona:[-20.160,28.600],Mahatshula:[-20.095,28.600],'Queens Park':[-20.150,28.620]};
const AREAS=Object.keys(XY),CATS={house:'House',service:'Service',job:'Job',ride:'Ride'},UNIT={house:'month',service:'job',job:'job',ride:'trip'},UNITS=['month','job','hour','visit','lesson','trip'];
const hv=(a,b)=>{const r=Math.PI/180,x=Math.sin((b[0]-a[0])*r/2)**2+Math.cos(a[0]*r)*Math.cos(b[0]*r)*Math.sin((b[1]-a[1])*r/2)**2;return 12742*Math.asin(Math.sqrt(x))};
const km=a=>LOC&&XY[a]?hv(LOC.xy,XY[a]):null;

let app,auth,db,U=null,L=[],RV={},MYRV={},CH=[],MS=[],cur=null,tab='home',F={cat:'',area:'',max:'',rooms:'',kw:'',text:''},uM=null;
const setup=CFG.apiKey.startsWith('PASTE');
if(!setup){app=initializeApp(CFG);auth=getAuth(app);db=getFirestore(app)}
const put=h=>{const d=document.createElement('div');d.className='card';d.innerHTML=h;$('#main').appendChild(d);return d};
const idoc=(c,id)=>doc(db,c,id),me=()=>U&&U.displayName||'Someone',stars=o=>o&&o.n?` ★ ${(o.s/o.n).toFixed(1)} (${o.n})`:'';
const agreed=c=>(c.confirmed||[]).length>=2,unread=c=>c.lastBy&&c.lastBy!=U.uid&&(c.last||0)>((c.seen||{})[U.uid]||0);
const unsub=()=>{uM&&uM();uM=null;MS=[]};

/* ---------- live data ---------- */
if(!setup){
 onSnapshot(query(collection(db,'listings'),orderBy('at','desc'),limit(100)),s=>{L=s.docs.map(d=>({id:d.id,...d.data()}));if(tab=='home'||tab=='post')render()},e=>toast('Could not load listings: '+e.code));
 onSnapshot(query(collection(db,'reviews'),limit(500)),s=>{RV={};MYRV={};s.docs.forEach(d=>{const r=d.data();(RV[r.to]=RV[r.to]||{s:0,n:0}).s+=r.stars;RV[r.to].n++;if(U&&r.from==U.uid)MYRV[r.chatId]=r.stars})});
 onAuthStateChanged(auth,u=>{U=u;CH=[];if(u)onSnapshot(query(collection(db,'chats'),where('participants','array-contains',u.uid)),s=>{CH=s.docs.map(d=>({id:d.id,...d.data()}));if(tab=='chats'||tab=='chat')render()},()=>{});render()});
}

/* ---------- shell ---------- */
document.querySelectorAll('nav button').forEach(b=>b.onclick=()=>{tab=b.dataset.t;cur=null;unsub();render()});
function render(){
 document.querySelectorAll('nav button').forEach(b=>{b.textContent=T(b.dataset.t);b.classList.toggle('on',b.dataset.t==(tab=='chat'?'chats':tab=='room'?'groups':tab))});
 $('#hl').textContent=LOC?'📍 '+LOC.area:'📍 Set area';$('#lg').textContent=LG.toUpperCase();$('#inp').placeholder=T('ph');$('#send').textContent=T('send');
 $('#bar').style.display=tab=='chat'||tab=='room'?'flex':'none';$('#off').style.display=$('#cam').style.display=tab=='chat'?'':'none';
 const m=$('#main'),keep=m.scrollTop;m.innerHTML='';
 if(setup){put('<h4>First-time setup</h4><p>In Firebase: Project settings, then Your apps, then the config box. Copy the whole config and paste it here. You only do this once on this phone.</p><textarea id="cf" rows="7" placeholder="apiKey: ..., authDomain: ..., projectId: ..., appId: ..."></textarea><p class="err" id="cer"></p><div class="row"><button class="b" data-a="cfg">Save and start</button></div>');return}
 ({home,post,chats,chat,room,groups,me:account})[tab]();m.scrollTop=tab=='chat'||tab=='room'?1e9:keep;
}

/* ---------- home: one search for everything ---------- */
function parse(t){t=t.toLowerCase();const f={cat:'',area:'',max:'',rooms:'',kw:'',text:t};
 if(/house|room|flat|cottage|rent|indlu|imba|renda/.test(t))f.cat='house';
 else if(/\bride\b|taxi|kombi|lift|uthekisi|rwendo/.test(t))f.cat='ride';
 else if(/\bjobs?\b|hiring|vacanc|basa|umsebenzi|employ/.test(t))f.cat='job';
 const k=t.match(/plumb|electric|tutor|lesson|clean|weld|carpent|garden|build|paint|tiler|tailor|barber|hair|mechanic|mover|photograph/);
 if(k){f.kw=k[0];if(!f.cat)f.cat='service'}
 const b=t.match(/(?:under|below|max|budget|\$)\s?(\d{1,3}(?:[ ,]\d{3})+|\d+)/);if(b)f.max=b[1].replace(/[ ,]/g,'');
 const r=t.match(/(\d)\s*-?\s*room/);if(r)f.rooms=r[1];
 f.area=AREAS.find(a=>t.includes(a.toLowerCase()))||'';return f}
function home(){
 put(`<form id="sf" style="display:flex;gap:8px"><input id="sq" style="margin:0" placeholder="${esc(T('sp'))}" value="${esc(F.text)}" aria-label="Search"><button class="b">${T('srch')}</button></form><div class="chips" style="margin-top:8px">${['',...Object.keys(CATS)].map(k=>`<button type="button" class="chip${F.cat==k?' on':''}" data-a="cat" data-i="${k}">${k?CATS[k]:'All'}</button>`).join('')}</div><div class="f" style="margin-top:8px"><select id="fa" aria-label="Area"><option value="">All areas</option>${AREAS.map(a=>`<option${F.area==a?' selected':''}>${a}</option>`).join('')}</select><input id="fm" type="number" min="0" placeholder="Max price $" value="${esc(F.max)}"></div>`);
 $('#sf').onsubmit=e=>{e.preventDefault();const t=$('#sq').value.trim();F=t?parse(t):{...F,text:'',kw:'',rooms:''};render()};
 $('#fa').onchange=e=>{F.area=e.target.value;render()};$('#fm').onchange=e=>{F.max=e.target.value;render()};
 const l=L.filter(x=>x.status!='taken'&&(!F.cat||x.cat==F.cat)&&(!F.area||x.area==F.area)&&(!F.max||x.price<=+F.max)&&(!F.rooms||x.rooms==+F.rooms)&&(!F.kw||(x.title+' '+(x.desc||'')).toLowerCase().includes(F.kw)));
 l.sort((a,b)=>(LOC?(km(a.area)??99)-(km(b.area)??99):0)||b.at-a.at);
 if(!l.length){put('<h4>Nothing here yet</h4><p>Be the first: open Post and list what you offer or what you need.</p>');return}
 l.forEach(x=>{const d=km(x.area),mine=U&&x.ownerId==U.uid;
  put(`${x.photo?`<img class="ph" alt="Photo" src="${x.photo}">`:''}<h4>${esc(x.title)}</h4><p><span class="tag">${x.mode=='need'?'Needs':'Offers'}</span> ${CATS[x.cat]||''} · ${esc(x.area)}${d!=null?' · '+d.toFixed(1)+' km':''}${x.rooms?' · '+x.rooms+' rooms':''}${x.to?' · to '+esc(x.to):''}</p>${x.desc?`<p>${esc(x.desc)}</p>`:''}<p class="price">$${x.price} per ${esc(x.unit)}</p><p>${esc(x.ownerName)} ${x.ownerVerified?'<span class="tag ok">✓ Email verified</span>':'<span class="tag">Unverified</span>'}${stars(RV[x.ownerId])}</p><div class="row">${mine?'<span class="tag">Your listing</span>':`<button class="b" data-a="msg" data-i="${x.id}">${T('msg')}</button><a data-a="rep" data-i="${x.id}">Report</a>`}</div>`)});
}

/* ---------- post ---------- */
const gate=()=>!U?(authView('Log in to post'),1):!U.emailVerified?(put('<h4>Verify your email</h4><p>We sent a link to '+esc(U.email)+'. Open it, then tap the button.</p><div class="row"><button class="b" data-a="chk">I have verified</button><button class="b o" data-a="resend">Resend email</button></div>'),1):0;
const shrink=(f,w=640)=>new Promise(r=>{const fr=new FileReader();fr.onload=()=>{const im=new Image();im.onload=()=>{const k=Math.min(1,w/Math.max(im.width,im.height)),c=document.createElement('canvas');c.width=im.width*k;c.height=im.height*k;c.getContext('2d').drawImage(im,0,0,c.width,c.height);r(c.toDataURL('image/jpeg',.6))};im.onerror=()=>r(null);im.src=fr.result};fr.onerror=()=>r(null);fr.readAsDataURL(f)});
function post(){
 if(gate())return;
 put(`<h4>Post something</h4><div class="f"><div><label>I am</label><select id="pm"><option value="offer">Offering</option><option value="need">Looking for</option></select></div><div><label>Category</label><select id="pc">${Object.entries(CATS).map(([k,v])=>`<option value="${k}">${v}</option>`).join('')}</select></div></div><label>Title</label><input id="pt" placeholder="e.g. 2-roomed cottage, Plumber, Ride to Town"><label>Area</label><select id="pa">${AREAS.map(a=>`<option${LOC&&LOC.area==a?' selected':''}>${a}</option>`).join('')}</select><div class="f"><div><label>Rooms (houses)</label><input id="pr" type="number" min="1"></div><div><label>Destination (rides)</label><input id="pd2"></div></div><div class="f"><div><label>Price $</label><input id="pp" type="number" min="1"></div><div><label>Per</label><select id="pu">${UNITS.map(u=>`<option>${u}</option>`).join('')}</select></div></div><label>Details (optional)</label><textarea id="pd" rows="2" maxlength="300"></textarea><label>Photo (optional)</label><input id="pf" type="file" accept="image/*"><p class="err" id="pe"></p><div class="row"><button class="b" data-a="pub">Publish</button></div>`);
 $('#pc').onchange=e=>{$('#pu').value=UNIT[e.target.value]};
 put('<b>Your posts</b>');const mine=L.filter(x=>x.ownerId==U.uid);if(!mine.length)put('<p>Nothing posted yet.</p>');
 mine.forEach(x=>put(`<h4>${esc(x.title)} · ${esc(x.area)}</h4><p class="price">$${x.price} per ${esc(x.unit)} · ${x.status=='taken'?'Closed':'Open'}</p><div class="row"><button class="b o" data-a="tk" data-i="${x.id}">${x.status=='taken'?'Reopen':'Mark closed'}</button><button class="b o" data-a="del" data-i="${x.id}">Delete</button></div>`));
}

/* ---------- chats and deals ---------- */
function chats(){
 if(!U)return authView('Log in to see your chats');
 if(!CH.length)return put('<h4>No chats yet</h4><p>Find a listing on Home and tap Message.</p>');
 CH.slice().sort((a,b)=>(b.last||0)-(a.last||0)).forEach(c=>{const o=c.participants.find(p=>p!=U.uid);put(`<h4>${esc(c.title)}</h4><p>With ${esc((c.names||{})[o])} · <span class="price">$${c.price}</span> · <span class="tag${agreed(c)?' ok':''}">${agreed(c)?'Agreed':'Negotiating'}</span> ${unread(c)?'<span class="tag ok">New</span>':''}</p><p>${esc(c.lastText||'')}</p><div class="row"><button class="b o" data-a="open" data-i="${c.id}">Open chat</button></div>`)});
}
function chat(){
 const c=CH.find(x=>x.id==cur);if(!c){tab='chats';return render()}
 const o=c.participants.find(p=>p!=U.uid),ag=agreed(c),mine=(c.confirmed||[]).includes(U.uid),ph=(c.phones||{})[o],oSeen=(c.seen||{})[o]||0;
 put(`<h4>${esc(c.title)}</h4><p>With ${esc((c.names||{})[o])}${stars(RV[o])} · <span class="price">$${c.price} per ${esc(c.unit)}</span> · <span class="tag${ag?' ok':''}">${ag?'Agreed':mine?'Waiting for them':'Negotiating'}</span></p><div class="row"><button class="b o" data-a="back">← Chats</button>${mine?'':'<button class="b" data-a="conf">'+T('conf')+'</button>'}${ag&&ph?`<a class="b" href="tel:${esc(ph)}">📞 Call phone</a>`:''}</div>${ag?(MYRV[c.id]?`<p>You rated ${MYRV[c.id]}★</p>`:`<div class="row"><span class="mut">Rate:</span>${[1,2,3,4,5].map(n=>`<button class="b o" data-a="rate" data-i="${n}">${n}★</button>`).join('')}</div>`):''}`);
 MS.forEach(m=>{const d=document.createElement('div'),me2=m.from==U.uid;d.className='bub'+(me2?' me':'');
  if(m.type=='img'){const i=document.createElement('img');i.src=m.img;i.alt='Photo';i.style.cssText='max-width:100%;border-radius:10px;display:block';d.appendChild(i)}
  else d.append(m.type=='offer'?`Offer: $${m.price} per ${c.unit}`:m.text);
  if(m.type=='offer'&&!me2){const b=document.createElement('button');b.className='b';b.style.marginTop='6px';b.textContent=c.price==m.price?'Accepted':'Accept offer';b.disabled=c.price==m.price;b.dataset.a='acc';b.dataset.i=m.price;d.appendChild(document.createElement('br'));d.appendChild(b)}
  if(me2){const t=document.createElement('div');t.style.cssText='font-size:11px;text-align:right;opacity:.85';t.textContent=m.at<=oSeen?'✓✓ Seen':'✓ Sent';d.appendChild(t)}
  $('#main').appendChild(d)});
 if(unread(c))updateDoc(idoc('chats',cur),{['seen.'+U.uid]:Date.now()}).catch(()=>{});
}
function openChat(id){unsub();cur=id;tab='chat';uM=onSnapshot(query(collection(db,'chats',id,'messages'),orderBy('at')),s=>{MS=s.docs.map(d=>d.data());if(tab=='chat')render()},e=>toast('Chat error: '+e.code));render()}
const say=(t,x={})=>addDoc(collection(db,'chats',cur,'messages'),{from:U.uid,text:t,at:Date.now(),...x}).then(()=>updateDoc(idoc('chats',cur),{lastText:t||(x.type=='img'?'📷 Photo':'Offer $'+x.price),last:Date.now(),lastBy:U.uid}));

/* ---------- groups ---------- */
function groups(){
 if(!U)return authView('Log in to join groups');
 put('<h4>Neighbourhood groups</h4><p>One chat room for each area. You need a verified email to write.</p><div class="chips">'+(LOC?'<button class="chip on" data-a="room" data-i="'+esc(LOC.area)+'">My area: '+esc(LOC.area)+'</button>':'')+AREAS.map(a=>'<button class="chip" data-a="room" data-i="'+a+'">'+a+'</button>').join('')+'</div>');
}
function openRoom(a){unsub();cur=a;tab='room';uM=onSnapshot(query(collection(db,'rooms',a,'messages'),orderBy('at','desc'),limit(100)),s=>{MS=s.docs.map(d=>d.data()).reverse();if(tab=='room')render()},e=># phomab
