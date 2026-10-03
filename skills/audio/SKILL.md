# audio skill

## Purpose

音に関する知識を横断的に扱うための基盤スキル。

対象は「音声処理」だけではなく、**Device / Input / Output / DSP / Voice / TTS / Music / MIDI / OSC / Network / Visual / Space / AI** まで含む。

research-audio が audio knowledge の正本を持つ。
kana はこの知識を探索・利用し、未知の領域を research-audio に委譲する。

## Responsibility

この skill は次を知識領域として扱う。

- Device
- Audio I/O
- Voice / Speech
- TTS / STT
- Music
- MIDI
- OSC
- DSP
- Synthesis
- Sampling
- Effects
- Mixing / Mastering
- Spatial Audio
- Live Performance
- Network Audio
- Web Audio
- DAW / Sequencer
- Visual / Audio Reactive
- AI Audio
- Physical Installation

## Knowledge model

基本単位:

```text
Device
  ↓
Capability
  ↓
Input / Output
  ↓
Event / Signal
  ↓
Transport
  ↓
Process
  ↓
Result
  ↓
Evidence
```

### Device

音に関係する実体。

例:

- smartphone
- microphone
- speaker
- headphone
- audio interface
- mixer
- MIDI controller
- synthesizer
- sampler
- PA
- sensor
- computer
- browser
- embedded device

### Capability

Device が何をできるか。

例:

- audio.input
- audio.output
- audio.record
- audio.playback
- audio.volume
- audio.mute
- midi.note
- midi.cc
- midi.pitchbend
- sensor.motion
- sensor.orientation
- speech.recognition
- speech.synthesis
- music.generate
- music.sequence
- dsp.filter
- dsp.delay
- dsp.reverb
- spatial.position

## Audio domains

### 1. Device

物理機器・OS・ブラウザ・仮想デバイスを調査する。

確認すること:

- input
- output
- protocol
- API
- permission
- latency
- sample rate
- channel
- platform
- connectivity

### 2. Voice

音声を扱う。

- microphone
- speech recognition
- speech synthesis
- voice conversion
- diarization
- speaker identification
- voice activity detection
- phoneme / pronunciation
- prosody
- emotion / style

### 3. TTS

Text-to-Speech を独立した知識領域として扱う。

記録対象:

- engine
- model
- language
- voice
- style
- pronunciation
- SSML / phoneme
- streaming
- latency
- audio format
- local / cloud
- API
- license

### 4. Music

音楽生成・演奏・構成を扱う。

- note
- chord
- scale
- rhythm
- tempo
- pattern
- sequence
- arrangement
- synthesis
- sample
- generative music
- AI music
- live coding
- composition

### 5. MIDI

- MIDI 1.0
- MIDI 2.0
- note
- velocity
- CC
- pitch bend
- program change
- clock
- SysEx
- MIDI device
- Web MIDI
- virtual MIDI
- network MIDI

### 6. OSC

- OSC message
- address
- argument
- bundle
- timetag
- UDP
- WebSocket bridge
- OSC ↔ MIDI
- OSC ↔ audio
- OSC ↔ visual

Browser から UDP/OSC が直接使えるとは仮定しない。
必要なら bridge を記録する。

### 7. DSP

- oscillator
- filter
- envelope
- LFO
- FFT
- convolution
- delay
- reverb
- distortion
- compressor
- limiter
- EQ
- spatialization

### 8. Web / JS Audio

- Web Audio API
- AudioWorklet
- MediaDevices
- Web MIDI
- WebSocket
- WebRTC
- Canvas
- WebGL
- WebGPU
- Tone.js
- p5.js
- Strudel
- Pure Data / WebPd

ブラウザ固有の permission / HTTPS / device support を必ず記録する。

### 9. Network Audio

- WebSocket
- WebRTC
- RTP
- OSC
- MIDI network
- streaming
- synchronization
- clock
- latency
- jitter
- discovery

### 10. Spatial Audio

基本モデル:

```text
Source
  +
Position
  +
Orientation
  +
Listener
  +
Room
  ↓
Spatial Audio
```

- stereo
- binaural
- ambisonics
- HRTF
- 3D positioning
- room simulation
- multi-speaker
- installation

### 11. AI Audio

- TTS
- STT
- voice conversion
- music generation
- sound generation
- audio understanding
- transcription
- separation
- enhancement
- tagging
- embeddings
- multimodal models

## Evidence

すべての知識は可能な限り Evidence と結び付ける。

Evidence level:

```text
spec
docs
code
prototype
device
measurement
unknown
```

Status:

```text
idea
research
prototype
working
limited
unavailable
rejected
```

unknown を working とみなさない。

## Research record

最小記録:

```yaml
id:
question:
domain:
devices:
inputs:
outputs:
capabilities:
transports:
environment:
result:
limitations:
evidence:
status:
next:
```

## Delegation

kana が audio に関する未知を発見したら、この skill / research-audio に委譲する。

```text
kana
  ↓
audio skill
  ↓
research question
  ↓
research / experiment
  ↓
evidence
  ↓
research-audio knowledge
  ↓
kana
```

kana は知識の正本を持たない。
**audio knowledge の正本は research-audio が持つ。**

## Rules

1. 音声・音楽・機器を分断しすぎない。
2. Device と Transport を分離する。
3. Capability を先に確認する。
4. 実機で確認した結果を優先する。
5. API の存在だけで「使える」と判断しない。
6. Permission / HTTPS / OS / Browser 制約を記録する。
7. 失敗した実験も記録する。
8. TTS と Music を同じ「生成AI」に丸めない。
9. MIDI / OSC / Audio を必要に応じて橋渡しする。
10. Knowledge は人間と agent が共同で更新する。
11. 未知を未知のまま残す。
12. 抽象化は実験の後に行う。

## Definition of Done

未知の audio technology が、

```text
Question
→ Research
→ Capability
→ Minimal experiment
→ Observe
→ Evidence
→ Record
→ Knowledge
→ Next question
```

まで進めば完了。

## Core principle

> research-audio は「音声技術のリンク集」ではない。
>
> Device から TTS、Music、MIDI、OSC、DSP、AI、空間音響まで、
> **実際に何ができるのかを人間とエージェントで確かめ、知識として残す研究室である。**
