# Raport Vanzari Dr. Ardeleanu Dental Clinics

Site privat cu rapoartele lunare de vanzari, protejat cu parola.

**URL:** https://vladtm75.github.io/raport-sales-dr-ardeleanu/

## Structura

- `index.html` — ecran de parola + rutare automata (desktop/mobil, dupa dispozitiv)
- `desktop.html` — raportul complet (dashboard React + Recharts)
- `mobile.html` — varianta lite pentru telefon
- `logo.png` — logo oficial Dr. Ardeleanu

Ambele pagini au buton de comutare desktop <-> mobil (dreapta-jos).

## Actualizare lunara

1. Inlocuieste continutul din `desktop.html` (sectiunea `<script type="text/babel">`) cu noul raport JSX — pastreaza scriptul de autentificare din `<head>` si butonul `#switchbtn`.
2. Inlocuieste `mobile.html` cu noua varianta mobila — pastreaza scriptul de autentificare din `<head>` si butonul `#switchbtn` de dinainte de `</body>`.
3. Schimba parola lunara in `index.html`: constanta `HASH` = SHA-256 (hex) al noii parole (ex. `ArdeleanuAugust`). Hash-ul se genereaza cu: `echo -n 'ParolaNoua' | sha256sum`.
4. Actualizeaza textul lunii in `index.html` (subtitlul cardului).

Nota: parola este un gate simplu in JavaScript (hash SHA-256 in pagina). Repo-ul este public — nu stoca aici date sensibile suplimentare.
