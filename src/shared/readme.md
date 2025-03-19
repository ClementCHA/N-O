# 📂 `shared/` - Code Transversal

Ce dossier contient tous les éléments **transversaux** utilisés à travers l'application.  
Il regroupe des composants réutilisables qui ne dépendent pas du métier (`domain/`) mais qui facilitent la gestion des requêtes, des réponses et des comportements globaux.

---

## 📌 Structure du dossier  

### 📁 `decorators/`  

➡️ Contient les **décorateurs** TypeScript utilisés dans l’application.  
_(Ex : `@Public()`, `@Roles()`, etc.)_

### 📁 `filters/`

➡️ Gestion des **erreurs globales** via des `ExceptionFilters`.  
_(Ex : `HttpExceptionFilter` pour formater les erreurs API.)_

### 📁 `interceptors/`

➡️ Intercepte les requêtes/réponses pour les modifier.  
_(Ex : `TransformInterceptor` pour formater les réponses.)_

### 📁 `middleware/`

➡️ Middlewares exécutés avant que les requêtes n’atteignent les contrôleurs.  
_(Ex : `LoggerMiddleware` pour logguer chaque requête.)_

---

## 🛠 Bonnes pratiques  

✅ **Les fichiers ici doivent être génériques et réutilisables**  
✅ **Pas de dépendance directe aux modules métiers (`modules/`)**  
✅ **Les éléments doivent être agnostiques et découplés du domaine (`domain/`)**  

💡 *Si un fichier est trop spécifique, il doit probablement être dans `application/` ou `modules/` plutôt que dans `shared/`.*

---

🚀 **Ce dossier aide à garder une architecture propre et scalable !**
