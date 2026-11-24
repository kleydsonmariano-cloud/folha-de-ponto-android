# Folha de Ponto — projeto Android offline

O projeto abre o PWA original como conteúdo local em um WebView Android. A tela não depende de hospedagem nem de internet para funcionar. Os dados ficam no armazenamento local do aplicativo.

## Gerar o APK usando somente o celular (GitHub Actions)
1. No celular, entre em https://github.com e crie uma conta ou faça login.
2. Crie um repositório novo (pode ser privado).
3. Extraia este ZIP no celular e envie o conteúdo da pasta `FolhaDePontoAndroid` para a raiz do repositório. É importante enviar também a pasta oculta `.github/workflows` e o arquivo `build-apk.yml` dentro dela.
4. No repositório, abra a aba **Actions** e habilite os workflows, se o GitHub solicitar.
5. Selecione **Gerar APK Android** e toque em **Run workflow**.
6. Quando terminar com sucesso, abra a execução e baixe o artefato **Folha-de-Ponto-APK**. O ZIP baixado contém `app-debug.apk`.
7. Abra o APK no celular e autorize a instalação de apps dessa origem, se o Android pedir.

## Compilar em computador
Abra a pasta no Android Studio e execute Build > Build APK(s), ou rode `gradle assembleDebug` com Android SDK instalado.

## Atenção
- APK debug serve para instalar/testar; publicação na Play Store exige assinatura de distribuição.
- Os registros ficam no aparelho. Limpar os dados ou desinstalar pode apagá-los.
- Impressão e PDF devem ser testados no aparelho; `window.print()` pode precisar de integração Android adicional.
