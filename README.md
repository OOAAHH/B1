# B1a
这是一个合作项目
# Notes
## Update
### 20240629
新增标签v.2024.06.28，用于本周的最新的改动。图像文件在release的部分。
### 20240702

- 1. Fig2o和Fig2n都是WT的样本，正确是需要YMKOVSYMWT的样本，Fig2o（YMKOVSYMWT的GOup）和Fig2n（YMKOVSYMWT的火山图）请重新检查确认；

  - 这里的WT是control组 选择ym-ko颜色

- 2. Fig2n是ExtendFig1c的内容

- 3. ExtendFig1g（实际应该是ExtendFig1e）的FemaleGOenrichment上调通路的少了ATPmetabolicprocess；下调通路少了regulationofmitochondrialmembranepotential

- 4. Fig1o两个重复的样本有些基因的重复性差别很大，是否可以取平均值？还是必须放两个重复呢？#。修改需求，把所有的开放区域合并在一起进行绘图，
  - 第二个 需求，增加一列注释在图的左侧，这部分是注释文件的注释，标记了这个区域来自基因的那个部分
  - 第三个需求，热图的小box必须是正方形

  - 这里有两个版本，一个是在原来的基础上，直接合并样本出图 还是只有启动子，和原来的一致.第二个版本的是不只对启动子做图，UTR区等全部进行补充，在热图 的左侧增加注释，注意这里按照UTR 启动子 进行分组，顺序如下图，这里也是合并样本和不合并样本2张图!

- 5. Go富集的通路的P值 求-log10，
  - 做两种富集
    - （1）对所有差异基因进行富集，然后画图；
    - （2）对上下调的基因分别富集，然后画图。
  - 富集结果 按照2的 cutoff 分别生成diff down up的文件按照1.9的重新出图barplot

- 6. Fig1p:需求：将上述基因转录因子的p值以dot plot的形式画出来
  - 代码：参考MotifStack和https://guangchuangyu.github.io/cn/2018/03/dotplot-for-homer-motif/
  - 修改代码：Arial字体, 6号大小
  - 样本顺序：YM，OM，YF，OF
   - 实际上这里合并了样本，实验条件改为Common、Male、Female  
