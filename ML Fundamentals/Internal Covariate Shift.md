## Internal Covariate Shift
Internal Covariate Shift가 Gradient Vanishing이나 Exploding 같은 문제를 만든다
> Training 분포와 Test 분포의 차이가 위와 같은 문제를 일으킨다

Sol
- 각 layer마다 normalization하는 Batch Norm 실행

> Batch norm으로 계속 normalization하면 activation func의 non linearity를 잃게 되는데 이를 완화시켜주기 위해 사용하는게 베타와, 감마
