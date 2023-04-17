## Publish

- 發行 MixedWindowsAuthenticate

    ```sh
    cd MixedWindowsAuthenticate
    dotnet publish -c Release -o g:\dist
    cd ..
    cd ADLogin
    dotnet publish -c Release -o g:\dist\ADLogin
    ```

- 將 `g:\dist` 部署到站台根目錄

- 將 `ADLogin` 轉成應用程式

    注意：站台根目錄與 ADLogin 不能共用相同的應用程式集區(AppPool)

- 設定 `ADLogin` 應用程式的 Authentication

    停用匿名驗證

    啟用 Windows 驗證

## 測試

- 開啟 `ADLogin` 的 `/userid` API

    http://DOMAIN/ADLogin/userid

- 開啟首頁

    http://DOMAIN/

    點擊「取得 Windows 認證的 userid」按鈕去呼叫 Windows Authentication 底下的 API

    查看 alert 訊息是否顯示使用者 AD 帳號
