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

1. **Clone o repositório**:
   - Acesse o terminal e execute o comando abaixo para clonar o repositório para sua máquina:
   ```bash
   git clone https://github.com/seuusuario/nome-do-repositorio.git
   cd nome-do-repositorio
Instale as dependências:

2. **Abra o terminal no VS Code ou na sua IDE favorita e execute o comando para instalar as dependências do projeto:**

`bash:
flutter pub get`

Isso vai baixar todos os pacotes necessários para o projeto, incluindo o shared_preferences que será utilizado para salvar os lembretes.

**3. Adicione o pacote shared_preferences no pubspec.yaml:**
Abra o arquivo `pubspec.yaml` no seu projeto e adicione o seguinte pacote na seção `dependencies`:
`dependencies:
  flutter:
    sdk: flutter
  flutter_local_notifications: ^9.1.4
  intl: ^0.17.0
  timezone: ^0.8.0
  shared_preferences: ^2.0.11  # Adicione esta linha`

Depois de salvar o arquivo `pubspec.yaml`, execute o comando `flutter pub get` novamente no terminal para garantir que o pacote `shared_preferences` seja instalado.

**4 Substitua o código do `main.dart`:**

Substitua o conteúdo do arquivo main.dart (ou o arquivo correspondente onde o código principal está) pelo código que você forneceu anteriormente. Isso incluirá a implementação de lembretes e notificações locais.

**5. Execute o aplicativo:**
Conecte um dispositivo Android ou inicie um emulador e execute o aplicativo com o comando.Com esse ultimo passo o aplicativo roda no dispositivo ou emulador, permitindo que você adicione, veja e remova lembretes com notificações locais.

```bash
flutter run

