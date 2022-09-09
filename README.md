# CSS-Grid


repeat : 행/열의 크기 정의 반복

 

.container{
    grid-template-columns: 100px 100px 100px 100px 100px 100px 100px 100px 100px;
    grid-template-columns: repeat(9, 100px);
}
 

 

minmax : 행/열의 '최소/최대 크기' 정의

 

.container{
    grid-template-columns: minmax(100px,1fr) minmax(200px, 1fr);
    /*첫번째열 최소최대, 두번째열 최소최대*/
}
 

 

fit-content : 행/열의 크기를 그리드 아이템이 포함하는 콘텐츠 크기에 맞추되,

내용의 최대 크기를 설정

minmax(auto,max-content)와 유사

 

.container{
    grid-template-columns: fit-content(300px) fit-content(300xpx);
}
 

 

Grid Units 단위
 

fr(fractional unit) : 사용 가능한 공간에 대한 비율을 의미

ex) 1fr 1fr = 1대1

 

 

min-content : 그리드의 아이템이 포함하는 콘텐츠의 최소 크기를 의미

max-content : 그리드의 아이템이 포함하는 콘텐츠의 최대 크기를 의미

 

 

예제

.container{
    grid-template-columns: min-content 1fr;
    /*해당 콘텐츠의 열의 너비는 최소한 작게 설정, 나머지 콘텐츠는 1fr 씩 할당*/
}
 

 

auto-fill, auto-fit  : 행/열의 개수를 그리드 컨테이너 및 행/열 크기에 맞게 자동으로(암시적으로) 조정

repeat 함수와 같이 사용, 개수가 명확할 필요가 없거나 명확하지 않을 경우 유용(반응형 그리드)

 

 


 

넘치는 문제 발생

 


 

 

※ auto-fill 과 auto-fit의 차이점

 

남는 공간이 있을 때 auto-fill : 남는 공간 그대로 유지

                           auto-fit : 남는 공간 축소
