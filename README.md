Прежде чем что либо делать со скриптами, убедитесь что отработали в корне модуля команду 
-------------------------------------
`ansible-galaxy install -r requirements.yml`

Установка серверов и приложения:
--------------------------------
1. Установить приложение 
    ```ansible-playbook -i development play-mesos.yml --tags bot-api```
    с параметрами
            `--tags bot-api` - только отдельный сервис
            
4. Рестарт приложения 
    ```ansible-playbook -i development play-mesos.yml --extra-vars "restart_app=true"```
5. Удалить приложение 
    ```ansible-playbook -i development play-mesos.yml --extra-vars "delete_app=true"```    