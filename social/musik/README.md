# YellowBlue Reel-Musik

Musikbibliothek für YellowBlue-Reels. Alle Stücke wurden am 21.11.2026 mit ElevenLabs
(Modell `eleven_music_v2_5`) während Bennys bezahltem ElevenLabs-Abo erzeugt. Laut ElevenLabs
gilt die kommerzielle Lizenz für Inhalte aus einem Abo auch nach dessen Ende weiter
(Hilfe-Artikel „What happens to my content after my subscription ends?“). Ab Dezember 2026
gibt es kein ElevenLabs-Abo mehr: **Neue Musik wird nicht mehr erzeugt, Reels nehmen ihre
Musik aus diesem Ordner.**

## Stücke

| Datei | Stimmung | Tempo | Länge | Passt zu |
| --- | --- | --- | --- | --- |
| `01-synthpop-118bpm.mp3` | hell, optimistisch, neugierig (Synth-Pop) | 118 BPM | 2:30 | Werkzeuge, Erklär-Reels, allgemein |
| `02-quizshow-124bpm.mp3` | verspielt, leicht spannend, tickende Hi-Hats | 124 BPM | 2:00 | Donnerstags-Quiz, Prüfungsaufgabe (Di) |
| `03-lofi-85bpm.mp3` | ruhig, konzentriert (Lo-Fi, Rhodes) | 85 BPM | 3:00 | Prüfungsaufgabe (Di), Lerninhalte |
| `04-ukulele-108bpm.mp3` | fröhlich, freundlich (Ukulele, Glockenspiel) | 108 BPM | 2:30 | Byte-Reels, Community, leichte Themen |
| `05-techhouse-124bpm.mp3` | treibend, energiegeladen (Tech-House) | 124 BPM | 3:00 | Ankündigungen, Sonder-Reels, schnelle Schnitte |
| `06-ambient-100bpm.mp3` | ruhig, klar, nachdenklich (Ambient) | 100 BPM | 3:00 | Betrugsmasche, Sicherheit, ernste Themen |
| `07-funk-112bpm.mp3` | locker, selbstbewusst (Funk, Slap-Bass) | 112 BPM | 3:00 | Alltags-IT, Quiz (Abwechslung) |
| `08-aufbruch-110bpm.mp3` | erst ruhig, dann aufsteigend, „Aha-Moment“ | 110 BPM | 3:00 | Auflösungen, Spickzettel, Erfolgsmomente |

## Regeln für den Einsatz

1. **Startpunkt:** Immer ab Sekunde 0 schneiden (`-ss 0`). Die ersten 10 Sekunden jedes Stücks
   hat Benny am 24.11.2026 per Hörprobe geprüft: alle 8 Stücke freigegeben (kein Gesang,
   passend). Andere Startpunkte erst nach seiner Freigabe.
2. **Abwechslung:** Ein Stück höchstens einmal pro Woche und nicht in zwei Wochen hintereinander
   für dasselbe Format. Welches Stück lief, steht im Wochen-Tab (KW NN) des Konzept-Dokuments
   in der Zeile „Musik:“ je Reel.
3. **Mischen** (ffmpeg): `-map 0:v -map 1:a -c:v copy`, Audio auf Videolänge kürzen
   (`-shortest` bzw. `atrim`), 0,5 s Fade-out am Ende, `volume=-1dB`, AAC 192k, 44,1 kHz.
   Prüfen: Videodauer unverändert, Audiospur vorhanden.
4. **Pfad im Buffer-Workflow:** Lokal aus dem geklonten Repo nehmen
   (`social/musik/<datei>.mp3`). Eine öffentliche URL braucht die Musik nicht, sie steckt
   danach im Video.
5. Keine Musik aus anderen Quellen (keine Gratis-Suno-Songs, keine Trend-Sounds über Buffer).

## Herkunft

ElevenLabs-Flow „hpL12Zf1TJb3nI1ecXGj“ (Workspace von Benny). Ein neuntes Stück
(Spannung/Suspense) ist am 21.11.2026 wegen aufgebrauchter Credits nicht entstanden.
