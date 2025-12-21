# 📚 Documentation Generator

Un générateur de documentation moderne et minimaliste en HTML/CSS/JS pur. Transformez vos fichiers Markdown en une documentation élégante avec thème sombre.

![Theme](https://img.shields.io/badge/theme-dark-black)
![License](https://img.shields.io/badge/license-MIT-blue)

## ✨ Fonctionnalités

- 🎨 **Thème sombre moderne** - Interface élégante en noir/gris
- 📁 **Organisation automatique** - Détection des dossiers et création de catégories
- 🔍 **Navigation intuitive** - Menu latéral avec hiérarchie claire
- 📝 **Support Markdown complet** - Rendu de tous les éléments Markdown
- 🚀 **Léger et rapide** - Aucune dépendance backend
- 📱 **Responsive** - Adapté mobile et desktop
- ⚡ **Sans serveur** - Fonctionne directement dans le navigateur

## 🚀 Installation

### 1. Cloner le dépôt

```bash
git clone https://github.com/votre-username/doc-generator.git
cd doc-generator
```

### 2. Structure du projet

```
doc-generator/
├── index.html              # Interface de documentation
├── generate_index.py       # Script de génération d'index
├── README.md              # Ce fichier
├── introduction.md        # Exemple de doc
└── tutoriels/             # Exemple de dossier
    ├── premier.md
    └── deuxieme.md
```

### 3. Ajouter vos fichiers Markdown

Placez vos fichiers `.md` n'importe où dans le projet :

```
votre-projet/
├── index.html
├── generate_index.py
├── guide.md                    # ← Fichier racine
├── installation.md             # ← Fichier racine
├── api/                        # ← Dossier = Catégorie
│   ├── authentication.md
│   └── endpoints.md
└── tutoriels/                  # ← Dossier = Catégorie
    ├── getting-started.md
    └── advanced.md
```

### 4. Générer l'index

```bash
python generate_index.py
```

Cela crée `index.json` avec la liste de tous vos fichiers `.md`

### 5. Ouvrir la documentation

Ouvrez simplement `index.html` dans votre navigateur !

## 📖 Utilisation

### Écrire en Markdown

Tous les éléments Markdown sont supportés :

```markdown
# Titre principal
## Sous-titre
### Section

Du texte normal, **gras**, *italique*, `code inline`

- Liste
- À puces

1. Liste
2. Numérotée

> Citation

\`\`\`javascript
// Bloc de code
console.log('Hello World');
\`\`\`

[Lien](https://example.com)

| Tableau | Colonne 2 |
|---------|-----------|
| Donnée  | Donnée    |
```

### Organisation par dossiers

Les fichiers sont automatiquement groupés par dossier :

- **Fichiers à la racine** → Affichés en premier
- **Fichiers dans dossiers** → Regroupés en catégories

Exemple :
```
api/endpoints.md       → Catégorie "Api"
tutorials/basics.md    → Catégorie "Tutorials"
getting_started.md     → Racine
```

### Mettre à jour la documentation

À chaque ajout/suppression de fichier `.md`, relancez :

```bash
python generate_index.py
```

## 🎨 Personnalisation

### Modifier les couleurs

Éditez les variables CSS dans `index.html` :

```css
/* Couleurs principales */
background: #0d0d0d;        /* Fond principal */
color: #e0e0e0;             /* Texte */
border: #2a2a2a;            /* Bordures */
accent: #3b82f6;            /* Accent bleu */
```

### Modifier le titre

Dans `index.html`, ligne ~44 :

```html
<h1>📚 Votre Titre</h1>
```

### Changer la largeur du contenu

Ligne ~85 du CSS :

```css
.content-inner {
    max-width: 850px;  /* Ajustez cette valeur */
}
```

## 🛠️ Technologies

- **HTML5** - Structure
- **CSS3** - Styling moderne avec gradients et animations
- **JavaScript** - Navigation et chargement dynamique
- **Marked.js** - Parser Markdown (v9.1.6)
- **Python 3** - Script de génération d'index

## 🤝 Contribution

Les contributions sont les bienvenues ! N'hésitez pas à ouvrir une issue ou une pull request.

⭐ **Star ce projet si vous le trouvez utile !**
