GenericLabelInterpolator
========================

.. image:: https://circleci.com/gh/fbudin69500/ITKGenericLabelInterpolator/tree/master.svg?style=svg
    :target: https://circleci.com/gh/fbudin69500/ITKGenericLabelInterpolator/tree/master

The basic idea of this generic interpolator for label images is to interpolate each label with an ordinary image interpolator, and return the label with the highest value. This is the idea used by the itk::LabelImageGaussianInterpolateImageFunction interpolator. Unfortunately, this class is currently limited to Gaussian interpolation. Using generic programming, our proposed interpolator extends this idea to any image interpolator. Combined with linear interpolation, this results in similar or better accuracy and much improved computation speeds on a test image.

A more detailed description can be found in the Insight Journal article::

  Schaerer, J., Roche, F., Belaroussi, B. \"A generic interpolator for multi-label images\".
    http://hdl.handle.net/10380/3506
    http://www.insight-journal.org/browse/publication/950
    December, 2014.

Since ITK 4.10.0, this module is available in the ITK source tree as a Remote
module.  To enable it, set::

  Module_GenericLabelInterpolator:BOOL=ON

in ITK's CMake build configuration.
