
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

* [device.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/device.json) - описание устройства общего вида (базовый типа для счетчиков и успд)
  * [device-data-record.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/device-data-record.json) - данные с устройства
  * [uspd.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/uspd.json) - успд
  * [meter.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/meter.json) - счетчик общего вида (базовый типа для счетчиков)
     * [archive-info.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/archive-info.json) - описание архива счетчика
     * [modbus-register.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/modbus-register.json) - modbus регистр
         * [modbus-register-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/modbus-register-data.json) - значение modbus регистра (текущие и их срезы)
  * [pulse-meter.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/pulse-meter.json) - импульсный счетчик
     * [pulse-meter-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/pulse-meter-data.json) - данные импульсного счетчика (текущие и архивы)
  * [electricity-meter.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/electricity-meter.json) - электросчетчик
     * [electricity-energy-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/electricity-energy-data.json) - структура данных энергии
     * [electricity-power-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/electricity-power-data.json) - структура данных мощности
     * [electricity-phase-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/electricity-phase-data.json) - сруктура данных 1-ой фазы
     * [electricity-meter-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/electricity-meter-data.json) - данные электросчетчика (текущие и их срезы)
     * [electricity-energy-log.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/electricity-energy-log.json) - архив данных по электроэнергии
     * [electricity-power-log.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/electricity-power-log.json) - архив данных мощности (профиль мощности)
     * [electricity-max-power-log.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/electricity-max-power-log.json) - архив данных максимальных мощностей в утреннее и вечернее время
  * [heat-meter.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/heat-meter.json) - теплосчетчик
     * [heat-system.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/heat-system.json) - теплосистема 
         * [heat-system-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/heat-system-data.json) - данные теплосистемы (текущие и архивы)
         * [heat-system-events-duration.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/heat-system-events-duration.json) - структура данных продолжительности событий теплосистемы
  * [measurer.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/measurer.json) - измеритель
     * [measurer-channel.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/measurer-channel.json) - канал измерителя
         * [measurer-channel-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/measurer-channel-data.json) - измеренное значение канала (текущие и их срезы)
  * [port.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/port.json) - описание порта общего вида
     * [analog-port.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/analog-port.json) - аналоговый порт
     * [com-port.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/com-port.json) - COM порт
     * [ethernet-port.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/ethernet-port.json) - ethernet
     * [pulse-port.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/pulse-port.json) - импульсный вход/выход
  * [extension-module.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/extension-module.json) - модуль расширения
* [schedule.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/schedule.json) - расписание опроса
  * [schedule-user-data.json](https://sandbox.proxia.ru/jsonschemaviewer/?schema=https://sandbox.proxia.ru/schemas/v02/schedule-user-data.json) - структура пользовательских данных расписания 