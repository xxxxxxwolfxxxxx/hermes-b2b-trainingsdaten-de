# Hermes B2B-Trainingsdaten (DE) – kostenlose Vorschau

83 vollständig **KI-generierte, synthetische** deutschsprachige Frage-Antwort-Datensätze aus 5 B2B-Branchen – für **Fine-Tuning und Evaluation von Sprachmodellen**. Kostenlos nutzbar, auch kommerziell.

[![Hugging Face](https://img.shields.io/badge/🤗-Hugging%20Face-yellow)](https://huggingface.co/datasets/xxxxwolfxxxx/hermes-b2b-trainingsdaten-vorschau)
[![Sprache](https://img.shields.io/badge/Sprache-Deutsch-blue)](#)
[![Daten](https://img.shields.io/badge/Datens%C3%A4tze-83-green)](data.jsonl)

> **Das ist die Gratis-Vorschau** eines größeren, kostenpflichtigen Angebots mit insgesamt **917 Datensätzen** über dieselben 5 Branchen. → [Zu den vollständigen Paketen](#vollständige-pakete)

## Inhalt

| Branche | Datensätze (Vorschau) |
|---|---|
| Recht (B2B-Vertragsrecht & Compliance) | 25 |
| Finanzen & Steuern (KMU) | 21 |
| Gesundheitswesen (Praxis-/Einrichtungsverwaltung, **nicht klinisch**) | 17 |
| HR / Personalwesen | 12 |
| Handwerk / KMU-Verwaltung | 8 |
| **Gesamt** | **83** |

Schwierigkeitsgrade: 72 × `mittel`, 11 × `komplex`.

## Datenformat

JSONL, ein Datensatz pro Zeile ([`data.jsonl`](data.jsonl)):

| Feld | Beschreibung |
|---|---|
| `branche` | B2B-Branche des Datensatzes |
| `thema` | Kurzes Thema / Titel des Szenarios |
| `szenario` | Ausgangssituation / Kontext |
| `frage` | Die gestellte Frage |
| `antwort` | Vollständige, ausformulierte Antwort |
| `schwierigkeitsgrad` | `mittel` oder `komplex` |
| `quellenhinweis` | Hinweis auf die synthetische Herkunft |

### Beispiel (gekürzt)

```json
{
  "branche": "Finanzen & Steuern (KMU)",
  "thema": "Reisekostenabrechnung (Einzelunternehmen)",
  "szenario": "Sie führen ein Einzelunternehmen mit 15 Mitarbeitenden und sind als Inhaber regelmäßig für Dienstreisen im Inland unterwegs. ...",
  "frage": "Welche Reisekosten können Sie als Einzelunternehmer steuerlich abziehen und wie müssen die Abrechnungen dokumentiert werden, ...?",
  "antwort": "Als Einzelunternehmer können Sie Reisekosten als Betriebsausgaben geltend machen, sofern sie geschäftlich veranlasst sind. ...",
  "schwierigkeitsgrad": "mittel",
  "quellenhinweis": "synthetisch, KI-generiert, keine Rechts-/Steuer-/Medizinberatung im Einzelfall"
}
```

## Laden

```python
from datasets import load_dataset

ds = load_dataset("xxxxwolfxxxx/hermes-b2b-trainingsdaten-vorschau", split="train")
print(ds[0]["frage"])
```

Oder direkt aus diesem Repo:

```python
import json

with open("data.jsonl", encoding="utf-8") as f:
    rows = [json.loads(line) for line in f]
```

## Herkunft und Qualität

- **Vollständig synthetisch:** Alle Inhalte wurden von einem KI-Modell neu erzeugt – nicht aus fremden Webseiten, Dokumenten oder Datenbanken kopiert oder gescraped. Keine realen Personen, Firmen oder Fälle.
- **Automatisiert geprüft:** Schema, Sprache und Duplikate werden vor Aufnahme ins Paket automatisiert kontrolliert.
- **Keine Beratung:** Die Datensätze sind Trainingsmaterial. Sie sind **keine** Rechts-, Steuer- oder medizinische Beratung und keine fachlich geprüfte Auskunft für einen Einzelfall. Einzelne Angaben können unvollständig oder unzutreffend sein.

## Vollständige Pakete

Die Vorschau zeigt nur einen Ausschnitt. Das gesamte Angebot (917 Datensätze) gibt es einzeln pro Branche oder im Komplettpaket (Preis · Anzahl Datensätze):

| Branche | Starter | Professional | Complete |
|---|---|---|---|
| [Recht](https://xxxxwolfxxxx.gumroad.com/l/xcidy) | [12 € · 69](https://xxxxwolfxxxx.gumroad.com/l/xcidy) | [34 € · 165](https://xxxxwolfxxxx.gumroad.com/l/fcynzo) | [69 € · 275](https://xxxxwolfxxxx.gumroad.com/l/lqgecq) |
| [Finanzen & Steuern](https://xxxxwolfxxxx.gumroad.com/l/jiepno) | [12 € · 57](https://xxxxwolfxxxx.gumroad.com/l/jiepno) | [34 € · 137](https://xxxxwolfxxxx.gumroad.com/l/mmaultq) | [69 € · 229](https://xxxxwolfxxxx.gumroad.com/l/fandq) |
| [Gesundheitswesen](https://xxxxwolfxxxx.gumroad.com/l/xdnlzk) | [12 € · 46](https://xxxxwolfxxxx.gumroad.com/l/xdnlzk) | [34 € · 110](https://xxxxwolfxxxx.gumroad.com/l/ikcjnt) | [69 € · 183](https://xxxxwolfxxxx.gumroad.com/l/cteqfu) |
| [HR / Personalwesen](https://xxxxwolfxxxx.gumroad.com/l/liqlc) | [12 € · 34](https://xxxxwolfxxxx.gumroad.com/l/liqlc) | [34 € · 83](https://xxxxwolfxxxx.gumroad.com/l/dqiok) | [69 € · 138](https://xxxxwolfxxxx.gumroad.com/l/ghlea) |
| [Handwerk / KMU](https://xxxxwolfxxxx.gumroad.com/l/vnizit) | [12 € · 23](https://xxxxwolfxxxx.gumroad.com/l/vnizit) | [34 € · 55](https://xxxxwolfxxxx.gumroad.com/l/segixv) | [69 € · 92](https://xxxxwolfxxxx.gumroad.com/l/poorjd) |

**[→ All-Access-Bundle: alle 917 Datensätze für 179 €](https://xxxxwolfxxxx.gumroad.com/l/mhcku)**
· [Gumroad-Shop](https://xxxxwolfxxxx.gumroad.com) · [Gratis-Vorschau auf Gumroad](https://xxxxwolfxxxx.gumroad.com/l/balpkl)

## Lizenz

Diese Vorschau (83 Datensätze) darf – auch kommerziell – zum Training, Fine-Tuning, Evaluieren und Benchmarken genutzt, verarbeitet und öffentlich weitergegeben werden (auch in öffentlichen Repositories), **solange der Hinweis auf die Originalquelle (Hermes Trainingsdaten, xxxxwolfxxxx.gumroad.com) und der Link zu den kostenpflichtigen Paketen erhalten bleiben.** Vollständiger Text: [LICENSE.txt](LICENSE.txt).

Die kostenpflichtigen Pakete unterliegen einer eigenen, strengeren Lizenz (keine Weitergabe der Rohdaten).

## Kontakt

Fragen zu Lizenz, individuellen Datenmengen oder Kooperationen: hebebuehnenboizenburg@gmail.com

---

## English summary

**Hermes B2B Training Data (DE) – free preview.** 83 fully synthetic, AI-generated German question-answer records across 5 B2B domains (business law & compliance, finance & tax for SMEs, healthcare administration – *non-clinical*, HR, trades/SME administration), intended for fine-tuning and evaluating language models.

- **Format:** JSONL with the fields `branche`, `thema`, `szenario`, `frage`, `antwort`, `schwierigkeitsgrad`, `quellenhinweis`.
- **Origin:** generated from scratch by an AI model; not scraped. Not legal, tax or medical advice; individual answers may be incomplete or inaccurate.
- **License:** free for commercial and non-commercial use, including public redistribution, provided the attribution to the original source and the link to the paid packages are kept (see [LICENSE.txt](LICENSE.txt)).
- **Also on Hugging Face:** [xxxxwolfxxxx/hermes-b2b-trainingsdaten-vorschau](https://huggingface.co/datasets/xxxxwolfxxxx/hermes-b2b-trainingsdaten-vorschau)
- **Full dataset:** 917 records in total, sold per domain or as an [All-Access bundle (€179)](https://xxxxwolfxxxx.gumroad.com/l/mhcku) – see the [shop](https://xxxxwolfxxxx.gumroad.com). Contact: hebebuehnenboizenburg@gmail.com
