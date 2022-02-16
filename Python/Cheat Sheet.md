# General

	• Difference b/w integer division and float division
	- List not in list:
    	- cont_cols = [col for col in income_df.columns if col not in cat_cols]
	• List comprehension:
        [ f(x) for i in list_a ]
	• Read labels of classes into a list
		with open() as f:
			arr = f.read().splitline()

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
	• add dimension to array:
		• IMAGE_SHAPE = (100,100)	
		• IMAGE_SHAPE+(3,)
	• add dimension in the front:
		• gold_fish[np.newaxis, ,,, ]

# Sklearn:

	• Sklearn.metrics -> classification_report 
	• sklearn.metrics.pairwise -> Cosine_similarity 
    • Model_selection -> train_tset_split
		- Stratify=label_column => evenly split target column in train/test


# Matplot
	- plt.axis('off')

# Seaborn
	• Heatmap -> Confusion Matrix -> annot=True, fmt='d'


# Tensorflow

## layers

	- layers.Conv2D(16, 3, padding='same')
