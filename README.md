# Retrigger Transformer

## What is this?

A simple example of a MIDI Transformer which is the new feature of Ableton Live 12 with Max for Live.

It divides notes by `Factor` note length.

## Disclaimer
**!!! This device is not for practical music workflow !!!**

Built-in `Arpeggiate` Transformer can perform as same as this device by setting `Distance` to 0sd.

## Dependency Environments
Ableton Live 12 / Max 8.6 or later

## Download

See Releases.

## Parameters

* `Factor`<br>
Represents the interval of transformed notes. 4 is for a quarter note.

* `Grid`<br>
When enabled, target notes are divided with the grid of the current MIDI clip.<br>
The `Factor` setting would be ignored.

* `Gate`<br>
The duration of transformed notes in percent of `Factor` length.

## Memorandum of M4L development for MIDI Transformer/Generator 

* `dictionary [dict name]` message from outlets of `live.miditool.in` is single symbol (string), however, it becomes a list of symbols after through out prepend objects or message objects like `set $1`.

* You can not open Max console from MIDI Transformers or Generators, however, you dan see the print outputs by a Max console window which is opened from regular M4L Instrument, MIDI effect, or Audio effect devices.

* You can obtain the global scale settings by LOM API with `get root_note` and `get scale_name` from path `live_set`.

## (Japanese) MIDIトランスフォーマー/ジェネレーターM4L開発メモ 

* `live.miditool.in` から出力される `dictionary [dict name]` は1つのシンボル (string型) ですが、prependオブジェクトや `set $1` といった内容のmessageオブジェクトをとおすとシンボルのリストに変わります。

* MIDIトランスフォーマー/ジェネレーターからMaxコンソールを開くことはできませんが、従来のM4Lデバイスから開いたMaxコンソールでMIDIトランスフォーマー/ジェネレーターがprintオブジェクトなどで出力する内容を確認できます。

* グローバルスケールの設定はLOM APIの `live_set` パスに追加された `get root_note` および `get scale_name` で取得できます。