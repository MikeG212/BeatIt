# BeatIt
Online drum kit.

[Play now](https://mikeg212.github.io/BeatIt/)

# Technologies
JavaScript to create query selectors and event handlers.
HTML5 music player to play the different sounds.


# Playing the Music
In order to `playSound` and `removeTransition`, I called `play` on the audio element and added and removed the `playing` class to the button.
This triggers the CSS to temporarily change the color and shadow.

```javascript
function playSound(e) {
    const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
    const key = document.querySelector(`.key[data-key="${e.keyCode}"]`);
    if (!audio) return;
    audio.currentTime = 0;
    audio.play();
    key.classList.add('playing');
}
```

# Bonus Features
- Create Guitar Hero-like game functionality so users can recreate famous drum solos.
