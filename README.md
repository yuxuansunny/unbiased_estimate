# unbiased_estimate
demonstrate sample variance unbiased
>> % %%无偏估计验证
% %%总共容量
 M=7;
% %%样本容量
 N=2;
% %填充第一列
% %填充循环次数
for t=1:M^(N-1)
    for i=1:M
        Sample1((i-1)*M^(N-1)+t) = i;
     end
 end
% Sample1'
% %填充第二列
 for t=1:M
     for i=1:M
         Sample2(M*(t-1)+i) = i;
     end
 end
% Sample2'
 Sample = [Sample1',Sample2']
 sLenght = length(Sample);
 for s=1:sLenght
     subSample = Sample(s,:)
     stdSample(s) = var(subSample,1);
 end
 stdSample =  var(Sample');
 stdSampleE = sum(stdSample)/M^N
 Total = 1:M;
 stdTotalE = var(Total,1)

 


Sample =

     1     1
     1     2
     1     3
     1     4
     1     5
     1     6
     1     7
     2     1
     2     2
     2     3
     2     4
     2     5
     2     6
     2     7
     3     1
     3     2
     3     3
     3     4
     3     5
     3     6
     3     7
     4     1
     4     2
     4     3
     4     4
     4     5
     4     6
     4     7
     5     1
     5     2
     5     3
     5     4
     5     5
     5     6
     5     7
     6     1
     6     2
     6     3
     6     4
     6     5
     6     6
     6     7
     7     1
     7     2
     7     3
     7     4
     7     5
     7     6
     7     7


subSample =

     1     1


subSample =

     1     2


subSample =

     1     3


subSample =

     1     4


subSample =

     1     5


subSample =

     1     6


subSample =

     1     7


subSample =

     2     1


subSample =

     2     2


subSample =

     2     3


subSample =

     2     4


subSample =

     2     5


subSample =

     2     6


subSample =

     2     7


subSample =

     3     1


subSample =

     3     2


subSample =

     3     3


subSample =

     3     4


subSample =

     3     5


subSample =

     3     6


subSample =

     3     7


subSample =

     4     1


subSample =

     4     2


subSample =

     4     3


subSample =

     4     4


subSample =

     4     5


subSample =

     4     6


subSample =

     4     7


subSample =

     5     1


subSample =

     5     2


subSample =

     5     3


subSample =

     5     4


subSample =

     5     5


subSample =

     5     6


subSample =

     5     7


subSample =

     6     1


subSample =

     6     2


subSample =

     6     3


subSample =

     6     4


subSample =

     6     5


subSample =

     6     6


subSample =

     6     7


subSample =

     7     1


subSample =

     7     2


subSample =

     7     3


subSample =

     7     4


subSample =

     7     5


subSample =

     7     6


subSample =

     7     7


stdSampleE =

     4


stdTotalE =

     4
