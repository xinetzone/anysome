#### 个人 Python 项目

1 自制数据集 X：https://github.com/DataLoaderX/datazone

- Situation: 创建自定义的数据集以适用于不同的深度学习框架。
- Task: 设计一个 API 将 MNIST, Cifar 10, cifar100, Fashion-MNIST 封装为数据集 X，并将 X 其保存为 HDF5 格式。
- Action: 借助 Python 的 Bunch 结构将数据进行管理，将图片以 Numpy 的形式进行封装，之后可以直接以数组的形式获取图片。将各个数据集的标签名称、数值标签以及数据集的源网站都封装进入数据集 X。
- Result: HDF5 是一个可以高效的存储和读取的数据结构，不仅仅支持 Python，也支持 Matlab 获取(https://yq.aliyun.com/articles/614332?spm=a2c4e.11155435.0.0.30543312vFsboY)。数据 X 被我被我放在了多个平台（博客园，云栖社区，简书）进行分享都获得超过 400 的阅读量。

2 改写 cocoapi：https://github.com/Xinering/cocoapi

- Situation: 利用 Python 的特性对原微软的 api 进行改写使其支持直接读取压缩文件而直接跳过繁琐的解压和重写工作。
- Task：利用 Python 的类的继承机制改写 cocoapi，并命名为 cocoz，令 cocoz 可以更加方便的处理 COCO 数据集，并且还可以使用 cocoz 来处理类似于 COCO 数据集的形式的数据集（https://nbviewer.jupyter.org/github/XinetAI/CVX/blob/master/Notebook/dog_cat_gluon.ipynb）。
- Action：创建 cocoz.py 来完成预期任务，并创建 pycocoZDemo.ipynb  和 pycocoZEvalDemo.ipynb 来说明如何使用 cocoz.py。
- Result：将 cocoz 的创建与使用分享在博客园（https://www.cnblogs.com/q735613050/p/8969452.html） 已经获得 15816 的阅读量（2019/3/22）。与北京源智天下科技有限公司签约写关于如何动手实现计算机视觉的书。

3 创建处理脱机和在线手写汉字库的 API：https://github.com/DataLoaderX/datasetsome

- Situation：中科院自动化研究所在 2007-2010 年间收集的 CASIA-HWDB 和 CASIA-OLHWDB 数据集。该数据集的学术研究的用途包括：手写文档分割、字符识别、字符串识别、文档检索、书写人适应、书写人鉴别等。但是直接使用该数据库有点困难，需要详细阅读官方提供的文档说明，并且辅以各种编码知识。
- Task：简化手写汉字库的读取过程，令数据的载入和读取更加人性化。
- Action：创建 xhw.py 实现数据的封装，以 HDF 格式直接获取手写汉字的图片和特征信息。
- Result：在慕课网分享该 API 获取超过 1000 的阅读量。
