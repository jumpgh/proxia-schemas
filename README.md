
### Текущая схема сообщений


**Перечень сообщений, используемых при взаимодействии с очередью сообщений.**

**LoRaWAN сервер**

|топик|отправитель|получатель|содержимое|описание|
|-----|-----------|----------|----------|--------|
|device/out/[devaddr]|LoRaWAN сервер|?|[lora-message.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/lora-message.json) |message from lorawan device|
|device/out/[devaddr]|?|LoRaWAN сервер|?|message to lorawan device|




**Служба опроса**

|топик|отправитель|получатель|содержимое|описание|
|-----|-----------|----------|----------|--------|
|/pollservice/registration/[poll srv id]|Poll Service|Poll Config Service|[poll-service-registration.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/poll-service-registration.json)|Регистрация службы опроса|
|/pollservice/[poll srv id]/object/list|Poll Config Service|Poll Service|[object-list.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/object-list.json) | Список подключенных устройств |
|/device/indications/heat/archive/[device id]|Poll Service|?|[heat-system-message.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/heat-system-message.json)|Сообщение от службы опроса с показаниями теплосчетчика|


**Список описанных типов данных**

 - [poll-service-registration.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/poll-service-registration.json) - Регистрация службы опроса
 - [heat-system-message.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/heat-system-message.json) - Сообщение от службы опроса с показаниями теплосчетчика
 - [heat-system-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/heat-system-data.json) - Показания теплосчетчика
 - [meter.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/meter.json) - Счетчик
 - [modbus-register-info.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/modbus-register-info.json) - 
 - [object-list.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/object-list.json) - Список подключенных устройств
 - [schedule.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/schedule.json) - расписание опроса
 - [uspd.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/uspd.json) - описание УСПД
 - [meter.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v01/meter.json) - описание счетчика


 ### Планируемая схема сообщений

**NB!** Описание и наименования полей должны быть на английской, желательно техническом и, по возможности, интуитивно понятном. В будущем, описательные поля схемы (description) будут использоваться при создании форм ввода, подсказок и т.п. с соответствующей локализацией через словари терминов.

**Список описанных типов данных**

- [com-port.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/com-port.json) - настройки com порта
- [modbus-register.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/modbus-register.json) - настройки modbus регистра
- [device.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/device.json) - описание устройства общего вида (базовый типа для счетчиков и успд)
- [uspd.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/uspd.json) - успд
- [meter.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/meter.json) - счетчик общего вида (базовый типа для счетчиков)
- [heat-meter.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/heat-meter.json) - теплосчетчик
- [electricity-meter.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/electricity-meter.json) - электросчетчик
- [extension-module.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/extension-module.json) - модуль расширения (пока совсем сырое)
- [schedule.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/schedule.json) - расписание опроса (пока совсем сырое)
- [heat-system-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/heat-system-data.json) - данные теплосистемы 
- [heat-system.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/heat-system.json) - теплосистема 
- [archive-info.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/archive-info.json) - описание архива счетчика