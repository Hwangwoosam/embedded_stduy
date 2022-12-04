#Memory MAP
====================
- - -   
1. Symbol      
 Layer1   
 Symbol이란 Linker가 알아볼 수 있는 기본 단위이며, Link를 한 후에는 자신만의 주소를 갖게되는 특별한 단위이다.   
 * Symbol이란, linker가 알아 볼 수 있는 기본 단위이며, Link를 한 후에는 자신만의 주소를 갖게된다. Symbol의 이름은 그 symobl이 갖는 메모리 영역의 시작 주소를 가리키는 Linker만의 pointer이며 이는 전역변수의 이름이나, 함수 이름 등으로 한다.   
  * Linker를 위해서 ELF object file 내에는 Symbol table 이라는 것을 두는데, source code에 의하여 참조되는 Symbol들의 이름과 위치 정보가 들어있으며, 다른 file에서 정의된 Symbol 사용할 경우에는 그 해당 파일에 Symbol이 없기 때문에 linker를 통해서 처리하여 다른 파일에 있는 Symbol을 연결하여 사용할 수 있도록 한다.   
  이때 Symbol은 memory에 실제로 적재되지 않고 Linker만 이 Symbol을 참조 및 주소로 변환해서 binary로 만든다.  
- - -
2. RO,RW,ZI   
Layer1   
RW는 Read-write 로서, 초기값이 있는 전역변수를 의미하고,ZI는 zero-initialized로서, 초기값이 0인 전역변수를 의미하고, 마지막으로 RO는 Read-only로서 수정이 불가능한 const 전역변수와 text인 code를 의미합니다. 단 전역변수중 const로 선언된 data들도 포함이 된다.   
- - -
