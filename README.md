# Line-search-golden-section-search
一维搜索——黄金分割法

## 1.算法原理
设目标函数为F(x)，则黄金分割算法的实现过程如下：  
(1)给定初始区间[a1,b1]，精度要求tol>0，黄金分割系数T=0.618，k=1。  
(2)令c1=a1+(1-T)(b1-a1)，d1=b1-(1-T)(b1-a1)，计算Fc=F(c1)，Fd=F(d1)。  
(3)若b(k+1)-a(k+1) >= tol，转到步骤(4),否则停止搜索，得到的结果为(a(k+1)+b(k+1))/2。  
(4)若Fc<Fd，转到(5);否则转到(6)。  
(5)a(k+1)=a(k);b(k+1)=d(k);d(k+1)=c(k),Fd=Fc;令c(k+1)=a(k+1)+(1-T)(b(k+1)-a(k+1));计算Fc=F(c(k+1)),转到(7)。  
(6)a(k+1)=c(k);c(k+1)=d(k);b(k+1)=b(k),Fc=Fd;令d(k+1)=b(k+1)- (1-T)(b(k+1)-a(k+1));计算Fd=F(d(k+1)),转到(7)。  
(7)置k=k+1;返回(3)。  
  
## 2.算法流程图
![fault](https://github.com/jnswx/Line-search-golden-section-search/blob/master/picture.png)
