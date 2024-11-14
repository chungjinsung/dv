<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>이미지 비교 선택</title>
  <style>
    body {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background-color: #f0f0f0;
    }
    .image-container {
      display: flex;
      gap: 20px;
    }
    .image-box {
      cursor: pointer;
      border: 2px solid transparent;
      transition: border-color 0.3s;
    }
    .image-box img {
      width: 300px;
      height: auto;
    }
    .image-box.selected {
      border-color: #007bff;
    }
  </style>
</head>
<body>
  <div class="image-container">
    <div class="image-box" onclick="selectImage(this)">
      <img src="image1.jpg" alt="Image 1">
    </div>
    <div class="image-box" onclick="selectImage(this)">
      <img src="image2.jpg" alt="Image 2">
    </div>
  </div>

  <script>
    function selectImage(selectedBox) {
      // 모든 이미지 박스에서 'selected' 클래스를 제거
      document.querySelectorAll('.image-box').forEach(box => {
        box.classList.remove('selected');
      });
      // 선택된 이미지 박스에 'selected' 클래스 추가
      selectedBox.classList.add('selected');
    }
  </script>
</body>
</html>
