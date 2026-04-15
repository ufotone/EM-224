EM‑224 — HONODORI Music Sequencer
多音源対応・PATTERN / SONG / MML の 3 モードを備えたマルチシーケンサー

EM‑224（通称 HONODORI）は、
SUBTRACTIVE / FM / PSG / DRUM / PCM を組み合わせて演奏できる
WEBベースのミュージックグルーブボックスです。

https://koodori.netlify.app/ を参考にしました。

Chrome, Safari等で動きます。(Web Audioを使用できるもの)


PATTERN（ループ制作）

SONG（曲構成）

MML（Music Macro Language）

の 3 モードを搭載し、テキストベースからステップ入力まで幅広い作曲スタイルに対応します。

📦 機能概要
PATTERN モード：最大 32 バンク、16/32 STEP のループ制作
SONG モード：最大 160 バンクを並べて曲を構築
MML モード：MML 文法で直接演奏（PATTERN/SONG を無視）

音源構成：

SUBTRACTIVE ×1
FM（4OP / 8ALG）×6
PSG（AY-3-8910 拡張）×3
DRUM ×8
PCM ×1
  ドラム MML 対応（%K %S %H …）
  PCM ロード（WAV/MP3 → 6bit ローファイ化）
ステップシーケンサー（16/32 STEP）


◆ モード説明
1. PATTERN モード
ループ素材（パターン）を作成するモード。

● 仕様
最大 32 バンク
各バンクは 16 STEP または 32 STEP
PLAY でループ再生　STOPで再生停止
1〜32 のバンクボタンでリアルタイム切り替え
「バンクをクリア」で選択中バンクを初期化

● 用途
ドラムループ
ベースリフ
ライブでのリアルタイム切り替え（マウスポチポチ)

2. SONG モード
PATTERN を並べて 1 曲として再生するモード。

● 仕様
最大 160 バンク（160 小節）
PATTERN のバンクを順番に登録
＋ ボタンで SONG に追加
CLEAR ALL で全初期化
LOOP OFF で 1 回のみ再生

● 用途
A/B/サビ構成
自動進行のライブセット

3. MML モード
Music Macro Language を直接実行するモード。  
PATTERN / SONG の内容は 完全に無視され、
MML がそのままシーケンサーとして動作します。

🎼 MML 記法リファレンス
記号	意味	例
C D E F G A B	音符	C4
+ / # / -	シャープ / フラット	C+ / D-
R	休符	R8
数字	音長	C8
.	付点	C4.
O + 数字	オクターブ	O4
オクターブ下/上	>C
L + 数字	デフォルト音長	L8
T + 数字	テンポ	T140
V + 数字	音量（0〜15）	V12
@ + 数字	音色	@3
&	タイ	C4&C4


MML チャンネル（A / B / C …）
コード
A: cdefgab
B: t120 o4 c4 c4 g4 g4
C: @3 l8 c8 r8 c8
A/B/C… で複数チャンネル
省略時は A のみ
各チャンネルで音色（@）を変えれば多声演奏が可能

🥁 ドラム MML（Channel D）
ドラム専用 MML は チャンネル D に記述します。

コマンド	音色
%K	KICK
%S	SNARE
%H	HAT
%TH	TOM Hi
%TM	TOM Mid
%TL	TOM Lo
%OH	Open HH
%CH	Close HH
%P	PCM


● 音長指定
%K8（八分音符）
省略時は L の値。

● 使用例
コード
L16 T120
%K R %K R %S R %K %K R %S R
%H %H %H %H

🥁 ドラム音源（8ch + PCM 1ch）
● ドラム 8ch（固定音色）
KICK / SNARE / HAT / TOM Hi / TOM Mid / TOM Lo / OpenHH / CloseHH
パラメータは ON/OFF と GAIN のみ
NOTE/VOL/PAN/TIE は無し（将来拡張予定）

● PCM 1ch
WAV / MP3 を読み込み可能
読み込み後は 6bit ローファイ化
ステップシーケンサーで ON/OFF
音程変更は不可（固定ピッチ）
X ボタンでアンロード
CLR PART で初期化
※ 現状再生 OFF が効かない既知仕様あり

🔷 PSG 音源（3ch）
AY-3-8910 をオマージュしつつ拡張。
https://github.com/IchigoJam/AY38910/　を参考にしました。

● 波形
SQ（矩形波）
SAW（のこぎり波）
TRI（三角波）
SIN（正弦波）
NOISE（ノイズ）

● 機能
デチューン
タイプ指定型エンベロープ
エンベロープタイム設定
MML 音色番号：@3 / @4 / @5


🎹 SUBTRACTIVE 音源（1ch）
減算方式のシンセ
フィルター・エンベロープ対応
リード・パッド・ベースなど幅広い用途

🎛 FM 音源（4OP / 8ALG × 6ch）
4 オペレーター8 アルゴリズム
FM1〜FM6 の 6ch

金属音・エレピ・ベースなど FM らしい音作りが可能


🎚 各音源のステップパラメータ（SUB / FM / PSG）
パラメータ	内容
NOTE	音程
VOL	音量（0〜15）
ON/OFF	発音の有無
TIE	タイ（スラー）
PAN	左右定位
STEP	16 / 32

📏 ステップシーケンサー（16 / 32 STEP）
PATTERN / DRUM / PCM すべて共通
16 STEP または 32 STEP
CLR PART で初期化

📘 ライセンス
フリー

📄 今後の予定（TODO）
ドラムPCM OFF 改善
PCM ピッチ変更




