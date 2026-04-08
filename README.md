# projet-web-components — Demo

Application de lecteur audio sous forme de studio modulaire, construite avec des Web Components personnalisés.

## Structure

```
index.html          — page principale
js/
  studio.js         — câblage de la chaîne audio et layout des fenêtres
  dragManager.js    — gestion du drag & drop des fenêtres
css/styles.css      — styles globaux
assets/             — pistes audio et couvertures
```

## Web Components

Les composants utilisés (`<my-audio-player>`, `<my-playlist>`, `<my-eq>`, `<my-waveform>`, `<my-butterchurn>`) sont définis dans le dépôt séparé :

**[Stitchal/projet-web-components_components](https://github.com/Stitchal/projet-web-components_components)**

Ils sont chargés via CDN jsDelivr directement depuis ce dépôt :

```html
<script type="module" src="https://cdn.jsdelivr.net/gh/Stitchal/projet-web-components_components/components/audioplayer.js"></script>
```

## Chaîne audio

```
player → eq → waveform → butterchurn → destination
```

Le câblage est effectué dans `js/studio.js` après que tous les composants sont définis.

## Raccourcis clavier

| Touche       | Action              |
|--------------|---------------------|
| `Espace`     | Lecture / Pause     |
| `←`          | Piste précédente    |
| `→`          | Piste suivante      |
| `M`          | Muet                |
