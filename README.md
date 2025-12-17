# 🧠 Simon Says - The Retro Memory Game

**[🔴 Hier Live Spielen](https://tsukasamita.github.io/Simon-Says-Game/)**

---

## 🎯 Über das Projekt
Dieses Projekt ist eine interaktive Web-Applikation, die zufällige Muster aus Farben und Tönen generiert, die der Spieler in der richtigen Reihenfolge wiederholen muss. Mit jedem Level wird die Sequenz um einen Schritt erweitert.

Das Ziel war es, **DOM-Manipulation** und **komplexe Spiel-Logik** mit JavaScript (und jQuery) sauber zu implementieren.

---

## ✨ Features
* **Progressive Schwierigkeit:** Das Spiel generiert unendlich lange Sequenzen (`nextSequence()`).
* **Audio-Visuelles Feedback:** Jede Farbe hat ihren eigenen Sound und eine Aufleucht-Animation.
* **Fehler-Handling:** Bei einer falschen Eingabe visuelles Feedback (roter Bildschirm) und "Game Over" Sound.
* **Retro Design:** Verwendung der 'Press Start 2P' Schriftart und eines dunklen Farbschemas (`#011F3F`) für authentisches Arcade-Feeling.

---

## 💡 Deep Dive: Was ich gelernt habe
Die Entwicklung dieses Spiels hat mein Verständnis für JavaScript-Konzepte vertieft, insbesondere:

### 1. Array-Management & Logik
Die größte Herausforderung war der Vergleich der Nutzer-Eingabe mit der generierten Sequenz. Ich habe zwei Arrays genutzt:
* `gamePattern`: Speichert die zufällige Computer-Sequenz.
* `userClickedPattern`: Speichert die Klicks des Spielers.

Ich habe gelernt, wie man diese Arrays Index für Index vergleicht, anstatt nur die Länge zu prüfen.

### 2. Asynchrones JavaScript & Timing
Um Animationen flüssig zu gestalten und dem Nutzer Zeit zu geben, musste ich mit `setTimeout` arbeiten.
* **Beispiel:** Wenn eine Sequenz korrekt ist, wartet der Code 1000ms, bevor das nächste Level startet, um dem Spieler eine mentale Pause zu gönnen.
* **Animation:** Das Entfernen der `.pressed` CSS-Klasse erfolgt verzögert nach 100ms, um einen realistischen Tastendruck zu simulieren.

### 3. jQuery zur DOM-Manipulation
Anstatt reinem Vanilla JS habe ich **jQuery** eingesetzt, um Event-Handling und Animationen effizienter zu schreiben:
* Kürzerer Code für Event-Listener (`$(".btn").click(...)`).
* Eingebaute Animationseffekte wie `.fadeOut(100).fadeIn(100)` für das Aufblinken der Buttons.

