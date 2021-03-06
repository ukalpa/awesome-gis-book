

四键具有几个有趣的属性。首先，四键的长度（位数）等于相应图块的详细程度。其次，任何图块的四键以其父图块（上一级包含的图块）的四键开头。如下例所示，图块2是图块20到23的父级，图块13是图块130到133的父级：

![](https://docs.microsoft.com/en-us/bingmaps/articles/media/5cff54de-5133-4369-8680-52d2723eb756.jpg)

最后，四键提供了一个一维索引键，通常可以保留XY空间中图块的接近度。换句话说，两个具有附近XY坐标的图块通常具有相对靠近的四键。这对于优化数据库性能非常重要，因为通常以组为单位请求相邻的切片，并且希望将这些切片保留在同一磁盘块上，以最大程度地减少磁盘读取次数。

## 参考

https://docs.microsoft.com/en-us/bingmaps/articles/bing-maps-tile-system