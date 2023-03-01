# Ebauche des vulnérabilités identifiées

## Enumeration des vulnérabilités connues 

### SQLi

En effet, toutes les requêtes implémentées en dur ne sont pas préparés, ce qui implique que la partie dynamique de la requête sera interprétée si du code y est inséré.

Cette vulnérabilité est présente dans le fichier auth.py, dans les fonction :

 - register(): 
	A la ligne 41
```
    db.execute(
    	f'INSERT INTO user (username, password) VALUES '  #TODO : préparer la requête
    	f'("{username}", "{password}")'
    )
    db.commit()
    
   ```

 - login():
 - load_logged_in_user():
 - 
 
 
 ### Injection XSS
 
 Dans le formulaire de création des posts
 
 ```<script>alert('XSS test')</script>```
 
 ### hash
 
 MDP non hashé dans la base
 
 ### anti bruteforce
 
 Pas d'anti brute force sur la page de connextion
 
 ### sanitization ?
 
 ### Authentification failure
 
 
