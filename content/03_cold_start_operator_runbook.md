---
title: Cold-Start Operator Runbook
version: v0
license: CC BY 4.0
---

<!--
SOURCE_PRS: #143 (cold_start_operator_runbook + workstation_readme)
CONSOLIDATION_TYPE: source unique #143 (runbook en corps, README workstation absorbé en intro contextuelle)
ANONYMIZATION_PASS: 5c.3 (P1 → [operator]/[stakeholder])
P4_MICROFILTER_PASS: 5c.3 (possessif_exposant + ref_meta_interne)
LICENSE: CC BY 4.0
EXTERNAL_ALIGNMENT_PASS: 5c.3.b (1B + 2A + 3A + 4B applied)
SOURCE_FILES: 03b_cold_start_operator_runbook__src.md (body) + 03a_asso_workstation_readme__src.md (intro)
-->
# Cold-Start Operator Runbook v0

## Contexte Workstation

### ASSO Workstation Product Index

Surfaces produit utiles pour reprise froide:

- [Cold start operator runbook](./asso_workstation_cold_start_operator_runbook_v0.md)
- [Local refresh prep](./asso_workstation_local_refreshable_readonly_prep_v0.md)
- [Local launcher](./asso_workstation_local_launcher_v0.md)
- [One-click entrypoint](./asso_workstation_one_click_entrypoint_v0.md)
- [Static snapshot sync to UI](../../project_governance/ace_board_static_snapshot_sync_to_ui_v0.md)

Posture:

- local
- manual
- visible
- no permission-to-act
- `local / manual / visible / non-live / no-permission-to-act`

---

## Statut

- Front: `ASSO_WORKSTATION_COLD_START_OPERATOR_RUNBOOK_INDEX_V0` *(internal identifier)*
- Etat courant: `USABLE_LOCAL_ONE_CLICK_ENTRYPOINT_V0` *(internal identifier)*
- Posture: `local / manual / visible / non-live / no-permission-to-act`

## Ou commencer

Commencer au repo root:

- `<repo_root>/asso-execution-bridge`

Point d'entree principal:

- `Start_ASSO_Workstation_Local_v0.cmd`

## Commandes

Commande principale:

```powershell
Start_ASSO_Workstation_Local_v0.cmd
```

Commande preflight:

```powershell
Start_ASSO_Workstation_Local_v0.cmd -PreflightOnly
```

Launcher PowerShell direct:

```powershell
powershell -ExecutionPolicy Bypass -File scripts/start_asso_workstation_local_v0.ps1
```

## Prérequis

Pré-requis locaux connus:

- `git`
- `python`
- `node`
- `npm`

Le launcher n'installe rien automatiquement.

Si `node_modules` ou `vite` sont absents dans une app:

- le preflight peut rester utile
- le launch reel des UIs peut ne pas partir
- une instruction humaine `npm install` peut etre affichee
- cette instruction n'est pas une installation automatique

## URLs attendues

- ACE Board Control Room: `http://127.0.0.1:5174/`
- ASSO Operations Floor: `http://127.0.0.1:5175/`

## Ce qu'il faut vérifier

Verifier en reprise froide:

1. le repo root est correct
2. le preflight s'exécute sans lancer de serveur
3. les URLs attendues sont affichees
4. aucune revendication live, runtime live ou permissionnelle n'apparait
5. le launch reel, si tente, ouvre des fenetres PowerShell visibles seulement

## Fermeture et relance

Pour fermer:

- fermer manuellement les fenetres PowerShell visibles

Pour relancer:

- revenir au repo root
- relancer `Start_ASSO_Workstation_Local_v0.cmd`
- ou relancer le launcher PowerShell direct

## Ce que le système ne prouve pas

Ne pas croire que ce chemin prouve:

- live
- runtime live
- current repo truth
- donnees marche courantes
- trading-ready
- permission-to-act
- autonomie

## Boundaries

- `NO LIVE`
- `NO RUNTIME LIVE`
- `NO FETCH`
- `NO WEBSOCKET`
- `NO DAEMON`
- `NO WATCHER`
- `NO PROVIDER`
- `NO SECRETS`
- `NO WALLET`
- `NO TRADING`
- `NO DEX`
- `NO LEVERAGE`
- `NO ORDER ROUTING`
- `NO MEMORY_WRITE`
- `NO LEDGER_WRITE`
- `NO PERMISSION_TO_ACT`
- `NO AUTONOMOUS DECISION`
- `NO DASHBOARD_LIVE_CLAIM`
- `NO DEPENDENCY INSTALL BY DEFAULT`
- `NO WINDOWS STARTUP REGISTRATION`
- `NO REGISTRY MUTATION`
- `NO HIDDEN BACKGROUND PROCESS`

## Références

- `README_RUN.md`
- `docs/product/asso_workstation/asso_workstation_local_launcher_v0.md`
- `docs/product/asso_workstation/asso_workstation_one_click_entrypoint_v0.md`
- `docs/project_checkpoints/2026-05-06_asso_workstation_one_click_entrypoint_closeout_v0.md`
