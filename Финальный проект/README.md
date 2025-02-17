# Исследование оттока клиентов телеком оператора.

#### Задание: 
- На основе персональных данных клиентов оператора определить уйдет клиент или нет

#### Описание:
- В нашем расположении есть персональные данные клиентов собранные командой оператора. На основании них нам требуется сделать прогноз уйдет клиент или нет, для того чтобы оператор мог заблаговременно предпринять какие-либо шаги по удержанию клиента(особые условия, скидки, промокоды и т.д). 

#### Используемые навыки:
- Pandas, Scikit-learn, plotly.express, matplotlib, roc_auc_score, f1_score, RandomizedSearchCV

#### Тэги:
- Анализ данных, классификация, подбор гиперпараметров, выбор модели МО 

#### Статус проекта: 
- Завершен 

#### Вывод: 
Лучше всех себя показал `LGBMClassifier` со следующими гиперпараметрами:

`random_state = 120922, n_jobs = -1, n_estimators = 541, max_depth = 36, class_weight='balanced'`

Его метрики составили:

`F1_score - 0.7286652078774617, roc_auc - 0.9048027628752702`
Наиболее важными признаками в предсказании оказались **`длительность контракта`** и **`месячный чек`**, соответственно оператору дается рекомендация в первую очередь обращать внимание на новеньких клиентов и стараться максимализировать их лояльность, так как больше всего уходят именно они. Для повышения лояльности "новеньких" клиентов предлагаем в первую очередь манипулировать ежемесечными тратами клиента предлагая скидки, а после уже предложением дополнительных услуг и прочих бонусов.
