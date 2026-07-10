# Matriz CSD — Ed (Back-end e DevOps) | Aplicativo Atual do Atacadão

## Certezas

**O app Meu Atacadão é focado no cliente final (B2C)**
> O app disponível na Play Store e App Store oferece ofertas exclusivas, folhetos promocionais e compras online — não tem funcionalidades de gestão de estoque interno.

**O app tem scanner de preços por código de barras**
> O usuário pode escanear o código de barras de qualquer produto para ver o preço atualizado em tempo real.

**O app permite ativar cupons de desconto personalizados**
> O cliente ativa ofertas no app e informa CPF/CNPJ no caixa para abater os descontos.

**O app tem integração com iFood, Rappi e Cornershop**
> As compras online podem ser feitas via parceiros de delivery, além do site próprio com Click & Retire.

**O Atacadão possui ERP próprio que controla estoque, vendas e logística**
> Conforme noticiado, o Carrefour está migrando suas lojas para o ERP do Atacadão, que serve como "cérebro comercial" da operação.

**O sistema atual não oferece visibilidade de estoque em tempo real para gerentes**
> Os documentos do projeto indicam que gerentes não têm dashboard com saldo atualizado, indicadores ou alertas.

**As transferências entre lojas não possuem rastreamento digital integrado**
> O processo de movimentação entre depósitos é lento e sem rastreabilidade segundo o levantamento de requisitos.

**O checkout diferencia preço CPF e CNPJ manualmente**
> O operador de caixa precisa saber qual preço aplicar para cada tipo de cliente, sem auxílio claro do sistema.

## Suposições

**Um novo módulo interno de gestão de estoque resolveria as dores operacionais**
> O app B2C já existe e funciona bem para clientes — a carência é de um sistema interno para estoquistas, gerentes e operadores de caixa.

**Um dashboard gerencial integrado ao ERP existente agilizaria decisões**
> Se o ERP já controla estoque e vendas, um painel com indicadores em tempo real aproveitaria dados já existentes.

**Alertas automáticos de estoque baixo evitariam rupturas**
> Notificações push ou no sistema quando um produto atingir o mínimo evitariam gôndolas vazias.

**Automação da diferenciação de preço CPF/CNPJ reduziria erros no caixa**
> O sistema poderia aplicar o preço correto automaticamente com base no tipo de cliente identificado no PDV.

## Dúvidas

**O ERP do Atacadão possui API aberta para integração com novos módulos?**
> Sem API, qualquer novo sistema precisaria acessar o banco de dados diretamente ou via arquivos, o que é mais arriscado.

**O app Meu Atacadão compartilha banco de dados com o ERP interno?**
> Se o app B2C e o ERP usam bancos separados, a integração de dados em tempo real pode ser um desafio técnico.

**Qual a volumetria atual de SKUs por loja?**
> O número de produtos impacta performance, armazenamento e estratégia de indexação do banco de dados.

**As lojas possuem infraestrutura de rede adequada para um sistema em tempo real?**
> Um dashboard e alertas em tempo real dependem de conectividade estável nas lojas físicas.

**O sistema atual atende às regras fiscais de transferência interestadual?**
> Transferências entre estados envolvem ICMS e prazos de NF-e que o novo sistema precisará respeitar.
