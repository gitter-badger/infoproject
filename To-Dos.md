- [x] Создать проект
- [ ] Создать домашнюю страницу
 - [ ] Простое окно с полем для ввода
    - [ ] Добавить instant search с помощью AJAX (опционально)
- [ ] Создать страницу с результатами выдачи
- [ ] Реализовать поиск по текстовому файлу с Анной Карениной (или другим, просто для тестирования функционала)
- [ ] Реализовать сжатие индекса
- [ ] Реализовать нормализацию (требуется обсуждение возможных способов)
  - [ ] \(?\) Дать пользователю возможность выбирать способ нормализации

Извлечение текстов:
- [ ] С использование API, предоставленного создателями:
  - [ ] Реализовать извлечение текста для Reddit (предоставляют API)
  - [ ] Реализовать извлечение текста для HackerNews (предоставля)
- [ ] Реализовать извлечение текста для Habrahabr (писать парсер html-страницы?)
- [ ] Добавить проверку того, что статью по урлу находится в индексе
  - [ ] Добавить возможность добавлять статью в индекс (для этого желательно использовать какой-нибудь RPC-механизм. Возможно, стоит посмотреть на это http://zerorpc.dotcloud.com/ )



Начинка поисковика:
- [ ] Обработка и расширение запроса
 - [ ] Парсер запроса
   - [ ] Отбрасывать или учитывать стоп-слова (когда одно, а когда другое?) + собрать список стоп-слов по нашей тематике
   - [ ] Нормализация (где-то лемматизация, а где-то стеммер. Подумать, когда что лучше. Возможно стеммер не подходит - лекция 3, стр 39). Можно использовать [PyMystem](https://github.com/Digsolab/pymystem3) в качестве лемматизатора.
   - [ ] Синонимы (кластеризация + готовый файл с синонимами использовать (эффективно ли?))
   - [ ] Исправление опечаток (каким образом?)
   - [ ] Определение языка (Если поймем, что с запросами на разных языках надо работать по-разному. Посмотреть вот это: [CLD](http://code.google.com/p/chromium-compact-language-detector/))
   - [ ] Снятие многозначности (Языковая модель)
   - [ ] \(?\) Использовать коллокации
   - [ ] Расширять запрос при необходимости (см. слайд 66, лекция 8 )
- [ ] Обратный индекс по документам (архитектура обратного индекса как на слайде 17 лекции 7. Только нужно добавить каждому термину idf и решить, нужны ли позиции)
  - [ ] \(?\) Сжатие индекса (Simple9, VarByte)
  - [ ] 
- [ ] Булев поиск
  - [ ] Оптимизация построения результата
- [ ] Ранжирование результатов (tf-idf)
- [ ] Веб-интерфейс
- [ ] Продумать методы оценки качества
- [ ] \(?\) Поиск дубликатов (актуально ли в нашем случае?)
