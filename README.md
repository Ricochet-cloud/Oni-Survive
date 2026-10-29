# 에셋 폴더 안내 (dawn-slayer.html과 같은 위치에 `assets/` 폴더로 두세요)

파일을 넣기만 하면 자동 적용됩니다. 파일이 없으면 기본 임시 그림/무음으로 동작해요.
파일 이름이나 크기를 바꾸고 싶으면 `dawn-slayer.html` 위쪽의 `ASSETS` 설정만 고치면 됩니다.

## sprites/ — 투명 배경 PNG, 정사각형, 오른쪽을 보는 모습 (왼쪽은 자동 반전)
- player.png  (플레이어, 기본 표시 크기 12px)
- grunt.png   (일반 적, 12px)
- runner.png  (빠른 적, 10px)
- tank.png    (탱커, 17px)
- boss.png    (보스, 38px)

해상도는 16×16, 32×32 등 자유예요. 화면 크기에 맞춰 줄여서 그려집니다.
걷기 애니메이션: 프레임을 가로로 이어 붙인 시트로 만들고 `frames`를 프레임 수로 바꾸세요.
(예: 4프레임이면 가로 128 × 세로 32)
캐릭터가 너무 작거나 크게 보이면 `mul` 값(배율)을 조절하세요.

## fx/ — 효과 이미지 (투명 PNG)
- slash.png   물결 베기 검기 (오른쪽 방향으로 그리면 날아가는 방향으로 회전)
- wind.png    바람 칼날
- flame.png   화염 구슬
- bolt.png    벼락 (세로로 긴 이미지, 위→아래)
- gem.png / gem_big.png  경험치 구슬

## bg/
- tile.png    16×16 반복 배경 타일

## audio/
- bgm.mp3     배경음 (반복 재생)
- slash.wav, wind.wav, thunder.wav, hit.wav, hurt.wav, levelup.wav, win.wav, lose.wav

게임 중 M 키로 음소거할 수 있어요.

## 참고
- `file://`로 직접 열어도 이미지는 보이지만, 브라우저에 따라 오디오가 막힐 수 있어요.
  그럴 땐 폴더에서 `python -m http.server` 로 열면(http://localhost:8000/dawn-slayer.html) 안정적이에요.
- BGM은 첫 클릭(시작하기 버튼) 이후에 재생돼요 (브라우저 자동재생 정책).
