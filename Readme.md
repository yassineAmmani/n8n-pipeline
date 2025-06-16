# 🚀 Pipeline d'Intégration ERP avec N8N

> Système d'automatisation CRM intelligent avec validation et scoring en temps réel

![N8N](https://img.shields.io/badge/N8N-Workflow-blue?style=flat-square&logo=n8n)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Status](https://img.shields.io/badge/Status-Demo-28a745?style=flat-square)

## 🎯 Aperçu

Pipeline automatisé pour traiter, valider et enrichir les données clients avec :

- **Validation intelligente** des champs obligatoires
- **Scoring automatique** de qualité (0-100%)
- **Enrichissement** avec métadonnées business
- **Intégration ERP** (compatible Odoo)

## 🏗️ Architecture

```
📥 Webhook → 🔍 Validation → 🏢 ERP Simulation → 📤 Response
                    ↓
              📊 Google Sheets Log
```

## 🚀 Démonstration

### 🌐 Landing Page

[**TechFlow Solutions**](./landing_page.html) - Formulaire client interactif avec intégration temps réel

### 🧪 Tests

[**Page de Test**](./test_page.html) - Interface pour tester différents scénarios

### 📊 Workflow N8N

Importez [`workflow.json`](./workflow.json) dans votre instance N8N

## 🔧 Utilisation Rapide

### Test API

```bash
curl -X POST YOUR_WEBHOOK_URL \
  -H "Content-Type: application/json" \
  -d '{
    "nom": "TechCorp",
    "email": "contact@techcorp.com",
    "entreprise": "Tech Corp",
    "secteur": "IT"
  }'
```

### Réponse

```json
{
  "success": true,
  "client_id": "CLIENT_1750070388239",
  "nom": "TechCorp",
  "score_qualite": 75,
  "priorite": "HAUTE"
}
```

## ⚙️ Configuration

### 📥 Import du Workflow

1. **N8N** → Import → Coller le contenu de `workflow.json`
2. **Activer** le workflow (bouton ON)
3. **Copier** l'URL webhook générée

### 🔧 Nœuds à Configurer

| Nœud                               | Configuration Requise                    |
| ---------------------------------- | ---------------------------------------- |
| **🔗 Webhook ERP**                 | ✅ Automatique                           |
| **🔍 Validation & Enrichissement** | ✅ Prêt à l'emploi                       |
| **🏢 Simulation ERP**              | 🔄 Remplacer par votre API ERP           |
| **📊 Google Sheets Log**           | 🔑 Connecter compte Google + URL feuille |
| **📤 Réponse API**                 | ✅ Automatique                           |

### 🎯 Personnalisation Rapide

- **ERP Integration** : Modifier l'URL dans le nœud "Simulation ERP"
- **Champs validation** : Ajuster `requiredFields` dans le code
- **Scoring** : Personnaliser les critères de qualité
- **Logging** : Connecter votre Google Sheets

## 📋 Fonctionnalités

- ✅ **Validation** : Email, champs obligatoires
- 🤖 **Enrichissement** : ID unique, timestamps, scoring
- 📊 **Priorité** : HAUTE (≥75%) | MOYENNE (50-74%) | BASSE (<50%)
- 🔄 **Intégration** : Compatible systèmes ERP
- 📝 **Logging** : Traçabilité complète

## 🛠️ Stack Technique

- **N8N** - Orchestration workflow
- **JavaScript** - Logique métier
- **Google Sheets** - Logging
- **HTML/CSS** - Interface utilisateur

---

**Développé pour démontrer l'expertise en automatisation IA et intégration ERP**
