# Registro da entrevista para o SPEC

Este documento registra as perguntas feitas durante a entrevista de definição do simulador Ravena Solar e as respostas do usuário. Respostas curtas como “Ok” confirmam a proposta apresentada imediatamente antes. Pequenas edições de redação foram feitas para facilitar a leitura, sem alterar as decisões.

## Contexto inicial

**Pergunta:** O que você quer construir? Descreva quem vai usar e qual problema a solução deve resolver.

**Resposta:** “Utilize o brief.md como contexto.”

## Decisões registradas

### Corte para contas de baixo valor

**Pergunta:** Qual deve ser o critério para dizer que uma conta é baixa demais para compensar: valor fixo, valor por cidade ou cálculo de viabilidade?

**Resposta:** “Considere como sendo um valor fixo.”

**Pergunta:** Qual o valor exato do limite? O brief cita R$ 200 como exemplo.

**Resposta:** “Use 200 reais mesmo.”

### Método de cálculo

**Pergunta:** Devemos começar pelo método de cálculo da economia e do retorno ou pelas regras de acesso e privacidade?

**Resposta:** “Qual você achar melhor.” A entrevista seguiu pelo método de cálculo.

**Pergunta:** A conta após a instalação deve considerar bandeira tarifária, iluminação pública por cidade, custo mínimo da ligação e Fio B?

**Resposta:** “Sim.”

**Pergunta:** Como calcular o tempo de retorno? Foi sugerida uma projeção ano a ano, com reajustes tarifários e do Fio B e premissas conservadoras.

**Resposta:** O usuário perguntou se seria interessante oferecer três cenários — conservador/realista, desastroso e esperançoso — ou manter apenas o conservador.

**Recomendação apresentada:** Um cenário conservador, com premissas e data dos dados visíveis, para evitar falsa precisão.

**Confirmação:** “Ok.”

### Tipo de ligação

**Pergunta:** Qual tipo de ligação assumir por padrão? Foi sugerida bifásica, com correção pelo vendedor depois da leitura da conta.

**Resposta:** “Ok.”

### Arquivo da conta e retenção

**Pergunta:** Como tratar foto/PDF da conta, que pode conter CPF e endereço? Foi sugerido acesso restrito ao administrador e vendedor responsável, com possibilidade de remover o arquivo.

**Resposta:** “Ok.”

**Pergunta:** Por quanto tempo manter pedidos e dados da simulação? Foi sugerido manter pedidos ativos durante o atendimento e apagar ou anonimizar os encerrados após prazo definido.

**Resposta:** “Ok.”

**Pergunta:** Quantos meses após o encerramento?

**Resposta:** “Considere 3 meses.”

### Administração e dados oficiais

**Pergunta:** Quem pode alterar tarifas, bandeiras, custos, premissas e demais números? Foi sugerido que somente o administrador altere parâmetros globais; vendedores corrigem os dados de cada lead.

**Resposta:** “Ok.”

**Pergunta:** Foi sugerida autenticação forte para a conta administrativa. (A sugestão foi incorporada ao SPEC.)

**Resposta:** “Ok.”

**Pergunta:** Se dados públicos estiverem desatualizados ou indisponíveis, usar o último valor conhecido com aviso ou bloquear resultados?

**Resposta:** O usuário perguntou qual opção seria melhor.

**Recomendação apresentada:** Ocultar o resultado financeiro até os dados essenciais estarem válidos; não usar dado antigo que possa produzir estimativa enganosa.

**Confirmação:** Primeiro, “Não.” Em seguida, ao ser perguntado qual comportamento preferia, respondeu: “Ocultar os resultados financeiros.”

**Pergunta:** Como definir “desatualizado” para tarifas e bandeiras? Foi sugerido respeitar o período de vigência oficial e mostrar a data de referência.

**Resposta:** O usuário perguntou em quanto tempo tarifas e bandeiras costumam mudar. Foi explicado que tarifas seguem períodos de vigência normalmente anuais, e bandeiras são definidas mensalmente pela ANEEL.

**Confirmação:** “Ok.”

### Ordem do fluxo público

**Pergunta:** A pessoa deve informar nome, WhatsApp e cidade antes de ver o resultado, ou só se quiser a simulação detalhada depois?

**Resposta:** “Ela preenche os dados somente depois de ver os números.”

**Pergunta:** Para contas de até R$ 200, mostrar explicação de que não compensa, sem simulação nem formulário?

**Resposta:** “Ok.”

### Correções dos vendedores

**Pergunta:** Quais campos o vendedor pode corrigir? Foram sugeridos consumo, valor da conta, tipo de ligação e cidade, mantendo histórico das simulações refeitas.

**Resposta:** “Ok.”

### Parâmetros editáveis e cidades

**Pergunta:** Foram sugeridos parâmetros comerciais editáveis e dados oficiais vinculados a fontes, mais confirmação das quatro cidades, anexos e demais premissas.

**Resposta 1:** “Os dados que podem ser obtidos de forma precisa por meio de APIs não devem ser possíveis de alterar manualmente, já as outras sim.”

**Resposta 2:** “Existe também o ‘Outra cidade da região’, que talvez dê para pensar o pior dos cenários, onde ele pega a cidade mais cara e trata como se a pessoa morasse nessa cidade.”

**Pergunta de esclarecimento:** Usar o pior cenário somente nos custos específicos da cidade ou em todas as variáveis da estimativa?

**Resposta:** “À todas as variáveis.”

### Anexos e projeção conservadora

**Pergunta:** Foi proposta projeção conservadora com tarifa sem reajuste futuro e Fio B seguindo cronograma legal até 2029. Também foi proposta aceitação de PDF, JPG e PNG até 10 MB.

**Resposta:** “Sim e coloque além dessas 3, WEBP.”

**Decisão consolidada:** Tarifa sem reajustes futuros na projeção conservadora; Fio B conforme cronograma legal até 2029; anexos PDF, JPG, PNG e WEBP, limite de 10 MB.

## Encerramento

Após a entrevista, o usuário autorizou a criação do `SPEC.md` com: “Pode criar o SPEC, por favor.” Depois pediu que o SPEC coubesse em uma página. Este registro documenta a entrevista e não substitui a especificação vigente.
