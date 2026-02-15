# AI Quality Engineering — заметки

## AI-pipeline (конвейер AI-системы)
данные (data) → подготовка данных (preprocessing) → обучение (training) → оценка (evaluation) → деплой (deployment) → использование модели (inference) → мониторинг (monitoring)

## Интерпретация через QA
набор данных (dataset) = тестовые данные (test data)  
обучение (training) = процесс сборки системы (build system)  
оценка (evaluation) = проверки через метрики (assertions)  
использование модели (inference) = поведение системы (system behavior)  
мониторинг (monitoring) = QA в production (production QA)

## Основные идеи
QA в AI тестирует поведение модели и качество решения задачи, а не точное совпадение с ожидаемым результатом.

Дефекты данных (data defects):
- недостаток данных (insufficient data)
- неконсистентность данных (inconsistent data)
- ошибки разметки (labeling errors)
- смещение данных (bias)
- дрейф данных (data drift)

Качество модели (model quality) — способность модели стабильно решать задачу на новых данных.
