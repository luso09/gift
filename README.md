<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>카카오톡 공유 테스트</title>
  <!-- 1. 카카오 SDK 추가 -->
  <script src="https://developers.kakao.com/sdk/js/kakao.js"></script>
</head>
<body>
  <!-- 2. 공유 버튼 추가 -->
  <button id="kakao-share-btn">카카오톡 공유</button>

  <!-- 3. 공유 기능 동작 스크립트 -->
  <script>
    // 카카오 SDK 초기화 (여기에 본인 JavaScript 키 입력)
    Kakao.init('f1823de766079a4f4cc7606eb7abb406');

    // 버튼 클릭 시 공유 동작
    document.getElementById('kakao-share-btn').onclick = function() {
      Kakao.Share.sendDefault({
        objectType: 'feed',
        content: {
          title: '타이틀',
          description: '설명',
          imageUrl: 'https://via.placeholder.com/300',
          link: {
            mobileWebUrl: 'https://open.kakao.com/o/pKJZpJVh',
            webUrl: 'https://open.kakao.com/o/pKJZpJVh'
          }
        },
        buttons: [
          {
            title: '웹으로 이동',
            link: {
              mobileWebUrl: 'https://open.kakao.com/o/pKJZpJVh',
              webUrl: 'https://open.kakao.com/o/pKJZpJVh'
            }
          }
        ]
      });
    }
  </script>
</body>
</html>
