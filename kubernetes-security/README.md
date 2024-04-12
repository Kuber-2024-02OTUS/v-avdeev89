1. Создаём ServiceAccount для нашего NS
2. Создаём  ClusterRole для нашего NS
3. Добавялем в deployment : spec: serviceAccountName: monitoring 
4. Создеем  ServiceAccount с именем "cd" в пространстве имен "homework"
5. Создаём RoleBinding, который свяжет ServiceAccount "cd" с ролью "admin" в пространстве имен "homework"
6. Запускаем проект kubectl apply -f deployment.yaml -f sa_cd.yml -f sa_monitoring.yml
7. Создаём токен: kubectl create token cd --namespace homework --duration 86400s > token
8. * - добавлено в deployment 53 строка
