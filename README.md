# 다시 뛴다, 한국 축구 — 웹 퍼블리싱 안내

제56대 대한축구협회장 선거 전략 보고서의 인터랙티브 웹 버전입니다.

## 폴더 구성
```
index.html              ← 메인 페이지 (이 파일이 홈이 됩니다)
assets/
  kfa-mark.webp/.png    ← KFA 로고 (nav·표지·푸터·파비콘)
  cover-emblem.webp     ← 진짜 커버의 심장박동 엠블럼
  kfa-emblem-only.webp  ← 밝은 배경 섹션 제목 앞 엠블럼
  kfa-emblem-white.webp ← 네이비 배경 섹션 제목 앞 엠블럼(흰색)
  cover-bg.jpg          ← 본문 커버 배경
  bi-emblem.png / bi-forward.jpg  ← 브랜드 섹션 이미지
  fans.jpg              ← 팬 메시지 섹션 배경
  og-image.png          ← 공유 시 뜨는 미리보기 이미지 (1200×630)
```

> 진짜 커버(맨 첫 화면)의 셰브론 배경은 이미지가 아니라 CSS로 그려집니다. 별도 배경 파일이 필요 없습니다.

## GitHub Pages로 올리는 법 (5분)

1. GitHub에서 새 저장소(repository)를 만든다. 예: `kfa-vision`
2. 이 폴더의 파일 전부(`index.html`, `assets/`)를 그 저장소에 업로드한다.
3. 저장소 **Settings → Pages** 로 간다.
4. **Source** 를 `Deploy from a branch`, 브랜치를 `main` / 폴더 `/root` 로 지정하고 Save.
5. 1~2분 뒤 `https://사용자명.github.io/kfa-vision` 주소로 라이브된다.

## ⚠️ 딱 한 곳만 고치면 됩니다 — 공유 미리보기(OG) 주소

`index.html` 상단의 주소가 임시값(`username.github.io/kfa-vision`)으로 되어 있습니다.
카카오톡·문자·SNS에 링크를 붙였을 때 미리보기 이미지가 뜨게 하려면, 본인 실제 주소로 바꿔야 합니다.

`index.html`을 열어 **`username.github.io/kfa-vision` 을 전부 본인 주소로 교체**하세요.
(에디터의 찾기·바꾸기로 한 번에 바꾸면 됩니다. 총 5군데.)

예를 들어 주소가 `https://hong.github.io/kfa` 라면:
- `og:image` → `https://hong.github.io/kfa/assets/og-image.png`
- `og:url`, `canonical`, `twitter:image` 등도 같은 규칙으로.

바꾼 뒤 다시 업로드하면 끝입니다. 링크 미리보기가 캐시될 수 있으니,
카카오는 [카카오 디버거](https://developers.kakao.com/tool/clear/og),
페이스북/스레드는 [Sharing Debugger](https://developers.facebook.com/tools/debug/) 에서 캐시를 갱신하면 즉시 반영됩니다.

## 커스텀 도메인을 쓰고 싶다면
Settings → Pages → Custom domain 에 도메인을 넣고, 위 OG 주소도 그 도메인으로 바꾸면 됩니다.

## 이미지 저작권 안내 (중요)

이 사이트의 일부 이미지는 외부 출처입니다. 실제 캠페인·언론 배포 전 사용권을 반드시 확인하세요.

- `assets/bi-*.jpg`, `bi-emblem.png` — 대한축구협회 공식 BI(브랜드 아이덴티티, 2021). 디자인: SAM SEOUL(샘서울). 출처: samseoul.com/branding/kfa. 협회/에이전시의 저작물이므로, 무단 상업적 사용은 권리 침해가 될 수 있습니다. 내부 검토용으로만 사용하거나 정식 허락을 받으세요.
- `assets/fans.jpg` — 2002 응원 사진. 출처·촬영자 확인 후 사용.
- `assets/cover-bg.jpg` — KFA 브랜드 키비주얼. 위와 동일하게 사용권 확인 필요.
- `assets/kfa-mark.*`, `cover-emblem.webp`, `kfa-emblem-*.webp` — 대한축구협회 엠블럼. 협회 상표. 후보 캠프의 실제 사용 시 협회 규정·상표권을 확인하세요.

컬러(KFA Blue/Red 등)는 공개된 브랜드 컬러 코드를 참조한 것으로 사용에 제약이 적지만, 로고·엠블럼·키비주얼 이미지는 권리 확인이 필요합니다.
