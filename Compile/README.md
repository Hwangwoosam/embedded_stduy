#Compile
<img src="./flow.jpg" width="450px" height="350px">
========
1. 전처리기(Preprocessor)
- - -
   Layer1   
   C processor와 link Processor를 이용하여 Syntax적인 것들을 정리한다   
   즉 선언된 macro, #define,#include 등을 compile 전에 교체하고, syntax error가 있는 지 점검하여 컴파일을 할 수 있는 단계까지 준비한다.   
   include를 선언하는 단계에서 " ", < > 의 차이점은 <>는 Compiler에 미리 설정된 path로 부터 Header파일을 찾아가는 것이고, " " 는 컴파일 하는 컴파일중인 디렉토리를 우선적으로 Header 파일을 찾는다.없을시에 Predefine에서 검색을 한다.   
   여러개의 파일이 하나의 헤더파일을 접근할 경우 #ifndef,#endif를 통해서 문제를 해결 할 수 있다.   
   옵션 -E를 통해서 Preprocess를 할 수 있다.(*.c --> *.i)   
   옵션 -I를 통해서 컴파일 중 include path를 설정할 수 있으며 -J옵션을 통해 Compiler Default include path를 설정할 수 있다.     
    
 2. 컴파일러(Compiler)
 - - -
   Layer1   
   High level language를 low level language로 변환한다.   
   옵션 -S 를 사용하여 *.s파일 형식으로 어셈블리(low level language)로 생성할 수 있다.   
 3. 어셈블러(Assembler)
 4. 링커(linker)
 5. ect
 - - -
   Layer1   
   Cross Compile: Source code를 다른 CPU에서 동작할 수 있도록 Target CPU에 맞도록 Compile 하는 것을 말한다.   