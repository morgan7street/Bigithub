# Bigithub

---

# **Uploader un dépôt sur GitHub sans restriction de taille**  

## 🚀 **Préparation**  
1. **Créer un workflow GitHub Actions**  
   - À la racine de votre dépôt, créez un dossier **`.github/workflows`**.  
   - À l’intérieur, ajoutez un fichier nommé **`unzip.yml`** et collez-y le contenu fourni.  

## 📂 **Upload des fichiers**  
2. **Préparer l’archive à envoyer**  
   - Placez tous les fichiers à uploader dans une **archive ZIP**.  
   - **Important** : L’archive doit être nommée **`.zip`**.  

## ⚙️ **Déroulement du processus**  
3. **Automatisation de l’extraction**  
   - Une fois l’archive `.zip` uploadée sur le dépôt, le processus démarre automatiquement.  
   - L’archive est **décompressée** et son contenu est restauré **à l’identique** à la racine du projet.  

---

## ⚠️ **Avertissement**  
📌 **Chaque fois que vous uploadez un fichier `.zip`, il sera automatiquement décompressé dans votre dépôt.**  
Assurez-vous que l’archive respecte **l’architecture actuelle** de votre projet pour éviter toute modification non souhaitée.  

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
