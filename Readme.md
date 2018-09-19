# HElib Revisited 

## Current

- NewBlockMatMul1D를 이용하려고 했는데, 뭔가 잘 안돼서 Original과 우리 것(mod_HElib)으로 디렉토리 분리

- mod_HElib의 BlockMatMul1D는 native에 따른 multiplication 분기들이 없고, 
Our bsgs를 옵션(force_block_bsgs)으로 선택할 수 있게 했음

- Exec의 멤버로 k_s와 g(=sqrt(D*d))를 가지게 되었으며 k_s는 알아서 찾도록 함

## TODO

### Writing

- 일단 제가 착수하고 분배하겠습니다

### Current 연장

- ProcessDiagonal2 함수

- (굳이 해야 하나 싶지만) D < d 인 경우

- BlockMatMul1D 생성할때 native를 아예 볼 필요가 없도록 할수도 있을 것 같은데, 굳이 안 해도 될것 같음.

- No Hoisting이지만 Key는 적당히 있는 경우의 BSGS 구현

### Summation 나누기

- 원래 있는 precon class들로 처리할 수 있는지 확인

- 아니면 새로 만들기
