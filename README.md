---


---

<h1 id="b1-réseau-2018---tp">B1 Réseau 2018 - TP</h1>
<h4 id="utilisez-une-commande-pour-prouver-que-vous-avez-internet-depuis-la-vm.">Utilisez une commande pour prouver que vous avez internet depuis la VM.</h4>
<p><code>curl google.com -L</code></p>
<h4 id="prouvez-que-votre-pc-hôte-et-la-vm-peuvent-communiquer.">Prouvez que votre PC hôte et la VM peuvent communiquer.</h4>
<p>Sachant que l’ip du PC hôte est : <strong>192.168.127.1</strong><br>
et que l’ip de la VM est : <strong>192.168.127.10</strong><br>
On peux prouver que la PC hôte et la VM peuvent communiquer en faisant un ping entre les 2 machines.</p>
<p>Sur le PC hôte :<br>
<code>Ping 192.168.127.10</code></p>
<p><em>Résultat</em></p>
<p>Sur la VM :<br>
<code>ping 192.168.127.1</code></p>
<p><em>Résultat</em></p>
<h4 id="affichez-votre-table-de-routage-sur-la-vm-et-expliquez-chacune-des-lignes.">Affichez votre table de routage <strong>sur la VM</strong> et expliquez chacune des lignes.</h4>
<p><code>ip route</code></p>

