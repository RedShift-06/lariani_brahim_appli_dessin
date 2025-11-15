# Application de Dessin Web (Canvas) - Lariani Brahim

## 💡 Description du Projet
Ce projet est une application de dessin interactive réalisée en Front-End pur. Il permet aux utilisateurs de créer des dessins sur une zone de travail (Canvas) en utilisant divers outils et contrôles d'interface.

## 🛠️ Technologies Utilisées
* **HTML5** : Structure du Canvas et des éléments de l'interface (outils, boutons, modals).
* **CSS3** : Design moderne, mise en page responsive et ajout d'animations (tooltips, modals, effets survol).
* **JavaScript (ES6+)** : Logique de l'application, gestion de l'API Canvas pour le dessin, interaction avec le DOM, et gestion des événements clavier.

## 📋 Fonctionnalités Principales

* **Outils de Dessin** : Pinceau, Gomme, et Pot de peinture (Remplissage de zone).
* **Contrôles de Style** : Sélecteur de couleur, curseurs pour ajuster la taille du trait (1 à 50px) et l'opacité (1% à 100%).
* **Actions** : Bouton d'Effacement total (avec modal de confirmation) et bouton de Sauvegarde du dessin au format PNG.
* **Accessibilité** : Raccourcis clavier pour les outils principaux (B, E, F, C, S).
* **UX/UI** : Modals de confirmation et de succès, tooltips (bulles d'aide) pour les icônes.

## 🌐 Rendu Final (GitHub Pages)
Le projet est hébergé en direct à l'adresse suivante :
https://redshift-06.github.io/lariani_brahim_appli_dessin/

---

## 🧭 Mon Journal de Bord

### Nouveautés Explorées
* **API Canvas :** Maîtrise des méthodes de dessin de base (`beginPath`, `lineTo`, `stroke`), de la gestion de l'état (`lineCap`, `lineWidth`) et de la gestion de la transparence (`globalAlpha`).
* **Gestion des Événements Complexes :** Mise en place des écouteurs d'événements pour le Canvas (souris) et le document (clavier) pour les raccourcis.
* **Structure Modulaire :** Organisation du code JavaScript en fonctions distinctes (initialisation, dessin, outils, modals).

### Difficultés Rencontrées
* La gestion des coordonnées de la souris pour qu'elles correspondent exactement au Canvas, surtout si la page est défilée, a été un défi.
* L'implémentation de la gomme : utiliser le pinceau n'était pas suffisant pour effacer proprement.

### Solutions Apportées
* J'ai utilisé `canvas.getBoundingClientRect()` pour obtenir la position exacte du Canvas dans la fenêtre, puis j'ai soustrait ces valeurs des coordonnées de l'événement souris (`clientX`, `clientY`).
* J'ai utilisé `ctx.globalCompositeOperation = 'destination-out'` pour que la gomme "retire" le contenu existant du Canvas, ce qui simule un effacement parfait sur fond blanc.

---

### 📅 Historique des Commits
J'ai effectué 5 commits significatifs pour documenter l'avancement du projet :

1. `1/5 Initialisation de la structure (HTML) et du design de base (CSS)`
2. `2/5 Implémentation de la fonctionnalité de dessin de base (pinceau)`
3. `3/5 Implémentation de la gestion des outils (Couleur, Taille, Opacité)`
4. `4/5 Implémentation des actions (Sauvegarde et Effacement avec Modals)`
5. `5/5 Amélioration finale: Ajout des modals, commentaires et raccourcis clavier`
