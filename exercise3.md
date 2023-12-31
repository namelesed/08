## Типы и уровни логов:

**Лог**— это текстовый файл, который содержит системную информацию о работе ПО или сервера. В лог вносятся данные о действиях, выполненных программой или пользователем.

### Для удобства обработки логов их делят на типы:

- **системные**, связанные с системными событиями,

- **серверные**, отвечающие за процесс обращения к серверу,

- **почтовые**, работающие с отправлениями,

- **логи баз данных**, которые отражают процессы обращения к базам данных,

- **авторизационные и аутентификационные**, которые отвечают за процесс входа, выхода из системы, восстановление доступа и пр.

У каждого типа логов свой журнал записи. Для проверки логов авторизации нужно идти в журнал доступов, чтобы проверить загрузку системы — в журнал ```dmesg```, за данными о запросах пользователей — в ```access_log```. Когда одни логи пишутся отдельно от других, проще диагностировать ситуацию и найти источник проблемы.

### Чтобы упростить поиск и чтение логов, их делят на уровни. Основных четыре:

1. **Debug** — запись масштабных переходов состояний, например, обращение к базе данных, старт/пауза сервиса, успешная обработка записи и пр.

2. **Warning** — нештатная ситуация, потенциальная проблема, может быть странный формат запроса или некорректный параметр вызова.

3. **Error** — типичная ошибка.

4. **Fatal** — тотальный сбой работоспособности, когда нет доступа к базе данных или сети, сервису не хватает места на жестком диске.

Дополнительно файл логирования может расширяться записями еще двух уровней:

1. **Trace**  — пошаговые записи процесса. Полезен, когда сложно локализовать ошибку.

2. **Info** — общая информация о работе службы или сервиса.

Работа с уровнями логирования регламентируется методическими документами и внутренними правилами организации. В них может определяться соответствие источника сообщения уровню логирования, значимость, порядок обработки каждого уровня и другие параметры.

### Какое расширение имеет файл с логами:

Логи хранятся в файлах с расширением ```.log```. Их можно открыть как обычные текстовые файлы и просмотреть содержимое.

### Какие программы используются для просмотра логов:

- **Менеджер событий SolarWinds Security** (30-дневная бесплатная пробная версия) - инструмент анализа журналов для Windows, обеспечивающий централизованный мониторинг журналов. Платформа предлагает обнаружение времени события, чтобы помочь пользователю быстро обнаруживать угрозы. Данные, обрабатываемые SolarWinds Security Event Manager, шифруются в состоянии покоя и в пути, поэтому не могут быть прочитаны неуполномоченными лицами.
- **Сетевой монитор Paessler PRTG** (30-дневная бесплатная пробная версия) - это платформа мониторинга сети, которая включает в себя Датчик журнала событий Windows и Syslog Receiver Sensor. Датчик журнала событий Windows контролирует файлы журнала системы и приложений Windows и отображает частоту сообщений журнала. Syslog Receiver Sensor записывает количество файлов системного журнала в секунду, отправляемых устройствами в сети, и фильтрует их. Фильтры можно настраивать, чтобы вы могли определить, какое действие вызовет тревогу.
- **Papertrail** (бесплатный план) - это анализатор логов для Windows, которая автоматически просматривает данные вашего журнала. При сканировании данных журнала вы можете выбрать, какую информацию вы хотите отображать в результатах сканирования.
- **Loggly** (14-дневная бесплатная пробная версия) -  онлайн-консолидатор логов с отличными инструментами анализа. Loggly позволяет анализировать все события, происходящие в вашей системе, включая удаленные сайты и облачные сервисы. Это отличный пакет, который включает в себя пространство хранения и функции агрегации журналов.
- **ManageEngine EventLog Analyzer** (30-дневная бесплатная пробная версия) - комплексный монитор событий для Windows Server и Linux. Это инструмент анализа журналов с оптимизированным пользовательским интерфейсом. ManageEngine EventLog Analyzer собирает журналы с платформ баз данных, веб-серверов, маршрутизаторов, коммутаторов, гипервизоров, сканеров уязвимостей, систем Linux, систем Unix, брандмауэров и решений Endpoint Security. Splunk Free доступна бесплатно и поддерживает одного пользователя с 500 МБ данных в день.
- **Splunk** - широко используемый монитор журналов с оповещениями в режиме реального времени, доступный для Windows, Mac OS и Linux. Splunk отслеживает данные журнала и машины в режиме реального времени. Splunk-х универсальность позволяет ему получать данные журнала практически с любого устройства или приложения в вашей сети. При использовании программы вы можете использовать панель поиска для просмотра в режиме реального времени и исторических данных. Существуют также поисковые подсказки, которые помогут вам легче найти нужную информацию. 
- **XpoLog** - интерактивный монитор журнала, который использует AI для обнаружения ошибок и вторжений. ы с производительностью и создавать оповещения. Пользователи могут определять правила оповещения и реализовывать свои собственные правила фильтрации. Базовая версия бесплатно и поддерживает 1 ГБ в день с неограниченным объемом данных и пять дней хранения данных. 
- **LOGalyze** - бесплатный монитор журнала с открытым исходным кодом. Продукт поддерживает приборы, хосты Windows, и Linux/Unix серверы с обнаружение событий в реальном времени. После сбора данных журнала вы можете использовать функцию поиска программы, чтобы найти нужную вам информацию. Пользователи также могут определять свои собственные оповещения. 
- **Datadog** - онлайн анализатор логов с живыми оповещениями. С Datadog Вы можете записывать и искать в журнале данных с самых разных устройств и приложений. Datadog-х визуализация отображает данные журнала в виде графиков, чтобы вы могли видеть, как производительность сети менялась с течением времени.
- **EventTracker** - анализатор и менеджер сообщений журнала для сред Windows. Программа может обнаруживать события безопасности в режиме реального времени. 
- **LogDNA** - облачный анализатор сообщений в реальном времени доступен по подписке. LogDNA это программная платформа для управления журналом, которая может отслеживать данные журнала в режиме реального времени. 