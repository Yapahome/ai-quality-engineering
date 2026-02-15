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
