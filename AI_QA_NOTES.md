# AI Quality Engineering — Notes

## AI pipeline
data → preprocessing → training → evaluation → deployment → inference → monitoring

## QA interpretation
dataset = test data
training = build system
evaluation = assertions
inference = system behavior
monitoring = production QA

## Core ideas
QA in AI tests model behavior and quality, not exact expected outputs.

Data defects:
- insufficient data
- inconsistent data
- labeling errors
- bias
- data drift

Model quality = ability to solve task reliably on new data.

## Model evaluation metrics (метрики оценки модели)

Confusion matrix (матрица ошибок):
TP — true positive
TN — true negative
FP — false positive
FN — false negative

Accuracy = (TP + TN) / all predictions
Recall = TP / (TP + FN)
Precision = TP / (TP + FP)
F1 = balance between precision and recall

Метрики в AI работают как вероятностные assertions.
