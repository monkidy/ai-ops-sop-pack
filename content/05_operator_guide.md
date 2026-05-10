---
title: Operator Guide — Avatar Text-Only Stack v0
version: v0
license: CC BY 4.0
---

<!--
SOURCE_PRS: #31 (avatar_text_only_v0)
CONSOLIDATION_TYPE: 4A (fusion Avatar Text-Only Stack en un fichier consolidé)
ANONYMIZATION_PASS: 5c.3 (P1 → [operator]/[stakeholder])
P4_MICROFILTER_PASS: 5c.3 (possessif_exposant + ref_meta_interne)
LICENSE: CC BY 4.0
EXTERNAL_ALIGNMENT_PASS: 5c.3.b (1B + 2A + 3A + 4B applied)
SOURCE_FILES: 05a_avatar_finish__src.md + 05b_avatar_operator_guide__src.md + 05c_avatar_usage__src.md
-->
# Operator Guide — Avatar Text-Only Stack v0

## 1. Usage

# ASSO Avatar Text-Only v0 Usage

FRONT: POST_AVATAR_BRANCH_ARBITRATION_TO_ASSO_RUNTIME_HIGHER_INTEGRATION
MAIN_BASE_OBSERVED: 411bc81c20ddca728141121bf3c7a29e80bcb0c8
ATTAINED_STATUS: AVATAR_TEXT_ONLY_V0_OPERATOR_SMOKE_TEST_PASS
HONEST_USAGE_LEVEL: USABLE_REVIEWABLE_LOCAL_TEXT_ONLY
PARKED_STATUS: AVATAR_TEXT_ONLY_V0_PARKED_AFTER_OPERATOR_SMOKE_TEST

## Realite sur main

Sur le sujet Avatar, `main` porte maintenant:

- doctrine presence intake
- technical manifest
- text-only API contract
- fixture packet
- local fixture harness
- local contract adapter
- local conversation loop stub
- local session policy stub

main porte desormais la chaine text-only locale non-live.

Cette chaine reste:

- local-only
- fixture-bound
- deterministic
- no provider
- no runtime
- no memory/ledger
- no permission-to-act

## Ce que ce guide permet reellement

Ce guide permet a [operator] de verifier honnetement que:

- les artefacts text-only locaux sont presents sur `main`
- la chaine `fixture -> harness -> adapter -> conversation loop -> session policy` est relancable localement
- les proof reports locaux sont inspectables sous `docs/asso_runtime/avatar/proof_reports/`
- un point d'entree operateur unique existe
- le smoke test operateur est passe

Ce guide ne prouve toujours pas:

- une conversation libre avec provider
- une integration UI
- une integration voix
- une integration Unity
- un runtime live
- un backend runtime
- une memoire persistante
- une session persistante
- une permission-to-act
- une readiness production

Ce guide n'ouvre aucun runtime live.
Ce guide n'appelle aucun provider.
Ce guide n'ecrit ni dans `memory/` ni dans `ledger/`.

## Frontieres absolues

- no Unity
- no voice
- no STT/TTS
- no provider
- no secret
- no runtime live
- no backend runtime
- no HTTP server
- no websocket
- no gateway
- no memory write
- no persistent memory
- no persistent session
- no ledger write
- no autonomous identity
- no permission-to-act

Ne surtout pas lancer Unity, voix, provider, runtime live, memory/ledger write.

## Commandes de verification sur main

Sur `main`, la verification locale non-live peut inclure:

```powershell
python scripts\asso_avatar_text_only_v0_operator_run.py
python scripts\asso_avatar_text_only_v0_operator_run_check.py
python scripts\asso_avatar_text_only_v0_operator_smoke_test_closeout_check.py
python scripts\asso_avatar_text_only_v0_finish_check.py
python scripts\asso_avatar_human_smoke_test_closeout_check.py
```

## OPERATOR ENTRYPOINT

- commande: `python scripts\asso_avatar_text_only_v0_operator_run.py`
- statut operateur precedent: `USABLE_LOCAL_TEXT_ONLY_OPERATOR_GUIDE_READY`
- ce point d'entree ne cree ni runtime/live, ni provider, ni voix, ni memoire, ni ledger

## OPERATOR SMOKE TEST RESULT

- verdict: `AVATAR_TEXT_ONLY_V0_OPERATOR_SMOKE_TEST_PASS`
- commande: `python scripts\asso_avatar_text_only_v0_operator_run.py`
- usage level: `USABLE_REVIEWABLE_LOCAL_TEXT_ONLY`
- rappel: pas `FINISHED_LOCAL_V0`
- rappel: pas runtime
- rappel: pas live
- rappel: pas provider
- rappel: pas voix
- rappel: pas memoire persistante

## PARKED AFTER OPERATOR SMOKE TEST

- status: `AVATAR_TEXT_ONLY_V0_OPERATOR_SMOKE_TEST_PASS`
- parked: yes
- next priority: `ASSO_RUNTIME_HIGHER_INTEGRATION` *(internal identifier)*
- this is not `FINISHED_LOCAL_V0`
- this is not `AVATAR_ALIVE`
- this is not `RUNTIME_READY`
- this is not `PRODUCTION_READY`
- this is not `LIVE`
- this is not `AUTONOMOUS`

## TEST HUMAIN

ouvrir / lancer :
`python scripts\asso_avatar_text_only_v0_operator_run.py`

entree utilisee :
fixtures locales sous `tests/fixtures/avatar/text_only/`

resultat attendu :
resume PASS en terminal + proof reports sous `docs/asso_runtime/avatar/proof_reports/`

preuve de reussite :

- `python scripts\asso_avatar_text_only_v0_operator_run.py` passe
- `python scripts\asso_avatar_text_only_v0_operator_run_check.py` passe
- `python scripts\asso_avatar_text_only_v0_operator_smoke_test_closeout_check.py` passe
- tous les checkers Avatar PASS

si echec :
ne pas corriger hors scope, copier la sortie et revenir Zone A

ne surtout pas faire :

- ne pas lancer Unity
- ne pas activer de voix
- ne pas appeler de provider
- ne pas ouvrir de runtime live
- ne pas ouvrir de backend runtime
- ne pas ouvrir de HTTP server
- ne pas ouvrir de websocket
- ne pas ouvrir de gateway
- ne pas ecrire dans `memory/`
- ne pas ecrire dans `ledger/`
- ne pas creer de memoire persistante
- ne pas creer de session persistante
- ne pas creer d'identite autonome
- ne pas revendiquer de permission-to-act

## 2. Operator Guide

# ASSO Avatar Text-Only v0 Operator Guide

- verdict: Avatar text-only v0 has a local operator path.
- statut: `USABLE_LOCAL_TEXT_ONLY_OPERATOR_GUIDE_READY`
- usage level precedent: `USABLE_REVIEWABLE_LOCAL_TEXT_ONLY`
- commande principale: `python scripts/asso_avatar_text_only_v0_operator_run.py`

## Image mentale

- cle de contact locale
- banc d'essai
- pas de route ouverte

Avatar text-only v0 demarre deja dans le garage.

Cette commande ajoute la cle de contact operateur.

Elle ne change pas la motorisation.

Elle n'ouvre ni route live, ni conduite autonome.

## Ce que fait la commande

La commande:

- lance successivement les quatre scripts locaux deja prouves
- verifie la presence des quatre proof reports
- imprime un resume operateur simple en terminal
- rappelle les frontieres a ne pas franchir

## Scripts appeles

Dans l'ordre:

1. `python scripts\asso_avatar_text_only_local_fixture_harness.py`
2. `python scripts\asso_avatar_text_only_local_contract_adapter.py`
3. `python scripts\asso_avatar_text_only_local_conversation_loop_stub.py`
4. `python scripts\asso_avatar_text_only_local_session_policy_stub.py`

## Fixtures utilisees

- fixtures locales sous `tests/fixtures/avatar/text_only/`

## Proof reports verifies

- `docs/asso_runtime/avatar/proof_reports/asso_avatar_text_only_local_fixture_harness_report.json`
- `docs/asso_runtime/avatar/proof_reports/asso_avatar_text_only_local_contract_adapter_report.json`
- `docs/asso_runtime/avatar/proof_reports/asso_avatar_text_only_local_conversation_loop_stub_report.json`
- `docs/asso_runtime/avatar/proof_reports/asso_avatar_text_only_local_session_policy_stub_report.json`

## Ce que [operator] doit regarder

- le code de sortie du runner: `0`
- le resume terminal de chaque etape
- la presence des quatre proof reports
- le checker operateur PASS
- les checkers Avatar PASS

## Si FAIL

- copier la sortie Zone A
- ne pas corriger hors scope
- verifier quelle etape a echoue
- revenir au front borne correspondant

## Ce qu'il ne faut surtout pas faire

- ne pas lancer Unity
- ne pas activer de voix
- ne pas appeler de provider
- ne pas ouvrir de serveur HTTP
- ne pas ouvrir de websocket
- ne pas ouvrir de runtime live
- ne pas ecrire dans `memory/`
- ne pas ecrire dans `ledger/`
- ne pas creer de session persistante
- ne pas revendiquer de permission-to-act

## Frontieres

- no Unity
- no voice
- no STT/TTS
- no provider
- no secret
- no runtime live
- no backend runtime
- no HTTP server
- no websocket
- no gateway
- no memory write
- no persistent memory
- no persistent session
- no ledger write
- no autonomous identity
- no permission-to-act

## TEST HUMAIN

ouvrir / lancer :
`python scripts/asso_avatar_text_only_v0_operator_run.py`

entree utilisee :
fixtures locales sous `tests/fixtures/avatar/text_only/`

resultat attendu :
resume PASS en terminal + proof reports sous `docs/asso_runtime/avatar/proof_reports/`

preuve de reussite :

- runner PASS
- checker operator PASS
- checkers Avatar PASS

si echec :
copier la sortie Zone A, ne pas corriger hors scope

ne surtout pas faire :

- Unity
- voix
- provider
- serveur HTTP
- websocket
- runtime live
- memory/ledger write
- session persistante

## Next gate

AVATAR_TEXT_ONLY_V0_OPERATOR_SMOKE_TEST_GATE

## 3. Finish

# AVATAR Text-Only v0 Finish Record

- front: POST_AVATAR_BRANCH_ARBITRATION_TO_ASSO_RUNTIME_HIGHER_INTEGRATION
- base commit: 411bc81c20ddca728141121bf3c7a29e80bcb0c8
- verdict: AVATAR_TEXT_ONLY_V0_OPERATOR_SMOKE_TEST_PASS
- niveau honnete: USABLE_REVIEWABLE_LOCAL_TEXT_ONLY
- operator status: USABLE_LOCAL_TEXT_ONLY_OPERATOR_GUIDE_READY
- parking decision: AVATAR_TEXT_ONLY_V0_PARKED_AFTER_OPERATOR_SMOKE_TEST

## Historical note

L'ancien verdict `BLOCKED_PENDING_STACK_REVIEW` est historique.

Le verdict `AVATAR_STACK_INTEGRATED_NON_LIVE_REVIEWABLE` a clos l'etape post-integration avant preuve humaine locale.

Le verdict `AVATAR_TEXT_ONLY_V0_HUMAN_SMOKE_TEST_PASS` reste la preuve humaine locale de base.

## Constat canonique

PR #10 intake doctrinal est canon sur `main`.

`main` porte maintenant:

- doctrine presence intake
- technical manifest
- text-only API contract
- fixture packet
- local fixture harness
- local contract adapter
- local conversation loop stub
- local session policy stub

## Preuve humaine locale

[operator] a synchronise `main` localement sur `cf81e247ecb2fb85401fa138a2ffc33a6648343f`.

La chaine locale smoke-testee reste validee par:

- `python scripts\asso_avatar_text_only_local_fixture_harness.py`
- `python scripts\asso_avatar_text_only_local_contract_adapter.py`
- `python scripts\asso_avatar_text_only_local_conversation_loop_stub.py`
- `python scripts\asso_avatar_text_only_local_session_policy_stub.py`

Les quatre executions ont retourne PASS.

Les quatre proof reports locaux existent sous `docs/asso_runtime/avatar/proof_reports/`.

## Operator entrypoint disponible

Une cle de contact operateur locale est disponible:

- commande: `python scripts\asso_avatar_text_only_v0_operator_run.py`
- statut operateur precedent: `USABLE_LOCAL_TEXT_ONLY_OPERATOR_GUIDE_READY`
- usage reel sous-jacent conserve: `USABLE_REVIEWABLE_LOCAL_TEXT_ONLY`

Cette commande orchestre uniquement les quatre scripts locaux deja prouves.

Elle sert de banc d'essai operateur local.

Elle n'ouvre ni route live, ni runtime, ni provider.

## Operator smoke test PASS

Le gate operateur est ferme sur preuve humaine locale.

- statut: `AVATAR_TEXT_ONLY_V0_OPERATOR_SMOKE_TEST_PASS`
- usage level conserve: `USABLE_REVIEWABLE_LOCAL_TEXT_ONLY`
- commande operateur confirmee: `python scripts\asso_avatar_text_only_v0_operator_run.py`

## Avatar parked cleanly after operator smoke test PASS

Avatar text-only v0 parked cleanly after operator smoke test PASS.

La priorite immediate ne va pas vers une augmentation de capacite Avatar.

La prochaine priorite projet retourne vers `ASSO_RUNTIME_HIGHER_INTEGRATION`.

## Ce que main prouve maintenant

La chaine locale non-live `fixture -> harness -> adapter -> conversation loop -> session policy` est utilisable comme chaine locale deterministe de review.

Elle peut etre relancee localement, ses proof reports peuvent etre reinspectes, et son comportement reste borne au text-only local sans provider.

## Ce que main ne prouve pas encore

Il n'existe toujours:

- aucune conversation libre avec provider
- aucune integration UI
- aucune voix
- aucune Unity
- aucun runtime live
- aucune memoire persistante
- aucune session persistante
- aucune identite autonome
- aucune permission d'agir
- aucune readiness production

## Boundaries

- no Unity
- no voice
- no STT/TTS
- no provider
- no secret
- no runtime live
- no backend runtime
- no HTTP server
- no websocket
- no gateway
- no memory write
- no persistent memory
- no persistent session
- no ledger write
- no autonomous identity
- no permission-to-act

## Decision

Statut atteint:
`AVATAR_TEXT_ONLY_V0_OPERATOR_SMOKE_TEST_PASS`

Parking decision:
`AVATAR_TEXT_ONLY_V0_PARKED_AFTER_OPERATOR_SMOKE_TEST`

Niveau d'usage reel:
`USABLE_REVIEWABLE_LOCAL_TEXT_ONLY`

Prochaine priorite:
`ASSO_RUNTIME_HIGHER_INTEGRATION` *(internal identifier)*

Statut explicitement non atteint:
`not FINISHED_LOCAL_V0`
`not AVATAR_ALIVE`
`not RUNTIME_READY`
`not PRODUCTION_READY`
`not FULLY_INTEGRATED`

## Next gate

Runtime higher integration reprise gate

---

Sourced from PR #31 (finish + operator_guide + usage).
