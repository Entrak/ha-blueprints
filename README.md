# ha-blueprints

Home Assistant Blueprints av **Bjørn Magne Slinde** (@entrak)

Dette repoet inneholder ferdige og veltestede Blueprints for Home Assistant, primært laget for automasjon av drivhus, vanning og smarthus-løsninger.

## 🌱 Tilgjengelige Blueprints

### Smart Plantekasse Vanning (v2 - Robust)

Automatisk **pulserende vanning** for opptil 12 plantekasser.

**Funksjoner:**
- Trigger når jordfuktighet har vært under 65 % i 20 minutter
- Pulserende vanning (20 sekunder på / 15 minutter av)
- Mål: 75 % fuktighet (justerbart per instans)
- Innebygd sikkerhetsgrense (maks antall pulser)
- Oppdaterbar persistent notification med live status og syklusnummer
- Robust feilhåndtering av sensorverdier og navngiving (regex-basert)

**Krav:**
- Global master switch: `input_boolean.automatic_watering_system`
- Per plantekasse: `input_boolean.input_boolean_grow_bed_X_watering_enabled` (X = 01–12)
- Egen fuktighetssensor (`sensor.xxx_soil_moisture`) og magnetventil/rele per kasse

### Hvordan importere Blueprinten

1. Gå til **Innstillinger → Blueprints** i Home Assistant
2. Trykk **Import Blueprint**
3. Lim inn denne URL-en:

```
https://raw.githubusercontent.com/Entrak/ha-blueprints/main/blueprints/automation/smart-plantekasse-vanning.yaml
```

Eller bruk den offisielle import-knappen:

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FEntrak%2Fha-blueprints%2Fmain%2Fblueprints%2Fautomation%2Fsmart-plantekasse-vanning.yaml)

### Filplassering i repoet

```
blueprints/automation/smart-plantekasse-vanning.yaml
```

---

## 🚀 Planlagte / Fremtidige Blueprints

Flere Blueprints vil bli lagt til etter hvert, blant annet:
- Drivhus temperatur- og ventilasjonsstyring
- Automatisk ROV / undervannskartlegging
- Lokal LLM / multi-agent integrasjoner (OpenClaw / Hermes)
- Energistyring, lastbalansering og ACER-relaterte automasjoner
- Fjellfoten Vel / lokalpolitikk-relaterte varsler

Har du ønsker eller ideer til nye Blueprints? Ta gjerne kontakt på X (@entrak).

---

## 📄 Bidra

Pull requests er hjertelig velkomne! 
Hvis du lager forbedringer, nye varianter eller egne Blueprints som kan være nyttige for andre, send gjerne en PR.

---

## ⚖️ Lisens & Ansvar

Dette er personlige Blueprints laget for eget bruk. 
Du kan bruke, kopiere og modifisere dem fritt, men på egen risiko. 
Ingen garanti gis for kompatibilitet med alle Home Assistant-oppsett eller hardware.

---

Laget med ❤️, Home Assistant og litt for mye kaffe av [@entrak](https://x.com/entrak)