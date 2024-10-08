# Прогнозирование уровня удовлетворенности сотрудников для компании «Работа с заботой»

HR-аналитики компании «Работа с заботой» помогают бизнесу оптимизировать управление персоналом: бизнес предоставляет данные, а аналитики предлагают, как избежать финансовых потерь и оттока сотрудников. В этом HR-аналитикам пригодится машинное обучение, с помощью которого получится быстрее и точнее отвечать на вопросы бизнеса.

Компания предоставила данные с характеристиками сотрудников компании. Среди них — уровень удовлетворённости сотрудника работой в компании. Эту информацию получили из форм обратной связи: сотрудники заполняют тест-опросник, и по его результатам рассчитывается доля их удовлетворённости от 0 до 1, где 0 — совершенно неудовлетворён, 1 — полностью удовлетворён. 
Собирать данные такими опросниками не так легко: компания большая, и всех сотрудников надо сначала оповестить об опросе, а затем проследить, что все его прошли. 

**Первая задача** — построить модель, которая сможет предсказать уровень удовлетворённости сотрудника на основе данных заказчика. 
Почему бизнесу это важно: удовлетворённость работой напрямую влияет на отток сотрудников. А предсказание оттока — одна из важнейших задач HR-аналитиков. Внезапные увольнения несут в себе риски для компании, особенно если уходит важный сотрудник.

**Вторая задача** — построить модель, которая сможет на основе данных заказчика предсказать то, что сотрудник уволится из компании.

## Задачи исследования
* провести предобработку и анализ данных для первой задачи (предсказание уровня удовлетворённости сотрудника)
* подготовить данные для первой задачи
* обучить модель для первой задачи
* оформить промежуточные выводы по первой задаче
* провести предобработку и анализ данных для второй задачи (предсказание увольнения сотрудника из компании)
* добавить новый входной признак для второй задачи 
* подготовить данные для второй задачи
* обучить модель для второй задачи
* оформить промежуточные выводы по второй задаче
* сделать общий вывод, дать рекомендации

## Цели исследования
1) построить модель, которая сможет предсказать уровень удовлетворённости сотрудника на основе данных заказчика  
2) построить модель, которая сможет на основе данных заказчика предсказать то, что сотрудник уволится из компании

## Данные для анализа

* для **первой задачи** заказчик предоставил файлы с данными:

*train_job_satisfaction_rate.csv* (тренировочная выборка)  
*test_features.csv* (входные признаки тестовой выборки)  
*test_target_job_satisfaction_rate.csv* (целевой признак тестовой выборки)

* для **второй задачи** заказчик предоставил файлы с данными:

*train_quit.csv* (тренировочная выборка)  
*test_features.csv* (входные признаки тестовой выборки)  
*test_target_quit.csv* (целевой признак тестовой выборки)

## Описание данных

Для **первой задачи**:
    
* *id* — уникальный идентификатор сотрудника
* *dept* — отдел, в котором работает сотрудник
* *level* — уровень занимаемой должности
* *workload* — уровень загруженности сотрудника
* *employment_years* — длительность работы в компании (в годах)
* *last_year_promo* — показывает, было ли повышение за последний год
* *last_year_violations* — показывает, нарушал ли сотрудник трудовой договор за последний год
* *supervisor_evaluation* — оценка качества работы сотрудника, которую дал руководитель
* *salary* — ежемесячная зарплата сотрудника
* *job_satisfaction_rate* — уровень удовлетворённости сотрудника работой в компании, целевой признак

Для **второй задачи** входные признаки - те же, что и в первой.  
* *quit* — увольнение сотрудника из компании (целевой признак)

## Этапы работы над проектом

**Задача 1: предсказание уровня удовлетворённости сотрудника**

*Шаг 1.* Загрузка данных  
*Шаг 2.* Предобработка данных  
*Шаг 3.* Исследовательский анализ  
*Шаг 4.* Корреляционный анализ  
*Шаг 5.* Подготовка данных и обучение моделей  
*Шаг 7.* Промежуточные выводы

**Задача 2: предсказание увольнения сотрудника из компании**

*Шаг 1.* Загрузка данных  
*Шаг 2.* Предобработка данных  
*Шаг 3.* Исследовательский анализ

* исследовательский анализ
* корреляционный анализ
* составление портрета уволившегося сотрудника
* проверка утверждения: уровень удовлетворённости сотрудника работой в компании влияет на то, уволится ли сотрудник

*Шаг 4.* Добавление нового входного признака

* добавление признака 'job_satisfaction_rate', предсказанный лучшей моделью первой задачи, к входным признакам второй задачи

*Шаг 5.* Подготовка данных и обучение моделей  
*Шаг 6.* Анализ важности признаков

* выявление признаков, которые оказывают наименьшее влияние на модель

*Шаг 7.* Подготовка данных и обучение моделей после исключения признаков  
*Шаг 8.* Промежуточные выводы

**Общий вывод**
