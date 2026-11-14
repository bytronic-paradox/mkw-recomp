# tests/c

C sources the Python tests next door build with the compiler at hand and run.

| File | Built by | What it checks |
|---|---|---|
| `t_switch2.c` | `test_switch2.py` | The Switch 2 controllers' protocol (`runtime/input/switch2_proto.h`): from seedds/mkw-neo (MIT), with reports and replies recorded from a left and a right Joy-Con 2 |
| `t_phonepad.c` | `test_phonepad.py` | Phones as controllers (`runtime/input/phonepad_proto.h`, `phonepad_srv.c`, `phonepad_cert.c`) and `runtime/core/base/qr.c`: the checks that need no socket, and `serve`, the server with a table for controllers that prints each event; no SDL, game or phone |
| `t_game_dir.c` | `test_game_dir.py`, `test_game_dir_windows.py` | Settings, installation discovery and log-folder discovery with real files and single-thread platform stubs; Windows uses UTF-16 file APIs and UTF-8 conversion through `wmain`; no game, SDL or GPU |
