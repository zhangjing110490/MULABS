# Datasets for Paper: MULABS: Multi-Task Learning with Attention-Based Scoring for Click-Through Rate Prediction on Sparse Data in Healthcare Real-World Scenarios

## Table of Contents

[comment]: <> (- [Security]&#40;#security&#41;)
* [Dataset](#Dataset)
  * [Description](#Description)
  * [Data Structure](#Data_Strcture)
  * [Example Code](#Example_Code) 
* [Dataset](#Dataset)
  * [Description](#Description)
  * [Data Structure](#Data_Strcture)
  * [Example Code](#Example_Code) 

[comment]: <> (- [Usage]&#40;#usage&#41;)
[comment]: <> (- [API]&#40;#api&#41;)
[comment]: <> (## Security)

## Dataset: duration_train_data.pkl & duration_test_data.pkl
### Description
training and testing dataset for reading time prediction task
### Data Structure
an dictionary with keys input and output; the value for key input is also an dictionary, which contains an numpy array for each feature; the value for key output is an numpy array containing ratings for all movies from 0 to 4.
### Example Code:
       import pickle
       with open('duration_train_data.pkl', 'rb') as f:
           data = pickle.load(f)
           input_data = data['input']
           output_data = data['output']
           for feature in input_data.keys():
               print(f'feature name is {feature}')
               print(f'check feature dimension: {input_data[feature].shape}')
           output_labels = set(list(output_data))
           print(f'the output labels include: {output_labels}')


## Dataset: ctr_train_data.pkl & ctr_test_data.pkl
### Description
training and testing dataset for CTR prediction task
### Data Structure
an dictionary with keys input and output; the value for key input is also an dictionary, which contains an numpy array for each feature; the value for key output is an numpy array containing binary labels for all movies.
### Example Code:
    import pickle
    with open('ctr_train_data.pkl', 'rb') as f:
        data = pickle.load(f)
        input_data = data['input']
        output_data = data['output']
        for feature in input_data.keys():
            print(f'feature name is {feature}')
            print(f'check feature dimension: {input_data[feature].shape}')
        output_labels = set(list(output_data))
        print(f'the output labels include: {output_labels}')
