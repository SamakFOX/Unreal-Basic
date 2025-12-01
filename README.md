# 언리얼 엔진 기초 사용법부터 레벨 제작 실습까지

## ! Unreal Engine 5.4.4 버전 기준으로 작성<br>신버전에서 키 또는 기능이 변경될 시 해당 기능에는 안내문구가 추가됩니다.   

| 분류기호 안내 |
|---|
| ◆ / ▶ / - : 기본 내용 정리(순차)<br>★ : 중요 정보<br>☆ : 비교적 덜 중요한 정보<br>// : 예시 또는 부가정보<br>▷ : 옵션<br>nn. : 순차 실행<br>♠ : 추가 상식<br>♣ : 팁<br>■ : 실습 |

---

### [ 프로그램 설정 ]

### [ 언리얼 기본 ]  

◆ 언리얼 엔진의 장점  
&nbsp;&nbsp;&nbsp;&nbsp;- RealTime Rendering (실시간으로 렌더링된 화면을 출력)  
&nbsp;&nbsp;&nbsp;&nbsp;- 프로그램 라이선스 : 한화 12억 미만의 스타트업은 무료  
&nbsp;&nbsp;&nbsp;&nbsp;- 모델링을 하지 않고도 디자인이 가능 (퀵셀 모델링을 무료로 사용 가능)  
	
	
◆ 컴퓨터 사양  
&nbsp;&nbsp;&nbsp;&nbsp;- 권장 : RTX 2060 이상, 16GB 이상의 램  
&nbsp;&nbsp;&nbsp;&nbsp;- 최적 : RTX 2080, 3070, 4070 이상 급, 32GB 이상의 램, 100GB 이상의 저장용량  


◆ 에픽게임즈 런처  
&nbsp;&nbsp;&nbsp;&nbsp;- 샘플 : 언리얼 기반 프로젝트 파일  
&nbsp;&nbsp;&nbsp;&nbsp;- 마켓플레이스 : 언리얼에서 사용할 수 있는 데이터(Assets)의 스토어  
&nbsp;&nbsp;&nbsp;&nbsp;- 라이브러리 : 설치된 언리얼 엔진과 에셋 목록이 표시됨 (버전별로 다운로드 가능)  


◆ 설치 시 고려할 것  
&nbsp;&nbsp;&nbsp;&nbsp;- 기본으로 코어 컴포넌트, 시작용 콘텐츠, 템플릿 & 피처 팩, 엔진 소스는 체크 그대로  
&nbsp;&nbsp;&nbsp;&nbsp;- 최초 설치 시 개발할 플랫폼을 확인 후 체크박스 체크 or 해제 (PC용 게임을 개발한다면 전부 체크 해제해도 됨)  
&nbsp;&nbsp;&nbsp;&nbsp;- 가장 최신 버전 한개만 설치되어 있으면 됨  
&nbsp;&nbsp;&nbsp;&nbsp;- 고퀄리티 텍스쳐를 사용하므로 한 개의 프로젝트 당 100GB 정도 용량을 잡아먹음, 감안하고 경로 지정  
	
	
◆ 프로젝트 생성  
&nbsp;&nbsp;&nbsp;&nbsp;- 첫 프로젝트는 게임으로 진행  
&nbsp;&nbsp;&nbsp;&nbsp;- 프로젝트 옵션 : 3인칭 템플릿 선택, 개발-플루프린트, 타깃-데스크톱, 퀄리티-Maximum, 시작용콘텐츠 체크, 레이 트레이싱 체크 (RTX 20 이상만)  
&nbsp;&nbsp;&nbsp;&nbsp;- 프로젝트 잘못 생성 시 대처 방법  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;01. +Add 버튼  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;02. Add Feature or Content Pack... 선택  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;03. Third Person(삼인칭) 선택 후 Add to Project 클릭  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;04. 콘텐츠브라우저의 ThirdPerson\Maps\ThirdPersonMap 더블클릭  
	
	
◆ 프로젝트 초기 설정  
&nbsp;&nbsp;&nbsp;&nbsp;- 레이아웃 구성 변경  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 창 > 레이아웃 불러오기 > UE4 클래식 레이아웃 (초기엔 4로 사용하다 적응이 되면 5 레이아웃으로 변경해서 사용)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 편집 > 에디터 개인 설정 > 지역&언어 > 에디터 언어 를 영어로 변경 (오류 방지, 해외 튜토리얼 습득 등)  
&nbsp;&nbsp;&nbsp;&nbsp;- 각 패널들은 툴바 Window에서 여러 개 꺼낼 수도 있음 (ex. 컨텐츠브라우저 2개 켜기)  
		
		
