#Compile
========
1. 전처리기(Preprocessor)
- - -
   Layer1
   C processor와 link Processor를 이용하여 Syntax적인 것들을 정리한다   
   즉 선언된 macro, define을 compile 전에 교체하고, syntax error가 있는 지 점검하여
   컴파일 전 단계까지 준비한다.   
   옵션 -E를 통해서 Preprocess를 할 수 있다.(*.c --> *.i)   
    
 2. 컴파일러(Compiler)
 3. 어셈블러(Assembler)
 4. 링커(linker)