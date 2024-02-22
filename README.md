# Выбор оптимального корпоративного тарифа для абонентов A1(Беларусь)

**Описание:**

Этот проект анализирует данные о звонках, трафике, пользователях и тарифах A1 для корпоративных клиентах на основании детализаций, доступных в Личном кабинете, и предланает оптимальные тарифы с указанием желательных опций по каждому абоненту.

Также доступна сегментация абонентов по группам и выбор тарифа для каждой группы.

**Язык программирования:** Python

**Библиотеки:** pandas, numpy, matplotlib

**Цель проекта:**

* Определить оптимальный тариф для каждого пользователя A1.
* Сравнить расходы пользователей на текущих и оптимальных тарифах.
* Выявить факторы, влияющие на выбор тарифа.

**Функциональные возможности:**

- **Загрузка и преобразование данных**: Проект автоматически загружает данные из предоставленных файлов Excel с детализацией звонков и трафика, а также информацию о пользователях и их текущих тарифах. Производится преобразование данных для удобства дальнейшего анализа, включая конвертацию длительности звонков из секунд в минуты и объема интернет-трафика из Кбайт в ГБ.

- **Расчет среднемесячных значений**: Для каждого пользователя рассчитываются среднемесячные значения исходящих минут и трафика. Это позволяет понять, каким образом пользователи используют свои тарифы и какие потребности у них возникают в среднем за месяц.

- **Определение оптимального тарифа и опции для каждого пользователя**: На основании среднемесячных значений потребления и текущих тарифов для каждого пользователя предлагается оптимальный тариф из линейки "Своё решение" от A1. Для каждого пользователя также предлагается опция внутри тарифа, которая наиболее точно соответствует его потребностям.

- **Визуализация данных о потреблении**: Проект предоставляет графики и диаграммы, показывающие распределение потребления минут и трафика среди пользователей, а также сравнение расходов на текущих и оптимальных тарифах. Это позволяет наглядно увидеть потенциальную экономию и более эффективное использование тарифных планов.

- **Сегментация пользователей**: С помощью методов машинного обучения (кластеризация K-means) пользователи группируются на основе их поведения и потребностей. Для каждого сегмента определяется наиболее подходящий тариф, что позволяет более целенаправленно подходить к предложению услуг для различных групп пользователей.

**Примеры использования функциональностей:**

После анализа данных пользователь с высоким потреблением интернет-трафика и низким объемом исходящих звонков может быть переведен на тариф с большим объемом трафика и опцией, предоставляющей дополнительный объем данных. Это позволит пользователю избежать сверхлимитных расходов и оптимизировать свои ежемесячные платежи.

Для сегмента пользователей, в основном использующих звонки, будет предложен тариф с большим количеством минут и возможностью бесплатных звонков внутри сети, что обеспечит им необходимый объем услуг без необходимости переплачивать за неиспользуемый трафик.

**Как использовать:**

1. Клонируйте репозиторий с помощью `git clone https://github.com/51n1au5k1/A1-CORP`.
2. Разместите файлы детализации в папку `RAW`.
3. Поместите список пользователей (выгруженный из ЛК) в корневую папку проекта.
4. Установите необходимые зависимости через `pip install -r requirements.txt`.
5. Запустите в Jupyter Notebook.

*Сейчас в RAW и accounts находятся тестовые данные. Их следует удалить перед использованием.* 
