# dino_coder

🦕 **공룡 디펜스 로그라이트** — 떨어지는 버그를 막으며 코드(LOC)를 쌓는 픽셀 아트 게임. [claude_coder](https://github.com/tinkerer0/claude_coder) 공유 코어의 **공룡 에디션**이다.

바닥의 공룡이 5개 레인에서 좌우로 움직이며 버그를 자동 공격한다. 죽거나 종료하면 ★로 영구 강화 → 다시 도전. **5000 LOC = 배포 성공(승리)**.

## Status

- **Last reviewed:** 2026-07-17 (base `6945904`)
- **Maturity:** 플레이 가능한 단일 HTML 스킨/포크. 이 README 작성 시 게임을 실행·플레이하지는 않았다.
- **License:** 저장소에 라이선스 파일 없음 — 재사용 조건은 현재 명시되지 않음.

## 공유 코어 vs 이 에디션

**공유 (claude_coder / duck_coder와 동일 계열 로직):**

- 무기 17종 · 한 판 1개 장착 · 영구 스탯 3종(추론력/출력속도/컨텍스트) · 테마 5종
- 버그 타입·5레인·자동 공격·★ 상점·승리 조건 5000 LOC
- 조작: ←→ 또는 A/D, `M` 음소거, `Esc` 종료, `1`/`2`/`3` 배속, **터치 이동**
- 바닐라 JS + Canvas 단일 `index.html`, 픽셀 폰트 Galmuri(jsDelivr CDN)

**이 저장소 차이:**

- 주인공·배경 장식: `dinoShape` 공룡 (티라노 스타일 실루엣, 배경에 흐릿한 공룡 떼)
- 세이브 키: `dino_coder_v1` (claude/duck 세이브와 **공유되지 않음**)
- UI 액센트: 그린 (`--coral:#6cc24a`), 메뉴 부제 “공룡 에디션”
- 루트에 `clawd_ref.png` 없음 (단일 `index.html` + README)

형제: [claude_coder](https://github.com/tinkerer0/claude_coder), [duck_coder](https://github.com/tinkerer0/duck_coder).

## Quick start

저장소 루트에서 (이 리프레시 중에는 **실행하지 않음**):

```sh
python3 -m http.server 8080
# 브라우저: http://localhost:8080/

# 또는
open index.html   # macOS
```

GitHub Pages (`main` 루트, API상 `built`):
https://tinkerer0.github.io/dino_coder/

## 파일 맵

```
index.html   게임 전부
README.md    이 문서
```

## 데이터 · 네트워크 · 안전

- **저장:** `localStorage` 키 `dino_coder_v1` (로컬 브라우저만).
- **네트워크:** 게임 서버 없음. Galmuri 폰트 CDN 요청 가능.
- **비밀·자격증명:** 없음.

## License

라이선스 파일 없음.
