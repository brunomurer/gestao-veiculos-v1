# GUIA DE IMPLEMENTAÇÃO
## Sistema de Gestão de Veículos

---

Este guia descreve o processo de instalação e configuração do Sistema de Gestão de Veículos.

> **NOTA:** Para realizar a instalação, você precisará do arquivo `codigo.gs` (script do sistema) que é fornecido junto com a licença de uso ou no pacote de entrega.

---

## 🚀 INSTALAÇÃO PASSO A PASSO

### PASSO 1: Criar a Planilha Principal

1. Acesse **Google Drive** (drive.google.com)
2. Clique em **Novo** > **Planilha Google**
3. Renomeie para: `Sistema de Gestão de Veículos`

### PASSO 2: Instalar o Sistema

1. Na planilha, vá em **Extensões** > **Apps Script**
2. Apague qualquer código que estiver no editor.
3. **Cole o conteúdo do script `codigo.gs`** (fornecido separadamente).
4. Salve o projeto com o nome `Sistema Gestão Veículos`.

### PASSO 3: Inicialização Automática

1. No editor, selecione a função `instalarSistema`.
2. Clique em **Executar** (Play ▶️).
3. Autorize as permissões solicitadas (acesso ao Drive, Planilhas e Email).
4. Aguarde a mensagem de "Sucesso".

O sistema criará automaticamente todas as abas, proteções e configurações necessárias.

---

## 📝 PRÓXIMOS PASSOS

Após a instalação do código, siga o restante da configuração:

### 1. Criar Formulários
Use o menu **"🚗 Gestão de Veículos"** que aparecerá na sua planilha para criar automaticamente:
- Formulário de Solicitação
- Formulário de Início de Corrida
- Formulário de Fim de Corrida

### 2. Configurar Usuários
Acesse a aba **"Usuários"** criada pelo sistema e cadastre:
- Gestores
- Motoristas
- Solicitantes

### 3. Distribuir Acessos
Envie os links dos formulários (gerados no passo 1) para os respectivos usuários, juntamente com os **Manuais em PDF** disponíveis neste repositório.

---

## 📚 DOCUMENTAÇÃO DE APOIO

Consulte os outros arquivos deste repositório para detalhes operacionais:

- **MANUAL_MOTORISTA.md**: Instruções para os condutores.
- **MANUAL_SOLICITANTE.md**: Instruções para quem pede veículos.
- **CONFORMIDADE_LGPD.md**: Detalhes sobre dados e privacidade.

---

**Suporte:**
Em caso de dúvidas na implementação, consulte o suporte técnico fornecido com sua licença.
