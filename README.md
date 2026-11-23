# SVT Toranalyse v6

## Update ohne Datenverlust
1. In der aktuellen App unter Daten ein Backup exportieren.
2. index.html, app.js, style.css, manifest.webmanifest, sw.js und icons bei GitHub ersetzen.
3. Nichts unter Daten zurücksetzen. Die App verwendet weiterhin localStorage-Key svt-v4; bestehende Bewertungen bleiben erhalten.

## BFV-Sync
`worker-bfv.js` ist ein vorbereiteter Cloudflare Worker. Er erkennt BFV-Spielseiten und liefert Diagnoseinformationen. Die automatische Übernahme von Torereignissen ist als Beta gekennzeichnet, weil BFV-Markup und Zugriff variieren können. Worker bereitstellen, URL mit `/api/bfv` in der App speichern und Diagnose prüfen. Fehlende Torzeiten werden nie geschätzt.

BFV-Team: https://www.bfv.de/mannschaften/016Q53TGR4000000VV0AG80NVS35AO43
