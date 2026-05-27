# AI Ops SOP Pack

"AI Ops SOP Pack" par Hichem Benali, sous licence [CC BY 4.0](./LICENSE). Source : https://github.com/monkidy/ai-ops-sop-pack.

> **Statut : V0.1 — publication documentation GitHub public ; GitHub Release v0.1.1 publié**
>
> La review humaine est passée. Ce dépôt est public comme publication canonique GitHub de AI Ops SOP Pack.
>
> Le GitHub Release v0.1.1 est publié comme release de visibilité documentation et alignement de statut. Aucun PDF, canal de vente, runtime, intégration provider ou annonce externe n'a été ouvert.

## Ce que contient ce pack

Un bundle consolidé et lisible de Standard Operating Procedures (SOPs) pour les équipes documentant et reviewant le travail d'ingénierie assisté par IA : discipline d'audit PR, procédures de cold recovery, format de handoff agent, et guides opérateur.

Le pack est un **pack de documentation**, pas un runtime, pas un outil, pas un service.

## Quand l'utiliser

Utilise ce pack quand ton équipe a besoin de réduire :

- les fausses déclarations de readiness après travail assisté par IA
- les handoffs PR faibles
- les hypothèses de merge non sécurisées
- le risque de perte de contexte après crash éditeur ou workstation
- la confusion entre évidence, review, approval et permission-to-act

Si tu ne lis qu'un fichier en premier, lis [`content/04_agent_handoff_format.md`](./content/04_agent_handoff_format.md).

## Public visé

Équipes AI Ops / Platform / SRE / ingénierie documentant ou reviewant du travail d'ingénierie assisté par IA et ayant besoin de procédures opératoires bornées pour :

- cold recovery humain-led après crash éditeur ou workstation pendant review PR / merge
- audit de pull requests avec head-guard discipline stricte avant merge
- remise en ligne d'une workstation après cold start sans ré-engager de longs contextes
- échanges de handoffs bornés entre agents ou opérateurs sous explicit decision values
- review de chemins opérateur local text-only sans aucun runtime live

## Contenu du pack

Commence par [`START_HERE.md`](./START_HERE.md) pour le guide de lecture externe, l'ordre de lecture recommandé, les notes de portabilité et les limites d'adaptation.

Le pack vit dans `content/`. Voir `content/_INDEX.md` pour l'index d'audit consolidé avec provenance par fichier, tailles et historique des review-tags. Voir `source_pr_references.md` pour le mapping par fichier PR-to-source.

| Fichier | Objectif |
|---------|----------|
| `content/01_oom_recovery_sop.md` | SOP OOM Recovery v0 — cold recovery humain-led après OOM pendant un gate PR/merge |
| `content/02_pr_final_audit_head_guard_sop.md` | SOP PR Final Audit + Head Guard v0 — procédure de review de merge bornée avec head-guard discipline |
| `content/03_cold_start_operator_runbook.md` | Cold-Start Operator Runbook v0 — index produit workstation + points d'entrée |
| `content/04_agent_handoff_format.md` | Agent Handoff Format v0 — structure minimale de handoff + allowed decision values |
| `content/05_operator_guide.md` | Operator Guide — Avatar Text-Only Stack v0 — étude de cas local text-only dérivée d'ASSO, pas un SOP générique plug-in |

## Templates

Les templates copiables vivent dans `templates/` :

| Fichier | Objectif |
|---------|----------|
| `templates/agent_handoff_template.md` | Structure de handoff vierge pour transfert borné opérateur / agent |
| `templates/pr_final_audit_checklist.md` | Checklist vierge pour audit final PR et review head-guard |
| `templates/oom_recovery_checklist.md` | Checklist vierge pour cold recovery après OOM / crash éditeur |
| `templates/cold_start_checklist.md` | Checklist vierge pour cold start local workstation |

Les templates sont des aides à la documentation uniquement. Ils n'accordent pas d'approval, d'autorité de merge, d'autorité runtime ou de permission-to-act.

## Exemples

Les exemples remplis vivent dans `examples/` :

| Fichier | Objectif |
|---------|----------|
| `examples/pr_crash_recovery_filled_example.md` | Parcours fictif non-live combinant OOM recovery, PR final audit et agent handoff |

Les exemples sont illustratifs uniquement. Ils ne prouvent pas de production readiness et ne doivent pas être copiés sans remplacer toutes les évidences par des observations de ton propre environnement.

## Release notes

Voir [`CHANGELOG.md`](./CHANGELOG.md) pour les changements du pack de documentation public.

Les release notes pour v0.1.1 vivent dans [`release_notes/v0.1.1.md`](./release_notes/v0.1.1.md). Les release notes pour v0.1.0 restent disponibles dans [`release_notes/v0.1.0.md`](./release_notes/v0.1.0.md).

## Comment l'utiliser

Chaque fichier est du Markdown auto-contenu. Lis `START_HERE.md` en premier, puis lis les SOPs consolidées et adapte les procédures à ton environnement. Garde les limites que les SOPs déclarent (pas de live, pas de provider, pas d'autorité runtime) : elles font partie de la discipline de design, pas des extras optionnels.

Pour un usage opérationnel, lis la SOP pertinente en premier, puis copie le template vierge correspondant depuis `templates/` et remplis-le avec les évidences observées dans ton propre environnement. Utilise `examples/` uniquement pour comprendre comment les pièces peuvent s'assembler ; ne traite pas les exemples comme autorité.

L'appendice "Trace de cycle ACE" à la fin des fichiers 01 et 02 documente la méthode de production (add → review → closeout → arbitration). Il est informatif et aide les lecteurs à voir comment la SOP a été durcie, pas une procédure à imiter verbatim.

## Statut

- **Version** : V0.1
- **Review humaine** : PASS
- **Publication** : PUBLIC_GITHUB_REPOSITORY
- **Visibilité publique** : PUBLIC
- **PDF** : NOT_GENERATED
- **Dernier tag** : v0.1.1
- **Dernier GitHub Release** : PUBLISHED — v0.1.1
- **Tag précédent** : v0.1.0
- **GitHub Release précédent** : PUBLISHED — v0.1.0
- **Tag initial** : v0.0.0
- **GitHub Release initial** : PUBLISHED — v0.0.0
- **Vente** : NOT_OPENED
- **Dernière mission** : v0.1.1 release de visibilité documentation et alignement de statut publiée ; pas de PDF, pas de canal de vente, pas de runtime, pas d'intégration provider, pas d'annonce externe.
- **Review markers** : 0 restants (`<<<REVIEW_HICHEM_5c3b>>>` count is zero across `content/*.md` ; vérifié par le checker d'intégrité `scripts/sop_pack_content_integrity_check.py --max-review 0` sur le dépôt source)
- **Licence** : CC BY 4.0. Le texte légal officiel CC BY 4.0 est bundlé dans `LICENSE` (récupéré verbatim depuis `creativecommons.org/licenses/by/4.0/legalcode.txt`). Aucun placeholder ne reste.
- **Source mapping** : présent dans `source_pr_references.md` (mapping par fichier PR-to-source pour traçabilité).

## Ce que ce pack n'est pas

- Pas un produit. Pas une offre. Pas un asset de vente.
- Pas un runtime. Pas un outil. Pas un service.
- Pas production-ready. Pas certifié. Pas warrantied.
- Pas une claim d'autorité opérationnelle sur ton environnement.
- Pas une permission-to-act, permission-to-trade, ou permission-to-publish en ton nom.

Le pack ne porte aucune garantie d'aucune sorte. Les procédures sont décrites pour référence opérationnelle ; toute adoption est à la responsabilité du lecteur.

## Licence et attribution

Le texte légal officiel CC BY 4.0 est bundlé dans `LICENSE`. L'attribution pour redistribution est :

> "AI Ops SOP Pack" par Hichem Benali, sous licence CC BY 4.0. Source : https://github.com/monkidy/ai-ops-sop-pack.

Le pack est publié dans ce dépôt GitHub public comme source canonique. Les GitHub Releases v0.0.0, v0.1.0 et v0.1.1 ont été publiés. Aucun PDF n'a été compilé, et aucun canal commercial n'a été ouvert. L'annonce externe n'est pas automatique et reste une décision explicite séparée.

## Prochaines étapes

- ~~Human review pass.~~ **FAIT** — statut review humaine : PASS.
- ~~Dépôt GitHub public.~~ **FAIT** — ce dépôt, public.
- ~~Tag `v0.0.0`.~~ **FAIT** — poussé sur ce dépôt.
- ~~GitHub Release v0.0.0.~~ **FAIT** — publié.
- ~~Polish d'utilisabilité.~~ **FAIT** — START_HERE, templates, exemple rempli, guidance case-study, changelog et release notes v0.1.0.
- ~~Tag `v0.1.0`.~~ **FAIT** — poussé sur ce dépôt.
- ~~GitHub Release v0.1.0.~~ **FAIT** — publié.
- ~~Tag `v0.1.1`.~~ **FAIT** — poussé sur ce dépôt.
- ~~GitHub Release v0.1.1.~~ **FAIT** — publié (release de visibilité documentation et alignement de statut).