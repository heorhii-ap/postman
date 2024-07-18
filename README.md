### Коллекция запросов для тестирования API Яндекс Прилавок

[Добавление продуктов в набор](https://www.postman.com/forweb/workspace/lavka/collection/34470293-43a0352a-462a-446f-ad79-50a57974f293?action=share&creator=34470293&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5) `POST /api/v1/kits/id/products`

---

| №   | Описание проверки                                                                                                                                              | Ожидаемый результат | Статус | Ссылки на баг-репорты                                     |
|:---:|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|:------:|:---------------------------------------------------------:|
| 1   | [Добавить продукты в существующий набор](https://www.postman.com/forweb/workspace/lavka/request/34470293-fe784084-0c06-414a-b4be-b25ca66d6696)                 | 200 ОК              | PASSED |                                                           |
| 2   | [Добавить продукты в несуществующий набор](https://www.postman.com/forweb/workspace/lavka/request/34470293-44a855d7-4b88-48a2-9cf5-b409f533ea35)               | 404 Not found       | PASSED |                                                           |
| 3   | [Передать productsList без массива в существующий набор](https://www.postman.com/forweb/workspace/lavka/request/34470293-2223f468-2c0a-4bce-8f34-e15160df49bb) | 400 Bad Request     | FAILED | [BUG-8](https://heorhii-ap.youtrack.cloud/issue/BUG-8)    |
| 4   | [Отправить запрос с пустым JSON-ом](https://www.postman.com/forweb/workspace/lavka/request/34470293-4bd8bd7e-e6a1-40fb-be6e-b0abec46f5fa)                      | 400 Bad Request     | FAILED | [BUG-9](https://heorhii-ap.youtrack.cloud/issue/BUG-9)    |
| 5   | [Добавить в набор продукт с id=50](https://www.postman.com/forweb/workspace/lavka/request/34470293-4a4deb60-b4b9-4ecf-bc91-ce85de34135a)                       | 200 ОК              | PASSED |                                                           |
| 6   | [Добавить в набор продукт с несуществующим id](https://www.postman.com/forweb/workspace/lavka/request/34470293-9f287045-d859-4a61-b893-1044c0a635d6)           | 400 Bad Request     | FAILED | [BUG-10](https://heorhii-ap.youtrack.cloud/issue/BUG-10)  |
| 7   | [Добавить в набор продукт с id = A](https://www.postman.com/forweb/workspace/lavka/request/34470293-6aecd383-8f82-4a9b-a427-f73764db65ad)                      | 400 Bad Request     | PASSED |                                                           |
| 8   | [Добавить в набор продукт с id = @](https://www.postman.com/forweb/workspace/lavka/request/34470293-cf63d202-8628-4398-8e25-b56c46cda4b7)                      | 400 Bad Request     | PASSED |                                                           |
| 9   | [Передать пробел в id продукта](https://www.postman.com/forweb/workspace/lavka/request/34470293-21fc245e-a633-4514-b8cc-df30c3127eda)                          | 400 Bad Request     | FAILED | [BUG-11](https://heorhii-ap.youtrack.cloud/issue/BUG-11)  |
| 10  | [Отсутствие параметра id продукта в теле запроса](https://www.postman.com/forweb/workspace/lavka/request/34470293-a66448c5-bf5a-4cad-971a-f1da3208185a)        | 400 Bad Request     | FAILED | [BUG-12](https://heorhii-ap.youtrack.cloud/issue/BUG-12)  |
| 11  | [Добавить в набор продукт с quantity=10](https://www.postman.com/forweb/workspace/lavka/request/34470293-62993dbb-0b49-4e92-8399-3bc38e94acc8)                 | 200 ОК              | PASSED |                                                           |
| 12  | [Добавить в набор продукт с quantity=100500](https://www.postman.com/forweb/workspace/lavka/request/34470293-811c99a8-9688-4708-a10c-4dc1d4a0cb9a)             | 200 ОК              | PASSED |                                                           |
| 13  | [Отправить запрос с quantity = 0](https://www.postman.com/forweb/workspace/lavka/request/34470293-6d624997-915c-4502-94f3-5c5f6b39881b)                        | 400 Bad Request     | FAILED | [BUG-13](https://heorhii-ap.youtrack.cloud/issue/BUG-13)  |
| 14  | [Отправить запрос с quantity = A](https://www.postman.com/forweb/workspace/lavka/request/34470293-d77ed467-de40-49d1-9d9c-393e7a3bf6b7)                        | 400 Bad Request     | PASSED |                                                           |
| 15  | [Отправить запрос с quantity = @](https://www.postman.com/forweb/workspace/lavka/request/34470293-0ba6583e-cee2-404f-8b8b-668a98a48916)                        | 400 Bad Request     | PASSED |                                                           |
| 16  | [Передать пробел в quantity продукта](https://www.postman.com/forweb/workspace/lavka/request/34470293-404cbebf-444c-45f6-9822-6f9a6d1f4bbb)                    | 400 Bad Request     | FAILED | [BUG-14](https://heorhii-ap.youtrack.cloud/issue/BUG-14)  |
| 17  | [Отсутствие параметра quantity продукта в теле запроса](https://www.postman.com/forweb/workspace/lavka/request/34470293-c4a8bf67-2070-4190-8247-ab3dc05c92b6)  | 400 Bad Request     | FAILED | [BUG-15](https://heorhii-ap.youtrack.cloud/issue/BUG-15)  |








