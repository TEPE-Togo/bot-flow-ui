# 🤖 BotFlow UI — Test Technique Stagiaire Frontend

> **Poste visé :** Stagiaire Développeur Frontend  
> **Stack attendue :** Next.js · React · Tailwind CSS  
> **Soumission :** Fork ce repo → développe → envoie le lien de ton repo à [recrutement@karaba.africa]

---

## Contexte

Karaba est une plateforme d'automatisation de flows conversationnels via WhatsApp (recrutement, santé, événements, e-commerce). Un des besoins récurrents est de permettre à des non-développeurs de **configurer visuellement les étapes d'un flow de conversation** — sans toucher à du code.

Ton mission : construire **BotFlow UI**, un outil de création de flows conversationnels.

---

## Ce que tu vas construire

### 1. Éditeur de flow (page principale)

Un canvas interactif où l'utilisateur peut :

- **Ajouter des nœuds** de différents types :
  - `Message` — le bot envoie un texte
  - `Question` — le bot pose une question et attend une réponse
  - `Condition` — branchement selon la réponse (ex: si réponse = "Oui" → nœud A, sinon → nœud B)
  - `Fin` — termine le flow
- **Relier les nœuds** entre eux (drag depuis une sortie vers une entrée)
- **Modifier le contenu** d'un nœud en cliquant dessus (panneau latéral ou modale)
- **Supprimer** un nœud ou une connexion

> Tu peux utiliser une lib comme [React Flow](https://reactflow.dev/) ou implémenter toi-même — les deux sont acceptés. Mentionne ton choix dans le README.

### 2. Simulateur de conversation

Un panneau (ou page séparée) qui **rejoue le flow** du début à la fin :

- Affiche les messages du bot
- Propose les choix de réponse si le nœud est une `Question` ou `Condition`
- Suit le chemin logique selon les réponses de l'utilisateur
- Affiche un écran de fin quand le nœud `Fin` est atteint

### 3. Persistance locale

- Le flow doit être **sauvegardé dans le localStorage** automatiquement
- Un bouton **"Nouveau flow"** remet à zéro le canvas

---

## Fonctionnalités bonus _(non obligatoires, mais appréciées)_

- [ ] Export du flow en JSON (bouton "Exporter")
- [ ] Import d'un JSON pour recharger un flow
- [ ] Plusieurs flows sauvegardés (liste de flows avec nom)
- [ ] Mode sombre / clair
- [ ] Validation du flow avant simulation (ex: nœud sans connexion sortante = warning)
- [ ] Responsive mobile pour le simulateur

---

## Ce qu'on évalue

| Critère | Points |
|---|---|
| Fonctionnalités obligatoires livrées | 30 |
| Qualité et lisibilité du code React | 20 |
| UI/UX — clarté, cohérence, soin visuel | 20 |
| README clair + setup qui fonctionne | 15 |
| Git hygiene (commits atomiques, nommage) | 10 |
| Bonus | +10 |

---

## Contraintes techniques

- **Next.js** (App Router ou Pages Router, au choix)
- **Tailwind CSS** pour le style — pas de CSS custom global sauf si justifié
- **TypeScript** fortement recommandé
- Pas de backend requis — tout est client-side
- Node.js 18+

---

## Structure de repo attendue

```
botflow-ui/
├── app/               # ou pages/
├── components/
│   ├── canvas/
│   ├── nodes/
│   └── simulator/
├── lib/
├── public/
├── README.md          # ton README avec instructions de lancement
└── ...
```

---

## Comment soumettre

1. **Fork** ce repository
2. Développe sur ta propre branche ou directement sur `main`
3. Assure-toi que `npm install && npm run dev` fonctionne sans erreur
4. Envoie le lien de ton repo GitHub à **recrutement@karaba.africa** avec en objet : `[STAGE FRONTEND] Ton Nom`

> ⚠️ Un repo sans README de lancement ou qui ne démarre pas sera automatiquement écarté.

---

## Questions ?

Ouvre une **GitHub Issue** sur ce repo. On répond sous 48h.
