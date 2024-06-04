# Recueil sur Angular
Use interceptor in Angular

Les interceptors sont une fonctionnalité puissante du module Http Client qui permet de modifier les requetes et les reponses Http de manière centralisée. Ils interceptent les requetes sortantes et les reponses entrantes, nous permettant de les modifiées ou d'exécuter une logique spécifique.   
Les paramètres de la méthode "intercept()" sont :
-HttpRequest: il représente la requete sortante;
-HttpHandler: il représente le prochaine intercepteur dans la chaine des interceptors.
Le type de retour "Observable<HttpEvent<any>>" représente le flux d'événement de la requete y compris la réponse.
Les interceptors sont souvent utilisés pour 'ajout de jeton d'authentification, la gestion des erreurs, le logging, ect.
