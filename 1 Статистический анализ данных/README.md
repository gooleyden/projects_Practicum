# Статистический анализ данных сервиса аренды самокатов

В нашем распоряжении данные с информацией о некоторых пользователях из разных городов, поездках и видах подписки сервиса аренды самокатов GoFast.

**Цель проекта:**  
- Выяснить, являются ли пользователи с подпиской более выгодными клиентами для бизнеса, чем пользователи без подписки.

**План работы:**  
1. Ознакомление с данными
2. Предобработка данных
3. Исследовательский анализ данных
4. Объединение данных в один датафрейм
5. Подсчет помесячной выручки для каждого клиента
6. Проверка гипотез 

**Общая информация о данных**  

Чтобы совершать поездки по городу, пользователи сервиса GoFast пользуются мобильным приложением.   
Сервисом можно пользоваться: 
1. без подписки
 * абонентская плата отсутствует;
 * стоимость одной минуты поездки — 8 рублей;
 * стоимость старта (начала поездки) — 50 рублей;
2. с подпиской Ultra
 * абонентская плата — 199 рублей в месяц;
 * стоимость одной минуты поездки — 6 рублей;
 * стоимость старта — бесплатно.
 
В нашем распоряжении 3 датасета с информацией о:
1. Пользователях - их имени, возрасте, городе и подписке;
2. Поездках - длительности, расстоянии и дате совершения;
3. Типах подписки - их условиях и стоимости.

# Результат

По результатам проверки гипотез можно сделать следующие выводы:

1. Есть основания полагать, что в среднем пользователи с подпиской тратят больше времени на поездки.
2. Вероятно, среднее расстояние, которое проезжают пользователи с подпиской за одну поездку, не превышает 3130 метров.
3. Есть серьезные основания полагать, что помесячная выручка от пользователей с подпиской выше, чем у пользователей без подписки.

Рекомендации:

- Есть основания полагать, что для компании пользователи с подпиской являются более выгодными, на основании результатов проверки гипотез.

- Вероятно, увеличение количества пользователей с подпиской ultra приведеет к увеличению средней длительности поездки и увеличению выручки.
