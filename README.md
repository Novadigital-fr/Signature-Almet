# Signatures email ALMET

4 templates HTML compatibles **Outlook (Windows/Mac/Web), Gmail, Apple Mail, Thunderbird, mobile**.

## Fichiers

| Fichier | Logo(s) | Site web | LinkedIn |
|---|---|---|---|
| `signature-almet.htm` | ALMET | almet-metal.com | linkedin.com/company/almet-france |
| `signature-alu3p.htm` | ALU3P (seul) | alu3p.com | linkedin.com/company/almet-france |
| `signature-lemetalservices.htm` | ALMET + LE METAL SERVICES | almet-metal.com | linkedin.com/company/almet-france |
| `signature-almetmarine.htm` | ALMET MARINE (seul) | almet-marine.com | linkedin.com/company/almet-france |
| `index.html` | — | (page de prévisualisation) | — |

## Prévisualiser

Ouvrir `index.html` dans un navigateur (ou lancer un petit serveur local : `python3 -m http.server` puis http://localhost:8000).

## Personnalisation par salarié

Dans chaque fichier `.htm`, remplacer :

- `{{Prénom}} {{NOM}}`
- `{{Fonction}}`
- `{{+33 4 00 00 00 00}}`
- `{{email@almet-metal.com}}` (deux fois : dans le `href` et dans le texte affiché)

## Remplacer les logos placeholders

Les URLs actuelles pointent vers `placehold.co` (logos fictifs).
Une fois les logos officiels prêts :

1. Héberger les images PNG sur une URL publique stable (ex. `https://www.almet-metal.com/signatures/logo-almet.png`)
2. Dans chaque `.htm`, remplacer toutes les URLs `https://placehold.co/...` par les vraies URLs.

**Dimensions recommandées :**
- Logo ALMET principal : 160 × 60 px
- Logo filiale (ALU3P, LE METAL SERVICES, ALMET MARINE) : 160 × 40 px
- Icônes sociales : 28 × 28 px
- Bannière "L'expertise du métal" : 600 × 90 px

## Déploiement Outlook

### Méthode manuelle (par salarié)
1. Ouvrir Outlook → Fichier → Options → Courrier → Signatures
2. Créer une nouvelle signature (laisser vide), valider
3. Fermer Outlook
4. Aller dans `%appdata%\Microsoft\Signatures\`
5. Remplacer le fichier `.htm` créé par celui fourni (renommé avec le même nom)
6. Rouvrir Outlook : la signature est prête

### Méthode centralisée (recommandée pour 10+ salariés)
Utiliser un outil de gestion centralisée : **Exclaimer**, **CodeTwo** ou **Letsignit** — permet à l'IT de pousser les signatures à toute l'entreprise et de garantir l'uniformité.

## Compatibilité technique

- Tableaux HTML avec CSS **inline uniquement** (pas de classes ni de feuilles externes)
- Aucun flexbox / grid / SVG / police custom
- Images PNG hébergées via URL (pas de base64)
- Polices système : Arial / Helvetica
- Dimensions fixes en pixels
