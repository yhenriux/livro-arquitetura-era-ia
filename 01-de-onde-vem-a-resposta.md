# De onde vem a resposta?

Uma estudante de pós-graduação abre o assistente da biblioteca da universidade. A dúvida é simples.

> Posso renovar um livro se outra pessoa já fez uma reserva?

O assistente responde que sim. Explica que estudantes de pós-graduação podem renovar empréstimos pelo portal e até indica onde fica o botão. A estudante abre o portal. A renovação foi bloqueada.

O que você faria se essa falha chegasse à sua equipe? Talvez pedisse ao assistente para ser mais cuidadoso ou testasse um modelo mais recente. Antes de mexer nessas duas coisas, eu abriria os documentos da biblioteca. Quero saber se a regra correta estava disponível, se chegou ao assistente e se a resposta respeitou a condição que ela descreve.

A biblioteca deste capítulo é fictícia. Vamos usar a mesma pergunta para investigar o que muda quando a regra é difícil de localizar, quando a busca recupera um trecho inadequado e quando a resposta ignora uma condição presente no trecho recuperado. Ao fim do capítulo, você terá uma ficha de fonte e um primeiro conjunto de testes para distinguir essas situações.

## Uma regra escrita em dois lugares

A equipe da Biblioteca Ipê mantém uma página de perguntas frequentes e um regulamento de circulação. Podemos começar com os trechos que interessam para a conversa.

| Fonte | Trecho | Estado no caso didático |
| --- | --- | --- |
| Perguntas frequentes, edição de 2024 | “Estudantes de pós-graduação podem renovar seus empréstimos pelo portal da biblioteca.” | Material de orientação de uma edição anterior |
| Regulamento de circulação, edição de 2026, art. 12 | “A renovação do empréstimo é permitida quando não houver reserva ativa para o exemplar. A condição se aplica a todas as categorias de usuários.” | Norma vigente, publicada pela biblioteca |

A página de perguntas frequentes parece responder diretamente à estudante. Menciona pós-graduação, renovação e portal. O regulamento usa termos mais gerais e só permite a renovação se o exemplar estiver sem reserva ativa. A estudante incluiu justamente essa condição na pergunta.

Também vale reparar na palavra *exemplar*. A biblioteca pode ter três exemplares de um título. O título identifica a obra no catálogo. O exemplar identifica a unidade que está emprestada. Para responder de acordo com o regulamento, precisamos saber se a reserva ativa diz respeito ao exemplar em questão. Na primeira pergunta, a estudante usa “livro” no sentido cotidiano. Um bom atendimento consegue explicar a regra nesse vocabulário e, quando a distinção fizer diferença, nomear o exemplar.

Já temos duas decisões de projeto. A primeira é indicar qual fonte tem autoridade para estabelecer a regra de renovação. A segunda é representar a relação entre empréstimo, exemplar e reserva. Nenhuma delas depende de escolher um fornecedor de IA. Ambas mudam o que a estudante pode fazer depois de ler a resposta.

## O que estamos arquitetando?

Em arquitetura da informação, costumamos trabalhar com organização, rótulos, navegação e busca. Esses elementos ajudam pessoas a compreender um ambiente informacional e encontrar o que precisam nele. Em um produto que responde com IA, parte desse trabalho também orienta o software que seleciona e apresenta informação. A estudante talvez nunca veja o catálogo de documentos. Ainda assim, a maneira como ele foi organizado chega até ela na forma de uma resposta. [Rosenfeld, Morville e Arango, *Information Architecture*](https://www.oreilly.com/library/view/information-architecture-4th/9781491913529/ch04.html)

Quando a bibliotecária responde no balcão, ela sabe que uma página explicativa pode estar desatualizada e que o regulamento define a regra. Também consegue distinguir uma pergunta geral de um pedido de consulta ao empréstimo da estudante. Para transformar esse conhecimento em comportamento do produto, a equipe precisa registrá-lo em algum lugar que seja consultável. Pode ser na identificação das fontes, nas regras de seleção ou na própria interface. O importante é que a decisão fique explícita e possa ser testada.

Três perguntas ajudam a equipe a localizar as decisões que precisa tomar.

1. **Que informação precisa ser encontrada?** Uma regra vigente de renovação aplicável ao caso.
2. **Que detalhe muda a resposta?** A existência de reserva ativa para o exemplar.
3. **Que informação a pessoa precisa para agir?** A regra, a fonte que a sustenta e, quando for o caso, onde consultar a situação do próprio empréstimo.

Essas perguntas conectam três trabalhos que frequentemente acontecem em reuniões diferentes. A Biblioteconomia ajuda a descrever o documento e distinguir sua autoridade. Design e conteúdo ajudam a formular uma resposta compreensível e a decidir quando pedir esclarecimento. A engenharia transforma essas decisões em seleção de fontes, contexto e comportamento verificável. Cada área enxerga uma parte do mesmo percurso.

## Do documento à resposta

Vamos percorrer o caminho que a pergunta pode seguir. A biblioteca publica documentos. O sistema registra os documentos e os prepara para busca. Quando chega uma pergunta, a busca seleciona trechos. Uma parte deles é entregue ao modelo como contexto. A resposta produzida pode apresentar os trechos de origem, ou ao menos permitir que a pessoa os encontre.

Quando uma aplicação recupera informação de uma fonte externa e usa esse material para orientar a geração de texto, estamos diante do princípio de *Retrieval-Augmented Generation*, ou RAG. A implementação pode incluir várias formas de busca e seleção. Neste capítulo, basta distinguir o momento de **encontrar a informação** do momento de **escrever com base nela**. Essa separação nos dá dois pontos de inspeção quando algo falha. [Lewis et al., *Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks*](https://arxiv.org/abs/2005.11401)

No caso da biblioteca, o assistente poderia receber apenas a frase da página de perguntas frequentes. A conclusão “sim” faria sentido diante daquele trecho isolado, embora continuasse inadequada para a pergunta da estudante. Se ele recebesse o art. 12 completo e ainda respondesse “sim”, nossa investigação mudaria de lugar. Examinaríamos como o modelo tratou a condição, o que mais recebeu no contexto e se a resposta final foi conferida contra a fonte.

Existe uma terceira possibilidade. O sistema recupera o artigo correto, porém corta a frase logo antes de “quando não houver reserva ativa”. O texto que chega ao modelo contém parte de uma regra e perdeu a condição que lhe dava sentido. Escolher onde um trecho começa e termina é uma decisão de arquitetura da informação. Quando a condição, a exceção e a regra dependem umas das outras, precisamos mantê-las juntas ou fornecer uma maneira de recuperá-las em conjunto.

O ponto de partida do diagnóstico é guardar o que foi recuperado e o que chegou ao modelo. Em um protótipo, basta registrar o identificador da fonte, a versão e a seção usada no teste. Um produto em operação exige decidir quem pode acessar esse registro e por quanto tempo mantê-lo. O exemplo deste livro usa documentos e perguntas fictícios, sem dados de empréstimos de pessoas reais.

## Como o sistema reconhece a fonte certa?

Uma busca pode aproximar textos pela similaridade de termos ou de sentido. Para a pergunta da estudante, a página antiga pode ficar bem colocada porque menciona diretamente seu perfil. O resultado também pode trazer o regulamento porque fala em renovação e reserva ativa. A similaridade ajuda a encontrar candidatos. A decisão sobre qual documento governa o caso depende de atributos que a biblioteca conhece e precisa registrar.

Comece com uma ficha simples. Vamos preenchê-la para o regulamento fictício.

| Campo | Valor no exemplo | Como o produto usa |
| --- | --- | --- |
| Identificador | `REG-CIRC-2026` | Localiza o documento e conecta a resposta ao registro usado |
| Título | Regulamento de circulação | Apresenta um nome reconhecível para a pessoa leitora |
| Seção | Art. 12 | Permite verificar a condição no trecho certo |
| Estado e versão | Vigente, edição de 2026 | Distingue a regra em uso de edições anteriores |
| Responsável | Coordenação da Biblioteca Ipê | Identifica quem mantém a regra e pode resolver dúvidas |
| Abrangência | Todas as categorias de usuários | Permite aplicar a condição também à pós-graduação |
| Assuntos e variantes | Renovação, empréstimo, reserva ativa, prorrogar devolução | Ajuda a localizar a regra quando a pergunta usa outras palavras |

Essa ficha reúne **metadados**, ou seja, informações que descrevem a fonte. Alguns ajudam na descoberta. Outros orientam a aplicação da regra. A versão é útil para as duas tarefas. “2026” informa qual edição foi usada e, junto do estado de vigência, permite escolher a fonte aplicável. Se amanhã aparecer uma minuta com data mais recente, o campo de estado ainda importa. Uma minuta de 2027 pode ser posterior e continuar sem efeito.

Os rótulos também merecem cuidado. “Prorrogar a devolução” pode ser uma forma de pedir “renovar o empréstimo”. “Reservar o livro” descreve outra ação. Se a equipe tratar tudo como uma lista de palavras equivalentes, a busca vai confundir tarefas diferentes. Um vocabulário controlado permite registrar os termos preferidos, as variantes e as relações entre conceitos. O padrão SKOS distingue, por exemplo, rótulos preferidos e alternativos. Para começar nosso projeto, uma tabela com essas distinções já permite discutir os casos. [W3C, *SKOS Simple Knowledge Organization System Reference*](https://www.w3.org/TR/skos-reference/)

Com a ficha em mãos, a equipe pode definir uma regra verificável de seleção. Quando a pergunta for sobre o que é permitido, priorize o regulamento vigente e o artigo aplicável. A FAQ pode complementar a resposta com o caminho no portal. Se dois regulamentos apresentados como vigentes trouxerem condições incompatíveis, o assistente deve indicar o conflito e encaminhar a dúvida para a biblioteca.

## Uma resposta que a estudante consegue conferir

Voltemos à pergunta inicial. Ela já inclui a condição necessária para explicar a regra. O assistente poderia responder assim.

> Se houver uma reserva ativa para o exemplar que está com você, a renovação fica bloqueada. Essa regra também vale para estudantes de pós-graduação. Você pode conferir a regra no art. 12 do Regulamento de circulação da Biblioteca Ipê, edição de 2026.

O nome do documento, a edição e o artigo dão à estudante uma maneira de conferir a resposta. Em uma interface real, o nome da fonte pode levar ao trecho e a equipe pode preservar um identificador estável para a versão consultada. Esse rastro é parte da **proveniência**. Ele permite reconstruir de onde veio a informação, sob responsabilidade de quem e em que versão. [W3C, *An Overview of the PROV Family of Documents*](https://www.w3.org/TR/prov-overview/)

Agora imagine que a estudante queira saber a situação do próprio empréstimo.

> Tem alguma reserva para o livro que está comigo agora?

A resposta depende de um dado atual do sistema de empréstimos. A norma informa o que acontece **se** houver uma reserva. Consultar se existe uma reserva requer acesso ao registro do exemplar emprestado, no contexto de uma sessão autorizada. Neste primeiro protótipo, a biblioteca publica a regra, e o assistente orienta a estudante a consultar a situação do empréstimo no portal. Quando a equipe acrescentar integração com o catálogo, terá de testar também o que o assistente pode consultar em nome da pessoa.

Repare no papel da citação. Uma resposta pode trazer um link e ainda atribuir à fonte algo que ela nunca disse. Também pode citar corretamente uma edição antiga e aplicar a regra errada. Por isso, ao testar, abra a fonte e procure o trecho que sustenta cada afirmação importante. Gao e colegas distinguem a qualidade da atribuição, a correção e a fluência do texto. Para o nosso caso, a pergunta é esta. Consigo chegar da condição informada na resposta ao trecho vigente que a estabelece? [Gao et al., *Enabling Large Language Models to Generate Text with Citations*](https://aclanthology.org/2023.emnlp-main.398/)

## Experimente com quatro perguntas

Use os dois trechos da biblioteca e a ficha do regulamento. Você pode fazer o exercício no papel, numa planilha ou no repositório de um projeto. Primeiro, preencha a resposta esperada. Depois, registre qual fonte seria recuperada e confira se o trecho entregue ao modelo contém a condição inteira.

| Pergunta ou condição de teste | Resposta esperada | O que verificar |
| --- | --- | --- |
| “Faço pós. Posso renovar se há reserva ativa para o meu exemplar?” | Explicar o bloqueio e citar o art. 12 vigente | A regra foi aplicada também à pós-graduação |
| “Dá para prorrogar a devolução se o meu exemplar está sem reserva?” | Dizer que o art. 12 permite a renovação nessa condição | A busca reconheceu “prorrogar a devolução” |
| “Tem reserva para o meu empréstimo agora?” | Explicar a regra, orientar consulta ao portal e deixar a situação do exemplar em aberto | A resposta respeitou o limite de acesso aos dados |
| Fazer a primeira pergunta com apenas a FAQ de 2024 disponível | Informar que a fonte disponível é insuficiente para responder sobre a condição | O assistente evitou concluir com base numa orientação genérica |

Para conferir o diagnóstico, repita o primeiro teste com a FAQ e o art. 12 juntos. Imagine que a busca tenha localizado o regulamento, mas que o contexto enviado ao modelo termine em “A renovação do empréstimo é permitida”. Se a resposta disser “sim”, o primeiro ajuste é manter a condição junto da regra ao preparar os trechos. Se a condição completa já estava no contexto, examine como a resposta foi composta e se há evidência de que a regra foi aplicada. Em ambos os casos, registre a fonte recuperada, o trecho enviado e a frase exibida. Esse registro permite reproduzir o problema com a equipe.

Depois de alterar qualquer parte, repita as quatro perguntas. Uma mudança que corrige a primeira resposta pode prejudicar a segunda, especialmente se restringir demais os termos da busca.

Se quiser aplicar o exercício a um produto seu, comece com uma pergunta que costuma gerar retrabalho no atendimento. Escolha duas fontes que uma pessoa da equipe consultaria. Anote quem é responsável por cada fonte, qual vale para aquela situação e que informação mudaria a resposta. Escreva também uma variação em que o produto deva pedir um dado ou encaminhar a pessoa para outro canal. Esse caso de fronteira costuma mostrar decisões que a equipe ainda precisa tomar.

## O que levamos para o projeto

A estudante precisava decidir se podia renovar o livro. Para ajudá-la, a biblioteca teve de distinguir a orientação da norma, representar a condição da reserva e tornar a origem da resposta acessível. O mesmo trabalho pode aparecer sob outras formas. Uma central de suporte precisa localizar a versão válida de um procedimento. Um assistente de produto precisa informar quando uma funcionalidade se aplica a determinado plano. Em ambos os casos, vale começar pela decisão que a pessoa quer tomar e rastrear a informação necessária até a sua fonte.

No próximo capítulo, vamos organizar as perguntas do atendimento a partir daquilo que as pessoas precisam fazer. Esse trabalho vai orientar o inventário de fontes da biblioteca. Antes de seguir, pense no seu próprio projeto. Se uma resposta importante fosse contestada amanhã, qual parte do caminho entre a fonte e a pessoa sua equipe conseguiria reconstruir?
