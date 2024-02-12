# gb-one-hot
# Импортируем библиотеку pandas
import pandas as pd

# Создаем DataFrame из списка
lst = ['robot'] * 10
lst += ['human'] * 10
random.shuffle(lst)
data = pd.DataFrame({'whoAmI':lst})

# Получаем список уникальных значений в столбце whoAmI
values = data['whoAmI'].unique()

# Для каждого уникального значения создаем новый столбец с названием value_oh и заполняем его 0 или 1
for value in values:
    data[value + '_oh'] = data['whoAmI'].apply(lambda x: 1 if x == value else 0)

# Выводим результат
data.head()
