# Тестовое задание на вакансию php разработчика в компанию wowworks
						
Необходимо сделать конвертер PDF в HTML слайдер. Основной алгоритм заключается в следующем:
						
1. Открываем страницу, которая содержит форму для загрузки PDF.
2. Выбираем PDF файл, нажимаем кнопку «Конвертировать».
3. Появляется «полоса загрузки», которая в процентах показывает процесс конвертации. (реализация этого пункта необязательна, но будет плюсом).
4. После того как процесс завершен, открывается новая страница на которой отображается HTML слайдер. В качестве слайдов используются изображения страниц PDF файла.
5. Также на странице слайдера есть кнопка «Скачать», при нажатии на которую скачивается zip архив, содержащий:						
  * index.html, который содержит слайдер.
  * папку images, в которой хранятся изображения, конвертированные из PDF
  * папку assets, в которой хранятся необходимые ресурсы, например JS- библиотека слайдера.
6. После генерации архива оставлять ссылку для просмотра слайдера и повторного скачивания архива, доступную в течение 30 минут после генерации.
7. Так же необходимо реализовать REST API метод для получения списка ссылок изображений конкретного слайдера (по его id) для генерации кастомных слайдеров на сторонних сайтах (json).

### Требования / Ограничения	

##### PDF				
* Ориентация – портретная;
* Количество страниц – не больше 20;
* Размер файла – не более 50 Мб.
						
##### Технологии				
* PHP, HTML, JS;
* Возможно использование готовых классов и библиотек;
* Framework – предпочтительно Yii2 или без framework’ов; 
* Возможно использование exec();
* Можно использовать composer;
* Должны быть unit тесты;
* В проекте должны быть тесты, которые проверяют REST API (behat или codeception);
* Проект должен проходить проверку https://github.com/squizlabs/PHP_CodeSniffer со стилем PSR2;
* Проект должен проходить проверку https://github.com/phpstan/phpstan;
* По REST API должна быть документация в формате https://swagger.io/;
* Комментарии в коде – приветствуются.
						
##### Результат				
* Ссылка на код на Github / BitBucket;
* Как плюс, ссылка на работающий пример.

## Критерии приемки

По каждому критерию можно получить только фиксированный балл, внутри одного критерия баллы не суммируются.

### C1. Deploy

| Описание  | Балл |
| --------- | ----:|
| есть README.md | 0.5 |
| использован vagrant | 0.75 |
| использован docker | 1 |
| есть docker-compose.yml | 1.5 |

### C2. Сodestyle

| Описание  | Балл |
| --------- | ----:|
| соблюден какой-либо codestyle | 0.5 |
| PSR2 | 1 |
| phpcs --standard=PSR2 не выдает ошибок | 1.75 |
| корректно настроен phpcs.xml.dist | 2 |

### C3. Phpstan

| Описание  | Балл |
| --------- | ----:|
| не исправлены ошибки phpstan level=0 | 0 |
| исправлены ошибки phpstan level=0 | 1 |
| настроен phpstan.neon. `vendor/bin/phpstan analyse -l 0 -c phpstan.neon <directories>` не показывает ошибок, где `<directories>` - папки с бизнес логикой, исправлять ошибки в `vendor`, либо в системных файлах фреймфорка не надо | 1.5 |

### C4. Composer

| Описание  | Балл |
| --------- | ----:|
| соблюден какой-либо codestyle | 0.5 |
| PSR2 | 1 |
| phpcs --standard=PSR2 не выдает ошибок | 1.75 |
| корректно настроен phpcs.xml.dist | 2 |

composer
api
нету
-1 бал
есть
+1 бал
swagger
MVC
DRY
phpcpd**
SOLID
Global variable
Неоправданный static
критерий - phpunit тест
бизнес-логика в классах ActiveRecord
-2 бала
толстый контроллер
-1 бал
Dependency Injection**
acceptance tests
есть
покрыты все endpoint
100% code coverage
vendor/bin/codecept run --coverage --coverage-xml --coverage-html --no-ansi --no-colors
unit tests
нету вообще никаких
-0.5 балов
codeception unit
phpunit
+1
phpunit.xml.dist
unit тесты реально unit

## Список литературы
* https://docs.docker.com/get-started/
* https://docs.docker.com/compose/
* https://www.php-fig.org/psr/
* https://github.com/squizlabs/PHP_CodeSniffer/wiki
* https://github.com/phpstan/phpstan
* https://getcomposer.org/doc/00-intro.md
* https://swagger.io/docs/
* https://codeception.com/quickstart
* https://github.com/sebastianbergmann/phpcpd
* https://phpunit.de/documentation.html
* https://refactoring.guru/ru
* Стив Макконнелл. Совершенный код.
* https://ru.wikipedia.org/wiki/Design_Patterns
* http://wiki.c2.com/?GlobalVariablesAreBad
