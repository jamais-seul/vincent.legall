<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Réunion Life — Simulation</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #0f172a;
  --card: #1e293b;
  --text: #f1f5f9;
  --muted: #94a3b8;
  --accent: #22d3ee;
  --green: #34d399;
  --orange: #fb923c;
  --pink: #f472b6;
  --red: #f87171;
  --border: #334155;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
body {
  font-family: 'Nunito', system-ui, sans-serif;
  background: var(--bg);
  color: var(--text);
  min-height: 100vh;
  line-height: 1.45;
}
#app { max-width: 920px; margin: 0 auto; padding: 1rem; }

/* Screens */
.screen { display: none; }
.screen.active { display: block; }

/* Header */
.topbar {
  display: flex; flex-wrap: wrap; gap: .6rem; align-items: center;
  background: var(--card); border: 1px solid var(--border);
  border-radius: 14px; padding: .7rem 1rem; margin-bottom: 1rem;
}
.topbar .money { font-weight: 800; color: var(--green); font-size: 1.1rem; }
.topbar .loc { color: var(--accent); font-weight: 700; }
.bars { display: flex; flex-wrap: wrap; gap: .5rem; flex: 1; }
.bar {
  flex: 1; min-width: 90px; background: #0f172a; border-radius: 8px;
  overflow: hidden; height: 22px; position: relative; border: 1px solid var(--border);
}
.bar span {
  position: absolute; left: 6px; top: 50%; transform: translateY(-50%);
  font-size: .7rem; font-weight: 700; z-index: 1; text-shadow: 0 1px 2px #000;
}
.bar .fill { height: 100%; transition: width .4s; }
.bar.hunger .fill { background: #f97316; }
.bar.energy .fill { background: #38bdf8; }
.bar.social .fill { background: #a78bfa; }
.bar.fun .fill { background: #f472b6; }

/* Cards & buttons */
.card {
  background: var(--card); border: 1px solid var(--border);
  border-radius: 14px; padding: 1.1rem; margin-bottom: 1rem;
}
h1, h2, h3 { font-weight: 800; }
h1 { font-size: 1.6rem; margin-bottom: .4rem; }
h2 { font-size: 1.25rem; margin-bottom: .6rem; color: var(--accent); }
.sub { color: var(--muted); margin-bottom: 1rem; font-size: .95rem; }

.btn {
  display: inline-flex; align-items: center; justify-content: center; gap: .35rem;
  background: var(--accent); color: #0f172a; border: 0; padding: .55rem 1rem;
  border-radius: 10px; font-weight: 700; font-size: .9rem; cursor: pointer;
  font-family: inherit; transition: filter .15s;
}
.btn:hover { filter: brightness(1.1); }
.btn.sec { background: #334155; color: var(--text); }
.btn.green { background: var(--green); color: #064e3b; }
.btn.orange { background: var(--orange); color: #7c2d12; }
.btn.pink { background: var(--pink); color: #831843; }
.btn.red { background: var(--red); color: #7f1d1d; }
.btn:disabled { opacity: .45; cursor: not-allowed; }
.btn-row { display: flex; flex-wrap: wrap; gap: .5rem; margin-top: .8rem; }

/* Character creation */
.grid2 { display: grid; grid-template-columns: 1fr 1fr; gap: .8rem; }
@media(max-width:600px){ .grid2 { grid-template-columns: 1fr; } }
input, select {
  width: 100%; padding: .6rem .8rem; border-radius: 10px; border: 1px solid var(--border);
  background: #0f172a; color: var(--text); font-family: inherit; font-size: .95rem;
}
label { font-weight: 700; font-size: .85rem; display: block; margin-bottom: .25rem; }

/* Locations & houses */
.loc-grid, .house-grid, .job-grid, .npc-grid, .shop-grid {
  display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: .7rem;
}
.item {
  background: #0f172a; border: 1px solid var(--border); border-radius: 12px;
  padding: .9rem; cursor: pointer; transition: border-color .15s;
}
.item:hover { border-color: var(--accent); }
.item h3 { font-size: 1rem; margin-bottom: .25rem; }
.item p { font-size: .82rem; color: var(--muted); }
.item .price { color: var(--green); font-weight: 800; margin-top: .4rem; }
.item.owned { border-color: var(--green); }
.item.selected { border-color: var(--accent); box-shadow: 0 0 0 2px rgba(34,211,238,.3); }

/* Log */
#log {
  max-height: 180px; overflow-y: auto; font-size: .88rem;
  background: #0f172a; border-radius: 10px; padding: .7rem;
  border: 1px solid var(--border); margin-top: .8rem;
}
#log div { margin-bottom: .3rem; color: var(--muted); }
#log div.imp { color: var(--accent); font-weight: 700; }

/* Inventory / furniture */
.inv { display: flex; flex-wrap: wrap; gap: .4rem; }
.tag {
  background: #334155; padding: .25rem .6rem; border-radius: 999px;
  font-size: .78rem; font-weight: 700;
}

/* Time */
.time { font-weight: 700; color: var(--orange); }

/* Avatar */
.avatar {
  width: 64px; height: 64px; border-radius: 50%;
  background: linear-gradient(135deg, #22d3ee, #a78bfa);
  display: flex; align-items: center; justify-content: center;
  font-size: 1.8rem; margin-bottom: .5rem;
}
</style>
</head>
<body>
<div id="app">

  <!-- ========== CRÉATION ========== -->
  <div id="screen-create" class="screen active">
    <div class="card">
      <h1>🌴 Réunion Life</h1>
      <p class="sub">Crée ton personnage et commence ta nouvelle vie sur l’île de la Réunion.</p>

      <div class="grid2">
        <div>
          <label>Prénom</label>
          <input id="cName" placeholder="Ex : Léa, Kevin, Marine…" maxlength="20" value="Léa">
        </div>
        <div>
          <label>Style</label>
          <select id="cStyle">
            <option value="😎">Cool</option>
            <option value="😊">Sympa</option>
            <option value="💪">Sportif</option>
            <option value="🎨">Artiste</option>
            <option value="📚">Studieux</option>
            <option value="🌺">Créole</option>
          </select>
        </div>
      </div>

      <div style="margin-top:1rem">
        <label>Personnalité (influence les dialogues)</label>
        <select id="cTrait">
          <option value="sociable">Sociable</option>
          <option value="ambitieux">Ambitieux</option>
          <option value="relax">Relax</option>
          <option value="romantique">Romantique</option>
          <option value="bagarreur">Bagarreur</option>
        </select>
      </div>

      <div class="btn-row">
        <button class="btn green" onclick="startGame()">Commencer ma vie →</button>
      </div>
    </div>
  </div>

  <!-- ========== JEU ========== -->
  <div id="screen-game" class="screen">
    <div class="topbar">
      <div class="avatar" id="pAvatar">😊</div>
      <div>
        <div style="font-weight:800" id="pName">—</div>
        <div class="loc" id="pLoc">—</div>
      </div>
      <div class="money" id="pMoney">0 €</div>
      <div class="time" id="pTime">Lundi 8h</div>
      <div class="bars">
        <div class="bar hunger"><span>Faim</span><div class="fill" id="bHunger" style="width:80%"></div></div>
        <div class="bar energy"><span>Énergie</span><div class="fill" id="bEnergy" style="width:90%"></div></div>
        <div class="bar social"><span>Social</span><div class="fill" id="bSocial" style="width:50%"></div></div>
        <div class="bar fun"><span>Fun</span><div class="fill" id="bFun" style="width:60%"></div></div>
      </div>
    </div>

    <div class="card">
      <h2 id="mainTitle">Que fais-tu ?</h2>
      <div id="mainContent"></div>
      <div class="btn-row" id="mainActions"></div>
      <div id="log"></div>
    </div>
  </div>

</div>

<script>
"use strict";

/* ========== DATA ========== */
const TOWNS = [
  { id:"saintdenis", name:"Saint-Denis", desc:"Capitale, animée, jobs faciles", emoji:"🏙️" },
  { id:"saintpierre", name:"Saint-Pierre", desc:"Sud, plages et ambiance", emoji:"🏖️" },
  { id:"saintpaul", name:"Saint-Paul", desc:"Ouest, marchés et coucher de soleil", emoji:"🌅" },
  { id:"saintbenoit", name:"Saint-Benoît", desc:"Est, nature et calme", emoji:"🌿" },
  { id:"cilaos", name:"Cilaos", desc:"Cirque, montagne, air pur", emoji:"⛰️" },
  { id:"saintleu", name:"Saint-Leu", desc:"Spot de surf et détente", emoji:"🏄" }
];

const HOUSES = [
  { id:"studio_sd", town:"saintdenis", name:"Studio centre-ville", price:18500, confort:1, emoji:"🏢" },
  { id:"appart_sd", town:"saintdenis", name:"Appart 2 pièces", price:32000, confort:2, emoji:"🏠" },
  { id:"case_sp", town:"saintpierre", name:"Case créole", price:28000, confort:2, emoji:"🏡" },
  { id:"appart_sp", town:"saintpierre", name:"Appart vue mer", price:41000, confort:3, emoji:"🌊" },
  { id:"maison_spaul", town:"saintpaul", name:"Petite maison", price:35000, confort:3, emoji:"🌴" },
  { id:"studio_sben", town:"saintbenoit", name:"Studio nature", price:16000, confort:1, emoji:"🍃" },
  { id:"chalet_cil", town:"cilaos", name:"Chalet montagne", price:24000, confort:2, emoji:"🏔️" },
  { id:"bungalow_leu", town:"saintleu", name:"Bungalow surf", price:29000, confort:2, emoji:"🏄" }
];

const JOBS = [
  { id:"caissier", name:"Caissier(e) supermarché", pay:85, energy:-25, fun:-10, town:"saintdenis", emoji:"🛒" },
  { id:"serveur", name:"Serveur(se) restaurant", pay:95, energy:-30, fun:5, town:"saintpierre", emoji:"🍽️" },
  { id:"maçon", name:"Aide-maçon", pay:120, energy:-40, fun:-15, town:"saintpaul", emoji:"🧱" },
  { id:"guide", name:"Guide touristique", pay:110, energy:-20, fun:20, town:"cilaos", emoji:"🗺️" },
  { id:"surf", name:"Moniteur de surf", pay:100, energy:-25, fun:30, town:"saintleu", emoji:"🏄" },
  { id:"marche", name:"Vendeur au marché", pay:75, energy:-20, fun:10, town:"saintpaul", emoji:"🥭" },
  { id:"bureau", name:"Employé de bureau", pay:130, energy:-15, fun:-20, town:"saintdenis", emoji:"💼" },
  { id:"agriculteur", name:"Aide agricole", pay:90, energy:-35, fun:5, town:"saintbenoit", emoji:"🌱" }
];

const NPCs = [
  { id:"maya", name:"Maya", trait:"sympa", age:24, town:"saintdenis", rel:0, emoji:"👩" },
  { id:"kevin", name:"Kévin", trait:"sportif", age:27, town:"saintpierre", rel:0, emoji:"👨" },
  { id:"sharon", name:"Sharon", trait:"romantique", age:22, town:"saintleu", rel:0, emoji:"💃" },
  { id:"jean", name:"Jean-Marc", trait:"calme", age:31, town:"cilaos", rel:0, emoji:"🧔" },
  { id:"lea", name:"Léa", trait:"ambitieuse", age:26, town:"saintpaul", rel:0, emoji:"👩‍💼" },
  { id:"tom", name:"Tom", trait:"bagarreur", age:29, town:"saintdenis", rel:0, emoji:"👊" }
];

const FOODS = [
  { id:"riz", name:"Riz cantonais", price:6, hunger:30, emoji:"🍚" },
  { id:"cari", name:"Cari poulet", price:12, hunger:50, emoji:"🍗" },
  { id:"bouchons", name:"Bouchons", price:8, hunger:35, emoji:"🥟" },
  { id:"samoussa", name:"Samoussas", price:5, hunger:25, emoji:"🥟" },
  { id:"rougail", name:"Rougail saucisse", price:11, hunger:45, emoji:"🌭" },
  { id:"salade", name:"Salade locale", price:7, hunger:20, emoji:"🥗" }
];

const FURNITURE = [
  { id:"canape", name:"Canapé", price:180, confort:1, emoji:"🛋️" },
  { id:"lit", name:"Lit confortable", price:250, confort:2, emoji:"🛏️" },
  { id:"tv", name:"Télévision", price:150, confort:1, emoji:"📺" },
  { id:"table", name:"Table à manger", price:120, confort:1, emoji:"🪑" },
  { id:"frigo", name:"Frigo", price:200, confort:1, emoji:"🧊" },
  { id:"plante", name:"Plantes", price:40, confort:1, emoji:"🪴" }
];

const DAYS = ["Lundi","Mardi","Mercredi","Jeudi","Vendredi","Samedi","Dimanche"];

/* ========== STATE ========== */
let state = {
  name: "",
  style: "😊",
  trait: "sociable",
  money: 25000,
  hunger: 80,
  energy: 90,
  social: 50,
  fun: 60,
  day: 0,
  hour: 8,
  town: null,
  house: null,
  job: null,
  inventory: [],
  furniture: [],
  relationships: {},
  log: []
};

/* ========== UTILS ========== */
function $(id){ return document.getElementById(id); }
function clamp(v){ return Math.max(0, Math.min(100, v)); }
function log(msg, imp=false){
  state.log.unshift({msg, imp, t: `${DAYS[state.day%7]} ${state.hour}h`});
  if(state.log.length > 40) state.log.pop();
  renderLog();
}
function renderLog(){
  const el = $("log");
  if(!el) return;
  el.innerHTML = state.log.slice(0,12).map(l =>
    `<div class="${l.imp?"imp":""}">[${l.t}] ${l.msg}</div>`
  ).join("");
}
function updateBars(){
  $("bHunger").style.width = state.hunger + "%";
  $("bEnergy").style.width = state.energy + "%";
  $("bSocial").style.width = state.social + "%";
  $("bFun").style.width = state.fun + "%";
  $("pMoney").textContent = state.money.toLocaleString("fr-FR") + " €";
  $("pTime").textContent = `${DAYS[state.day%7]} ${state.hour}h`;
  $("pName").textContent = state.name;
  $("pAvatar").textContent = state.style;
  const town = TOWNS.find(t => t.id === state.town);
  $("pLoc").textContent = town ? town.emoji + " " + town.name : "—";
}
function advanceTime(hours){
  state.hour += hours;
  while(state.hour >= 24){
    state.hour -= 24;
    state.day++;
    // decay
    state.hunger = clamp(state.hunger - 15);
    state.energy = clamp(state.energy - 8);
    state.social = clamp(state.social - 5);
    state.fun = clamp(state.fun - 6);
  }
  updateBars();
  checkDeath();
}
function checkDeath(){
  if(state.hunger <= 0 || state.energy <= 0){
    log("Tu es épuisé(e)… Tu t’évanouis et on t’emmène à l’hôpital. (-800 €)", true);
    state.money = Math.max(0, state.money - 800);
    state.hunger = 50;
    state.energy = 40;
    advanceTime(8);
  }
}

/* ========== START ========== */
function startGame(){
  state.name = $("cName").value.trim() || "Inconnu";
  state.style = $("cStyle").value;
  state.trait = $("cTrait").value;
  state.money = 25000;
  $("screen-create").classList.remove("active");
  $("screen-game").classList.add("active");
  log(`Bienvenue ${state.name} ! Tu débarques sur l’île avec 25 000 €.`, true);
  showChooseTown();
}

/* ========== SCREENS ========== */
function clearMain(){
  $("mainContent").innerHTML = "";
  $("mainActions").innerHTML = "";
}

function showChooseTown(){
  clearMain();
  $("mainTitle").textContent = "Choisis ta ville de départ";
  const grid = document.createElement("div");
  grid.className = "loc-grid";
  TOWNS.forEach(t => {
    const d = document.createElement("div");
    d.className = "item";
    d.innerHTML = `<h3>${t.emoji} ${t.name}</h3><p>${t.desc}</p>`;
    d.onclick = () => {
      state.town = t.id;
      log(`Tu t’installes à ${t.name}.`);
      showChooseHouse();
    };
    grid.appendChild(d);
  });
  $("mainContent").appendChild(grid);
}

function showChooseHouse(){
  clearMain();
  $("mainTitle").textContent = "Achète une maison (dans ton budget)";
  const available = HOUSES.filter(h => h.town === state.town && h.price <= state.money);
  if(!available.length){
    $("mainContent").innerHTML = `<p>Aucune maison abordable ici. Tu reçois une aide de 5 000 €.</p>`;
    state.money += 5000;
    updateBars();
  }
  const grid = document.createElement("div");
  grid.className = "house-grid";
  (available.length ? available : HOUSES.filter(h => h.town === state.town)).forEach(h => {
    const d = document.createElement("div");
    d.className = "item" + (h.price > state.money ? "" : "");
    d.innerHTML = `<h3>${h.emoji} ${h.name}</h3>
      <p>Confort : ${"★".repeat(h.confort)}</p>
      <div class="price">${h.price.toLocaleString("fr-FR")} €</div>`;
    d.onclick = () => {
      if(h.price > state.money){ log("Pas assez d’argent !"); return; }
      state.house = h.id;
      state.money -= h.price;
      log(`Tu as acheté : ${h.name} pour ${h.price.toLocaleString("fr-FR")} €`, true);
      updateBars();
      showHub();
    };
    grid.appendChild(d);
  });
  $("mainContent").appendChild(grid);
}

function showHub(){
  clearMain();
  updateBars();
  const town = TOWNS.find(t => t.id === state.town);
  const house = HOUSES.find(h => h.id === state.house);
  $("mainTitle").textContent = `${town.emoji} ${town.name} — Que fais-tu ?`;

  let html = `<p>Maison : <b>${house ? house.emoji + " " + house.name : "Aucune"}</b></p>`;
  if(state.job){
    const j = JOBS.find(j => j.id === state.job);
    html += `<p>Emploi : <b>${j.emoji} ${j.name}</b> (${j.pay} € / service)</p>`;
  } else {
    html += `<p style="color:var(--orange)">Tu n’as pas encore de travail.</p>`;
  }
  html += `<p style="margin-top:.5rem">Meubles : ${state.furniture.length ? state.furniture.map(f => FURNITURE.find(x=>x.id===f)?.emoji).join(" ") : "aucun"}</p>`;
  $("mainContent").innerHTML = html;

  const actions = [
    { label: "💼 Travailler", fn: doWork, show: !!state.job },
    { label: "🔍 Chercher un job", fn: showJobs, show: !state.job },
    { label: "🛒 Faire les courses", fn: showShop },
    { label: "🍳 Cuisiner / Manger", fn: showEat },
    { label: "🛋️ Meubles", fn: showFurniture },
    { label: "🗣️ Voir des gens", fn: showNPCs },
    { label: "🌴 Se promener / Loisirs", fn: doLeisure },
    { label: "✈️ Changer de ville", fn: showTravel },
    { label: "😴 Dormir", fn: doSleep },
    { label: "💾 Sauvegarder", fn: saveGame }
  ];

  actions.filter(a => a.show !== false).forEach(a => {
    const b = document.createElement("button");
    b.className = "btn sec";
    b.textContent = a.label;
    b.onclick = a.fn;
    $("mainActions").appendChild(b);
  });
}

/* ========== ACTIONS ========== */
function showJobs(){
  clearMain();
  $("mainTitle").textContent = "Emplois disponibles";
  const local = JOBS.filter(j => j.town === state.town);
  const grid = document.createElement("div");
  grid.className = "job-grid";
  local.forEach(j => {
    const d = document.createElement("div");
    d.className = "item";
    d.innerHTML = `<h3>${j.emoji} ${j.name}</h3>
      <p>${j.pay} € / service · Énergie ${j.energy} · Fun ${j.fun > 0 ? "+"+j.fun : j.fun}</p>`;
    d.onclick = () => {
      state.job = j.id;
      log(`Tu as été embauché(e) comme ${j.name} !`, true);
      showHub();
    };
    grid.appendChild(d);
  });
  $("mainContent").appendChild(grid);
  const back = document.createElement("button");
  back.className = "btn sec";
  back.textContent = "← Retour";
  back.onclick = showHub;
  $("mainActions").appendChild(back);
}

function doWork(){
  const j = JOBS.find(j => j.id === state.job);
  if(!j) return;
  if(state.energy < 20){ log("Trop fatigué(e) pour travailler."); return; }
  state.money += j.pay;
  state.energy = clamp(state.energy + j.energy);
  state.fun = clamp(state.fun + j.fun);
  state.hunger = clamp(state.hunger - 10);
  advanceTime(4);
  log(`Tu as travaillé (${j.name}) → +${j.pay} €`, true);
  showHub();
}

function showShop(){
  clearMain();
  $("mainTitle").textContent = "Courses — Marché local";
  const grid = document.createElement("div");
  grid.className = "shop-grid";
  FOODS.forEach(f => {
    const d = document.createElement("div");
    d.className = "item";
    d.innerHTML = `<h3>${f.emoji} ${f.name}</h3>
      <p>+${f.hunger} faim</p>
      <div class="price">${f.price} €</div>`;
    d.onclick = () => {
      if(state.money < f.price){ log("Pas assez d’argent."); return; }
      state.money -= f.price;
      state.inventory.push(f.id);
      log(`Acheté : ${f.name}`);
      updateBars();
    };
    grid.appendChild(d);
  });
  $("mainContent").appendChild(grid);
  const back = document.createElement("button");
  back.className = "btn sec";
  back.textContent = "← Retour";
  back.onclick = showHub;
  $("mainActions").appendChild(back);
}

function showEat(){
  clearMain();
  $("mainTitle").textContent = "Manger";
  if(!state.inventory.length){
    $("mainContent").innerHTML = `<p>Tu n’as rien à manger. Va faire les courses !</p>`;
  } else {
    const grid = document.createElement("div");
    grid.className = "shop-grid";
    // count items
    const counts = {};
    state.inventory.forEach(id => counts[id] = (counts[id]||0)+1);
    Object.keys(counts).forEach(id => {
      const f = FOODS.find(x => x.id === id);
      if(!f) return;
      const d = document.createElement("div");
      d.className = "item";
      d.innerHTML = `<h3>${f.emoji} ${f.name}</h3><p>x${counts[id]} · +${f.hunger} faim</p>`;
      d.onclick = () => {
        const idx = state.inventory.indexOf(id);
        if(idx >= 0) state.inventory.splice(idx,1);
        state.hunger = clamp(state.hunger + f.hunger);
        advanceTime(1);
        log(`Tu as mangé : ${f.name}`);
        updateBars();
        showEat();
      };
      grid.appendChild(d);
    });
    $("mainContent").appendChild(grid);
  }
  const back = document.createElement("button");
  back.className = "btn sec";
  back.textContent = "← Retour";
  back.onclick = showHub;
  $("mainActions").appendChild(back);
}

function showFurniture(){
  clearMain();
  $("mainTitle").textContent = "Meubles & déco";
  const grid = document.createElement("div");
  grid.className = "shop-grid";
  FURNITURE.forEach(f => {
    const owned = state.furniture.includes(f.id);
    const d = document.createElement("div");
    d.className = "item" + (owned ? " owned" : "");
    d.innerHTML = `<h3>${f.emoji} ${f.name}</h3>
      <p>${owned ? "Déjà possédé" : "Confort +"+f.confort}</p>
      <div class="price">${owned ? "✓" : f.price + " €"}</div>`;
    d.onclick = () => {
      if(owned) return;
      if(state.money < f.price){ log("Pas assez d’argent."); return; }
      state.money -= f.price;
      state.furniture.push(f.id);
      state.fun = clamp(state.fun + 8);
      log(`Acheté : ${f.name}`, true);
      updateBars();
      showFurniture();
    };
    grid.appendChild(d);
  });
  $("mainContent").appendChild(grid);
  const back = document.createElement("button");
  back.className = "btn sec";
  back.textContent = "← Retour";
  back.onclick = showHub;
  $("mainActions").appendChild(back);
}

function showNPCs(){
  clearMain();
  $("mainTitle").textContent = "Personnes présentes";
  const local = NPCs.filter(n => n.town === state.town);
  const grid = document.createElement("div");
  grid.className = "npc-grid";
  local.forEach(n => {
    const rel = state.relationships[n.id] || 0;
    const d = document.createElement("div");
    d.className = "item";
    d.innerHTML = `<h3>${n.emoji} ${n.name}</h3>
      <p>${n.trait} · ${n.age} ans</p>
      <p>Relation : ${rel}/100</p>`;
    d.onclick = () => showNPCActions(n);
    grid.appendChild(d);
  });
  $("mainContent").appendChild(grid);
  const back = document.createElement("button");
  back.className = "btn sec";
  back.textContent = "← Retour";
  back.onclick = showHub;
  $("mainActions").appendChild(back);
}

function showNPCActions(n){
  clearMain();
  const rel = state.relationships[n.id] || 0;
  $("mainTitle").textContent = `${n.emoji} ${n.name}`;
  $("mainContent").innerHTML = `<p>Relation actuelle : <b>${rel}/100</b></p>
    <p style="color:var(--muted)">${n.trait} · ${n.age} ans · ${TOWNS.find(t=>t.id===n.town).name}</p>`;

  const actions = [
    { label: "💬 Discuter", fn: () => interact(n, "talk") },
    { label: "😄 Blaguer", fn: () => interact(n, "joke") },
    { label: "❤️ Draguer", fn: () => interact(n, "flirt"), show: rel >= 20 },
    { label: "💋 Embrasser", fn: () => interact(n, "kiss"), show: rel >= 50 },
    { label: "👊 Se bagarrer", fn: () => interact(n, "fight") },
    { label: "← Retour", fn: showNPCs }
  ];
  actions.filter(a => a.show !== false).forEach(a => {
    const b = document.createElement("button");
    b.className = "btn sec";
    b.textContent = a.label;
    b.onclick = a.fn;
    $("mainActions").appendChild(b);
  });
}

function interact(n, type){
  let delta = 0;
  let msg = "";
  const rel = state.relationships[n.id] || 0;

  if(type === "talk"){
    delta = 8 + Math.floor(Math.random()*6);
    msg = `Tu discutes avec ${n.name}.`;
    state.social = clamp(state.social + 12);
  } else if(type === "joke"){
    delta = Math.random() > 0.3 ? 12 : -5;
    msg = delta > 0 ? `${n.name} rit de ta blague !` : `${n.name} n’a pas trouvé ça drôle…`;
    state.social = clamp(state.social + 8);
    state.fun = clamp(state.fun + 10);
  } else if(type === "flirt"){
    delta = state.trait === "romantique" ? 15 : 10;
    if(Math.random() < 0.25) delta = -8;
    msg = delta > 0 ? `Tu flirtes avec ${n.name}… ça a l’air de plaire.` : `${n.name} n’est pas réceptif(ve).`;
    state.social = clamp(state.social + 10);
  } else if(type === "kiss"){
    delta = 18;
    msg = `Tu embrasses ${n.name} ! 💕`;
    state.social = clamp(state.social + 15);
    state.fun = clamp(state.fun + 20);
  } else if(type === "fight"){
    delta = -25;
    msg = `Tu te bagarres avec ${n.name} !`;
    state.energy = clamp(state.energy - 20);
    state.social = clamp(state.social - 15);
    if(state.trait === "bagarreur") delta = -15;
  }

  state.relationships[n.id] = clamp(rel + delta);
  advanceTime(1);
  log(msg + ` (relation ${delta >= 0 ? "+" : ""}${delta})`, true);
  showNPCActions(n);
}

function doLeisure(){
  clearMain();
  $("mainTitle").textContent = "Loisirs";
  const options = [
    { name: "Aller à la plage", fun: 25, energy: -10, time: 2, emoji: "🏖️" },
    { name: "Randonnée", fun: 20, energy: -25, time: 3, emoji: "🥾" },
    { name: "Écouter de la musique", fun: 15, energy: 5, time: 1, emoji: "🎵" },
    { name: "Regarder la TV", fun: 12, energy: 5, time: 2, emoji: "📺" },
    { name: "Faire la sieste", fun: 5, energy: 30, time: 2, emoji: "😴" }
  ];
  const grid = document.createElement("div");
  grid.className = "shop-grid";
  options.forEach(o => {
    const d = document.createElement("div");
    d.className = "item";
    d.innerHTML = `<h3>${o.emoji} ${o.name}</h3>
      <p>Fun ${o.fun > 0 ? "+"+o.fun : o.fun} · Énergie ${o.energy > 0 ? "+"+o.energy : o.energy}</p>`;
    d.onclick = () => {
      state.fun = clamp(state.fun + o.fun);
      state.energy = clamp(state.energy + o.energy);
      state.hunger = clamp(state.hunger - 5);
      advanceTime(o.time);
      log(`Tu as fait : ${o.name}`);
      showHub();
    };
    grid.appendChild(d);
  });
  $("mainContent").appendChild(grid);
  const back = document.createElement("button");
  back.className = "btn sec";
  back.textContent = "← Retour";
  back.onclick = showHub;
  $("mainActions").appendChild(back);
}

function showTravel(){
  clearMain();
  $("mainTitle").textContent = "Voyager sur l’île";
  const grid = document.createElement("div");
  grid.className = "loc-grid";
  TOWNS.forEach(t => {
    if(t.id === state.town) return;
    const d = document.createElement("div");
    d.className = "item";
    d.innerHTML = `<h3>${t.emoji} ${t.name}</h3><p>${t.desc}</p><p style="color:var(--muted)">Coût : 15 € · 2h</p>`;
    d.onclick = () => {
      if(state.money < 15){ log("Pas assez d’argent pour le trajet."); return; }
      state.money -= 15;
      state.town = t.id;
      advanceTime(2);
      log(`Tu arrives à ${t.name}.`, true);
      showHub();
    };
    grid.appendChild(d);
  });
  $("mainContent").appendChild(grid);
  const back = document.createElement("button");
  back.className = "btn sec";
  back.textContent = "← Retour";
  back.onclick = showHub;
  $("mainActions").appendChild(back);
}

function doSleep(){
  state.energy = clamp(state.energy + 60);
  state.hunger = clamp(state.hunger - 10);
  advanceTime(8);
  log("Tu as dormi profondément.");
  showHub();
}

function saveGame(){
  localStorage.setItem("reunion_life_save", JSON.stringify(state));
  log("Partie sauvegardée !", true);
}

function loadGame(){
  try {
    const s = localStorage.getItem("reunion_life_save");
    if(s){
      state = JSON.parse(s);
      $("screen-create").classList.remove("active");
      $("screen-game").classList.add("active");
      updateBars();
      showHub();
      log("Partie chargée.", true);
    }
  } catch(e){}
}

// Auto-load if save exists
loadGame();
</script>
</body>
</html>
