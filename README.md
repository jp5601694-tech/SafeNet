# SafeNet — projeto Android

Este é um projeto-fonte inicial para Android Studio.

## O que inclui
- Tela simples em português.
- Ativação e desativação de uma VPN local.
- Encaminhamento de consultas DNS para `1.1.1.3` (Cloudflare for Families), que filtra malware e conteúdo adulto no nível DNS.
- Não exige senha dentro do aplicativo.

## Como abrir
1. Instale o Android Studio.
2. Abra a pasta `SafeNetAndroid`.
3. Aguarde a sincronização do Gradle.
4. Execute em um aparelho Android (API 26 ou superior).
5. Ao ativar, aceite a solicitação de conexão VPN do Android.

## Limitações importantes
- Este pacote contém o código-fonte; não é um APK já compilado.
- O filtro DNS não é infalível: apps que usam DNS próprio, DoH/DoT embutido, proxy ou outra VPN podem contorná-lo.
- O Android permite apenas uma VPN ativa por vez.
- O serviço usa um resolvedor DNS familiar de terceiros. A disponibilidade e a política do resolvedor podem mudar.
- Para distribuição pública, é necessário testar em aparelhos reais, revisar o ciclo de vida do serviço e cumprir as políticas atuais do Android/Google Play.


## Gerar APK automaticamente pelo GitHub
1. Envie o conteúdo desta pasta para um repositório GitHub.
2. Abra a aba **Actions** do repositório.
3. Execute **Build SafeNet APK** com **Run workflow** (ou envie um commit para `main`).
4. Quando terminar, abra a execução e baixe o artefato **SafeNet-debug-apk**.
5. O APK estará dentro do ZIP do artefato.

O APK gerado será uma compilação de depuração, adequada para testes e instalação manual; não é uma versão assinada para publicação na Play Store.
