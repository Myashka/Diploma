# Data

## Part 1

- Первый взгляд на данные
- Отсеяны вопросы с \<pre>\<code>
- Отфильтрованы данные с \<img>
- Выбраны ответы с _score > 5_
- Очищены данные от HTML Разметки
- Посмотрено распределение длин

## Part 2

- Проверены данные на наличие пропусков
- Отсеяны вопросы с \<pre>\<code>
- Отфильтрованы данные с \<img>
- Выбраны ответы с _score > 1_
- Очищены данные от HTML Разметки
- Сохранены данные в _filtered_df.csv_

## Part 3

- Отобраны ответы с тегом _Android_
- Выбраны только лучшие ответы на каждый вопрос и вопросы имеющие score > 1
- Выбраны ответы ограниченной длины (150 и 200)
- Использованы regex для классификации выпросов на темы
- Данные сохранены в _df_200.csv_ и _df_150.csv_

### Классификация regex

За основу взяты regex из [статьи](https://link.springer.com/article/10.1007/s10664-019-09758-x)

Сами файлы можно найти [здесь](https://figshare.com/articles/online_resource/qc_replication_package_zip/8870123/1)

## Part 4

- Сделана эвалуацию базовой GPT neo на случайной выборке из датасета, включающего 105, либо 500 экземпляров (API Usage category, <=200 length)
- Отобраны экземпляры, имеющие наименьшее косинусное расстояние Q_title и Q_Body, используя [BERToflow](https://github.com/lanwuwei/BERTOverflow) или [StackOverFlow MPnet](https://huggingface.co/flax-sentence-embeddings/stackoverflow_mpnet-base), информация добавлена в _df_200.csv_
- Сделана эвалуация базовой модели на случайной, хорошей и плохих выборках с различными promts
- Произведены сравнения результатов (Notebooks/GPT_neo_analys_3.ipynb)