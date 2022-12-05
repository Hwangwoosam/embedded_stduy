#Mapfile
==========
- - -
1. 구성은 Image Symbol Table, Memory Map of the image, Image component size, 전체 Layout으로 이루어져 있다.   
* Image Symbol Table: Linker가 만들어낸 Symbol과 주소 그리고 Region
    * User가 만들어낸 Symbol과 주소,Size 그리고 속해 있는 object Memory Map of the image
    * Scatter Loading에 맞춘 Region에 따라 구획을 표시
    * 주소와 size,type 그리고 section과 object 표시
    * 각 object 또는 library에 대한 RO,RW,ZI가 차지하는 size
    * 전체적인 Memory에 RO,RW,ZI가 비율 표시
- - -