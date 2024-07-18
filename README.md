### Коллекция запросов для тестирования API Яндекс Прилавок

[Добавление продуктов в набор](https://www.postman.com/forweb/workspace/lavka/collection/34470293-43a0352a-462a-446f-ad79-50a57974f293?action=share&creator=34470293&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5) `POST /api/v1/kits/id/products`

| №   | Описание проверки                                                                                                                                                                                                                                               |
|:---:|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | [Добавить продукты в существующий набор](https://www.postman.com/forweb/workspace/lavka/request/34470293-fe784084-0c06-414a-b4be-b25ca66d6696?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5) |
| 2   |
| 3   |
| 4   |
| 5   |
| 6   |
| 7   |
| 8   |
| 9   |
| 10  |


<details><summary>id набора в URL и productsList</summary><br>

| № | Описание проверки                                      | Ожидаемый результат                                  | Статус | Ссылки на баг-репорты |
|:-:|--------------------------------------------------------|-------------------------------------|:------:|:--------------------:|
| 1 | [Добавить продукты в существующий набор](https://www.postman.com/forweb/workspace/lavka/request/34470293-fe784084-0c06-414a-b4be-b25ca66d6696?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5)             | Код и статус ответа 200 ОК          | PASSED |                      |
|   |                                                        | Ошибок в структуре ответа нет       | PASSED |                      |
|   |                                                        | Продукты в набор добавлены          | PASSED |                      |
|   |                                                        | Появилась запись в БД               | PASSED |                      |
| 2 | [Добавить продукты в несуществующий набор](https://www.postman.com/forweb/workspace/lavka/request/34470293-44a855d7-4b88-48a2-9cf5-b409f533ea35?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5)               | Код и статус ответа 404 Not found   | PASSED |                      |
| 3 | [Передать productsList без массива в существующий набор](https://www.postman.com/forweb/workspace/lavka/request/34470293-2223f468-2c0a-4bce-8f34-e15160df49bb?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5) | Код и статус ответа 400 Bad Request | FAILED | [BUG-8](https://heorhii-ap.youtrack.cloud/issue/BUG-8)           |
| 4 | [Отправить запрос с пустым JSON-ом](https://www.postman.com/forweb/workspace/lavka/request/34470293-4bd8bd7e-e6a1-40fb-be6e-b0abec46f5fa?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5)                      | Код и статус ответа 400 Bad Request | FAILED | [BUG-9](https://heorhii-ap.youtrack.cloud/issue/BUG-9)           |

---

</details>

<details><summary>id продукта в теле запроса</summary><br>

| №  | Описание проверки                               |  Ожидаемый результат                | Статус  | Ссылка на баг-репорт |
|:--:|-------------------------------------------------|-------------------------------------|:-------:|:--------------------:|
| 5  | [Добавить в набор продукт с id=50](https://www.postman.com/forweb/workspace/lavka/request/34470293-4a4deb60-b4b9-4ecf-bc91-ce85de34135a?tab=body)                | Код и статус ответа 200 ОК          | PASSED  |                      |
|    |                                                 | Ошибок в структуре ответа нет       | PASSED  |                      |
|    |                                                 | Продукты в набор добавлены          | PASSED  |                      |
|    |                                                 | Появилась запись в БД               | PASSED  |                      |
| 6  | [Добавить в набор продукт с несуществующим id](https://www.postman.com/forweb/workspace/lavka/request/34470293-9f287045-d859-4a61-b893-1044c0a635d6?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5)    | Код и статус ответа 400 Bad Request | FAILED  | [BUG-10](https://heorhii-ap.youtrack.cloud/issue/BUG-10/Kod-200-OK-pri-otpravke-POST-zaprosa-api-v1-kits-id-products-na-dobavlenie-produktov-s-nesushestvuyushim-id-v-nabor)    |
| 7  | [Добавить в набор продукт с id = A](https://www.postman.com/forweb/workspace/lavka/request/34470293-6aecd383-8f82-4a9b-a427-f73764db65ad?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5)               | Код и статус ответа 400 Bad Request | PASSED  |                      |
| 8  | [Добавить в набор продукт с id = @](https://www.postman.com/forweb/workspace/lavka/request/34470293-cf63d202-8628-4398-8e25-b56c46cda4b7?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5)              | Код и статус ответа 400 Bad Request | PASSED  |                      |
| 9  | [Передать пробел в id продукта](https://www.postman.com/forweb/workspace/lavka/request/34470293-21fc245e-a633-4514-b8cc-df30c3127eda?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5)                   | Код и статус ответа 400 Bad Request | FAILED  | [BUG-11](https://heorhii-ap.youtrack.cloud/issue/BUG-11/Oshibka-500-pri-otpravke-POST-zaprosa-api-v1-kits-id-products-na-dobavlenie-produktov-v-nabor-s-probelom-v-id-produkta)    |
| 10 | [Отсутствие параметра id продукта в теле запроса](https://www.postman.com/forweb/workspace/lavka/request/34470293-a66448c5-bf5a-4cad-971a-f1da3208185a?action=share&creator=34470293&ctx=documentation&active-environment=34470293-0f725035-fc11-4334-81d0-6ce0972fbef5) | Код и статус ответа 400 Bad Request | FAILED  | [BUG-12](https://heorhii-ap.youtrack.cloud/issue/BUG-12/Kod-200-OK-pri-otpravke-POST-zaprosa-api-v1-kits-id-products-na-dobavlenie-produktov-v-nabor-bez-parametra-id-produkta)    |

---
  
</details>
