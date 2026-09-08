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
- Navigation clavier : [à compléter]
- Lecteur d'écran ([NVDA/VoiceOver]) : [à compléter]
- Contraste (WebAIM Contrast Checker) : [à compléter]

## Publication
- URL du site en ligne : [à compléter]
