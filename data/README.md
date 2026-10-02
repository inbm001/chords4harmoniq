# data 폴더

장르마다 `data/<genre>/songs.jsonl` 하나입니다. 나중에 장르를 더할 때도 같은 자리에 폴더만 추가합니다.

## 지금 있는 장르

- `data/kpop-ballad/songs.jsonl` — K-pop·한국 발라드
- `data/jpop-ani/songs.jsonl` — J-pop 애니송(OP/ED, 애니 관련곡)

한 줄이 한 곡입니다. 가사 원문은 없고 코드 진행만 있습니다.

## 맞춤 규칙

- verified: 제목과 원곡 가수가 둘 다 맞음. 한·일·영 제목과 흔한 가수 로마자 표기는 같은 곡으로 봄.
- uncertain: 제목은 맞지만 가수가 다름(커버 등). 파일에는 남기되 그 곡으로 치지 않음. `artist`는 페이지에 적힌 가수입니다.
- mismatch: 다른 곡. 이 파일에 넣지 않음.
- 코드 순서와 반복 표기는 출처 그대로. `E`와 `E7`을 섞지 않음. 슬래시 코드는 출처에 있는 것만.
- `key`, `capo`는 페이지에 적힌 것만. 전조 UI 값은 넣지 않음.

## 출처

- 일본 곡: ChordWiki (`ja.chordwiki.org`)가 우선. 이번 50곡은 모두 거기에서 verified로 가져옴.
- 한국 곡: Ultimate Guitar가 우선. 이번 50곡은 모두 거기에서 가져옴(verified 47, uncertain 3).
- ChordTool은 코드 악보가 비어 있어 쓰지 않음. koreanchords.com은 여기서 DNS가 안 됨. e-chords.com은 526. 유료 악보 상점은 쓰지 않음. kpopchords.com은 무료 블로그로 일부 곡 코드가 있으나 이번 수집에서 저장된 건 없음.

## 새 장르

`data/<genre>/songs.jsonl` 폴더를 추가하면 됩니다. 예: `data/jpop-ballad/`. 장르 폴더를 섞지 않습니다.
