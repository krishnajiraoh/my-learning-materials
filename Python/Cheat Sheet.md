# General

	• Difference b/w integer division and float division
	• List comprehension:
        [ f(x) for i in list_a ]

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
