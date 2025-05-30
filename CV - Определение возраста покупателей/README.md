# Определение возраста покупателей

Сетевой супермаркет внедряет систему компьютерного зрения для обработки фотографий покупателей. Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:
- Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы;
- Контролировать добросовестность кассиров при продаже алкоголя.
________
**Цель:**
- Построить модель, которая по фотографии определит приблизительный возраст человека.
_______
**Задача:**
- Построить и обучите свёрточную нейронную сеть на датасете с фотографиями людей. 
- Добиться значения MAE на тестовой выборке не больше 8.
__________
**План работы:**
1. Исследовательский анализ данных
2. Обучение модели
3. Анализ обученной модели
__________
**Данные:**
- Набор фотографий людей с указанием возраста.

__________

# Результат работы

- MAE = 7.0411

В среднем предсказания возраста моделью отличаются от реальных возрастов примерно на 7 лет.
__
**Выводы для бизнеса:**

Одно из применений модели: предлагать товары, которые могут заинтересовать покупателей этой возрастной группы.   
- Если возрастные группы разбиты на 10-15 лет (вероятно, даже больше), то эта ошибка (в 7 лет) не критична.

Вторая задача: контролировать добросовестность кассиров при продаже алкоголя.  
- В данном случае не можем гарантировать, что модель поможет качественно решить задачу. Здесь имеет место высокая чувствительность к погрешности предсказания модели. 
- С учетом достигнутой средней ошибки в 7 лет, можем сказать, что для возрастов 11-25 лет высока вероятность ошибки в оценке того, ниже или выше 18 лет реальный возраст клиента.
- При предсказанном возрасте посетителя выше 26 лет или ниже 11 с большей уверенностью можно оценивать, является ли постетель совершеннолетним или нет.
