
Primeiramente, gostaria de fazer uma breve introdução ao Bitrix. **Bitrix24** é uma plataforma criada na Rússia para facilitar a organização de negócios com uma abordagem integrada. Ela oferece um CRM para gerenciar clientes e vendas, automações para simplificar tarefas repetitivas e ferramentas de colaboração que mantêm as equipes conectadas.

Além disso, o Bitrix24 centraliza a gestão de tarefas e projetos, comunicação interna (chat e videoconferências) e até processos de RH, tudo em um único lugar. Com acesso via nuvem e aplicativos móveis, a plataforma permite que as equipes trabalhem de forma eficiente, de qualquer lugar.

O Bitrix oferece um nível totalmente gratuito de utilização, onde podemos ter acesso a um CRM simplificado, de certa forma, podemos desfrutar de diversas ferramentas, porém ficamos limitados a algumas opções e automações do próprio Bitrix, por conta disso, peço que, considerem que para esse guia, estou utilizando de uma assinatura paga da plataforma, para ter acesso a todas as funções possíveis.

Em um primeiro momento, quando temos nosso primeiro contato com a plataforma, podemos ficar extremamente confusos, o que é perfeitamente normal, de certa forma, o Bitrix oferece uma vasta gama de funcionalidades, páginas, e configurações, o que pode facilmente confundir um novo usuário. Por esse motivo, começarei esse guia com uma rápida apresentação da plataforma.


#### Primeiro contato:
A completar ainda
#### Um pouco sobre automações e a API do Bitrix

Agora que temos uma visão mais geral sobre as principais abas do Bitrix, podemos aprofundar um pouco mais no universo de automações de alguns processos. De certa forma, podemos criar automações para a plataforma de três formas diferentes. Podemos começar a explicar então sobre as automações nos fluxos. 

##### Modelos de automações para CRM

Aqui teremos uma das formas mais convencionais de criar automações, onde podemos definir tanto automações de nível global, que podem ser ativadas de qualquer Pipeline possível, e também podemos criar Modelos de automações  para serem chamadas e ativadas em um determinado momento em um fluxo de uma pipeline, veremos essa segunda opção melhor quando chegarmos nas automações de Fluxo. Para acessar essa ferramenta, podemos fazer da seguinte forma: 

 Podemos seguir o seguinte passo a passo, já no nosso CRM, podemos clicar em Mais > Configurações > Configurações do CRM que está localizado no canto superior direito da aba, logo acima da barra de pesquisa dos cards:
![[Pasted image 20241111155011.png|659]]

![[Pasted image 20241111153040.png|659]]

Então,

![[Pasted image 20241111153418.png|659]]

A partir desse momento, teremos diversas opções de "área" de atuação dos nossos modelos, neste guia me aprofundarei apenas nos modelos dos "Deals", podendo aparecer também como "Negócio":
![[Pasted image 20241111154447.png|659]]
Aqui temos duas opções, podemos criar um novo modelo, ou podemos também Listar os modelos já existentes, além de listar, podemos também ver e editar essas automações. Como esse guia tem a intenção de demonstrar as funcionalidades, vamos criar um novo Modelo e explicar um pouco de como funciona para configurar e ativar uma automação a partir de um modelo.

###### Parte prática 1: Demonstrando a Criação de automações de modelos
Aqui vamos criar uma situação fictícia onde precisaremos desenvolver uma automação para um problema X, vamos criar o seguinte cenário, que será utilizado para desenvolver as problemáticas ao longo dessa documentação:

Voce acabou de instalar o Bitrix24 e já começou a utilizá-lo, Criou no seu CRM, uma Pipeline de Clientes e uma Pipeline do Financeiro, para acompanhar emissão de notas, e para ter um visão geral de como vai a contabilidade da sua empresa ao longo do ano. Para atualizar seu fluxo de financeiro, voce copiava os Cards do seu Fluxo de Clientes para o Fluxo Financeiro mensalmente, por ter poucos clientes, essa duplicação não era tão trabalhosa assim, porém, sua empresa teve um Boom repentino, e de repente, voce se viu responsável por duplicar Milhares de cards manualmente, e como todo seus contratos são de 12 meses, esse evento trabalhoso vai se repetir por diversos meses. Apenas em pensar nessa carga intensa de trabalho você já ficou cansado, e por isso, você abriu o google e pesquisou sobre automações no Bitrix24, e por pura coincidência você encontrou esse mesmo guia, sendo assim, vamos entender melhor o que podemos fazer para sanar esse problema. 

Primeiramente, antes de acessar a aba de modelos, precisamos ir até a nossa Pipeline de Clientes, e acessar qualquer um dos Cards que estiverem no nosso fluxo. Com um card aberto, podemos descer a página dele até encontrar na esquerda a seguinte opção:

![[Pasted image 20241111165204.png|340]]
A partir dessa opção, poderemos criar um campo personalizável, que apesar de ser criado dentro de um card específico, será criado para todos os outros cards do fluxo, e até para os que irão ser criados posteriormente, no caso, vamos criar um campo de lista chamado "1 - Copiar para financeiro?"  e vamos configurar ele pra receber apenas dois valores: "Sim" e "Não", vamos ver como podemos fazer isso:
![[Pasted image 20241111170832.png|340]]

Podemos configurar esse campo da seguinte forma:
![[Pasted image 20241111171001.png|340]]

Certo, dessa forma, podemos salvar e agora teremos acesso a esse campo no nosso Fluxo inteiro.

Antes de iniciarmos a criação da automação, é importante esboçar um "Mapa Mental" dos passos necessários. Embora isso possa parecer repetitivo e cansativo, no Bitrix24, uma automação pode rapidamente crescer e se tornar complexa. Ao desenhar o fluxo que a automação deve seguir, conseguimos nos organizar melhor e identificar possíveis falhas ou problemas que poderiam comprometer todo o processo. Além disso, mapear o processo previamente ajuda a visualizar melhorias que poderiam simplificar e otimizar a automação. É essencial lembrar que, com o tempo, nossa memória pode falhar, e ajustar um fluxo complexo depois de muito tempo pode se tornar uma tarefa árdua, especialmente se esquecermos o propósito de determinados elementos. Por isso, essa etapa de planejamento é crucial para economizar tempo e facilitar futuras manutenções. Sendo assim, precisamos pensar em todos os elementos que precisamos usar e posteriormente, após desenhar o fluxo de uma forma bem idealista precisamos pensar em possíveis erros que podemos ter com aquele fluxo:





##### Automações de Fluxo
Basicamente, esse tipo de automação é bem útil quando pensamos em automações mais ligadas a um fluxo especifico, onde precisamos que em determinadas etapas, gatilhos específicos daquele fluxo aconteçam, dentre as opções que veremos, essa é mais limitada, onde podemos configurar algumas coisas sobre os cards do fluxo, mas nem por isso essa opção chega a ser inutilizável, na verdade, ela pode ser bem útil para automatizar processos mais simples, como para limpar um campo específico quando o card chegar naquele fluxo, ou até mesmo para ativar automaticamente outras automações. Agora que sabemos o básico sobre essa ferramenta, vamos acessar, dentro dos Fluxos de Leads, Deals ou Tasks, vamos acessar essa aba que pode ser identificada por esse pequeno "robozinho" destacado na imagem abaixo em verde:

![[Pasted image 20241107145851.png]]

Ao clicar nessa caixinha, teremos a esse a algo muito parecido com isso:
![[Pasted image 20241107153354.png|659]]

Vamos focar primeiramente na primeira aba "Regras de automação". Aqui podemos ver que basicamente temos o fluxo Kanban do nosso fluxo original, logo abaixo do nome das fases temos um símbolo de "+" onde poderemos configurar as automações específicas para cada fase do nosso fluxo, quando criadas, poderemos visualizar todas elas no campo de Gatilhos, que fica um pouco mais abaixo, vamos nos familiarizar mais com essa opção, ao clicar no + de qualquer uma das etapas, teremos algo parecido com isso aqui:

![[Pasted image 20241111135800.png|659]]

Logo no cabeçalho da janela, podemos destacar a opção "Adicionar à etapa 'Novos Negócios' ", ao clicar em Novos Negócios, teremos acesso a todas as fases do nosso fluxo.

![[Pasted image 20241111141210.png|659]]


















