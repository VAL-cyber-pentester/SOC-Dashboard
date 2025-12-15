# 📊 SOC Dashboard Interactif

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Live](https://img.shields.io/badge/Demo-Live-success?style=for-the-badge)

Dashboard de supervision de sécurité en temps réel avec visualisations interactives et alertes dynamiques.

🌐 **[DÉMO EN LIGNE](https://val-cyber-pentester.github.io/SOC-Dashboard/soc-dashboard.html)**

---

## 🎯 Objectif

Créer une interface de supervision SOC (Security Operations Center) moderne et intuitive permettant de visualiser en temps réel les événements de sécurité, les alertes et les statistiques de menaces.

---

## ✨ Fonctionnalités

### 📈 Visualisations Temps Réel

#### 🔴 Compteurs Dynamiques
- **Événements totaux** avec évolution
- **Alertes critiques** en cours
- **Menaces bloquées** aujourd'hui
- **Score de sécurité** global (0-100)

#### 📊 Graphiques Interactifs
- **Timeline des événements** (dernières 24h)
- **Top 10 IPs suspectes** (graphique en barres)
- **Répartition des attaques** (camembert)
- **Événements par criticité** (donut chart)

### 🚨 Système d'Alertes

#### Alertes en Temps Réel
- **Couleurs par criticité :**
  - 🔴 Critique (rouge)
  - 🟠 Élevée (orange)
  - 🟡 Moyenne (jaune)
  - 🔵 Info (bleu)
- **Informations détaillées :**
  - Type d'alerte
  - Source (IP/hostname)
  - Timestamp précis
  - Description de la menace

#### Notifications
- **Badge de compteur** (nouvelles alertes)
- **Animation** lors de nouvelles alertes
- **Son** configurable (optionnel)
- **Historique** scrollable

### 📋 Logs de Sécurité

#### Tableau Dynamique
- **Filtres** par type, criticité, source
- **Recherche** en temps réel
- **Tri** par colonne
- **Pagination** automatique
- **Export** CSV/JSON

#### Types de Logs
- Tentatives d'intrusion (SSH, RDP)
- Scans de ports (Nmap, Masscan)
- Malware détectés
- Accès non autorisés
- Activités suspectes

### 🎨 Design Moderne

#### Glassmorphism
- Effet de verre dépoli
- Transparence et blur
- Ombres subtiles
- Animations fluides

#### Dark Theme
- Réduit la fatigue oculaire
- Contraste optimisé
- Accent sur les données importantes
- Mode clair (optionnel)

#### Responsive
- Adapté aux écrans 4K
- Optimisé pour tablettes
- Compatible mobile
- Grille flexible

---

## 🚀 Installation & Utilisation

### Option 1 : Démo en Ligne (Immédiat)

**Accéder directement à :** https://val-cyber-pentester.github.io/SOC-Dashboard/soc-dashboard.html

### Option 2 : Installation Locale

```bash
# Cloner le repository
git clone https://github.com/VAL-cyber-pentester/SOC-Dashboard.git
cd SOC-Dashboard

# Ouvrir dans un navigateur
# Windows
start soc-dashboard.html

# Linux/Mac
open soc-dashboard.html
```

Aucune dépendance nécessaire ! Pure HTML/CSS/JavaScript.

---

## 🛠️ Structure du Code

```
SOC-Dashboard/
├── soc-dashboard.html    # Page principale
├── README.md             # Documentation
└── screenshots/          # Captures d'écran
    ├── main-view.png
    ├── alerts.png
    └── graphs.png
```

### Architecture Front-End

```javascript
// Génération de données simulées
function generateMockData() {
    // Simulation réaliste de menaces
    // IPs aléatoires, types d'attaques variés
    // Distribution réaliste des criticités
}

// Mise à jour temps réel
setInterval(() => {
    updateCounters();
    updateCharts();
    addNewAlert();
    updateLogTable();
}, 3000); // Toutes les 3 secondes
```

---

## 📊 Données Simulées

### Types d'Attaques Simulées

| Type | Description | Fréquence |
|------|-------------|-----------|
| **SSH Brute Force** | Tentatives de connexion multiples | Haute |
| **Port Scanning** | Scan Nmap/Masscan détecté | Moyenne |
| **SQL Injection** | Tentative d'injection SQL | Moyenne |
| **XSS Attempt** | Tentative de Cross-Site Scripting | Basse |
| **Malware Download** | Téléchargement de fichier malveillant | Basse |
| **DDoS Attack** | Déni de service distribué | Très basse |

### IPs Suspectes Simulées

Génération aléatoire d'IPs avec :
- Géolocalisation approximative
- Nombre de tentatives
- Type d'attaque préférentiel
- Niveau de menace

---

## 🎓 Ce Que J'ai Appris

### Compétences Techniques

#### Front-End Development
- ✅ **HTML5** sémantique et structuré
- ✅ **CSS3** avancé (Grid, Flexbox, animations)
- ✅ **JavaScript** moderne (ES6+)
- ✅ **Visualisation de données** (Chart.js)
- ✅ **Design responsive** mobile-first
- ✅ **Performance** et optimisation

#### Design UI/UX
- ✅ **Glassmorphism** et tendances modernes
- ✅ **Color theory** pour dashboards
- ✅ **Hiérarchie visuelle** des informations
- ✅ **Accessibilité** (WCAG guidelines)
- ✅ **Micro-interactions** et feedback

### Concepts SOC

#### Supervision de Sécurité
- ✅ Types d'événements de sécurité
- ✅ Classification des alertes par criticité
- ✅ Indicateurs clés (KPI) d'un SOC
- ✅ Visualisation de données de sécurité
- ✅ Workflow d'analyse d'incident

#### Détection de Menaces
- ✅ Signatures d'attaques courantes
- ✅ Comportements suspects
- ✅ Corrélation d'événements
- ✅ Priorisation des alertes

---

## 🎨 Personnalisation

### Modifier les Couleurs

```css
:root {
    --primary: #00d4ff;      /* Bleu cyan */
    --critical: #ff4757;     /* Rouge critique */
    --high: #ffa502;         /* Orange élevé */
    --medium: #ffd32a;       /* Jaune moyen */
    --low: #1e90ff;          /* Bleu bas */
}
```

### Ajouter des Types d'Alertes

```javascript
const alertTypes = [
    'SSH Brute Force',
    'Port Scanning',
    'SQL Injection',
    'Custom Attack Type' // Nouveau type
];
```

### Modifier la Fréquence de Mise à Jour

```javascript
// De 3 secondes à 5 secondes
setInterval(updateDashboard, 5000);
```

---

## 🔌 Intégration avec Données Réelles

### Option 1 : API Backend

```javascript
async function fetchRealData() {
    const response = await fetch('/api/security/events');
    const data = await response.json();
    updateDashboard(data);
}
```

### Option 2 : WebSocket (Temps Réel)

```javascript
const ws = new WebSocket('ws://your-soc-server:8080');
ws.onmessage = (event) => {
    const alert = JSON.parse(event.data);
    addAlert(alert);
};
```

### Option 3 : Elasticsearch/Kibana Integration

```javascript
// Connexion à Elasticsearch
fetch('http://elasticsearch:9200/security-logs/_search', {
    method: 'POST',
    body: JSON.stringify({ query: {...} })
});
```

---

## 📈 Métriques Affichées

### Compteurs Principaux
- **Événements totaux** : Volume global d'événements
- **Alertes actives** : Alertes nécessitant une action
- **Menaces bloquées** : Attaques stoppées avec succès
- **Score de sécurité** : Santé globale (0-100)

### Graphiques
- **Timeline** : Évolution temporelle des événements
- **Top IPs** : Sources principales d'attaques
- **Répartition** : Distribution par type d'attaque
- **Criticité** : Proportion des niveaux de risque

---

## 🚀 Évolutions Futures

### Fonctionnalités Planifiées
- [ ] **Intégration SIEM** (Splunk, ELK, QRadar)
- [ ] **Alertes email/SMS** configurables
- [ ] **Playbooks automatisés** (SOAR)
- [ ] **Machine Learning** pour détection d'anomalies
- [ ] **Mode multi-tenant** (plusieurs clients)
- [ ] **Export de rapports** (PDF, Excel)
- [ ] **Cartes géographiques** des attaques
- [ ] **Dark/Light theme** switcher

### Améliorations Techniques
- [ ] Backend Python/Flask pour données réelles
- [ ] Base de données MongoDB/PostgreSQL
- [ ] Cache Redis pour performance
- [ ] WebSocket pour temps réel
- [ ] Docker containerization
- [ ] CI/CD avec GitHub Actions

---

## 🎯 Cas d'Usage

### 🔵 Centre Opérationnel de Sécurité
```
Usage : Dashboard sur grands écrans muraux
Bénéfice : Visibilité instantanée des menaces
Public : Analystes SOC, responsables sécurité
```

### 🟢 Démonstration Client
```
Usage : Présentation des capacités de monitoring
Bénéfice : Interface moderne et professionnelle
Public : Prospects, décideurs IT
```

### 🟡 Formation & Éducation
```
Usage : Support pédagogique pour cours de SOC
Bénéfice : Visualisation concrète des concepts
Public : Étudiants en cybersécurité
```

---

## 📚 Technologies & Ressources

### Bibliothèques Utilisées
- Pur **HTML5/CSS3/JavaScript** (aucune dépendance)
- Alternative avec Chart.js possible pour graphiques

### Inspirations
- [Grafana](https://grafana.com/) - Dashboards de monitoring
- [Kibana](https://www.elastic.co/kibana/) - Visualisation Elasticsearch
- [Splunk](https://www.splunk.com/) - SIEM leader du marché

### Standards
- [MITRE ATT&CK](https://attack.mitre.org/) - Framework de menaces
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)

---

## 📧 Contact

**Valérie ENAME**
- GitHub : [@VAL-cyber-pentester](https://github.com/VAL-cyber-pentester)
- LinkedIn : [Valérie ENAME](https://linkedin.com/in/valérie-ename-02ba7733a)
- Portfolio : [val-cyber-pentester.github.io](https://val-cyber-pentester.github.io/projets)

---

## 📄 License

MIT License - Libre utilisation éducative et professionnelle.

---

## 🙏 Remerciements

Projet créé pour démontrer :
- Compétences en développement front-end moderne
- Compréhension des opérations SOC
- Capacité à créer des interfaces utilisateur intuitives
- Sens du design et de l'UX

---

🌐 **[ESSAYEZ LA DÉMO EN LIGNE](https://val-cyber-pentester.github.io/SOC-Dashboard/soc-dashboard.html)**

⭐ **Dashboard utile ? Laissez une étoile sur GitHub !**
