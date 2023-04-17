## Publish

- �o�� MixedWindowsAuthenticate

    ```sh
    cd MixedWindowsAuthenticate
    dotnet publish -c Release -o g:\dist
    cd ..
    cd ADLogin
    dotnet publish -c Release -o g:\dist\ADLogin
    ```

- �N `g:\dist` ���p�쯸�x�ڥؿ�

- �N `ADLogin` �ন���ε{��

    �`�N�G���x�ڥؿ��P ADLogin ����@�άۦP�����ε{������(AppPool)

- �]�w `ADLogin` ���ε{���� Authentication

    ���ΰΦW����

    �ҥ� Windows ����

## ����

- �}�� `ADLogin` �� `/userid` API

    http://DOMAIN/ADLogin/userid

- �}�ҭ���

    http://DOMAIN/

    �I���u���o Windows �{�Ҫ� userid�v���s�h�I�s Windows Authentication ���U�� API

    �d�� alert �T���O�_��ܨϥΪ� AD �b��

## �����s��

- [Configure Windows Authentication in ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/security/authentication/windowsauth?view=aspnetcore-7.0&tabs=visual-studio&WT.mc_id=DT-MVP-4015686)
- [�_�޲]�� - ASP.NET �P�ɤ䴩 Form �� Windows ����](https://blog.darkthread.net/blog/mix-form-win-auth/)
- [ASP.Net �P�ɨϥ�Windows Authentication�PForms Authentication�V�X�{�� Mixed Security](https://blog.tenyi.com/2012/12/aspnet-windows-authenticationforms.html)