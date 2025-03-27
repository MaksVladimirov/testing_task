# testing_task
Бригада: Владимиров М.П., Лаптев А.И., Толкачев Р.Д.
Написание тест кейсов на примере магазина электроники DNS
# Функциональные требования

## 1. Авторизация и регистрация

- Система должна позволять пользователю регистрироваться, используя уникальный email и пароль.
- После успешной регистрации система должна отправить email с подтверждением для активации учетной записи.
- Пользователь должен иметь возможность восстановить пароль, получив ссылку на email для создания нового пароля.
- Вход в систему должен быть возможен через корректные учетные данные (email и пароль).
- Система должна показывать сообщение об ошибке при вводе неправильных учетных данных (неверный email или пароль).

## 2. Корзина

- Пользователь должен иметь возможность добавлять товары в корзину, изменять их количество и удалять.
- Система должна обновлять общую стоимость корзины при изменении количества товаров.
- Пользователь должен иметь возможность оформить заказ, указав контактные данные и способ доставки.
- После оформления заказа система должна отображать подтверждение и добавить заказ в историю.

## 3. Оформление заказа

- На этапе оформления заказа пользователь должен вводить свои контактные данные (ФИО, телефон, email).
- Система должна предоставить выбор способа доставки и оплаты.
- Система должна подтверждать успешную оплату и отображать номер заказа.

## 4. Отзывы и рейтинги

- Пользователь должен иметь возможность добавлять отзыв и рейтинг товара.
- Система должна проводить модерацию отзывов, фильтруя неподобающие или запрещенные слова.
- Должна быть возможность фильтровать товары по рейтингу.

## 5. Поиск и фильтрация товаров

- Пользователь должен иметь возможность искать товары по ключевому слову.
- Система должна показывать товары по выбранной категории или фильтру по цене.
- Должна быть возможность сортировки товаров по популярности.

## 6. Личный кабинет

- Пользователь должен иметь возможность обновить свои личные данные (имя, телефон, email).
- Система должна позволять пользователю изменить пароль и просматривать историю заказов.
- Должна быть возможность повторно заказать товары из истории заказов.

## 7. Оповещения и уведомления

- Система должна отправлять email-уведомления о статусе заказа.
- Должны приходить push-уведомления о статусе заказа и скидках.

## 8. Оплата и возвраты

- Система должна поддерживать оплату картой, через электронный кошелек, а также оплату при получении.
- Должен быть предусмотрен механизм возврата товаров с возвратом средств.

## 9. Поддержка и обратная связь

- Пользователь должен иметь возможность отправить сообщение в поддержку, задать вопросы через онлайн-чат или запросить обратный звонок.
- Система должна фиксировать обратную связь от пользователей и оценку работы оператора.

## 10. Безопасность и авторизация через соцсети

- Система должна поддерживать вход через Google, Facebook, и Apple ID.
- При множественных неудачных попытках входа система должна блокировать учетную запись и требовать подтверждения через капчу или сброс пароля.
- Должна быть возможность выхода из аккаунта с требованием повторной авторизации.

## 1. Авторизация и регистрация

### Описание: Проверка входа, регистрации и восстановления пароля

| #  | Тест-кейс                      | Шаги выполнения | Ожидаемый результат | Статус |
|----|--------------------------------|----------------|---------------------|--------|
| 1  | Регистрация нового пользователя | 1. Открыть главную страницу сайта. 2. Нажать "Регистрация". 3. Ввести email, пароль и подтвердить пароль. 4. Согласиться с условиями. 5. Нажать "Зарегистрироваться". 6. Проверить получение письма с подтверждением. 7. Перейти по ссылке из письма. | Успешная регистрация и автоматический вход. | Выполнено. Test case пройден. |
| 2  | Вход с верными учетными данными | 1. Перейти на страницу входа. 2. Ввести корректный email и пароль. 3. Нажать "Войти". | Успешная авторизация, редирект в личный кабинет. | Выполнено. Test case пройден. |
| 3  | Вход с неверными данными | 1. Перейти на страницу входа. 2. Ввести несуществующий email или неправильный пароль. 3. Нажать "Войти". | Появляется ошибка "Неверный email или пароль". | Выполнено. Test case пройден. |
| 4  | Восстановление пароля | 1. На странице входа нажать "Забыли пароль?". 2. Ввести email. 3. Нажать "Отправить инструкцию". 4. Проверить почтовый ящик. 5. Перейти по ссылке из письма и задать новый пароль. 6. Ввести новый пароль и подтвердить. | Отображается сообщение "Пароль успешно изменен", можно войти с новым паролем. | Выполнено. Test case пройден. |

## 2. Корзина

### Описание: Проверка добавления, удаления и управления товарами в корзине

| #  | Тест-кейс                      | Шаги выполнения | Ожидаемый результат | Статус |
|----|--------------------------------|----------------|---------------------|--------|
| 1  | Добавление товара в корзину | 1. Открыть страницу товара. 2. Нажать "Добавить в корзину". 3. Открыть корзину. | Товар появляется в корзине, отображается его название, цена и количество. | Выполнено. Test case пройден. |
| 2  | Изменение количества товаров в корзине | 1. Добавить товар в корзину. 2. Перейти в корзину. 3. Увеличить количество товара (например, до 3 штук). 4. Проверить обновление общей стоимости. | Количество товара изменено, цена пересчитана. | Выполнено. Test case пройден. |
| 3  | Удаление товара из корзины | 1. Добавить товар в корзину. 2. Перейти в корзину. 3. Нажать "Удалить" рядом с товаром. | Товар удален из корзины, отображается сообщение "Корзина пуста". | Выполнено. Test case пройден. |
| 4  | Оформление заказа | 1. Добавить товар в корзину. 2. Перейти в корзину. 3. Нажать "Оформить заказ". 4. Ввести контактные данные, выбрать доставку и оплату. 5. Нажать "Подтвердить заказ". | Отображается сообщение "Заказ успешно оформлен", заказ появляется в истории заказов. | Выполнено. Test case пройден. |

## 3. Оформление заказа

### Описание: Проверка корректности процесса оформления заказа

| #  | Тест-кейс                      | Шаги выполнения | Ожидаемый результат | Статус |
|----|--------------------------------|----------------|---------------------|--------|
| 1  | Заполнение данных покупателя | 1. Перейти на страницу оформления заказа. 2. Ввести ФИО, телефон, email. 3. Выбрать тип доставки. 4. Нажать "Продолжить". | Данные корректно сохраняются, переход на следующий этап оформления. | Выполнено. Test case пройден. |
| 2  | Выбор способа доставки | 1. На странице оформления выбрать "Курьерская доставка". 2. Ввести адрес. 3. Указать удобное время доставки. 4. Нажать "Продолжить". | Данные сохранены, стоимость доставки пересчитана. | Выполнено. Test case пройден. |
| 3  | Выбор способа оплаты | 1. На этапе оплаты выбрать "Оплата картой". 2. Ввести данные карты (номер, срок действия, CVV). 3. Подтвердить платеж. | Оплата проходит успешно, заказ переходит в статус "Оплачен". | Выполнено. Test case пройден. |
| 4  | Подтверждение заказа | 1. Проверить детали заказа. 2. Нажать "Подтвердить заказ". | Заказ оформлен, появляется страница с подтверждением и номером заказа. | Выполнено. Test case пройден. |

## 4. Проверка отзывов и рейтингов

### Описание: Тестирование функционала отзывов

| #  | Тест-кейс                      | Шаги выполнения | Ожидаемый результат | Статус |
|----|--------------------------------|----------------|---------------------|--------|
| 1  | Добавление отзыва | 1. Открыть карточку товара. 2. Пролистать вниз до блока "Отзывы". 3. Написать текст отзыва, добавить фото. 4. Нажать "Отправить". | Отзыв отображается после модерации. | Выполнено. Test case пройден. |
| 2  | Добавление рейтинга | 1. Перейти на страницу товара. 2. Поставить оценку (1-5 звезд). 3. Нажать "Отправить". | Рейтинг товара обновляется. | Выполнено. Test case пройден. |
| 3  | Проверка модерации отзывов | 1. Написать отзыв с запрещенными словами. 2. Нажать "Отправить". | Отзыв не публикуется, отображается ошибка "Отзыв не соответствует правилам". | Выполнено. Test case пройден. |
| 4  | Фильтрация по рейтингу | 1. Открыть страницу "Каталог". 2. Выбрать фильтр "Только с рейтингом 4+ звезды". 3. Проверить выдачу. | Показываются товары только с высоким рейтингом. | Выполнено. Test case пройден. |

## 5. Поиск и фильтрация товаров
**Описание:** Проверка работы поиска и фильтров на сайте

| # | Тест-кейс | Шаги выполнения | Ожидаемый результат | Статус |
|---|-----------|----------------|----------------------|--------|
| 1 | Поиск товара по ключевому слову | 1. Ввести название товара в строку поиска. 2. Нажать "Поиск". | В результатах поиска отображаются соответствующие товары. | Выполнено. Test case пройден.  |
| 2 | Поиск несуществующего товара | 1. Ввести несуществующее название товара. 2. Нажать "Поиск". | Отображается сообщение "Товар не найден". | Выполнено. Test case пройден.  |
| 3 | Фильтрация по категории | 1. Открыть каталог. 2. Выбрать категорию товаров. | Отображаются только товары выбранной категории. | Выполнено. Test case пройден.  |
| 4 | Фильтрация по цене | 1. Установить диапазон цен (например, 1000 - 5000 рублей). 2. Нажать "Применить". | Отображаются только товары в заданном диапазоне цен. | Выполнено. Test case пройден.  |
| 5 | Сортировка по популярности | 1. Открыть каталог. 2. Выбрать сортировку "Популярные". | В верхних позициях отображаются популярные товары. | Выполнено. Test case пройден.  |

## 6. Личный кабинет
**Описание:** Проверка функционала личного кабинета пользователя

| # | Тест-кейс | Шаги выполнения | Ожидаемый результат | Статус |
|---|-----------|----------------|----------------------|--------|
| 1 | Обновление личных данных | 1. Перейти в личный кабинет. 2. Изменить имя, телефон или email. 3. Нажать "Сохранить". | Данные успешно обновлены. | Выполнено. Test case пройден.  |
| 2 | Изменение пароля | 1. Перейти в настройки аккаунта. 2. Ввести старый пароль. 3. Ввести новый пароль и подтвердить. 4. Нажать "Сохранить". | Пароль изменен, можно войти с новым паролем. | Выполнено. Test case пройден.  |
| 3 | Просмотр истории заказов | 1. Перейти в раздел "Мои заказы". | Отображается список оформленных заказов. | Выполнено. Test case пройден.  |
| 4 | Повторный заказ | 1. В разделе "Мои заказы" выбрать заказ. 2. Нажать "Повторить заказ". | Товары добавляются в корзину. | Выполнено. Test case пройден.  |

## 7. Оповещения и уведомления
**Описание:** Проверка работы уведомлений для пользователя

| # | Тест-кейс | Шаги выполнения | Ожидаемый результат | Статус |
|---|-----------|----------------|----------------------|--------|
| 1 | Получение email-уведомления о заказе | 1. Оформить заказ. 2. Проверить почтовый ящик. | Приходит письмо с подтверждением заказа. | Выполнено. Test case пройден.  |
| 2 | Push-уведомление о статусе заказа | 1. Оформить заказ. 2. Дождаться изменения статуса. | Приходит push-уведомление о смене статуса. | Выполнено. Test case пройден.  |
| 3 | Уведомление о скидках и акциях | 1. Подписаться на рассылку. 2. Дождаться нового промо-предложения. | Приходит уведомление о скидках. | Выполнено. Test case пройден.  |

## 8. Оплата и возвраты
Описание: Проверка различных способов оплаты и процесса возврата средств

| #  | Тест-кейс                      | Шаги выполнения                                                                 | Ожидаемый результат                                       | Статус     |
|----|---------------------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------|------------|
| 1  | Оплата картой                   | 1. Добавить товар в корзину. <br> 2. Перейти к оформлению заказа. <br> 3. Выбрать "Оплата картой". <br> 4. Ввести данные карты. <br> 5. Подтвердить платеж. | Заказ оплачен, статус изменяется на "Оплачен".             | Выполнено. Test case пройден.|
| 2  | Оплата через электронный кошелек| 1. Выбрать способ оплаты "Электронный кошелек". <br> 2. Авторизоваться в платежной системе. <br> 3. Подтвердить оплату. | Заказ успешно оплачен.                                      | Выполнено. Test case пройден.|
| 3  | Оплата при получении            | 1. Выбрать "Оплата при получении". <br> 2. Оформить заказ. <br> 3. Получить товар и оплатить при доставке. | Оплата фиксируется в системе.                             | Выполнено. Test case пройден.|
| 4  | Возврат товара                  | 1. Перейти в раздел "Мои заказы". <br> 2. Выбрать заказ. <br> 3. Нажать "Оформить возврат". <br> 4. Заполнить форму возврата. <br> 5. Подтвердить возврат. | Возврат оформлен, средства возвращены.                   | Выполнено. Test case пройден.|
| 5  | Отмена заказа                   | 1. Перейти в "Мои заказы". <br> 2. Выбрать активный заказ. <br> 3. Нажать "Отменить заказ". | Заказ отменен, средства возвращены (если были оплачены).   | Выполнено. Test case пройден.|

## 9. Поддержка и обратная связь
Описание: Проверка работы службы поддержки и системы обратной связи

| #  | Тест-кейс                      | Шаги выполнения                                                                 | Ожидаемый результат                                       | Статус     |
|----|---------------------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------|------------|
| 1  | Отправка сообщения в поддержку  | 1. Перейти в раздел "Поддержка". <br> 2. Написать сообщение. <br> 3. Нажать "Отправить". | Приходит уведомление о принятии обращения.                | Выполнено. Test case пройден.|
| 2  | Онлайн-чат с оператором         | 1. Открыть онлайн-чат. <br> 2. Написать сообщение. <br> 3. Дождаться ответа оператора. | Оператор отвечает в течение указанного времени.           | Выполнено. Test case пройден.|
| 3  | Запрос обратного звонка         | 1. Открыть "Обратный звонок". <br> 2. Ввести телефон. <br> 3. Подтвердить заявку. | В течение указанного времени поступает звонок.           | Выполнено. Test case пройден.|
| 4  | Оценка работы поддержки         | 1. Завершить чат с оператором. <br> 2. Оценить качество ответа.                | Оценка зафиксирована в системе.                           | Выполнено. Test case пройден.|

## 10. Безопасность и авторизация через соцсети
Описание: Проверка безопасности учетной записи и входа через соцсети

| #  | Тест-кейс                      | Шаги выполнения                                                                 | Ожидаемый результат                                       | Статус     |
|----|---------------------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------|------------|
| 1  | Вход через Google               | 1. Нажать "Войти через Google". <br> 2. Выбрать аккаунт Google. <br> 3. Подтвердить вход. | Успешный вход через Google.                               | Выполнено. Test case пройден.|
| 2  | Вход через Facebook             | 1. Нажать "Войти через Facebook". <br> 2. Ввести учетные данные Facebook. <br> 3. Подтвердить вход. | Успешный вход через Facebook.                             | Выполнено. Test case пройден.|
| 3  | Вход через Apple ID             | 1. Нажать "Войти через Apple". <br> 2. Ввести данные Apple ID. <br> 3. Подтвердить вход. | Успешный вход через Apple.                                | Выполнено. Test case пройден.|
| 4  | Блокировка аккаунта при множественных неверных попытках входа | 1. Ввести неправильный пароль 5 раз.                                            | Аккаунт временно заблокирован, требуется капча или сброс пароля. | Выполнено. Test case пройден.|
| 5  | Проверка выхода из аккаунта     | 1. Авторизоваться. <br> 2. Нажать "Выйти".                                      | Система выходит из аккаунта, требуется повторная авторизация. | Выполнено. Test case пройден.|


