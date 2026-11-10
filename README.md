# zmk-config-roBa

<img src="keymap-drawer/roBa.svg" >
## DYA Studio 対応 (このブランチ)

[DYA Studio](https://github.com/cormoran/dya-studio) から設定できるよう、cormoran 版 ZMK (`main+dya`) と関連モジュールを使う構成です。キーマップは `robaish+coropit@black` のものを使用し、Prospector (`prospector-zmk-module` v2.2.1) にも対応しています。

- `config/west.yml`: cormoran 版 ZMK / Zephyr 4.1 と DYA Studio 用モジュール群、Prospector モジュール
- `build.yaml`: ボード名を `xiao_ble//zmk` に変更 (Zephyr 4.1 のボード命名)
- `roBa_R.overlay` / `roBa_R.conf`: PMW3610 を cormoran 版ドライバに置き換え、トラックボールの感度・スクロールを入力プロセッサ (ランタイム) 化
- 注意: 旧ドライバの `ORIENTATION_0` / `INVERT_SCROLL_X` / スクロール加速などは cormoran 版にないため、向きやスクロールは実機で確認し DYA Studio または `roBa_R.conf` の `SWAP_XY` / `INVERT_*` で調整してください
