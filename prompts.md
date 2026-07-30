# 테스트에 쓴 프롬프트 모음

셀4의 `prompt` 부분에 넣어 실험한 문장들입니다.

## 공통 negative prompt
```
lowres, bad anatomy, blurry, extra limbs, deformed
```

## 실험 ① 같은 포즈 + 프롬프트만 바꾸기
| # | 프롬프트 | 결과 |
|---|---------|------|
| 1 | `an astronaut in a white spacesuit, standing, high quality, detailed` | 잘 됨 |
| 2 | `a medieval knight in shining armor, standing, detailed` | 잘 됨 (자세 유지) |
| 3 | `a robot made of metal, standing, cinematic lighting` | 잘 됨 |

## 실험 ② 같은 프롬프트 + 포즈 사진만 바꾸기
| # | 포즈 사진 | 프롬프트 | 결과 |
|---|----------|---------|------|
| 1 | 서 있는 사진 | `a person in casual clothes, detailed` | 잘 됨 |
| 2 | 앉아 있는 사진 | `a person in casual clothes, detailed` | 앉은 자세로 잘 나옴 |
| 3 | 옆모습/관절 겹친 사진 | `a person in casual clothes, detailed` | 약간 어긋남 |
