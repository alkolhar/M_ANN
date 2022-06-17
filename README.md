# M_ANN
NTB elective module for Artificial Neural Networks<br>

In this project, an artistic style is to be adapted to an arbitrary photo.
Artificial neural networks based on VGG19 serve as a tool.
We want to test whether certain styles are better or worse suited for style transfer.
Furthermore, we want to use single layers of the VGG19 to better understand this algorithm.
Finally, we want to make a statement about whether neural networks will make humans obsolete as artists.
In this notebook, code fragments from StackOverflow and Kaggle can be found.
The notebook "13. Neural Style Transfer" by Christoph Würsch served mainly as a template.


We did a lot more than described here, so check out our [Jupyter Notebook](https://github.com/alkolhar/M_ANN/blob/2595306487930711596f89d223bc96ed60b6209c/ANN_Koller_Schreiber_final.ipynb)

## VGG 19
We load a VGG19 model for feature extraction and define below which layers we want to use.
As users of our time, we are fortunate to be able to use algorithms like the VGG19 with pre-trained weights just like that.
With our Keras model, we give a specific input, which then returns us the feature maps as output.
That means we don't necessarily use the whole VGG19 network.

## Base image
<p align="center">
    <img src='https://github.com/alkolhar/M_ANN/blob/77274759385c885c0c2eda8e7363b5c4975b283a/Data/images/Wasserauen-Seealpsee.jpg?raw=true' />
</p>

## Style image
<p align="center">
    <img src='https://github.com/alkolhar/M_ANN/blob/77274759385c885c0c2eda8e7363b5c4975b283a/Data/artworks/Pablo_Picasso/Pablo_Picasso_102.jpg?raw=true' />
</p>

## Compare Iterations
### Image after 100 iterations
<p align="center">
    <img src='https://github.com/alkolhar/M_ANN/blob/77274759385c885c0c2eda8e7363b5c4975b283a/CompareIteration/generated_iter_100.png?raw=true' />
</p>

### Image after 300 iterations
<p align="center">
    <img src='https://github.com/alkolhar/M_ANN/blob/77274759385c885c0c2eda8e7363b5c4975b283a/CompareIteration/generated_iter_300.png?raw=true' />
</p>

### Image after 1000 iterations
<p align="center">
    <img src='https://github.com/alkolhar/M_ANN/blob/77274759385c885c0c2eda8e7363b5c4975b283a/CompareIteration/generated_iter_900.png?raw=true' />
</p>
Objectively, it is hard to say when the result is considered "good".
However, it can be seen that from 300 to 1000 iterations no big change is noticeable anymore.
So for a good style image, 300 iterations are quite sufficient.

### Compare different style layers
<p align="center">
  <img src='https://github.com/alkolhar/M_ANN/blob/879846c501da07f47ddb5f7d7104452b94128c84/Data/layer4.png?raw=true' />
</p>
In the comparison we have found that `block4_conv1` has the strongest influence of all layers.
However, the comparison with all layers clearly shows that the other layers do not become invalid.
Unfortunately, we could not answer why block4 has the strongest influence.







