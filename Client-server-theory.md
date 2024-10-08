
## Клиент - серверная архитектура (Client-Server Architecture)
### Клиент - сервер
вычислительная или сетевая архитектура, в которой задания или сетевая нагрузка распределены между поставщиками услуг, называемыми серверами, и заказчиками услуг, называемыми клиентами. Фактически клиент и сервер - это программное обеспечение. Обычно эти программы расположены на разных вычислительных машинах и взаимодействуют между собой через вычислительную сеть посредством сетевых протоколов, но они могут быть расположены также и на одной машине. Программы-серверы ожидают от клиентских программ запросы и предоставляют им свои ресурсы в виде:
* данных (например, загрузка файлов посредством HTTP, FTP, BitTorrent, потоковое мультимедиа или работа с базами данных);
* сервисных функций (например, работа с электронной почтой, общение посредством систем мгновенного обмена сообщениями или просмотр web-страниц во всемирной паутине).

Поскольку одна программа-сервер может выполнять запросы от множества программ-клиентов, ее размещают на специально выделенной вычислительной машине, настроенной особым образом, как правило, совместно с другими программами-серверами, поэтому производительность этой машины должна быть высокой. Из-за особой роли такой машины в сети, специфики ее оборудования и программного обеспечения, её также называют сервером, а машины, выполняющие клиентские программы, соответственно, клиентами.

### Одноуровневая архитектура (1-Tier)

* Одноуровневая архитектура «клиент-сервер» (1-Tier) - такая, где все прикладные программы рассредоточены по рабочим станциям, которые обращаются к общему серверу баз данных или к общему файловому серверу. Никаких прикладных программ сервер при этом не исполняет, только предоставляет данные.
* В целом, такая архитектура очень надежна, однако, ей сложно управлять, поскольку в каждой рабочей станции данные будут присутствовать в разных вариантах. Поэтому возникает проблема их синхронизации на отдельных машинах. В общем, как можно видеть из рисунка, в этой архитектуре просматривается еще один уровень - базы данных, что дает повод во многих случаях называть её двухуровневой.

### Двухуровневая архитектура (2-Tier)

* К двухуровневой архитектуре «клиент-сервер» следует относить такую, в которой прикладные программы сосредоточены на сервере приложений (Application Server), например, сервере 1С или сервере CRM, а в рабочих станциях находятся программы-клиенты, которые предоставляют для пользователей интерфейс для работы с приложениями на общем сервере.

* Такая архитектура представляется наиболее логичной для архитектуры «клиент-сервер». В ней, однако, можно выделить два варианта. Когда общие данные хранятся на сервере, а логика их обработки и бизнес-данные хранятся на клиентской машине, то такая архитектура носит название “fat client thin server” (толстый клиент, тонкий сервер). Когда не только данные, но и логика их обработки и бизнес-данные хранятся на сервере, то это называется “thin client fat server” (тонкий клиент, толстый сервер). Такая архитектура послужила прообразом облачных вычислений (Cloud Computing).

### Трехуровневая архитектура (3-Tier)

* В трехуровневой архитектуре сервер баз данных, файловый сервер и другие представляют собой отдельный уровень, результаты работы которого использует сервер приложений. Логика данных и бизнес-логика находятся в сервере приложений. Все обращения клиентов к базе данных происходят через промежуточное программное обеспечение (middleware), которое находится на сервере приложений. Вследствие этого, повышается гибкость работы и производительность.

### Многоуровневая архитектура (N-Tier)

* В отдельный класс архитектуры «клиент-сервер» можно вынести многоуровневую архитектуру, в которой несколько серверов приложений используют результаты работы друг друга, а также данные от различных серверов баз данных, файловых серверов и других видов серверов.

* По сути, предыдущий вариант, трехуровневая архитектура - не более, чем частный случай многоуровневой архитектуры.

* Преимуществом многоуровневой архитектуры является гибкость предоставления услуг, которые могут являться комбинацией работы различных приложений серверов разных уровней и элементов этих приложений.
* Очевидным недостатком является сложность, многокомпонентность такой архитектуры.

## Монолин и микросервисы

Микросервисная архитектура или просто микросервисы - это особый метод разработки программных систем, который пытается сосредоточиться на создании однофункциональных модулей с четко определенными интерфейсами и операциями. Эта тенденция стала популярной в последние годы, поскольку предприятия стремятся стать более гибкими и перейти к DevOps и непрерывному тестированию.

Микросервисы имеют множество преимуществ для Agile- и DevOps-команд - как отмечает Мартин Фаулер, Netflix, eBay, Amazon, Twitter, PayPal и другие звезды технологий перешли от монолитной к микросервисной архитектуре. В отличие от микросервисов монолитное приложение строится как единая автономная единица. Это замедляет внесение изменений в приложение, поскольку влияет на всю систему. Модификация, внесенная в небольшой участок кода, может потребовать создания и развертывания совершенно новой версии программного обеспечения. Масштабирование определенных функций приложения также означает, что вам необходимо масштабировать все приложение. Микросервисы решают эти проблемы монолитных систем, будучи максимально модульными. В простейшей форме они помогают создать приложение в виде набора небольших служб, каждая из которых работает в своем собственном процессе и развертывается независимо. Эти сервисы могут быть написаны на разных языках программирования и могут использовать разные методы хранения данных. Хотя это приводит к разработке систем, которые являются масштабируемыми и гибкими, они нуждаются в динамическом преобразовании. Микросервисы часто подключаются через API и могут использовать многие из тех же инструментов и решений, которые выросли в экосистеме RESTful и веб-сервисов. Тестирование этих API может помочь проверить поток данных и информации во время развертывания микросервиса.

Точно так же, как не существует формального определения термина «микросервисы», нет и стандартной модели, которую вы увидите представленной в каждой системе, основанной на этом архитектурном стиле. Но вы можете ожидать, что большинство микросервисных систем будут иметь несколько примечательных характеристик:

* Мультикомпонентные: Программное обеспечение, созданное как микрослужбы, по определению может быть разбито на несколько составных служб. Почему? Таким образом каждую из этих служб можно развертывать, настраивать, а затем повторно развертывать независимо друг от друга без ущерба для целостности приложения. В результате вам может потребоваться изменить только одну или несколько отдельных служб вместо повторного развертывания целых приложений. Но у этого подхода есть свои недостатки, в том числе дорогостоящие удаленные вызовы (вместо вызовов внутри процесса), более грубые удаленные API и повышенная сложность при перераспределении обязанностей между компонентами;

* Созданы для бизнеса: Стиль микросервисов обычно организован вокруг бизнес-возможностей и приоритетов. В отличие от традиционного монолитного подхода к разработке, когда разные команды уделяют особое внимание, скажем, пользовательскому интерфейсу, базам данных, технологическим уровням или логике на стороне сервера, в микросервисной архитектуре используются кроссфункциональные команды. В обязанности каждой команды входит создание конкретных продуктов на основе одного или нескольких отдельных сервисов, взаимодействующих через шину сообщений. В микросервисах команда владеет продуктом всю жизнь, как в часто цитируемой максиме Amazon: “Вы создаете это, вы это запускаете”;

* Простая маршрутизация: Микросервисы действуют примерно так же, как классическая система UNIX: они получают запросы, обрабатывают их и генерируют соответствующий ответ. Это противоположно тому, как работают многие другие продукты, такие как ESB (Enterprise Service Buses), где используются высокотехнологичные системы для маршрутизации сообщений, хореографии и применения бизнес-правил. Можно сказать, что у микросервисов есть интеллектуальные конечные точки (endpoints), которые обрабатывают информацию и применяют логику, и тупые каналы (?dumb pipes), по которым информация течет;

* Децентрализованные: Поскольку микросервисы включают множество технологий и платформ, старые методы централизованного управления не являются оптимальными. Сообщество микросервисов предпочитает децентрализованное управление, потому что его разработчики стремятся создавать полезные инструменты, которые затем могут использоваться другими для решения тех же проблем. Как и децентрализованное управление, микросервисная архитектура также способствует децентрализованному управлению данными. Монолитные системы используют одну логическую базу данных для разных приложений. В микросервисном приложении каждая служба обычно управляет своей уникальной базой данных;

* Отказоустойчивые: Как всесторонне развитый ребенок, микросервисы созданы, чтобы справляться с ошибками. Поскольку несколько уникальных и разнообразных сервисов взаимодействуют друг с другом, вполне возможно, что сервис может выйти из строя по той или иной причине (например, когда поставщик недоступен). В этих случаях клиент должен позволить своим соседним службам работать, пока он отключается. Однако мониторинг микросервисов может помочь предотвратить риск сбоя. По понятным причинам это требование делает микросервисы более сложными по сравнению с архитектурой монолитных систем;

* Эволюционные: Архитектура микросервисов представляет собой эволюционный дизайн и, опять же, идеально подходит для эволюционирующих систем, в которых вы не можете полностью предвидеть типы устройств, которые однажды могут получить доступ к вашему приложению. , можно постепенно преобразовать в микросервисы, взаимодействующие с более старой монолитной архитектурой через API.

## Веб-страница, веб-сайт, веб-приложение, веб-сервис, веб-сервер







### Принципы проектирования REST API (Если выполняются все принципы, то RESful)
Теперь, когда мы рассмотрели основы и узнали об определении REST API, давайте перейдем к шести принципам REST, которые определяют дизайн API:
* Клиент-сервер
  
Принцип REST основан на концепции, согласно которой клиент и сервер должны быть изолированы друг от друга и иметь возможность развиваться независимо. Таким образом, вы можете улучшить управляемость на многочисленных платформах и увеличить масштабируемость за счет оптимизации серверных компонентов, поскольку проблемы пользовательского интерфейса отделены от проблем хранения данных.
* Stateless

Этот принцип REST требует, чтобы API не сохраняли состояние, что позволяет выполнять независимые вызовы. Более того, каждый вызов включает в себя данные, необходимые для его эффективного завершения.
Другими словами, каждый запрос, отправляемый клиентом на сервер, должен включать всю информацию, необходимую для обработки запроса.
* Кэшируемый
  
Поскольку API без сохранения состояния может увеличить накладные расходы на запросы, управляя огромными нагрузками входящих и исходящих вызовов, дизайн REST API должен хранить кэшируемые данные. Согласно этому принципу проектирования API, данные в ответе должны быть косвенно или классифицированы как кэшируемые или некэшируемые.
Если ответ кэшируется, кэшу клиента предоставляется право повторно использовать эти данные ответа для аналогичных запросов в будущем.
* Единый интерфейс
  
Чтобы отделить клиент от сервера, вам необходимо иметь единый интерфейс, который позволяет автономно разрабатывать приложение без жесткой привязки его сервисов, моделей и действий к самому уровню API. Этот принцип проектирования оптимизирует всю архитектуру системы и повышает наглядность. коммуникаций.Некоторые архитектурные элементы управления требуют управления производительностью элементов в архитектуре REST API для достижения единообразного интерфейса.
Архитектура REST API определяет принципы REST с помощью четырех элементов управления интерфейсом, включая идентификацию ресурсов, управление ресурсами посредством представлений, обеспечение самоописательной связи и превращение гипермедиа в механизм состояния приложения.
* Многоуровневая система
  
Архитектура REST API включает в себя несколько уровней, которые работают вместе, создавая иерархию, помогающую создать более масштабируемое и гибкое приложение. Благодаря многоуровневой системе приложение имеет более высокий уровень безопасности, поскольку компоненты каждого уровня не могут взаимодействовать за пределами последующего уровня. Более того, он балансирует нагрузки и предлагает общие кэши для стимулирования Масштабируемость.
Система многоуровневой архитектуры REST API обладает большей стабильностью, поскольку ограничивает производительность компонентов. так что каждый компонент не может «видеть» дальше непосредственного слоя, с которым он смешивается.
* Код по требованию
  
Принцип REST обеспечивает передачу кода или апплетов через API, используемый внутри приложения.
Определение REST API позволяет расширять функциональность клиента путем загрузки и реализации кода в форме апплетов или сценариев. Это оптимизирует работу клиентов за счет уменьшения количества функций, которые необходимо предварительно реализовать.
Большую часть времени сервер возвращает статическое представление ресурса в формате XML или JSON. Но при необходимости серверы могут доставить клиенту исполняемый код.

### 5 категорий серверных ответов:
* 1xx Информационный ответ. Запрос получен и понятен. Обработка запросов продолжается.
* 2xx Успех. Акция была успешно принята, понята и принята.
* 3xx Перенаправление. Для выполнения запроса клиент должен принять дальнейшие меры.
* 4xx Ошибки клиента. Ошибка можно было вызвать клиентом. Запрос содержит плохой синтаксис или не может быть выполнен.
* 5xx Ошибки сервера. Сервер столкнулся с ошибкой и не выполнил запрос.

### Общие коды статуса HTTP

* Статус-код 200

— это стандартный код статуса «OK» для успешного запроса HTTP. Ответ, который возвращается, зависит от запроса. Например, для запроса GET ответ будет включен в тело сообщения. Для запроса PUT/POST ответ будет включать ресурс, содержащий результат действия.
* Статус-код 201

 — это код статуса, который подтверждает, что запрос был успешным и, как следствие, был создан новый ресурс. Как правило, это код статуса, который отправляется после запроса POST/PUT.
* Статус-код 204

 – Этот код статуса подтверждает, что сервер выполнил запрос, но не нуждается в возврате информации. Примеры этого кода статуса включают запросы на удаление или если запрос был отправлен через форму, и ответ не должен вызывать обновление формы или загрузку новой страницы.
* Статус-код 304

 — код состояния, используемый для кэширования браузера. Если ответ не был изменен, клиент/пользователь может продолжать использовать ту же версию ответа/кэша. Например, браузер может запросить, если ресурс был изменен с определенного времени. Если это не так, отправляется код статуса 304. Если он был изменен, отправляется код состояния 200 вместе с ресурсом.
* Код статуса 400

 – Bad Request Запрос неправильный. Ошибка возникает в случае, если браузер клиента отправляет некорректный запрос серверу. Это может быть синтаксическая ошибка. Например, в запросе отсутствовали символы завершения строки.
* Код статуса 401

 – Unauthorized Этот код ошибки HTTP клиента сообщает, что на ресурс можно войти, используя действительный ID пользователя и пароль. Отказ в доступе также возникает, если пользователь неправильно ввел данные для авторизации (логин и пароль).
* Код статус 402

 – Payment Required Это нестандартный HTTP-статус. Он означает, что запрос не может быть выполнен, пока пользователь не произведет оплату. Код используется в платных пользовательских сервисах, а не в хостинговых провайдерах.
* Статус-код 403

 – Forbidden Запрет доступа к запрашиваемой странице. Он связан с тем, что у пользователя нет прав. Доступ может быть ограничен для определенных IP или в случае, если неавторизованный клиент пытается открыть файлы в системной папке. Этот код встречается, если сервер обнаружил вредоносные данные.
* Статус-код 404

 —  Not Found Это один из самых распространенных кодов ошибки HTTP клиента. Сервер дает ответ, что страница не найдена по данному URL. Например, страница перенесена на другой адрес. Не стоит путать код 404 с ошибкой «Сервер не найден». В данном случае клиент в состоянии общаться с сервером, но данных по его запросу нет.
* Статус-код 405

 —  Method Not Allowed Сервер сообщает, что используемый метод не может применяться на данном ресурсе. Он предложит доступные методы в заголовке Allow.
 409

 — Conflict Запрос пользователя вызывает конфликт с текущим состоянием сервера или несовместим с другим запросом.
* Код статуса 410

 – Gone Это ответ сервера в случае, если запрашиваемый контент больше недоступен или удален.

*  Статус-код 422

- Unprocessable Entity — сервер успешно принял запрос, может работать с указанным видом данных (например, в теле запроса находится XML-документ, имеющий верный синтаксис), однако имеется какая-то логическая ошибка, из-за которой невозможно произвести операцию над ресурсом. Введено в WebDAV.

* Статус код 500

– Internal Server Error
Код ошибки HTTP сервера появляется, когда он встречает ситуацию, обработка которой ему не знакома. Также возможен вариант, что данный запрос не поддерживается сервером и его обработка невозможна. В таких ситуациях сервер тоже отправляет HTTP-статус 500.

* Статус код 501

 — Not Implemented Ошибка 501 сообщает, что метод запроса сервером не поддерживается и его невозможно корректно обработать.
В ряде случаев в теле ошибки может быть указано: «Отправьте запрос позднее. Возможно, необходимая функция будет доступна».

* Статус код 503

 — Service Unavailable Сервер временно не доступен. Он не может обработать запрос клиента по следующим причинам:

* Статус код 505

 — HTTP Version Not Supported Этот код аналогичен 426. Он сообщает, что сервер не поддерживает версию протокола HTTP, который используется клиентом. Это случается, если используется устаревший формат HTTP-протокола. Решением проблемы будет установка одной версии.

# Методы HTTP запроса


























































































































