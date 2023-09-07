# Título do Projeto (divulgável) - (Máximo de 450 caracteres):

Sistemas de Reputação Não Permissionados para Redes Públicas de Disseminação de Conteúdo

# Resumo em português (divulgável) - (Máximo de 2000 caracteres):

Sistemas de reputação permitem que usuários avaliem conteúdos e usuários de
modo a construir comunidades online com qualidade e confiança.
Esses sistemas aparecem em plataformas populares, tais como Facebook, Amazon e
Youtube.
No entanto, os sistemas vigentes são considerados permissionados, pois dependem
de uma autoridade central para validação e controle dos usuários.
Como uma alternativa possível, nós propomos o Freechains como um protocolo
peer-to-peer que permite a comunicação entre usuários desconhecidos mesmo em
fóruns de conteúdo público.
O Freechains introduz um sistema de reputação não permissionado em uma
blockchain com um algoritmo de consenso original.
Nesse projeto, propomos adaptar sistemas de reputação permissionados para o
sistema não permissionado do Freechains.
Ao final, pretendemos verificar a viabilidade de um sistema de reputação não
permissionado no lugar de sistemas permissionados, mesmo considerando a
presença de agentes maliciosos.

# Abstract em inglês (divulgável) - (Máximo de 2000 caracteres):

Reputation systems permit that users evaluate content and users in order to
build online communities with quality and trust.
These systems appear in popular platforms, such as Facebook, Amazon, and
Youtube.
However, the current systems are considered to be permissioned, since they
depend on a central authority to validate and control users.
As an alternative, we propose Freechains as a peer-to-peer protocol that
provides communication between unknown users even in public forums.
Freechains introduces a permissionless reputation system in a blockchain with
an original consensus algorithm.
In the end, we pretend to verify the feasibility of replacing permissioned
reputation systems with a permissionless alternative, even considering the
presence of malicious users in public forums.

# Introdução e justificativas - (Máximo de 9000 caracteres):

Sistemas de reputação são adotados com frequência na internet para construir
confiança em comunidades online.
As curtidas no Facebook, as avaliações de produtos na Amazon, ou os likes em
vídeos no Youtube são exemplos de avaliação de reputação que aparecem no nosso
cotidiano.
No entanto, todos esses sistemas são permissionados, ou seja, a autenticação
dos usuários ocorre através de um órgão central junto ao sistema de reputação.
Novos participantes de um sistema permissionado precisam se inscrever nesse
órgão e estão sujeitos às suas decisões, que muitas vezes podem ser
arbitrárias.

Atualmente, as principais redes sociais são propriedade de grandes empresas,
que por sua vez detém poder e informações pessoais de seus usuários em demasia.
Além disso, com a rápida adoção de plataformas de comunicação online, é difícil
que governos consigam regular essas empresas para proteger de abusos os seus
cidadãos de maneira efetiva.
Sendo assim, como escopo geral desse projeto, é desejável encontrar
alternativas não permissionadas, que não estejam sujeitas aos interesses de
empresas ou à morosidade de governos.

Um sistema de reputação não permissionado não deve depender de um órgão
central, devendo ser gerido pelos próprios usuários das comunidades online de
um modo auto suficiente.
No entanto, sem uma autoridade central, esse tipo de sistema traz dificuldades
para combater ataques e abuso da rede.
Como uma alternativa, o nosso grupo de pesquisa vêm desenvolvendo nos últimos
5 anos o Freechains, um protocolo peer-to-peer para comunicação em fóruns
públicos que pretende prover um sistema de reputação não permissionado.

# Objetivos - (Máximo de 9000 caracteres):

1. Substituir sistemas de reputação permissionados por não permissionados.
2. Aprimorar e validar um algoritmo de consenso distribuído.
3. Quantificar em números as regras concretas do sistema de reputação.
4. Prototipar e validar aplicações de redes sociais que efetivamente usam
   sistemas de reputação.

# Método - (Máximo de 9000 caracteres):

O Freechains é um sistema publish-subscribe no qual os usuários podem se
inscrever e publicar conteúdo em tópicos de interesse.
Cada tópico é estruturado como uma blockchain independente que é replicada na
rede e gerida de maneira descentralizada.
As postagens de cada tópico formam um Merkle-DAG que representa as relações
causais entre elas.
Um algoritmo de consenso próprio então ordena essas postagens e calcula a
reputação de cada usuário de forma determinística e global.
O algoritmo básico foi recentemente publicado, mas ainda precisa de
aprimoramentos e, principalmente, de uma validação rigorosa em um projeto
dedicado.
A ideia básica do algoritmo é disponibilizar uma reputação inicial ao pioneiro
do fórum, que é identificado em seu bloco gêneses.
Através de likes e dislikes, que transferem reputação entre usuários, o
pioneiro modera e modela o estado inicial do fórum.
Com o tempo, a ideia é que a reputação inicial do pioneiro se dispersa e o
fórum pode evoluir de maneira descentralizada.

Nós propomos modelar as operações gerais de reputação em fóruns públicos da
seguinte maneira:
A emissão de reputação se dá através de postagens antigas que, por estarem
consolidadas, premiam os seus autores com reputação.
Essa regra visa fomentar a criação de conteúdo.
O gasto de reputação se dá através de postagens novas que, por ainda não terem
sido validadas por outros usuários, reduzem a reputação dos seus autores.
Essa regra visa desestimular o excesso de conteúdo, tal como SPAM.
A transferência de reputação se dá através de curtidas, que servem para avaliar
o conteúdo entre usuários.
Essa regra visa destacar o conteúdo de qualidade e combater o conteúdo abusivo.
Através dessas regras, que já foram avaliadas por pares em um artigo recente,
entendemos que é possível oferecer um sistema de reputação em redes não
permissionadas.
Os valores exatos de emissão, gasto e transferência ainda precisam ser
quantificados através de casos de uso neste projeto.

A nossa proposta também visa recriar as aplicações que efetivamente usam
sistemas de reputação, tais como redes sociais públicas, mas agora em um
ambiente não permissionado.
Como caso de uso, propomos começar por um sistema inspirado no Reddit, já que é
uma das plataformas de fóruns públicos permissionadas mais utilizadas nos dias
de hoje.
Como proposta de metodologia, iremos coletar informações básicas de postagens
do sistema original, tais como data, autor e karma (sua unidade de reputação),
e depois replicá-las no Freechains e verificar se a adaptação foi bem sucedida.
Para validar o resultado, iremos verificar se o sistema simulado no Freechains
se comporta de forma aproximada ao sistema original.
A mesma metodologia pode ser aplicada a outras redes sociais.

A seguir, tomamos o Reddit como caso de uso para aprofundarmos a metodologia
proposta.
O Reddit oferece o conceito de subreddits para representar assuntos ou tópicos
diferentes.
Na nossa proposta, cada subreddit torna-se um tópico ou cadeia diferente
no Freechains, com sua própria blockchain independente.
Em uma dada cadeia, iremos simular as postagens do subreddit correspondente, de
modo a atingir uma equivalência entre os sistemas.
Cada comentário postado no Reddit também torna-se uma postagem no Freechains,
mas com um metadado associado diferente.
No Reddit um usuário pode avaliar positivamente ou negativamente uma postagem
ou comentário utilizando karma, e o mesmo pode ser feito no Freechains
utilizando likes e dislikes.

No fim, pretendemos responder se com o Freechains conseguimos, não só replicar
os benefícios de controle de abuso, tipicamente associados a sistemas
permissionados, mas também acrescentar os benefícios de descentralização,
tipicamente associados a sistemas não permissionados.

Cronograma:
https://docs.google.com/spreadsheets/d/1axP4RduwWCXfzI0iOISHWlQHhnmHxttTaO-5bkHAnkQ/edit#gid=399060574

# Resultados Esperados - (Máximo de 9000 caracteres):

1. Garantia de que todas as operações comuns em sistemas de reputação em
   ambientes permissionados também funcionam em ambientes não permissionados:
   remoção de conteúdo malicioso (SPAM, fake news), bloqueio de usuários
   maliciosos, destaque de conteúdo de qualidade, garantia de disponibilidade e
   escalabilidade de acesso, etc.
2. Obtenção de um algoritmo de consenso distribuído em um ambiente não
   permissionado, de modo que todas as operações na rede possam ser ordenadas
   de forma total, garantindo um resultado determinístico e idêntico em todos
   os nós da rede.
3. Definição de regras claras e efetivas para operações de moderação no sistema
   de reputação (likes, dislikes, block, post, etc), de modo que os usuários
   tenham transparência e entendimento no uso da rede.
4. Entrega de protótipo de uma aplicação de redes sociais real com o sistema
   de reputação não permissionado.

# Equipe envolvida - (Máximo de 9000 caracteres):

Além do proponente, existem dois alunos de Mestrado trabalhando com o sistema
Freechains:
- O Lucas d'Amaral está avaliando sistemas de reputação centralizados para
  futura comparação com o sistema não permissionado.
- A Cláudia Bartholomeu está iniciando um trabalho com Smart Grids que deve
  usar o sistema de reputação não permissionado para o comércio de energia em
  pequenas comunidades.

Atualmente há uma disciplina de Sistemas Peer-to-Peer oferecida a cada ano para
alunos de graduação e pós graduação.
Esse semestre é o terceiro ano em que a disciplina é oferecida.

# Local de execução do projeto - (Máximo de 9000 caracteres):

O projeto será executado em dois laboratórios da UERJ, campus Maracanã:

- LCC: Laboratório de alunos de pesquisa do Departamento de Ciência da
       Computação. Possui estações de trabalho.
- LRC: Laboratório de Redes da Pós-Graduação em Engenharia Eletrônica.
       Possui estações de trabalho e infraestrutura de eletrônica.

O projeto não exige uma infraestrutura complexa, mas apenas estações para
desenvolvimento de software, além de um conjunto de máquinas em rede para as
simulações.

# Potenciais veículos de apresentação de resultados - (Máximo de 9000 caracteres):

Journals:

- Peer-to-Peer Networking and Applications
- Ad-Hoc Networks
- ITU Journal on Future and Evolving Technologies
- Elsevier Journal of Network and Computer Applications
- International Journal of Parallel, Emergent and Distributed System
- Distributed Ledger Technologies: Research and Practice

Conferências:

- SBSeg: Simpósio Brasileiro em Segurança da Informação e de Sistemas Computacionais
- SBRC:  Simpósio Brasileiro de Redes de Computadores
- P2PTM: International Conference on Peer-to-Peer Networks and Trust Management 
- DEBS:  International Conference on Distributed and Event‐Based Systems

# Orçamento detalhado e justificado - (Máximo de 9000 caracteres):

# Bibliografia relacionada ao projeto - (Máximo de 9000 caracteres):

Bou Abdo, J., El Sibai, R., and Demerjian, J. (2021).
Permissionless proof-of-reputation-x: A hybrid reputation-based consensus
algorithm for permissionless blockchains.

Transactions on Emerging Telecommunications Technologies, 32(1):e4148.
Creech, B. (2020).
Fake news and the discursive construction of technology companies' social power.
Media, Culture & Society, 42(6):952–968.

Gray, J. N. (1986).
An approach to decentralized computer systems.
IEEE Transactions on Software Engineering, (6):684–692.

Hendrikx, F., Bubendorfer, K., and Chard, R. (2015).
Reputation systems: A survey and taxonomy.
Journal of Parallel and Distributed Computing, 75:184–197.

Rodrigues, B., Franco, M., Killer, C., Scheid, E. J., and Stiller, B. (2022).
On trust, blockchain, and reputation systems.
In Handbook on Blockchain, pages 299–337. Springer.

Sant’Anna, F., Bosisio, F., and Pires, L. (2020).
Freechains: Disseminação de conteúudo peer-to-peer.
Simpóosio Brasileiro em Segurança da Informacão e de Sistemas Computacionais, pages 101–108, Porto Alegre, RS, Bra-
sil. SBC.

Sant’Anna, F., Bosisio, F., and Pires, L. (2023).
Peer-to-Peer Permissionless Consensus via Reputation
Simpóosio Brasileiro em Segurança da Informacão e de Sistemas Computacionais, pages 101–108, Porto Alegre, RS, Bra-
sil. SBC.

Swanson, T. (2015). Consensus-as-a-service: a brief report on the emergence of permissioned, distributed ledger systems.
Report, available online, 28

# Especialidade 1/4 - (Máximo de 45 caracteres):

Redes e Sistemas Distribuídos
Redes e Sistemas Peer-to-Peer
Algoritmos de Consenso Distribuído
Distributed Ledgers Technologies

# Palavra Chave 1/4 - (Máximo de 45 caracteres):

blockchains
proof of authoring
reputation systems
consensus algorithm
