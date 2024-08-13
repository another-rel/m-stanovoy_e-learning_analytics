# Описание проекта

## Цель проекта: Оценка метрик качества предлагаемых e-learning платформой курсов и качественный анализ аудитории

Работа выполнена на **Python** с использованием **Jupyter Notebook**.

Описание данных:

* **assessments.csv** – данные о существующем наборе оценочных работ

| code_module | code_presentation | id_assessment | assessment_type | date | weight |
| ----------- | ----------------- | ------------- | --------------- | ---- | ------ |
| AAA | 2013J | 1752 | TMA | 19.0 | 10.0 |
| AAA | 2013J | 1753 | TMA | 54.0 | 20.0 |
| AAA | 2013J | 1754 | TMA | 117.0 | 20.0 |
| AAA | 2013J | 1755 | TMA | 166.0 | 20.0 | 
| AAA | 2013J | 1756 | TMA | 215.0 | 30.0 |

* **courses.csv** – данные о списках предметов по семестрам

| code_module | code_presentation | module_presentation_length |
| ----------- | ----------------- | -------------------------- |
| AAA | 2013J | 268 |
| AAA | 2013J | 269 |
| AAA | 2013J | 268 |
| AAA | 2013J | 262 |
| AAA | 2013J | 240 |

* **studentRegistration.csv** – данные о регистрации студентов на прохождение курса

| code_module | code_presentation | id_student | date_registration | date_unregistration |
| ----------- | ----------------- | ---------- | ----------------- | ------------------- |
| AAA | 2013J | 11391 | -159.0 | NaN |
| AAA | 2013J | 28400 | -53.0 | NaN |
| AAA | 2013J | 30268 | -92.0 | 12.0 |
| AAA | 2013J | 31604 | -52.0 | NaN |
| AAA | 2013J | 32885 | -176.0 | NaN |

* **studentAssessment.csv** – данные о результатах оценочных работ студентов

| id_assessment | id_student | date_submitted | is_banked | score |
| ------------- | ---------- | -------------- | --------- | ----- |
| 1752 | 11391 | 18 | 0 | 78.0 |
| 1752 | 28400 | 22 | 0 | 70.0 |
| 1752 | 31604 | 17 | 0 | 72.0 |
| 1752 | 32885 | 26 | 0 | 69.0 |
| 1752 | 38053 | 19 | 0 | 79.0 |

### **Задача 1** 

Определить сколько студентов успешно сдали только один курс. (Успешная сдача — это зачёт по курсу на экзамене)

### **Задача 2**

Выявить самый сложный и самый простой экзамен, т.е. найти курсы и экзамены в рамках курса, которые обладают самой низкой и самой высокой завершаемостью.

*Под завершаемостью подразумевается отношение кол-ва успешных экзаменов к кол-ву всех попыток сдать экзамен.*

### **Задача 3**

По каждому предмету определить средний срок сдачи экзаменов (под сдачей понимается последнее успешное прохождение экзамена студентом)

### **Задача 4**

Выявить самые популярные предметы (ТОП-3) по количеству регистраций на них. А также предметы с самым большим оттоком (ТОП-3)

### **Задача 5**

В период с начала 2013 по конец 2014 выявить семестр с самой низкой завершаемостью курсов и самыми долгими средними сроками сдачи курсов.

### **Задача 6**

Построить адаптированные RFM-кластеры студентов, чтобы качественно оценить аудиторию платформы. Для каждого RFM-сегмента построить границы метрик recency, frequency и monetary для интерпретации этих кластеров.

<hr>

### **Реализация проекта:**
<ul>
<li>Применены API для выгрузки данных из Яндекс.Диска.</li>
<li>Проведен предварительный анализ (EDA) и предобработка данных.</li>
<li>Выявлены курсы и экзамены в рамках курса, которые обладают самой низкой и самой высокой завершаемостью.</li>
<li>Определен средний срок сдачи экзаменов.</li>
<li>Выявлены самые популярные предметы по количеству регистраций на них (ТОП-3) и предметы с самым большим оттоком (ТОП-3).</li>
<li>Выявлены семестры с самой низкой завершаемостью курсов и самыми долгими средними сроками сдачи курсов на период с начала 2013 по конец 2014.</li>
<li>Проведен качественный анализ аудитории с помощью RFM-кластеризации.</li>
</ul>
