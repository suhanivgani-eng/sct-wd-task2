# ⏱️ Accurate Stopwatch Web App

A modern, responsive, and highly accurate stopwatch web application built using **HTML**, **CSS**, and **JavaScript**.
Designed with accessibility, performance, and clean UI/UX in mind.


## 🚀 Features

* **Performance-accurate timing** using `performance.now()`
* **Start, Pause, Reset** controls
* **Lap recording** with:

  * Total elapsed time
  * Delta time since previous lap
* **CSV export** of lap data
* **Keyboard shortcuts**

  * **Space** → Start/Pause
  * **L** → Lap
  * **R** → Reset
* **Responsive design**
* **Accessible ARIA roles**, live regions, and labels



## 🧠 How It Works

The timing system uses:

```
startTime  → timestamp at start
offset     → accumulated paused time
elapsed    → offset + (now - startTime)
```

`requestAnimationFrame()` updates the display without drift, while visibility change handling prevents tab-switch inaccuracies.

---

## 📁 Project Structure

```
/
│── index.html   # Main stopwatch application
```

This project is fully self-contained in a single HTML file with embedded CSS and JavaScript.

---

## 📦 Technologies Used

* **HTML5**
* **CSS3 (custom responsive styles)**
* **Vanilla JavaScript**
* **performance.now() API**
* **requestAnimationFrame()**

---

## 🎮 Controls

| Action        | Control                     |
| ------------- | --------------------------- |
| Start / Pause | Space or Start/Pause button |
| Lap           | L                           |
| Reset         | R                           |
| Export CSV    | "Export Laps" button        |

---

## 📤 Exporting Laps

Click **Export Laps** to download a CSV containing:

* Lap number
* Total time (ms + formatted)
* Delta time (ms + formatted)

Example CSV structure:

```
Lap,TotalMs,Total,DeltaMs,DeltaFormatted
1,5321,00:05.32,5321,00:05.32
2,8240,00:08.24,2919,00:02.91
```

---


## 🛠️ Setup

No installation required.

Just open `index.html` in any modern browser:

```
chrome index.html
```

Or use a local server (recommended):

* VS Code Live Server
* Python `http.server`
* Node `serve`

---


