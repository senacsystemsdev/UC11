# MVP — Central de Inteligência de Estoque (Atacadão)

**UC11:** Gerir Projetos de Tecnologia da Informação  
**Equipe:** William, Alaide, Ed

---

## Visão Geral

MVP de um sistema integrado de gestão de estoque com inteligência artificial, focado em reduzir ruptura, perdas e estoque excessivo na rede Atacadão.

---

## 1. Previsão de Demanda

### Sistema Atual
- Comprador decide o que e quanto comprar baseado na experiência própria e em planilhas manuais
- Não há análise de sazonalidade (ex.: aumenta estoque de cerveja no verão, panetone no fim de ano)
- Pedidos são feitos em datas fixas, sem considerar velocidade real de venda
- Resultado: ruptura frequente de produtos que vendem rápido e sobra de produtos encalhados

### Sistema com IA (MVP)
- Modelo de ML treinado com histórico de vendas dos últimos 2 anos
- Leva em conta: dia da semana, sazonalidade, promoções, feriados regionais
- Gera previsão de demanda para os próximos 7, 15 e 30 dias por produto/filial
- Comprador recebe sugestão com justificativa: *"Produto X vendeu 30% a mais no mês passado. Sugerir aumentar 40% no pedido?"*

---

## 2. Sugestão de Compras

### Sistema Atual
- Comprador calcula manualmente quanto comprar olhando o saldo atual
- Não há integração entre estoque mínimo e histórico de vendas
- Pedidos são enviados por e-mail ou telefone para fornecedores
- Diferentes compradores tomam decisões diferentes para o mesmo produto

### Sistema com IA (MVP)
- Sugestão automática de compra baseada na previsão de demanda + estoque atual + estoque mínimo dinâmico
- Considera lead time do fornecedor (ex.: leite leva 3 dias para chegar, então pedido é antecipado)
- Comprador aprova, ajusta ou rejeita com um clique
- Pedido é gerado automaticamente no sistema do fornecedor após aprovação

---

## 3. Recomendação no PDV

### Sistema Atual
- PDV apenas registra a venda e emite cupom/NFe
- Nenhuma sugestão de produtos adicionais no momento da compra
- Cliente compra apenas o que veio buscar — oportunidades de venda cruzada perdidas

### Sistema com IA (MVP)
- Algoritmo de market basket analysis identifica produtos comprados juntos com frequência
- No momento da venda, sistema sugere item complementar na tela do operador
- Exemplos reais:
  - Leva carne? Sugere carvão e refrigerante
  - Leva feijão? Sugere arroz
  - Leva fralda? Sugere lenço umedecido
- Operador pergunta: *"O(a) senhor(a) também vai levar [produto]?"*
- Meta: aumentar ticket médio em 10%

---

## 4. Detecção de Anomalias em Perdas

### Sistema Atual
- Perda é registrada manualmente pelo estoquista (vencimento, avaria, extravio)
- Não há cruzamento de dados para identificar padrões suspeitos
- Furto interno/externo passa despercebido até o inventário físico (que é mensal)
- Relatório de perdas é apenas uma planilha somando valores — sem análise de causa

### Sistema com IA (MVP)
- ML monitora continuamente os registros de perda por loja, turno, categoria e funcionário
- Detecta anomalias como:
  - *"Loja X registra 3x mais perda por avaria em eletrônicos que as demais lojas"*
  - *"Perdas no turno da noite são 50% maiores que no turno da manhã"*
  - *"Produto Y teve 10 registros de extravio no mesmo mês — provável furto"*
- Gera alerta automático para o gerente investigar
- Classifica perda por causa provável: vencimento, manuseio, furto, erro de sistema

---

## Fluxo do MVP

### Cenário Atual
```
Venda PDV → Planilha manual de saldo → Comprador decide compra →
  → Telefone/e-mail para fornecedor → Chegada da mercadoria →
    → Conferência manual → Atualização da planilha
```

### Cenário com IA
```
Venda PDV → Baixa automática no estoque →
  → ML prevê demanda futura →
    → Abaixo do mínimo? → Sugestão de compra inteligente →
      → Comprador aprova com 1 clique →
        → Pedido eletrônico enviado ao fornecedor →
          → Entrada no estoque → Saldo atualizado em tempo real
                              → ML detecta anomalias em perdas
```

---

## Tecnologias

| Camada | Tecnologia |
|--------|-----------|
| Frontend | React + TypeScript |
| Backend | Node.js (API) + Python (ML) |
| Banco de Dados | PostgreSQL |
| ML | scikit-learn, pandas, numpy |
| Vizualização | Chart.js / Recharts (dashboard) |
| Mobile | React Native (para inventário futuro) |

---

## Critérios de Sucesso

| Indicador | Meta |
|-----------|------|
| Redução de ruptura de estoque | 20% |
| Redução de perdas totais | 15% |
| Aumento do ticket médio (recomendação) | 10% |
| Precisão da previsão de demanda | > 80% |
| Tempo do comprador na decisão de compra | Redução de 50% |
