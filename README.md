### Коллекция запросов для тестирования API Яндекс Прилавок

---

[Добавление продуктов в набор](https://www.postman.com/forweb/workspace/lavka/collection/34470293-43a0352a-462a-446f-ad79-50a57974f293) `POST /api/v1/kits/id/products`

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
| 18  | [Добавить в пустой набор 1 продукт](https://www.postman.com/forweb/workspace/lavka/request/34470293-e85e38ec-230a-4482-8a67-0a8c171b19ac)                      | 200 ОК              | PASSED |                                                           |
| 19  | [Добавить в пустой набор 2 продукта](https://www.postman.com/forweb/workspace/lavka/request/34470293-8be17f0d-3b1a-4220-acda-a460247c5585)                     | 200 ОК              | PASSED |                                                           |
| 20  | [Добавить в пустой набор 15 продуктов](https://www.postman.com/forweb/workspace/lavka/request/34470293-497a254c-8187-4940-ab43-745ffbaa8022)                   | 200 ОК              | PASSED |                                                           |
| 21  | [Добавить в пустой набор 29 продуктов](https://www.postman.com/forweb/workspace/lavka/request/34470293-27fcc352-bfdd-404f-927e-4eeba75952d7)                   | 200 ОК              | PASSED |                                                           |
| 22  | [Добавить в пустой набор 30 продуктов](https://www.postman.com/forweb/workspace/lavka/request/34470293-65d6ff1f-ace0-4f18-b09a-926445d3b256)                   | 200 ОК              | PASSED |                                                           |
| 23  | [Добавить в пустой набор 31 продукт](https://www.postman.com/forweb/workspace/lavka/request/34470293-94ea7414-244c-43b6-baa8-d6ca0dee4dc0)                     | 400 Bad Request     | PASSED |                                                           |
| 24  | [Добавить в пустой набор 105 продуктов](https://www.postman.com/forweb/workspace/lavka/request/34470293-d9a6acc5-448b-4957-a3b2-e0328e0715f7)                  | 400 Bad Request     | PASSED |                                                           |

---

[Курьерская служба «Привезём быстро»](https://www.postman.com/forweb/workspace/lavka/collection/34470293-2639eb85-a518-4f07-a05c-d891af007682) `POST /fast-delivery/v3.1.1/calculate-delivery.xml`

---

| №   | Описание проверки                                                                                                                                              | Ожидаемый результат | Статус | Ссылки на баг-репорты                                     |
|:---:|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|:------:|:---------------------------------------------------------:|
| 25  | [Возможность доставки в 15 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-237e0fab-9c7c-43b3-b391-ed9a234fba95)                        | 200 ОК              | PASSED |                                                           |
| 26  | [Возможность доставки в 7 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-8d04cf5e-e57d-4858-8e01-6167c1758b77)                         | 200 ОК              | PASSED |                                                           |
| 27  | [Возможность доставки в 07 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-6e47f12c-c47b-4674-9aa3-c6b9ace0f20d)                        | 200 ОК              | PASSED |                                                           |
| 28  | [Возможность доставки в 8 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-74b24edf-9208-4c03-814c-24ffd385bdf4)                         | 200 ОК              | PASSED |                                                           |
| 29  | [Возможность доставки в 08 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-3447549f-e157-4845-a6f8-d0b35a7b45d2)                        | 200 ОК              | PASSED |                                                           |
| 30  | [Возможность доставки в 20 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-19dca10c-f40a-4f1e-a3bc-9b234c2a60bf)                        | 200 ОК              | PASSED |                                                           |
| 31  | [Возможность доставки в 21 час](https://www.postman.com/forweb/workspace/lavka/request/34470293-a1c29b29-7b34-4501-b302-ab90b62ee434)                          | 200 ОК              | PASSED |                                                           |
| 32  | [Возможность доставки в 0 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-d1b17e8e-5263-4871-a674-430cb7b21038)                         | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 33  | [Возможность доставки в 00 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-a0a26588-113f-441d-af6e-ff2b3dfd0a5e)                        | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 34  | [Возможность доставки в 1 час](https://www.postman.com/forweb/workspace/lavka/request/34470293-a052d679-aac1-4f92-801b-bfc385e2ada8)                           | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 35  | [Возможность доставки в 01 час](https://www.postman.com/forweb/workspace/lavka/request/34470293-ff4e546b-4494-40e2-90c1-868fbc459bde)                          | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 36  | [Возможность доставки в 5 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-75caf522-cfca-45d1-b327-9b5596a6af2e)                         | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 37  | [Возможность доставки в 05 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-b4c2580c-b33c-42bd-b8cc-6e922eafd15d)                        | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 38  | [Возможность доставки в 6 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-ab014d3c-3f6d-4a8f-a9f4-2d2f3230898d)                         | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 39  | [Возможность доставки в 06 часов](https://www.postman.com/forweb/workspace/lavka/request/34470293-b12ee82b-9363-4289-add1-a3595418cb3f)                        | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 40  | [Возможность доставки в 22 часа](https://www.postman.com/forweb/workspace/lavka/request/34470293-e6dd7f99-f290-461a-b5b5-cd3cd059ae27)                         | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 41  | [Возможность доставки в 23 часа](https://www.postman.com/forweb/workspace/lavka/request/34470293-7beba713-c4c3-4827-adf7-f06cde095c29)                         | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 42  | [Возможность доставки в 24 часа](https://www.postman.com/forweb/workspace/lavka/request/34470293-301c53e0-f796-484b-a459-5ac9dcb0423d)                         | 200 ОК              | FAILED | [BUG-16](https://heorhii-ap.youtrack.cloud/issue/BUG-16)  |
| 42  | [Отправить запрос с deliveryTime=242](https://www.postman.com/forweb/workspace/lavka/request/34470293-21dd1b2b-122b-43e3-b11f-2b4c13176833)                    | 400 Bad Request     | FAILED | [BUG-17](https://heorhii-ap.youtrack.cloud/issue/BUG-17)  |
| 42  | [Отправить запрос с deliveryTime=Aa](https://www.postman.com/forweb/workspace/lavka/request/34470293-f5780c4f-dd50-4bc2-a9a6-29fa7b53f1fa)                     | 400 Bad Request     | FAILED | [BUG-18](https://heorhii-ap.youtrack.cloud/issue/BUG-18)  |






