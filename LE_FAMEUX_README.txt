---
INFOS ET PREREQUIS :
---
Ce projet en langage C est de niveau intermédiaire/avancé. Il demande de bonnes connaissances en réseau et spécifiquement en modèle OSI.
Il a été utilisé sous Linux uniquement.
Il est séparé en fichiers sources traitant des couches OSI différentes : transport, réseau, liaison de données, etc...
Il convient au préalable d'installer les bibliothèques pcap : 
sudo apt install libpcap-dev

---
UTILISATION :
---
Pour le lancer (en étant dans le bon dossier) :
make
sudo ./sniffer [-i <interface> -o <fichier> -f <filtre BPF>]

---
EXEMPLES :
---
sudo ./sniffer // mode par défaut
sudo ./sniffer -i lo // choisit l'interface loopback pour la capture
sudo ./sniffer -f "tcp and dst port 80" // filtre le trafic pour HTTP uniquement
sudo ./sniffer -o monfichier.pcap // utilise un fichier .pcap à la place

---
PISTES D'AMELIORATION :
---
-Vous pouvez prendre en compte plus de protocoles (selon vos préférences)
-Vous pouvez ajouter une option pour exporter les résultats dans un fichier
-Vous pouvez ajouter des fonctionnalités
-Vous pouvez tenter de le porter sur une interface graphique (avancé)
-Vous pouvez le recopier dans un autre langage de programmation
-etc...!

