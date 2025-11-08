# Hint of Green
Jellyfin CSS Theme

Sort of my first try on a css template. When I first designed this template, I tried my best to design something new but familar. I wanted something that is different from the other masterpiece that the other wizards have created.

## Tested on
- Chrome, Firefox, Safari and common Jellyfin applications
- Jellyfin 10.11.2

## Features
- Colours are based on a popular template
- Little spinkle of green everywhere, but never too much (UPDATE: temporarily removed all colours)
- Lighter theme for video playback (better if you see for yourself) (UPDATE: removed, no longer neccessary)
- Better support for mobile devices (UPDATE: updated)
- Works extremely beautiful with backdrop enabled

This theme can be considered as heavy, but of course there some css will disable by itself if certain unfavourable conditions are met.

## Installation
There will be two channels, one stable and one nightly. It is always ideal to use the stable version if you are deploying to a large amount of people. But if you like to be risky, feel free to use the nightly version. I will merge nightly into stable once I feel the nightly version is performing well enough.
Copy this code into Dashboard > General > Custom CSS
#### Stable:
```css
@import url('https://looi-wh.github.io/HintOfGreenCSS/theme.css');
```
or
#### Tester/Nightly (deprecated):
```css
@import url('https://looi-wh.github.io/HintOfGreenCSS/themeNightly.css');
```

## Nginx
If you are using nginx as a reverse proxy for Jellyfin, replace the "add_header Content-Security-Policy" in your nginx config with this line below
```shell
add_header Content-Security-Policy "default-src https: data: blob: http://image.tmdb.org; style-src 'self' 'unsafe-inline' https://looi-wh.github.io ; script-src 'self' 'unsafe-inline' https://www.gstatic.com/cv/js/sender/v1/cast_sender.js https://www.youtube.com blob:; worker-src 'self' blob:; connect-src 'self'; object-src 'none'; frame-ancestors 'self'";
```

## Images
Home Page (With Media Bar Plugin)
![alt text](1.HomePage(WithMediaBar).png)

Movie Detail Page
![alt text](2.ItemDetails.png)

Movie Detail Page
![alt text](3.ItemDetails.png)

Series Detail Page
![alt text](4.ItemDetails.png)

Series Session Detail Page
![alt text](5.Season.png)
