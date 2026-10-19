# Codex Pets: Si

這裡提供一款以祀（Si）為主題的 Codex 寵物：[Codex Pets](https://developers.openai.com/codex/app/settings#pets)。祀是《明日方舟：終末地》中巨獸「歲」的代理人。

安裝之後，你寫 Code 時就不再是孤軍奮戰。

每當你完成任務、或是遇到突發狀況時，祀就會在旁邊帶著從容又有點高傲的神情看著你，像是在說：

「哼哼，呆瓜管理員，這種小事交給本姑娘就好，才不是特地來幫你的呢！」

![Si spritesheet](spritesheet.webp)

## 安裝

最簡單的安裝方式是在 Codex app 直接輸入以下提示詞：

```text
安裝 cdcd72/codex-pet-si repo 的 Codex Pet 給我的 Codex app 使用
```

如果你想手動安裝，這個 repo 的 CI 會產出 GitHub Pages 套件：

```text
https://cdcd72.github.io/codex-pet-si/si.codex-pet.zip
```

macOS 或 Linux 可在終端機執行：

```sh
curl -sL "https://cdcd72.github.io/codex-pet-si/si.codex-pet.zip" -o "/tmp/si.codex-pet.zip" && mkdir -p "$HOME/.codex/pets/si" && unzip -o "/tmp/si.codex-pet.zip" -d "$HOME/.codex/pets/si"
```

Windows PowerShell 可執行：

```powershell
New-Item -ItemType Directory -Force "$HOME/.codex/pets/si" | Out-Null
Invoke-WebRequest "https://cdcd72.github.io/codex-pet-si/si.codex-pet.zip" -OutFile "$env:TEMP/si.codex-pet.zip"
Expand-Archive -Path "$env:TEMP/si.codex-pet.zip" -DestinationPath "$HOME/.codex/pets/si" -Force
```

執行後，Codex 會在 `~/.codex/pets/si` 讀取這個寵物。

## 使用

1. 下載並解壓縮寵物檔案。
2. 確認 `~/.codex/pets/si` 內有 `pet.json` 與 `spritesheet.webp`。
3. 重新啟動 Codex 並到設定中的寵物選單選取 `Si`。
4. 到聊天視窗輸入 `/pet` 或從指令選單啟用寵物功能。
5. 啟用後，祀就會在介面中依狀態播放對應動畫。

## 檔案說明

- `pet.json`: 寵物的中繼資料。
- `spritesheet.webp`: 寵物的圖像素材。
- `AGENTS.md`: 祀的角色與性格設定。

## 授權說明

- 本專案為《明日方舟：終末地》（Arknights: Endfield）的非官方同人二次創作，僅供個人興趣與交流使用，**不得用於商業營利**。
- 創作內容遵循官方對二次創作的相關規範：不冒充官方、不暗示獲得官方背書、不含違法或損害角色與遊戲形象的內容。
- 角色「祀」及其相關名稱、設定與原始美術素材，其著作權與商標權均歸原權利人（GRYPH FRONTIER PTE. LTD. / 鷹角網絡 / 悠星網絡，以官方公告為準）所有。
- 本專案與上述公司沒有任何隸屬或合作關係；若權利人認為內容不妥，請聯繫作者，將立即處理。
