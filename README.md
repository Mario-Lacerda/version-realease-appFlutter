# **Desafio Dio -  Criando a Versão de Release do seu App com Flutter**



Para criar a versão de release do seu app com Flutter, você precisará seguir os seguintes passos:

1. Criar uma chave de assinatura.
2. Configurar o seu projeto para assine bundles.
3. Compilar o seu projeto para a versão de release.



### **1. Criar uma chave de assinatura**

A primeira coisa que você precisa fazer é criar uma chave de assinatura. Para isso, você pode usar o seguinte comando:

```plaintext
flutter create-keychain-file -t codesign -u seu-email
```



Este comando irá criar um arquivo chamado `codesign.keychain` na sua pasta `~/Library/Keychains/System.keychain`.



### **2. Configurar o seu projeto para assine bundles**

Para configurar o seu projeto para assinar bundles, você precisará adicionar as seguintes linhas ao seu arquivo `pubspec.yaml`:

```plaintext
flutter:
  uses-material-design: true
  assets:
    - images/icon.png
    - images/logo.png
    - images/background.png

flutter_app_release:
  name: Meu App
  description: Um app muito legal!
  version: 1.0.0
  build_number: 1
  icon: images/icon.png
  # Define o SHA-256 da chave de assinatura
  signing_key: sha256:<chave>
  # Define o nome do arquivo do bundle assinado
  output: build/release/app.aab
```



### **3. Compilar o seu projeto para a versão de release**

Para compilar o seu projeto para a versão de release, você pode usar o seguinte comando:

```plaintext
flutter build apk --release
```



Este comando irá criar um arquivo chamado `app.apk` na sua pasta `build/app/outputs/apk/release`. Este é o arquivo que você pode enviar para a Google Play Store ou outras lojas de aplicativos.

É isso! Agora você sabe como criar a versão de release do seu app com Flutter.



# Aplicativo de Lista de Tarefas em Flutter

Este é um simples de lista de tarefas desenvolvido em Flutter que permite aos usuários adicionar, remover e gerenciar tarefas diárias.


![Capturar](https://github.com/KamiahAlves/app-lista-de-tarefas/assets/31547468/f23ea912-b31d-49ed-a54d-70e8d2d1c7d9)


## O Que Aprendi

Durante o desenvolvimento deste projeto, tive a oportunidade de aprender e aprimorar várias habilidades e conceitos, incluindo:

- Utilização do framework Flutter para criar interfaces de usuário atraentes e funcionais.
- Gerenciamento de estados no Flutter usando o widget `StatefulWidget`.
- Trabalhar com listas e manipulação de dados dinâmicos em aplicativos móveis.
- Interação com elementos de interface do usuário, como botões e listas.
- Implementação de funcionalidades básicas, como adicionar e remover itens da lista.
- Personalização da aparência do aplicativo, incluindo a AppBar e ícones.
- Experiência prática no uso do VS Code como ambiente de desenvolvimento para o Flutter.
- Colaboração e versionamento de código usando o GitHub.

Este projeto serviu como um ótimo ponto de partida para minha jornada de aprendizado em desenvolvimento móvel com Flutter.



## Funcionalidades

- Adicionar uma nova tarefa.
- Remover uma tarefa da lista.
- Marcar tarefas como concluídas.
- Interface de usuário simples e intuitiva.



## Pré-requisitos

- Flutter instalado em seu sistema. Se você ainda não o fez, siga as [instruções de instalação do Flutter](https://flutter.dev/docs/get-started/install).



## Como Executar o Aplicativo

1. Clone este repositório para o seu computador:

   ```
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```

2. Navegue até o diretório do projeto:

   ```
   cd seu-repositorio
   ```

3. Execute o aplicativo:

   ```
   flutter run
   ```

   Isso iniciará o aplicativo no emulador ou dispositivo conectado.



## Personalização

Você pode personalizar este aplicativo adicionando mais recursos, como lembretes, categorização de tarefas ou sincronização em nuvem. Sinta-se à vontade para explorar o código-fonte e fazer as alterações que desejar.



## Contribuição

Contribuições são bem-vindas! Se você encontrar um problema ou desejar melhorar o aplicativo de alguma forma, sinta-se à vontade para abrir uma "issue" ou enviar um "pull request".



## Licença

Este projeto é licenciado sob a Licença MIT - consulte o arquivo [LICENSE](LICENSE) para obter detalhes.

**Desenvolvido por:** [Kamiah Alves](https://github.com/KamiahAlves) 

*Projeto desenvolvido com base no que foi estudado no Bootcamp da DIO em parceria com o Santander* 

