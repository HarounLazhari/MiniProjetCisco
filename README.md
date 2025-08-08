# 🚀  NetSolutions – Maquette Réseau Cisco

> **Packet Tracer 8.2+** · VLAN · Wi-Fi · DHCP/DNS · WebServer · Router-on-a-Stick

Une démo complète d’un petit réseau d’entreprise : trois équipes isolées par VLAN **et** par SSID, un routeur qui fait le routage inter-VLAN, un serveur Web/DNS, le tout sous Cisco Packet Tracer.  
Cloner, ouvrir, tester… c’est prêt !

---

## 📦 Ce repo contient :

```
packet-tracer/      →  NetSolutions_v1.pkt
configs/            →  exports CLI (router, switch, AP, serveurs)
docs/               →  cahier des charges, plan d’adressage, guide de tests
captures/           →  pings, nslookup, page Web pour preuve visuelle
```

---

## 🗺️ Aperçu de l’architecture

| Équipe / service | VLAN | Sous-réseau | SSID | Clé Wi-Fi |
|------------------|------|-------------|------|-----------|
| Dév              | 10   | 192.168.10.0/24 | Dev-WiFi | **Dev2025!** |
| Marketing        | 20   | 192.168.20.0/24 | Mkt-WiFi | **Mkt2025!** |
| RH               | 30   | 192.168.30.0/24 | RH-WiFi  | **Rh2025!** |
| Serveurs         | 40   | 192.168.2.0/24  | — | — |

> Le routeur 2911 est passerelle (.1) pour chaque VLAN et héberge le DHCP.  
> Le serveur **192.168.2.2** fait DNS + HTTP.

---

## ⚡ Tester en 3 commandes

```bash
# 1. Cloner
git clone https://github.com/ton-user/projet-reseau.git
cd projet-reseau

# 2. Ouvrir le .pkt dans Packet Tracer (double-clic)
# 3. Suivre docs/Guide_de_tests.md  ➜  tout doit passer au vert ✅
```

---

## ✨ Fonctionnalités clés

- **VLAN + Wi-Fi** : isolation par câble et par ondes  
- **Router-on-a-Stick** : sous-interfaces dot1Q (.10 / .20 / .30 / .40)  
- **DHCP** : pools automatiques, exclusions, DNS poussé aux clients  
- **DNS interne** : `webserver.company.local` résout en **192.168.2.2**  
- **HTTP** : petite page “Welcome” pour valider l’accès depuis chaque VLAN  
- **Docs & captures** : tout est prouvé (pings, nslookup, navigateur)  

---

## 🎓 Compétences mises en avant

- Conception d’un plan d’adressage & d’un schéma VLAN  
- Configuration Cisco IOS : switch 2960 & routeur 2911  
- Wi-Fi sécurisé (WPA2/WPA3, mappage SSID ↔ VLAN)  
- Dépannage : `show *`, ping, traceroute, nslookup  
- Documentation technique + gestion de projet sous **Git / Git LFS**

---


