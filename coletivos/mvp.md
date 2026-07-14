# MVP — Central de Inteligência de Estoque (Atacadão)

**UC11:** Gerir Projetos de Tecnologia da Informação  
**Equipe:** William, Alaide, Ed

---

## Visão Geral

MVP de um sistema integrado de gestão de estoque com inteligência artificial, focado em reduzir ruptura, perdas e estoque excessivo na rede Atacadão.

---

## Funcionalidades

### 1. Previsão de Demanda (ML)
- Modelo preditivo baseado em histórico de vendas, sazonalidade e promoções
- Sugere quantidade ideal de compra por produto por período
- Reduz ruptura (falta de produto) e excesso de estoque

### 2. Sugestão Inteligente de Compras
- Alimentada pela previsão de demanda
- Considera estoque mínimo dinâmico e lead time do fornecedor
- Comprador aprova ou ajusta antes de gerar o pedido

### 3. Recomendação no PDV
- Análise de cestas de produtos (market basket analysis)
- Sugere itens complementares no momento da venda
- Exemplo: *"Quem comprou carne, leva carvão"*
- Objetivo: aumentar ticket médio do cliente

### 4. Detecção de Anomalias em Perdas
- ML identifica padrões atípicos de perda (avaria, extravio, furto)
- Gera alertas para o gerente da loja investigar
- Relatório mensal de perdas com classificação por causa provável

---

## Fluxo do MVP

```
Venda PDV → Baixa no estoque → ML prevê demanda futura →
  → Abaixo do mínimo? → Sugestão de compra com IA →
    → Aprovado? → Pedido ao fornecedor → Entrada no estoque
```

---

## Tecnologias

| Camada | Tecnologia |
|--------|-----------|
| Frontend | React |
| Backend | Node.js + Python (ML) |
| Banco de Dados | PostgreSQL |
| ML | scikit-learn / pandas |
| Mobile | React Native (para inventário futuro) |

---

## Critérios de Sucesso

- Redução de 20% na ruptura de estoque
- Redução de 15% nas perdas registradas
- Aumento de 10% no ticket médio (recomendação)
- Sugestão de compra com precisão > 80%
