# HangulIyagi 노린 (Norin)

노린(Norin)은 순수 우리말의 의미를 담은 독자적인 한글 입력기다.  
기존 입력기와 전혀 다른 구조로 설계된 새로운 입력 시스템이다.

외부 입력 프레임워크에 의존하지 않으며, 자체 구현된 입력 엔진으로 동작한다.

- HangulIyagi는 Linux 한글 입력의 새로운 구조를 완성했다.  
- 이제 한글 입력은 HangulIyagi 노린으로 날개를 달았다.
---

## 개발 배경

기존 한글 입력기는 조합 상태 기반 구조로 인해  
포커스 이동, 마우스 클릭 등에서 마지막 글자가 사라지는 문제가 존재한다.

이는 구조적인 한계이며 오랫동안 해결되지 않았다.

HangulIyagi는 이 문제를 해결하기 위해  
처음부터 새로운 입력 구조로 설계되었다.

👉 어떤 상황에서도 입력 중인 글자가 소실되지 않도록 설계됨

---

## 이름

아른 / 노린 (Norin) / 사른 / 하린 / 모린 / 나른 / 도린 / 라른

“노린(Norin)”은 발음이 자연스럽고 제품 이름으로 사용하기 적합한 핵심 명칭이다.

---

## 특징 (핵심 차별점)

### <sub>🔴 노린은 기존 한글 입력기와 입력 방식 자체가 다르다</sub>  
- <sub>조합 중심 구조를 벗어나 입력 흐름 자체를 재설계한 완전히 다른 방식</sub>

### <sub>🔵 편안한 진짜 한글 입력기</sub>  
- <sub>타이핑 중 끊김 없이 자연스럽게 이어지는 입력 경험을 제공</sub>

### <sub>🟣 마지막 글자까지 검색에서 인식</sub>  
- <sub>입력이 완전히 끝나기 전 상태에서도 마지막 글자까지 검색과 인식이 유지됨</sub>  

---

### ⚡ 완성형 직출력 입력

- ㅏ → 아  
- ㅗ → 오  
- ㅠ → 유  

👉 초성 없이 즉시 완성 글자 생성

---

### 🚀 입력 속도 향상

기존:
- ㅇ + ㅏ → 아

노린:
- ㅏ → 아

👉 입력 횟수 감소  
👉 상태 전환 제거  
👉 타이핑 리듬 유지

---

### 🧠 구조적 차이

기존 입력기:
- 조합 상태 중심
- 끝문자 소실 가능

노린:
- 완성 중심 구조
- 상태 최소화
- 입력 흐름 단순화

👉 구조적으로 문제 발생 차단

---

### 🎯 설계 철학

- 불필요한 입력 제거
- 최소한의 상태 처리
- 빠르고 끊김 없는 입력

---

### ⚠️ 의도된 차이

- 모음 입력 시 항상 완성 글자로 변환됨
- 순수 모음 단독 입력 제한됨 (예: ㅠ 단독 입력 어려움)

👉 속도와 안정성을 위한 설계 선택

---

## 📊 입력 방식 비교

| 항목 | 기존 입력기 | HangulIyagi |
|------|------------|-------------|
| 입력 구조 | 조합 기반 | 완성 직출력 |
| 입력 단계 | 2단계 이상 | 1단계 |
| 상태 관리 | 있음 | 최소화 |
| 출력 방식 | 조합 후 출력 | 즉시 출력 |
| 초성 ㅇ | 필요 | 불필요 |
| 입력 지연 | 있음 | 거의 없음 |
| 타이핑 흐름 | 끊김 | 유지 |
| 끝문자 문제 | 존재 | 없음 |
| 순수 모음 | 가능 | 제한 |
| 수정 방식 | 조합 단위 | 키 단위 |

---

## ⚡ 속도 비교

| 항목 | 기존 | 노린 |
|------|------|------|
| 입력 키 수 | 100% | 약 70~80% |
| 입력 효율 | 기준 | +20~30% |
| 체감 속도 | 기준 | +30~70% |
| 입력 지연 | 있음 | 거의 없음 |

---

## 🔥 핵심

👉 ㅇ 없이 한글 완성  
👉 입력 단계 감소 → 속도 증가  
👉 상태 제거 → 안정성 확보  
👉 즉시 출력 → 리듬 유지  
👉 키 단위 삭제 → 구조 단순화  

---

## 지원 환경

- Linux (GNOME, KDE)
- Wayland / X11

---

## 기능

- 두벌식 한글 입력 (자체 엔진)
- 한/영 전환
- 쌍자음 입력
- 포커스 변경 시 자동 입력 확정
- 빠른 키 단위 삭제

---

## 설치

### 1. 다운로드

GitHub 릴리즈에서 파일 3개를 다운로드:

| 파일 | 설명 |
|------|------|
| `hanguliyagi` | 입력기 데몬 (IBus 불필요, 자체 D-Bus 구현) |
| `im-hanguliyagi.so` | GTK3 IM 모듈 |
| `libim-hanguliyagi.so` | GTK4 IM 모듈 |

---

### 2. 설치

터미널에서 다운로드 폴더로 이동 후 실행:

```bash
# 데몬 실행 파일
sudo cp hanguliyagi /usr/local/bin/
sudo chmod +x /usr/local/bin/hanguliyagi

# GTK3 IM 모듈
GTK3_IM=$(pkg-config --variable=libdir gtk+-3.0)/gtk-3.0/3.0.0/immodules
sudo mkdir -p "$GTK3_IM"
sudo cp im-hanguliyagi.so "$GTK3_IM/"
sudo gtk-query-immodules-3.0 --update-cache

# GTK4 IM 모듈
GTK4_IM=$(pkg-config --variable=libdir gtk4)/gtk-4.0/4.0.0/immodules
sudo mkdir -p "$GTK4_IM"
sudo cp libim-hanguliyagi.so "$GTK4_IM/"
```

---

### 3. 환경변수 설정

`~/.profile` 또는 `~/.bashrc` 에 추가:

```bash
export GTK_IM_MODULE=hanguliyagi
export QT_IM_MODULE=ibus
export XMODIFIERS=@im=hanguliyagi
```

적용:

```bash
source ~/.profile
```

---

### 4. 실행

로그아웃 후 다시 로그인하면 자동 시작됩니다.

수동 실행:

```bash
hanguliyagi &
```

---

## 사용 방법

| 키 | 동작 |
|----|------|
| 한/영 키 | 한영 전환 |
| Shift+Space | 한영 전환 |
| 우측 Alt | 한영 전환 |
| Shift+자음 | 쌍자음 입력 |
| Backspace | 글자 단위 삭제 |

---

## 제거

```bash
sudo rm /usr/local/bin/hanguliyagi

GTK3_IM=$(pkg-config --variable=libdir gtk+-3.0)/gtk-3.0/3.0.0/immodules
sudo rm "$GTK3_IM/im-hanguliyagi.so"
sudo gtk-query-immodules-3.0 --update-cache

GTK4_IM=$(pkg-config --variable=libdir gtk4)/gtk-4.0/4.0.0/immodules
sudo rm "$GTK4_IM/libim-hanguliyagi.so"
```

`~/.profile` 에서 환경변수 3줄 제거 후 로그아웃/로그인.

---

## 개발

IYAGI INC
