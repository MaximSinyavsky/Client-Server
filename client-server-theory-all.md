## ✅1.	Что такое клиент?
Клиент - это устройство на стороне пользователя, которое отправляет запрос к серверу для предоставления информации или выполнения определенных действий.
## ✅2.	Что такое сервер
Сервер - это более мощный компьютер или оборудование, предназначенное для решения определенных задач по выполнению программного кода, сервисных функций по запросу клиентов, предоставления пользователям доступа к определенным ресурсам, хранения информации и баз данных.
## 3.	Что такое Interface
## 4.	Примеры Interface 
## ✅5.	Какие бывают уровни клиент серверной архитектуры?
### Клиент-серверная архитектура обычно включает несколько уровней:
* Одноуровневая архитектура: Клиент напрямую взаимодействует с сервером. Простейший случай, часто встречающийся в небольших приложениях.
* Двухуровневая архитектура: Клиент и сервер разделены на два уровня. Клиентский уровень отвечает за пользовательский интерфейс, а серверный — за обработку данных и логику приложения.
* Трехуровневая архитектура: Включает три уровня — клиентский, сервер приложений (где выполняется бизнес-логика) и сервер данных (БД). Часто используется в крупных корпоративных приложениях.
* Многоуровневая архитектура: Включает более трех уровней. Например, может быть уровень веб-сервера, сервер приложений, сервер базы данных и уровни для внешних сервисов и API. Такая архитектура обеспечивает лучшую масштабируемость и распределение нагрузки.

## ✅6.	горячий резерв серверов? холодный резерв серверов? 
Для балансировщика на серверах существуют такие понятия как горячий и холодный резерв.
* Горячий резерв — когда у нас есть несколько серверов, работающих в параллель, и балансировщик распределяет нагрузку между ними.
* Холодный резерв — когда у нас второй сервер является резервной копией первого. Все запросы идут на первый сервер, второй в ожидании.

## ✅7.	балансировщики
Балансировщик нагрузки — это специальное устройство или программа, которая распределяет входящий трафик (запросы) между несколькими серверами.

Балансировщик может быть размещен до (на фронтэнде) или после (на бэкенде) серверов в зависимости от архитектуры системы.

## ✅8.	Прокси сервер
Прокси-сервер — это промежуточное звено между пользователем и сайтом. Если пользователь не использует прокси-сервер, веб-сайт может определить его местоположение по IP-адресу.

Прокси-сервер выполняет разные задачи. В зависимости от типа и настроек он может кэшировать информацию или фильтровать веб-контент.

### Для чего нужен proxy:
* обеспечивает анонимность — прокси меняет IP-адрес, поэтому сторонним лицам сложнее отследить местоположение пользователя;
* блокирует сайты — можно настроить его так, чтобы ограничить доступ к определенным ресурсам, например, социальным сетям в офисе;
* ускоряет работу — за счет кэширования данных страницы загружаются быстрее;
* фильтрует контент — прокси позволяет отсеивать нежелательную рекламу и опасные сайты.
### Прокси-сервер также можно использовать для бизнес-задач:
* контролировать трафик — компании могут отслеживать запросы сотрудников и анализировать их активность в интернете;
* повышать безопасность — он защищает от утечек данных, делая взаимодействие с сетью более безопасным;
* оптимизировать рекламу — с его помощью можно собирать данные о предпочтениях пользователей и настраивать рекламу точнее.

## ✅9.	Что такое API
API (Application Programming Interface) — это набор правил и протоколов, которые позволяют различным программам взаимодействовать друг с другом. По сути, это способ, с помощью которого один программный компонент может "общаться" с другим. APIs используются повсеместно, от веб-сервисов до настольных приложений, чтобы обеспечивать интеграцию и работу между различными системами и платформами. API предоставляет методы и функции, которые разработчики могут использовать для выполнения определенных задач, таких как доступ к данным, управление пользователями или обмен сообщениями.

## ✅10.	Что такое REST API
REST API (Representational State Transfer API) — это архитектурный стиль для создания веб-сервисов, которые могут взаимодействовать через HTTP-протокол. REST API позволяют различным приложениям обмениваться данными и выполнять операции, используя стандартные HTTP-методы: GET, POST, PUT, DELETE и др.

Простыми словами, REST API позволяют получать доступ к ресурсам сервера (данные, функции и т.д.) через URL-адреса, отправляя запросы и получая ответы в формате JSON или XML. Они широко используются благодаря своей простоте и гибкости, и помогают обеспечить легкую интеграцию между различными системами.

## ✅11.	Требования к архитектуре Rest
Принципы проектирования REST API (Если выполняются все принципы, то RESful)
Теперь, когда мы рассмотрели основы и узнали об определении REST API, давайте перейдем к шести принципам REST, которые определяют дизайн API:

* Клиент-сервер

Принцип REST основан на концепции, согласно которой клиент и сервер должны быть изолированы друг от друга и иметь возможность развиваться независимо. Таким образом, вы можете улучшить управляемость на многочисленных платформах и увеличить масштабируемость за счет оптимизации серверных компонентов, поскольку проблемы пользовательского интерфейса отделены от проблем хранения данных.

* Stateless

Этот принцип REST требует, чтобы API не сохраняли состояние, что позволяет выполнять независимые вызовы. Более того, каждый вызов включает в себя данные, необходимые для его эффективного завершения. Другими словами, каждый запрос, отправляемый клиентом на сервер, должен включать всю информацию, необходимую для обработки запроса.

* Кэшируемый

Поскольку API без сохранения состояния может увеличить накладные расходы на запросы, управляя огромными нагрузками входящих и исходящих вызовов, дизайн REST API должен хранить кэшируемые данные. Согласно этому принципу проектирования API, данные в ответе должны быть косвенно или классифицированы как кэшируемые или некэшируемые. Если ответ кэшируется, кэшу клиента предоставляется право повторно использовать эти данные ответа для аналогичных запросов в будущем.

* Единый интерфейс

Чтобы отделить клиент от сервера, вам необходимо иметь единый интерфейс, который позволяет автономно разрабатывать приложение без жесткой привязки его сервисов, моделей и действий к самому уровню API. Этот принцип проектирования оптимизирует всю архитектуру системы и повышает наглядность. коммуникаций.Некоторые архитектурные элементы управления требуют управления производительностью элементов в архитектуре REST API для достижения единообразного интерфейса. Архитектура REST API определяет принципы REST с помощью четырех элементов управления интерфейсом, включая идентификацию ресурсов, управление ресурсами посредством представлений, обеспечение самоописательной связи и превращение гипермедиа в механизм состояния приложения.

* Многоуровневая система

Архитектура REST API включает в себя несколько уровней, которые работают вместе, создавая иерархию, помогающую создать более масштабируемое и гибкое приложение. Благодаря многоуровневой системе приложение имеет более высокий уровень безопасности, поскольку компоненты каждого уровня не могут взаимодействовать за пределами последующего уровня. Более того, он балансирует нагрузки и предлагает общие кэши для стимулирования Масштабируемость. Система многоуровневой архитектуры REST API обладает большей стабильностью, поскольку ограничивает производительность компонентов. так что каждый компонент не может «видеть» дальше непосредственного слоя, с которым он смешивается.

* Код по требованию

Принцип REST обеспечивает передачу кода или апплетов через API, используемый внутри приложения. Определение REST API позволяет расширять функциональность клиента путем загрузки и реализации кода в форме апплетов или сценариев. Это оптимизирует работу клиентов за счет уменьшения количества функций, которые необходимо предварительно реализовать. Большую часть времени сервер возвращает статическое представление ресурса в формате XML или JSON. Но при необходимости серверы могут доставить клиенту исполняемый код.
## ✅12.	Что такое HTTP
HTTP (HyperText Transfer Protocol) — это основной протокол, используемый для передачи данных в интернете. Он определяет, как сообщения формируются и передаются, и какие действия веб-серверы и браузеры должны выполнять в ответ на различные команды. HTTP работает на основе клиент-серверной модели, где клиент (ваш браузер) отправляет запросы на сервер, а сервер отвечает, предоставляя нужные данные (например, веб-страницы, изображения).

Изначально HTTP был разработан для передачи гипертекстовых документов, но теперь используется для передачи любого типа данных, от HTML и JSON до видеозаписей и файлов. HTTP/2 и HTTP/3 — более современные версии, которые обеспечивают улучшенную производительность и безопасность.

## 13.	Что такое HTTPS


HTTPS обычно работает на порту 443, в то время как обычный HTTP использует порт 80. Вы можете заметить эти порты в URL-адресах: https:// (периодически указывают порт 443) и http:// (периодически указывают порт 80). Безопасный обмен данными обеспечивается как раз благодаря этому шифрованию и сертификатам безопасност



## ✅14.	Что такое статус код сервера
Статус-код сервера — это числовой код в ответе от веб-сервера на запрос клиента (обычно веб-браузера), который указывает на результат обработки запроса. Эти коды помогают определить, была ли операция успешной, возникли ли ошибки и какие именно ошибки произошли.
### Основные группы статус-кодов:
* 1xx: Информационные — запрос принят, продолжается обработка.
* 2xx: Успешные — запрос успешно обработан.
* 3xx: Перенаправление — клиенту нужно предпринять дополнительные действия для завершения запроса.
* 4xx: Ошибки клиента — ошибка на стороне клиента.
* 5xx: Ошибки сервера — ошибка на стороне сервера.
## 15.	Какие ты знаешь?

## 16. ✅Что такое IP адрес
IP-адрес (Internet Protocol address) — это уникальный числовой идентификатор, присваиваемый каждому устройству, подключенному к интернету или локальной сети. Он позволяет устройствам обмениваться данными, отправлять и получать информацию.
### Существуют два основных типа IP-адресов:
* IPv4: Состоит из четырех чисел от 0 до 255, разделенных точками (например, 192.168.0.1).
* IPv6: Более современный стандарт, использует восемь групп шестнадцатеричных цифр, разделенных двоеточиями (например, 2001:0db8:85a3:0000:0000:8a2e:0370:7334).

IP-адреса обеспечивают возможность правильного направления данных между отправителем и получателем.
## 17.	Что такое порт
## 18.	Что такое хост?
## 19.	Чем web service отличается от web server ?
## ✅20.	Что такое толстый клиент?
Толстый клиент представляет собой клиентское приложение, которое содержит значительную часть логики и функциональности непосредственно на стороне пользователя. Этот тип клиента активно взаимодействует с сервером, но при этом обладает значительной автономностью.

## ✅21.	Что  такое тонкий клиент?
Тонкий клиент – это клиентское приложение, которое минимизирует логику и функциональность на стороне пользователя, делегируя большинство задач серверу. Он зависит от сервера для предоставления большей части функциональности.

## 22.	Что такое теплый клиент
## 23.	Что такое холодный клиент
## 24.	Что такое куки
## 25.	Что такое кеш
## 26.	Какие ты знаешь методы HTTP
## 27.	Что такое CRUD
## 28.	Чем GET отличается от POST
## 29.	Чем POST отличается от PUT
## 30.	Чем PUT отличается от PUTCH
## 31.	Какие методы бывают идемпотентные
## 32.	Какие методы есть безопасные
## 33.	В чем разница между безопасностью и идемпатентностью?
## 34.	Можно ли в POST передать данные и через URL и через Body
## 35.	Можно ли с помощью URLa передать данные на сервер?
## 36.	Какое ограничение есть у URLa по количеству символов
## 37.	Что такое URL
## 38.	В чем разница между URI, URL, URN ?
## 39.	Из чего состоит путь запроса?
## 40.	Из чего состоит запрос HTTP - реквест
## 41.	Из чего состоят ответы HTTP -респонс
## 42.	Что такое REST 
## 43.	Что такое SOAP
## 44.	Чем REST отличается от SOAP
## 45.	Что такое JSON и XML
## 46.	Каким форматом данных могут быть ключи в JSON
## 47.	Каким форматом данных могут быть значения в JSON

## 48.	Что такое WSDL
## 49.	Что такое WADL
## 50.	Что такое Ad point
## 51.	Что такое атака MAN in the Midl
## 52.	Что такое и какая разница, Идентификация, Аутентификация, Авторизация

## 53.	Как узнать схему API проекта
## 54.	Какие ты знаешь Headers в Request
## 55.	Какие ты знаешь Headers в Responce

## 56.	Какие стореджи браузера ты знаешь?
## 57.	В чем разница между сешин сторедж и локал сторедж?
## 58.	Что такое валидация и верификация

## 59.	Что такое HTML/CSS/JavaScript?
## 60.	Какую структуру имеет веб-страница?
## 61.	Зачем чистить кэш?
## 62.	Какие виды тестирования можно применить только к Web? вопрос на понимание видов тетсирования в применении к вебу

## 63.	Для чего в веб-страницах используют JavaScript?
## 64.	Что такое AJAX?
## 65.	Что такое адаптивная и респонсивная верстка?
## 66.	Как выполнить Debug страницы в браузере?
## 67.	Как протестировать адаптивную верстку?
## 68.	Что такое WebSocket ?

## 69.	SSL и TLS - это?
## 70.	TCP/IP - это
## 71.	Уровни TCP/IP
## 72.	Уровни OSI
## 73.	Что такое FTP?
## 74.	Что такое логи?
## 75.	Что такое логирование?
## 76.	Перечислите типы логов
## 77.	Механизм записи информации в логи
