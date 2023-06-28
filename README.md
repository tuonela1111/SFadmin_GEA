# SFadmin_GEA
Итоговый проект 3

#1 UZAB-server - установка вручную: Zabbix, Grafana, Ansible, OpenVPN, filebeat;
               - роли ansible:  install_mysql_server.yml
                              
#2 UWDM-server - роли ansible:  install_openvpn.yml
                                install_zabbix_agent.yml
                                install_nginx_apache2.yml                                 
                                install_java.yml
                                install_filebeat.yml
                                install_mysql_server.yml

                   Non-ansible installation: bind9 (DNS-сервер устанавливается один раз и используется долгое время) 
                                             Wordpress (устанавливается один раз для этого задания) 
                                             mail:postfix+dovecot+roundcube (почтовый сервер устанавливается один раз и используется долгое время)

                   !!! Письма наружу по 25 порту отправляются только на внутренние адреса и адреса почты Яндекса !!!
                       (ниже приведен запрос в службу поддержки)

#3 CELK-server - роли ansible:  install_openvpn.yml
                                install_zabbix_agent.yml   
                                copy_elk.yml
                                install_java.yml
                                install_elk.yml
                                  
                   Non-ansible installation: PostgreSQL-12 (по заданию требуется именно эта версия)
                                             pgadmin4


https://console.cloud.yandex.ru/support/tickets/LS779379?utm_source=emailing&utm_campaign=support_ticket_reply&utm_term=support-ticket-replied&utm_medium=mail&utm_id=875582da-c7b7-4ef3-9727-be3b039c558a
Обращение
LS779379
Евгений Глазков
23.05.2023, в 02:34
Отправка писем наружу
Здравствуйте. Создал в облаке на сервере (публичный ip 158.160.44.233, к которому привязан мой домен evglaz.ru) почту. 
Письма наружу отправляются только на адреса почты Яндекса. Прошу открыть мне порты для отправки почты на другие адреса.

Служба поддержки
23.05.2023, в 02:55
Здравствуйте!

В Яндекс Облаке блокируем трафик в целях безопасности по порту 25. 
Подробнее описали здесь: https://cloud.yandex.ru/docs/vpc/concepts/address#port-25. 
Трафик по 25 порту разрешён только на почтовые серверы Яндекса.
