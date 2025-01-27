# Команды Kubernetes:


### Основные команды:

* **kubectl version:** Выводит информацию о версии клиента и сервера kubectl.
* **kubectl config view:** Отображает все настройки kubeconfig.
* **kubectl get nodes:** Выводит список всех узлов в кластере.
* **kubectl get pods:** Выводит список всех подов в кластере.
* **kubectl get deployments:** Выводит список всех развертываний в кластере.
* **kubectl get services:** Выводит список всех служб в кластере.
* **kubectl describe node <имя_узла>:** Отображает подробную информацию о конкретном узле.
* **kubectl describe pod <имя_пода>:** Отображает подробную информацию о конкретном поде.
* **kubectl describe deployment <имя_развертывания>:** Отображает подробную информацию о конкретном развертывании.
* **kubectl describe service <имя_службы>:** Отображает подробную информацию о конкретной службе.


### Создание объектов:

* **kubectl run <имя_пода> --image=<образ>:** Создает новый под, который будет запускать контейнер из образа.
* **kubectl create deployment <имя_развертывания> --image=<образ>:** Создает новое развертывание, которое будет запускать реплики пода.
* **kubectl expose deployment <имя_развертывания> --type=LoadBalancer:** Создает службу для развертывания, которая будет балансировать нагрузку между репликами пода.


### Управление объектами:

* **kubectl delete pod <имя_пода>:** Удаляет под.
* **kubectl delete deployment <имя_развертывания>:** Удаляет развертывание.
* **kubectl delete service <имя_службы>:** Удаляет службу.
* **kubectl scale deployment <имя_развертывания> --replicas=<количество>:** Изменяет количество реплик в развертывании.
* **kubectl edit pod <имя_пода>:** Редактирует конфигурацию пода.
* **kubectl edit deployment <имя_развертывания>:** Редактирует конфигурацию развертывания.


### Другие команды:

* **kubectl logs <имя_пода>:** Просматривает журналы пода.
* **kubectl port-forward <имя_пода> <порт_контейнера>:<порт_локальный>:** Перенаправляет порт с контейнера на локальный порт.
* **kubectl exec <имя_пода> -- <команда>:** Выполняет команду в контейнере.
