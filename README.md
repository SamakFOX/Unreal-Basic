# 언리얼 엔진 기초 사용법부터 레벨 제작 실습까지

## ! Unreal Engine 5.6.1 버전 기준으로 작성되었습니다.<br>신버전에서 키 또는 기능이 변경될 시 해당 기능에는 안내문구가 추가됩니다.   

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

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/SamakFOX/Unreal-Basic/blob/main/images/00000_EG_Launcher.jpg" width="600"><br>
      <em>'에픽게임즈 런처' 내 '언리얼엔진' 탭</em>
    </td>
  </tr>
</table>

◆ 에픽게임즈 런처  
&nbsp;&nbsp;&nbsp;&nbsp;- 샘플 : 언리얼 기반 프로젝트 파일  
&nbsp;&nbsp;&nbsp;&nbsp;- 마켓플레이스 : 언리얼에서 사용할 수 있는 데이터(Assets)의 스토어 (2025년 FAB으로 통합됩)  
&nbsp;&nbsp;&nbsp;&nbsp;- 라이브러리 : 설치된 언리얼 엔진과 에셋 목록  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (엔진버전 우측 [+] 버튼을 통해 여러 버전 설치 가능)  
&nbsp;&nbsp;&nbsp;&nbsp;- 트윈모션 : 사실적 디자인을 구현할 수 있는 리얼타임 3D 렌더러  
&nbsp;&nbsp;&nbsp;&nbsp;- 리얼리티스캔 : 이미지와 라이다(LiDAR)를 통해 실제 오브젝트를 3D로 스캐닝  

<table>
  <tr>
    <td align="center" width="59%">
      <img src="https://github.com/SamakFOX/Unreal-Basic/blob/main/images/00000_Install-Engine-5.6.jpg"><br>
      <em>언리얼엔진 설치</em>
    </td>
    <td align="center" width="39%">
      <img src="https://github.com/SamakFOX/Unreal-Basic/blob/main/images/00000_Install-Options-5.6.jpg"><br>
      <em>설치 옵션</em>
    </td>
  </tr>
</table>

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
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 창 > 레이아웃 불러오기 > UE4 클래식 레이아웃  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(예전 레이아웃이 편해서 클래식에서 일부 변경한 UI로 사용중입니다. UE5가 편하신 분은 그냥 사용하시면 됩니다.)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 편집 > 에디터 개인 설정 > 지역&언어 > 에디터 언어를 `영어`로 변경 (오류 방지, 해외 튜토리얼 습득 유연성을 위해)  
&nbsp;&nbsp;&nbsp;&nbsp;- 각 패널들은 툴바 Window에서 여러 개 꺼낼 수도 있음 (ex. 컨텐츠브라우저 2개 켜기)  

◆ 기본 조작  

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/SamakFOX/Unreal-Basic/blob/main/images/00001_Interface01.jpg" width="600"><br>
      <em>언리얼 5.6 인터페이스 (UE4 레이아웃)</em>
    </td>
  </tr>
</table>

&nbsp;&nbsp;&nbsp;&nbsp;▶ 뷰포트 조작 방법  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 우클릭 + 마우스이동 : 화면 회전  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 좌/우클릭 + W/A/S/D : 상하좌우 이동  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 좌/우클릭 + Q/E : 수직 상승/하강  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Alt + 좌클릭 : 클릭한 지점을 기준으로 화면 회전  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 마우스 휠업/다운 : 줌인/줌아웃 (카메라확대)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Ctrl + Z : 되돌리기  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 오브젝트 좌클릭 : 오브젝트 선택  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Obj 선택 후 E : 오브젝트 회전 조정 (중심축을 선택하면 3축을 동시에 조정)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Obj 선택 후 R : 크기 조정  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 상단 포인터/이동/회전/크기 버튼 : 오브젝트 조작  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 상단 그리드버튼 : 가상의 그리드에 오브젝트를 스내핑 (숫자: 1틱당 움직일 단위, 구체적일수록 낮은숫자)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 상단 각도 버튼 : 1틱당 회전할 각도 단위  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 상단 크기 버튼 : 1틱당 조절할 크기 단위  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 상단 카메라 모양 : 뷰를 이동하는 속도 조절  

&nbsp;&nbsp;&nbsp;&nbsp;▶ 오브젝트 배치와 조작  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 뷰포트 좌측의 Place Actors 패널에서 오브젝트를 드래그&드랍  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 이동모드에서 Alt를 누른채로 오브젝트를 이동시키면 복제가 됨  

&nbsp;&nbsp;&nbsp;&nbsp;▶ 게임 플레이  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 뷰포트 위의 재생버튼을 클릭하여 게임 플레이 (Player Start 오브젝트가 있는 곳에서 시작됨)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 뷰포트에서 특정 지점을 우클릭 후 Play From Here 클릭하여 해당 지점에서 플레이 시작  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 키보드 ESC를 누르면 작업창으로 복귀  
	
&nbsp;&nbsp;&nbsp;&nbsp;▶ Content Browser : 현재 프로젝트의 모든 파일과 폴더의 탐색기 (좌측: 트리 뷰, 우측: 폴더 뷰)  
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/SamakFOX/Unreal-Basic/blob/main/images/00001_cbrowser.jpg" width="600"><br>
      <em>컨텐츠 브라우저 창</em>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/SamakFOX/Unreal-Basic/blob/main/images/00001_cbrowser_addbtn.jpg" width="600"><br>
      <em>Add 버튼 클릭 시 드랍다운 메뉴</em>
    </td>
  </tr>
</table>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Add : 엔진 및 로컬에서 컨텐츠 로드  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Import : 로컬스토리지에서 컨텐츠 임포트  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Save All : 작업한 모든 파일 목록이 나타나며, 저장할 오브젝트를 선택하여 저장  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Fab : 펩에서 컨텐츠 임포트  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;★ 폴더를 우클릭하여 폴더 색상을 변경하거나 Add to Favorites를 통해 즐겨찾기에 고정할 수 있음 (자주쓰는 폴더)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;★ 외부에서 가져온 에셋들도 한번 레벨에 배치했다면 Place Actors에서 검색하여 찾을 수 있음  

&nbsp;&nbsp;&nbsp;&nbsp;▶ 콘텐츠 브라우저를 통한 오브젝트 배치 (Place Actors 보다 다양한 오브젝트를 배치 가능)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 먼저 StarterContent의 오브젝트로 시작, 드래그&드랍으로 오브젝트 배치  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`없다면 Add > Add Feature or Content Pack... > Content > Starter Content > Add to Project 클릭하여 추가`  

<table>
  <tr>
    <td align="center">
		<img src="https://github.com/SamakFOX/Unreal-Basic/blob/main/images/00001_cbrowser_StaticMesh.jpg" width="100">
		<img src="https://github.com/SamakFOX/Unreal-Basic/blob/main/images/00001_cbrowser_Material.jpg" width="100">
		<img src="https://github.com/SamakFOX/Unreal-Basic/blob/main/images/00001_cbrowser_texture.jpg" width="100"><br>
		<em>요소별 라벨 컬러</em>
    </td>
  </tr>
</table>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Static Mesh (3D 모델링 에셋) - 하늘색 라벨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Materials (Static Mesh의 재질, 질감을 설정하는 에셋) - 초록색 라벨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`뷰에 직접 드래그&드랍 해도 되고, 오브젝트의 Details > Materials에 넣어도 됨`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`재질 적용 시 크기가 안맞는 경우 : Static Mesh의 크기가 작거나 크기 때문 -> 재질을 프로시져로 재생성해야 함`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`더블클릭하여 블루프린트에서 상세 설정 변경 가능`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Texture(이미지) - 빨간색 라벨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Material을 만들 때 사용함 (Static Mesh에 바로 넣을 수 없음)`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Particle (동적인 오브젝트)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`드래그&드랍으로 환경에 바로 배치가 가능`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`T 버튼이 눌려 있으면 반투명한 파티클들이 선택이 불가능 (T를 다시 눌러 해제하고 선택)`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Audio  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`드래그&드랍으로 환경에 배치 가능(배치된 곳에서 소리가 남)`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`WAV 파일 포맷만 인식 가능`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`더블클릭하여 상세 설정창에서 값 변경 가능 (Looping: 루프, Volume: 음량, Pitch: 음정 등)`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Blueprints  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`특정 기능을 하도록 만들어진 사전 설정 복합체 또는 효과 등`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`코드를 사용하지 않고 게임 기능과 논리 구조를 만들 수 있음`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Maps (level) - 주황색 라벨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`여러 맵(레벨)을 만들고 이동할 수 있음`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Props (퀄리티 있는 3D 모델)  
	
&nbsp;&nbsp;&nbsp;&nbsp;▶ Details : 선택된 오브젝트의 세부 설정값  

&nbsp;&nbsp;&nbsp;&nbsp;▶ Outliner : 배치한 모든 오브젝트를 리스트화  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Visibility를 끄면 뷰에서는 보이지 않고 게임 플레이시엔 보이게 됨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 조합키 - Ctrl 키 : 다중 선택, Shift 키 : 구간 선택  

◆ UE5 / 3D 이해하기  
&nbsp;&nbsp;&nbsp;&nbsp;▶ 오브젝트의 구성  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 3D 오브젝트는 여러개의 폴리곤으로 구성되어 있음  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 이 폴리곤의 수가 많아질 수록 퀄리티는 좋아지지만 게임에 부하가 걸리며 렉이 걸릴 수 있음(UE4까지)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 각 오브젝트에 마우스를 올리면 세부정보가 표시되는데, 이 중 Triangles(폴리곤)의 갯수를 확인하면 됨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Alt + 2 단축키를 통해 와이어프레임으로 폴리곤을 확인할 수 있음  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 언리얼엔진 5부터는 나나이트 기술을 통해 폴리곤에 구애받지 않게 됨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;// 나나이트 기술 : 엔진 자체적으로 오브젝트가 화면에서 멀어질수록 폴리곤의 수를 자동으로 줄여 부하를 줄임  

&nbsp;&nbsp;&nbsp;&nbsp;▶ 고퀄리티 에셋(데이터) 사용하기  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 언리얼에서 퀵셀을 인수하여 고퀄리티 텍스쳐와 모델링들을 무료로 다운로드하여 사용 가능함  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`퀵셀 : 실제 자연환경을 리얼리티캡쳐를 통해 사실적이게 구현해 둔 에셋을 배포`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;01. 뷰포트 상단에 박스모양 위에 플러스 모양이 있는 버튼 클릭  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;02. Quixel Bridge 클릭 후 에픽게임즈 계정으로 로그인  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;03. 우측상단 계정아이콘 > Preferences > Library Path 설정 (고용량 에셋들이므로 보조 저장장치를 사용하는 것이 좋음 - SSD 아니여도 됨)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;04. 원하는 에셋 선택 후 품질을 선택하여 다운로드 클릭 (Ctrl 키로 여러 에셋 선택 가능)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;05. 다운로드가 완료되면 Add 버튼을 클릭  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;06. UE로 돌아가 콘텐츠 브라우저의 Megascans 폴더 확인  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;07. Static Mesh에 텍스쳐와 재질이 적용되어 있으므로 바로 사용 가능  

&nbsp;&nbsp;&nbsp;&nbsp;▶ 퀵셀 데이터 용량 최적화하기  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 폴리곤 못지 않게 텍스쳐의 용량이 큼 : 상세정보의 Dimensions(해상도)와 Disk Size(용량) 확인  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 8K 텍스쳐와 4K 텍스쳐는 게임에서 드라마틱한 차이가 있지 않으므로 텍스쳐 품질은 4K 또는 2K로 사용해도 됨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`오브젝트를 가까이서 보여줘야 하는 프로젝트의 경우는 8K LOD 0`  
&nbsp;&nbsp;&nbsp;&nbsp;★ 인게임 리소스 사용량 줄이기  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;01. 텍스쳐를 더블클릭하여 상세정보 창 오픈  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;02. Details의 LOD Bias 값을 증가시키면 텍스쳐 해상도가 변경됨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`(8K -> LOD 1 -> 4K) - 인게임 리소스 사용량도 1/4`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`(8K -> LOD 2 -> 2K) - 인게임 리소스 사용량도 1/4 * 1/4 = 1/16`  
&nbsp;&nbsp;&nbsp;&nbsp;★ 저장장치 사용량 줄이기  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 나나이트 품질의 오브젝트를 사용한다면 노멀맵 텍스쳐는 사실상 필요성이 적음 (LOD를 변경해보면 변화가 없는 걸 알 수 있음)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- DpR 텍스쳐는 필요 없음 (하지만 여러 사람과 협업을 한다면 유지를 고려해야 함)  
&nbsp;&nbsp;&nbsp;&nbsp;☆ 노멀맵 파일은 낮은 품질로 다운로드하고 필요하다면 LOD를 더 낮춰줌  
&nbsp;&nbsp;&nbsp;&nbsp;☆ DpR 파일은 제거 (Delete 키 또는 우클릭>Delete 클릭 후 Force Delete)  
			
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;● 퀵셀에서 데이터별로 품질 조정하기  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 퀄리티를 Nanaite로 설정하고 다운로드  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Add를 눌러 콘텐츠 브라우저에 추가  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 퀄리티를 High(4K)로 설정하고 다운로드 또는 Midium(2K)으로 설정하고 다운로드  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Add를 눌러 콘텐츠 브라우저에 추가  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 콘텐츠 브라우저에서 해당 모델의 Static Mesh를 둘 다 배치  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 텍스쳐 중 8K로 설정된 파일들, 4K의 DpR 텍스쳐, 4K Static Mesh를 선택하고  Delete > Force Delete  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;// 8k 검색, DpR 검색, Static Mesh 필터링 후 lod0 검색 - 순서대로 삭제  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;// UE5가 강제종료될 경우 배치된 오브젝트를 삭제하고 리소스를 다시 제거  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 나나이트 모델의 텍스쳐가 미싱 상태로 바뀜  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 콘텐츠 브라우저에서 Static Mesh를 더블클릭하여 새 창 오픈 (월드에 배치된 오브젝트에 넣으면 다음에 사용 시 텍스쳐를 또 넣어줘야됨)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Details의 Material Slots에 4K Material을 드래그&드랍  
				
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;● 여러 텍스쳐를 작업할 때  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Content Browser 좌측의 트리 뷰에서 여러 폴더를 다중선택or구간선택  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 선택된 폴더의 모든 리소스가 우측에 표시됨  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;//  썸네일 로딩이 되지 않는 경우 한 번 배치하면 전부 로딩됨 (하늘색 라벨 에셋만 전부 배치하면 됨)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Ctrl + 휠다운 : 우측 뷰 목록 작게보기  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 검색바 이용 8k 검색 후 전체 삭제, lod 검색 후 전체 삭제(High 모델), DpR 검색 후 전체 삭제  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;// 검색바 좌측의 필터버튼을 이용해서 필터링할수도 있음  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 나나이트 모델 세부정보를 하나씩 켜서 Material을 재적용  
