# TP Introduction à Kubernetes

Antoine Zachariades

Roy Sarkis

## 1. Installation de Minikube et Kubectl
Installation de minikube : 
![](https://i.imgur.com/ZZzzYms.png)

![](https://i.imgur.com/SaRi6yb.png)

Installation de Kubectl :
`curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"`

`sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl`
```
chmod +x kubectl
mkdir -p ~/.local/bin
mv ./kubectl ~/.local/bin/kubectl
```
![](https://i.imgur.com/GmEkzy0.png)

## 2. Pod Nginx

Création du pod avec un fichier .yaml :`kubectl apply -f pods1.yaml`

![](https://i.imgur.com/W8hEtNJ.png)


Forward du port : `kubectl port-forward webserver 8080:`
![](https://i.imgur.com/Zwpe7BJ.png)

kubectl apply -f mysql.yaml
kubectl apply -f phpmyadmin.yaml

## 3. Connexion entre plusieurs Pods

Les parties a,b,c sont dans les fichiers mysql.yaml et phpmyadmin.yaml
La partie d : `kubectl port-forward -n tp-kube-3 phpmyadmin-7d845f97c7-qfk5d 8080:80`


