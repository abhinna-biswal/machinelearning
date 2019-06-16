TensorFlow supports different ways of loading datasets, depending on how much data you are dealing with. 
The simplest method is to preload all your data into memory and pass it to TensorFlow as a single array. To do this, you just write plain Python code to load your data. There's nothing TensorFlow specific. 

The second more complicated option is to write code that feeds your training data step-by-step into TensorFlow as TensorFlow requests it. This gives you more control over when the data is loaded but it requires you to manage everything yourself. 

The third option is to set up a custom data pipeline in TensorFlow. This is the best option when you are working with enormous datasets like millions of images. A data pipeline allows TensorFlow to manage loading data into memory itself as it needs it. 

It is recommended choosing the simplest solution that works for your project. If your dataset fits in the memory, preload the entire dataset. It require the least amount of code. But if your dataset is huge, then set up a data pipeline. It's the most efficient way to work with large datasets. Data pipelines are especially common for image-based datasets since images take up a lot of the memory. Just think of building a data pipeline as additional complexity you only need to add if other solutions won't work. In this project, we'll be using preloading to build a neural network, since our data will fit into memory.
