---
tags: cyberia, cyber valley, strategy, tool
alias: annual leasehold, lease pricer, ground lease pricer, lease calculator
crystal-type: pattern
crystal-domain: cyberia
---
# annual leasehold

enter [[cyber valley]] with a deposit. the rest is held in [[century index]] quantities — fixed on day one, valued on the day you pay, never renegotiated at market.

one scheduled form of the same [[hak sewa]]:

| deposit | balance | if the balance is still open after a year |
|---|---|---|
| 30% at signing | the remaining 70% of the CX quantities, due within 12 months at their value on the payment date | 5 equal annual instalments of the same quantities, each valued on its due date |

on bali, land often wants full cash or rides ~9% a year. that builds flips, not businesses. here there is no rate and no fee: the balance is the index and nothing else, the same Annex E that prices the renewal.

[[hak sewa]] with the estate: build, live, sublet. after build — [[hak pakai]] with KITAS/KITAP, or [[hak milik]] if you are WNI. full cash today? [[leasehold upfront]].

arrears: 6 months to clear or to assign the lease. after that the Holder ceases and leaves the land. sums already paid stay as the price of the time held.

## price your deal

<div id="lcalc"></div>

<style>
#lcalc{color:#f0f0f0;font-family:var(--font-body,'Play',system-ui,sans-serif);width:min(640px,100%);margin:28px auto;padding:0}
#lcalc .panel{background:#0a0a0a;border:1px solid #222;border-radius:10px;padding:16px}
#lcalc h4{font-family:var(--font-mono,'JetBrains Mono',monospace);font-size:11px;color:#22c55e;letter-spacing:2.5px;text-transform:uppercase;margin:0 0 12px}
#lcalc label{font-size:12.5px;color:#8b948c;display:block;margin-bottom:4px}
#lcalc input[type=number]{width:100%;background:#111;border:1px solid #222;color:#f0f0f0;padding:8px;border-radius:6px;font-family:var(--font-mono,'JetBrains Mono',monospace)}
#lcalc .plans{display:flex;gap:8px;margin:12px 0}
#lcalc .plan{flex:1;padding:10px;border:1px solid #222;border-radius:8px;background:#0a0a0a;color:#8b948c;cursor:pointer;font-family:var(--font-mono,'JetBrains Mono',monospace);font-size:12px}
#lcalc .plan.on{color:#000;background:#22c55e;border-color:#22c55e}
#lcalc .stats{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:14px}
#lcalc .stat{background:#111;border:1px solid #222;border-radius:8px;padding:10px 12px}
#lcalc .stat .l{font-size:11px;color:#8b948c;margin-bottom:4px}
#lcalc .stat .v{font-family:var(--font-mono,'JetBrains Mono',monospace);font-size:17px}
#lcalc .note{font-size:12px;color:#8b948c;line-height:1.6;margin:12px 0 0}
</style>

<script>
(function(){
  const el=id=>document.getElementById(id);
  const state={price:100000,plan:"1"};
  const plans={
    "1":{years:1,deposit:0.30,fee:0,label:"30% down · balance in 12 months"},
    "5":{years:5,deposit:0.30,fee:0,label:"30% down · then 5 annual instalments"}
  };
  function fmt(n){return "$"+Math.round(n).toLocaleString("en-US")}
  function render(){
    const p=plans[state.plan];
    const total=state.price*(1+p.fee);
    const down=total*p.deposit;
    const rest=total-down;
    const per=rest/(p.years*12);
    el("st").innerHTML=
      "<div class=stat><div class=l>Pay now (deposit)</div><div class=v>"+fmt(down)+"</div></div>"+
      "<div class=stat><div class=l>Total you pay</div><div class=v>"+fmt(total)+"</div></div>"+
      "<div class=stat><div class=l>Balance</div><div class=v>"+fmt(rest)+"</div></div>"+
      "<div class=stat><div class=l>Equal monthly</div><div class=v>"+fmt(per)+"</div></div>";
    el("note").textContent="figures at today's CX level. the balance is held in CX quantities and is valued on the day you pay. arrears: 6 months to clear, then the Holder ceases.";
  }
  el("lcalc").innerHTML='<div class="panel"><h4>Scheduled hak sewa</h4><label>Plot price (upfront = 100%)</label><input id="price" type="number" min="10000" step="1000" value="100000"><div class="plans"><button type="button" class="plan on" data-plan="1">30% · balance in 12 months</button><button type="button" class="plan" data-plan="5">30% · then 5 annual</button></div><div class="stats" id="st"></div><p class="note" id="note"></p></div>';
  el("price").oninput=e=>{state.price=Math.max(10000,+e.target.value||0);render();};
  el("lcalc").querySelectorAll(".plan").forEach(b=>{
    b.onclick=()=>{state.plan=b.getAttribute("data-plan");el("lcalc").querySelectorAll(".plan").forEach(x=>x.classList.toggle("on",x===b));render();};
  });
  render();
})();
</script>

## legal form

[[hak sewa]] now; after build → [[hak pakai]] (KITAS/KITAP) or [[hak milik]] (WNI). skeleton: [[land-rights-agreement]]. scheduled terms: [[hak-sewa-deed]] §3.2.

indexed annual *rent* without a land right — occupation only — is B-rent, a separate form under deed 3.1, governed by the same [[annex-e-century-index|Annex E]]. this page is the scheduled purchase of the lease, the other of the two forms next to [[leasehold upfront]].
