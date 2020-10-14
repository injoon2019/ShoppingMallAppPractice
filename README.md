# Shopping Mall App Example - Parayo
- 책 : [코틀린으로 쇼핑몰 앱 만들기](http://www.yes24.com/Product/Goods/89913111?scode=029)

<img width = "300" height = "400" src = "https://user-images.githubusercontent.com/52276038/84369198-75437c80-ac11-11ea-8e75-0017559b81e4.png"> 

- 책에 나온 [MVP(Minumum Viable Product)](https://ko.wikipedia.org/wiki/%EC%B5%9C%EC%86%8C_%EA%B8%B0%EB%8A%A5_%EC%A0%9C%ED%92%88) 프로젝트를 완성 시킨 간단한 중고 거래 애플리케이션 & 서버 API

### 2020.10 기준으로 버전 차이가 나거나 에러가 나는 부분 및 책에서 설명 놓친 부분들 표기
------

53p 스프링과 연결되지 않을 경우
 p.57과 부록에 나오는 데이터 베이스 연결을 하지 않아서 그렇다 (책의 순서 문제)
 부록에서 나오는 application.yml 파일 추가는 p.59에 있다.
 
------

76p 에러나는 경우
 implementation "androidx.constrainlayout:constraintlayout:2.0.0-beta2" -> implementation "androidx.constrainlayout:constraintlayout:2.0.0-beta4"
 
------

136p "PreferenceManager depreceated"뜨는 경우
 큰 문제 없지만 build.gradle( Module: App) implementation 'androidx.preference:preference:1.1.1'추가하고
 package com.example.parayo.common 에서 import androidx.preference.PreferenceManager 로 교체
 
------

140p 에러나는 경우
책에 SigninAcitivity의 onCreate가 빠져있다.

    override fun onCreate(savedInstanceState: Bundle?){
        super.onCreate(savedInstanceState)

        SigninActivityUI(getViewModel())
            .setContentView(this)
    }
    
------
141p 에러나는 경우
Server Application: 
 url: jdbc:mysql://부록 따라서 aws에서 데이터베이스 만들고 엔드포인트:포트번호/스키마이름

------
148p 에러나는 경우

navigationView 파트 에러나는 경우: 

navigationView = navigationView{
 ///
} 이 아니라
변수 선언하지 하지 않고 바로
navigationView{
}

------
이쯤에서 실제 안드로이드 디바이스랑 연결해봤다. 인터넷 연결을 같은 와이파이로 하고 방화벽을 꺼준다. 그리고 네트워크를 개인으로 돌려준다 
그리고 ApiGenerator에서 const val HOST = "http://10.0.2.2:8080" 대신 const val HOST = "http://172.22.77.134:8080" 컴퓨터의 주소를 넣어준다. ipconfig로 쉽게 ipv4 찾을 수 있다. 

------
157p 에러나는 경우
ProductMainActivity에서
    private val ui by lazy { ProductMainUI(getViewModel())} 변수 선언을 먼저 해놔야하는데 책에 안나와있다
    
------


 추가할 것 sdsdsd
  
