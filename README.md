# Compact Dark Gradient Themes

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://hacs.xyz/)
[![Validate](https://github.com/rvdlinden/HA-Themes/actions/workflows/validate.yml/badge.svg)](https://github.com/rvdlinden/HA-Themes/actions/workflows/validate.yml)

Drie compacte, donkere Home Assistant-themes met een platte, matte kaartstijl
en een subtiele gradient-glow linksboven op de kaartrand.

| Theme | Hoofdkleur | Secundair accent |
|---|---|---|
| **Compact Dark Lime Gradient** | `#aeea00` lime | `#6366f1` indigo |
| **Compact Dark Violet Gradient** | `#7c4dff` violet | `#00c8d4` cyaan |
| **Compact Dark Electric Blue Gradient** | `#00b0ff` electric blue | `#e040fb` magenta |

## Kenmerken

- Donkere achtergrond met een radiale gradient op het dashboard-canvas
  (`lovelace-background`); sidebar en dialogen blijven vlak.
- Platte, matte kaarten (radius 3px, geen schaduw) met een gradient-rand.
- Volledig gethemede invoervelden, dropdowns, kaart-/YAML-editor en dialogen.
- Kleurpalet voor HA 2025.8+ (`ha-color-primary-*`) en grafiekkleuren.
- Afgestemde syntax-highlighting per theme.
- Compacte rijen (32px) en compactere kaart-padding via card-mod.

## Vereisten

- Home Assistant **2025.8** of nieuwer (voor het nieuwe kleurpalet; oudere
  versies werken grotendeels, maar negeren die variabelen).
- [card-mod](https://github.com/thomasloven/lovelace-card-mod) (via HACS) voor
  de compacte rijen en de kaart-styling. Zonder card-mod werken de kleuren wel,
  maar niet de compacte layout.

## Installatie

### Via HACS (aanbevolen)

1. Open HACS in Home Assistant.
2. Menu (⋮) → **Custom repositories**.
3. Voeg `https://github.com/rvdlinden/HA-Themes` toe met type **Theme**.
4. Zoek **Compact Dark Gradient Themes** en klik op **Download**.
5. Zorg dat themes geladen worden in `configuration.yaml`:

   ```yaml
   frontend:
     themes: !include_dir_merge_named themes
   ```

6. Herstart Home Assistant (of roep de actie `frontend.reload_themes` aan).
7. Kies het theme via **Profiel** → **Thema**.

### Handmatig

Kopieer `themes/compact-dark-gradient.yaml` naar de map `themes/` in je
Home Assistant-configuratie en volg daarna stap 5 t/m 7 hierboven.

## Aanpassen

De kaartrand-glow en afronding zijn per theme af te stellen in
`ha-card-background` en `ha-card-border-radius`; de commentaarblokken in het
YAML-bestand beschrijven welke waarden je waarvoor aanpast.

> **Let op:** `card-mod-theme` moet exact gelijk zijn aan de themanaam.
> Hernoem je een theme, pas dan ook die waarde aan, anders wordt de
> card-mod-styling niet toegepast.

## Licentie

[MIT](LICENSE)
