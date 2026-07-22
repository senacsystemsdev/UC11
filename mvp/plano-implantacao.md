# Plano de Implantação Resumido — MVP Controle de Validade com IA

**UC11:** Gerir Projetos de Tecnologia da Informação  
**Equipe:** William, Alaide, Ed  
**Data:** 22/07/2026

---

## 1. Visão Geral

Implantação do MVP em 4 sprints (total aproximado de **138 dias**), começando com piloto em 1 loja e expandindo gradualmente para a rede.

---

## 2. Cronograma

| Sprint | Duração | Período | Entregas |
|--------|---------|---------|----------|
| **Sprint 1 — Fundação** | 30 dias | Ago/2026 | Setup React + Node + PostgreSQL; integração TOTVS; login; dashboard básico |
| **Sprint 2 — Núcleo Validade** | 35 dias | Set-Out/2026 | ML de risco por lote; classificação verde/amarelo/vermelho; sugestão de desconto e realocação |
| **Sprint 3 — Anomalias** | 38 dias | Out-Nov/2026 | Isolation Forest; classificação de causa; alertas em tempo real; relatório mensal |
| **Sprint 4 — Refino e Testes** | 35 dias | Nov-Dez/2026 | Testes de integração; ajustes ML (precisão > 85%); documentação Swagger; piloto em 1 loja |

---

## 3. Fases de Implantação

### Fase 1 — Piloto (Sprint 4 + 2 semanas)
- **Escopo:** 1 loja piloto (alta complexidade operacional)
- **Duração:** 2 semanas de validação
- **Critérios de sucesso:**
  - Zero produtos vencidos não detectados
  - Precisão do ML > 85%
  - Taxa de falsos positivos < 10%
  - Feedback positivo dos usuários (NPS > 70)

### Fase 2 — Expansão Controlada (Mês 5-6)
- **Escopo:** 5 lojas com perfis variados (grande porte, periferia, centro)
- **Duração:** 60 dias
- **Monitoramento:** Comparação de indicadores pré e pós implantação

### Fase 3 — Rollout Nacional (Mês 7-12)
- **Escopo:** Todas as lojas da rede
- **Estratégia:** 10 lojas/semana com suporte dedicado
- **Treinamento:** Workshops presenciais + materiais EAD

---

## 4. Recursos Necessários

| Recurso | Quantidade | Responsável |
|---------|------------|-------------|
| Desenvolvedor Frontend (React/TS) | 1 | William |
| Desenvolvedor Backend (Node.js) | 1 | Ed |
| Cientista de Dados (Python/ML) | 1 | Ed |
| Designer UI/UX | 1 | Alaide |
| Analista de Negócios (integração TOTVS) | 1 | Equipe |
| Gerente de Projeto | 1 | Ed |
| Infraestrutura (Cloud) | Conforme arquitetura | Ed |

---

## 5. Infraestrutura

| Componente | Especificação | Custo Estimado (mês) |
|------------|--------------|---------------------|
| Frontend (CDN) | 2 vCPU, 4 GB RAM | ~R$ 200 |
| Backend API | 4 vCPU, 8 GB RAM | ~R$ 600 |
| ML Service | 4 vCPU, 16 GB RAM | ~R$ 1.200 |
| PostgreSQL | 4 vCPU, 16 GB RAM, SSD | ~R$ 800 |
| Redis | 2 vCPU, 4 GB RAM | ~R$ 300 |
| **Total** | | **~R$ 3.100/mês** |

---

## 6. Riscos e Mitigação

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Qualidade dos dados do ERP | Alta | Alto | Limpeza e validação de dados na Sprint 1 |
| Resistência dos gerentes ao sistema | Média | Alto | Treinamento presencial; envolvimento desde Sprint 1 |
| Integração com legado TOTVS | Média | Alto | Prova de conceito na Sprint 1; contrato com suporte TOTVS |
| Falsos positivos do ML | Média | Médio | Ajuste contínuo do threshold; feedback loop do usuário |
| Atraso no cronograma | Média | Médio | Priorização de funcionalidades críticas; sprints curtas |

---

## 7. ROI Esperado

| Indicador | Valor Estimado |
|-----------|---------------|
| Redução de perdas totais | 15% |
| Economia anual estimada (por loja) | ~R$ 120.000 |
| Custo total do projeto (implantaçao) | ~R$ 180.000 |
| Retorno do investimento | 18 meses |
| Redução de multas e indenizações | Não mensurável, mas significativa |

---

## 8. Próximos Passos

1. Aprovação do orçamento pela diretoria
2. Setup da infraestrutura cloud
3. Kickoff do projeto com equipe técnica e stakeholders
4. Início da Sprint 1 — integração com TOTVS
5. Validação do piloto com métricas reais
