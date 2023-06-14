# Проект по парсингу цен и характеристик смартфонов с торговой площадки eBay

## Предыстория
Для курсовой работы Андрея Кривоносова мы решили спарсить данные с ebay: продаваемые там телефоны, их марки и характеристики. На основне этих данныех Андрей далее будет определять изменение в истинном спросе потребителей на товар после ажиотажа перед началом продаж.

## Суровое описание проекта

Этот проект предназначен для сбора данных о ценах и характеристиках смартфонов с торговой площадки eBay для последующего анализа гедонистического спроса на эти товары и взаимосвязи между реальной ценностью товаров и их субъективной ценностью (хайпом).

## Структура проекта
* Data Tables 
  * Global
    * Characteristics.tsv
    * Sales.tsv
  * Nokia
    * Nokia Characteristics.tsv
    * Nokia Sales.tsv
  * Redmi
    * Redmi Characteristics.tsv
    * Redmi Sales.tsv 
  * Trends
    * Nokia.csv
    * Redmi.csv
* EDA
  * Global EDA.ipynb - файл с первичным анализом полученных датафреймов и визуализацией данных
* MathStat
  * Global Hypothesis.ipynb
* ML
  * Create Model.ipynb
  * Nokia and Redmi estimated.tsv
  * Price Model.pkl
  * Sales Value Model.pkl
  * Using model and analyse.ipynb
* Parsers 
  * Parser Global.ipynb - файл с кодом парсера данных с платформы eBay. С его помощью собирается информация о статистике продаж различных моделей смартфонов и их характеристики. 
  * Parser Nokia.ipynb - файл с кодом парсера данных с платформы eBay. С его помощью собирается информация о статистике продаж смартфонов Nokia и их характеристики. 
  * Parser Redmi.ipynb - файл с кодом парсера данных с платформы eBay. С его помощью собирается информация о статистике продаж смартфонов Redmi и их характеристики. 
* Preprocessing
  * Global
    * Global Merged.tsv - таблица с объединёнными исходными данными для случайной выборки смартфонов
    * Global preprocessed.tsv - таблица с предобработанными объединёнными данными для случайной выборки смартфонов, на основе которых возможно построение гедонистической функции спроса
    * Global preprocessing.ipynb - код для объединения и предобработкой данных случайной выборки смартфонов, который позволяет получить две таблицы в этой же директории
  * Nokia
    * Nokia Merged.tsv  - таблица с объединёнными исходными данными для выборки смартфонов бренда Nokia
    * Nokia preprocessed.tsv - таблица с предобработанными объединёнными данными для выборки смартфонов бренда Nokia, для которых будет применяться гедонистическая функции спроса
    * Nokia preprocessing.ipynb - код для объединения и предобработкой данных случайной выборки смартфонов, который позволяет получить две таблицы в этой же директории
  * Redmi
    * Redmi Merged.tsv  - таблица с объединёнными исходными данными для выборки смартфонов бренда Redmi
    * Redmi preprocessed.tsv - таблица с предобработанными объединёнными данными для выборки смартфонов бренда Redmi, для которых будет применяться гедонистическая функции спроса
    * Redmi preprocessing.ipynb - код для объединения и предобработкой данных случайной выборки смартфонов, который позволяет получить две таблицы в этой же директории
  * Creating GreatBD.ipynb - код для объединения выборок Global, Redmi и Nokia
  * Great_BD.tsv - таблица с предобработанными объединёнными данными для выборки смартфонов бренда Redmi, Nokia и случайной выборки смартфонов
* LICENSE - Файл 
* README.md - файл, который Вы читаете сейчас

* preprocessed.tsv 
* Second EDA.ipynb - файл с вторичной предобработкой, который позволяет получить preprocessed.tsv.
* First model.ipynb - Случайный лес для прогнозирования цены на основе характеристик и Линейная регрессия для прогнозирования спроса на основе характеристик и цены

* Папка Data Tables содержит промежуточные таблицы, а именно: 
  * Names.tsv: файл с собранной базой данных наименований смартфонов и их показателями продаж
  * characteristics_df.tsv: файл с базой данных характеристик смартфонов
  * great_bd.tsv: объединённая таблица со статистикой продаж и характеристиками смартфонов без предобработки

