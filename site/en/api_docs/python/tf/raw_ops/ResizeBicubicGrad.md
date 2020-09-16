description: Computes the gradient of bicubic interpolation.

robots: noindex

# tf.raw_ops.ResizeBicubicGrad

<!-- Insert buttons and diff -->

<table class="tfo-notebook-buttons tfo-api nocontent" align="left">

</table>



Computes the gradient of bicubic interpolation.

<section class="expandable">
  <h4 class="showalways">View aliases</h4>
  <p>
<b>Compat aliases for migration</b>
<p>See
<a href="https://www.tensorflow.org/guide/migrate">Migration guide</a> for
more details.</p>
<p>`tf.compat.v1.raw_ops.ResizeBicubicGrad`</p>
</p>
</section>

<pre class="devsite-click-to-copy prettyprint lang-py tfo-signature-link">
<code>tf.raw_ops.ResizeBicubicGrad(
    grads, original_image, align_corners=(False), half_pixel_centers=(False),
    name=None
)
</code></pre>



<!-- Placeholder for "Used in" -->


<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Args</h2></th></tr>

<tr>
<td>
`grads`
</td>
<td>
A `Tensor` of type `float32`.
4-D with shape `[batch, height, width, channels]`.
</td>
</tr><tr>
<td>
`original_image`
</td>
<td>
A `Tensor`. Must be one of the following types: `float32`, `float64`.
4-D with shape `[batch, orig_height, orig_width, channels]`,
The image tensor that was resized.
</td>
</tr><tr>
<td>
`align_corners`
</td>
<td>
An optional `bool`. Defaults to `False`.
If true, the centers of the 4 corner pixels of the input and grad tensors are
aligned. Defaults to false.
</td>
</tr><tr>
<td>
`half_pixel_centers`
</td>
<td>
An optional `bool`. Defaults to `False`.
</td>
</tr><tr>
<td>
`name`
</td>
<td>
A name for the operation (optional).
</td>
</tr>
</table>



<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Returns</h2></th></tr>
<tr class="alt">
<td colspan="2">
A `Tensor`. Has the same type as `original_image`.
</td>
</tr>

</table>
