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
