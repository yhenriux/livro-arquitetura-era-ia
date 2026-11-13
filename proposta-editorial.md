# De onde vem a resposta?

**Arquitetura da informação para produtos com IA**

Proposta editorial para a Casa do Código · Yago Henrique Andrade Almeida · novembro de 2026

Título e subtítulo provisórios

## Panorama

“Sou da pós-graduação. Posso renovar um livro que está reservado?” A pergunta parece simples. Um assistente pode respondê-la em segundos e ainda citar a versão errada do regulamento. Para ajudar a pessoa a decidir o que fazer, ele precisa encontrar a regra vigente, distinguir o pedido de renovação da reserva feita por outra pessoa e mostrar de onde tirou a resposta. Cada uma dessas tarefas depende de escolhas sobre como a informação foi organizada.

Minha proposta é ensinar a fazer essas escolhas em produtos com inteligência artificial. A arquitetura da informação reúne práticas de organizar, nomear e tornar encontrável o que as pessoas precisam saber. Quando uma interface passa a produzir respostas, esse trabalho chega ao conteúdo que o sistema consegue consultar, às evidências que recupera e à forma como as apresenta. Uma regra pode ser fácil de ler na página original e perder o sentido quando o sistema recupera um trecho separado da exceção. A escolha de onde começa e termina esse trecho passa a afetar o que a pessoa pode fazer a partir da resposta.

O projeto retoma a investigação que comecei em *Arquitetura de Informação para Chatbots*. Ali, a conversa era o ponto de partida para organizar conteúdo e orientar a interação. Nesta proposta, sigo a pergunta pelo sistema inteiro, da fonte à resposta, incluindo busca, assistentes e agentes. Assim, o desenho de diálogo ganha o apoio de fontes consultáveis, respostas verificáveis e regras de atualização, acesso e responsabilidade pelo conteúdo.

Esse problema aparece em produtos que já precisam responder a partir de manuais, políticas e bases de atendimento. Equipes de design, conteúdo e engenharia passam a decidir juntas o que é uma fonte autorizada, quando uma exceção precisa acompanhar a regra e como testar se a resposta continua correta depois de uma atualização. O livro oferece um caso trabalhado de ponta a ponta, em português, para que essas decisões possam ser discutidas, prototipadas e avaliadas em conjunto.

## Público e ganhos de leitura

Escrevo para pessoas de design de produto, UX Writing, conteúdo, arquitetura da informação e biblioteconomia que participam de projetos com IA, além de profissionais de produto e engenharia que projetam busca, assistentes ou bases de conhecimento. A parte principal pode ser acompanhada com familiaridade básica com produtos digitais. Experimentos opcionais apresentam as etapas técnicas com exemplos pequenos e dados fictícios.

As atividades desenvolvem cinco capacidades que a pessoa leitora poderá aplicar em projetos próprios.

- Mapear perguntas reais de um serviço e identificar de quais informações cada resposta depende.
- Modelar um acervo com vocabulário, metadados, vigência e responsabilidade pela fonte.
- Comparar maneiras de segmentar e recuperar conteúdo, observando quando a regra chega separada de sua exceção.
- Projetar respostas que mostrem a evidência, façam perguntas de esclarecimento e encaminhem situações que exigem atendimento humano.
- Montar um conjunto de testes e rastrear se uma falha veio da fonte, da busca, da composição da resposta ou da interface.

## Projeto prático

Ao longo do livro, a pessoa leitora projeta um assistente para uma biblioteca universitária fictícia. A pergunta sobre renovar um livro reservado abre o caso. Depois entram fontes com datas diferentes, termos que as pessoas usam de maneiras diferentes e situações em que falta informação para responder. O projeto avança com pequenos exercícios de diagnóstico e decisões registradas, de modo que o mesmo caso possa ser revisitado a cada mudança.

O resultado será um projeto de assistente auditável, com inventário de fontes, modelo de conteúdo, exemplos de recuperação e respostas, roteiro de avaliação e plano de manutenção. O repositório acompanhará o manuscrito com exemplos reproduzíveis à medida que forem escritos.

## Ementa comentada

**De onde vem a resposta?** A renovação do livro revela o caminho entre a dúvida da pessoa e o regulamento que sustenta a resposta. O primeiro exercício pede que a pessoa leitora identifique de onde veio uma resposta aparentemente correta e registre o dado de que ainda precisa.

**O que a pessoa precisa saber para agir.** A partir das perguntas de atendimento, o capítulo distingue necessidade de informação, termos usados na conversa e tarefa a realizar. O exercício produz um conjunto inicial de perguntas, incluindo casos ambíguos e perguntas que exigem esclarecimento.

**O que a biblioteca sabe e quem pode afirmar.** Inventário, fontes oficiais, autoria, vigência e responsabilidade pela atualização entram no mesmo caso. A atividade monta um inventário e identifica o que fazer quando duas fontes parecem sustentar respostas diferentes.

**Como representar regras, exceções e relações.** Vocabulário controlado, taxonomias e metadados ajudam a ligar diferentes formas de dizer a mesma coisa e a registrar para quem uma regra vale. O exercício modela categoria de usuário, tipo de material, estado da reserva e condições de renovação.

**Como a evidência chega à resposta.** O capítulo introduz a geração aumentada por recuperação, conhecida como RAG, e trabalha segmentação de documentos, busca lexical e semântica, filtros e ordenação. O exercício compara trechos recuperados com e sem a exceção que muda a resposta.

**Como responder quando a fonte deixa dúvidas.** O caso avança para citações, perguntas de esclarecimento, abstenção e encaminhamento. Também distingue responder sobre uma regra de executar uma renovação, ação que depende de identidade, permissão e confirmação. A atividade desenha respostas para perguntas completas, ambíguas e sem evidência suficiente.

**Como avaliar a resposta e localizar a falha.** O capítulo propõe testes de recuperação, fundamentação e conclusão da tarefa. A pessoa leitora usa um conjunto de perguntas esperadas e investiga falhas da fonte, da busca e da interface, inclusive quando a resposta tem uma citação que não sustenta a afirmação.

**Como manter a resposta válida.** O caso se fecha com versionamento, permissões, revisão de conteúdo e testes de regressão. A atividade final simula a mudança de uma regra e verifica quais fontes, respostas e testes precisam ser atualizados antes de publicar a alteração.

## Original disponível

O primeiro capítulo apresenta o caso da Biblioteca Ipê, uma ficha de fonte e quatro testes que podem ser feitos com os materiais da própria leitura. A bibliografia será desenvolvida junto com o manuscrito. A revisão da literatura em andamento orienta a seleção de fontes e exemplos para os próximos capítulos. [Ler o primeiro capítulo](01-de-onde-vem-a-resposta.md)

## Livros semelhantes e posição no catálogo

- Em *Engenharia de IA do protótipo à produção*, Leonardo Pena percorre implementação, avaliação e operação de sistemas com LLMs, RAG e agentes. *De onde vem a resposta?* se concentra nas decisões sobre fontes, representação, recuperação e apresentação que design, conteúdo e engenharia precisam tomar em conjunto. [Casa do Código](https://www.casadocodigo.com.br/products/livro-engenharia-ia)
- Em *User Experience Design*, Rogério Pereira aborda arquitetura da informação, modelagem de conteúdo, interfaces e usabilidade no processo de criação de produtos digitais. Minha proposta acompanha essas decisões quando a interface consulta fontes e compõe respostas diferentes a cada pergunta. [Casa do Código](https://www.casadocodigo.com.br/products/livro-ux-produtos-digitais)
- *Information Architecture: For the Web and Beyond*, de Louis Rosenfeld, Peter Morville e Jorge Arango, é uma referência para organização, navegação, busca e encontrabilidade. O caso da biblioteca aproxima esses fundamentos do trabalho de selecionar evidências, formular respostas e verificar se continuam válidas após mudanças nas fontes. [O’Reilly](https://www.oreilly.com/library/view/information-architecture-4th/9781491913529/)

## Divulgação

Pretendo apresentar a pergunta da biblioteca e alguns exercícios em artigos no LinkedIn e na UX Potion. Para o lançamento, proponho uma oficina em que profissionais de conteúdo, design e engenharia possam examinar juntos uma resposta, localizar a falha e reconstruir a evidência. O material de divulgação pode incluir um trecho autorizado e uma versão do exercício para uso em aulas e comunidades de UX, biblioteconomia e IA. Formato e agenda serão combinados com a editora.

## Minibiografia

Sou Yago Henrique Andrade Almeida, bibliotecário de formação pela UFMG e professor de Arquitetura da Informação e Design Centrado no Usuário. Trabalho como Staff AI Solutions Architect no Inter, com foco em arquitetura de soluções, agentes, governança, avaliação e confiabilidade de sistemas com IA. Sou doutorando em Ciência e Tecnologia Web pela Universidade de Trás-os-Montes e Alto Douro e pela Universidade Aberta de Portugal. Escrevo a UX Potion e pesquiso como a informação é organizada e recuperada em sistemas digitais. Este livro reúne perguntas que atravessam meu trabalho em Biblioteconomia, design conversacional e engenharia de IA. [Site e portfólio](https://yagohenrique.com.br/) · [LinkedIn](https://www.linkedin.com/in/yhenria/)

## Organização da escrita

Proponho começar pelo alinhamento editorial da ementa e do capítulo de amostra. A escrita pode avançar em três entregas. A primeira cobre fundamentos e fontes, a segunda trabalha recuperação e desenho das respostas, e a terceira chega à avaliação e manutenção. Cada entrega incorpora os exercícios correspondentes e o material do projeto prático, com tempo para revisão antes da próxima. A sequência e as datas podem ser acertadas com a Casa do Código para o calendário de 2027.
