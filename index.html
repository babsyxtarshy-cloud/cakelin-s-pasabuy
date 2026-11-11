<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Cakelin’s Longchamp Pasabuy</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@500;700;800&family=Quicksand:wght@700&display=swap" rel="stylesheet">
<style>
:root{--bg:#fdf4f0;--card:#ffffff;--ink:#5a3e38;--muted:#8f6f67;--acc:#e89bb0;--acc-deep:#a4566e;--ok:#d9a3b5;--line:#f0d5cc;--tint:#fbe5e9;color-scheme:light;box-sizing:border-box}
*,*::before,*::after{box-sizing:inherit}
body{margin:0;background:var(--bg);color:var(--ink);font:500 18px/1.6 "Nunito",system-ui,-apple-system,"Segoe UI",sans-serif;padding:env(safe-area-inset-top,0px) 0 env(safe-area-inset-bottom,0px)}
main{max-width:560px;margin:0 auto;padding:40px 22px 64px}
h1,h3,.lbl{font-family:"Quicksand","Nunito",system-ui,sans-serif;font-weight:700;line-height:1.2;margin:0 0 12px;color:var(--acc-deep)}
h1{font-size:clamp(34px,9vw,46px)} h3{font-size:21px;margin-bottom:8px;color:var(--ink)}
p{margin:0 0 14px}.muted{color:var(--muted)}
.lbl{font-size:15px;text-transform:uppercase;letter-spacing:.08em;margin:6px 0}
input{width:100%;font:700 19px "Nunito",system-ui,sans-serif;letter-spacing:.08em;padding:15px 16px;border-radius:16px;border:2px solid var(--line);background:var(--card);color:var(--ink);margin-bottom:8px;text-transform:uppercase}
.btn{display:block;width:100%;background:var(--acc);color:#4a2a2f;border:0;border-radius:18px;font:800 18px "Nunito",system-ui,sans-serif;padding:15px 20px;min-height:52px;cursor:pointer;text-align:center;text-decoration:none;box-shadow:0 4px 0 #cf8197}
.btn.alt{background:var(--card);color:var(--acc-deep);border:2px solid var(--line);box-shadow:none;margin-top:12px}
.back{background:none;border:0;color:var(--muted);font:700 16px "Nunito",sans-serif;padding:14px 0;cursor:pointer}
button:focus-visible,a:focus-visible,input:focus-visible{outline:3px solid var(--acc);outline-offset:2px}
.err{color:var(--acc-deep);font-weight:800;min-height:24px;margin:0 0 8px}
.card{background:var(--card);border:2px solid var(--line);border-radius:22px;padding:20px;margin-bottom:14px}
.sum{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin:0 0 16px}
.sum div{background:var(--tint);border-radius:18px;padding:12px 8px;text-align:center}
.sum span{display:block;font-size:14px;color:var(--muted);font-weight:700}
.sum b{font-size:19px;font-family:"Quicksand",sans-serif}
.choices{list-style:none;margin:0 0 12px;padding:0;display:grid;gap:6px}
.choices li{background:var(--tint);border-radius:14px;padding:8px 12px;font-weight:700}
.choices span{color:var(--acc-deep);font-size:14px;margin-right:6px}
.row{display:flex;justify-content:space-between;gap:12px;padding:8px 0;border-top:1px dashed var(--line)}
.note{background:var(--tint);border-radius:14px;padding:10px 14px;margin:10px 0 0;font-weight:700;font-size:16px;color:var(--ink)}
.st{list-style:none;margin:0;padding:0}
.st li{position:relative;padding:6px 0 6px 32px;color:var(--muted);font-size:16px;font-weight:600}
.st li::before{content:"";position:absolute;left:0;top:11px;width:18px;height:18px;border-radius:50%;border:2px solid var(--line);background:var(--card)}
.st li.done{color:var(--ink)} .st li.done::before{background:var(--ok);border-color:var(--ok)}
.st li.cur{color:var(--acc-deep);font-weight:800} .st li.cur::before{border-color:var(--acc-deep);background:var(--acc)}
</style>
</head>
<body>
<main id="app"></main>

<script>
/* ============================================================
   SETUP: paste your two values between the quotes below.
   Project URL looks like: https://abcdwxyz.supabase.co
   Anon key is a long string starting with: eyJ...
   ============================================================ */
const SUPABASE_URL = "https://bhvrvlykrxaxryiktnoa.supabase.co";
const SUPABASE_KEY = "sb_publishable_Qwibu4XpIyeIymhBURX8zg_-ry0J460";

const MSG = "https://www.facebook.com/share/1CCPXzw6fN/?mibextid=wwXIfr";
const STAGES = ["Reserved","Down payment received","Bought in Italy","Packed for travel","Arrived in the Philippines","Ready for pickup or delivery","Completed"];

const app = document.getElementById("app");

function esc(s){ return String(s == null ? "" : s).replace(/[&<>"]/g, c => ({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c])); }
function php(n){ return "₱" + Number(n || 0).toLocaleString("en-PH"); }

async function fetchOrder(code){
  const res = await fetch(SUPABASE_URL + "/rest/v1/rpc/get_my_order", {
    method: "POST",
    headers: { "apikey": SUPABASE_KEY, "Content-Type": "application/json" },
    body: JSON.stringify({ p_code: code })
  });
  if (!res.ok) throw new Error("Server error");
  return await res.json(); // returns the order, or null if the code doesn't match
}

function loginScreen(message){
  window.scrollTo(0,0);
  app.innerHTML =
    '<p class="lbl">Track your order</p>' +
    '<h1>Cakelin’s Longchamp Pasabuy</h1>' +
    '<input type="text" id="code" placeholder="Access code" autocapitalize="characters" autocomplete="off">' +
    '<p class="err" id="err">' + esc(message || "") + '</p>' +
    '<button class="btn" onclick="lookup()">View my order</button>' +
    '<p class="muted" style="font-size:15px;margin-top:18px">No code yet? Message me and I’ll send one once your order is reserved.</p>' +
    '<a class="btn alt" href="' + MSG + '">Message me</a>';
}

async function lookup(){
  const el = document.getElementById("err");
  const code = (document.getElementById("code").value || "").toUpperCase().replace(/[^A-Z0-9]/g, "");
  if (code.length < 10) { el.textContent = "Enter your 10-character access code."; return; }
  el.textContent = "Checking…";
  try {
    const order = await fetchOrder(code);
    if (!order) { loginScreen("That code doesn’t match. Check it and try again."); return; }
    showOrder(order);
  } catch (e) {
    loginScreen("Couldn’t open that code. Check your connection and try again.");
  }
}

function showOrder(o){
  window.scrollTo(0,0);
  const items = o.items || [];
  let total = 0, paid = 0;
  items.forEach(i => { total += (i.price || 0) * (i.qty || 1); paid += i.paid || 0; });

  const colors = (o.colors || []).length
    ? '<p class="lbl" style="font-size:14px">Color choices</p><ol class="choices">' +
      o.colors.map((c, k) => '<li><span>' + ["1st","2nd","3rd","4th"][k] + ' choice</span>' + esc(c) + '</li>').join('') + '</ol>'
    : '';

  const info = '<div class="row"><span>Size</span><b>' + esc(o.size || "-") + '</b></div>' +
    '<div class="row"><span>Where I’ll buy</span><b>' + esc(o.where_to_buy || "-") + '</b></div>' +
    '<div class="row"><span>Stamping</span><b>' + esc(o.stamping || "None") + '</b></div>';

  const itemCards = items.map(i => {
    const q = i.qty || 1;
    const steps = STAGES.map((s, k) => '<li class="' + (k < i.stage ? 'done' : (k == i.stage ? 'cur' : '')) + '">' + s + '</li>').join('');
    return '<div class="card"><h3>' + esc(i.name) + '</h3>' +
      '<p class="muted" style="margin:0 0 8px">' + (q > 1 ? '×' + q + ' · ' : '') + php((i.price || 0) * q) + '</p>' +
      '<ol class="st">' + steps + '</ol>' +
      '<p class="muted" style="font-size:14px;margin:10px 0 0">Updated ' + esc(i.updated || "") + '</p></div>';
  }).join('');

  const plan = o.payment_plan || {};
  const planRows = (plan.lines || []).map(l => '<div class="row"><span>' + esc(l[0]) + '</span><b>' + esc(l[1]) + '</b></div>').join('');
  const planNotes = (plan.notes || []).map(n => '<p class="note">' + esc(n) + '</p>').join('');

  app.innerHTML =
    '<p class="lbl">Cakelin’s Longchamp Pasabuy</p>' +
    '<h1>Hi, ' + esc(o.buyer_name) + '</h1>' +
    '<div class="sum"><div><span>Total</span><b>' + php(total) + '</b></div><div><span>Paid</span><b>' + php(paid) + '</b></div><div><span>Balance</span><b>' + php(total - paid) + '</b></div></div>' +
    '<div class="card"><h3>Your choices</h3>' + info + colors +
      (o.buyer_note ? '<p class="note"><b>Note from buyer:</b> ' + esc(o.buyer_note) + '</p>' : '') + '</div>' +
    itemCards +
    '<div class="card"><h3>Payment plan</h3>' +
      (plan.due ? '<p class="muted" style="margin:4px 0 10px">Payment due: ' + esc(plan.due) + '</p>' : '') +
      planRows + planNotes + '</div>' +
    '<div class="card"><h3>Shipping and perks</h3>' +
      '<div class="row"><span>Perks</span><b>' + esc(o.perks || "None") + '</b></div>' +
      '<div class="row"><span>Shipping</span><b>' + esc(o.shipping || "TBA") + '</b></div></div>' +
    '<a class="btn alt" href="' + MSG + '">Message me</a>' +
    '<button class="back" onclick="loginScreen()">Log out</button>';
}

loginScreen();
</script>
</body>
</html>
