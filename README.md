# Lighthouse


## Performance
```
<h1>Lighthouse - Performance</h1>
```


## Accessibility-Для прохождения нужно чтобы Performance был выполнен
```
<html lang="en">
        <title>Page title</title>
        <h1>Lighthouse - Accessibility</h1>
</html>
```


## Best Practices-Для прохождения нужно чтобы Performance был выполнен+Нужно HTTPS
```
<!doctype html>
<meta charset="utf-8">
        <h1>Lighthouse - Best Practices</h1>
```


## SEO-Для прохождения нужно чтобы Performance был выполнен
```
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Page title</title>
<meta name="description" content="description">
<h1>Lighthouse - SEO</h1>
```


## Минимальный код для салюта -Для прохождения нужно чтобы Performance был выполнен+Нужно HTTPS
```
<!doctype html>
<html lang="en">
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="description">
    <title>Page title</title>
        <h1>Lighthouse - min-code-lighthouse-salute</h1>
</html>
```

## PWA
```
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#FFFFFF">
<link rel="manifest" href="manifest.webmanifest">
<h1>Lighthouse - PWA</h1>
```

```
{
  "name": "Grigoryan Vahe Arseni",
  "short_name": "GriArsVa",
  "background_color": "#FFFFFF",
  "theme_color": "#FFFFFF",
  "display": "standalone",
  "start_url": "index.html",
  "icons": [
    {
      "src": "imgs/maskable-144.png",
      "type": "image/png",
      "sizes": "144x144",
      "purpose": "maskable"
    },
      "src": "imgs/512.png",
      "type": "image/png",
      "sizes": "512x512"
    }
  ]
}
```

Нужны две картинки 144 или 192 для маскировочного, а так же 512
Про маскировочный можно почитать [тут](https://developer.chrome.com/docs/lighthouse/pwa/maskable-icon-audit?utm_source=lighthouse&utm_medium=devtools&hl=ru), а сделать [тут](https://maskable.app/editor)


## Publisher Ads
```
<h1>Lighthouse - Publisher Ads</h1>
<script async src="tag/js/gpt.js"></script>
```
