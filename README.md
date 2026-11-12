# Remote Monitoring Windows（RMW）

Windows Agent／安裝載體與 Catalog 的公開固定版本入口。適用 Windows 10／11 x64；目前配對資源為 [RMW-v0.1.3-prerelease.20261109.1](https://github.com/kaikaiwang7777-png/remote-monitoring-windows-release/releases/tag/RMW-v0.1.3-prerelease.20261109.1)（Pre-release）。請使用配對 RMR 的正式流程，不自行替換 Catalog 或手工解壓安裝。

## 安裝與註冊

1. 管理員登入健康、HTTPS 信任有效且配套資源已驗證的 VPS WUI，進入「設備註冊」。
2. 選擇 1–15 台並按「產生安裝指令」。必要資源驗證與合法授權由系統流程處理；有安全確認時先閱讀後果。
3. 每台只複製對應列首次提供的獨立指令，在獲授權電腦的系統管理員 **Windows PowerShell 5.1** 執行。不要分享指令、Token 或註冊碼。
4. 依正式流程完成註冊與必要啟用。需要註冊碼時，使用 WUI 對應安裝／generation 的「完成註冊」流程，不用其他設備的碼。
5. WUI 安裝紀錄可查看及匯出安全診斷；另確認註冊、Windows Service、啟用及 VPS heartbeat。安裝開始、結束紀錄送達或 Service 存在都不等於全部上線成功。

已複製的指令含一次性秘密，只在首次回覆保留於該頁記憶體。重新整理、歷史查詢或重新登入不能重建。複製按鈕只在剪貼簿真正寫入後報成功。

## 故障與安全

指令未產生時先看資源／授權狀態，使用安全唯讀重新確認；既有 UNKNOWN 只查原申請。已到期紀錄不需要再停止，也不是資源核准失敗的證據。停止有效授權須選擇正確原授權並確認後果；停止結果未知不得盲目重送。

安裝失敗保留安全階段／原因碼，不修改 Windows ACL、停用來源／簽章／Hash 驗證或反覆執行原指令。連線中斷時不能保證即時回報；只有合法後續執行機會才能嘗試補送，不能把未收到紀錄直接判成失敗。不要公開完整命令、原始例外、密碼或憑證。

[RMR VPS 安裝與更新](https://github.com/kaikaiwang7777-png/remote-monitoring-release)。公開資源及隔離測試通過不等於 Windows 真機安裝／註冊已驗收；Owner 現場 P0 仍須實測。
