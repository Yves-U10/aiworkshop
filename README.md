# aiworkshop

AI Workshop - OpenEdge ABL Project.

This repository contains the ProjectGengar workshop code (Step-16), an OpenEdge ABL (12.8) GUI application built on the **Business Entity** pattern against the `sports2000` database.

## Structure

| Path | Contents |
|------|----------|
| `src/business/` | Business entities (`CustomerEntity.cls`), the singleton `EntityFactory.cls` and dataset includes (`CustomerDataset.i`) |
| `src/*.w` | AppBuilder GUI windows (`CustomerWin.w`, `ItemWin.w`) |
| `doc/business-entity-pattern.md` | Architecture and refactoring guide for the Business Entity pattern |
| `dump/sports2000-schema.txt` | Summary of the sports2000 database schema |
| `.windsurf/rules/` | AI assistant rules (ABL syntax, buffers, schema) |
| `.windsurf/workflows/` | AI assistant workflows (new class/method/property/constructor) |
| `openedge-project.json`, `build.xml` | OpenEdge project and PCT build configuration |

## Getting started

1. Install OpenEdge 12.8 and set `DLC`.
2. Create the sports2000 database: `ant db` (uses PCT, see `build.xml`).
3. Open the folder in an OpenEdge-aware editor; `openedge-project.json` defines the PROPATH and DB connection (`-db db/sports2000 -ld sp2k`, alias `sports`).
4. Run `src/CustomerWin.w` or `src/ItemWin.w`.
