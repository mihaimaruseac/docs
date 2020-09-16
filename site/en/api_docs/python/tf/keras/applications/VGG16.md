description: Instantiates the VGG16 model.

<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.keras.applications.VGG16" />
<meta itemprop="path" content="Stable" />
</div>

# tf.keras.applications.VGG16

<!-- Insert buttons and diff -->

<table class="tfo-notebook-buttons tfo-api nocontent" align="left">
<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r2.3/tensorflow/python/keras/applications/vgg16.py#L45-L225">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td>
</table>



Instantiates the VGG16 model.

<section class="expandable">
  <h4 class="showalways">View aliases</h4>
  <p>
<b>Main aliases</b>
<p>`tf.keras.applications.vgg16.VGG16`</p>

<b>Compat aliases for migration</b>
<p>See
<a href="https://www.tensorflow.org/guide/migrate">Migration guide</a> for
more details.</p>
<p>`tf.compat.v1.keras.applications.VGG16`, `tf.compat.v1.keras.applications.vgg16.VGG16`</p>
</p>
</section>

<pre class="devsite-click-to-copy prettyprint lang-py tfo-signature-link">
<code>tf.keras.applications.VGG16(
    include_top=(True), weights='imagenet', input_tensor=None, input_shape=None,
    pooling=None, classes=1000, classifier_activation='softmax'
)
</code></pre>



<!-- Placeholder for "Used in" -->


#### Reference paper:


- [Very Deep Convolutional Networks for Large-Scale Image Recognition](
https://arxiv.org/abs/1409.1556) (ICLR 2015)

By default, it loads weights pre-trained on ImageNet. Check 'weights' for
other options.

This model can be built both with 'channels_first' data format
(channels, height, width) or 'channels_last' data format
(height, width, channels).

The default input size for this model is 224x224.

Caution: Be sure to properly pre-process your inputs to the application.
Please see <a href="../../../tf/keras/applications/vgg16/preprocess_input.md"><code>applications.vgg16.preprocess_input</code></a> for an example.

<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Arguments</h2></th></tr>

<tr>
<td>
`include_top`
</td>
<td>
whether to include the 3 fully-connected
layers at the top of the network.
</td>
</tr><tr>
<td>
`weights`
</td>
<td>
one of `None` (random initialization),
'imagenet' (pre-training on ImageNet),
or the path to the weights file to be loaded.
</td>
</tr><tr>
<td>
`input_tensor`
</td>
<td>
optional Keras tensor
(i.e. output of <a href="../../../tf/keras/Input.md"><code>layers.Input()</code></a>)
to use as image input for the model.
</td>
</tr><tr>
<td>
`input_shape`
</td>
<td>
optional shape tuple, only to be specified
if `include_top` is False (otherwise the input shape
has to be `(224, 224, 3)`
(with `channels_last` data format)
or `(3, 224, 224)` (with `channels_first` data format).
It should have exactly 3 input channels,
and width and height should be no smaller than 32.
E.g. `(200, 200, 3)` would be one valid value.
</td>
</tr><tr>
<td>
`pooling`
</td>
<td>
Optional pooling mode for feature extraction
when `include_top` is `False`.
- `None` means that the output of the model will be
the 4D tensor output of the
last convolutional block.
- `avg` means that global average pooling
will be applied to the output of the
last convolutional block, and thus
the output of the model will be a 2D tensor.
- `max` means that global max pooling will
be applied.
</td>
</tr><tr>
<td>
`classes`
</td>
<td>
optional number of classes to classify images
into, only to be specified if `include_top` is True, and
if no `weights` argument is specified.
</td>
</tr><tr>
<td>
`classifier_activation`
</td>
<td>
A `str` or callable. The activation function to use
on the "top" layer. Ignored unless `include_top=True`. Set
`classifier_activation=None` to return the logits of the "top" layer.
</td>
</tr>
</table>



<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Returns</h2></th></tr>
<tr class="alt">
<td colspan="2">
A <a href="../../../tf/keras/Model.md"><code>keras.Model</code></a> instance.
</td>
</tr>

</table>



<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Raises</h2></th></tr>

<tr>
<td>
`ValueError`
</td>
<td>
in case of invalid argument for `weights`,
or invalid input shape.
</td>
</tr><tr>
<td>
`ValueError`
</td>
<td>
if `classifier_activation` is not `softmax` or `None` when
using a pretrained top layer.
</td>
</tr>
</table>
