# research-audio

音について研究するための研究室。

## 役割

`research-audio` は、音に関する技術・事例・実験・制約を探索し、知識を蓄積する場所。

ここで扱うのは「完成した答え」だけではない。

- 何ができるか
- 何ができそうか
- 実際に何ができたか
- 何ができなかったか
- どんな条件ならできるか
- 次に何を調べるべきか

を記録する。

## kanaとの関係

- **research-audio** = 研究室
- **kana** = 探索エージェント
- **Knowledge Base** = 人間とエージェントが一緒に作る知識
- **Ontology** = 知識を整理するための共通語彙・関係

```text
research-audio
      │
      │ 研究・資料・実験
      ↓
 Knowledge Base
      ↕
     kana
  Explorer Agent
      ↕
    人間
      │
      └── 仮説・経験・判断
```

## 知識の作り方

知識は最初から固定しない。

`kana` が探索し、人間が問い・経験・判断を加え、実験で確認する。

```text
問い → 探索 → 候補 → 検証 → 実験 → 記録 → 知識 → 次の問い
```

未確認の情報は未確認として残す。失敗した実験も知識として残す。

## 基本原則

1. Research before abstraction
2. Evidence before assumption
3. Capability before command
4. Observation before control
5. 人間とエージェントで知識を作る
6. 未知を未知のまま記録する
7. 失敗を捨てない

## 現時点の対象

Browser / Web Audio / MIDI / OSC / WebSocket / Sensor / Pure Data / p5.js / Tone.js など、音に関係する技術とその組み合わせを探索する。

> research-audio は、音の正解を収集する場所ではない。
> 音の世界で「何ができるか」を一緒に発見する研究室である。