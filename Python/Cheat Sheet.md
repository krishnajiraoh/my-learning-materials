# General

	• Difference b/w integer division and float division
	• List comprehension:
        [ f(x) for i in list_a ]

# Dictonary
	- Looping
		for a,b in dict_name.items()

# Pandas:

	• Read_csv
		• header=None -> auto idx col names
	• Pd.get_dummies() -> one hot encoding
		• drop_first=True => for binary
	• Lambda function
		• df['col].apply(lambda x : f(x))
	• Sampling
		• df.sample(count)


# Numpy:

	• Unique counts
		• np.unique(y_pred, return_counts=True)
	• Reshape -> arr.reshpae(new_shape)
		• y_train.reshape(-1,)  => -1 refs mpt to drop the dimension
	• Apply function in an array:
		• y_pred = (y_pred < 0).astype(int)
	• argmax -> get the index of max value
		• np.argmax(arr)

# Sklearn:

	• Sklearn.metrics -> classification_report
    • Model_selection -> train_tset_split


# Matplot
	- plt.axis('off')

# Seaborn
	• Heatmap -> Confusion Matrix -> annot=True, fmt='d'


# Tensorflow

## layers

	- layers.Conv2D(16, 3, padding='same')
