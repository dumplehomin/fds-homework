# Image Gallery

전체 배경이미지는 body 요소에  linear-gradient 를 이용하여 넣었다.
>background: linear-gradient(#222222 8%, #393939 10%, #c2c2c2)

___

이미지는 ul요소 안에 li로 넣었고 li는 array변수 imgSRCArray에 이미지URL을 삽입하면 이미지URL 갯수만큼 li>div.centered>img가 동적으로 생성된다.
___

갤러리 배경은 linear-gradient 가 아닌 radial-gradient 로 원형 그라데이션으로 적용하였다.
>background-image: radial-gradient(center, ellipse cover, #fafafa 0%,#eeeeee 50%,#d1d1d1 100%)

___

이미지(li)들은 border-radius 를 적용시켜 외각선을 둥글게 표현하였고 box-sizing: border-box 를 적용시켜 width가 border 만큼 커지는 현상을 해결하였다.
>border-radius: 15px 50px; 
>box-sizing: border-box;

___

이미지 크기를 고려 이미지 삽입시 가로 크기가 크면 클래스 portrait를, 세로 크기가 크면 클래스 landscape 를 스크립트로 삽입하였고 정렬을 위해 position 과 transform을 이용하여 항상 이미지가 가운데 정렬이 되도록 하였다.
```
.centered {
	position: absolute;
	top: 0; bottom: 0; left: 0; right: 0;
	-webkit-transform: translate(50%,50%);
   -ms-transform: translate(50%,50%);
   transform: translate(50%,50%);
}

.centered>img {
	position: absolute;
	top: 0; left: 0;
	width: 100%;
	height: auto;
	-webkit-transform: translate(-50%,-50%);
   -ms-transform: translate(-50%,-50%);
   transform: translate(-50%,-50%);
}

.centered>img.portrait {
	width: 100%;
	height: auto;
}

.centered>img.landscape {
	width: auto;
	height: 100%;
}
```
___


미디어쿼리를 사용해 분기마다 이미지 나열을 다르게 하였다
```
@media screen and (min-width: 321px) and (max-width: 768px) {
	.gallery-container>li {
		width: 100%;
		height: 40%;
		margin-right: 0;
	}
}

@media screen and (min-width: 769px) and (max-width: 1024px) {
	.gallery-container>li {
		width: 45%;
		height: 30%;
		margin-right: 10%;
	}
}
```