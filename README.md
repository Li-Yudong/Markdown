# Markdown
学习一次Markdown
# 这是一级标题
## 这是二级标题
### 下面三条-就可以画出一条线
---
~~删除线~~
--
###### 下面是斜体  
*试试*

> 前面有个杠杠
- 这是1
- 这是2
- 这是3
---
1. 1111
1. 2222
1. 3333
- [ ] 全面有框框
- [x] 选中的框框
---
[点击可进入百度](http://www.baidu.com)
---

### 看到没下面是一张图片
![这是一张图片地址](http://imgsrc.baidu.com/forum/pic/item/cefc1e178a82b9017ad72597738da9773912ef18.jpg)

###下面就可以贴代码
```
//创建最底部的collectionView
-(void)creatCollectionView{
    UICollectionViewFlowLayout *flowLayout = [[UICollectionViewFlowLayout alloc]init];
    flowLayout.minimumLineSpacing = 10;//最小行间距
    flowLayout.minimumInteritemSpacing = 4;//每个单元格的左右间距
    flowLayout.scrollDirection = UICollectionViewScrollDirectionVertical;//垂直方向滑动
    flowLayout.sectionInset = UIEdgeInsetsMake(10, 3, 10, 3);//区的周边间距(上、左、下、右)
    flowLayout.itemSize = CGSizeMake((UISCREEN_W-10)/2, (UISCREEN_W-10)/2*370/310 +100 +19-3+5);//单元格大小
    if (self.bottomCollectionView ==nil) {
        
        self.bottomCollectionView = [[UICollectionView alloc]initWithFrame:CGRectMake(0, UISCREEN_W*90/640 + 0.5 +UISCREEN_W*90/640, UISCREEN_W, UISCREEN_H-UISCREEN_W*90/640+0.5  -40- UISCREEN_W*90/640) collectionViewLayout:flowLayout];
        self.bottomCollectionView.backgroundColor = [UIColor colorWithHexString:@"#ebebeb"];
    }
    //设置代理
    self.bottomCollectionView.dataSource = self;
    self.bottomCollectionView.delegate = self;
    [self.view addSubview:self.bottomCollectionView];
    
    //注册
    [self.bottomCollectionView registerClass:[HomeBottomCollectionViewCell class] forCellWithReuseIdentifier:@"homeBottonCell"];
    [self.bottomCollectionView registerClass:[CustomCollectionReusableView class] forSupplementaryViewOfKind:UICollectionElementKindSectionHeader withReuseIdentifier:@"CustomCollectionReusableViewIdentifier"];
}

#pragma mark -
#pragma mark -UICollectionViewDelegate,UICollectionViewDataSource
- (NSInteger)collectionView:(UICollectionView *)collectionView numberOfItemsInSection:(NSInteger)section{
    
    return self.cellArray.count;
}
- (NSInteger)numberOfSectionsInCollectionView:(UICollectionView *)collectionView{
    return 1;
}

```

###看到没,下面就是表格
header 1 | header 2
---|---
row 冬 col 旭 | row 1 col 2 | 周一  | 周二
row 旭 col 爷 | row 2 col 2
row 旭 col 爷 | row 3 col 4 | 周三  | 周日


###看下面的表情大小可以搞哎
<img src="emoji/smile" width="16"/>
<img src="emoji/smile" width="17"/>
<img src="emoji/smile" width="18"/>
<img src="emoji/smile" width="19"/>
<img src="emoji/smile" width="20"/>
<img src="emoji/smile" width="21"/>
<img src="emoji/smile" width="19"/>
<img src="emoji/smile" width="18"/>
<img src="emoji/smile" width="17"/>
<img src="emoji/smile" width="16"/>


<i class="fa fa-heart"/>
<i class="fa fa-heart"/>
<i class="fa fa-heart"/>
<i class="fa fa-heart"/>
<i class="fa fa-heart"/>
<i class="fa fa-heart"/>
<i class="fa fa-heart"/>
<i class="fa fa-heart"/>
<i class="fa fa-heart"/>
<i class="fa fa-heart"/>
<i class="fa fa-heart"/>


<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>
<i class="icon ion-beer"/>



```math
E = mc^2 +QWWEWRER
```

###看下面的
```
graph LR
A-->B
```


```
sequenceDiagram
M->>V: 写内容
V->>C: 写内容
```
