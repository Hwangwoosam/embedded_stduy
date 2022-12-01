#변수의 Scope
==============
1. auto
- - -
    Layer1   
    auto(auto Local) 변수란 이 변수들의 동작 범위가 자신이 선언된 함수 또는 Block 안 영역에서 동작한다.   
    즉 그 함수의 수행이 모두 종료되면 return과 동시에 사라저 버린다.   

2. extern
- - -
    Layer1   
    보통 Global 변수로 불리는 유형으로 auto local 변수 유형과 다른 점은 변수가 정의 된 위치이다.   
    이런 유형의 변수들은 함수의 안쪽이 아닌 함수 바깥쪽에 정의되며 이 변수가 선언된 파일의 전체에 사용될 수 있다.   
    다른 파일에서 선언된 변수를 사용하고자 하려면 extern <type> name 을 선언하면 사용할 수 있다.   

3. static
- - -
    Layer1   
    static 유형의 변수들은 local static과 global static 유형으로 나누어 진다.   
    Local 변수 앞에 static이 선언될 경우에는 자신이 선언된 함수나 Block이 종료되더라도 그 값을 저장하고 있으며,   
    Global 변수 앞에 static이 선언될 경우에는 다른 파일에서 extern을 선언하여 사용할 수 없도록 한다.   

4. volatile
- - -
    Layer1
    volatile을 변수 앞에 선언하여 사용한다면 compiler가 컴파일하는 과정에서 optimization을 하지 않는다.   
    Device Driver를 설계할 때 많이 사용하는데 Memory mapped I/O의 경우에 가은 주소에 다른 값들을 연속해서 쓰게되기 때문이다.