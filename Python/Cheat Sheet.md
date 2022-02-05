# General

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
	• Apply function in an array:
		• y_pred = (y_pred < 0).astype(int)


# Sklearn:

	• Sklearn.metrics -> classification_report
    • Model_selection -> train_tset_split
