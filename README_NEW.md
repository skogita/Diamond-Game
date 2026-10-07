# Diamond Game — companion source for the book

[日本語](README.ja.md)

Design documents and code for the Diamond Game app built in ***Toward a Million Lines IV — Building Computer Players for the Diamond Game*** (Japanese title 『LLM で 100 万行のソフトウェア開発 IV — ダイヤモンドゲームの打ち手を作る』; Volume 4 of the series).

A Diamond Game (a Japanese relative of Chinese checkers) for three players on a star-shaped board: 181 squares, 15 pieces each, one of which is the king. Each seat can be a human or a computer. The computer player has 14 levels; each level adds one more idea on top of the last (search, weights learned from game records, Monte Carlo tree search, and elementary deep learning).

## Download

**Ready-to-run apps are on the [Releases](../../releases) page**, not in this repository.

| File | Contents |
|:---|:---|
| `diamond_en.zip` | **English edition.** Design documents, READMEs and screens in English (code comments stay in Japanese). Windows installer and Android APK, version 1.69.1 |
| `diamond.zip` | **Japanese edition.** Design documents and screens in Japanese. Same layout |

The apps are **not code-signed**, so Windows and Android may warn you (Windows: More info → Run anyway; Android: allow installs from unknown sources).

## What is in each ZIP

| Location | Contents |
|:---|:---|
| `prebuilt/windows/diamond-flutter-setup.exe` | The Windows installer. Double-click to install |
| `prebuilt/android/diamond-flutter.apk` | The Android app (release build) |
| `docs/` | Design documents (DD), 22 files, plus one list of RF and CR. Levels L1 to L4 |
| `requirements/` | Requirements, RF (9 items) and CR (50 items, CR-17 to CR-69), exported from the development system's database |
| `src/flutter/` | Dart code of the app (Flutter, Windows and Android) |
| `src/learn/` | Python that learns weights and networks from game records |
| `src/installer/` | The tool that builds the Windows installer |
| `experiments/` | The experiments of §7.13–§7.14 of the book (the no-search player): design documents and tool code. Not part of the app |
| `LICENSE`, `LICENSE-DOCS.md` | Terms of use (below) |

Not included: test files, the database itself, the book files, build output, and `local.properties`.

## Rules

The start window defaults to the Japanese preset (Diamond Game): the king finishes last by entering the goal ◎ (the top). Version 1.69.1 also fixed the general rules' default to this rule (CR-69).

---

## License

- **The author holds the copyright.**
- **The code is under the GNU General Public License v3.0 (GPL-3.0).** The full text is [`LICENSE`](LICENSE). **If you modify it and distribute it, you must publish the source under the same GPL-3.0.**
- **The design documents and the text are under the Creative Commons Attribution-ShareAlike 4.0 International license (CC BY-SA 4.0).** This covers `docs/`, the READMEs and the other written text of this repository, and the text of the matching book. See [`LICENSE-DOCS.md`](LICENSE-DOCS.md). **If you distribute what you changed, you must publish it under the same terms.**
- **If you use them, say so.** State where it came from (the title of the book and the name of this repository) and keep the copyright notice. If you changed it, say that you changed it.
- **In this project the design documents are the source of the code** (the tests and the code are generated from them). When you publish something made from this code, **publish the design documents together with the code.**
- Third-party components used by the code (Flutter and Dart packages, PyTorch, and so on) remain under their own original licenses.
- Provided "as is", without warranty — as the GPL-3.0 text says.
