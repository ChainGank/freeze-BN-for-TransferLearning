# freeze BatchNormalization layer for Transfer Learning
The problem is "The BatchNormalization layer of Keras is broken" which can be seen in the blog bellow:
http://blog.datumbox.com/the-batch-normalization-layer-of-keras-is-broken/

Briefly, it can be described as "how to use moving_mean&&var(pre-trained model's dataset) instead of the mean&&var caculated by mini-batch during finetuning".

To address the problem above, I use tensorflow2.0 keras api to gain expected result in my test.

The main api is tf.keras.backend.learning_phase_scope() which can be seen bellow:
https://www.tensorflow.org/versions/r2.0/api_docs/python/tf/keras/backend/learning_phase_scope
