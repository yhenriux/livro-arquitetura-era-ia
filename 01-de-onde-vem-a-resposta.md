# De onde vem a resposta?

## A pergunta da estudante

“Faço pós-graduação. Posso renovar um livro se outra pessoa já fez uma reserva?”

Imagine que essa pergunta chegue ao assistente de uma biblioteca universitária. O assistente responde que sim e indica o botão de renovação no portal. A estudante segue a orientação. O portal bloqueia a operação.

Por onde você começaria a investigar? Eu abriria a página de perguntas frequentes, o regulamento e a tela do empréstimo. Quero saber qual regra vale, que informação a estudante consegue ver e em que momento a resposta se afastou do que o serviço permite fazer.

A Biblioteca Ipê é fictícia. No nosso exemplo, uma FAQ de 2024 explica que estudantes de pós-graduação podem renovar empréstimos pelo portal. O regulamento vigente de 2026 acrescenta uma condição no art. 12. A renovação é permitida quando o exemplar está sem reserva ativa. A condição vale para todas as categorias de usuários.

Se a equipe resolver o problema apenas na conversa, ainda terá de perguntar se a mesma condição aparece no portal e se a bibliotecária consegue explicá-la no balcão. Talvez o catálogo tenha três exemplares do mesmo título. O regulamento se refere ao exemplar emprestado. A palavra “livro”, perfeitamente compreensível na conversa, pode designar o título ou a unidade que está com a estudante. Precisamos representar essa diferença na informação que o serviço usa e decidir quando ela importa para a pessoa.

## De onde vem a Arquitetura da Informação?

Quando alguém entra em uma biblioteca e pergunta onde estão os livros sobre um assunto, uma parte da resposta já está inscrita no espaço. A classificação agrupou obras, o catálogo descreveu os exemplares e as placas ajudam a pessoa a se orientar. Essas escolhas têm consequências. Uma classificação pode aproximar obras que a pessoa procuraria juntas. Uma descrição pode permitir que ela encontre um título mesmo quando conhece apenas o assunto.

A Biblioteconomia e a Documentação desenvolveram formas de organizar, descrever e relacionar materiais. Em 1876, Melvil Dewey publicou um esquema de classificação decimal para bibliotecas. Paul Otlet e Henri La Fontaine partiram desse esquema para desenvolver a Classificação Decimal Universal, usada no Repertório Bibliográfico Universal. [Dewey, *A classification and subject index*](https://www.gutenberg.org/ebooks/12513) · [Mundaneum, Repertório Bibliográfico Universal](https://mundaneum.org/en/collections-and-resarch/our-collections/the-universal-bibliographic-repertory-rbu/)

O *Traité de documentation*, publicado por Paul Otlet em 1934, sistematiza questões de representação e acesso a documentos. A relação com o nosso caso aparece quando precisamos decidir o que será uma unidade de informação. Podemos descrever um regulamento inteiro, identificar cada artigo e registrar a relação entre eles. Essa escolha muda o que pode ser encontrado e citado. [Paul Otlet, *Traité de documentation*](https://mundaneum.org/articles/librairie/autour-du-mundaneum/le-livre-sur-le-livre-traite-de-documentation/)

Outra trajetória passa pelas maneiras de conectar informações. Em 1945, Vannevar Bush descreveu trilhas associativas no Memex, um dispositivo imaginado para consulta e associação de registros. Em 1965, Ted Nelson discutiu estruturas de informação interligadas em seu trabalho sobre processamento complexo da informação. Esses textos pertencem a contextos históricos diferentes. Eles nos ajudam a formular uma pergunta que reaparece no catálogo da Biblioteca Ipê. Que relação entre dois registros vale a pena tornar explícita para que alguém consiga seguir adiante? [Bush, *As We May Think*](https://www.w3.org/History/1945/vbush/vbush5.shtml) · [Nelson, *Complex Information Processing*](https://doi.org/10.1145/800197.806036)

Richard Saul Wurman levou à prática de projeto a preocupação com a compreensão de informações complexas. Em 1998, Rosenfeld e Morville sistematizaram para a Web práticas de organização, rotulagem, navegação e busca. A quarta edição da obra, escrita também com Jorge Arango, trata de ambientes informacionais que se estendem por canais e serviços. No Brasil, Flávia Macedo, Alfram Albuquerque, Mamede Lima-Marques e André Siqueira investigaram como fundamentar e caracterizar a disciplina. Essas tradições oferecem pontos de partida diferentes para investigar um mesmo produto. [Wurman, *Information Anxiety*](https://www.wurmanarchive.org/shop/p/information-anxiety) · [Rosenfeld e Morville, edição de 1998](https://www.oreilly.com/library/view/information-architecture-for/1565922824/) · [Rosenfeld, Morville e Arango, *Information Architecture*](https://www.oreilly.com/library/view/information-architecture-4th/9781491913529/) · [Macedo, *Arquitetura da informação*](https://repositorio.unb.br/handle/10482/35858?locale=en) · [Albuquerque e Lima-Marques, *Sobre os fundamentos da Arquitetura da Informação*](https://periodicos.ufpb.br/index.php/pgc/article/view/10827) · [Siqueira, *Arquitetura da informação*](https://repositorio.unb.br/handle/10482/12157)

Neste livro, vou tratar a Arquitetura da Informação como o trabalho de projetar estruturas que permitem encontrar, compreender, relacionar e usar informação em determinado contexto. A definição nos ajuda a examinar tanto um catálogo navegável quanto uma classificação automatizada ou uma resposta de IA. Em cada caso, vamos perguntar que estrutura foi escolhida, quem pode usá-la e como sabemos se ela ajuda.

## Quatro sistemas de uma mesma arquitetura

Talvez você já tenha ouvido falar em taxonomias, mapas de site ou mecanismos de busca. Onde entra cada um? Os quatro sistemas descritos por Rosenfeld, Morville e Arango oferecem um ponto de partida. Na Biblioteca Ipê, cada sistema leva a uma decisão diferente sobre a renovação. [Rosenfeld, Morville e Arango, *Information Architecture*](https://www.oreilly.com/library/view/information-architecture-4th/9781491913529/)

| Sistema | Pergunta de projeto | Aplicação na biblioteca |
| --- | --- | --- |
| Organização | Como agrupamos e relacionamos a informação? | Relacionar obra, exemplar, empréstimo e reserva. Reunir orientações de renovação por tarefa. |
| Rotulagem | Que palavras ajudam a pessoa a reconhecer uma opção? | Usar “Renovar empréstimo” para a ação e reconhecer “prorrogar a devolução” como uma forma de procurá-la. |
| Navegação | Como a pessoa entende onde está e aonde pode ir? | Levar de “Meus empréstimos” ao estado do exemplar, à regra aplicável e ao atendimento. |
| Busca | Como a pessoa encontra informação por uma consulta? | Recuperar o artigo vigente mesmo quando a pergunta usa termos diferentes dos que aparecem no regulamento. |

A representação atravessa os quatro sistemas. Ao registrar que um empréstimo se refere a um exemplar e que uma reserva pode estar ativa ou encerrada, a equipe transforma uma distinção do serviço em relações que a interface e o software conseguem usar. O rótulo “Reserva ativa” comunica um estado. Para mostrá-lo no momento certo, precisamos saber de que registro veio, quando foi atualizado e a quem pode ser exibido.

Em 2026, Daiane Procópio e Patrícia Silva usaram os quatro sistemas para analisar como estudos publicados entre 2022 e 2025 tratavam a informação em modelos de linguagem. O trabalho oferece um modo de reconhecer escolhas de organização, rotulagem, navegação e busca em aplicações recentes. Na Biblioteca Ipê, a distinção ajuda a fazer um diagnóstico. Se a estudante escolheu a opção errada, precisamos examinar o rótulo e o percurso. Se a opção estava certa e a orientação contrariou a regra vigente, precisamos verificar a fonte e como o sistema a usou. [Procópio e Silva, *Organização e Arquitetura da Informação em Large Language Models*](https://ojs.uel.br/revistas/uel/index.php/informacao/article/view/53808)

Uma arquitetura de conteúdo também ajuda a manter a regra e suas condições ligadas. Se o portal, o atendimento e o assistente usam três cópias independentes da orientação, a equipe precisa descobrir quais devem mudar quando o regulamento for atualizado. Um inventário com fonte, versão, seção e responsável permite localizar a regra e suas reutilizações. Esses dados sobre a fonte são metadados. Eles ajudam a preservar a proveniência, isto é, a informação sobre de onde o conteúdo veio e como foi produzido. [W3C, *PROV Overview*](https://www.w3.org/TR/prov-overview/)

## Pessoas, conteúdo e contexto

A estudante precisa tomar uma decisão. A bibliotecária precisa explicar a regra. A equipe de produto precisa descobrir se o portal mostra uma saída quando o bloqueio ocorre. O mesmo conteúdo participa de tarefas diferentes e circula entre pessoas, sistemas e canais. É isso que vamos observar quando falarmos em ecologia da informação.

Resmini e Rosati discutem a Arquitetura da Informação pervasiva, que acompanha experiências distribuídas entre canais. Na Biblioteca Ipê, a pessoa pode descobrir a condição no site, consultar o empréstimo pelo celular e pedir ajuda no balcão. Cada canal tem suas possibilidades. A continuidade depende de como a biblioteca organiza os estados, as orientações e a passagem de uma etapa para outra. [Resmini e Rosati, *Pervasive Information Architecture*](https://shop.elsevier.com/books/pervasive-information-architecture/resmini/978-0-12-382094-5)

Há também uma decisão sobre acesso. O regulamento pode ser público. O estado do empréstimo de uma pessoa depende de uma sessão autorizada. Se o assistente tem acesso apenas à norma, pode explicar a condição e indicar onde consultar o empréstimo. Se receber permissão para consultar ou renovar, a equipe precisa definir qual ação foi autorizada, o que será confirmado com a pessoa e como corrigir um erro.

## O que muda quando o produto usa IA?

A mesma biblioteca pode usar IA em lugares diferentes. Um classificador pode sugerir assuntos para novos documentos. Para avaliar a sugestão, precisamos de categorias compreensíveis, exemplos e uma regra para casos que cabem em mais de uma categoria. Um recomendador pode usar assuntos para sugerir leituras. A pessoa precisa conseguir reconhecer o motivo da recomendação, ajustar preferências e explorar alternativas.

Um sistema de extração pode ler um regulamento digitalizado e propor campos como vigência e número do artigo. Uma validação pode conferir se a data extraída é de publicação ou de entrada em vigor. Um sistema de apoio à decisão pode sinalizar que uma renovação exige conferência quando o estado da reserva estiver indisponível. A interface precisa mostrar o que foi observado e o que ainda depende de confirmação. Um agente pode consultar o portal e executar uma ação autorizada. A distinção entre consultar e alterar um empréstimo precisa existir nas permissões e na própria experiência.

Quando um assistente recupera trechos de uma fonte externa para orientar a geração da resposta, temos uma aplicação de geração aumentada por recuperação, conhecida como RAG. No nosso caso, poderíamos verificar se o modelo recebeu a regra inteira, com a condição da reserva, e se a referência apontou para o artigo correto. Pesquisas sobre geração com citações distinguem a fluência do texto, a correção da resposta e a qualidade da atribuição. Essa distinção nos dá três perguntas de avaliação que podem produzir respostas diferentes para o mesmo teste. [Lewis et al., *Retrieval-Augmented Generation*](https://arxiv.org/abs/2005.11401) · [Gao et al., *Enabling Large Language Models to Generate Text with Citations*](https://aclanthology.org/2023.emnlp-main.398/)

Cada implementação muda as decisões que precisamos testar. No catálogo, posso observar se a pessoa encontra a regra. Na classificação, posso verificar se as categorias sugeridas correspondem aos critérios da biblioteca. Na conversa, posso conferir se a resposta preserva uma condição e indica o caminho para agir. Na renovação automática, preciso também verificar o estado atualizado e confirmar que a ação ocorreu no exemplar certo.

## Experimente na Biblioteca Ipê

Use a FAQ de 2024 e o regulamento fictício de 2026. Você pode simular as quatro situações no papel. Primeiro, anote que decisão cada caso exige. Depois, escreva o resultado esperado e registre onde a equipe procuraria a causa de um erro.

| Situação | Resultado esperado | O que investigar se falhar |
| --- | --- | --- |
| A estudante procura “prorrogar a devolução” no portal | Encontrar a orientação de renovação e a condição aplicável | Rótulos, termos alternativos e navegação |
| Um classificador recebe o art. 12 | Associar o artigo a renovação e reserva | Definição das categorias e possibilidade de múltiplos rótulos |
| O assistente recebe apenas a FAQ antiga e responde à pergunta sobre reserva ativa | Informar que precisa consultar a regra vigente ou encaminhar ao atendimento | Autoridade, vigência e suficiência da fonte |
| Um agente recebe o pedido “renove meu livro” em uma sessão com dois empréstimos | Identificar o exemplar antes de realizar a ação, verificar a condição e pedir confirmação | Representação da entidade, permissão e confirmação |

Escolha uma mudança e repita os quatro casos. Se a equipe acrescentar “prorrogar a devolução” como termo alternativo, observe se a busca passa a encontrar a página correta e se continua distinguindo renovação de reserva. Em um produto real, combine essa simulação com observação de pessoas realizando as tarefas. O exercício produz hipóteses sobre a arquitetura. O teste com pessoas ajuda a descobrir se os rótulos e percursos funcionam nas condições de uso.

## O que sua equipe consegue explicar?

A pergunta da estudante serviu para localizar decisões sobre agrupamento, linguagem, navegação, acesso e uso de fontes. Nos próximos capítulos, vamos investigá-las com pesquisa de necessidades, modelagem, prototipação e avaliação. Algumas vão aparecer em busca e conversação. Outras vão orientar recomendações, classificações, extração de dados e ações entre canais.

Pense em um produto que sua equipe projeta. Escolha uma informação que a pessoa precisa para tomar uma decisão. Quem a organiza, que caminho a pessoa pode percorrer até ela e como você verificaria se continua adequada quando uma fonte, regra ou interface muda?

[Bibliografia editorial](referencias.md)
