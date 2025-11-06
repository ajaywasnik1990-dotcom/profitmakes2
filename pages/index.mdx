<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Profitmakes Algo — Dashboard</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body {background:#f8fafc;font-family:"Inter",Arial,sans-serif;margin:0;color:#111827;}
    header {background:linear-gradient(90deg,#4f46e5,#10b981);color:white;padding:18px 0;}
    header .container {max-width:1100px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;padding:0 16px;}
    .brand{font-size:22px;font-weight:800;}
    .index-box{background:rgba(255,255,255,0.15);padding:6px 10px;border-radius:6px;font-size:13px;text-align:center;}
    .index-input{width:80px;background:transparent;border:none;border-bottom:1px solid rgba(255,255,255,0.5);color:#fff;text-align:center;font-weight:600;font-size:13px;}
    .change-input{width:60px;background:transparent;border:none;text-align:center;font-weight:700;font-size:12px;margin-top:2px;color:#16a34a;}
    .change-input.red{color:#ef4444;}
    a.open-btn{background:#111827;color:white;padding:8px 14px;border-radius:8px;text-decoration:none;font-size:13px;}
    main{max-width:980px;margin:20px auto;padding:0 12px;}
    .card{background:#fff;padding:14px;border-radius:12px;box-shadow:0 2px 6px rgba(0,0,0,0.06);}
    .flex{display:flex;gap:12px;margin-bottom:12px;flex-wrap:wrap;}
    table{width:100%;border-collapse:collapse;font-size:13px;border:1px solid #e5e7eb;}
    th,td{padding:10px;text-align:left;border-bottom:1px solid #e5e7eb;}
    thead{background:#eef2ff;color:#374151;font-weight:600;}
    tr.profit td:last-child{color:#16a34a;font-weight:600;}
    tr.loss td:last-child{color:#dc2626;font-weight:600;}
    tbody tr:nth-child(even){background:#f9fafb;}
    tbody tr:hover{background:#e0f2fe;}
    .editable-input{border:none;border-bottom:1px solid #ccc;width:100px;text-align:center;font-weight:600;background:transparent;}
    #totalProfitDisplay{font-size:22px;font-weight:800;}
    .profit-green{color:#16a34a;}
    .profit-red{color:#dc2626;}
  </style>
</head>
<body>

<header>
  <div class="container">
    <div>
      <div class="brand">🚀 Profitmakes Algo</div>
      <div>Welcome, <input id="userName" class="index-input" value="Ajay"> 👋</div>
    </div>
    <div style="display:flex;align-items:center;gap:16px;flex-wrap:wrap;">
      <div class="index-box">NIFTY:<br><input id="niftyIndex" class="index-input" value="25780.50"><input id="niftyChange" class="change-input" value="+23.45"></div>
      <div class="index-box">BANKNIFTY:<br><input id="bankIndex" class="index-input" value="57625.40"><input id="bankChange" class="change-input" value="-120.75"></div>
      <a class="open-btn" href="https://ekyc.aliceblueonline.com/?source=EMPH2168/open-account/?c=YOUR_REF_CODE" target="_blank">OPEN DEMAT ACCOUNT</a>
    </div>
  </div>
</header>

<main>
  <div class="flex">
    <div class="card" style="flex:1">
      <div style="font-size:12px;color:#6b7280;">Investment Cost</div>
      <input id="investmentInput" class="editable-input" type="text" value="0"> ₹
    </div>
    <div class="card" style="width:240px;text-align:center;">
      <div style="font-size:12px;color:#6b7280;">Today's P&L</div>
      <div id="totalProfitDisplay">₹0.00</div>
    </div>
  </div>

  <section class="card">
    <h3 style="margin:0 0 12px 0;">PURE BUY STRATEGY</h3>
    <div class="flex">
      <input type="file" id="csvFile" accept=".csv">
      <input type="search" id="searchInput" placeholder="Search rows...">
    </div>
    <div id="tableContainer"></div>
  </section>
</main>

<script>
document.getElementById("csvFile").addEventListener("change", e => {
  const file = e.target.files[0];
  if (!file) return;
  const reader = new FileReader();
  reader.onload = ev => {
    const rows = ev.target.result.split("\n").map(r => r.split(",").map(c => c.trim()));
    renderTable(rows);
  };
  reader.readAsText(file);
});

function renderTable(rows) {
  if (!rows.length) return;
  const table = document.createElement("table");
  const thead = document.createElement("thead");
  const tbody = document.createElement("tbody");

  thead.innerHTML = "<tr>" + rows[0].map(h => `<th>${h}</th>`).join("") + "</tr>";
  table.appendChild(thead);

  let totalProfit = 0, totalInvestment = 0;
  const headers = rows[0].map(h => h.toLowerCase());

  const symbolIndex = headers.findIndex(h => h.includes("symbol"));
  const entryIndex = headers.findIndex(h => h.includes("entry") || h.includes("buy") || h.includes("price"));
  const qtyIndex = headers.findIndex(h => h.includes("qty") || h.includes("quantity") || h.includes("lot"));
  const profitIndex = headers.findIndex(h => h.includes("p&l") || h.includes("profit") || h.includes("pl"));

  for (let i = 1; i < rows.length; i++) {
    const cols = rows[i];
    if (!cols.length || cols.every(c => c === "")) continue;

    const tr = document.createElement("tr");
    const symbol = (cols[symbolIndex] || "").toUpperCase();
    const entry = parseFloat(cols[entryIndex]);
    const qty = parseFloat(cols[qtyIndex]);
    const profit = parseFloat(cols[profitIndex]);

    let lotSize = 1;
    if (symbol.includes("BANKNIFTY")) lotSize = 15;
    else if (symbol.includes("NIFTY")) lotSize = 50;

    if (!isNaN(entry) && !isNaN(qty)) {
      totalInvestment += entry * qty * lotSize;
    }

    if (!isNaN(profit)) {
      totalProfit += profit;
      tr.classList.add(profit >= 0 ? "profit" : "loss");
    }

    tr.innerHTML = cols.map(c => `<td>${c}</td>`).join("");
    tbody.appendChild(tr);
  }

  table.appendChild(tbody);
  const container = document.getElementById("tableContainer");
  container.innerHTML = "";
  container.appendChild(table);

  document.getElementById("totalProfitDisplay").textContent = "₹" + totalProfit.toFixed(2);
  document.getElementById("totalProfitDisplay").className = totalProfit >= 0 ? "profit-green" : "profit-red";
  document.getElementById("investmentInput").value = Math.round(totalInvestment).toLocaleString();

  document.getElementById("searchInput").addEventListener("input", function () {
    const query = this.value.toLowerCase();
    tbody.querySelectorAll("tr").forEach(tr => {
      const match = [...tr.children].some(td => td.textContent.toLowerCase().includes(query));
      tr.style.display = match ? "" : "none";
    });
  });
}

function updateChangeColor(id) {
  const el = document.getElementById(id);
  el.classList.toggle('red', el.value.trim().startsWith('-'));
}
updateChangeColor('niftyChange');
updateChangeColor('bankChange');
</script>

</body>
</html>
