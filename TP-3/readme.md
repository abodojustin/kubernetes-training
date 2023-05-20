# TP-3: GESTION DU RÉSEAU

> - on crée un manifest namespace.yml qui crée un namespace nommé production
> - on lance la création de notre namespace à partir du manifest
``
kubectl apply -f namespace.yml
``


> - Ecrire un manifest pod-red.yml pour déployer un pod avec l'image mmumshad/simple-webapp-color en précisant que la color souhaitée est la rouge (red), le pod doit posséder le label "app:web"
``
kubectl apply -f pod-red.yml -n production
``

Pour vous rassurez que le pod a bien été crée, tapez la commande:

``kubectl get pod -n production
``

> - Ecrire un manifest pod-blue.yml pour déployer un pod avec l'image mmumshad/simple-webapp-color en précisant que la color souhaitée est la rouge (blue), le pod doit posséder le label "app:web"

> - lancez la création des deux pods
``
kubectl apply -f pod-red.yml -n production``

> - ecrivez un manifest service-nodeport-web.yml qui permettra d'exposer les pods via un service de type node port, le nodeport devra être le 30008 et les target les ports 8080 de nos pods dont le label est "app:web"

> - lancer la création du service ``kubectl apply -f service-nodeport-web.yml -n production`` et vérifiez qu'il trouve les deux pods ``kubectl -n production describe svc service-nodeport-web ``

> - vérifiez que l'appli est bien disponible en ouvrant le port 30008 de votre noeud