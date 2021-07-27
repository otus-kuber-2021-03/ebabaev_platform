## Основное задание:
 - Запуском kube-apiserver/kube-controller-manager/kube-scheduler-minikube подов в Minikube управляет kubelet, который в свою очередь запускается, как systemd демон на VM, статические манифесты этих компонент лежат в /etc/kubernetes/manifests/
 - coredns задеплоен в кластер, как реплика set, с помощью механизма deployment, поэтому при удалении подов scheduler поднимает их в соответствии с параметрами заданными в манифестах
 - kube-proxy задеплоен в кластер как daemon set, scheduler поднимает его в соответствии с параметрами заданными в манифест

### Hipster Shop | Задание со ⭐
Для запуска приложения на базе имаджа из задания не хватало переменных окружения:
https://github.com/GoogleCloudPlatform/microservices-demo/blob/master/kubernetes-manifests/frontend.yaml#L52
Необходимые переменные добавлены в манифест frontend-pod-healthy.yaml
