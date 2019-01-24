# mixassio_infra
mixassio Infra repository

ДЗ 5-го урока
команда для захода на `someinternalhost`
```
ssh -A mihailbondarev@35.210.255.185 ssh 10.142.0.2
```

hosts:
```
bastion_IP = 35.210.255.185 
someinternalhost_IP = 35.210.255.185
```

testapp_IP = 35.221.142.125
testapp_port = 9292

Выполнено ДЗ по Packer, сделаны все пункты

Сделана первая часть домашки по терраформу, основная проблема была с ключами, для `.examle` поменял ключи на 
```
public_key_path = "~/.ssh/authorized_keys"
private_key_path = "~/.ssh/authorized_keys"
```
и тесты прошли

# ansible-1
вывод `ansible-playbook clone.yml`
```
PLAY [Clone] *******************************************************************

TASK [Gathering Facts] *********************************************************
ok: [appserver]

TASK [Clone repo] **************************************************************
ok: [appserver]

PLAY RECAP *********************************************************************
appserver                  : ok=2    changed=0    unreachable=0    failed=0

```
`changed=0` проверили - всё на месте
после 
```
app -m command -a 'rm -rf ~/reddit'
ansible-playbook clone.yml
```
вывод
```
PLAY [Clone] *******************************************************************

TASK [Gathering Facts] *********************************************************
ok: [appserver]

TASK [Clone repo] **************************************************************
ok: [appserver]

PLAY RECAP *********************************************************************
appserver                  : ok=2    changed=1    unreachable=0    failed=0
```
`changed=0` проверили - нету, было удалено и склонировали
