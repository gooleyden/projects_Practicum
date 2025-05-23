# Модель предсказания ухода клиентов для оператора связи
Оператор связи хочет бороться с оттоком клиентов. Для этого его сотрудники начнут предлагать промокоды и специальные условия всем, кто планирует отказаться от услуг связи. 
Чтобы заранее находить таких пользователей, нужна модель, которая будет предсказывать, разорвёт ли абонент договор. 
_______________

**Цель**
- Построить модель машинного обучения, которая по входным признакам будет предсказывать, разорвет ли клиент контракт с операторов связи.
________
**Задача**
- Построить несколько моделей МО, включая градиентный бустинг
- Выбрать наиболее эффективную модель
- Достичь значения ROC-AUC более 85 на тестовой выборке
- Проанализировать результаты и сделать выводы для бизнеса

_________ 
**Описание данных:**

4 датасета со следующими признаками:

*1 информация о договоре*:
- id абонента; дата начала действия договора; дата окончания действия договора; тип оплаты (раз в год-два или ежемесячно); электронный расчётный лист; тип платежа; расходы за месяц; общие расходы абонента.

*2 персональные данные клиента*:
- id пользователя; пол; является ли абонент пенсионером; есть ли у абонента супруг или супруга; есть ли у абонента дети.

*3 информация об интернет-услугах*
- id пользователя; тип подключения;  блокировка опасных сайтов; облачное хранилище файлов для резервного копирования данных; антивирус; выделенная линия технической поддержки; стриминговое телевидение; каталог фильмов.

*4 информация об услугах телефонии*
- id пользователя; подключение телефона к нескольким линиям одновременно (да/нет).
_____

**Описание услуг**

Оператор предоставляет два основных типа услуг: 
- Стационарную телефонную связь. Телефон можно подключить к нескольким линиям одновременно.
- Интернет. Подключение может быть двух типов: через телефонную линию (DSL, от англ. digital subscriber line — «цифровая абонентская линия») или оптоволоконный кабель (Fiber optic).

Также доступны такие услуги:
- Интернет-безопасность: антивирус (DeviceProtection) и блокировка небезопасных сайтов (OnlineSecurity);
- Выделенная линия технической поддержки (TechSupport);
- Облачное хранилище файлов для резервного копирования данных (OnlineBackup);
- Стриминговое телевидение (StreamingTV) и каталог фильмов (StreamingMovies).

Клиенты могут платить за услуги каждый месяц или заключить договор на 1–2 года. Возможно оплатить счёт разными способами, а также получить электронный чек.

_______
**План работы**
1. Загрузка данных
2. Предобработка и исследовательский анализ данных
3. Объедиинение датасетов
4. Создание и отбор признаков
5. Исследовательский анализ данных объединенного датасета
6. Корреляционный анализ данных
7. Подготовка данных для обучения модели
8. Обучение моделей МО
9. Выбор лучшей модели
10. Проверка на тестовой выборке и рекомендации заказчику
11. Общий вывод
___
# Результат работы

ROC-AUC на тестовой выборке:
- 0.92

Точность модели: 91.7%  
Модель выявляет 57% клиентов, планирующих разорвать договор. Из клиентов, помеченных моделью как потенциально разрывающих договор, 85% действительно такими являются.
____
**Выводы для бизнеса:**

На текущем этапе рекомендуется установить скидку 20-30% при пороге классификации 0.6.

Предложение скидок клиентам, которых модель определяет как готовых разорвать договор, позволит снизить эти убытки ориентировочно до 18.5% - 13%, в зависимости от размера скидок и процента клиентов, согласившихся остатся на таких условиях.

График влияния скидки на уровень сохраненного дохода при пороге классификации 0.6:
<img width="611" alt="image" src="https://github.com/user-attachments/assets/354c8029-acbd-4355-a5e2-b3c7c239c369" />
