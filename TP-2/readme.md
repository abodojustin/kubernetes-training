> - on crée notre pod
> - on lance notre pod à travers la commande

``
kubectl apply -f pod.yml
``

> - pour avoir le descriptif de notre pod, on tape la commande suivante:

``
kubectl describe po nom_du_pod
``

> - pour lister tout les pods, on a:
``
kubectl get po
``

> - pour exposer notre application, on tape la commande:

``
kubectl port-forward simple-webapp-color 8080:8080 --address 0.0.0.0
``

> - suppression de notre pod:

``
kubectl delete -f pod.yml
``

# Création de notre manifest de type deployment
