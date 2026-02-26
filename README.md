# APLM Master Constructs & Compounds

**18 master construct files** (`K-*.json`) and **18 master compound files** (`CP-*.json`) for the Atomised Pedagogical Layer Model (APLM).

Schema v4.0.0 — one construct + one compound per agent (1:1:1 mapping).

## Constructs (`K-*.json`)

Each construct contains `sections[]` — one section per original construct. Every section has a `was` field tracing back to the original construct ID.

## Compounds (`CP-*.json`)

Each compound contains `phases[]` — one phase per original compound. Every phase has a `was` field tracing back to the original compound ID. Phases reference Elements via `calls_elements[]`.

## Files

| Agent | Construct | Sections | Compound | Phases | Layer |
|-------|-----------|----------|----------|--------|-------|
| LOPA | `K-LOPA.json` | 7 | `CP-LOPA.json` | 7 | L01 |
| LODA | `K-LODA.json` | 8 | `CP-LODA.json` | 8 | L01 |
| CogniStruct | `K-CS.json` | 8 | `CP-CS.json` | 8 | L01 |
| Personality | `K-PER.json` | 5 | `CP-PER.json` | 5 | L01/Personality |
| CSA | `K-CSA.json` | 10 | `CP-CSA.json` | 10 | L02 |
| CLEA | `K-CLEA.json` | 9 | `CP-CLEA.json` | 9 | L03 |
| EthicalCore | `K-ETHCORE.json` | 10 | `CP-ETHCORE.json` | 10 | L04 |
| MSA | `K-MSA.json` | 9 | `CP-MSA.json` | 9 | L05 |
| MIA | `K-MIA.json` | 4 | `CP-MIA.json` | 4 | L05 |
| HOA | `K-HOA.json` | 11 | `CP-HOA.json` | 10 | L06 |
| HICE | `K-HICE.json` | 13 | `CP-HICE.json` | 13 | L07 |
| SFE | `K-SFE.json` | 12 | `CP-SFE.json` | 12 | L08 |
| MP1 | `K-MP1.json` | 6 | `CP-MP1.json` | 19 | MP01 |
| MP2 | `K-MP2.json` | 5 | `CP-MP2.json` | 15 | MP02 |
| MP3 | `K-MP3.json` | 8 | `CP-MP3.json` | 46 | MP03 |
| MP4 | `K-MP4.json` | 6 | `CP-MP4.json` | 34 | MP04 |
| MP5 | `K-MP5.json` | 8 | `CP-MP5.json` | 26 | MP05 |
| MP6 | `K-MP6.json` | 8 | `CP-MP6.json` | 8 | MP06 |

## Schema

### Construct
```json
{
  "construct_id": "K-{AGENT}",
  "construct_name": "...",
  "version": "4.0.0",
  "guides_compound": "CP-{AGENT}",
  "sections": [
    { "section_id": "S-{ID}", "was": "{original_id}", ... }
  ]
}
```

### Compound
```json
{
  "compound_id": "CP-{AGENT}",
  "compound_name": "...",
  "version": "4.0.0",
  "implements_construct": "K-{AGENT}",
  "phases": [
    { "phase_id": "PH-{ID}", "was": "{original_id}", "calls_elements": [...] }
  ]
}
```

## Source

Consolidated from the APLM ontology as part of the N→1 construct/compound consolidation (Feb 2026).
