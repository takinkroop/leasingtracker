# Leasingtracker · Polestar 3 EN48110

Personlig webapp for å spore kilometerstand og holde oversikt over leasingavtalen.

## Hva ligger her

- `index.html` — selve appen (HTML + CSS + JS i én fil)
- `setup.sql` — oppretter tabell og legger inn eksisterende datapunkter i Supabase

## Avtaledetaljer (i index.html)

- Bil: Polestar 3
- Reg.nr: EN48110
- Leasingstart: 23.05.2025
- Leasingslutt: 23.05.2028 *(antatt 3-årig avtale — endre `CONTRACT.endDate` i index.html om annerledes)*
- Inkludert: 75 000 km
- Pris pr overkjørt km: 2,50 kr

## Slik fungerer det

1. Avlesninger lagres i Supabase-tabellen `readings`
2. Appen henter alle avlesninger og regner ut snitt, prognose og avvik mot ideallinjen
3. Statusbanneret viser om du er på rute, foran eller bak budsjett
4. Grafen viser faktisk kjørelengde vs ideallinjen vs prognose

## Endre avtaledetaljer senere

Åpne `index.html`, finn `const CONTRACT = {…}` øverst i `<script>`-blokken og endre verdiene.
