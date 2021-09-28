#  Написать эссе, в котором анализируется процесс аутентификации пользователей в двух произвольных web-ресурсах.

В настоящее время информационные системы (ИС) различного масштаба стали неотъемлемой частью базовой инфраструктуры государства, бизнеса, гражданского общества. Все больше защищаемой информации переносится в ИС. Современные информационные технологии не только обеспечивают новые возможности организации бизнеса, ведения государственной и общественной деятельности, но и создают значительные потребности в обеспечении безопасности для защиты информации.

Рассмотрим пару вариантов таких как:**Github** и **BlackBoard**

**![Github]() :thumbsup:**
![Github](1git.jpg)

При переходе на страницу мы видим, что необходимо автоизироваться. У нас выдается код 200 значально «Все в порядке» и **Referrer Policy**: strict-origin-when-cross-origin– для запросов в пределах текущего источника отправлять полный Referer, для запросов на другой источник отправлять только значение источника.
```css
etag: W/"a9d243f9cfe38727b8c3aa85f6267368"
expect-ct: max-age=2592000, report-uri="https://api.github.com/_private/browser/errors"
permissions-policy: interest-cohort=()
referrer-policy: origin-when-cross-origin, strict-origin-when-cross-origin
server: GitHub.com
set-cookie: _gh_sess=IrtYJ7Q1YQDjxHp0zXPRBCaBX5%2FgkbYNWdMeSUNtXZy3dFJQAdkRt6fuwu%2ByQ0sk3oCFcqMF4X3w4DoxcgKLZVc61Hsu3H3IUzl%2BwAR1SiOSEwMuYVjh1scMh7%2FXCNM1eaEu5PbMT57oZTzmTUJpYJl2ewz7qwnOucVh1qQQRi3%2FaIWanjsd9Uj5jkvyB5lnh5xkza0fKyYpcr17Hay3eoVHRrjkc6cXfgM%2BrlhFB69fU168X4JqT4zssFe6LyB0Ov7QU8pxkVdB8uZRzFQKRQ%3D%3D--v576DcjBaHtj7yxZ--Rnx0HJqDoWx%2BPL1JNwifFg%3D%3D; path=/; secure; HttpOnly; SameSite=Lax
strict-transport-security: max-age=31536000; includeSubdomains; preload
vary: X-PJAX, X-PJAX-Container
vary: Accept-Encoding, Accept, X-Requested-With
x-content-type-options: nosniff
x-frame-options: deny
x-github-request-id: F67F:60B2:28CE80:2CA6F0:6152FAFC
x-xss-protection: 0
```
**etage** это служебный заголовок который означает:
 Если ETag существует: значит, это вернувшийся посетитель. Можно зафиксировать как удостоверение его личности.
 Если ETag не существует: это новый посетитель. Новый ID. С этого момента этот идентификатор будет включен во все заголовки запросов устройства этого пользователя на сайте.
 **expect-ct**  заголовок, чтобы предотвратить мошеннические SSL-сертификаты для клиентов.  max-age=2592000  скажет браузеру что в течение (2592000 секунд) он не должен взаимодействовать с приложением по небезопасным протоколам. Если нарушение выявленно то должен отправить отчет по указанному URL-адресу.
**Permissions-Policy** Это заголовок безопасности, который определяет, какие функции браузер можно использовать на данном сайте. *interest-cohort=()* запрещает браузеру использовать новую технологию Google FLoC для создания “цифрового” отпечатка пользователя.
**Referrer-Policy** Настраивает уровень детализации для включения в заголовок Referer при уходе со страницы. Помогает предотвратить утечку данных на сайты, куда идут ссылки.
**Strict Transport Security** — механизм, активирующий форсированное защищённое соединение.
**x-github-request-id** заключается в том, что клиент может создать некоторые случайные ID и передать его на сервер.


![Github](2git.jpg)
а уже при входе мы получаем код 302– документ был временно перемещен на новый URL. Код указывает, что данный URI будет учитываться клиентом в последующих запросах. **Referrer Policy: origin**."origin" – отправлять в Referer только текущий источник, а не полный URL-адрес страницы
 Тем самым понимая что вход осуществляется по простой базе данных.


**![BlackBoard]():thumbsdown:**
![BlackBoard](1bleg.jpg)



![BlackBoard](2bleg.jpg)
===================
# Вывод :neutral_face:
