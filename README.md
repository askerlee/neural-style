# Laplacian-preserving Neural Style Transfer

An image Laplacian loss is imposed to the original neural style transfer method, so that the produced image better preserves fine details of the original content image.

Check [https://github.com/anishathalye/neural-style] for original documentation.

The only extra command line argument:

`--content-lapweight` (default: 100)

An example command line:

`python neural_style.py --content megan.jpg --styles spring.jpg --output megan_spring.jpg --content-weight 50`

## Comparison with original method

Example 1:

![megan](examples/megan/megan.jpg |width=250)

![spring](examples/megan/spring.jpg)

The original method produces such an image:

![megan_spring500](examples/megan/megan_spring500.jpg)

A lot of unpleasing artifacts are visible, e.g. there is a big blob on Megan's face.

With the Laplacian loss constraint, the produced image becomes:

![megan_spring510](examples/megan/megan_spring510.jpg)

Example 2:

The style image is from Prisma.

![xiuchao](examples/xiuchao/xiuchao.jpg)

![comic](examples/xiuchao/comic.jpg)

The original method produces:

![xiuchao_comic500](examples/xiuchao/xiuchao_comic500.jpg)

Again, the image, especially the face, is fragmented.

With the Laplacian loss constraint, the produced image becomes much more smooth, although less "stylish":

![xiuchao_comic510](examples/xiuchao/xiuchao_comic510.jpg)
