# PICONOMY — 피코 광고 제작 가이드
과제1-2: GenAI 기초 2 — 멀티모달 콘텐츠 제작
브랜드(PICONOMY)를 알리기 위한 16:9 광고형 영상 제작 프로젝트

---

## 1. 브랜드/캠페인 정의

- **브랜드**: PICONOMY (캐릭터: 피코)
- **타겟**: MZ세대 중 절약·지출 콘텐츠를 유머로 소비하는 층
- **톤앤매너**: 자연다큐멘터리 진지함 → 반전 코미디, 귀여운 외형과 집요한 생존본능의 대비, 능청스러움
- **USP**: 실제 동물(피카)의 생태를 그대로 자본주의적 생존 전략으로 재해석하는 캐릭터 IP
- **광고 목적**: 인지 — 피코 캐릭터와 세계관을 처음 소개
- **핵심 메시지(한 문장)**: "세상은 넓고, 챙길 건 더 많다."

---

## 2. 사용 도구 총괄

| 역할 | 도구 | 선택 이유 |
|---|---|---|
| 이미지(키프레임) | ChatGPT (GPT 이미지) | 씬별 키비주얼 생성, 캐릭터 묘사 고정 반복으로 일관성 확보 |
| 비디오 (씬1) | Veo 3.1 Fast | Sora 2와 비교 테스트 결과 의도한 동작을 더 정확히 수행해 채택 |
| 비디오 (씬2) | Sora 2 | 제작 도중 Veo 3.1 Fast에서 일시적 생성 오류 발생 → Sora 2로 전환해 완성 (도구 접근성 대응 사례) |
| 비디오 (씬3) | Veo 3.1 Fast | Sora 2로 1차 제작 후, Veo 오류 복구 확인되어 최종적으로 Veo 3.1 Fast 버전 채택 |
| 오디오(내레이션) | TTS (진지한 남자 성우톤, EBS/내셔널지오그래픽 느낌) | 다큐 톤 유지, 반전을 대사가 아닌 상황으로 보여주기 위함 |
| 대체 도구 | 이미지: Gemini/Imagen · 비디오: Runway/Pika 2.5 · 오디오: 타 TTS 서비스 | 크레딧/대기열 이슈 대응 |

**일관성 유지 전략**: 모든 이미지 프롬프트에 피코의 고정 캐릭터 묘사(작고 둥근 몸, 두꺼운 갈색 털, 까맣고 동그란 눈, 능청스러운 표정)를 동일 문구로 반복 삽입. 색감은 "따뜻한 골든아워 조명, 뮤트된 흙톤 색감"으로 씬 전체 고정.

### 도구 비교: Sora 2 vs Veo 3.1 Fast (씬1 기준)
동일한 씬1 프롬프트("앞발로 꽃을 정리하는 동작")로 두 도구를 비교 테스트함.

| 항목 | Sora 2 | Veo 3.1 Fast |
|---|---|---|
| 의도한 동작 수행 | 동작 해석에 오차 있었음 | 의도한 동작(앞발로 정리, 먹지 않음)을 더 정확히 수행 |
| 디테일 표현 | 보통 | 작은 디테일(사물의 미세한 부분)까지 선명하게 표현 |
| 결론 | 비교 후 미채택 | 전 씬 공통 도구로 채택 |

이 비교 결과를 근거로 씬2·씬3도 Veo 3.1 Fast로 통일해 캐릭터 일관성과 제작 효율을 모두 확보함.

### 도구 접근성 대응 사례
제작 도중 Veo 3.1 Fast에서 일시적인 생성 오류(연결/처리 오류)가 발생함. 과제 제약사항의 "도구 접근성 대응" 원칙에 따라 대체 도구(Sora 2)로 즉시 전환해 씬2를 완성함. 이후 Veo 오류가 사이트 측 일시적 문제였음을 확인, 오류 복구 후 씬3은 다시 Veo 3.1 Fast로 제작함. → 이미지/비디오/오디오 각 파트에 대체 도구를 미리 준비해두는 전략이 실제로 유효했던 사례.

---

## 3. 씬별 스토리보드 (총 10초 이내, 3씬)

### 씬 1 — 다큐 설정 (3~4초)
- **목표 메시지**: 낭만적으로 보이는 피카의 실제 생태(꽃 채집)를 진지한 다큐 톤으로 제시
- **화면 구성**: 구도 — 고정 와이드샷, 피사체(피코) 화면 중앙 배치 / 피사체 — 피코 / 배경 — 산악 바위 지대 / 텍스트 유무 — 없음. 피코가 앞발로 꽃과 풀을 정리해 바위 위에 널어놓는 모습
- **내레이션**: "피카가 꽃을 모아 바위에 널어둡니다." (2초 분량, 앞부분)
- **사용 도구**: 이미지 — ChatGPT / 비디오 — Veo 3.1 Fast (Sora 2와 비교 테스트 후 채택, 상세는 위 "도구 비교" 참고)
- **입력 프롬프트(이미지)**:
  > A small round pika creature with thick brown fur, black round eyes, calm expression, standing on a sunlit mountain rock, carrying fresh pink and yellow wildflowers in its mouth, laying them out to dry on the rock surface, warm golden-hour lighting, muted earth-tone color palette, wildlife documentary photography style, shallow depth of field
- **출력 결과 요약**: 따뜻한 다큐 톤의 꽃 채집 키비주얼 확보
- **입력 프롬프트(영상) — 수정 전**:
  > A small, round pika creature with thick brown fur, black round eyes, short rounded ears, and plump cheeks, calm and slightly lazy expression. It stands on a sunlit mountain rock, holding fresh pink and yellow wildflowers in its mouth, and gently lays them out to dry in a neat row on the rock surface. Camera is mostly static with minimal movement. Warm golden-hour lighting, muted earth-tone color palette, shallow depth of field, wildlife documentary photography style, realistic fur texture. Slow, deliberate, natural movement. Horizontal 16:9 aspect ratio. 3-4 seconds.
  - **문제**: "꽃을 물고 와 줄지어 널어놓는다"는 여러 단계 동작을 한 번에 요청했더니, 영상 도구가 짧은 클립(3~4초) 안에서 동작을 완결하지 못하고 "입에 물고 있다가 내려놓는" 동작에서 멈춰버림. 의도한 "채집 후 정리해서 저장" 뉘앙스가 약하게 전달됨.
  - **원인 분석**: 짧은 길이의 영상 생성에서는 다단계 시퀀스보다 단일 동작 하나가 훨씬 안정적으로 구현됨 (멀티모달 제작에서 흔한 "동작 시퀀스 유실" 문제).
- **입력 프롬프트(영상) — 수정 후**:
  > A small, round pika creature with thick brown fur, black round eyes, short rounded ears, and plump cheeks, calm and slightly lazy expression. It carefully places a flower it's holding in its mouth down next to a row of other flowers already drying on the sunlit rock, completing the neat row. Camera is mostly static with minimal movement. Warm golden-hour lighting, muted earth-tone color palette, shallow depth of field, wildlife documentary photography style, realistic fur texture. Slow, deliberate, natural movement. Horizontal 16:9 aspect ratio. 3-4 seconds.
  - **결과 변화**: 동작을 "이미 놓인 꽃 줄에 마지막 한 송이를 채워 넣어 완성하는" 단일 동작으로 좁히자, 저장 행동의 완결된 순간이 안정적으로 표현됨.
- **입력 프롬프트(영상) — 2차 수정 전** (위 "수정 후" 프롬프트 그대로 사용):
  - **문제**: "holding a flower in its mouth"라는 표현을 AI가 "먹는(chewing)" 동작으로 잘못 해석함. 의도한 "채집/저장" 행동이 아니라 "섭취" 행동으로 나와 캐릭터 원칙(먹이가 아니라 저장 목적)과 어긋남.
  - **원인 분석**: "mouth" 단어가 먹는 행위를 연상시키는 트리거로 작동한 것으로 보임 — 멀티모달 생성에서 흔한 "단어의 중의적 해석" 문제.
- **입력 프롬프트(영상) — 2차 수정 후**:
  > A small, round pika creature with thick brown fur, black round eyes, short rounded ears, and plump cheeks, calm and slightly lazy expression. Using its front paws, it carefully arranges a pile of fresh pink and yellow wildflowers into a neat row on a sunlit rock, gently patting them into place. It is not eating or chewing the flowers — this is a careful, deliberate arranging motion with its paws only, mouth closed. Camera is mostly static with minimal movement. Warm golden-hour lighting, muted earth-tone color palette, shallow depth of field, wildlife documentary photography style, realistic fur texture. Slow, deliberate, natural movement. Horizontal 16:9 aspect ratio. 3-4 seconds.
  - **결과 변화**: 동작 주체를 "mouth"에서 "paws"로 명확히 바꾸고 "not eating, mouth closed"를 직접 명시하자 섭취 동작 없이 정리 동작만 안정적으로 표현됨.
- **파일명**: scene01_keyvisual.png / scene01_motion.mp4

### 씬 2 — 반전 (2~3초)
- **목표 메시지**: 꽃더미 아래 숨겨진 절약 정보 뭉치가 드러나는 반전
- **화면 구성**: 구도 — 고정 미디엄샷, 손동작과 종이뭉치가 선명히 보이는 거리 / 피사체 — 피코, 꽃더미, 종이뭉치 / 배경 — 이끼 낀 바위 / 텍스트 유무 — 없음. 피코가 꽃을 걷어내면 포스트잇/메모(핸드폰 요금 절약법, 병원비 아끼는 법 등)가 빼곡히 드러남. 걷어낸 꽃이 주변에 흩어져 "가려져 있었다"는 흔적이 남음
- **내레이션**: "꽃 밑에 무언가 보이는군요. 피카가 숨겨놓은 것은 과연 무엇일까요?" (4초) — 내레이션이 끝나자마자 화면 전환되며 씬3(무음, 로고+슬로건)으로 이어짐
- **사용 도구**: 이미지 — ChatGPT / 비디오 — Sora 2 (제작 중 Veo 3.1 Fast 오류로 전환, 아래 "도구 접근성 대응" 참고)
- **입력 프롬프트 — 1차 (수정 전)**:
  > A small pika creature sitting among dried flowers on a rock, camera pulls back to reveal sticky notes and papers hidden underneath, documentary nature style, 4K, cinematic lighting
  - **문제**: 표정이 놀란/당황한 얼굴로 나와 "능청스러움" 컨셉과 불일치. 꽃 색감·조명이 씬1과 미묘하게 달라 화풍 불일치. 손동작이 빨라 반전 정보가 잘 안 읽힘.
- **입력 프롬프트 — 2차 (Veo 채택 버전)**:
  > A small round pika creature with thick brown fur and black round eyes, calm and nonchalant expression with a slight knowing look (no fear, no surprise), slowly and deliberately pushing aside a pile of dried pink and yellow flowers on a mossy rock to reveal folded paper notes and receipts stacked underneath. Same warm golden-hour lighting and muted earth-tone color grade as the previous shot. Slow hand movement, documentary wildlife cinematography, shallow depth of field, 24fps
  - **결과 변화**: 표정 침착·능청스럽게 유지, 색감 일관성 확보, 동작 속도 조절로 반전 정보 명확히 전달
  - **후속 문제**: 제작 중 Veo 3.1 Fast에서 생성 오류 발생 → Sora 2로 전환
- **입력 프롬프트 — 3차 (Sora 2 전환, 종이 시인성 강화)**:
  > A small, round pika creature with thick brown fur, black round eyes, short rounded ears, and plump cheeks, calm and slightly lazy expression, with a subtle knowing look in its eyes. Sitting beside a large pile of dried pink and yellow flowers on a mossy rock, it uses its front paws to slowly push the flowers apart and to the sides, clearing a wide open gap in the middle. Underneath, a thick, clearly visible stack of folded paper notes and receipts is fully exposed and prominent in the center of the frame, well-lit and in sharp focus. Its expression stays calm and unbothered throughout. Horizontal 16:9 aspect ratio. 2-3 seconds.
  - **문제**: 종이는 잘 보이지만, 애초에 꽃으로 "가려놓았었다"는 은닉의 흔적이 안 드러남
- **입력 프롬프트 — 최종 수정**:
  > ...(위 3차 프롬프트에서) It sits beside a rock where a thick stack of folded paper notes and receipts had been carefully hidden underneath a pile of dried pink and yellow flowers, deliberately arranged on top to disguise them. With its front paws, it slowly pushes the flowers aside, clearing a gap in the middle — some flowers remain scattered around the edges of the exposed papers, making it visually obvious the papers had been intentionally covered and concealed...
  - **결과 변화**: "deliberately arranged to disguise"로 은폐 의도를 명시하고 "flowers remain scattered around the edges"로 걷어낸 흔적을 남겨, 종이가 잘 보이면서도 "가려져 있었다"는 반전 뉘앙스가 시각적으로 명확해짐
- **파일명**: scene02_keyvisual.png / scene02_motion.mp4

### 씬 3 — 브랜드 각인 (4초)
- **목표 메시지**: 다큐 톤을 유지한 채 브랜드/슬로건 각인
- **화면 구성**: 구도 — 고정 와이드샷, 배경 전체와 표지판이 보이는 구도, 하단 1/3은 자막 공간으로 비움 / 피사체 — 바위와 PICONOMY 표지판 (캐릭터 등장 없음) / 배경 — 산악 바위 지대(씬1·씬2와 동일) / 텍스트 유무 — 있음(로고+슬로건 자막)
- **내레이션**: 없음 (직전 씬2에서 "무언가 보이는군요"로 끊긴 뒤, 설명 없이 곧바로 슬로건으로 전환 — 반전을 대사로 설명하지 않는 원칙 반영)
- **화면 텍스트**: 로고 "PICONOMY" + 슬로건 "세상은 넓고, 챙길 건 더 많다"
- **사용 도구**: 이미지 — ChatGPT / 비디오 — Veo 3.1 Fast (1차 Sora 2로 제작 → Veo 오류 복구 확인 후 최종 Veo 3.1 Fast 버전 채택)
- **입력 프롬프트**:
  > Same mountain rock scene as the previous shots, same warm golden-hour lighting and muted earth-tone color palette, wildlife documentary photography style. No character action, no new movement — a calm, static wide shot holding on the rock and landscape. A small wooden signpost-style sign reading "PICONOMY" sits naturally beside the rock, as if it has always been part of the documentary landscape, gently weathered wood texture. Leave the bottom third of the frame open and empty for text overlay to be added later.
- **출력 결과 요약**: 다큐 톤 유지한 정적 브랜드 각인 배경 컷 확보. 로고 텍스트는 AI 렌더링 대신 편집 단계에서 자막으로 삽입 예정
- **파일명**: scene03_keyvisual.png / scene03_motion.mp4

---

## 4. 실행 순서 (체크리스트)

1. **이미지 생성 (ChatGPT)**: 씬1→씬2→씬3 순서로 키프레임 생성. 매 프롬프트에 고정 캐릭터 묘사 문구를 동일하게 복사해 붙여넣기 (일관성 유지).
2. **비디오 변환**: 씬1(Veo 3.1 Fast) → 씬2(Sora 2) → 씬3(Veo 3.1 Fast) 순서로 키프레임을 영상으로 변환.
3. **오디오 생성**: TTS로 씬1·씬2 내레이션 생성(진지한 남자 성우톤, 다큐 어미). 씬3은 내레이션 없이 슬로건 자막만.
4. **통합 편집 (프리미어/캡컷 등)**:
   - 3개 씬 컷 편집으로 연결 (총 10초 이내로 트리밍)
   - 씬3 하단에 슬로건 자막 삽입
   - 오디오 레벨 조정, 씬2 진입 시 내레이션 페이드아웃 처리
   - 해상도 1920×1080(16:9), 24~30fps로 통일 export (H.264/AAC)
5. **파일명**: `PICONOMY_pico_ad_v1.mp4`
6. **최종 체크**: 10초 이내 확인 / 마지막 3~5초 브랜드 인지 장치 포함 확인 / 시각+청각 AI 생성 요소 포함 확인

---

## 5. 스토리보드 PDF 문서화

이 문서를 그대로 PDF로 변환하거나, 표 형식으로 다시 정리해 제출용 스토리보드(PDF 1개)로 마무리하면 됩니다. 각 씬 항목은 과제에서 요구하는 필수 필드(씬 번호/길이, 목표 메시지, 화면 구성, 내레이션, 사용 도구와 목적, 입력 프롬프트+출력 요약, 파일명)를 모두 포함하고 있습니다.
