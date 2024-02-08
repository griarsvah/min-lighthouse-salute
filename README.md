# Lighthouse


## Performance
```
index.html

<h1>Lighthouse - Performance</h1>
```


## Accessibility-Для прохождения нужно чтобы Performance был выполнен
```
index.html

<html lang="en">
        <title>Page title</title>
        <h1>Lighthouse - Accessibility</h1>
</html>
```


## Best Practices-Для прохождения нужно чтобы Performance был выполнен+Нужно HTTPS
```
index.html

<!doctype html>
<meta charset="utf-8">
        <h1>Lighthouse - Best Practices</h1>
```


## SEO-Для прохождения нужно чтобы Performance был выполнен
```
index.html

<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Page title</title>
<meta name="description" content="description">
<h1>Lighthouse - SEO</h1>
```


## Минимальный код для салюта -Для прохождения нужно чтобы Performance был выполнен+Нужно HTTPS
```
index.html

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
index.html

<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#FFFFFF">
<link rel="manifest" href="manifest.webmanifest">
<h1>Lighthouse - PWA</h1>
```

```
manifest.webmanifest

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


## Ошибки и предупреждения в инструментах разработчика в вкладке "Aplication/Приложение"

## Errors and warnings

Richer PWA Intall UI won't be available on desktop. Please add at least one screenshot with the form_factor set to wide. - Пропала ошибка когда добавили иконку с ключём и значением "form_factor": "narrow",

Richer PWA Intall UI won't be available on mobile. Please add at least one screenshot for with form_factor is not set or set to a value other than wide. - Пропала ошибка когда добавили иконку с ключём и значением "form_factor": "wide",

Actual width (144px) of icon https://example.com/ does not match specified width (144px)
Actual width (144px) of Screenshot https://example.com/ does not match specified width (144px)

```
manifest.webmanifest

"screenshots": [
    {
      "src": "https://image-placeholder.com/images/actual-size/320x320.png",
      "type": "image/png",
      "sizes": "320x320",
      "form_factor": "narrow",
      "label": "Homescreen of Awesome App"
    },
    {
      "src": "https://griarsvah.github.io/PWABuilder/images/maskable/icon_x384.png",
      "type": "image/png",
      "sizes": "384x384",
      "form_factor": "wide",
      "label": "Homescreen of Awesome App"
    }
  ]
```

Screenshot https:// size should be at least 320x320
```
manifest.webmanifest

{
  "src": "https://griarsvah.github.io/PWABuilder/images/maskable/icon_x384.png",
  "type": "image/png",
  "sizes": "384x384",
  "form_factor": "wide",
  "label": "Homescreen of Awesome App"
}
```

Пропала ошибка когда добавили иконку с ключём и значением "form_factor": "narrow",
Richer PWA Intall UI won't be available on desktop. Please add at least one screenshot with the form_factor set to wide.

---

В разделе "Presentation" пустое поле "Orientation"
Добавляю "orientation": "any",
```
manifest.webmanifest

"orientation": "any",
```

---

Заметка
Note: id is not specified in the manifest, start_url is used instead. To specify an App ID that matches the current identity, set the id field to /index.html
```
manifest.webmanifest

id: "/?homescreen=1",
start_url: "/?homescreen=1",
```

---

Раздел "Window Controls Overlay"
Define display-override in the manifest to use the Window Controls Overlay API and customize your app's title bar.
Need help? [Read](https://learn.microsoft.com/en-us/microsoft-edge/progressive-web-apps-chromium/how-to/window-controls-overlay)
```
"display_override": ["fullscreen", "standalone", "minimal-ui", "standalone", "window-controls-overlay"],
```

---

В разделе "Protocol Handlers" вижу восклицательный знак
Define protocol handlers in the manifest to register your app a handler for custom protocols when your app is intalled.
Need help? Read [URL protocol handler registration for PWAs.](https://web.dev/url-protocol-handler/?utm_source=devtools)

---
manifest.json:1 Manifest: property 'url' ignored, should be within scope of the manifest.
manifest.json:1 Manifest: protocol_handlers entry ignored, required property 'url' is invalid.
---
```
manifest.webmanifest

"protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "/shop?for=%s"
    }
  ]
```

В "url" путь прописывать полный

```
manifest.webmanifest

"protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "https://griarsvah.github.io/min-lighthouse-salute/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "https://griarsvah.github.io/min-lighthouse-salute/shop?for=%s"
    }
  ]
```

---


## Publisher Ads
```
index.html

<h1>Lighthouse - Publisher Ads</h1>
<script async src="tag/js/gpt.js"></script>
```

---

```
chrome://whats-new/
chrome://web-app-internals/
chrome://restart
chrome://apps/

chrome://web-app-internals/
chrome://serviceworker-internals/

"narrow - узкий"
"wide - широкий"
```
