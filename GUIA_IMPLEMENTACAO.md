# GUIA DE IMPLEMENTAÇÃO COMPLETO
## Sistema de Gestão de Veículos - Contrato Público Federal

---

## 📋 SUMÁRIO

1. [Pré-requisitos](#pré-requisitos)
2. [Instalação Passo a Passo](#instalação-passo-a-passo)
3. [Configuração dos Formulários](#configuração-dos-formulários)
4. [Configuração de Usuários e Permissões](#configuração-de-usuários-e-permissões)
5. [Deploy da Interface Mobile (PWA)](#deploy-da-interface-mobile-pwa)
6. [Testes e Validação](#testes-e-validação)
7. [Uso do Sistema](#uso-do-sistema)
8. [Manutenção e Backup](#manutenção-e-backup)
9. [Conformidade LGPD](#conformidade-lgpd)
10. [Troubleshooting](#troubleshooting)

---

## 🔧 PRÉ-REQUISITOS

### Conta Google Workspace ou Gmail
- Acesso ao Google Drive
- Acesso ao Google Sheets
- Acesso ao Google Forms
- Permissões para criar e executar Apps Script

### Conhecimentos Básicos
- Navegação no Google Drive
- Uso básico de planilhas
- Acesso a configurações de compartilhamento

---

## 🚀 INSTALAÇÃO PASSO A PASSO

### PASSO 1: Criar a Planilha Principal

1. Acesse **Google Drive** (drive.google.com)
2. Clique em **Novo** > **Planilha Google**
3. Renomeie para: `Sistema de Gestão de Veículos`
4. Salve a planilha

### PASSO 2: Adicionar o Código Apps Script

1. Na planilha, vá em **Extensões** > **Apps Script**
2. Delete o código padrão (`function myFunction() {}`)
3. Copie todo o conteúdo do arquivo `codigo.gs` fornecido
4. Cole no editor do Apps Script
5. Clique no **ícone de disquete** para salvar
6. Renomeie o projeto para: `Sistema Gestão Veículos`

### PASSO 3: Executar a Instalação Inicial

1. No editor do Apps Script, localize a função `instalarSistema`
2. Clique em **Executar** (botão play ▶️)
3. Na primeira execução, será solicitada autorização:
   - Clique em **Revisar permissões**
   - Selecione sua conta Google
   - Clique em **Avançado**
   - Clique em **Ir para Sistema Gestão Veículos (não seguro)**
   - Clique em **Permitir**
4. Aguarde a execução (pode levar 30-60 segundos)
5. Verifique se aparece o alerta: "Sistema instalado com sucesso!"

### PASSO 4: Verificar Abas Criadas

Volte à planilha e verifique se foram criadas as seguintes abas:
- ✅ Solicitações
- ✅ Corridas
- ✅ Usuários
- ✅ Log de Auditoria
- ✅ Backup
- ✅ Dashboard

### PASSO 5: Verificar Menu Personalizado

1. Recarregue a página da planilha (F5)
2. Verifique se apareceu o menu: **🚗 Gestão de Veículos**
3. Se não aparecer, aguarde 30 segundos e recarregue novamente

---

## 📝 CONFIGURAÇÃO DOS FORMULÁRIOS

### FORMULÁRIO 1: Solicitação de Corrida

1. No menu **🚗 Gestão de Veículos**, clique em:
   - **📝 Criar Formulário Solicitação**
2. Aguarde a criação (10-15 segundos)
3. Anote as URLs que aparecem no log:
   - **URL de edição**: Para você fazer ajustes
   - **URL pública**: Para compartilhar com solicitantes
4. Copie a **URL pública** e salve em local seguro

**Personalizações Opcionais:**
- Adicionar logo da instituição
- Personalizar cores (tema do formulário)
- Ajustar textos de ajuda

### FORMULÁRIO 2: Iniciar Corrida (Mobile)

1. No menu **🚗 Gestão de Veículos**, clique em:
   - **🚀 Criar Formulário Iniciar Corrida**
2. Anote as URLs
3. Copie a **URL pública** para os motoristas

**IMPORTANTE:** Este formulário deve ser preenchido APENAS pelos motoristas, no momento de iniciar a viagem.

### FORMULÁRIO 3: Encerrar Corrida (Mobile)

1. No menu **🚗 Gestão de Veículos**, clique em:
   - **🏁 Criar Formulário Encerrar Corrida**
2. Anote as URLs
3. Copie a **URL pública** para os motoristas

**IMPORTANTE:** Este formulário deve ser preenchido APENAS pelos motoristas, ao retornar da viagem.

### CONFIGURAR RESPOSTAS DOS FORMULÁRIOS

Para cada formulário criado:

1. Abra o formulário (use a URL de edição)
2. Clique em **Respostas**
3. Clique no ícone do Google Sheets (link verde)
4. Selecione **Selecionar planilha existente**
5. Escolha: `Sistema de Gestão de Veículos`
6. Clique em **Selecionar**

---

## 👥 CONFIGURAÇÃO DE USUÁRIOS E PERMISSÕES

### PASSO 1: Adicionar Usuários

1. Acesse a aba **Usuários** na planilha
2. Adicione uma linha para cada usuário com:
   - **Email**: Email institucional do usuário
   - **Nome**: Nome completo
   - **Perfil**: Escolha um dos três:
     - `Gestor` - Acesso total, pode gerar relatórios
     - `Motorista` - Pode iniciar/encerrar corridas
     - `Solicitante` - Pode apenas solicitar corridas
   - **Setor**: Departamento do usuário
   - **Ativo**: `Sim` ou `Não`
   - **Data Cadastro**: Data de hoje

**Exemplo:**

| Email | Nome | Perfil | Setor | Ativo | Data Cadastro |
|-------|------|--------|-------|-------|---------------|
| joao@orgao.gov.br | João Silva | Gestor | TI | Sim | 28/01/2025 |
| maria@orgao.gov.br | Maria Santos | Motorista | Administrativo | Sim | 28/01/2025 |
| pedro@orgao.gov.br | Pedro Costa | Solicitante | RH | Sim | 28/01/2025 |

### PASSO 2: Configurar Permissões de Compartilhamento

1. Clique em **Compartilhar** (canto superior direito)
2. Adicione todos os usuários:
   - **Gestores**: Permissão de **Editor**
   - **Motoristas**: Permissão de **Leitor** (eles usarão apenas os formulários)
   - **Solicitantes**: Não precisam de acesso à planilha
3. Configure: **Pessoas com o link podem visualizar**
4. Clique em **Concluído**

### PASSO 3: Distribuir URLs dos Formulários

Envie por email para cada grupo:

**Para Solicitantes:**
- URL do Formulário de Solicitação
- Instruções de uso

**Para Motoristas:**
- URL do Formulário Iniciar Corrida
- URL do Formulário Encerrar Corrida
- Instruções detalhadas

**Para Gestores:**
- URL da Planilha Principal
- Todas as URLs dos formulários
- Manual completo

---

## 📱 DEPLOY DA INTERFACE MOBILE (PWA)

### OPÇÃO 1: Usando Google Sites (Recomendado)

1. Acesse **Google Sites** (sites.google.com)
2. Clique em **+** para criar novo site
3. Escolha **Página em branco**
4. Configure:
   - Título: `Gestão de Veículos - Mobile`
5. Adicione uma seção **Incorporar**
6. Cole o código HTML do arquivo `interface-mobile.html`
7. **IMPORTANTE**: Substitua os placeholders:
   - `[URL_FORM_SOLICITACAO]` → URL real do formulário
   - `[URL_FORM_INICIAR]` → URL real do formulário
   - `[URL_FORM_ENCERRAR]` → URL real do formulário
   - `[URL_PLANILHA]` → URL da planilha
8. Clique em **Publicar**
9. Copie a URL gerada
10. Compartilhe com os usuários

### OPÇÃO 2: Hospedagem Externa (GitHub Pages)

1. Crie uma conta no **GitHub** (github.com)
2. Crie um novo repositório público
3. Faça upload dos arquivos:
   - `interface-mobile.html` (renomeie para `index.html`)
   - `manifest.json`
   - `sw.js`
4. Vá em **Settings** > **Pages**
5. Ative GitHub Pages
6. Copie a URL gerada
7. Teste o acesso

### OPÇÃO 3: Apps Script Web App

1. No editor do Apps Script, adicione este código:

```javascript
function doGet() {
  return HtmlService.createHtmlOutputFromFile('interface-mobile')
    .setTitle('Gestão de Veículos')
    .addMetaTag('viewport', 'width=device-width, initial-scale=1');
}
```

2. Crie um arquivo HTML chamado `interface-mobile`
3. Cole o conteúdo do HTML
4. Clique em **Implantar** > **Nova implantação**
5. Tipo: **Aplicativo da Web**
6. Execute como: **Eu**
7. Quem tem acesso: **Qualquer pessoa**
8. Clique em **Implantar**
9. Copie a **URL do aplicativo da Web**

### INSTALAÇÃO COMO APP NO CELULAR

#### Android:
1. Abra a URL no **Chrome**
2. Menu (⋮) > **Adicionar à tela inicial**
3. Confirme
4. O ícone aparecerá na tela inicial

#### iOS (iPhone/iPad):
1. Abra a URL no **Safari**
2. Toque no ícone **Compartilhar** (quadrado com seta)
3. Role e toque em **Adicionar à Tela de Início**
4. Confirme
5. O ícone aparecerá na tela inicial

---

## 🧪 TESTES E VALIDAÇÃO

### TESTE 1: Fluxo Completo de Solicitação

1. **Como Solicitante:**
   - Acesse o formulário de solicitação
   - Preencha todos os campos
   - Envie o formulário
   - Verifique se recebeu email de confirmação

2. **Como Gestor:**
   - Acesse a aba **Solicitações**
   - Verifique se a solicitação apareceu
   - Mude o status para **Aprovada**
   - Adicione um motorista no campo **Motorista Designado**

3. **Como Motorista:**
   - Acesse o formulário **Iniciar Corrida**
   - Selecione a solicitação aprovada
   - Preencha KM inicial
   - Envie

4. **Verificação:**
   - Vá para aba **Corridas**
   - Verifique se a corrida foi registrada
   - Status da solicitação deve estar **Em Andamento**

5. **Como Motorista (ao retornar):**
   - Acesse o formulário **Encerrar Corrida**
   - Selecione a corrida
   - Preencha KM final
   - Envie

6. **Verificação Final:**
   - Aba **Corridas**: KM percorridos calculado
   - Aba **Solicitações**: Status **Concluída**
   - Aba **Dashboard**: Números atualizados

### TESTE 2: Backup Automático

1. No editor Apps Script, execute manualmente: `backupDiario()`
2. Verifique a aba **Backup**
3. Verifique no Google Drive se foi criada uma cópia

### TESTE 3: Log de Auditoria

1. Realize várias ações no sistema
2. Acesse a aba **Log de Auditoria**
3. Verifique se todas as ações foram registradas

### TESTE 4: Relatório PDF

1. No menu **🚗 Gestão de Veículos**
2. Clique em **📊 Gerar Relatório Mensal PDF**
3. Aguarde a geração
4. Verifique no Google Drive

---

## 📖 USO DO SISTEMA

### Para SOLICITANTES

**Solicitar uma Corrida:**

1. Acesse o link do formulário (enviado por email)
2. Preencha:
   - Seu nome completo
   - Setor
   - Destino (endereço completo)
   - Motivo da viagem
   - Número de passageiros
   - Data e hora desejadas
   - Observações (opcional)
3. Clique em **Enviar**
4. Você receberá um email com o número da solicitação
5. Aguarde aprovação do gestor

### Para MOTORISTAS

**Antes de Sair (Iniciar Corrida):**

1. Abra o app mobile ou link do formulário
2. Selecione a solicitação aprovada
3. Informe seu nome
4. Digite a placa do veículo
5. **IMPORTANTE**: Anote o KM exato do hodômetro
6. Adicione observações se necessário
7. Clique em **Enviar**

**Ao Retornar (Encerrar Corrida):**

1. Abra o app mobile ou link
2. Selecione a corrida em andamento
3. **IMPORTANTE**: Anote o KM exato do hodômetro
4. Adicione observações finais
5. Clique em **Enviar**

**Dicas Importantes:**
- Sempre registre o início e o fim da corrida
- Confira os KMs antes de enviar (não é possível alterar depois)
- Em caso de erro, contate imediatamente o gestor

### Para GESTORES

**Aprovar Solicitações:**

1. Acesse a planilha principal
2. Vá para aba **Solicitações**
3. Localize solicitações com status **Pendente**
4. Avalie:
   - Justificativa
   - Data/hora solicitada
   - Disponibilidade do veículo
5. Mude o status para:
   - **Aprovada** - se OK
   - **Cancelada** - se negada
6. Se aprovada, adicione o nome do motorista designado

**Acompanhar Corridas:**

1. Aba **Corridas**: Todas as viagens
2. Aba **Dashboard**: Resumo em tempo real
3. Verifique diariamente:
   - Corridas em andamento
   - KM percorridos
   - Solicitações pendentes

**Gerar Relatórios:**

1. Menu **🚗 Gestão de Veículos**
2. **📊 Gerar Relatório Mensal PDF**
3. O arquivo será salvo automaticamente no Drive
4. Envie para superiores conforme necessário

**Gerenciar Usuários:**

1. Aba **Usuários**
2. Para adicionar: Insira nova linha
3. Para desativar: Mude **Ativo** para **Não**
4. Nunca delete linhas (histórico)

---

## 🔒 CONFORMIDADE LGPD

### Dados Coletados

O sistema coleta apenas dados necessários:
- **Identificação**: Nome, email, setor
- **Operacionais**: Destino, KM, horários
- **Auditoria**: Logs de ações

### Finalidade

Todos os dados são utilizados exclusivamente para:
- Gestão da frota oficial
- Controle de uso do patrimônio público
- Prestação de contas
- Auditoria interna

### Segurança

**Medidas Implementadas:**

1. **Controle de Acesso:**
   - Apenas usuários cadastrados
   - Perfis com permissões específicas
   - Autenticação via Google Workspace

2. **Rastreabilidade:**
   - Log completo de todas as ações
   - Registro de data/hora
   - Identificação do usuário

3. **Backup:**
   - Backup diário automático às 3h
   - Cópias mantidas por 1 ano
   - Armazenamento seguro no Google Drive

4. **Retenção de Dados:**
   - Logs mantidos por 1 ano
   - Limpeza automática de logs antigos
   - Dados operacionais mantidos conforme legislação

### Direitos dos Titulares

Os usuários podem solicitar:
- **Acesso**: Visualizar seus dados
- **Retificação**: Corrigir dados incorretos
- **Eliminação**: Após período legal
- **Portabilidade**: Exportar seus dados

**Para exercer direitos:**
- Contatar o gestor do sistema
- Email: [email do responsável]
- Prazo de resposta: 15 dias úteis

### Termo de Uso e Privacidade

**Adicione ao formulário de solicitação:**

```
Ao utilizar este sistema, você concorda que:
- Os dados fornecidos são verdadeiros
- Os dados serão usados apenas para gestão da frota
- Você tem ciência dos seus direitos LGPD
- O uso indevido é passível de sanções administrativas
```

### Encarregado de Dados (DPO)

Defina um responsável:
- Nome: ___________________________
- Cargo: ___________________________
- Email: ___________________________
- Telefone: ___________________________

---

## 🛠️ MANUTENÇÃO E BACKUP

### Backup Automático

**Configurado por padrão:**
- Horário: 03:00 da manhã
- Frequência: Diária
- Local: Google Drive (mesma pasta)
- Formato: Cópia completa da planilha
- Nomenclatura: `BACKUP_YYYY-MM-DD HH:mm:ss`

**Verificar se está funcionando:**
1. No Google Drive, verifique a pasta
2. Deve haver arquivos com prefixo `BACKUP_`
3. Data recente

**Se não estiver funcionando:**
1. Vá em Apps Script > **Gatilhos** (ícone de relógio)
2. Verifique se existe: `backupDiario`
3. Se não existir, execute: `configurarTriggers()`

### Backup Manual

Sempre que necessário:
1. Menu **🚗 Gestão de Veículos**
2. **💾 Fazer Backup Manual**
3. Aguarde confirmação

### Limpeza de Logs

**Automática:**
- Logs com mais de 1 ano são removidos automaticamente
- Execução: Todo dia 1º do mês às 02:00

**Manual:**
- Se necessário, execute: `limparLogsAntigos()` no Apps Script

### Monitoramento

**Verificar semanalmente:**

1. **Aba Log de Auditoria:**
   - Ações suspeitas
   - Erros frequentes
   - Acessos não autorizados

2. **Aba Backup:**
   - Últimos backups realizados
   - Sucesso/falha

3. **Dashboard:**
   - Dados coerentes
   - Fórmulas funcionando

### Atualizações do Sistema

**Para aplicar atualizações:**

1. Faça backup manual completo
2. No Apps Script, substitua o código
3. Execute `instalarSistema()` novamente
4. Teste todas as funcionalidades

---

## ❓ TROUBLESHOOTING

### Problema: Formulário não envia para a planilha

**Solução:**
1. Abra o formulário em modo de edição
2. Vá em **Respostas** > Ícone do Sheets
3. Vincule novamente à planilha correta
4. Teste enviando uma resposta

### Problema: Menu "Gestão de Veículos" não aparece

**Solução:**
1. Recarregue a página (F5)
2. Aguarde 30 segundos
3. Se persistir, execute manualmente `onOpen()` no Apps Script

### Problema: Erro "Script não autorizado"

**Solução:**
1. Apps Script > **Executar** qualquer função
2. Autorize novamente
3. Revise permissões
4. Aceite todos os termos

### Problema: Dashboard não atualiza

**Solução:**
1. Verifique se as fórmulas estão corretas
2. Aba Dashboard > Revisar fórmulas
3. Execute `configurarDashboard()` no Apps Script

### Problema: Backup não está sendo criado

**Solução:**
1. Apps Script > **Gatilhos** (relógio)
2. Verifique se `backupDiario` está listado
3. Execute `configurarTriggers()` novamente
4. Teste com backup manual

### Problema: KM percorrido dá negativo

**Solução:**
- Ocorre quando KM final < KM inicial
- Motorista digitou incorretamente
- **Correção manual:**
  1. Aba **Corridas**
  2. Localize a linha
  3. Corrija KM inicial ou final
  4. KM percorrido será recalculado automaticamente

### Problema: Email de confirmação não chega

**Solução:**
1. Verifique caixa de spam
2. Confirme que o email está correto
3. Verifique quota de emails do Google:
   - Limite: 100 emails/dia para contas gratuitas
   - Limite: 1500 emails/dia para Workspace

### Problema: Fórmulas com #REF! ou #VALOR!

**Solução:**
1. Nunca delete linhas inteiras
2. Sempre insira novas linhas ao final
3. Se ocorreu, restaure backup recente

### Problema: PWA não instala no celular

**Solução Android:**
1. Use **Chrome** (não outros navegadores)
2. Acesse via HTTPS
3. Menu > Adicionar à tela inicial

**Solução iOS:**
1. Use **Safari** (não Chrome)
2. Compartilhar > Adicionar à Tela de Início

---

## 📞 SUPORTE

Para dúvidas ou problemas:

**Nível 1 - Usuários:**
- Contate o gestor do sistema
- Email: ___________________________

**Nível 2 - Gestores:**
- Contate o setor de TI
- Email: ___________________________
- Telefone: ___________________________

**Nível 3 - Técnico:**
- Consulte a documentação do Apps Script
- https://developers.google.com/apps-script

---

## 📄 CHECKLIST DE IMPLEMENTAÇÃO

Marque conforme concluir:

- [ ] Planilha criada
- [ ] Apps Script instalado
- [ ] Sistema inicializado (`instalarSistema()`)
- [ ] Todas as 6 abas criadas
- [ ] Menu personalizado aparecendo
- [ ] Formulário de Solicitação criado
- [ ] Formulário Iniciar Corrida criado
- [ ] Formulário Encerrar Corrida criado
- [ ] Formulários vinculados à planilha
- [ ] Usuários cadastrados (mínimo 3)
- [ ] Permissões de compartilhamento configuradas
- [ ] URLs dos formulários distribuídas
- [ ] Interface mobile deployada
- [ ] Teste completo realizado
- [ ] Backup automático funcionando
- [ ] Relatório PDF testado
- [ ] Log de auditoria registrando
- [ ] Dashboard atualizando
- [ ] Documentação entregue aos usuários
- [ ] Termo LGPD adicionado

---

## 📚 ANEXOS

### Anexo A: Estrutura de Pastas Recomendada

```
Google Drive
└── Sistema Gestão de Veículos/
    ├── Sistema de Gestão de Veículos (planilha principal)
    ├── Backups/
    │   ├── BACKUP_2025-01-28.xlsx
    │   ├── BACKUP_2025-01-29.xlsx
    │   └── ...
    ├── Relatórios/
    │   ├── Relatorio_Mensal_01_2025.pdf
    │   ├── Relatorio_Mensal_02_2025.pdf
    │   └── ...
    └── Documentação/
        ├── Manual_Solicitantes.pdf
        ├── Manual_Motoristas.pdf
        └── Manual_Gestores.pdf
```

### Anexo B: Campos dos Formulários

**Solicitação de Corrida:**
- Nome Completo (texto curto) *obrigatório
- Setor/Departamento (texto curto) *obrigatório
- Destino (texto curto) *obrigatório
- Motivo da Viagem (parágrafo) *obrigatório
- Número de Passageiros (texto curto) *obrigatório
- Data Desejada (data) *obrigatório
- Horário Desejado (hora) *obrigatório
- Observações (parágrafo) opcional

**Iniciar Corrida:**
- Selecione a Solicitação (lista) *obrigatório
- Motorista (lista) *obrigatório
- Placa do Veículo (texto curto) *obrigatório
- KM Inicial (texto curto) *obrigatório
- Observações (parágrafo) opcional

**Encerrar Corrida:**
- Selecione a Corrida (lista) *obrigatório
- KM Final (texto curto) *obrigatório
- Observações Finais (parágrafo) opcional

### Anexo C: Fórmulas do Dashboard

```
Total Corridas Hoje:
=COUNTIF(Corridas!A:A,TEXT(TODAY(),"dd/MM/yyyy")&"*")

KM Percorridos Hoje:
=SUMIF(Corridas!E:E,">="&TODAY(),Corridas!K:K)

Solicitações Pendentes:
=COUNTIF(Solicitações!J:J,"Pendente")

Total Corridas Mês:
=COUNTIF(Corridas!E:E,">="&DATE(YEAR(TODAY()),MONTH(TODAY()),1))

KM Percorridos Mês:
=SUMIF(Corridas!E:E,">="&DATE(YEAR(TODAY()),MONTH(TODAY()),1),Corridas!K:K)

Média KM por Corrida:
=IF(B9=0,0,B10/B9)
```

---

## ✅ CONCLUSÃO

Este sistema foi desenvolvido para atender plenamente aos requisitos de contratos públicos federais, incluindo:

- ✅ Rastreabilidade completa
- ✅ Controle de acesso por perfis
- ✅ Backup automático diário
- ✅ Log de auditoria
- ✅ Conformidade LGPD
- ✅ Relatórios em PDF
- ✅ Interface mobile (PWA)
- ✅ Operação 100% online
- ✅ Sem custos adicionais

**Sistema desenvolvido em Janeiro/2025**

---

**IMPORTANTE:**

> Este sistema deve ser mantido atualizado e os backups devem ser verificados regularmente.
> Em caso de auditoria, todos os logs e backups devem estar disponíveis.
> Mantenha sempre uma cópia offline dos dados mais críticos.

---
