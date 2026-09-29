# Repo 整理紀錄（2026-09-29）

這份文件記錄 GitHub repo 的整理原則、改名對照與處理過程，供日後查閱。

## 整理原則

- **🔒 Private ＝ 學校課程原樣教材練習**：未改動的上課內容屬老師智慧財產權，維持私人。
- **🌐 Public ＝ 已動手修改的作品**：程式碼已不是原本教材的樣子，作為自己的作品公開。
- **命名前綴即分組**：`feva-*`（fevawork Unity 課）、`erb-*`（erb VR 課）、`dungeon-*`（個人作品）。
- 改名一律由 GitHub 自動 301 轉址，舊連結、stars、issues 全部保留。

## 改名對照表（33 個）

### fevawork Unity 課程（`feva-*`）
| 舊名 | 新名 |
|---|---|
| `Lesson-01` ~ `Lesson-22`（01–13、21、22） | `feva-lesson-01` ~ `feva-lesson-22` |
| `fevawork21` | `feva-work-21` |
| `TEST` | `feva-test` |
| `newcombat` | `feva-newcombat` |
| `A2` | `feva-homework-02` |

### erb VR 課程（`erb-*`）
| 舊名 | 新名 |
|---|---|
| `VR0` | `erb-vr-blink-v0` |
| `VR` | `erb-vr-blink-v1` |
| `VR1` | `erb-vr-balls` |
| `VR-assignment` | `erb-vr-assignment` |
| `VR-door` | `erb-vr-door` |
| `homework` | `erb-vr-homework` |
| `movable-furniture` | `erb-vr-movable-furniture` |
| `Bouncing-Ball` | `erb-vr-bouncing-ball` |
| `Digital-Clock` | `erb-vr-digital-clock` |
| `Master-of-Cube` | `erb-vr-master-of-cube` |
| `MoC` | `erb-vr-master-of-cube-variant` |
| `blender-mcp` | `erb-blender-mcp` |

### 個人作品（`dungeon-*`）
| 舊名 | 新名 |
|---|---|
| `25done` | `dungeon-ai-game` |
| `OLD25` | `dungeon-ai-game-old` |

## Metadata

所有 repo 均已補上中文描述與分組標籤（topics）：
- 分組：`feva-course` / `erb-vr-course` / `portfolio`
- 技術：`unity3d` `csharp` `vr` `xr` `blender` `mcp` `python` `gamedev` 等

## 本地 clone 處理紀錄

- 改名後已更新 21 個本地 clone 的 git remote。
- 確認 4 個 repo 有未保存工作，**先 push 並在 GitHub 驗證 commit SHA 後**才刪除：
  - `feva-homework-02`（原 `A2`）：`8e60032` BGM 音訊與場景更新
  - `feva-lesson-13`：`751a796` Player.controller 更新
  - `dungeon-ai-game`（原 `25done`）：`ff7c99d` token 腳本與專案資產、`76e5934` NavMesh/Golem 重構
  - `feva-newcombat`（原 `newcombat`）：`e8b7aa0` HierarchyDumper 工具
- 其後刪除全部 21 個本地 clone，釋放約 22 GB。

## 使用方式

```bash
# 需要時重新 clone
git clone https://github.com/kalpakjian/feva-lesson-01.git

# 若仍有舊本地 clone，更新 remote 即可
git remote set-url origin https://github.com/kalpakjian/feva-lesson-01.git
```

舊名稱的 GitHub URL 會自動轉址到新名稱，書籤不需更動。

## ⚠️ 備忘

- `feva-homework-02` 的 `tokyo-hot-theme.mp3` 等 BGM 檔案位於公開 repo，若音樂有版權疑慮應從 repo 移除。
- `feva-lesson-14` ~ `feva-lesson-20`、`23`+ 目前沒有對應 repo（原命名即缺號）。