# Лабораторная работа №1

Тема: Формулирование требований к программной системе. Описание ВКР https://aibazar.vercel.app/


Цель работы: Научиться анализировать поставленную задачу, формулировать функциональные и нефункциональные требования к проектируемой системе.

---

## 1. Перечень заинтересованных лиц (стейкхолдеров)

1. Пользователи: Лица, заинтересованные в использовании платформы для работы с документами и инструментами.
2. Гости (Guest): Незарегистрированные пользователи, которые могут просматривать публичные документы.
3. Администраторы (Admin): Пользователи с расширенными правами для управления системой и её участниками.
4. Разработчики: Команда, ответственная за разработку и поддержку системы.

---

## 2. Перечень функциональных требований

1. Регистрация и аутентификация:
   - Регистрация новых пользователей.
   - Аутентификация пользователей для доступа к их личным данным и инструментам.
   - Удаление учётной записи по запросу пользователя.

2. Управление документами:
   - Создание новых документов.
   - Выбор существующих документов для работы.
   - Редактирование документов.
   - Опубликовать документ.
   - Закрыть доступ к опубликованному документу.
   - Поместить документ в корзину.
   - Восстановить документ из корзины.
   - Удаление документа навсегда.
   - Просмотр корзины удалённых документов.

3. Работа с опубликованными документами:
   - Открытие опубликованных документов.
   - Написание отзывов на опубликованные статьи (документы).
   - Просмотр списка всех опубликованных документов.

4. Управление инструментами:
   - Добавление инструментов в корзину.
   - Редактирование и создание инструментов.
   - Просмотр списка доступных инструментов.
   - Добавление инструмента в избранное.

5. Управление персональными данными и настройками:
   - Просмотр и редактирование персональных данных.
   - Использование настроек для кастомизации системы.

6. Работа с пользователями и ролями:
   - Назначение ролей участникам (например, "Admin" или "User").

7. Финансовые операции:
   - Оплата услуг и инструментов.

8. Оставление обратной связи:
   - Возможность оставить отзыв о работе системы.



## 3. Диаграмма вариантов использования

Диаграмма ниже описывает различные взаимодействия пользователей с системой. В центре находится пользователь, который имеет доступ к широкому спектру функций, включая аутентификацию, создание и редактирование документов, добавление инструментов в избранное, а также управление настройками и оплатой услуг. Пользователь может взаимодействовать с документами, например, публиковать или восстанавливать их, оставлять отзывы и обратную связь.
Гость имеет ограниченные возможности, такие как просмотр инструментов и документов, а также оплата услуг. Администратор, в свою очередь, обладает более широкими правами, включая управление ролями пользователей, редактирование и удаление документов, а также закрытие доступа к ним. Все эти взаимодействия связываются друг с другом через роли и функции, предоставляемые системой для каждого типа пользователя. Подробнее смотреть https://miro.com/app/board/uXjVLRTT9W4=/
![](./images/1.jpg)

## Диаграммы последовательностей
Диаграмма последовательностей на рисунке описывает процесс оплаты AI-инструмента. Пользователь выбирает инструмент, затем способ оплаты и вводит данные для оплаты на странице платёжной системы. Система проверяет корректность введённых данных, и если оплата прошла успешно, пользователь получает подтверждение заказа, а также уведомление на электронную почту. В случае неудачной оплаты пользователь получает сообщение об ошибке и возможность повторить попытку
![](./images/2.jpg)

Диаграмма последовательностей на рисунке иллюстрирует процесс написания статьи. Пользователь проходит авторизацию на сайте, и, если авторизация успешна, ему открывается доступ к функционалу для создания документа. В процессе написания статьи происходит динамическое сохранение данных, чтобы предотвратить их потерю. После завершения работы пользователь может либо сохранить статью как черновик, либо опубликовать её на сайте. Если авторизация не прошла, пользователь получает уведомление с просьбой повторить попытку.
![](./images/3.jpg)

Диаграмма последовательностей на рисунке показывает процесс оценки статьи. Пользователь вводит комментарий и выставляет оценку, после чего система проверяет его авторизацию. Если авторизация пройдена, отзыв сохраняется в базе данных и публикуется на сайте. Если же авторизация не удалась, пользователь получает уведомление с предложением авторизоваться и повторить попытку.
![](./images/5.jpg)

Диаграмма последовательностей на рисунке описывает процесс добавления AI-инструмента в избранное. Пользователь выбирает инструмент и нажимает кнопку добавления в избранное. Система проверяет, авторизован ли пользователь. В случае успешной авторизации инструмент сохраняется в списке избранного. Если авторизация не удалась, система уведомляет пользователя о необходимости авторизоваться для завершения действия.
![](./images/4.jpg)

---

## 4. Перечень сделанных предположений

1. Доступность платформы:
   - Предполагается, что все функции платформы доступны зарегистрированным пользователям после аутентификации.
2. Роли пользователей:
   - Роль "Guest" имеет доступ только к просмотру опубликованных документов и оставлению обратной связи.
   - Роль "Admin" обладает расширенными правами, включая управление ролями, удаление учётных записей и настройку инструментов.
3. Права на документы:
   - Документы, помещённые в корзину, можно восстановить до момента их окончательного удаления.
   - Опубликованные документы доступны всем пользователям, если доступ не закрыт владельцем.
4. Оплата услуг:
   - Платформа предусматривает поддержку нескольких способов оплаты, включая банковские карты и электронные кошельки.
5. Инструменты и настройки:
   - Пользователи могут настраивать инструменты и сохранять их в избранное для удобного доступа.
6. Отзывы и обратная связь:
   - Все отзывы на опубликованные документы модерируются администратором платформы.

---

## 5. Перечень нефункциональных требований

1. Производительность:
   - Система должна обеспечивать отклик на действия пользователей не более чем за 2 секунды.
2. Масштабируемость:
   - Платформа должна поддерживать одновременное использование до 10,000 пользователей без потери производительности.
3. Доступность:
   - Гарантированная доступность платформы составляет не менее 99.5% времени.
4. Безопасность:
   - Использование двухфакторной аутентификации для защиты учётных записей.
   - Шифрование всех пользовательских данных и платёжной информации.
5. Юзабилити:
   - Интерфейс должен быть интуитивно понятным, включая простую навигацию по документам, инструментам и настройкам.
6. Совместимость:
   - Поддержка всех современных браузеров (Chrome, Firefox, Safari, Edge).
   - Корректная работа на мобильных и настольных устройствах.
7. Поддержка пользователей:
   - Наличие службы технической поддержки с гарантированным ответом на запросы в течение 24 часов.