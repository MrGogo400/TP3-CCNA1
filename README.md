---


---

<h1 id="b1-réseau-2018---tp">B1 Réseau 2018 - TP</h1>
<h2 id="utilisez-une-commande-pour-prouver-que-vous-avez-internet-depuis-la-vm.">Utilisez une commande pour prouver que vous avez internet depuis la VM.</h2>
<p><code>curl -SL google.com</code></p>
<p><img src="https://github.com/MrGogo400/TP3-CCNA1/blob/master/images/centos-curl-google.png?raw=true" alt="enter image description here"></p>
<p>Cette commande va afficher le code source de la page demander.<br>
En encadré on retrouve le texte <code>Recherche Google</code> qui provient du bouton pour faire une recherche google, ce qui prouve que la VM a internet.</p>
<h2 id="prouvez-que-votre-pc-hôte-et-la-vm-peuvent-communiquer.">Prouvez que votre PC hôte et la VM peuvent communiquer.</h2>
<p>Sachant que l’ip du PC hôte est : <strong>192.168.127.1</strong><br>
et que l’ip de la VM est : <strong>192.168.127.10</strong><br>
On peux prouver que la PC hôte et la VM peuvent communiquer en faisant un ping entre les 2 machines.</p>
<p>Sur le PC hôte :<br>
<code>Ping 192.168.127.10</code></p>
<hr>
<pre><code>Envoi d’une requête 'Ping'  192.168.127.10 avec 32 octets de données :
Réponse de 192.168.127.10 : octets=32 temps&lt;1ms TTL=64
Réponse de 192.168.127.10 : octets=32 temps&lt;1ms TTL=64
Réponse de 192.168.127.10 : octets=32 temps&lt;1ms TTL=64
Réponse de 192.168.127.10 : octets=32 temps&lt;1ms TTL=64

Statistiques Ping pour 192.168.127.10:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 0ms, Maximum = 0ms, Moyenne = 0ms
</code></pre>
<p>Sur la VM :</p>
<p><code>ping 192.168.127.1</code></p>
<hr>
<pre><code>PING 192.168.12?.1 (192.168.127.1) 56(84) bytes of data.

4 bytes from 192.168.127.1: icmp_seq=1 ttl=128 time=0.273 ms
4 bytes from 192.168.127.1: icmp_seq=2 ttl=128 time=0.816 ms
4 bytes from 192.168.127.1: icmp_seq=3 ttl=128 time=0.883 ms
4 bytes from 192.168.127.1: icmp_seq=4 ttl=128 time=0.767 ms

--- 192.168.127.1 ping statistics ---

4 packets transmitted, 4 received, 0% packet loss, time 3009ms
rtt min/avg/max/mdev = 0.273/0.684/0.883/0.243 ms
</code></pre>
<h2 id="affichez-votre-table-de-routage-sur-la-vm-et-expliquez-chacune-des-lignes.">Affichez votre table de routage <strong>sur la VM</strong> et expliquez chacune des lignes.</h2>
<p><code>ip route</code></p>
<hr>
<pre><code>default via 10.0.2.2 dev enp0s3 proto dhcp metric 100

10.0.2.0/24 dev enp0s3 proto kernel scope link src 10.0.2.15 metric 100
192.168.127.8/24 dev enp0s8 proto kernel scope link src 192.168.127.10 metric 10
</code></pre>
<p>La première ligne :</p>
<pre><code>default via 10.0.2.2 dev enp0s3 proto dhcp metric 100 
</code></pre>
<p>Elle montre que enp0s3 est utiliser par défaut</p>
<p>2 ème ligne :</p>
<pre><code>10.0.2.0/24 dev enp0s3 proto kernel scope link src 10.0.2.15 metric 100
</code></pre>
<p>3 ème ligne :</p>
<pre><code>192.168.127.8/24 dev enp0s8 proto kernel scope link src 192.168.127.10 metric 10
</code></pre>
<h2 id="faire-joujou-avec-quelques-commandes">5. Faire joujou avec quelques commandes</h2>

