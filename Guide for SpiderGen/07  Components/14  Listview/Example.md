# Example

**스파이더젠 홈페이지에 사용된 실제 페이지를 바탕으로 직접 제작**

### 1️⃣ [ListView](<../14  Listview.md>)

**여러 개의 아이템을 리스트 형태로 표시하고 관리할 수 있는 컴포넌트**

반복적인 레이아웃을 여러개 만들 필요없이 하나의 레이아웃을 여러번 사용하기에 효과적

> ex ) 게시글 목록

![](https://wikidocs.net/images/page/276280/board.png)

**< 🔼 사진 -** [**스파이더젠 홈페이지 > 커뮤니티 > 질의응답**](https://www.spidergen.org:3003/?pid=T030200) **>**

해당 페이지 내 게시판을 만들기 위해 리스트 뷰를 사용\
아래는 해당 페이지를 레이아웃으로 구성한 사진

![](https://wikidocs.net/images/page/276280/board_lay.png)

**< 🔼 사진 - 홈페이지 게시판을 구현한 레이아웃 >**

> 빨간 박스: ListView

해당 파일의 js에 예시로 만들 목업 데이터를 만듦

```js
this.Data = [
	{img: '이미지 주소', title: '게시글 제목', nickName: '작성자', date: '작성일', count_answer: 답글 수, count_view:  조회 수, count_recommand: 추천 수},
	...
]
```

리스트 뷰에 아이템을 넣을 때 위처럼 작성한 데이터도 함께 넘김

```js
this.listView.addItem('Source/리스트 뷰 아이템.lay',  this.Data);
```

\


해당 리스트 뷰에 아래 사진과 같은 아이템을 추가해 게시판을 구현

![](https://wikidocs.net/images/page/276280/listview_item.png)

**< 🔼 사진 -** [**스파이더젠 홈페이지 > 커뮤니티 > 질의응답**](https://www.spidergen.org:3003/?pid=T030200) **내의 게시글 >**

마찬가지로 아래와 같이 레이아웃 구성

![](https://wikidocs.net/images/page/276280/listview_item_lay.png)

**< 🔼 사진 - 홈페이지 게시글을 구현한 레이아웃 >**

해당 파일의 js에 넘겨받은 데이터를 셋팅

```js
setData(data)  {
	this.data = data;
	
	this.profile.setImage(data.img);
	this.title.setText(data.title);
	this.nickName.setText(data.nickName);
	this.date.setText(data.date);
	this.count_answer.setText(data.count_answer);
	this.count_view.setText(data.count_view);
	this.count_recommand.setText(data.count_recommand);
}
```

🔽 시뮬레이터로 완성된 화면을 확인

![](https://wikidocs.net/images/page/276280/board_res.png)

#### 자동 데이터 바인딩

내부적으로 각 데이터 객체를 **setData** 메소드에 전달하여 아이템 뷰에 데이터를 설정

이 과정은 데이터 배열의 각 객체에 대해 반복적으로 수행되어,\
리스트 뷰에 **모든 데이터가 자동으로 추가**
