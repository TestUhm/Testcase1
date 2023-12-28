### Test Case ✍🏼
___

# 1. 테스트 대상
MYCLE
> 차량을 관리할 수 있는 앱

[![1](https://github-production-user-asset-6210df.s3.amazonaws.com/154364394/293132492-1e17cede-6475-4e03-b9a6-a40127af9b0b.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20231228%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20231228T231423Z&X-Amz-Expires=300&X-Amz-Signature=30f008fa470aad096b8bac89a6bbd46aa70f9774be1259bf8050ab6fbb8f75ea&X-Amz-SignedHeaders=host&actor_id=154364394&key_id=0&repo_id=736461276)](https://mycle.co.kr/)


<br/>
<br/>
<br/>


# 2. 앱 분석


<img src="https://github-production-user-asset-6210df.s3.amazonaws.com/154364394/293131275-1a213e0e-fc6f-44b8-ae31-81207e8783e1.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20231228%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20231228T231744Z&X-Amz-Expires=300&X-Amz-Signature=13a96afe7f90bc4311ec591b45761885d37bf62415d9edcb886040526895bec9&X-Amz-SignedHeaders=host&actor_id=154364394&key_id=0&repo_id=736461276" alt="" width="40%" height="520" align="right">


```사용자 리뷰에 대한 평가```

<br/>
<br/>

> 장점
- 다양한 기능을 제공해 편리함
- 정비소, 검사소 예약 시스템 만족
- 운행 일지 기록을 저장할 수 있어서 만족

<br/><br/>

> 단점
- 엔진오일 교체 업체 가격이 다소 높음
- 차량 정보를 불러오지 못하는 오류 발생
- 정비 및 주유 기록이 초기화되는 오류 발생
- 첫 사용자가 해당 앱을 접하기에는 다소 복잡함
- 서비스 지점을 미리 예약한 후 당일 해당 지점에 도착했으나<br/>
자재가 없는 경우 발생

<br/>
<br/>
<br/>

# 3. 우선순위
```사용자 평가를 통해 테스트 케이스 작성```
- 사용자들이 주로 이용할 수 있는 기능
- 단점을 중심으로 오류가 발생할 수 있는 기능


<br/>
<br/>
<br/>

# 4. 테스트 진행

[![3](https://github-production-user-asset-6210df.s3.amazonaws.com/154364394/293131894-6cc14b3b-33f8-4819-a7e6-1f6fe0e41b7d.PNG?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20231228%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20231228T231816Z&X-Amz-Expires=300&X-Amz-Signature=b23d911f631e7c22d8009299e065015b553f16d68423990e0857d84eabd469b1&X-Amz-SignedHeaders=host&actor_id=154364394&key_id=0&repo_id=736461276)](https://docs.google.com/spreadsheets/d/12sLQMDEUuU9e9TURRgcy3NTbxH1CY_6oO4BnkGtvbO8/edit?usp=sharing)<br/>
( ↑ 이미지를 클릭하여 자세히 보기 )


<br/>
<br/>
<br/>

# 5. 이슈

```
- TC_018
 1) 분류
  → 홈 화면 - 중앙 메뉴 - 내 주변 장소 - 주유소

 2) 중요도
  → High

 3) 제목
  → 최저가 순 주유수

 4) 수행 순서
  → 1. 홍 화면 중앙 "내 주변 장소" 내 "주유소" 메뉴 선택
    2. "최저가 순" 탭 선택
    3. 주유소 선택
    4. 하단 "추천하기", "리뷰작성", "전화걸기" 메뉴 선택

 5) 이슈
  → 필터 기능 이용 시 간헐적으로 설정한 거리 외에 주유소가 출력되는 현상

 6) 판단 / 확인 사항
  → 필터 기능을 이용하지 않으면 정상 출력되나 필터 기능 이용 시에만 간헐적으로 오류가 발생하는 것으로 확인
```

```
- TC_019
 1) 분류
  → 홈 화면 - 중앙 메뉴 - 내 주변 장소 - 주유소

 2) 중요도
  → High

 3) 제목
  → 거리 순 주유수

 4) 수행 순서
  → 1. 홍 화면 중앙 "내 주변 장소" 내 "주유소" 메뉴 선택
    2. "거리 순" 탭 선택
    3. 주유소 선택
    4. 하단 "추천하기", "리뷰작성", "전화걸기" 메뉴 선택

 5) 이슈
  → 1km 반경 내에 주유소가 실제 존재하나 앱 화면에는 출력되지 않는 현상

 6) 판단 / 확인 사항
  → 해당 주유소가 앱 상에 미등록 상태인지 확인 필요
```

