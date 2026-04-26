<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,15,18,20,25&height=250&section=header&text=V2Ray%20WebSocket%20Tunnel&fontSize=52&fontAlignY=38&desc=Déploiement%20sur%20Google%20Cloud%20Run&descAlignY=58&descSize=20&animation=fadeIn" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&duration=3500&pause=500&color=2E9FFF&center=true&vCenter=true&width=600&lines=⚡+Connexion+sécurisée+et+ultra+rapide;🔒+Tunnel+WebSocket+V2Ray;☁️+Déploiement+serverless;🌍+Accessible+depuis+n'importe+où" alt="Typing Animation" />
</p>

<br/>

<!---
<div align="center">
--->

# 🌟 Proxy Nginx pour VPS 🌟

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-Supported-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Google Cloud Run](https://img.shields.io/badge/Google_Cloud_Run-Deployed-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-Proxy-009639?style=for-the-badge&logo=nginx&logoColor=white)

</div>

---

## 🚀 **Redirection TCP haute performance vers VPS principal**

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&duration=3000&pause=500&color=00FF00&center=true&vCenter=true&width=600&lines=Déployé+sur+Google+Cloud+Run;Haute+disponibilité+garantie;Low+latency+%26+haute+performance" alt="Typing Animation" />
</div>

---

## 📊 **Configuration Technique**

<table align="center">
  <tr>
    <td align="center"><b>🎯 VPS Cible</b></td>
    <td><code>207.126.161.196:443</code></td>
  </tr>
  <tr>
    <td align="center"><b>🔌 Port d'écoute</b></td>
    <td><code>8080</code></td>
  </tr>
  <tr>
    <td align="center"><b>🌍 Région VPS</b></td>
    <td>🇬🇧 europe-west2 (Londres)</td>
  </tr>
  <tr>
    <td align="center"><b>☁️ Région Cloud Run</b></td>
    <td>🇬🇧 europe-west2 (Londres)</td>
  </tr>
  <tr>
    <td align="center"><b>⚡ Type</b></td>
    <td>TCP Stream (Layer 4)</td>
  </tr>
</table>

---

## 🛠️ **Déploiement**

<div align="center">

```bash
gcloud run deploy ultra-speed-proxy \
  --source . \
  --platform managed \
  --region europe-west2 \
  --allow-unauthenticated \
  --port 8080 \
  --memory 512Mi \
  --cpu 1 \
  --timeout 3600
```

</div>

---

## 📊 **Configuration Technique**

<table align="center">
  <tr>
    <td align="center"><b>🎯 VPS Cible</b></td>
    <td><code>207.126.161.196:443</code></td>
  </tr>
  <tr>
    <td align="center"><b>🔌 Port d'écoute</b></td>
    <td><code>8080</code></td>
  </tr>
  <tr>
    <td align="center"><b>🌍 Région VPS</b></td>
    <td>🇬🇧 europe-west2 (Londres)</td>
  </tr>
  <tr>
    <td align="center"><b>☁️ Région Cloud Run</b></td>
    <td>🇬🇧 europe-west2 (Londres)</td>
  </tr>
  <tr>
    <td align="center"><b>⚡ Type</b></td>
    <td>TCP Stream (Layer 4)</td>
  </tr>
</table>

---

🌊 ARCHITECTURE DU FLUX

<div align="center">

```mermaid
flowchart LR
    A[👤 CLIENT] -->|Requête| B[☁️ CLOUD RUN<br/>Port: 8080]
    B -->|TCP Stream| C[🖥️ VPS PRINCIPAL<br/>Port: 443]
    C -->|Réponse| B
    B -->|Réponse| A
    
    style A fill:#4CAF50,stroke:#2E7D32,stroke-width:3px,color:#fff
    style B fill:#2196F3,stroke:#0D47A1,stroke-width:3px,color:#fff
    style C fill:#FF9800,stroke:#E65100,stroke-width:3px,color:#fff
```

</div>

<br>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&duration=1500&pause=300&color=00FF00&center=true&vCenter=true&width=600&lines=📦+Client+→+Cloud+Run+:8080;⚡+Cloud+Run+→+VPS+:443;💨+VPS+:443+→+Cloud+Run;✅+Cloud+Run+→+Client" alt="Flow Animation">
</div>

<br>

📈 STATUT & MONITORING

<div align="center">
  <img src="https://img.shields.io/badge/UPTIME-99.99%25-brightgreen?style=flat-square&logo=statuspage">
  <img src="https://img.shields.io/badge/RESPONSE_TIME-%3C50ms-brightgreen?style=flat-square&logo=clockify">
  <img src="https://img.shields.io/badge/ACTIVE_CONNECTIONS-24%2F7-success?style=flat-square&logo=cloudflare">
</div>

<br>


🎯 COMMENT ÇA MARCHE ?

<div align="center">

```mermaid
sequenceDiagram
    participant C as 👤 Client
    participant CR as ☁️ Cloud Run (:8080)
    participant V as 🖥️ VPS (:443)
    
    C->>CR: 1. Connexion TCP
    CR->>V: 2. Proxy TCP Stream
    V-->>CR: 3. Réponse
    CR-->>C: 4. Transmission
```

</div>

<br>

---

📈 Statut & Monitoring

<div align="center">

https://img.shields.io/badge/uptime-99.99%25-brightgreen?style=flat-square
https://img.shields.io/badge/response_time-<50ms-brightgreen?style=flat-square
https://img.shields.io/badge/status-active-success?style=flat-square

</div>
---

⭐ N'hésitez pas à laisser une étoile si ce projet vous est utile ! ⭐

</div>

---

<br/>

🤝 Contribution

Les contributions sont les bienvenues !

1. Fork le projet
2. Crée ta branche (git checkout -b feature/AmazingFeature)
3. Commit tes changements (git commit -m 'Add AmazingFeature')
4. Push la branche (git push origin feature/AmazingFeature)
5. Ouvre une Pull Request

<br/>

📝 Licence

Distribué sous licence MIT. Voir LICENSE pour plus d'informations.

<br/>

👨‍💻 Auteur

WorldSolutionRdc

· GitHub: @WorldSolutionRdc
· Email: worldsolutiontv@gmail.com

<br/>

🙏 Remerciements

· PANCHO7532 - Proxy Bridge original
· BadVPN - Tunneling UDP/TCP
· stunnel - Couche TLS/SSL
· Dropbear - Serveur SSH léger
· Google Cloud Run - Infrastructure serverless

<br/>

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer" />
</p>
