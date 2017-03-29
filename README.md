# Laplacian-preserving Neural Style Transfer

An image Laplacian loss is imposed to the original neural style transfer method, so that the produced image better preserves fine details of the original content image.

Check [https://github.com/anishathalye/neural-style] for original documentation.

The only extra command line argument:

`--content-lapweight` (default: 100)

An example command line:

`python neural_style.py --content megan.jpg --styles spring.jpg --output megan_spring.jpg --content-weight 50`
