# Install docker:

    docker pull tensorflow/serving

# Run the docker TF serving image in the interactive mode:

    docker run -it -v {path_to_model_dir}:/tf_serving -p 8605:8605 --entrypoint /bin/bash tensorflow/serving
    ls -ltr tf_serving

# Automatically pick & serve the latest version of the model in saved_models:

    tensorflow_model_server --rest_api_port=8605 --model_name=spam_classification_model --model_base_path=/tf_serving/saved_models

Open "http://localhost:8605/v1/models/spam_classification_model" in a browser

# Postman

### Request : 

    http://localhost:8605/v1/models/spam_classification_model:predict
### Body : 

    {
        "instances": [
            "Let's meet for dinner tomorrow",
            "You are awarded a SiPix Digital Camera! call 09061221061 from landline. Delivery within 28days. T Cs Box177"
        ]
    }

# Serve all the versions of a model via a config file

    tensorflow_model_server --rest_api_port=8605 --model_config_path=/tf_serving/model_a.config --allow_version_labels_for_unavailable_models

    Inspect : http://localhost:8605/v1/models/spam_classification_model
    Request : http://localhost:8605/v1/models/spam_classification_model/versions/2:predict

# Serve with model labels {beta , production}

    tensorflow_model_server --rest_api_port=8605 --model_config_path=/tf_serving/model_b.config --allow_version_labels_for_unavailable_models

# Monitoring and other configurations

https://www.tensorflow.org/tfx/serving/serving_config
