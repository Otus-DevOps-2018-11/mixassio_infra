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
