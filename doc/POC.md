## Інсталяція та налаштування ArgoCD

#### Створення namespace
`kubectl create namespace argocd`
#### Інсталяція ArgoCD
`kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml`
#### Отримання пароля для admin
`kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}"|base64 -d;echo`
#### Запуск та Вхід в ArgoCD
`kubectl port-forward svc/argocd-server -n argocd 8080:443`

---
### Дtмо ArgoСВ
![Демо ArgoCD](https://github.com/Andy-Well/AsciiArtify/blob/07bd3445a3150e865ff7c98a1115b2b96862cf5c/doc/ArgoCD_install.GIF)
