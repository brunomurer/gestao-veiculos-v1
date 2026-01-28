# TEMPLATES DE COMUNICAÇÃO
## Sistema de Gestão de Veículos

---

## 📧 EMAILS AUTOMÁTICOS

### 1. Email de Confirmação de Solicitação

**Assunto:** Solicitação de Veículo Recebida - {ID_SOLICITACAO}

**Corpo:**
```
Prezado(a) {NOME_SOLICITANTE},

Sua solicitação de uso do veículo oficial foi recebida com sucesso!

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
DADOS DA SOLICITAÇÃO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Número da Solicitação: {ID_SOLICITACAO}
Data/Hora da Solicitação: {DATA_HORA}
Solicitante: {NOME_SOLICITANTE}
Setor: {SETOR}

Destino: {DESTINO}
Data Desejada: {DATA_DESEJADA}
Horário Desejado: {HORA_DESEJADA}
Passageiros: {NUM_PASSAGEIROS}

Status: PENDENTE DE APROVAÇÃO

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

O que acontece agora?

→ Sua solicitação será analisada pelo gestor
→ Você será notificado da decisão em até 24 horas
→ Se aprovada, será informado qual motorista foi designado

IMPORTANTE: Mantenha este email para referência futura.

Em caso de dúvidas, entre em contato:
{NOME_GESTOR} - {EMAIL_GESTOR}

Atenciosamente,
Sistema de Gestão de Veículos
```

---

### 2. Email de Aprovação

**Assunto:** ✅ Solicitação APROVADA - {ID_SOLICITACAO}

**Corpo:**
```
Prezado(a) {NOME_SOLICITANTE},

Ótima notícia! Sua solicitação foi APROVADA!

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
INFORMAÇÕES DA VIAGEM
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Número da Solicitação: {ID_SOLICITACAO}
Status: APROVADA ✅

Motorista Designado: {NOME_MOTORISTA}
Telefone do Motorista: {TELEFONE_MOTORISTA}

Data da Viagem: {DATA_DESEJADA}
Horário: {HORA_DESEJADA}
Destino: {DESTINO}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

INSTRUÇÕES IMPORTANTES:

✓ Esteja pronto 10 minutos antes do horário combinado
✓ Aguarde no local de embarque previamente acordado
✓ Tenha em mãos todos os documentos necessários
✓ Em caso de atraso ou impedimento, avise imediatamente

CANCELAMENTO: Se precisar cancelar, avise com antecedência!

Contato de emergência: {TELEFONE_EMERGENCIA}

Tenha uma ótima viagem!

Atenciosamente,
Sistema de Gestão de Veículos
```

---

### 3. Email de Negativa

**Assunto:** ❌ Solicitação NÃO APROVADA - {ID_SOLICITACAO}

**Corpo:**
```
Prezado(a) {NOME_SOLICITANTE},

Informamos que sua solicitação não foi aprovada.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
INFORMAÇÕES DA SOLICITAÇÃO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Número da Solicitação: {ID_SOLICITACAO}
Status: NÃO APROVADA ❌

Motivo: {MOTIVO_NEGATIVA}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PRÓXIMOS PASSOS:

Você pode:
→ Fazer nova solicitação com data/horário diferente
→ Buscar alternativas de transporte
→ Entrar em contato para mais esclarecimentos

Para dúvidas ou reconsideração:
{NOME_GESTOR} - {EMAIL_GESTOR}
Telefone: {TELEFONE_GESTOR}

Atenciosamente,
Sistema de Gestão de Veículos
```

---

### 4. Email de Lembrete (1 dia antes)

**Assunto:** 🔔 Lembrete: Viagem Amanhã - {ID_SOLICITACAO}

**Corpo:**
```
Prezado(a) {NOME_SOLICITANTE},

Este é um lembrete sobre sua viagem AMANHÃ.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
DETALHES DA VIAGEM
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Data: {DATA_VIAGEM}
Horário: {HORA_VIAGEM}
Destino: {DESTINO}

Motorista: {NOME_MOTORISTA}
Contato: {TELEFONE_MOTORISTA}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CHECKLIST:

[ ] Confirme que ainda precisa da viagem
[ ] Esteja pronto 10 minutos antes
[ ] Tenha documentos necessários
[ ] Salve o contato do motorista

Se precisar CANCELAR, avise AGORA!
Contato: {TELEFONE_GESTOR}

Até amanhã!

Sistema de Gestão de Veículos
```

---

## 📋 TEMPLATES DE DOCUMENTOS

### 5. Termo de Responsabilidade do Motorista

```
TERMO DE RESPONSABILIDADE - USO DE VEÍCULO OFICIAL

Eu, {NOME_MOTORISTA}, CPF {CPF}, motorista oficial, 
declaro estar ciente e concordar com:

1. RESPONSABILIDADES:
   • Dirigir com prudência e respeitar o Código de Trânsito
   • Zelar pela conservação do veículo
   • Registrar corretamente início e fim de cada corrida
   • Informar imediatamente qualquer problema mecânico
   • Não usar o veículo para fins pessoais

2. USO DO SISTEMA:
   • Preencher formulário de INÍCIO antes de sair
   • Preencher formulário de FIM ao retornar
   • Informar quilometragem EXATA
   • Registrar qualquer ocorrência

3. PENALIDADES:
   Estou ciente que o uso inadequado do veículo ou do sistema
   pode resultar em sanções administrativas conforme legislação.

4. LGPD:
   Declaro ciência sobre a Lei 13.709/2018 e comprometo-me a:
   • Não divulgar dados de solicitantes
   • Manter sigilo sobre informações do sistema
   • Usar dados apenas para fins do serviço

Local: _______________  Data: ___/___/______

___________________________________
Assinatura do Motorista

___________________________________
Testemunha (Gestor)
```

---

### 6. Formulário de Ocorrência

```
REGISTRO DE OCORRÊNCIA - VEÍCULO OFICIAL

Data: ___/___/______  Hora: ___:___

ID da Corrida: _______________________________

Motorista: ____________________________________

Tipo de Ocorrência:
[ ] Acidente de trânsito
[ ] Pane mecânica
[ ] Multa de trânsito
[ ] Dano ao veículo
[ ] Outra: _____________________

Descrição Detalhada:
_________________________________________________
_________________________________________________
_________________________________________________
_________________________________________________

Local da Ocorrência: __________________________

Havia passageiros? [ ] Sim [ ] Não
Se sim, quantos? _____

Boletim de Ocorrência registrado? [ ] Sim [ ] Não
Número do BO: __________________

Danos Materiais:
_________________________________________________
_________________________________________________

Providências Tomadas:
_________________________________________________
_________________________________________________

Observações:
_________________________________________________
_________________________________________________

___________________________________
Assinatura do Motorista

___________________________________
Ciência do Gestor

Anexar: fotos, documentos, laudos, etc.
```

---

### 7. Checklist de Vistoria do Veículo

```
CHECKLIST DE VISTORIA - VEÍCULO OFICIAL

Placa: ____________  Data: ___/___/______

Motorista: ____________________________________

KM Atual: __________

ITENS A VERIFICAR:

DOCUMENTAÇÃO:
[ ] CRLV (licenciamento) válido
[ ] Seguro em dia
[ ] Certificado de vistoria DETRAN

EXTERNO:
[ ] Lataria (amassados, riscos)
[ ] Vidros (trincas, quebras)
[ ] Faróis e lanternas
[ ] Pneus (calibragem e desgaste)
[ ] Limpadores de para-brisa

INTERNO:
[ ] Painel (luzes de alerta)
[ ] Bancos e cintos de segurança
[ ] Ar condicionado
[ ] Rádio/som
[ ] Limpeza geral

MECÂNICO:
[ ] Nível de óleo
[ ] Nível de água
[ ] Combustível
[ ] Freios
[ ] Direção

SEGURANÇA:
[ ] Estepe
[ ] Macaco e chave de roda
[ ] Triângulo
[ ] Extintor (validade)

OBSERVAÇÕES:
_________________________________________________
_________________________________________________
_________________________________________________

AVALIAÇÃO GERAL:
[ ] APROVADO - Veículo em condições de uso
[ ] ATENÇÃO - Requer manutenção breve
[ ] REPROVADO - Não usar até conserto

___________________________________
Assinatura do Motorista

___________________________________
Ciência do Gestor

Próxima vistoria: ___/___/______
```

---

## 📄 TEMPLATES DE RELATÓRIOS

### 8. Relatório Semanal Simplificado

```
RELATÓRIO SEMANAL - GESTÃO DE VEÍCULOS

Período: ___/___/______ a ___/___/______

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
RESUMO EXECUTIVO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Total de Solicitações: ______
Solicitações Aprovadas: ______
Solicitações Negadas: ______
Solicitações Pendentes: ______

Total de Corridas Realizadas: ______
KM Percorridos: ______ km
Tempo Total em Viagem: ______ horas

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ANÁLISE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Destinos Mais Frequentes:
1. ______________________________________
2. ______________________________________
3. ______________________________________

Setores que Mais Solicitaram:
1. ______________________________________
2. ______________________________________
3. ______________________________________

Média de KM por Corrida: ______ km

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
OCORRÊNCIAS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[ ] Nenhuma ocorrência
[ ] Ocorrências registradas (ver anexo)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
MANUTENÇÕES NECESSÁRIAS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[ ] Nenhuma
[ ] Manutenção preventiva
[ ] Manutenção corretiva urgente

Detalhes: ___________________________________

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Elaborado por: _______________________________
Data: ___/___/______
```

---

### 9. Relatório Mensal Completo

```
RELATÓRIO MENSAL - GESTÃO DE VEÍCULOS

Mês/Ano: ___________/___________

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. ESTATÍSTICAS GERAIS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Solicitações:
• Total recebidas: ______
• Aprovadas: ______ (____%)
• Negadas: ______ (____%)
• Canceladas: ______ (____%)

Corridas:
• Total realizadas: ______
• Corridas completadas: ______
• Corridas canceladas: ______

Quilometragem:
• KM inicial do mês: ______
• KM final do mês: ______
• Total percorrido: ______ km
• Média por corrida: ______ km

Tempo:
• Total em viagem: ______ horas
• Média por corrida: ______ horas

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
2. ANÁLISE POR SETOR
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Ranking de Utilização:

1. {SETOR}: ______ corridas (____%)
2. {SETOR}: ______ corridas (____%)
3. {SETOR}: ______ corridas (____%)
4. {SETOR}: ______ corridas (____%)
5. {SETOR}: ______ corridas (____%)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
3. PRINCIPAIS DESTINOS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. {DESTINO}: ______ viagens
2. {DESTINO}: ______ viagens
3. {DESTINO}: ______ viagens
4. {DESTINO}: ______ viagens
5. {DESTINO}: ______ viagens

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
4. DESEMPENHO DOS MOTORISTAS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Motorista 1:
• Corridas realizadas: ______
• KM percorridos: ______
• Tempo em viagem: ______

Motorista 2:
• Corridas realizadas: ______
• KM percorridos: ______
• Tempo em viagem: ______

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
5. CUSTOS OPERACIONAIS (se aplicável)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

• Combustível: R$ ______
• Manutenção: R$ ______
• Seguros: R$ ______
• Outros: R$ ______

Total: R$ ______

Custo por KM: R$ ______

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
6. OCORRÊNCIAS E INCIDENTES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[ ] Nenhuma ocorrência neste mês

[ ] Ocorrências registradas:
    Data: ___/___  Tipo: _______________
    Descrição: ___________________________
    Providências: ________________________

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
7. MANUTENÇÕES REALIZADAS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Data: ___/___  Tipo: _______________
Descrição: ______________________________
Custo: R$ ______

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
8. CONFORMIDADE E AUDITORIA
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

• Backups realizados: ______ dias
• Log de auditoria: Ativo
• Usuários cadastrados: ______
• LGPD: Conforme

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
9. OBSERVAÇÕES E RECOMENDAÇÕES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

_________________________________________________
_________________________________________________
_________________________________________________

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
10. PRÓXIMAS AÇÕES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[ ] Manutenção preventiva programada para ___/___
[ ] Revisão de usuários
[ ] Atualização do sistema
[ ] Outros: _____________________________

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Elaborado por: _______________________________
Cargo: _______________________________________
Data: ___/___/______

Aprovado por: ________________________________
Cargo: _______________________________________
Data: ___/___/______
```

---

## 🔐 TEMPLATES DE TERMOS

### 10. Termo de Uso do Sistema

```
TERMO DE USO E ACEITAÇÃO
SISTEMA DE GESTÃO DE VEÍCULOS

Ao acessar e utilizar o Sistema de Gestão de Veículos, 
você concorda com os seguintes termos:

1. FINALIDADE
   Este sistema destina-se exclusivamente à gestão do 
   veículo oficial da instituição.

2. RESPONSABILIDADES DO USUÁRIO
   • Fornecer informações verdadeiras
   • Usar o sistema apenas para fins oficiais
   • Não compartilhar suas credenciais de acesso
   • Reportar imediatamente qualquer uso indevido

3. PROTEÇÃO DE DADOS (LGPD)
   • Seus dados serão usados conforme Lei 13.709/2018
   • Base legal: cumprimento de obrigação legal
   • Finalidade: gestão de frota e prestação de contas
   • Retenção: 5 anos conforme Lei 8.666/93

4. DIREITOS
   Você tem direito a:
   • Acessar seus dados
   • Corrigir informações incorretas
   • Solicitar portabilidade

5. VEDAÇÕES
   É proibido:
   • Uso para fins pessoais
   • Fornecimento de informações falsas
   • Tentativa de burlar controles do sistema
   • Acesso não autorizado a dados de terceiros

6. CONSEQUÊNCIAS
   O uso indevido pode resultar em:
   • Suspensão de acesso
   • Processo administrativo
   • Responsabilização civil e criminal

7. CONTATO
   Para dúvidas ou exercício de direitos:
   {NOME_ENCARREGADO} - {EMAIL_ENCARREGADO}

ACEITE:

Declaro que li, compreendi e concordo com os termos acima.

Nome: ___________________________________________
Email: ___________________________________________
Data: ___/___/______

[ ] Li e aceito os termos de uso
[ ] Autorizo o tratamento dos meus dados conforme descrito
```

---

## 📱 TEMPLATES DE SMS/WhatsApp

### 11. Lembrete Rápido (SMS)

```
[VEÍCULO OFICIAL]
Olá {NOME}! 

Lembrete: Viagem AMANHÃ
📅 {DATA} às {HORA}
📍 {DESTINO}
🚗 Motorista: {MOTORISTA}
☎️ {TELEFONE}

Esteja pronto 10min antes!
Cancelou? Avise: {TEL_GESTOR}
```

---

### 12. Confirmação de Corrida Iniciada

```
[VEÍCULO OFICIAL] ✅

Corrida iniciada!
ID: {ID_CORRIDA}
Motorista: {NOME}
Destino: {DESTINO}
KM Inicial: {KM}

Boa viagem!
```

---

### 13. Confirmação de Corrida Encerrada

```
[VEÍCULO OFICIAL] 🏁

Corrida finalizada!
ID: {ID_CORRIDA}
KM Final: {KM_FINAL}
Percorrido: {KM_TOTAL} km
Tempo: {TEMPO}

Obrigado por usar o sistema!
```

---

## 📊 TEMPLATE DE DASHBOARD EXECUTIVO

### 14. Painel Executivo (para impressão)

```
═══════════════════════════════════════════════════════
        PAINEL EXECUTIVO - GESTÃO DE VEÍCULOS
═══════════════════════════════════════════════════════

Período: {MES}/{ANO}               Gerado em: {DATA}

┌─────────────────────────────────────────────────────┐
│                    INDICADORES                       │
├─────────────────────────────────────────────────────┤
│                                                      │
│  📊 Total de Solicitações          ▶  {NUMERO}     │
│  ✅ Taxa de Aprovação              ▶  {PERCENTUAL}  │
│  🚗 Corridas Realizadas            ▶  {NUMERO}     │
│  📏 KM Percorridos                 ▶  {KM} km      │
│  ⏱️  Tempo Total                    ▶  {HORAS}h     │
│  💰 Custo/KM                       ▶  R$ {VALOR}   │
│                                                      │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│              TOP 3 SETORES USUÁRIOS                  │
├─────────────────────────────────────────────────────┤
│                                                      │
│  🥇 {SETOR}                        ▶  {NUMERO}     │
│  🥈 {SETOR}                        ▶  {NUMERO}     │
│  🥉 {SETOR}                        ▶  {NUMERO}     │
│                                                      │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│            COMPARATIVO MÊS ANTERIOR                  │
├─────────────────────────────────────────────────────┤
│                                                      │
│  Solicitações    ▶  {VAR}% {SETA}                  │
│  KM Percorridos  ▶  {VAR}% {SETA}                  │
│  Taxa Aprovação  ▶  {VAR}% {SETA}                  │
│                                                      │
└─────────────────────────────────────────────────────┘

═══════════════════════════════════════════════════════

Observações: _________________________________________
__________________________________________________________

Gestor: ______________________  Data: ___/___/______
```

---

## 💡 DICAS DE USO DOS TEMPLATES

### Como usar estes templates:

1. **Emails**: Copie e cole no código Apps Script, substituindo as variáveis entre chaves
2. **Documentos**: Imprima e preencha à mão ou use como base para versões digitais
3. **SMS**: Configure integração com serviço de SMS se disponível
4. **Relatórios**: Use como base para seus relatórios mensais

### Variáveis comuns:

```
{ID_SOLICITACAO} - Número da solicitação
{NOME_SOLICITANTE} - Nome de quem solicitou
{SETOR} - Departamento/setor
{DESTINO} - Local de destino
{DATA_DESEJADA} - Data da viagem
{HORA_DESEJADA} - Horário da viagem
{NOME_MOTORISTA} - Nome do motorista
{TELEFONE_MOTORISTA} - Telefone do motorista
{KM} - Quilometragem
{NOME_GESTOR} - Nome do gestor
{EMAIL_GESTOR} - Email do gestor
```

---

FIM DOS TEMPLATES

Versão 1.0 - Janeiro 2025
Sistema de Gestão de Veículos
