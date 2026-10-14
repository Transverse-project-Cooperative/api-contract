# Contrat d'interface NoCode × Tech Lead

Contrat d'API au format **OpenAPI 3**, livrable commun du projet transverse, co-signé par les référents des deux équipes au jalon J3.

| Élément | Où |
|---|---|
| Contrat | [`openapi.yaml`](openapi.yaml) |
| Historique des versions | [`CHANGELOG.md`](CHANGELOG.md) |
| Demandes de changement | [`change-requests/`](change-requests/) |
| Signatures | [`SIGNATURES.md`](SIGNATURES.md) |

## Règles d'usage
1. La version co-signée en J3 fait foi.
2. Toute évolution passe par une demande de changement écrite (demandeur, motif, impact, nouvelle version), acceptée par les deux référents. Les demandes acceptées **et refusées** sont conservées.
3. Chaque équipe développe contre un mock généré depuis le contrat (ex. `npx @stoplight/prism-cli mock openapi.yaml`).
4. L'API réelle de l'autre équipe est branchée au plus tard en J5.

## Versionnement (SemVer)
- **MAJEURE** (2.0.0) : changement cassant (champ supprimé ou renommé, type changé). Préfixe d'URL `/v2`.
- **MINEURE** (1.1.0) : ajout compatible (nouveau champ optionnel, nouvel endpoint).
- **CORRECTIF** (1.0.1) : correction de documentation, sans effet sur le comportement.

## Frontière
Les deux systèmes ne communiquent que par cette API. Aucune écriture directe dans la base de l'autre équipe.
