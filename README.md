# Correlation Miner: первая фаза

Дополнительное задание по дисциплине «Системы поддержки принятия решений». Ноутбук `correlation_miner_phase1.ipynb` строит граф процесса по мини-журналу из статьи Pourmirza, Dijkman и Grefen без идентификаторов экземпляров. Рассматривается только первая фаза: матрицы порядка и длительности, целочисленная модель и устранение циклов.

В статье не раскрыт точный код эвристики сопоставления событий, поэтому используется собственный воспроизводимый локальный поиск; проверка с опубликованной матрицей длительностей приведена отдельно. Результат также сравнивается с реализацией PM4Py classic, отличающейся ограничениями на начало и конец процесса.

## Запуск

Рекомендуется Python 3.12 и отдельное виртуальное окружение:

```bash
python -m pip install pyomo highspy numpy pandas matplotlib networkx pm4py==2.7.23.12 scipy jupyterlab
python -m jupyter lab correlation_miner_phase1.ipynb
```

Выберите Kernel → Restart Kernel and Run All Cells. Основной решатель — HiGHS через `appsi_highs`; предусмотрены `highs` и CBC. PM4Py Community распространяется на условиях [AGPL-3.0](https://github.com/process-intelligence-solutions/pm4py/blob/release/LICENSE).

Источник: [Pourmirza, Dijkman, Grefen, Correlation Miner (2017)](https://doi.org/10.1142/S0218843017420023). Документация: [PM4Py Correlation Miner](https://processintelligence.solutions/pm4py/examples/process-discovery).
