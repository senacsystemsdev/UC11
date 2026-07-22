# Problema Identificado — Controle de Validade e Prevenção de Perdas no Atacadão

**UC11:** Gerir Projetos de Tecnologia da Informação  
**Equipe:** William, Alaide, Ed  
**Data:** 22/07/2026

---

## 1. Contexto do Cliente

O **Atacadão** é uma rede de supermercados do grupo Carrefour com presença nacional, operando no formato atacarejo (atacado + varejo). A unidade de negócio enfrenta desafios críticos relacionados à gestão de validade de produtos e prevenção de perdas, agravados por:

- Operação em larga escala com múltiplas filiais
- Alto volume de produtos perecíveis com prazo de validade reduzido
- Processos manuais e reativos de controle de estoque
- Fiscalização rigorosa por órgãos reguladores (MPDFT, MP-BA)

---

## 2. O Problema

### 2.1 Perda Financeira

O varejo brasileiro perdeu **R$ 42,1 bilhões** em 2025, equivalente a **1,65%** do faturamento total do setor (fonte: ABRAPPE — 9ª Pesquisa de Prevenção de Perdas no Varejo Brasileiro). Deste total:

| Causa | Participação |
|-------|-------------|
| Vencimento / Validade | 35% |
| Furto externo | 25% |
| Avaria / Manuseio | 20% |
| Furto interno | 12% |
| Erro de sistema | 8% |

O Atacadão, por operar com alto giro de estoque e grande variedade de perecíveis, é diretamente impactado por essas perdas.

### 2.2 Risco Sanitário e Legal

- **TAC nº 851/2023 (MPDFT):** O Ministério Público do Distrito Federal firmou Termo de Ajustamento de Conduta com o Atacadão Dia a Dia após fiscalização encontrar **113 produtos vencidos** em uma única loja em Samambaia/DF. O TAC permanece vigente, com metas de adequação e monitoramento contínuo.
- **Investigação MP-BA (março/2026):** O Ministério Público da Bahia investiga denúncias graves em loja de Salvador:
  - Substituição de carnes escolhidas por produtos de menor qualidade ou vencidos
  - Moagem de carnes fora do prazo de validade para vendê-las como novas
  - Recongelamento de carnes totalmente descongeladas

### 2.3 Falha Operacional no ERP

O Atacadão já possui controle de lote e validade no ERP **TOTVS Consinco/RMS**, mas:

- A execução do controle é falha — não há alertas preditivos
- A detecção de produtos vencidos ocorre apenas no inventário físico mensal
- Não há integração entre dados de validade e velocidade de venda
- Perdas por avaria, furto e erro de sistema não são cruzadas para identificar padrões

### 2.4 Impactos

| Impacto | Consequência |
|---------|-------------|
| **Financeiro** | Perda de R$ 42,1 bi/ano no setor; impacto direto no lucro do Atacadão |
| **Legal** | Multas, indenizações, TAC vigente com MPDFT, investigação do MP-BA |
| **Reputacional** | Danos à imagem da marca; notícias negativas na imprensa |
| **Operacional** | Processos manuais, retrabalho, falta de visibilidade em tempo real |
| **Cliente** | Risco à saúde do consumidor; experiência negativa de compra |

---

## 3. Evidências

| Evidência | Fonte |
|-----------|-------|
| Perdas de R$ 42,1 bi no varejo em 2025 (alta de 15,3%) | ABRAPPE, 2025 |
| 113 produtos vencidos encontrados em 1 loja | MPDFT, TAC nº 851/2023 |
| Investigação por carnes impróprias em Salvador | BNews, março/2026 |
| Desabastecimento de carnes em lojas do Atacadão | Estadão, novembro/2024 |
| Índice de ruptura em supermercados | Neogrid, maio/2026 |
| Transformação digital no Atacadão | Diário do Comércio, 2025 |

---

## 4. Por Que Resolver Agora?

1. **TAC vigente:** O Atacadão está formalmente comprometido com o MPDFT a adequar seus processos
2. **Investigação em andamento:** MP-BA pode resultar em novas sanções
3. **Crescimento das perdas:** Alta de 15,3% em relação ao ano anterior (ABRAPPE)
4. **Concorrência:** Redes concorrentes já investem em transformação digital para prevenção de perdas
5. **Exigência do consumidor:** Mercado cada vez mais exigente com qualidade e segurança alimentar

---

## 5. Oportunidade

Implementar um sistema de **Controle de Validade e Prevenção de Perdas com IA** que:

- Monitore em tempo real o risco de vencimento de cada lote
- Sugira ações preventivas (desconto, realocação, descarte programado)
- Detecte anomalias em perdas (furto, avaria, erro de sistema)
- Se integre ao ERP TOTVS existente
- Gere relatórios para auditoria e prestação de contas ao MP

**Meta:** Reduzir produtos vencidos a zero, diminuir perdas totais em 15% e reduzir tempo de detecção de perdas em 70%.
