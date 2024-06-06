# Recueil sur Angular
1- Use interceptor in Angular

Les interceptors sont une fonctionnalité puissante du module Http Client qui permet de modifier les requetes et les reponses Http de manière centralisée. Ils interceptent les requetes sortantes et les reponses entrantes, nous permettant de les modifiées ou d'exécuter une logique spécifique.   
Les paramètres de la méthode "intercept()" sont :
-HttpRequest: il représente la requete sortante;
-HttpHandler: il représente le prochaine intercepteur dans la chaine des interceptors.
Le type de retour "Observable<HttpEvent<any>>" représente le flux d'événement de la requete y compris la réponse.
Les interceptors sont souvent utilisés pour 'ajout de jeton d'authentification, la gestion des erreurs, le logging, ect.


2- Use guard in Angular
Les Guards sont un mécanisme mis en Angular pour protéger la navigation au sein d'une application. Il existe différentes types : 
-CanActivate : permet de surveiller l'accés à un URL;
-CanDesactivate: permet de surveiller la navigation en quittqnt l'URL;
-Revolve: permet de récupérer des données avant de charger l'URL;
-CanLoad: permet de prévenir la navigation asynchrone.
Les différents types utilisés pour les guards :
-ActivatedRouteSnapshot: Elle représente l'état statique de l'URL à un instant T. Elle contient les informations d'une route active, y compris les paramètres, les données 
 statiques, et les segments d'url.  
-canActivate: C'est une interface utilisée pour déterminer si une route doit etre activée. Elle doit etre implémentée lorsqu'on utilse les guards. Elle peut retouner Observable<boolean> | Promise<boolean> | boolean.
-canActivateChild: C'est une interface similaire à canActivate, à la seule différence est qu'elle permet de déterminer si les routes enfants du module doivent etre activées.
-RouterStateSnapshot: Elle représente l'état de l'url du routeur à un instant T. Contrairement à ActivatedRouteSnapshot, il fournit une vue globale de l'état de l'url et de toutes les routes activées. Ces principales propriétés : url: L'url de la route active sous forme de chaîne de caractères, root: La racine de l'arbre des routes activées, de type ActivatedRouteSnapshot.  
-canActivateFn et canActivateChildFn : C'est une version simplifiée de canActivate et canActivationChild. Au lieu d'utiliser des interfaces, un utilise des méthodes.
