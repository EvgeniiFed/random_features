### Ускоряем Ansible с помощью mitogen

https://mitogen.networkgenomics.com/ansible_detailed.html#installation

Скачиваем архив для установки:
```
wget https://networkgenomics.com/try/mitogen-0.2.9.tar.gz
```

Далее распаковываем архив:
```
tar -xvf mitogen-0.2.9.tar.gz
```

Переносим файлы в директорию с ansible

```
mv mitogen-0.2.9 /etc/ansible/mitogen
```

Переходим в настройки ansible

```
nano /etc/ansible/ansible.cfg
```

Вносим следующие строчки:

```
[defaults]
strategy_plugins = /etc/ansible/mitogen/ansible_mitogen/plugins/strategy
strategy = mitogen_linear
```

Готово
