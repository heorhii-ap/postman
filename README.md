> [!TIP]
> Чек-лист на API Яндекс Прилавок и результаты выполнения тестов.

[Добавление продуктов в набор](https://www.postman.com/forweb/workspace/lavka/collection/34470293-43a0352a-462a-446f-ad79-50a57974f293?action=share&creator=34470293&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5) `POST /api/v1/kits/id/products`

<details><summary>id набора в URL и productsList</summary><br>

| № | Описание проверки                                      | ОР                                  | Статус | Ссылка на баг-репорт |
|:-:|--------------------------------------------------------|-------------------------------------|:------:|:--------------------:|
| 1 | [Добавить продукты в существующий набор](https://www.postman.com/forweb/workspace/lavka/request/34470293-fe784084-0c06-414a-b4be-b25ca66d6696?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5)             | Код и статус ответа 200 ОК          | PASSED |                      |
|   |                                                        | Ошибок в структуре ответа нет       | PASSED |                      |
|   |                                                        | Продукты в набор добавлены          | PASSED |                      |
|   |                                                        | Появилась запись в БД               | PASSED |                      |
| 2 | [Добавить продукты в несуществующий набор](https://www.postman.com/forweb/workspace/lavka/request/34470293-44a855d7-4b88-48a2-9cf5-b409f533ea35?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5)               | Код и статус ответа 404 Not found   | PASSED |                      |
| 3 | Передать productsList без массива в существующий набор | Код и статус ответа 400 Bad Request | FAILED | [BUG-8](https://heorhii-ap.youtrack.cloud/issue/BUG-8)           |
| 4 | Отправить запрос с пустым JSON-ом                      | Код и статус ответа 400 Bad Request | FAILED | [BUG-9](https://heorhii-ap.youtrack.cloud/issue/BUG-9)           |

---
