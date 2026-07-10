# Matriz CSD — William (Front-end e Banco de Dados) | Carlos Silva (Operador de Caixa)

## Certezas

1. **O sistema trava em horários de pico**
   > O PDV demora a responder quando o movimento da loja aumenta, gerando filas e clientes insatisfeitos.

2. **Preço CPF/CNPJ não é claro no sistema**
   > O operador precisa memorizar ou consultar fora do sistema qual preço aplicar — não há indicação visual na tela.

3. **Não há consulta de estoque no PDV**
   > No momento da venda, o operador não consegue ver se o produto tem saldo disponível antes de finalizar a compra.

## Suposições

1. **Interface simples reduziria filas no caixa**
   > Um PDV leve, com poucos cliques por venda, agilizaria o atendimento e melhoraria a experiência do cliente.

2. **Automação do preço CPF/CNPJ evitaria erros**
   > Se o sistema identificar automaticamente o tipo de cliente e exibir o preço correto, o operador não precisaria decidir.

3. **Consulta de estoque no PDV evitaria vendas sem produto**
   > Ver o saldo antes de finalizar permitiria ao operador avisar o cliente ou sugerir um similar.

## Dúvidas

1. **O hardware do PDV suporta um novo sistema?**
   > Máquinas antigas podem não rodar um front-end moderno ou integrar com novas bibliotecas.

2. **Qual o volume de transações nos horários de pico?**
   > Saber o pico de vendas ajuda a dimensionar o banco de dados e a infraestrutura para evitar lentidão.

3. **O sistema legado tem API para integrar com o PDV?**
   > Para conectar o PDV ao estoque e à emissão fiscal, o sistema antigo precisa expor interfaces de comunicação.

---

## Fonte

- Google Play — Meu Atacadão (funcionalidades do app B2C)
- Atacadão S.A. — site oficial e Group Carrefour Brasil
- Times Brasil | CNBC — reportagem sobre integração do ERP do Atacadão
- Documentos do projeto: levantamento de requisitos, personas e mapa de empatia
