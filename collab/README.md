# backtest-lab 협업 규칙 (검토자 최초 안내)

이 폴더는 **외부 검토자(AI 포함)와 주고받는 의뢰서·회신**을 두는 곳입니다.
검토를 맡으셨다면 이 문서를 먼저 읽어 주십시오.

---

## 이 프로젝트가 무엇인가

**"거짓말하지 않는 백테스트 도구"** — 투자 전략을 과거 데이터로 검증하되,
거래비용·벤치마크 비교·가정 공개를 사용자가 끌 수 없게 만든 무료 웹 도구입니다.

- 서비스: https://leehojun8450-netizen.github.io/backtest-lab/
- 저장소: https://github.com/leehojun8450-netizen/backtest-lab

**따라서 이 프로젝트에서 가장 나쁜 것은 "틀린 화려한 숫자"입니다.**
검토도 그 기준으로 해 주시면 됩니다.

---

## 읽을 수 있는 것 (raw URL — 항상 최신)

| 대상 | URL |
|---|---|
| 무한매수법 엔진 | https://raw.githubusercontent.com/leehojun8450-netizen/backtest-lab/main/tools/infinite-buy.html |
| 포트폴리오 엔진 | https://raw.githubusercontent.com/leehojun8450-netizen/backtest-lab/main/tools/portfolio.html |
| 변동성 끌림 엔진 | https://raw.githubusercontent.com/leehojun8450-netizen/backtest-lab/main/tools/volatility-drag.html |
| 프로젝트 문서 | https://raw.githubusercontent.com/leehojun8450-netizen/backtest-lab/main/README.md |
| 데이터 목록 | https://raw.githubusercontent.com/leehojun8450-netizen/backtest-lab/main/data/manifest.json |
| 홈 화면 | https://raw.githubusercontent.com/leehojun8450-netizen/backtest-lab/main/index.html |

계산 로직은 각 HTML 파일 하단 `<script>` 블록 안에 전부 있습니다. 별도 번들·난독화 없습니다.

---

## 회신 규격 (반드시 지켜 주십시오)

각 지적마다:

| 항목 | 내용 |
|---|---|
| **판정** | 사실 / 반증 / **확인 불가** |
| **근거** | **URL 필수.** 공식 기관(법령·거래소·국세청) 우선 |
| **재현** | 파일명 + 함수명 또는 코드 조각, 어떤 조건에서 발생하는지 |
| **심각도** | ① 결과값이 바뀜 ② 표현·문서 문제 ③ 개선 제안 |

## 금지 사항

1. **추측을 사실처럼 쓰지 마십시오.** 모르면 "확인 불가"라고 적어 주십시오.
   이 프로젝트는 근거 없는 수치를 삭제해 온 이력이 있습니다.
2. **수정된 코드를 보내지 마십시오.** 지적만 해 주시면 저희가 고치고 다시 검증받습니다.
   (동시 편집은 충돌을 만듭니다)
3. **수익률·성과 수치를 직접 계산해 제시하지 마십시오.**
   결과표의 모든 숫자는 실제 실행값이어야 합니다. 의심되면 "재계산 필요"라고만 적어 주십시오.

---

## 이미 알고 있는 한계 (다시 지적할 필요 없음)

| 한계 | 상태 |
|---|---|
| 상장폐지 종목 미포함 (생존편향) | 인지·명시 완료, 미해결 |
| 국내 배당 미반영 | 인지·명시 완료 (KRX 데이터 한계) |
| 국내 데이터 2014-05부터 | KRX 공개 API가 3,000거래일만 제공 |
| 레버리지·인버스 ETF 매매차익세 미반영 | 과표기준가 데이터 미확보 — 화면에 경고 표시 중 |
| 과최적화 검증(Walk-Forward·DSR·PBO) 없음 | **미착수 — 현재 최우선 과제** |
| 부분체결·시장충격·현금이자 미반영 | 인지·명시 완료 |
| 미국 양도소득세·환율 미반영 | 인지·명시 완료 |
| `release_date` 필드가 엔진에서 미사용 | 인지·명시 완료 (가격은 `d=r`이라 현재 영향 없음) |

---

## 검토 이력

| 회차 | 일자 | 결과 |
|---|---|---|
| 1차 | 2026-08-05 | 지적 14건 → 사실 11건 확인, 결과값 변경 4건 수정. 1건 부분 기각(근거: 실측) |
