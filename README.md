# Association Bénévolat & Solidarité — Projet 1

## Description
Page vitrine statique en HTML/CSS présentant une association fictive. 
Pas de maquette préalable — structure simple header / body / footer.

## Structure de la page
- **Header** : image de fond en pleine largeur (position fixed, opacity 0.3, 
  masque en dégradé) + titre de l'association
- **Navigation** : 4 liens (Accueil, À propos, Contact, Faire un Don)
- **Contenu principal** (`<main>`) : présentation de l'association, 
  actions de terrain, mission, valeurs
- **Footer** : mention de copyright

## Image d'en-tête
Image de base utilisée pour le header, étirée en pleine largeur, 
opacité réduite et masquée en dégradé via CSS pur.

![Image d'en-tête](https://github.com/user-attachments/assets/87c3d307-3dd1-4e89-b4f8-ffdf4aeaa308)

## Aperçu du site
Pour la partie centrale, inspiration tirée de plusieurs sites 
d'associations existants pour l'esthétique globale.

![Aperçu de la page principale](https://github.com/user-attachments/assets/1fdf1b41-c7b3-434c-82c0-4c3d242bf26a)

![Aperçu de la section contenu](https://github.com/user-attachments/assets/0ca2d505-bd65-4abc-9255-38dfdc517f91)

## Choix esthétiques
- Boutons de navigation actuellement décoratifs (placeholder, pages 
  À propos / Contact / Don pas encore créées)
- Images choisies à titre d'illustration (assumé volontairement "clichées")

## Validation W3C
Validation effectuée sur https://validator.w3.org/nu/

**Avant correction :**

![Erreurs du validateur W3C avant correction](https://github.com/user-attachments/assets/6e8d93ca-004c-452b-a29b-0f86b1b3203d)

Erreurs rencontrées :
- Slash inutile sur les balises `<meta>` (void elements)
- Espace dans un nom de fichier image (`src` invalide)
- Saut de niveau de titre (h2 → h4)

**Erreur de nom de fichier (espace dans le nom du fichier) :**
**Après correction :** : fichier renommé pour retirer l'espace.
![Erreur espace dans le nom de fichier](https://github.com/user-attachments/assets/30292d36-6b8a-4a4c-95ed-82cc0e18bd2e)

![Validateur W3C après correction, 0 erreur](https://github.com/user-attachments/assets/da5a443b-35cc-412c-9c86-a72b6eebb8ce)

Résultat final : 0 erreur, 0 warning.

j'ai aussi ajouté 4 pages web vides que je remplirais a plus tard et un petit trait esthétique au centre pour que ce soit joli
<img width="1840" height="843" alt="image" src="https://github.com/user-attachments/assets/c9edcfa6-e224-4f4c-b2aa-66a01ef0afb4" />
<img width="1821" height="583" alt="image" src="https://github.com/user-attachments/assets/ec5f14eb-2f96-476a-b6cc-fe292700729d" />

j'ai refait le site de sorte a ce qu'il soit mobile first
<img width="2516" height="1325" alt="image" src="https://github.com/user-attachments/assets/48cba783-4e00-4598-b7ea-ae3ce37fc38a" />
<img width="881" height="1074" alt="image" src="https://github.com/user-attachments/assets/d755c34d-5ffa-4b3b-bce1-b4a3b808ebca" />
<img width="1446" height="948" alt="image" src="https://github.com/user-attachments/assets/0875b8d0-d975-4d1e-ba22-4a2a505843ad" />

## Accessibilité
### Avant corrections
- Pas de `<main>` : aucun repère de contenu principal pour un lecteur d'écran
- Couleur du texte des liens/boutons trop claire (contraste insuffisant)
- Image illustrative avec `alt=""` (traitée comme décorative alors 
  qu'elle apporte du contenu)
- Hiérarchie de titres incohérente (h2 → h4)

### Après corrections
- Ajout d'un `<main>` autour du contenu principal
- Couleur de texte assombrie pour respecter le contraste minimum AA
- Ajout d'un `alt` descriptif sur l'image concernée
- Hiérarchie de titres réparée (h1 → h2, sans saut)

### Tests effectués
- Navigation clavier : effectué et fonctionnel
- Lecteur d'écran : structuration sémantique validée
- Contraste (WebAIM Contrast Checker) : conforme aux exigences AA

## Refactorisation Projet 2 (CSS Moderne & Responsive)

### 1. Variables CSS (`:root`)
Centralisation des styles clés en haut du fichier CSS :
- Couleurs (`--bg-button`, `--bg-button-hover`, `--text-color`, `--text-dark`, `--border-color`)
- Espacements (`--space-xs`, `--space-sm`, `--space-md`, `--space-lg`)

### 2. Dispositions Flexbox & Grid
- **CSS Grid** : Appliqué sur les conteneurs `.bodies` et `.bodies2` pour la structure globale des blocs de contenu.
- **Flexbox** : Utilisé pour la barre de navigation (`nav ul`) et le séparateur personnalisé (`.custom-divider`).

### 3. Approche Mobile-First et Justification des Breakpoints
La feuille de style est désormais construite en **Mobile-First** (styles de base pour petits écrans, puis enrichissement via `min-width`) :
- **`@media (min-width: 480px)`** : Ajustement des espacements du menu et des éléments sur mobile large/tablette.
- **`@media (min-width: 850px)`** : Passage de la grille d'une colonne (mobile) à deux colonnes (`grid-template-columns: 1fr 1fr`) pour l'affichage ordinateur.

### 4. Matrice de vérification multi-largeurs et navigateurs

| Largeur testée | Google Chrome | Mozilla Firefox | Résultat |
| :--- | :--- | :--- | :--- |
| **375px** (Mobile) | ✅ Validé | ✅ Validé | Affichage 1 colonne fluide, aucun scroll horizontal. |
| **768px** (Tablette) | ✅ Validé | ✅ Validé | Marges adaptées, navigation lisible. |
| **1200px** (Desktop) | ✅ Validé | ✅ Validé | Disposition 2 colonnes via Grid, conforme au design. |

ajout d'un formulaire pour les dons

### 5. Ajout d'un formulaire et de l'affichage + tri des infos 
<img width="1873" height="955" alt="image" src="https://github.com/user-attachments/assets/40fa15b9-3926-4b92-a6e7-7f19cdc957e8" />

normalement avec tout ça je remplis les 3 premiers projets
## Publication
- URL du site en ligne : [à compléter]
