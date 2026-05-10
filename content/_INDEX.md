# content/_INDEX.md

Index post-consolidation, mission 5c.3. Source : content_raw/ (mission 5c.2). 5 fichiers consolidés finaux.

## Fichiers consolidés

| Destination | Type | Sources | P1 remplacements | P4 possessif_exposant | P4 ref_meta_interne | Total P4 | Taille |
|-------------|------|---------|------------------|-----------------------|---------------------|----------|--------|
| `01_oom_recovery_sop.md` | 3B | #81, #82, #83 | 0 | 0 | 0 | 0 | 5612 b |
| `02_pr_final_audit_head_guard_sop.md` | 3B+arbitration | #87, #88, #89, #90 | 0 | 0 | 0 | 0 | 4774 b |
| `03_cold_start_operator_runbook.md` | source unique | #143 | 1 | 0 | 0 | 0 | 3922 b |
| `04_agent_handoff_format.md` | source unique | #27 | 0 | 0 | 0 | 0 | 3441 b |
| `05_operator_guide.md` | 4A | #31 | 3 | 0 | 0 | 0 | 12480 b |

## Récapitulatif global

- Total fichiers consolidés : 5
- Total remplacements P1 (anonymisation [operator]/[stakeholder]) : **4**
- Total balises `<<<REVIEW_HICHEM_P4>>>` posées (microfiltrage) : **0**
- Taille cumulée des fichiers consolidés : 30229 octets (29.5 KB)

## Mission suivante (5c.5b ciblée)

Le mainteneur reviewera chaque balise `<<<REVIEW_HICHEM_P4>>>` posée (motifs `possessif_exposant` ou `ref_meta_interne`) et tranchera : conserver tel quel (méthode portable acceptée), reformuler la phrase pour retirer la référence interne, supprimer la ligne, ou remplacer le token MAJUSCULES_SNAKE_CASE par un placeholder neutre. Aucun arbitrage tranché à ce stade.

---

## Patch 5c.3.b — Alignement externe CC BY 4.0

Patch 5c.3.b appliqué : alignement CC BY 4.0 (1B), placeholder repo path (2A), neutralisation tokens internes (3A), H1 nettoyés (4B).

### H1 finaux par fichier (premier H1 du body) — post-5c.3.c

| Fichier | H1 final | Statut PHASE D |
|---------|----------|----------------|
| `01_oom_recovery_sop.md` | `# OOM Recovery SOP v0` | nettoyé en 5c.3.b (préfixe `Capital Engine - Documentation Operatoire` retiré, suffixe ` Closeout` retiré) |
| `02_pr_final_audit_head_guard_sop.md` | `# PR Final Audit And Head Guard SOP v0` | nettoyé en 5c.3.b |
| `03_cold_start_operator_runbook.md` | `# Cold-Start Operator Runbook v0` | nettoyé en 5c.3.c (top H1 ajouté depuis frontmatter+scope ; ancien H1 `# ASSO Workstation Product Index` rétrogradé en H3, ancien H1 redondant `# ASSO Workstation Cold Start Operator Runbook v0` retiré) |
| `04_agent_handoff_format.md` | `# Agent Handoff Format v0` | nettoyé en 5c.3.c (alignement H1↔frontmatter, BOM U+FEFF retiré) |
| `05_operator_guide.md` | `# Operator Guide — Avatar Text-Only Stack v0` | conservé sans modification, déjà propre |

### Balises `<<<REVIEW_HICHEM_5c3b>>>` posées et résolues

État après mission 5c.3.d (toutes les balises résolues, dernière par arbitrage maintainer + Zone A control tower en Zone A) :

| Fichier | Balises 5c.3.b posées | Résolues 5c.3.c | Résolues 5c.3.d | Restantes |
|---------|----------------------:|----------------:|----------------:|----------:|
| `01_oom_recovery_sop.md` | 7 | 6 | 1 | 0 |
| `02_pr_final_audit_head_guard_sop.md` | 1 | 1 | 0 | 0 |
| `03_cold_start_operator_runbook.md` | 2 | 2 | 0 | 0 |
| `04_agent_handoff_format.md` | 0 | 0 | 0 | 0 |
| `05_operator_guide.md` | 1 | 1 | 0 | 0 |
| **Total** | **11** | **10** | **1** | **0** |

Détail par classe :
- `MECHANICAL_SAFE_FIX` (5c.3.c) : 3 balises résolues (01 ligne 34 token MERGED, 01 ligne 98 et 02 ligne 23 équivalents français)
- `FALSE_POSITIVE_REMOVE` (5c.3.c) : 7 balises résolues (toutes les "non-live" opérationnels confirmés par les boundary lists du même document)
- `HUMAN_ARBITRATION_RESOLVED` (5c.3.d, arbitrage maintainer + Zone A control tower Zone A) : 1 balise résolue. Le token `CLOSED_INTERNAL_PROOF_ONLY_OOM_RECOVERY_SOP_V0` a été converti en formulation naturelle historique `source closeout status: closed as internal proof model candidate`, en cohérence avec la nouvelle séparation source/pack appliquée au file 01.

Détail des règles et de l'arbitrage : voir `docs/project_evidence/sop_pack_5c3c_content_repair_and_5c4_scaffold_v0/review_resolution_report.md`.

### Volumétrie post-5c.3.b

| Fichier | Taille avant (5c.3) | Taille après (5c.3.b) | Δ |
|---------|---------------------|-----------------------|---|
| `01_oom_recovery_sop.md` | 5612 b | 5427 b | -185 b (-3.3 %) |
| `02_pr_final_audit_head_guard_sop.md` | 4774 b | 4424 b | -350 b (-7.3 %) |
| `03_cold_start_operator_runbook.md` | 3922 b | 4041 b | +119 b (+3.0 %) |
| `04_agent_handoff_format.md` | 3441 b | 3501 b | +60 b (+1.7 %) |
| `05_operator_guide.md` | 12480 b | 12612 b | +132 b (+1.1 %) |
| **Total** | **30229 b** | **30005 b** | **-224 b (-0.7 %)** |

Aucun fichier ne dépasse le seuil de -30 % de volumétrie (pas de sur-suppression).

### Volumétrie post-5c.3.c

| Fichier | Taille 5c.3.b | Taille 5c.3.c | Δ vs. 5c.3.b |
|---------|--------------:|--------------:|--------------|
| `01_oom_recovery_sop.md` | 5 427 b | 5 175 b | -252 b (-4.6 %) |
| `02_pr_final_audit_head_guard_sop.md` | 4 424 b | 4 392 b | -32 b (-0.7 %) |
| `03_cold_start_operator_runbook.md` | 4 041 b | 3 946 b | -95 b (-2.4 %) |
| `04_agent_handoff_format.md` | 3 501 b | 3 494 b | -7 b (-0.2 %, BOM 3 b + H1 4 b nets) |
| `05_operator_guide.md` | 12 612 b | 12 572 b | -40 b (-0.3 %) |
| **Total** | **30 005 b** | **29 579 b** | **-426 b (-1.4 %)** |

---

## Patch 5c.3.d — Status alignment + distribution files DRAFT

Patch 5c.3.d appliqué : arbitrage de la dernière balise REVIEW (option 3 Zone A : formulation naturelle historique), séparation source/pack des statuts dans file 01, création des fichiers de distribution `LICENSE` (placeholder de licence CC BY 4.0, remplacé en 5c.3.h) et `source_pr_references.md`, mise à jour du README pour réintégrer l'attribution CC BY 4.0 tout en conservant le statut DRAFT (PDF + revue finale non faits).

### Alignements de statut appliqués à `01_oom_recovery_sop.md`

| Avant 5c.3.d | Après 5c.3.d |
|---|---|
| `- status: <<<REVIEW>>>CLOSED_INTERNAL_PROOF_ONLY_OOM_RECOVERY_SOP_V0<<<END>>>` | `- source closeout status: closed as internal proof model candidate` |
| `- publication scope: non-public` | `- source publication scope: non-public at source time`<br>+ `- pack publication status: DRAFT pending PDF compilation and final review` |
| _strong external-release wording (pre-5c.3.d, replaced — see git history for literal text)_ | `Status: SOP V0 draft, prepared for external review. External release pending final PDF compilation and review.` |

L'objectif : distinguer **statut historique source** (état du SOP dans le repo source au moment du closeout d'origine, PR #83) du **statut courant pack** (état du SOP dans la livraison externe DRAFT). Aucun statut sur-déclaré.

### Fichiers de distribution créés

| Fichier | Statut |
|---------|--------|
| `LICENSE` | placeholder de licence CC BY 4.0 (remplacé en 5c.3.h par le texte officiel verbatim depuis `creativecommons.org/licenses/by/4.0/legalcode.txt`). |
| `source_pr_references.md` | mapping complet des 5 fichiers `content/*.md` vers leurs PR sources (#27, #31, #81-83, #87-90, #143) + types de consolidation + note sur le statut interne de `content_raw/`. |

### Vérification

- `python scripts/sop_pack_content_integrity_check.py --max-review 0` : **OVERALL PASS** (7/7)
- `python scripts/asso_gate_t1_run_non_live_tests.py --tier minimal` : passed=12 failed=0 skipped=0 deferred=0

### Mission suivante (release humain final)

Le pack reste DRAFT. Pour atteindre publication-readiness :

1. ~~Pass de suivi avec accès vérifié à creativecommons.org : remplacer le placeholder de licence par le texte officiel CC BY 4.0 verbatim.~~ **FAIT en 5c.3.h.**
2. Pass de revue humaine finale (mainteneur) : valider l'ensemble des artefacts, optionnellement compiler en PDF, retirer le statut DRAFT du README.
3. Publication selon le canal choisi (`EXTRACT_SOP_PACK_SCOPE.md` §6.2).

---

## Patch 5c.3.e — Distribution structure dédiée

Patch 5c.3.e appliqué : création de la structure `dist/ai-ops-sop-pack-v0/` (9 fichiers — copies octet-pour-octet des artefacts racine au commit 6bc4c59) ; checker dédié `scripts/sop_pack_dist_integrity_check.py` (8 invariants D1–D8) ; LICENSE officiel CC BY 4.0 reste un placeholder (`LICENSE_OFFICIAL_TEXT_BLOCKED` documenté — aucun fichier tracké du repo ne contient le texte officiel, fetch externe non autorisé). Aucun fichier racine ni `content_raw/` modifié.

Détail dans `docs/project_evidence/sop_pack_5c3e_release_structure_and_license_text_v0/release_structure_report.md`.

---

## Patch 5c.3.f — Status claim repair + checker hardening

Patch 5c.3.f appliqué : réparation d'un claim fort résiduel détecté par Zone A après 5c.3.e (file 02 racine + dist contenait encore une phrase de release explicite sous CC BY 4.0 — voir git diff `a835615..HEAD` pour le texte littéral remplacé), incompatible avec le placeholder de licence CC BY 4.0 alors en vigueur. Durcissement parallèle des deux checkers pour transformer le bug 5c.3.d/5c.3.e en garde automatisée.

### Réparation du claim fort

Fichiers modifiés (claim → DRAFT-compatible) :
- `content/02_pr_final_audit_head_guard_sop.md` : phrase de closeout réécrite vers le statut DRAFT explicite (mention LICENSE_PENDING + final review + optional PDF) et corridor « closes the corridor » → « records the source corridor »
- `dist/ai-ops-sop-pack-v0/content/02_pr_final_audit_head_guard_sop.md` : même réécriture
- `content/_INDEX.md` + `dist/ai-ops-sop-pack-v0/content/_INDEX.md` : références historiques en table « Avant 5c.3.d | Après 5c.3.d » obfusquées (la phrase littérale d'origine est remplacée par une description neutre « _strong external-release wording (pre-5c.3.d, replaced — see git history for literal text)_ ») pour ne pas re-déclencher le nouveau checker
- `docs/project_evidence/sop_pack_5c3c_content_repair_and_5c4_scaffold_v0/review_resolution_report.md` : 2 références historiques également obfusquées + ajout d'une §10 documentant la pass

### Durcissement des checkers (C7 + D7)

Les deux checkers (`sop_pack_content_integrity_check.py` C7 et `sop_pack_dist_integrity_check.py` D7) sont restructurés pour :

1. **Élargir la scope** au-delà des seuls fichiers de distribution (était : README + LICENSE + source_pr_references.md uniquement). Inclut désormais les 5 SOPs + `_INDEX.md`.
2. **Séparer deux classes de claims** :
   - `ALWAYS_FORBIDDEN` — claims opérationnels jamais appropriés pour un pack documentaire borné (lists précises dans `scripts/sop_pack_content_integrity_check.py` et `scripts/sop_pack_dist_integrity_check.py`). Appliqués UNIQUEMENT aux fichiers de distribution. Tolérés dans les SOPs en contexte de négation (boundaries qui disent ce que le pack ne fait pas).
   - `DRAFT_FORBIDDEN` — claims d'état de release (variantes de readiness sous CC BY 4.0, mentions de licence accordée, claims de commercial-readiness — listes précises dans les checkers). Appliqués à la SCOPE COMPLÈTE (5 SOPs + _INDEX.md + 3 distribution files) UNIQUEMENT tant que le placeholder de licence était présent dans `LICENSE`. Une fois la licence officielle bundlée (5c.3.h), cette liste cesse d'être enforcée.
3. **Ajouter des tokens de négation française** au détecteur `_has_negation_before` : `aucune`, `aucun`, `pas de`, `pas d'`, `ne pas`, `n'accorde`, `n'autorise`, `n'approuve`, `n'ouvre`, `ni`, `sans`, `jamais`. Permet de couvrir correctement les SOP bodies en français.

### Vérification

- `python -m py_compile scripts/sop_pack_content_integrity_check.py scripts/sop_pack_dist_integrity_check.py` : PASS
- `python scripts/sop_pack_content_integrity_check.py --max-review 0` : **OVERALL PASS** (7/7) avec scope élargi
- `python scripts/sop_pack_dist_integrity_check.py` : **OVERALL PASS** (8/8) avec scope élargi
- `python scripts/asso_gate_t1_run_non_live_tests.py --tier minimal` : passed=12 failed=0 skipped=0 deferred=0
- `git diff --check` : PASS

Le pack reste DRAFT. Détail dans `docs/project_checkpoints/2026-05-09_sop_pack_5c3f_dist_status_claim_repair_v0.md`.

---

## Patch 5c.3.g — Publication strategy + LICENSE source gate definition

Patch 5c.3.g appliqué : décision de stratégie de publication enregistrée comme document, sans publier, sans finaliser la licence, sans générer de PDF, sans créer de repo externe, sans merger. Comparaison de trois topologies (A standalone repo extraction, B merge dans `main`, C tarball/zip détaché). Recommandation : standalone repo extraction depuis `dist/ai-ops-sop-pack-v0/` après bundling licence + revue humaine finale.

### Tokens de statut verrouillés

| Token | Valeur |
|-------|--------|
| `SELECTED_STRATEGY_RECOMMENDATION` | `STANDALONE_REPO_EXTRACTION` |
| `MAIN_MERGE_STATUS` | `BLOCKED_UNTIL_ROOT_README_RESTORED` |
| `LICENSE_STATUS` | ~~placeholder~~ → `LICENSE_OFFICIAL_TEXT_BUNDLED` (5c.3.h) |
| `PUBLICATION_STATUS` | `NOT_PUBLISHED` |
| `PDF_STATUS` | `NOT_GENERATED` |
| `FINAL_REVIEW_STATUS` | `PENDING` |
| `NEXT_GATE_DEFINED` | `SOP_PACK_5C3H_OFFICIAL_LICENSE_TEXT_BUNDLING_V0` |

`MAIN_MERGE_STATUS` est marqué `BLOCKED_UNTIL_ROOT_README_RESTORED` parce que le `README.md` racine de la branche `extract/sop-pack-v0` écrase le README parent du repo ACE / Asso. Un merge dans `main` exigerait une mission de restauration séparée (revert du README racine, revert du LICENSE racine, retrait des fichiers pack au niveau racine), non comprise dans 5c.3.g et non recommandée pour V0.

### Prochain gate défini (non ouvert)

`SOP_PACK_5C3H_OFFICIAL_LICENSE_TEXT_BUNDLING_V0` — **EFFECTUÉ (5c.3.h)** : fetch du texte officiel CC BY 4.0 depuis `creativecommons.org/licenses/by/4.0/legalcode.txt` et remplacement verbatim du placeholder de licence dans `LICENSE` (racine) et `dist/ai-ops-sop-pack-v0/LICENSE`. Résultat : les deux fichiers LICENSE contiennent le texte officiel, aucun placeholder ne subsiste dans les fichiers du pack.

### Vérification

- `python -m py_compile scripts/sop_pack_content_integrity_check.py scripts/sop_pack_dist_integrity_check.py` : PASS
- `python scripts/sop_pack_content_integrity_check.py --max-review 0` : OVERALL PASS (7/7)
- `python scripts/sop_pack_dist_integrity_check.py` : OVERALL PASS (8/8)
- `python scripts/asso_gate_t1_run_non_live_tests.py --tier minimal` : passed=12 failed=0 skipped=0 deferred=0
- `git diff --check` : PASS

Détail dans `docs/project_evidence/sop_pack_5c3g_publication_strategy_and_license_source_gate_v0/publication_strategy_report.md` et `docs/project_checkpoints/2026-05-09_sop_pack_5c3g_publication_strategy_and_license_source_gate_v0.md`. Le pack reste DRAFT.

---

## Patch 5c.3.h — Bundling du texte officiel CC BY 4.0

Patch 5c.3.h appliqué : le texte officiel CC BY 4.0 a été récupéré verbatim depuis `creativecommons.org/licenses/by/4.0/legalcode.txt` (18 656 octets, SHA-256 : `9E5F1B3C610B9C2DA5C313BF81D577A7D1ACEC686BDB0384EDEFA6DF0F90CD94`) et écrit sans reformatage ni traduction dans `LICENSE` (racine) et `dist/ai-ops-sop-pack-v0/LICENSE`. Les deux fichiers sont byte-identiques. Aucun placeholder ne subsiste dans les fichiers du pack.

### Statuts après 5c.3.h

| Token | Valeur |
|-------|--------|
| `LICENSE_STATUS` | `LICENSE_OFFICIAL_TEXT_BUNDLED` |
| `PUBLICATION_STATUS` | `NOT_PUBLISHED` |
| `PDF_STATUS` | `NOT_GENERATED` |
| `FINAL_REVIEW_STATUS` | `PENDING` |
| `PACK_STATUS` | `DRAFT` |

### Vérification

- `python -m py_compile scripts/sop_pack_content_integrity_check.py scripts/sop_pack_dist_integrity_check.py` : PASS
- `python scripts/sop_pack_content_integrity_check.py --max-review 0` : OVERALL PASS (7/7)
- `python scripts/sop_pack_dist_integrity_check.py` : OVERALL PASS (8/8)
- `python scripts/asso_gate_t1_run_non_live_tests.py --tier minimal` : passed=12 failed=0 skipped=0 deferred=0
- `git diff --check` : PASS
- Occurrences du placeholder de licence dans les fichiers pack : 0

Détail dans `docs/project_evidence/sop_pack_5c3h_official_license_text_bundling_v0/license_bundling_report.md` et `docs/project_checkpoints/2026-05-09_sop_pack_5c3h_official_license_text_bundling_v0.md`. Le pack reste DRAFT.

---

## Patch 5c.3.i — Final human review packet

Patch 5c.3.i appliqué : préparation du paquet de revue humaine finale (pas de publication, pas de PDF, pas de modification de la licence, pas de création de repo externe, pas de merge). Manifest de release candidate (paths, tailles, SHA-256 sur les 9 fichiers de `dist/ai-ops-sop-pack-v0/`) et review packet structurée (scope de lecture, checklist H1–H11, notes par fichier, table de décision bloquante, prochain gate par verdict).

### Tokens de statut

| Token | Valeur |
|-------|--------|
| `REVIEW_PACKET_STATUS` | `READY_FOR_HUMAN_REVIEW` |
| `RELEASE_CANDIDATE_MANIFEST_STATUS` | `LOCKED_AT_BASE_COMMIT_d0ca9d1` |
| `DIST_FILES_HASHED` | `9 / 9` |
| `LICENSE_STATUS` | `CC_BY_4_0_OFFICIAL_TEXT_BUNDLED` (carried from 5c.3.h) |
| `DRAFT_STATUS` | `DRAFT` |
| `PUBLICATION_STATUS` | `NOT_PUBLISHED` |
| `PDF_STATUS` | `NOT_GENERATED` |
| `FINAL_REVIEW_STATUS` | `PENDING` |
| `SELECTED_STRATEGY_RECOMMENDATION` | `STANDALONE_REPO_EXTRACTION` (carried from 5c.3.g) |
| `MAIN_MERGE_STATUS` | `BLOCKED_UNTIL_ROOT_README_RESTORED` (carried from 5c.3.g) |

### Verdicts possibles à la fin de la revue humaine

- `HUMAN_REVIEW_PASS` → ouvre `SOP_PACK_5C3J_OPTIONAL_PDF_OR_STANDALONE_REPO_PREP_V0`
- `NEEDS_FIX_BEFORE_PDF` → ouvre `SOP_PACK_5C3I_REPAIR_PASS`
- `STOP_PUBLICATION_RISK` → closeout, pas d'autre extract pass sans réouverture explicite du mainteneur

5c.3.i n'ouvre aucun de ces gates. Le verdict est posé par le mainteneur (Hichem Benali).

### Vérification

- `python -m py_compile scripts/sop_pack_content_integrity_check.py scripts/sop_pack_dist_integrity_check.py` : PASS
- `python scripts/sop_pack_content_integrity_check.py --max-review 0` : OVERALL PASS (7/7)
- `python scripts/sop_pack_dist_integrity_check.py` : OVERALL PASS (8/8)
- `python scripts/asso_gate_t1_run_non_live_tests.py --tier minimal` : passed=12 failed=0 skipped=0 deferred=0
- `git diff --check` : PASS
- 0 occurrence du placeholder de licence dans `dist/`
- LICENSE racine et LICENSE dist byte-identiques (18656 octets, sha256 `9e5f1b3c…0cd94`)
- README racine + README dist contiennent `DRAFT`

Détail dans `docs/project_evidence/sop_pack_5c3i_final_human_review_packet_v0/final_human_review_packet.md`, `docs/project_evidence/sop_pack_5c3i_final_human_review_packet_v0/release_candidate_manifest.md` et `docs/project_checkpoints/2026-05-09_sop_pack_5c3i_final_human_review_packet_v0.md`. Le pack reste DRAFT.

---

## Patch 5c.3.j — Standalone repo prep

Patch 5c.3.j appliqué : préparation du passage vers un repo standalone, **sans** créer le repo, **sans** publier, **sans** générer de PDF, **sans** merger, **sans** modifier la LICENSE/README/SOPs/`content_raw`. Préparation seule : rapport de stratégie, plan de fichiers (mapping `dist/ai-ops-sop-pack-v0/*` → repo standalone), checklist preflight (13 décisions P1–P13).

### Tokens de statut

| Token | Valeur |
|-------|--------|
| `STANDALONE_REPO_PREP_STATUS` | `STANDALONE_REPO_PREPARED_NOT_CREATED` |
| `DIST_ROOT` | `dist/ai-ops-sop-pack-v0/` |
| `DIST_FILES_COUNT` | `9 / 9` |
| `LICENSE_STATUS` | `CC_BY_4_0_OFFICIAL_TEXT_BUNDLED` (porté depuis 5c.3.h) |
| `DRAFT_STATUS` | `DRAFT` |
| `PUBLICATION_STATUS` | `NOT_PUBLISHED` |
| `PDF_STATUS` | `NOT_GENERATED` |
| `REPO_CREATION_STATUS` | `NOT_CREATED` |
| `HUMAN_REVIEW_VERDICT` | `HUMAN_REVIEW_PASS` (porté depuis 5c.3.i, déclaré par le mainteneur) |
| `SELECTED_STRATEGY_RECOMMENDATION` | `STANDALONE_REPO_EXTRACTION` (porté depuis 5c.3.g) |
| `MAIN_MERGE_STATUS` | `BLOCKED_UNTIL_ROOT_README_RESTORED` (porté depuis 5c.3.g) |
| `INDEX_SYNC_STATUS` | `ROOT_DIST_INDEX_IDENTICAL` (porté depuis 5c.3.i repair) |

### Prochain gate défini (non ouvert)

`SOP_PACK_5C3K_STANDALONE_REPO_CREATION_OR_ARCHIVE_EXPORT_V0` — création effective du repo standalone (ou export d'archive selon canal choisi) + seed depuis `dist/ai-ops-sop-pack-v0/` + tag de version + vérification visuelle. Pré-requis : items P1, P3, P4, P9 de la preflight checklist cochés ; HUMAN_REVIEW_PASS confirmé ; tous les checks automatiques toujours PASS.

5c.3.j **n'ouvre pas** 5c.3.k. L'ouverture est conditionnée à un mandat explicite du mainteneur après remplissage de la checklist.

### Vérification

- `python -m py_compile scripts/sop_pack_content_integrity_check.py scripts/sop_pack_dist_integrity_check.py` : PASS
- `python scripts/sop_pack_content_integrity_check.py --max-review 0` : OVERALL PASS (7/7)
- `python scripts/sop_pack_dist_integrity_check.py` : OVERALL PASS (8/8)
- `python scripts/asso_gate_t1_run_non_live_tests.py --tier minimal` : passed=12 failed=0 skipped=0 deferred=0
- `git diff --check` : PASS
- Aucun fichier `dist/` modifié hors `dist/ai-ops-sop-pack-v0/content/_INDEX.md`
- LICENSE racine et dist non touchés (18656 octets, sha256 `9e5f1b3c…0cd94`)
- README racine et dist non touchés
- Les 5 SOPs (racine et dist) non touchés
- `content_raw/` non touché

Détail dans `docs/project_evidence/sop_pack_5c3j_standalone_repo_prep_v0/standalone_repo_prep_report.md`, `docs/project_evidence/sop_pack_5c3j_standalone_repo_prep_v0/standalone_repo_file_plan.md`, `docs/project_evidence/sop_pack_5c3j_standalone_repo_prep_v0/standalone_repo_preflight_checklist.md` et `docs/project_checkpoints/2026-05-09_sop_pack_5c3j_standalone_repo_prep_v0.md`. Le pack reste DRAFT.
