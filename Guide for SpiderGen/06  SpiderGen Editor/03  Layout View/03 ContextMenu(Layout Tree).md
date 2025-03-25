# 03 ContextMenu(Layout Tree)

레이아웃 뷰의 레이아웃 트리 컨텍스트 메뉴

![](https://wikidocs.net/images/page/23229/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2025-02-03_151754.png)

**Copy**

선택한 컴포넌트 복사

**Paste**

선택한 컴포넌트 적용

현재 선택된 컴포넌트가 뷰일 경우 뷰 안에 추가되고 일반 컴포넌트일 경우 선택된 컴포넌트 다음에 추가됩니다.

***

**Copy Style**

컴포넌트 스타일 속성 복사

CSS 속성들이 포함되며, 복사된 스타일은 클립보드에 저장됩니다.

**Paste Style**

컴포넌트 스타일 속성 적용

스타일을 붙여넣을 때, 대상 컴포넌트의 기존 스타일 속성은 복사된 스타일로 덮어씌워집니다.

***

**Copy Event**

컴포넌트 이벤트 설정 복사

해당 컴포넌트에 설정된 이벤트 핸들러와 관련된 정보가 포함됩니다.

**Paste Event**

컴포넌트 이벤트 설정 적용

이벤트를 붙여넣을 때, 대상 컴포넌트의 기존 이벤트 설정은 복사된 이벤트로 덮어씌워집니다.

***

**Object Sequence**

동일 레이어상에서 컴포넌트의 겹침 순서 변경

레이아웃 트리에서 컴포넌트를 선택하고 드래그앤드롭으로 이동시키는 기능과 동일합니다.

![](https://wikidocs.net/images/page/23229/context-objseq.png)

* **Send To Back** 현재 선택된 컴포넌트를 뒤로 보냄
* **Send Backward** 현재 선택된 컴포넌트를 맨 뒤로 보냄
* **Bring Forward** 현재 선택된 컴포넌트를 앞으로 보냄
* **Bring To Front** 현재 선택된 컴포넌트를 맨 앞으로 보냄

**Add/Remove Event**

선택된 컴포넌트에 이벤트를 추가 또는 삭제하는 기능

이벤트를 선택하고 Function Name을 빈값으로 실행하면 해당 이벤트에 설정 된 이벤트 함수가 삭제됩니다.

**Data Query**

해당 컴포넌트에 데이터를 매핑하기 위한 기능

오픈된 다이얼로그에 매핑정보를 가지고 있는 Query 파일을 로드 또는 선택하고 Query 파일의 매핑 정보를 이용해 컴포넌트에 정보를 매핑합니다.

![](https://wikidocs.net/images/page/23229/pop-mapping-info.png)

***

**Reload Comp**

선택한 컴포넌트를 새로 로드하는 기능
