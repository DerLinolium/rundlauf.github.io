# rundlauf.github.io
Rundlauf-Varianten TT by Joël Oettlin
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>Meine Simple Website</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; }
    .tabs { display: flex; background: #444; }
    .tab {
      padding: 14px 20px;
      color: white;
      cursor: pointer;
      flex: 1;
      text-align: center;
      transition: background 0.2s;
    }
    .tab.active { background: #222; }
    .content { padding: 30px; }
    .content > div { display: none; }
    .content > .active { display: block; }
  </style>
</head>
<body>
  <div class="tabs">
    <div class="tab active" data-tab="start">Startseite</div>
    <div class="tab" data-tab="seite1">Seite 1</div>
    <div class="tab" data-tab="seite2">Seite 2</div>
  </div>
  <div class="content">
    <div class="start active">
      <h1>Rundlauf (Klassisch)</h1>
      <p><b>🎯 Ziel des Spiels:</b>

<i>Jeder Spieler versucht, möglichst lange im Spiel zu bleiben. Wer einen Fehler macht, scheidet aus. Der letzte verbleibende Spieler gewinnt.</i>

<b>📋 Grundregeln:</b>

Aufstellung:

- Alle Spieler stellen sich in einer Schlange auf beiden Seiten der Platte auf.
- Zwei Spieler stehen spielbereit an der Platte – einer auf jeder Seite.
- Spielbeginn:
- Der erste Spieler schlägt auf.
- Wichtig: Der Aufschlag muss diagonal erfolgen – wie im offiziellen Regelwerk.
- Danach wird der Ball abwechselnd hin- und hergespielt.

Laufen:

- Nach jedem Schlag rennt der Spieler direkt zur gegenüberliegenden Seite und stellt sich dort hinten wieder an.
- So rotiert jeder Spieler ständig um die Platte herum.

Fehler (führt zum Ausscheiden):

- Der Ball verfehlt die gegnerische Tischhälfte.
- Der Ball bleibt im Netz hängen.
- Der Ball wird gar nicht getroffen oder zu spät gespielt.
- Der Ball springt zweimal oder wird mit dem Körper berührt.

Ausscheiden:

Wer einen Fehler macht, stellt sich zur Seite und wartet.
Sobald nur noch zwei Spieler übrig sind, folgt ein Endduell – oft „Best of 3“ oder bis zu 5 Punkten.

</p>
    </div>
    <div class="seite1">
      <h1>Seite 1</h1>
      <p>Hier ist Text für Seite 1.</p>
      <img src="dein-bild1.jpg" alt="Bild 1" width="300">
    </div>
    <div class="seite2">
      <h1>Seite 2</h1>
      <p>Hier ist Text für Seite 2.</p>
      <img src="dein-bild2.jpg" alt="Bild 2" width="300">
    </div>
  </div>
  <script>
    const tabs = document.querySelectorAll('.tab');
    const contents = document.querySelectorAll('.content > div');
    tabs.forEach(tab => {
      tab.addEventListener('click', () => {
        // Tabs aktivieren/deaktivieren
        tabs.forEach(t => t.classList.remove('active'));
        tab.classList.add('active');
        // Inhalte anzeigen/verstecken
        contents.forEach(c => c.classList.remove('active'));
        document.querySelector('.' + tab.dataset.tab).classList.add('active');
      });
    });
  </script>
</body>
</html>
