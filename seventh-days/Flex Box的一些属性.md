# flex 项的动态尺寸(flex元素)
	article {
	  flex: 1;
	}
	这是一个无单位的比例值，表示每个 flex 项沿主轴的可用空间大小。本例中，我们设置 <article> 元素的 flex 值为 1，这表示每个元素占用空间都是相等的，占用的空间是在设置 padding 和 margin 之后剩余的空间。因为它是一个比例，这意味着将每个 flex 项的设置为 400000 的效果和 1 的时候是完全一样的。
	article:nth-of-type(3) {
	  flex: 2;
	}
	你会看到第三个 <article> 元素占用了两倍的可用宽度和剩下的一样 — 现在总共有四个比例单位可用。 前两个 flex 项各有一个，因此它们占用每个可用空间的1/4。 第三个有两个单位，所以它占用2/4或这说是1/2的可用空间。

	article {
	  flex: 1 200px;
	}

	article:nth-of-type(3) {
	  flex: 2 200px;
	}
	指定 flex 的最小值。这表示“每个flex 项将首先给出200px的可用空间，然后，剩余的可用空间将根据分配的比例共享“。

# flex: 缩写与全写
	flex 是一个可以指定最多三个不同值的缩写属性：
		第一个就是上面所讨论过的无单位比例。可以单独指定全写 flex-grow 属性的值。
		第二个无单位比例 — flex-shrink — 一般用于溢出容器的 flex 项。这指定了从每个 flex 项中取出多少溢出量，以阻止它们溢出它们的容器。 这是一个相当高级的弹性盒子功能。
		第三个是上面讨论的最小值。可以单独指定全写 flex-basis 属性的值。

# 水平垂直居中
	align-items 控制 flex 项在交叉轴上的位置。
		默认的值是 stretch，其会使所有 flex 项沿着交叉轴的方向拉伸以填充父容器。如果父容器在交叉轴方向上没有固定宽度（即高度），则所有 flex 项将变得与最长的 flex 项一样长（即高度保持一致）。
		 center 值会使这些项保持其原有的高度，但是会在交叉轴居中。
		也可以设置诸如 flex-start 或 flex-end 这样使 flex 项在交叉轴的开始或结束处对齐所有的值。
	justify-content 控制 flex 项在主轴上的位置。
		默认值是 flex-start，这会使所有 flex 项都位于主轴的开始处。
		你也可以用 flex-end 来让 flex 项到结尾处。
		center 在 justify-content 里也是可用的，可以让 flex 项在主轴居中。
		space-around 是很有用的——它会使所有 flex 项沿着主轴均匀地分布，在任意一端都会留有一点空间。
		还有一个值是 space-between，它和 space-around 非常相似，只是它不会在两端留下任何空间。

# flex 项排序（flex元素）
	弹性盒子也有可以改变 flex 项的布局位置的功能，而不会影响到源顺序（即 dom 树里元素的顺序）。利用的order属性
	所有 flex 项默认的 order 值是 0。
	order 值大的 flex 项比 order 值小的在显示顺序中更靠后。
	相同 order 值的 flex 项按源顺序显示。所以假如你有四个元素，其 order 值分别是2，1，1和0，那么它们的显示顺序就分别是第四，第二，第三，和第一。
	第三个元素显示在第二个后面是因为它们的 order 值一样，且第三个元素在源顺序中排在第二个后面。

# flex可以嵌套，flex项仍然可以设置为flex容器，它的子元素就变为了flexbox

# 跨浏览器兼容性
	大多数浏览器都支持 弹性盒子，诸如 Firefox, Chrome, Opera, Microsoft Edge 和 IE 11，较新版本的 Android/iOS 等等。但是你应该要意识到仍旧有被人使用的老浏览器不支持 弹性盒子（或者支持，但是只是支持非常非常老版本的 弹性盒子）。