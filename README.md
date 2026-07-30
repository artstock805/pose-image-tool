# 원하는 포즈로 이미지 만드는 도구

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/artstock805/pose-image-tool/blob/master/pose_tool.ipynb)

참조 사진 속 사람의 **자세(포즈)** 만 따와서, 프롬프트로 지정한 **다른 인물/장면**을
그 자세 그대로 만들어 주는 Colab 도구입니다. (Stable Diffusion 1.5 + ControlNet OpenPose)

## 도구 설명
- 사람 사진 → OpenPose로 관절(뼈대) 추출 → 그 자세 조건 + 프롬프트로 새 이미지 생성.
- 자세는 참조 사진이, 겉모습·배경은 프롬프트가 결정합니다.

## 사용법
1. `pose_tool.ipynb`를 Colab에서 엽니다. (GitHub에서 파일 클릭 → "Open in Colab")
2. 상단 메뉴 `런타임 → 런타임 유형 변경 → T4 GPU`로 설정합니다.
3. 셀을 위에서부터 순서대로 실행합니다.
   - 셀1 설치 → 셀2 모델 로드 → 셀3 참조 사진 업로드 & 포즈 추출 → 셀4 이미지 생성 → 셀5 저장
4. 결과 이미지는 셀5에서 자동으로 내 컴퓨터로 다운로드됩니다.

## 테스트 결과
- 포즈 1: 서서 손 든 자세 → 프롬프트: `astronaut in a white spacesuit` → 결과: 잘 됨
- 포즈 2: 앉은 자세 → 프롬프트: `knight in armor, sitting` → 결과: 대체로 잘 됨 (옆모습은 약간 어긋남)

## 한계
- 관절이 겹치거나 옆모습·부분만 보이는 사진은 뼈대 추출이 부정확해 결과가 어긋날 수 있습니다.
- 손가락 등 세밀한 부위는 SD 1.5 특성상 뭉개질 수 있습니다.
