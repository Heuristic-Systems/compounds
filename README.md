# APLM Master Compounds

**18 master compound definitions** for the Atomised Pedagogical Layer Model (APLM).

Each file (`CP-*.json`) is a consolidated compound following schema v4.0.0:
- One compound per agent (1:1 mapping)
- Each compound contains `phases[]` — one phase per original compound
- Every phase has a `was` field tracing back to the original compound ID
- Phases reference Elements via `calls_elements[]`

## Files

| File | Agent | Layer | Phases |
|------|-------|-------|--------|
| `CP-CLEA.json` | CLEA | L03 | 9 |
| `CP-CS.json` | CS | L01 | 8 |
| `CP-CSA.json` | CSA | L02 | 10 |
| `CP-ETHCORE.json` | ETHCORE | L04 | 10 |
| `CP-HICE.json` | HICE | L07 | 13 |
| `CP-HOA.json` | HOA | L06 | 10 |
| `CP-LODA.json` | LODA | L01 | 8 |
| `CP-LOPA.json` | LOPA | L01 | 7 |
| `CP-MIA.json` | MIA | L05 | 4 |
| `CP-MP1.json` | MP1 | MP01 | 19 |
| `CP-MP2.json` | MP2 | MP02 | 15 |
| `CP-MP3.json` | MP3 | MP03 | 46 |
| `CP-MP4.json` | MP4 | MP04 | 34 |
| `CP-MP5.json` | MP5 | MP05 | 26 |
| `CP-MP6.json` | MP6 | MP06 | 8 |
| `CP-MSA.json` | MSA | L05 | 9 |
| `CP-PER.json` | Personality | L01/Personality | 5 |
| `CP-SFE.json` | SFE | L08 | 12 |

## Schema

```json
{
  "compound_id": "CP-{AGENT}",
  "compound_name": "...",
  "implements_construct": "K-{AGENT}",
  "version": "4.0.0",
  "phases": [
    {
      "phase_id": "PH-{ID}",
      "was": "{original_compound_id}",
      "calls_elements": ["E-..."],
      "decision_outputs": {...}
    }
  ],
  "cross_agent_handoffs": {...},
  "failure_modes": [...]
}
```

## Source

Consolidated from the [APLM ontology](https://github.com/Heuristic-Systems) as part of the N→1 compound consolidation (Feb 2026).
