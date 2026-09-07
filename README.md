# Savs meistars — priekšlikumu vāks

Viena lapa, kas saliek blakus četras mājaslapas dizaina versijas, lai pasūtītājam jāsūta viena saite, nevis četras. Katrs variants redzams vesels, no augšas līdz apakšai, un attēls ir saite uz dzīvo versiju.

Publicēts: https://lavrinovich86.github.io/versijas/

## Saturs

- `index.html` — visa lapa, stili iekļauti pašā failā.
- `assets/v1…v4.webp` — pilnas lapas priekšskati, 600 px plati, pārmēroti no katras versijas `desktop-preview.png` ar Lanczos filtru.
- `assets/archivo-*.woff2` — Archivo, latin un latin-ext apakškopas, glabātas lokāli, lai lapa nav atkarīga no Google Fonts. Licence: `assets/Archivo-OFL.txt`.
- `assets/favicon.svg` — logo zīme no pirmās versijas.
- `robots.txt` un `<meta name="robots">` — lapa netiek pieteikta meklētājiem, jo tajā ir uzņēmuma īstie kontakti un tā vēl nav apstiprināta publiskošanai. Saite darbojas ikvienam, kam to nosūta.

## Versijas

| # | Virsraksts | Repozitorijs |
|---|---|---|
| 01 | Jūsu iecerei. Mūsu meistarība. | [savs-meistars](https://github.com/lavrinovich86/savs-meistars) |
| 02 | Viss sākas ar labu plānu. | [savs-meistars-v2](https://github.com/lavrinovich86/savs-meistars-v2) |
| 03 | Labs darbs. Stingrs pamats. | [savs-meistars-v3](https://github.com/lavrinovich86/savs-meistars-v3) |
| 04 | Telpa labākai ikdienai. | [savs-meistars-v4](https://github.com/lavrinovich86/savs-meistars-v4) |

## Priekšskatu atjaunošana

Ja kādā versijā mainās dizains, pārtaisa tās priekšskatu un pārraksta attiecīgo `assets/vN.webp`:

```
magick ../savs-meistars-vN/desktop-preview.png -filter Lanczos -resize 600x -quality 80 assets/vN.webp
```

Ja mainās arī attēla augstums, jāsalabo `width`/`height` atribūti `index.html`, citādi lapa ielādes laikā palēks.
