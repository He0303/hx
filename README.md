[<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>你好，欢迎来到</title>
    <style>
        body {
            width: 640px;
            height: 1030px;
            margin: 0 auto;
            background-color: #f0f0f0;
            text-align: center;
            border: 10px solid green; /* 在body元素上绘制绿色边框 */
            position: relative; /* 设定body元素为相对定位，以便绝对定位的子元素参考 */
        }

        .image-container {
            position: relative;
            width: 640px;
            margin: 0 auto; /* 水平居中图片容器 */
        }

        .image-container img {
            width: 640px;
            height: 1030px; /* 设置图片容器的大小 */
            object-fit: cover;
            display: block; /* 让图片成为块级元素，以便设置上下居中 */
            margin: 0 auto; /* 水平居中图片 */
        }

        h1 {
            position: absolute; /* 将h1标签设为绝对定位 */
            top: 15%; /* 从顶部50%的位置开始显示 */
            left: 30%; /* 从左侧50%的位置开始显示 */
			font-size: 50px;
            z-index: 1; /* 设置显示优先级，确保文字显示在图片上面 */
            color: white; /* 设置文字颜色为白色 */
        }
		h2{
			position: absolute; /* 将h1标签设为绝对定位 */
			top: 18%; /* 从顶部50%的位置开始显示 */
			left: 17%; /* 从左侧50%的位置开始显示 */
			font-size: 80px;
			z-index: 1; /* 设置显示优先级，确保文字显示在图片上面 */
			color: white; /* 设置文字颜色为白色 */
		}
		button{
			position:relative;
			top:-400px;
			font-size: 100px;
			color:black;
			background-color:white;
		}
		#new-label {
			opacity: 0; /* 初始时设置透明度为0，隐藏新标签 */
			position: absolute; 
			top: 18%; 
			left: 50%; 
			transform: translate(-50%, -50%);
			font-size: 100px;
			color: white;
			z-index: 1; 
			transition: opacity 1s; /* 添加过渡效果 */
		}
		.second-image {
		    opacity: 0;
		    position: absolute;
		    top: 40%;
		    left: 50%;
		    transform: translate(-50%, -50%);
		    z-index: 1;
		    transition: opacity 1s;
		    width: 200px; /* 设置图片宽度 */
		    height: 200px; /* 设置图片高度 */
		}
        #enter-button {
			display: none; /* 默认隐藏按钮 */
			position: absolute;
			top: 60%; 
			left: 20%; 
			font-size: 80px;
			z-index: 1;
		}
    </style>
</head>
<body>
    <div class="image-container">
        <img src="新地图.jpg" />
        <h1>欢迎来到</h1>
		<h2>飞来峰景区</h2>
    </div>
	<button onclick="hideElements()">进入景区</button>
	<div id="new-label" onclick="hideElements()">你好</div>
	<img class="second-image" src=" 灵隐寺.jpg" onclick="hideElements()" /> <!-- 新添加的图片 -->
   <button id="enter-button" onclick="hideElements2()" style="display:none;">进入灵隐寺</button>
	
	<script>
		function hideElements(){
			document.querySelector('h1').style.display = 'none';
			document.querySelector('h2').style.display = 'none';
			document.querySelector('button').style.display = 'none';
			showNewLabel(); // 调用显示新标签的函数
			showSecondImage(); // 调用显示第二张图片的函数
			showButton();
		}

		function showNewLabel(){
			document.querySelector('#new-label').style.opacity = '1'; // 点击按钮后显示新标签
		}

		function showSecondImage(){
			document.querySelector('.second-image').style.opacity = '1'; // 点击按钮后显示第二张图片
		}
		function showButton() {
        document.getElementById('enter-button').style.display = 'block';
    }
	function hideElements2(){
	        window.location.href = 'https://space.bilibili.com/457706009?spm_id_from=333.999.0.0';
	    }
   


	</script>
</body>
</html>
](URL_of_your_HTML_file)
