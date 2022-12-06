#ARM_MODE
================
- - -
1. MODE
Layer1   
    ARM의 Mode는 총 7개로 1개의 Normal mode(User mode)와 6개의 Privileged mode(System, FIQ, IRQ, Supervisor, Abort, Undef mode)로 이루어져 있다.Privileged mode 간의 모드변경이 가능하며 IRQ나 FIQ등의 interrupt의 사용 가능 유무를 직접 설정할 수 있다.   

* User mode : Normal Program excution mode로 Application Program으로 User Task나 Application을 수행 할때의 동작모드로 모든 동작모드 중 유일하게 non-Privileged mode 이다. User Mode는 메모리, I/O 장치와 같은 시스템 자원을 사용하는데 제한을 두어 사용자의 실수를 방지한다. 다른 모드(SVC)로 이동하기 위한 방법으로는 소프트웨어 인터럽트를 발생시킨다.또한 User mode에서 System mode로 변환은 가능하지 않다.   
* FIQ(Fast IRQ): 2개의 인터럽트 소스 중 아주 빠르게 인터럽트를 처리할 수 있도록 구성된 모드이다. 빠른 처리를 위해서 Exception Vector에서도 최하단에 존재하고 별도의 레지스터를 소유한다.   
* IRQ(Interrupt Request): 일반적으로 사용되는 Interrupt로 외부 장치에서 요청되는 하드웨어적인 IRQ의 발생에 의해 ARM Core는 IRQ모드로 전환하고 Interrupt를 처리한다.   
* SVC(Supervviser): 대부분의 시스템 자원을 자유롭게 관리할 수 있는 동작모드로 주로 커널이나 디바이스 드라이버를 처리할 때 동작되는 모드이다. Power on, Reset, SWI가 발생할 경우에 해당 모드로의 변환이 이루어진다.   
* Abort: 메모리에서 명령을 읽거나 데이터를 읽거나 쓸때 오류가 발생할 때 Abort Mode로 전환하여 오류를 처리한다. 커널등의 패닉시 Abort Mode로 전환되어 스택 내용이 전달됨을 알 수 있다.   
* Undefined: 명령어를 읽어 실행하고자 하나 읽어온 명령이 디코더에 정의되어 있지 않은 명령인 경우 발생되는 오류를 처리하는 모드이다.   
* System: User Mode와 동일한 Register를 사용하고 동일한 용도로 사용된다. User Mode와의 차이점은 User mode에서는 device등의 자원을 사용하는데 제한이 있다.   
- - -