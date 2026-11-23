# 🔁 Relance : le skill Claude qui sait qui tu dois relancer

**Tu envoies un devis… et le client ne répond jamais. Toi, tu oublies de relancer. L'argent dort.**

Ce skill gratuit pour Claude relit tes mails envoyés et te sort, en une seule demande :

- 💤 **L'argent qui dort** : le total de tes factures impayées et de tes devis sans réponse, en euros.
- 🔁 **Qui relancer, dans l'ordre** : chaque conversation a un score d'urgence (montant, jours d'attente, échéance).
- ✍️ **Le brouillon de relance déjà écrit**, dans la bonne conversation, au bon ton : rappel léger à J+3, relance directe à J+7, dernier message à J+14. Pour les factures : rappel, 1re relance, 2e relance, relance ferme, selon le retard.
- 📥 **Les réponses que TOI tu dois** encore (parce que ça aussi, ça se perd).
- 📅 **Et chaque lundi à 8 h, tout seul**, si tu veux.

**Il n'envoie jamais rien.** Tu relis, tu cliques sur « Envoyer ». Il ne supprime rien, ne déplace rien.

---

## Ce qu'il te faut

- **Claude** (app Claude ou Claude Code).
- **Ta boîte mail connectée à Claude** : connecteur Gmail (ou Outlook) dans l'app Claude, ou un serveur MCP mail dans Claude Code.
- Pour la relance automatique du lundi : un **abonnement Claude payant** (les tâches planifiées n'existent pas en gratuit).

## L'installer

### Le plus simple : demande à Claude

Colle ce lien dans Claude Code et écris : « Installe ce skill pour moi »
```
https://github.com/tech-ia-oui/relance-skill
```

### Claude Code, en plugin

Dans ton terminal :
```bash
claude plugin marketplace add tech-ia-oui/relance-skill
claude plugin install relance@tech-ia-oui
```
Puis ouvre une nouvelle session Claude Code.

### Claude Code, à la main

```bash
git clone https://github.com/tech-ia-oui/relance-skill
mkdir -p ~/.claude/skills && cp -r relance-skill/skills/relance ~/.claude/skills/
```

### App Claude (web ou bureau)

1. Télécharge le dossier `skills/relance` en .zip.
2. Dans Claude : **Paramètres → Capacités → Skills**, ajoute le .zip.

## L'utiliser

Écris simplement :
```
Qui je dois relancer ?
```
ou
```
/relance sur mes mails envoyés des 30 derniers jours
```

À la fin, il te propose de le faire tout seul **chaque lundi à 8 h**. Tu dis oui, c'est réglé.

## À quoi ressemble le rapport (exemple, données inventées)

> **💤 4 750 € qui dorment** : 2 factures (3 200 €), 1 devis (1 550 €)
>
> | Score | Qui | Objet | Type | Montant | Attente | Niveau |
> |---|---|---|---|---|---|---|
> | 95 | Studio Lumen | Facture F-2026-031 | facture | 2 000 € | 12 j, échue | 1re relance |
> | 80 | Agence Nova | Devis site vitrine | devis | 1 550 € | 8 j | J+7 |
> | 70 | Boulangerie Marc | Facture F-2026-028 | facture | 1 200 € | 5 j | rappel courtois |
> | 40 | Clara (podcast) | Proposition de collab | partenariat | non indiqué | 4 j | J+3 |
>
> **📥 Réponse que tu dois** : Julie (comptable) attend ton relevé d'octobre depuis jeudi.
>
> ✍️ 4 brouillons prêts dans Gmail. Rien n'a été envoyé.

## Les règles qu'il respecte

- Il ouvre **chaque conversation en entier** (la liste rapide de Gmail peut afficher « 1 message » alors qu'il y en a plusieurs).
- Une **réponse automatique** (« Merci pour votre message ») n'est pas une vraie réponse.
- **2 relances sans réponse ? Pas de troisième** : il te propose de classer le dossier.
- Si un client écrit qu'il a payé, il ne le relance pas : il te demande de vérifier.
- **Jamais de menace, de pénalité ni de mise en demeure** que tu n'as pas demandées. Pour le juridique : ton expert-comptable.
- Des messages courts (3 à 5 phrases), une seule demande claire, pas de « je me permets de vous relancer ».

## ⚠️ Honnêtement

- Il ne voit que ce qui est **écrit dans tes mails**. Une facture envoyée par un logiciel de facturation sans passer par ta boîte, il ne la voit pas.
- **Relis toujours les brouillons** : Claude ne connaît pas toute l'histoire avec ton client.
- Il n'invente jamais un montant : s'il n'est pas écrit, il met « non indiqué ».

---

Fait par **Tiao** · [@tech.ia.oui](https://www.instagram.com/tech.ia.oui/) sur Instagram · Le guide pas à pas : [bounkhong.de/guides/relance-fr](https://bounkhong.de/guides/relance-fr)

*Moi c'est Tiao : même si tu codes pas, l'IA va bosser pour toi. Tech, IA, oui.*

Licence MIT.
