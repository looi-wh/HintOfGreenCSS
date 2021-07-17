# Hint of Green
## Jellyfin CSS Theme

Sort of my first try on a css template. When I first designed this template, I tried my best to design something new but familar. I wanted something that is different from the other masterpiece that the other wizards have created.

## Features
- Colours are based on a popular template
- Little spinkle of green everywhere, but never too much
- Lighter theme for video playback (better if you see for yourself)
- Disabled blurring on Safari (performance issues)
- Better support for mobile devices
- Works extremely beautiful with backdrop enabled
- Some playful colouring at unexpected places (you will like it)

This theme can be considered as heavy, but of course there some css will disable by itself if certain unfavourable conditions are met.

## Installation
There will be two channels, one stable and one nightly. It is always ideal to use the stable version if you are deploying to a large amount of people. But if you like to be risky, feel free to use the nightly version. I will merge nightly into stable once I feel the nightly version is performing well enough.
Copy this code into Dashboard > General > Custom CSS
#### Stable:
```css
@import ur("https://raw.githubusercontent.com/looi-wh/HintOfGreenCSS/main/theme.css");
```
or
#### Tester/Nightly:
```css
@import ur("https://raw.githubusercontent.com/looi-wh/HintOfGreenCSS/main/themeNightly.css");
```

## NGINX fixes
If you are using nginx as a reverse proxy for Jellyfin, replace the "add_header Content-Security-Policy" in your nginx config with this line below
```
add_header Content-Security-Policy "default-src https: data: blob: http://image.tmdb.org; style-src 'self' 'unsafe-inline'https://raw.githubusercontent.com/looi-wh/HintOfGreenCSS/main/theme.css; script-src 'self' 'unsafe-inline'https://raw.githubusercontent.com/looi-wh/HintOfGreenCSS/main/themeNightly.css; script-src 'self' 'unsafe-inline' https://www.gstatic.com/cv/js/sender/v1/cast_sender.js https://www.youtube.com blob:; worker-src 'self' blob:; connect-src 'self'; object-src 'none'; frame-ancestors 'self'";
```

## Note to self
Its been a busy week, so some notes might be important later on
- Add images later to this readme
