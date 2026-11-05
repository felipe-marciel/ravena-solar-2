# Ravena Solar — SPEC

## Objetivo e escopo

Simulador público de energia solar e painel de vendas, usando **o mesmo motor de cálculo**. Visitantes simulam sem cadastro; quem quiser atendimento envia pedido depois de ver o resultado. O botão atual da P1 leva ao simulador. Interface em português, simples e responsiva, sobretudo no celular.

## Fluxo público

- Entrada: valor mensal da conta e cidade (**Sorocaba, Votorantim, Itu, Salto** ou **Outra cidade da região**); consumo em kWh opcional. Ligação bifásica por padrão.
- Conta de **até R$ 200**: explicar que não compensa; sem resultado financeiro e sem formulário.
- Acima de R$ 200: mostrar potência e quantidade estimadas de painéis, investimento, conta após instalação, economia do primeiro ano e prazo de retorno, antes de pedir dados pessoais. Deixar claro que é estimativa, não proposta nem garantia; proposta exige visita técnica.
- Pedido opcional: nome, WhatsApp, cidade e anexo PDF/JPG/PNG/WEBP de até 10 MB. Guardar com o pedido um retrato reproduzível do que foi digitado, mostrado e usado no cálculo, incluindo fontes, datas, vigências e versão do algoritmo.
- “Outra cidade”: calcular todas as variáveis geográficas pela cidade atendida de maior custo total; encaminhar o pedido ao administrador para triagem.

## Cálculo e dados

O mesmo motor calcula resultado público e revisões do vendedor. Estimar consumo pelo valor da conta e custo efetivo vigente por kWh quando não informado; usar consumo informado para dimensionar quando disponível. Dimensionar pela geração regional, converter para módulos de 550 W arredondando para cima e aplicar a tabela comercial Ravena (referência do brief: R$ 2.300–2.900/kWp, mais barato em sistemas maiores). Nunca projetar conta zero: incluir disponibilidade por ligação, energia não compensada, Fio B, bandeira e iluminação pública local. Exibir economia do primeiro ano.

Retorno em um único cenário conservador, ano a ano: sem reajuste futuro de tarifa e com Fio B conforme cronograma legal até 2029. Não prometer retorno fora do horizonte calculado. Se dado essencial estiver indisponível, vencido ou fora da vigência, ocultar resultados financeiros e informar o motivo; nunca calcular silenciosamente com dado antigo. Tarifas seguem a vigência oficial; bandeira vale para o mês anunciado. Mostrar fonte e data.

Dados oficiais integrados são somente leitura e devem respeitar suas vigências. Não haverá painel para edição manual de tarifas, bandeiras ou outros parâmetros pelo administrador. Antes do lançamento, confirmar fórmula tarifária e tributos, fontes e tolerâncias de atualização, tabela comercial, horizonte de retorno, projeção da bandeira, iluminação pública e premissas regionais. Não inventar esses valores. Se um dado essencial não puder ser obtido de fonte oficial ou de premissa validada, ocultar os resultados financeiros afetados e informar o motivo.

## Painel, acesso e privacidade

Carlos acessa apenas Sorocaba/Votorantim; Renata, apenas Itu/Salto; administrador acessa todos os pedidos. O painel administrativo não inclui edição de parâmetros do cálculo. Aplicar autorização no servidor, inclusive em anexos. Estados: Chegou, Respondi, Visita marcada, Proposta enviada, Fechou, Não vai. Vendedor pode corrigir valor, consumo, cidade e ligação e recalcular; preservar resultado original e histórico auditável. Autenticação obrigatória; proteção forte para administrador.

Dados guardados: nome, WhatsApp, cidade, valor/consumo, tipo de ligação, retratos e revisões de simulação, anexo de conta (pode conter endereço, CPF, instalação e histórico de consumo), usuário e trilha de auditoria. Anexo restrito ao administrador e vendedor responsável, removível. Pedidos ativos ficam enquanto em atendimento; após Fechou/Não vai, apagar ou anonimizar dados pessoais e anexos em **3 meses**. Evitar dados pessoais em logs; manter apenas estatística não reidentificável.

## Aceitação e limites

Validar o corte de R$ 200, reprodução do retrato, rejeição de anexos inválidos/maiores que 10 MB, isolamento entre vendedores, recálculo sem sobrescrever original, bloqueio por dado vencido e expurgo em 3 meses. Testar especialmente cálculos financeiros, permissões, uploads e retenção; documentar revisão adversarial e correções no projeto. README deve listar decisões, exclusões e dados pessoais tratados.

Fora do escopo: edição manual de números ou parâmetros pelo administrador (a quarta funcionalidade do brief), financiamento, baterias, comércio acima de 75 kWp, cidades fora do raio e proposta comercial automatizada. O escopo prioriza três funcionalidades completas: simulador público, pedido detalhado e painel de vendas com recálculo pelo mesmo motor. Cálculo e lançamento dependem de validar as fontes oficiais e premissas pendentes acima.
