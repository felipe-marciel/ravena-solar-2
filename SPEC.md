# Ravena Solar — SPEC resumido

## Objetivo

Criar um simulador público de energia solar e um painel de vendas que usem o mesmo motor de cálculo. A interface deve ser simples, responsiva e em português. Visitantes simulam sem cadastro e só depois podem pedir atendimento.

## Simulador e cálculo

- Entrada: valor mensal da conta, cidade atendida e, opcionalmente, consumo em kWh. Ligação bifásica por padrão.
- Conta de até R$ 200: explicar que não compensa; não mostrar resultado financeiro nem formulário.
- Acima de R$ 200: mostrar estimativas de sistema, investimento, conta após instalação, economia no primeiro ano e prazo de retorno. Informar que não é proposta nem garantia.
- Estimar o consumo quando não for informado; dimensionar por geração regional, usando módulos de 550 W e a tabela comercial validada.
- Nunca estimar conta zero. Calcular o retorno em cenário conservador, sem reajuste futuro de tarifa e respeitando o cronograma do Fio B.
- Exibir fontes e datas. Se faltar dado essencial ou ele estiver vencido, ocultar os resultados afetados e explicar o motivo.
- “Outra cidade” usa a cidade atendida de maior custo total e encaminha o pedido ao administrador.

## Pedidos e painel de vendas

- Pedido opcional: nome, WhatsApp, cidade e conta em PDF/JPG/PNG/WEBP, até 10 MB.
- Guardar um retrato reproduzível da simulação, com dados, fontes, vigências e versão do algoritmo.
- Carlos atende Sorocaba/Votorantim; Renata, Itu/Salto; administrador vê todos os pedidos. Aplicar permissões no servidor, inclusive aos anexos.
- Vendedores podem corrigir dados e recalcular, preservando o resultado original e o histórico.
- Estados do pedido: Chegou, Respondi, Visita marcada, Proposta enviada, Fechou e Não vai.

## Privacidade e limites

- Anexos restritos ao administrador e ao vendedor responsável; permitir remoção.
- Três meses após Fechou ou Não vai, apagar ou anonimizar dados pessoais e anexos. Não registrar dados pessoais em logs.
- Não incluir edição manual dos parâmetros, financiamento, baterias, sistemas acima de 75 kWp, cidades fora do raio ou propostas automatizadas.
- Antes do lançamento, validar fontes oficiais e premissas tarifárias, comerciais e regionais. Documentar decisões, exclusões, dados tratados, testes e revisão adversarial.
