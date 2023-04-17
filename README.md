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

## 相關連結

- [Configure Windows Authentication in ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/security/authentication/windowsauth?view=aspnetcore-7.0&tabs=visual-studio&WT.mc_id=DT-MVP-4015686)
- [奇技淫巧 - ASP.NET 同時支援 Form 及 Windows 驗證](https://blog.darkthread.net/blog/mix-form-win-auth/)
- [ASP.Net 同時使用Windows Authentication與Forms Authentication混合認證 Mixed Security](https://blog.tenyi.com/2012/12/aspnet-windows-authenticationforms.html)