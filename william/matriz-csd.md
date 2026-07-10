# Matriz CSD — William (Front-end e Banco de Dados) | Aplicativo Atual do Atacadão

## Certezas

**O app Meu Atacadão é focado no cliente final (B2C)**
> O app disponível na Play Store e App Store oferece ofertas exclusivas, folhetos promocionais e compras online — não tem funcionalidades de gestão de estoque interno.

**O app tem scanner de preços por código de barras**
> O usuário pode escanear o código de barras de qualquer produto para ver o preço atualizado em tempo real.

**O checkout diferencia preço CPF e CNPJ manualmente**
> O operador de caixa precisa saber qual preço aplicar para cada tipo de cliente, sem auxílio claro do sistema.

**O Atacadão possui ERP próprio que controla estoque, vendas e logística**
> Conforme noticiado, o Carrefour está migrando suas lojas para o ERP do Atacadão, que serve como "cérebro comercial" da operação.

**O sistema atual não oferece consulta de estoque integrada ao PDV**
> No momento da venda, o operador não consegue ver se o produto está disponível em estoque.

**O sistema atual tem desempenho lento em horários de pico**
> O aplicativo trava ou demora a responder quando o movimento da loja aumenta, gerando filas.

## Suposições

**Automação da diferenciação de preço CPF/CNPJ reduziria erros no caixa**
> O sistema poderia aplicar o preço correto automaticamente com base no tipo de cliente identificado no PDV.

**Um novo módulo interno de gestão de estoque resolveria as dores operacionais**
> O app B2C já existe e funciona bem para clientes — a carência é de um sistema interno para estoquistas, gerentes e operadores de caixa.

**Alertas automáticos de estoque baixo evitariam rupturas**
> Notificações no sistema quando um produto atingir o mínimo evitariam gôndolas vazias e perda de vendas.

**Integração da consulta de estoque ao PDV evitaria vendas sem produto**
> Se o operador visse o saldo na hora da venda, poderia avisar o cliente ou sugerir substituição.

## Dúvidas

**O ERP do Atacadão possui API aberta para integração com novos módulos?**
> Sem API, qualquer novo sistema precisaria acessar o banco de dados diretamente ou via arquivos, o que é mais arriscado.

**O app Meu Atacadão compartilha banco de dados com o ERP interno?**
> Se o app B2C e o ERP usam bancos separados, a integração de dados em tempo real pode ser um desafio técnico.

**Qual a volumetria atual de SKUs por loja?**
> O número de produtos impacta performance, armazenamento e estratégia de indexação do banco de dados.

**O sistema atual atende às regras fiscais de emissão de NF-e?**
> A emissão de cupom e NF-e precisa cumprir legislação fiscal específica que o novo sistema precisará implementar.

**As lojas possuem infraestrutura de rede adequada para um sistema em tempo real?**
> Um sistema de PDV integrado ao estoque depende de conectividade estável nas lojas físicas.
