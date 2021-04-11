## Задача
Определить сельскохозяйственную культуру по ежедневным значениям нормализованного индекса вегетации.
### Описание данных¶
Данные собраны по 17 регионам РФ преимущественно Европейской части России. Каждая культура задаётся набором полей:
Year – год
Field ID – поле, на котором растёт культура
Culture – вид культуры
Field Area – площадь поля, занимаемая данной культурой
Day i – нормализованный индекс вегетативности в i-ый день
### Метрика
Для оценивания качества прогноза используется метрика f1_score (с параметром average = ‘weighted’): Прогноз y_preds представляет собой вектор длины len(X_test), где- вид культуры для i-ого объекта из X_test. y_true содержит истинные классы культуры. Скор считается следующим образом: f1_score(y_test, y_preds, average='weighted')