# RLFC Coach U12

Application de coaching football pour l'équipe U12 du **Royal Léopold FC** (IRIS Elite · ACFF).

App web single-file (un seul `index.html`) — React 18 + Babel Standalone, aucune dépendance npm, déployable sur n'importe quel serveur statique ou ouverte directement dans le navigateur.

## Fonctionnalités

- **Accueil** — vue d'ensemble (stats équipe, prochain match, séances à venir, actions rapides)
- **Séances** — bibliothèque de **50 exercices préfaits** + builder de séance + mode LIVE avec chrono
- **Groupe** — gestion du roster (filtres par poste/statut, CRUD complet)
- **Match** — préparation tactique (formations 8v8, composition, banc, absents) + mode LIVE (scoreboard, événements, chrono mi-temps)
- **Suivi** — évaluation joueurs sur 6 piliers (technique, tactique, physique, mental, collectif, leadership) avec radar + historique
- **Saison** — bilan global, top buteurs, temps de jeu, calendrier mensuel avec créneaux d'entraînement récurrents (mer/ven 17h-18h30, août à mai)

## Stack

- React 18 (UMD) + Babel Standalone (JSX compilé dans le navigateur)
- Tout inline — pas de build, pas de bundler, pas de node_modules
- LocalStorage pour la persistance
- Composants UI maison : Btn, IconBtn, Card, Modal, Select, MultiSelect (custom dropdown via React.createPortal), Tabs, Chip, Slider, Radar SVG, etc.
- 60+ icônes SVG inline (Lucide-inspired)
- Light / Dark theme
- Import / Export JSON pour backup
- Responsive iPad + desktop

## Utilisation

### En local
```bash
# Avec Python
python3 -m http.server 3000 --bind 0.0.0.0
# Puis ouvrir http://localhost:3000/index.html
```

### Sur tablette (même Wi-Fi)
Récupérer l'IP locale du Mac : `ipconfig getifaddr en0`, puis ouvrir sur la tablette :
```
http://<IP-DU-MAC>:3000/index.html
```

### Ajout à l'écran d'accueil (mode app)
- **iPad Safari** : Partager → "Sur l'écran d'accueil"
- **Android Chrome** : ⋮ → "Ajouter à l'écran d'accueil"

L'app s'ouvre alors en plein écran comme une vraie application.

## Données

- Toutes les données restent **locales** dans le navigateur (LocalStorage)
- Export JSON disponible dans **Réglages → Exporter mes données**
- Aucun serveur, aucun cloud, aucun tracking

## Licence

Usage personnel — Royal Léopold FC.
