# custom-datasets

Supported custom datasets

<pre>
</pre>

Custom dataset examples for machine learning.

download from github
<pre>
!git clone https://github.com/automatethem/download
</pre>

install datasets package
<pre>
pip install datasets
</pre>

python example
<pre>
from datasets import Dataset
from datasets import load_dataset

dataset_dict = load_dataset("csv", data_files={"train": "download/tabular_regression/father_son_height/train.csv", "validation": "download/tabular_regression/father_son_height/validation.csv"})
#dataset_dict = load_dataset("json", data_files={"train": "download/tabular_regression/father_son_height/train.json", "validation": "download/tabular_regression/father_son_height/validation.json"})
#print(dataset_dict)
'''
DatasetDict({
    train: Dataset({
        features: ['Father', 'Son'],
        num_rows: 755
    })
    validation: Dataset({
        features: ['Father', 'Son'],
        num_rows: 323
    })
})
'''

train_dataset = dataset_dict['train']
validation_dataset = dataset_dict['validation']

#print(train_dataset)
'''
Dataset({
    features: ['Father', 'Son'],
    num_rows: 755
})
'''

for example in train_dataset:
    print(example['Father']) #165.1
    print(example['Son']) #151.892
    break
</pre>

other examples

<a href="https://github.com/automatethem/download/tree/main/tabular_regression/father_son_height">tabular_regression/father_son_height</a><br>
<a href="https://github.com/automatethem/download/tree/main/image_classification/multiple_classes/grayscale">image_classification/multiple_classes/grayscale</a>


