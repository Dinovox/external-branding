# external-branding

Voici la structure et les formats recommandés pour externaliser les assets de vos collections.

Pour chaque collection (identifiée par son ID, ex: `DINO-123456`), créez un dossier avec les fichiers suivants :

## 1. Structure des Fichiers

```text
/collections
  └── /DINO-123456/          <-- Dossier portant l'ID de la collection
       ├── logo.png          (Image de profil / Avatar)
       ├── banner.png        (Image de couverture / Header)
       └── info.json         (Description et liens sociaux)
```

## 2. Spécifications des Images

| Fichier       | Usage                                         | Format Recommandé | Dimensions Idéales | Poids Max |
| :------------ | :-------------------------------------------- | :---------------- | :----------------- | :-------- |
| `logo.webp`   | Avatar rond/carré dans les listes et en-têtes | WebP (carré)      | 500x500 px         | < 200 Ko  |
| `banner.webp` | Image large en fond d'écran de l'en-tête      | WebP (paysage)    | 1600x400 px        | < 500 Ko  |

> **Note :** Le format WebP est aussi très bien supporté et plus léger, mais le PNG reste le standard le plus simple à éditer pour l'instant.

## 3. Fichier de Données (Optionnel mais recommandé)

Pour externaliser aussi les textes, ajoutez un fichier `info.json`.
Par défaut, le système cherche `logo.webp` et `banner.webp`. Si vous utilisez d'autres formats (ex: .webp, .jpg), vous devez les spécifier :

```json
{
  "name": "DinoVox Legacy",
  "description": "La collection officielle des Dinos...",
  "website": "https://dinovox.com",
  "twitter": "https://twitter.com/dinovox",
  "discord": "https://discord.gg/...",
  "logo": "logo.jpg", // Optionnel : ne mettre que si différent de logo.png
  "banner": "banner.jpg" // Optionnel : ne mettre que si différent de banner.png
}
```
