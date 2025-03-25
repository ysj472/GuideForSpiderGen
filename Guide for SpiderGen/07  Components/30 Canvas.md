# 30 Canvas

![](https://wikidocs.net/images/page/274093/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2025-01-23_175042.png)

그래픽을 그리거나 다양한 시각적 요소를 렌더링할 수 있는 기능을 제공 하는 **캔버스 컴포넌트**

> 💫 캔버스 태그 살펴보기 : [이동](https://developer.mozilla.org/ko/docs/Web/API/Canvas_API/Tutorial)

🔹**주요 속성 및 메서드**

| 값                                 | 설명                         |
| --------------------------------- | -------------------------- |
| `ctx`                             | 캔버스의 드로잉 컨텍스트              |
| `getData()`                       | 현재 캔버스의 데이터를 문자열 형태로 반환    |
| `setData(data)`                   | 문자열 형태의 데이터를 캔버스에 설정       |
| `resizeCanvas()`                  | 캔버스의 크기를 재조정               |
| `updatePosition(pWidth, pHeight)` | 캔버스의 위치나 크기가 변경될 때 호출하여 갱신 |

### Example

> #### 빨간색 하트❤️를 그리기 

#### 1. 툴을 이용하는 방법

**1-1. Canvas 컴포넌트를 추가하고, id 를 할당**

`ex) ID = 'canvas001'`

**1-2. canvas 코드를 작성**

```js
const ctx =  this.canvas001.ctx;

// 하트를 그립니다.
ctx.fillStyle =  "red";
ctx.beginPath();
ctx.moveTo(75,  40);
ctx.bezierCurveTo(75,  37,  70,  25,  50,  25);
ctx.bezierCurveTo(20,  25,  20,  62.5,  20,  62.5);
ctx.bezierCurveTo(20,  80,  40,  102,  75,  120);
ctx.bezierCurveTo(110,  102,  130,  80,  130,  62.5);
ctx.bezierCurveTo(130,  62.5,  130,  25,  100,  25);
ctx.bezierCurveTo(85,  25,  75,  37,  75,  40);
ctx.fill();
```

![](https://wikidocs.net/images/page/274093/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2025-01-23_175042.png)

`결과 화면`

### 2. 코드로 추가하기 

```js
// 컴포넌트 생성 
const myCanvas = new ACanvas(); 

// 컴포넌트 초기화 
myCanvas.init({ 
	id: 'myCanvasId', 
	position: 'left:10px, top:10px', 
	size: 'width:300px, height:200px' 
});
```
