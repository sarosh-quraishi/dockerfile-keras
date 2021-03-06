# dockerfile-keras

Dockerized [Keras] with [TensorFlow].

## Get Started

Build an keras and keras+jupyter containers:
```sh
docker build -t keras:cpu --build-arg http_proxy=$http_proxy --build-arg https_proxy=$https_proxy  .
```

```sh
docker build -t keras_jupyter:cpu --build-arg http_proxy=$http_proxy --build-arg https_proxy=$https_proxy ./jupyter
```


Run an example from keras examples directory within jupyter notebook:

```sh
docker run -d -p 8888:8888 -v /home/sarosh/Documents/keras/examples:/keras_examples -e KERAS_BACKEND=tensorflow -e http_proxy=$http_proxy -e https_proxy=$https_proxy keras_jupyter:cpu

```

Just browse localhost:8888 and write code with Keras!


[Keras]: http://keras.io/
[Theano]: http://deeplearning.net/software/theano/
[TensorFlow]: https://www.tensorflow.org/
[Keras Backend]: http://keras.io/backend/
