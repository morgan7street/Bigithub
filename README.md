# **Bigithub**

---

## **Uploader un dépôt sur GitHub sans restriction de taille**  

## 🚀 **Préparation**  
1. **Créer un workflow GitHub Actions**  
   - À la racine de votre dépôt, créez un dossier **`.github/workflows`**.  
   - À l’intérieur, ajoutez un fichier nommé **`unzip.yml`** et collez-y le contenu fourni.  

## 📂 **Upload des fichiers**  
2. **Préparer l’archive à envoyer**  
   - Placez tous les fichiers à uploader dans une **archive ZIP**.  
   - **Important** : L’archive doit être nommée **`depot.zip`**.  

## ⚙️ **Déroulement du processus**  
3. **Automatisation de l’extraction**  
   - Une fois l’archive `.zip` uploadée sur le dépôt, le processus démarre automatiquement.  
   - L’archive est **décompressée** et son contenu est restauré **à l’identique** à la racine du projet.  

---

## ⚠️ **Avertissements**  

### 📌 **1. Attention à l’upload automatique**  
- **Chaque fois que vous uploadez un fichier `.zip`, il sera automatiquement décompressé dans votre dépôt.**  
- **Vérifiez que votre archive respecte l’architecture actuelle** du projet pour éviter toute modification non souhaitée.  

### 🔑 **2. Vérifier les permissions des workflows**  
Pour que le processus fonctionne correctement, assurez-vous que **les permissions GitHub Actions** sont bien configurées en **lecture et écriture** :  
1. **Accédez aux paramètres de votre dépôt** (`Settings`).  
2. **Dans le menu de gauche, cliquez sur "Actions" → "General"**.  
3. **Faites défiler jusqu’à la section "Workflow permissions"**.  
4. **Cochez "Read and Write permissions"** si ce n'est pas déjà fait.  

Si cette option n'est pas activée, GitHub ne pourra pas extraire et modifier les fichiers dans votre dépôt.  

---

## ❌ **Désactiver le processus automatique**  
Si vous souhaitez **désactiver** l’extraction automatique des fichiers ZIP, **commentez** ces lignes dans le fichier `unzip.yml` :  

```yaml
# name: Extract ZIP Files

# on:
#   push:
#     paths:
#       - "*.zip"
```
Cela empêchera GitHub Actions de déclencher le processus lors de l’upload d’un fichier ZIP.  

---

✅ **Avantages :**  
- Contourne les restrictions de taille des fichiers sur GitHub.  
- Facile à mettre en place et entièrement automatisé.  
- Préserve la structure originale des fichiers.  

📌 **Testez et profitez d’un déploiement simplifié !** 🚀  

---

😊
