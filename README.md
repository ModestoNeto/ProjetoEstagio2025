# ProjetoEstagio2025
# Lembretes Visuais com Notificações Locais

Este é um aplicativo Flutter que permite criar lembretes visuais com notificações locais. O usuário pode adicionar, visualizar e remover lembretes, que são agendados para um horário específico, e receber notificações no momento selecionado.

## Funcionalidades

- **Adicionar lembretes**: O usuário pode inserir um título e escolher a data e hora do lembrete.
- **Notificações locais**: O aplicativo agenda notificações para o horário selecionado.
- **Excluir lembretes**: O usuário pode remover um lembrete e a notificação correspondente.
- **Suporte ao fuso horário**: O aplicativo usa a biblioteca `timezone` para agendar notificações de acordo com o fuso horário local.

## Tecnologias Utilizadas

- Flutter
- `flutter_local_notifications`
- `intl`
- `timezone`
- `shared_preferences`

## Como Rodar o Projeto

### Passos para rodar o aplicativo

### 1. Clone o repositório

```bash
git clone https://github.com/seuusuario/nome-do-repositorio.git
cd nome-do-repositorio
```

### 2. Instale o Flutter

Se você ainda não tem o Flutter instalado:

- Acesse: https://docs.flutter.dev/get-started/install  
- Siga as instruções para o seu sistema operacional (Windows, macOS ou Linux)  
- Adicione o Flutter ao seu `PATH`  
- Confirme a instalação com:

```bash
flutter doctor
```

Resolva qualquer pendência indicada no relatório.

### 3. Verifique e atualize o `pubspec.yaml`

Certifique-se de que o seu arquivo `pubspec.yaml` contenha as dependências:

```yaml
dependencies:
  flutter:
    sdk: flutter
  flutter_local_notifications: ^9.1.4
  intl: ^0.17.0
  timezone: ^0.8.0
  shared_preferences: ^2.0.11
```

Depois, instale os pacotes:

```bash
flutter pub get
```

### 4. Configure o Android (para notificações locais)

No arquivo `android/app/src/main/AndroidManifest.xml`, adicione as permissões:

```xml
<uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED"/>
<uses-permission android:name="android.permission.SCHEDULE_EXACT_ALARM"/>
```

Dentro da tag `<application>`, adicione:

```xml
<receiver android:name="com.dexterous.flutterlocalnotifications.ScheduledNotificationBootReceiver" android:exported="true">
    <intent-filter>
        <action android:name="android.intent.action.BOOT_COMPLETED"/>
        <action android:name="android.intent.action.MY_PACKAGE_REPLACED"/>
    </intent-filter>
</receiver>
```

### 5. Substitua o conteúdo do `main.dart`

Abra o arquivo `lib/main.dart` e cole o código principal da aplicação, incluindo a lógica de lembretes, notificações e armazenamento.

### 6. Execute o aplicativo

Conecte um dispositivo físico ou inicie um emulador e rode o app com:

```bash
flutter run
```

---

## 🔔 Lembretes Visuais com Notificações e Feedback

Este projeto Flutter permite que o usuário crie lembretes com data e hora, receba notificações locais e envie feedback com avaliação de 1 a 5 estrelas e sugestões.

---

## ✅ Pré-requisitos

- Flutter instalado e funcionando (`flutter doctor`)
- Emulador ou dispositivo físico com Android API 21+

---

## 📦 Dependências (pubspec.yaml)

```yaml
dependencies:
  flutter:
    sdk: flutter
  flutter_local_notifications: ^15.1.1
  intl: ^0.18.1
  timezone: ^0.9.2

