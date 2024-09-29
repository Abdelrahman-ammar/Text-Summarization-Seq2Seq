# Text Summarization Seq2Seq model using Attention

A text summarizer project (built with tensorflow), where it utilizes the encoder decoder architecture of the Seq2Seq models to accomplish the summarization process , although the summarization is 3 to 4 words max, but it accomplishes the Abstractive summarization type of task , where it generates new words for the summarization rather than using the words that came with data.

## Table of Contents

- [Information about the project](https://github.com/Abdelrahman-ammar/Text-Summarization-Seq2Seq/blob/master/README.md#What-is-this-project)

- [Project Structure](https://github.com/Abdelrahman-ammar/Text-Summarization-Seq2Seq/blob/master/README.md#Project-Structure)

### Information about the Project

This project summarizer model is trained on Amazon reviews dataset , you can get the data from here : [Kaggle/Datasets](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews) , the model accuracy doesn't exceed 70% , but it really gives amazing results

## Project Structure

- [Notebooks](./Notebooks/) : Project Notebooks where training and testing has been done

- [Models](./Models/) : The encoder , decoder and the entilre model files is there , there is also another version of the model but only weights is saved , you can use `load_weights` function from tensorflow to lload the model weights into your model structure

- [Tokenizers](./Tokenizers/) : Essential tokenizers could be found here

- [Deployment](./Deployment/) : The Deployment was made using 2 methods , Docker file and Flask application

  - [Dockerfile](./Deployment/Dockerfile) : build the docker file from here using the command `docker build -t text_summarizer:v1.0 .` (notice that you should be placed in the deployment directory for the command to work) , then you could run the container using `docker run -it -p 9002:9002 text_summarizer:v1.0` ,by doing this you could send a request , curl a post request on this specific port.

  - [Flask App](./Deployment/app.py) : or you can just `pip install -r requirements.txt` and then use `python app.py` to run the flask application

# Demo:

---

![Prediction Result](./assets/image1.png)

![Postman Flask Docker](./assets/image.png)
