# 2 types of model architecture:
Ref <a href="https://becominghuman.ai/sequential-vs-functional-model-in-keras-20684f766057>Article</a>
	• Sequential
	• Functional
		○ more flexibility
		○ For ex, in sequential model you can only stack one layer after another, while in functional model you can connect a layer to literally any other layer.


## Sequential:

    model_seq = Sequential()
    model_seq.add(Dense(5, activation='sigmoid', input_shape (X_train.shape[1],)))
    model_seq.add(Dense(4, activation='sigmoid'))
    model_seq.add(Dense(10, activation='softmax'))

## Functional:

    input1 = Input(shape=(X_train.shape[1],))
    hidden1 = Dense(5, activation='sigmoid')(input1)
    hidden2 = Dense(4, activation='sigmoid')(hidden1)
    output = Dense(10, activation='softmax')(hidden2)
    model_func = Model(inputs=input1, outputs=output)

# Input Pipeline:

<p align="center">
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Tensorflow/.images/input_pipeline.png" height=300 />
</p>

    tf.data.Dataset : 
        • Load data in batches
        • Filter data
            ○ tf_dataset.filter(filter_func)
        • Scale:
            ○ tf.dataset_map(lambda x: x/255)




