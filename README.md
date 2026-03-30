# 🏨 Hotel Sol&Mare — Concierge IA

> Projet portfolio · AI × Hospitality · Alicante, Spain

![Demo](https://img.shields.io/badge/demo-live-brightgreen) ![Stack](https://img.shields.io/badge/stack-HTML%20%2F%20JS%20%2F%20Vercel-terracotta) ![IA](https://img.shields.io/badge/AI-Claude%20Sonnet-blue) ![Langs](https://img.shields.io/badge/langues-FR%20%2F%20ES%20%2F%20EN-gold)

---

## 🎯 Présentation

Application de **concierge virtuelle IA** développée pour démontrer l'intégration de l'intelligence artificielle dans les opérations hôtelières. Projet réalisé dans le cadre d'une formation en **gestion hôtelière & tourisme** à Alicante (Espagne).

L'objectif : simuler un assistant de réception disponible 24h/24, capable de répondre aux clients en 3 langues, d'analyser leur sentiment en temps réel, et de gérer des demandes de réservation.

---

## ✨ Fonctionnalités

### 🤖 Chat IA (Sofia — Concierge virtuelle)
- Réponses en temps réel via **Claude Sonnet** (Anthropic API)
- Trilingue : **Français / Español / English**
- Prompt engineering orienté hospitality (tarifs, services, infos locales Alicante)
- Historique de conversation multi-tour

### 📊 Analyse de sentiment client
- Détection automatique du sentiment sur chaque message (positif / neutre / négatif)
- Dashboard en temps réel avec barres de progression
- Score de satisfaction calculé dynamiquement (de -100 à +100)
- Journal d'activité horodaté

### 📅 Système de réservation simulé
- Sélection de chambre (Standard 85€ / Supérieure 120€ / Suite 195€)
- Calcul automatique du total (nuits + animaux)
- Confirmation avec numéro de référence généré
- Affichage des disponibilités en temps réel

---

## 🛠️ Stack technique

| Couche | Technologie |
|--------|-------------|
| Frontend | HTML5 / CSS3 / JavaScript vanilla |
| Backend (proxy API) | Vercel Serverless Functions (Node.js) |
| IA | Anthropic Claude Sonnet (`claude-sonnet-4-20250514`) |
| Déploiement | Vercel |
| Sécurité | Clé API côté serveur uniquement (variable d'environnement) |

---

## 🏗️ Architecture

```
hotel-solmare/
├── index.html          # Frontend complet (UI + logique client)
├── vercel.json         # Configuration routing Vercel
├── api/
│   └── chat.js         # Serverless function — proxy Anthropic API
└── README.md
```

**Flux d'une conversation :**
```
Utilisateur → index.html → POST /api/chat → Vercel Function → Anthropic API → Réponse Sofia
```

La clé API n'est jamais exposée côté client.

---

## 🚀 Déploiement local

```bash
# 1. Cloner le repo
git clone https://github.com/ton-username/hotel-solmare.git
cd hotel-solmare

# 2. Installer Vercel CLI
npm install -g vercel

# 3. Configurer la clé API
export ANTHROPIC_API_KEY=sk-ant-...

# 4. Lancer en local
vercel dev
```

---

## 🌐 Déploiement Vercel (production)

1. Connecter le repo GitHub à [vercel.com](https://vercel.com)
2. Ajouter la variable d'environnement `ANTHROPIC_API_KEY`
3. Déployer → URL publique générée automatiquement

---

## 💡 Cas d'usage hospitality démontrés

- **Réduction de la charge à la réception** — questions FAQ gérées automatiquement
- **Disponibilité 24/7** — pas de créneau horaire limité
- **Multilinguisme** — adaptation automatique au client (FR/ES/EN)
- **Analyse satisfaction** — indicateur en temps réel pour le management hôtelier
- **Pré-réservation assistée** — qualification et orientation du client avant contact humain

---

## 📌 Contexte

Projet réalisé par **Foued**, étudiant en gestion hôtelière & tourisme (ICAN, Alicante), dans le cadre d'un profil hybride **Hospitality × Intelligence Artificielle**.

> L'hôtel Sol&Mare est un établissement fictif créé pour les besoins de ce portfolio. Les données (prix, disponibilités) sont simulées.

---

## 📄 Licence

MIT — libre d'utilisation à des fins éducatives et de démonstration.
