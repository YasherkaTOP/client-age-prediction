## Предсказание возраста клиента на основе информации о его расходах по карте. 
### Изменённое задание соревнования "Уроки настоящего от Сбербанка"
Соревнование, в котором нужно предсказать возраст клиента по его расходам.

### Данные
Для решения задачи участникам предоставляется информация о транзакциях клиентов банка. Объемом около 27 000 000 миллионов записей. Каждая запись описывает одну банковскую транзакцию.

#### Мы подготовили два набора данных:
##### Обучающий transactions_train.csv, в котором для каждой транзакции известна дата, сумма, тип и id клиента:
1. сlient_id – уникальный номер клиента;
2. trans_date – дата транзакции (представляет из себя просто номер дня в хронологическом порядке, начиная от заданной даты);
3. small_group – группа транзакций, характеризующих тип транзакции (например, продуктовые магазины, одежда, заправки, детские товары и т.п.);
4. amount_rur – сумма транзакции (для анонимизации данные суммы были трансформированы без потери структуры).
   
##### train_target.csv. В нем содержится информация о Клиенте и метка возрастной группы, к которой он относится:
1. client_id – уникальный номер Клиента (соответствует client_id из файла transactions_train.csv);
2. bins – метка возраста.

### Задача
Построить модель мультиклассовой классификации.
Оценка проводится по accuracy метрике.

### Использованные библиотеки
1. pandas
2. sklearn
3. optuna
4. catboost

### Итог
Baseline решение от организаторов имеет accuracy = 0.6119

Моё решение имеет accuracy = 0.6277
