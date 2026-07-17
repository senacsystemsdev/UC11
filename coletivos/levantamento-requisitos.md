# Levantamento de Requisitos

**Projeto:** Modernização da Gestão de Estoque — Rede de Supermercados Atacadão  
**Data:** 17/07/2026  
**Versão:** 2.0 — Alinhado ao MVP de Controle de Validade e Prevenção de Perdas com IA

---

## Legenda

| Marcação | Significado |
|----------|-------------|
| ✅ MVP | Requisito incluído no escopo do MVP |
| ⏳ Futuro | Requisito previsto para versões futuras |

---

## 1. Requisitos Funcionais

### Módulo de Vendas (PDV) — ⏳ Futuro

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RF001 | O sistema deve registrar vendas para clientes CPF com cadastro simplificado (nome, CPF, contato) | ⏳ |
| RF002 | O sistema deve registrar vendas para clientes CNPJ com cadastro completo (dados fiscais, tabela de preço diferenciada) | ⏳ |
| RF003 | O sistema deve emitir cupom fiscal para vendas CPF | ⏳ |
| RF004 | O sistema deve emitir NF-e para vendas CNPJ | ⏳ |
| RF005 | O sistema deve dar baixa automática no estoque a cada venda realizada | ⏳ |
| RF006 | O sistema deve suportar venda no balcão e autoatendimento | ⏳ |
| RF007 | O sistema deve permitir condições de pagamento especiais por tipo de cliente | ⏳ |

### Módulo de Controle de Estoque — ⏳ Futuro

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RF008 | O sistema deve manter saldo atualizado em tempo real a cada venda ou entrada | ⏳ |
| RF009 | O sistema deve disparar alerta quando o estoque atingir o nível mínimo | ⏳ |
| RF010 | O sistema deve disparar alerta quando houver excesso de estoque | ⏳ |
| RF011 | O sistema deve controlar estoque por filial/unidade | ⏳ |
| RF012 | O sistema deve permitir consulta de saldo por produto, categoria e filial | ⏳ |

### Módulo de Planejamento de Compras — ⏳ Futuro

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RF013 | O sistema deve sugerir automaticamente quais produtos comprar com base no histórico de vendas | ⏳ |
| RF014 | O sistema deve sugerir a quantidade ideal de compra com base no estoque mínimo e no histórico | ⏳ |
| RF015 | O sistema deve permitir que o comprador aprove ou ajuste as sugestões geradas | ⏳ |
| RF016 | O sistema deve gerar pedido de compra ao fornecedor após aprovação | ⏳ |

### Módulo de Perdas — ✅ MVP (base)

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RF017 | O sistema deve permitir registro de perdas por vencimento, avaria ou extravio | ✅ |
| RF018 | O sistema deve notificar automaticamente sobre produtos próximos ao vencimento | ✅ |
| RF019 | O sistema deve gerar relatório mensal de perdas por categoria | ✅ |
| RF020 | O sistema deve ajustar o saldo do estoque automaticamente após registro de perda | ✅ |

### Módulo de Inventário — ⏳ Futuro

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RF021 | O sistema deve permitir contagem cíclica por coletor ou aplicativo mobile | ⏳ |
| RF022 | O sistema deve realizar conferência por código de barras | ⏳ |
| RF023 | O sistema deve ajustar automaticamente o saldo após validação da contagem | ⏳ |
| RF024 | O sistema deve gerar relatório de divergência entre saldo contábil e físico | ⏳ |

### Módulo de Movimentação entre Depósitos — ⏳ Futuro

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RF025 | O sistema deve registrar transferências de mercadorias entre filiais | ⏳ |
| RF026 | O sistema deve controlar origem, destino e responsável pela movimentação | ⏳ |
| RF027 | O sistema deve permitir rastreamento em tempo real da mercadoria em trânsito | ⏳ |
| RF028 | O sistema deve atualizar o saldo de origem e destino automaticamente | ⏳ |

### Módulo de Indicadores Gerenciais — ✅ MVP (parcial)

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RF029 | O sistema deve calcular o giro de estoque por produto e categoria | ✅ |
| RF030 | O sistema deve identificar os produtos mais vendidos (por cliente CPF e CNPJ) | ⏳ |
| RF031 | O sistema deve calcular a taxa de ruptura (falta de produto) | ⏳ |
| RF032 | O sistema deve calcular o ticket médio por tipo de cliente | ⏳ |
| RF033 | O sistema deve exibir o valor total em estoque | ✅ |
| RF034 | O sistema deve permitir a visualização de indicadores consolidados por unidade e por rede | ✅ |

---

### Módulo MVP — Controle de Validade e Prevenção de Perdas com IA

| Código | Descrição |
|--------|-----------|
| RF035 | O sistema deve calcular o risco de vencimento de cada lote com base na data de validade e na velocidade média de venda do produto na filial |
| RF036 | O sistema deve classificar automaticamente cada lote em três níveis de risco: verde (baixo), amarelo (médio) e vermelho (crítico) |
| RF037 | O sistema deve sugerir automaticamente um percentual de desconto para lotes classificados como amarelo ou vermelho |
| RF038 | O sistema deve identificar filiais com excesso de estoque e sugerir realocação para filiais com maior demanda |
| RF039 | O sistema deve emitir alerta para retirada de gôndola de lotes em estado crítico sem chance de venda |

### Módulo MVP — Detecção de Anomalias em Perdas

| Código | Descrição |
|--------|-----------|
| RF040 | O sistema deve monitorar continuamente os padrões de perda cruzando dados de filial, turno, operador, categoria e dia da semana |
| RF041 | O sistema deve detectar anomalias em perdas utilizando algoritmo de machine learning (Isolation Forest) |
| RF042 | O sistema deve notificar o gerente em tempo real quando uma anomalia for detectada, com detalhes da suspeita |
| RF043 | O sistema deve classificar automaticamente a causa provável de cada perda: vencimento, manuseio, furto ou erro de sistema |
| RF044 | O sistema deve gerar relatório mensal consolidado de perdas por causa, permitindo exportação |

### Módulo MVP — Dashboard Preditivo

| Código | Descrição |
|--------|-----------|
| RF045 | O sistema deve exibir um heatmap de risco por filial, categoria e fornecedor |
| RF046 | O sistema deve exibir um ranking dos produtos com maior risco de perda no período |

### Módulo MVP — Integração com ERP

| Código | Descrição |
|--------|-----------|
| RF047 | O sistema deve integrar com o ERP TOTVS Consinco/RMS via API REST para obter dados de lote, validade e vendas |
| RF048 | O sistema deve aplicar ações (desconto no PDV, transferência entre filiais) no ERP após aprovação do usuário |
| RF049 | O sistema deve registrar trilha de auditoria para todas as ações executadas |

---

## 2. Requisitos Não Funcionais

### Performance

| Código | Descrição | Métrica | Escopo |
|--------|-----------|---------|--------|
| RNF001 | O dashboard deve carregar em até 3 segundos | Tempo de carregamento < 3s | ✅ |
| RNF002 | Alertas de anomalia devem ser entregues em até 1 minuto após a detecção | Latência < 60s | ✅ |
| RNF003 | O sistema deve suportar até 500 filiais simultâneas | 500 usuários concorrentes | ✅ |
| RNF004 | Consultas no histórico de perdas devem retornar em até 5 segundos para 12 meses de dados | Query < 5s | ✅ |
| RNF005 | A baixa no estoque deve ocorrer em até 2 segundos após a venda | < 2s | ⏳ |

### Disponibilidade

| Código | Descrição | Métrica | Escopo |
|--------|-----------|---------|--------|
| RNF006 | Disponibilidade do sistema em horário comercial (06h–22h) | 99,5% | ✅ |
| RNF007 | Janela de manutenção programada: noturno (22h–05h) | Máx 2h/semana | ✅ |
| RNF008 | Plano de recuperação de desastres (RPO) | Máx 15 minutos | ✅ |

### Segurança

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RNF009 | O sistema deve garantir que apenas usuários autenticados acessem as funcionalidades (SSO / JWT) | ✅ |
| RNF010 | O controle de acesso deve ser baseado em papéis: Gerente, Operador, Auditor, Administrador | ✅ |
| RNF011 | Todas as ações devem ser logadas com timestamp e usuário (trilha de auditoria) | ✅ |
| RNF012 | Dados em trânsito devem ser criptografados (TLS 1.3) | ✅ |
| RNF013 | Dados em repouso devem ser criptografados (AES-256) | ✅ |

### Usabilidade

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RNF014 | A interface deve ser responsiva, funcional em desktop e tablet | ✅ |
| RNF015 | O sistema deve estar em português (PT-BR) | ✅ |
| RNF016 | O sistema deve atender à conformidade WCAG 2.1 nível AA | ✅ |

### Compatibilidade

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RNF017 | Navegadores suportados: Chrome, Firefox, Edge (2 versões mais recentes) | ✅ |
| RNF018 | Integração com ERP TOTVS Consinco/RMS via API REST | ✅ |
| RNF019 | Exportação de relatórios em CSV e PDF | ✅ |

### Manutenibilidade

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RNF020 | Código versionado com Git e GitFlow | ✅ |
| RNF021 | Testes automatizados com cobertura mínima de 70% | ✅ |
| RNF022 | Documentação da API no padrão OpenAPI 3.0 (Swagger) | ✅ |

### Stack Tecnológica

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RNF023 | Frontend em React + TypeScript com Chart.js/Recharts | ✅ |
| RNF024 | Backend em Node.js com Express | ✅ |
| RNF025 | Serviço de ML em Python com Flask/FastAPI e scikit-learn | ✅ |
| RNF026 | Banco de dados relacional PostgreSQL 16 | ✅ |
| RNF027 | Cache Redis para consultas frequentes | ✅ |
| RNF028 | Notificações em tempo real via WebSocket (Socket.io) | ✅ |
| RNF029 | Containerização com Docker e Docker Compose | ✅ |
| RNF030 | Proxy reverso com NGINX | ✅ |

---

## 3. Perfis de Usuário

### Perfis do MVP

| Perfil | Descrição | Casos de Uso |
|--------|-----------|--------------|
| Gerente de Loja | Monitora risco de vencimento, recebe sugestões de desconto e alertas de anomalia | UC01, UC02, UC03, UC08 |
| Operador de Estoque | Visualiza classificação de risco e recebe alertas de descarte programado | UC02, UC05 |
| Coordenador de Operações | Gerencia realocação de produtos entre filiais | UC04 |
| Analista de Prevenção de Perdas | Monitora padrões de perda e investiga anomalias | UC06 |
| Gerente Regional | Compara indicadores entre filiais e visualiza heatmap de risco | UC07, UC11 |
| Auditor | Classifica causas de perda e audita o processo | UC09 |
| Comprador | Visualiza ranking de produtos críticos para negociar com fornecedores | UC12 |
| Diretoria | Acompanha relatórios consolidados de perdas | UC10 |

### Perfis Completos (Sistema Futuro)

| Perfil | Módulos Acessíveis | Escopo |
|--------|-------------------|--------|
| Operador de Caixa | PDV (RF001 a RF007) | ⏳ |
| Estoquista | Estoque (RF008-RF012), Perdas (RF017-RF020), Inventário (RF021-RF024) | ⏳ |
| Comprador | Planejamento de Compras (RF013-RF016), Indicadores (RF029-RF034) | ⏳ (parcial) |
| Gerente de Loja | Todos os módulos da sua unidade | ✅ (MVP) |
| Logística | Movimentação (RF025-RF028), Estoque (RF008-RF012) | ⏳ |
| Diretoria | Indicadores (RF029-RF034) | ✅ (parcial) |

---

## 4. Regras de Negócio

| Código | Descrição | Escopo |
|--------|-----------|--------|
| RN001 | Cliente CNPJ deve ter cadastro completo com dados fiscais para emissão de NF-e | ⏳ |
| RN002 | Cliente CNPJ pode ter tabela de preço diferenciada por volume | ⏳ |
| RN003 | Venda CNPJ pode exigir pedido mínimo | ⏳ |
| RN004 | Produto com estoque abaixo do mínimo deve gerar sugestão de compra | ⏳ |
| RN005 | Produto vencido deve ser bloqueado para venda | ✅ |
| RN006 | Transferência entre depósitos deve ter origem, destino e responsável registrados | ✅ |
| RN007 | Lote com risco alto (vermelho) deve gerar alerta imediato para retirada da gôndola | ✅ |
| RN008 | Desconto sugerido não pode exceder o custo do produto | ✅ |
| RN009 | Anomalia detectada com confiança superior a 90% deve gerar notificação automática ao gerente | ✅ |
| RN010 | Relatório mensal de perdas por causa deve ser disponibilizado até o 5º dia útil do mês seguinte | ✅ |

---

## 5. Critérios de Aceitação do MVP

| Critério | Descrição |
|----------|-----------|
| CA01 | Alertas devem ser emitidos em até 5 minutos após a detecção |
| CA02 | Dashboard deve atualizar em tempo real via WebSocket |
| CA03 | Taxa de falsos positivos em anomalias < 10% |
| CA04 | Precisão da classificação de causa > 85% |
| CA05 | Sistema deve registrar trilha de auditoria para todas as ações |
| CA06 | Heatmap deve refletir dados em no máximo 5 minutos de atraso |
| CA07 | Sugestão de desconto deve considerar margem do produto |

---

## 6. Matriz de Rastreabilidade MVP

A relação completa entre casos de uso (UC01 a UC12) e requisitos está documentada em `requisitos-por-caso-de-uso.md`.

---

*Documento atualizado em 17/07/2026 — Versão 2.0 (alinhado ao MVP)*
