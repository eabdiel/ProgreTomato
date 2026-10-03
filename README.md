# ProgreTomato 🍅 (Alpha)

Windows automation recorder and replay workbench for mouse, keyboard, and clipboard workflows, with editable steps and target-window locking.

A project of **[ProgreTech LLC](https://progretech.com)**, owned and maintained by **Ed Rodriguez**. Third-party components and contributions retain their respective ownership and notices.

[Project website](https://progretech.com) · [Report an issue](https://github.com/eabdiel/ProgreTomato/issues) · [Contribute](CONTRIBUTING.md)

**ProgreTomato** is a Windows-only automation workbench that records user actions (mouse, keyboard, clipboard) into a step list, lets you edit/debug them, and replays them reliably using a target-window “lock” and window-relative coordinates.

This is an **early alpha** focused on recording/replay for internal tools (browser, SAP GUI, and Windows apps).


## How to Use
- Launch ProgreTomato
- Click Pick Target (click next window)
Then click the target app (browser / SAP GUI / Windows app)
- Ensure Target Lock is ON
- Click Start Recording
- Perform your workflow in the target app
- Click Stop
- Edit steps as needed
- Use:
  - Run for full replay
  - F10 to Step
  - F8 to Reset Step

---

## Key Features (Alpha)

- **Record** mouse clicks, typing, hotkeys, and clipboard copies
- **Target Lock** so the recorder ignores ProgreTomato UI interactions and records only the selected app
- **Pick Target (next click)**: click the button, then click your target app window to select it
- **Replay**
  - **Run** full automation
  - **Step** through one action at a time (F10)
  - **Reset Step** (F8)
- **Window-relative click recording** (normalized client coords) for better reliability when windows move
- **Project persistence**
  - Save/Load JSON
  - Export XLSX template (Inputs/Outputs + steps)

---

## Supported (Current)

- Windows 10/11
- Python 3.10+ recommended
- Tested with:
  - PySide6 (UI)
  - pynput (input capture/replay)
  - pywin32 (window introspection)
  - psutil (process info)

> Note: “Enterprise” apps (SAP GUI, internal portals) often require waits and robust locators (future roadmap).

---

## Setup (Dev)

```bash
git clone https://github.com/eabdiel/ProgreTomato.git
cd ProgreTomato

python -m venv .venv
.venv\Scripts\activate

pip install -r requirements.txt
python main.py
```

## Collaboration

Reproducible bug reports, platform compatibility, installation documentation, and small regression fixes are useful ways to help. Read [CONTRIBUTING.md](CONTRIBUTING.md) for issue reports, proposed changes, and attribution requirements.

## License and reuse

The repository includes MIT terms in [LICENSE](LICENSE). Preserve applicable copyright and license notices. Consult the full license for modification, distribution, and any source-provision requirements.

## More from ProgreTech

Explore [CodeSeal](https://codeseal.progretech.com) for signed software provenance and project history.

Discover the wider portfolio at [progretech.com](https://progretech.com). These links identify related products; they do not imply a bundled integration or shared license.
