Соглашение по адресации подключенных устройств

[ip(legacy), mac, imei, deveui адрес ] / тип порта / номер порта (локально уникальное) / адрес на порту (локально  уникальный) / ... / имя порта (локально уникальное) / адрес на порту (локально  уникальный)


пример 00:00:00:00:00:00:85:36/com/1/1
       00:00:00:00:00:00:85:36/pulse/1
       00:00:00:00:00:00:85:36/com/1/1/pulse/1


00:00:00:00:00:00:85:36
└── com
    ├── 1
    │   └── 1
    │       └── pulse
    │           └── 1
    └── 2
        ├── 1
        │   └── pulse
        │       └── 1
        └── 2
            └── pulse
                └── 1
