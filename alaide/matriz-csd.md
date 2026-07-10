# Matriz CSD — Alaide (Documentação) | Aplicativo Atual do Atacadão

## Certezas

**O app Meu Atacadão é focado no cliente final (B2C)**
> O app disponível na Play Store e App Store oferece ofertas exclusivas, folhetos promocionais e compras online — não tem funcionalidades de gestão de estoque interno.

**O app tem scanner de preços por código de barras**
> O usuário pode escanear o código de barras de qualquer produto para ver o preço atualizado em tempo real.

**O sistema atual não oferece visibilidade de estoque em tempo real para gerentes**
> Os documentos do projeto indicam que gerentes não têm dashboard com saldo atualizado, indicadores ou alertas.

**O Atacadão possui ERP próprio que controla estoque, vendas e logística**
> Conforme noticiado, o Carrefour está migrando suas lojas para o ERP do Atacadão, que serve como "cérebro comercial" da operação.

**As transferências entre lojas não possuem rastreamento digital integrado**
> O processo de movimentação entre depósitos é lento e sem rastreabilidade segundo o levantamento de requisitos.

**Perdas são difíceis de justificar por falta de dados**
> Produtos vencem, estragam ou somem sem registro de quando, onde ou por quê, conforme documento de requisitos.

## Suposições

**Um novo módulo de inventário mobile com leitor de código de barras agilizaria a contagem**
> O scanner de preços do app atual prova que a tecnologia de leitura de código de barras já existe — falta aplicá-la ao inventário interno.

**Um dashboard gerencial integrado ao ERP existente agilizaria decisões**
> Se o ERP já controla estoque e vendas, um painel com indicadores em tempo real aproveitaria dados já existentes.

**Alertas automáticos de estoque baixo evitariam rupturas**
> Notificações no sistema quando um produto atingir o mínimo evitariam gôndolas vazias e perda de vendas.

**Registro digital de perdas com causa facilitaria a justificativa**
> Um campo obrigatório no sistema para registrar motivo, data e responsável pela perda geraria dados para análise.

## Dúvidas

**O ERP do Atacadão possui API aberta para integração com novos módulos?**
> Sem API, qualquer novo sistema precisaria acessar o banco de dados diretamente ou via arquivos, o que é mais arriscado.

**O app Meu Atacadão compartilha banco de dados com o ERP interno?**
> Se o app B2C e o ERP usam bancos separados, a integração de dados em tempo real pode ser um desafio técnico.

**Qual a volumetria atual de SKUs por loja?**
> O número de produtos impacta performance, armazenamento e estratégia de indexação do banco de dados.

**As lojas possuem infraestrutura de rede adequada para um sistema em tempo real?**
> Um dashboard e alertas em tempo real dependem de conectividade estável nas lojas físicas.
