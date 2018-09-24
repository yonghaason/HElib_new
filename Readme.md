# HElib Revisited 

## Current

- mod_HElib의 BlockMatMul1D는 native에 따른 multiplication 분기들이 없고, 
Our bsgs를 옵션(force_block_bsgs)으로 선택할 수 있게 했음

- 09/24: ProcessDiagonal 함수들 오버라이딩이 잘 안돼서, PAlgebra, EncryptedArray 수준에서 Frobenius shifts를 찾아서 가지고 있도록 하고, ProcessDiagonal의 인자는 원래처럼 가져오도록 했습니다. 

e.g) 바뀐 파일들: EncryptedArray, PAlgebra, matmul.

## TODO

### Writing

- 일단 제가 착수하고 분배하겠습니다

- 09/24: 아직 하나도 안바뀜

### Current 연장

- ProcessDiagonal2 함수

- (굳이 해야 하나 싶지만) D < d 인 경우

- DONE : BlockMatMul1D 생성할때 native를 아예 볼 필요가 없도록 할수도 있을 것 같은데, 굳이 안 해도 될것 같음.

- DONE : No Hoisting이지만 Key는 적당히 있는 경우의 BSGS 구현

- 09/24: Key 생성은, Test_matmul.cpp 파일 중간에 add1DMatrices 등등부터 시작해서 좀 뜯어보면 되지 않을까 싶은데 좀더 찾아보겠습니다.

### Summation 나누기

- 원래 있는 precon class들로 처리할 수 있는지 확인

- 아니면 새로 만들기
