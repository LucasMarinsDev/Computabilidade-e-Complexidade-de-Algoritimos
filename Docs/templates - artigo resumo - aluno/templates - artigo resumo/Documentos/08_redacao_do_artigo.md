# Etapa 8 Redação do artigo

## Solicitação

Escreva a primeira versão completa do artigo seguindo a estrutura abaixo.

# Título

Algoritmo de Dijkstra, otimizações e complexidade computacional: revisão narrativa com foco em roteamento de emergência

## Palavras-chave

Algoritmo de Dijkstra; caminho mínimo; complexidade computacional

## Introdução

O problema do caminho mínimo em grafos ponderados sustenta sistemas de navegação, de logística e de planejamento de rotas. Nele, os vértices representam pontos de interesse e os pesos das arestas representam o custo de se deslocar entre eles, como tempo, distância ou dificuldade do trajeto. O algoritmo apresentado por Dijkstra (1959) tornou-se a referência para esse problema. Desde então, a literatura propôs estruturas de dados mais eficientes (FREDMAN; TARJAN, 1987), pré-processamento por hierarquias de contração (GEISBERGER et al., 2008) e algoritmos alternativos, como o A* (HART; NILSSON; RAPHAEL, 1968), o Bellman-Ford e o Floyd-Warshall (BAST et al., 2016; MADKOUR et al., 2017).

Este artigo trata do desempenho e da complexidade computacional do algoritmo de Dijkstra e de suas variações, tendo como pano de fundo o roteamento de emergência. Em operações de busca e resgate, sobretudo em áreas isoladas, trilhas ou locais de acesso comprometido, a escolha do caminho interfere diretamente no tempo de resposta da equipe. Sob pressão, com pouca visibilidade do terreno e informação incompleta, a rota tende a ser decidida no improviso, o que aumenta o risco e atrasa o resgate. O caminho que parece mais curto nem sempre é o melhor, pois um trecho pode ser mais difícil ou mais lento que uma alternativa. O tema interessa a equipes de busca e resgate, brigadistas, defesa civil e bombeiros e, na academia, à aplicação de algoritmos clássicos de grafos. Esse é o contexto do projeto Atlas Global, desenvolvido pelo grupo com dados da região de Mogi das Cruzes (SP). Este artigo, porém, é uma revisão da literatura e não apresenta resultados experimentais do sistema.

A lacuna que motiva o trabalho é dupla. Há ampla literatura sobre o Dijkstra e suas otimizações, mas ela se apoia em estudos de naturezas muito distintas (provas teóricas, experimentos em redes continentais, experimentos em grafos sintéticos), e não é evidente como comparar seus resultados. Além disso, entre os oito estudos selecionados nesta revisão, nenhum trata diretamente de roteamento de emergência ou de busca e resgate.

Para enfrentar essa lacuna, a revisão busca (i) conceituar o algoritmo de Dijkstra e sua complexidade; (ii) comparar as principais variações e otimizações, quanto a estrutura de dados, busca bidirecional, pré-processamento e adaptação do modelo do grafo; (iii) confrontar o Dijkstra com o A*, o Bellman-Ford e o Floyd-Warshall; e (iv) identificar o que a literatura reunida deixa em aberto para a aplicação em emergências. Assim, o objetivo geral do artigo é analisar, por meio de revisão narrativa da literatura, como o algoritmo de Dijkstra e suas variações e otimizações são tratados em estudos sobre roteamento em grafos de grande escala e quais são suas limitações de desempenho e de complexidade computacional frente ao A*, ao Bellman-Ford e ao Floyd-Warshall, apontando as lacunas para o apoio a operações de busca e resgate e à logística de emergência.

## Metodologia

Trata-se de uma revisão bibliográfica narrativa. Não houve protocolo sistemático registrado e, por isso, o trabalho não se declara revisão sistemática. O plano de busca (termos, strings, bases e critérios) foi definido antes da triagem, com termos em português e em inglês, organizados em seis conceitos: algoritmo de Dijkstra, grafos ponderados, otimização de rotas, complexidade computacional, roteamento de emergência e otimizações do Dijkstra.

Foram elaboradas cinco strings de busca com operadores booleanos. A string 1 combina "Dijkstra" ou "Dijkstra's algorithm" com "shortest path", "shortest-path" ou "minimum path", e foi usada no IEEE Xplore e na ACM Digital Library. A string 2 combina termos de caminho mínimo e otimização de rotas com teoria dos grafos e complexidade computacional, e foi usada no Scopus. A string 3, em português, combina "algoritmo de Dijkstra" ou "caminho mínimo" com termos de otimização de rotas, e foi usada no Portal de Periódicos CAPES. A string 4 combina "Dijkstra" com A*, Bellman-Ford ou Floyd-Warshall e com termos de comparação de desempenho (IEEE Xplore e Scopus). A string 5 combina "Dijkstra" ou "shortest path" com termos de roteamento de emergência e busca e resgate (IEEE Xplore e Scopus). As bases foram escolhidas pela cobertura de computação, algoritmos e roteamento (IEEE Xplore, ACM Digital Library), pela abrangência multidisciplinar (Scopus) e pelo acesso institucional e produção nacional (Portal CAPES).

As oito combinações entre string e base foram executadas entre 17 e 19 de setembro de 2026, sem filtros nas bases, e retornaram 15.889 resultados: 1.622, 10 e 126 no IEEE Xplore (strings 1, 4 e 5); 10.550 na ACM Digital Library (string 1); 3.517, 0 e 41 no Scopus (strings 2, 4 e 5); e 23 no Portal CAPES (string 3). Somados a uma consulta complementar na base MDPI, registrada na etapa de levantamento bibliográfico, o total foi de 15.894 resultados.

Os critérios de inclusão foram: publicação entre 2016 e 2026, com exceção de obras clássicas ou fundamentais (Dijkstra, 1959; Hart, Nilsson e Raphael, 1968; Fredman e Tarjan, 1987; Geisberger et al., 2008); idioma português ou inglês; revisão por pares (periódicos ou anais indexados); texto completo disponível; e aderência direta ao algoritmo de Dijkstra, às suas variações e otimizações ou a comparações de complexidade com outros algoritmos de caminho mínimo. Foram excluídos duplicatas, estudos fora do tema (por exemplo, que citam o Dijkstra apenas de passagem), registros sem texto completo, materiais não revisados por pares (inclusive *preprints* sem publicação posterior) e trabalhos de divulgação sem contribuição técnica clara.

Foram removidas 11 duplicatas, e 31 registros foram avaliados por título e resumo e depois lidos na íntegra.  Por orientação docente, o conjunto final foi limitado a oito estudos, priorizando os de maior aderência à pergunta de pesquisa; os outros 23 foram excluídos. Dois dos oito foram localizados fora das bases planejadas: Tang, Sun e Chen (2016), publicado em anais pela Atlantis Press, e Madkour et al. (2017), disponível no arXiv. Este último é um *preprint*, e sua inclusão contraria o critério de exclusão adotado. Ele foi mantido provisoriamente porque, no conjunto, é a fonte que reúne o Bellman-Ford e o Floyd-Warshall com suas complexidades (Bast et al., 2016, dedicam uma frase a cada um), e suas afirmações são tratadas com cautela e confrontadas com fontes primárias quando possível. 

Os estudos foram lidos na íntegra entre 30 de setembro e 5 de outubro de 2026. Cada um recebeu uma ficha com problema, objetivo, método, resultados, limitações e contribuição para a pergunta de pesquisa. Em seguida, as fichas foram reunidas em uma matriz de síntese organizada em três eixos, que comparou convergências, divergências, limitações e lacunas. A análise é qualitativa e comparativa. Os números citados na revisão são os reportados pelos autores de cada estudo, nas condições de cada experimento, e não resultados produzidos pelo grupo.

## Revisão da literatura

### Eixo 1 — Fundamentos do algoritmo de Dijkstra e sua complexidade

Dijkstra (1959) resolve dois problemas em grafos com ramos de comprimento conhecido: construir a árvore de comprimento total mínimo que liga todos os nós e encontrar o caminho de menor comprimento entre dois nós dados, ambos sob a hipótese de que existe pelo menos um caminho entre quaisquer dois nós. No segundo problema, o procedimento mantém um conjunto de nós cujo caminho mínimo já é conhecido e, a cada passo, examina os ramos que saem do nó recém-incluído e transfere para o conjunto o nó de menor distância provisória, parando ao alcançar o destino. O autor observa que o método vale também quando o comprimento do ramo depende do sentido do percurso, propriedade útil para ruas de mão única, e afirma que o trabalho parece consideravelmente menor que o do método de Ford, sem medi-lo. O texto, porém, não traz limite de complexidade em notação O nem enuncia a exigência de pesos não negativos. Esses elementos vêm da literatura posterior e devem ser atribuídos a ela.

Madkour et al. (2017) descrevem o Dijkstra como algoritmo de origem única para grafos direcionados com pesos não negativos e estáticos, com custo O(n²), sem distinguir a implementação com heap. Bast et al. (2016) apresentam as complexidades com heap: O((|V|+|A|) log |V|) com heap binário e O(|A| + |V| log |V|) com heap de Fibonacci. Fredman e Tarjan (1987) é a fonte primária desse último resultado: o heap de Fibonacci reduz o custo do Dijkstra de origem única a O(n log n + m), melhorando o limite O(m log_(m/n+2) n) então conhecido, e os autores notam que, em um modelo baseado em comparações, esse limite só pode ser superado por outras abordagens.

Os estudos convergem quanto ao papel do Dijkstra e divergem apenas no valor de complexidade citado, que depende da estrutura de dados usada na fila de prioridade (O(n²) com implementação simples; O(n log n + m) com heap de Fibonacci). As limitações aparecem na natureza das fontes: Dijkstra (1959) supõe grafo conexo e compara-se com Ford apenas de forma qualitativa; Fredman e Tarjan (1987) apresentam resultados assintóticos e amortizados, mais claros para grafos de densidade intermediária, sem avaliação empírica; e Madkour et al. (2017) é um *preprint* com imprecisões de redação.

### Eixo 2 — Otimizações e variações do Dijkstra

Os estudos reunidos indicam que o desempenho do Dijkstra em grafos grandes depende de quatro frentes: a estrutura de dados, a direção da busca, o pré-processamento e a adaptação do modelo do grafo. As evidências, no entanto, vêm de escalas muito diferentes e nem sempre confirmam a teoria.

Verma et al. (2021) implementaram quatro abordagens (lista ligada com força bruta, heap de Fibonacci, heap binário e Dijkstra bidirecional) em 18 casos de teste, 9 de grafos densos e 9 de esparsos. O Dijkstra bidirecional foi o mais rápido ou empatou em 16 dos 18 casos, e o heap binário o superou em dois casos esparsos por 1 ms. No caso 15 (1E5 × 10E5), os tempos foram 37.172 ms (força bruta), 94 ms (heap binário), 3 ms (bidirecional) e 7.103 ms (heap de Fibonacci). Nos grafos esparsos, a força bruta ficou à frente do heap de Fibonacci (por exemplo, 16 ms contra 292 ms em 1E4 × 500). Esse resultado contraria a vantagem teórica de Fredman e Tarjan (1987). Os próprios autores não o analisam, e ele pode refletir uma implementação pouco otimizada. O estudo também não descreve a origem dos grafos nem informa repetições, e não esclarece se as variantes unidirecionais param ao alcançar o destino, como o bidirecional faz por natureza.

Em redes viárias continentais, Bast et al. (2016) reúnem, na Tabela 1, resultados na rede da Europa Ocidental, com cerca de 18 milhões de vértices: o Dijkstra processa 9.326.696 vértices em 2.195.080 µs; a busca bidirecional, 4.914.804 vértices em 1.205.660 µs; e as hierarquias de contração, 280 vértices em 110 µs, ao custo de cerca de cinco minutos de pré-processamento. Os tempos vêm de fontes distintas e foram normalizados pelos autores, que concluem que não há melhor técnica em todos os critérios. Geisberger et al. (2008) propõem a contração de nós, que substitui caminhos mínimos que passam por um nó por atalhos e responde às consultas com busca bidirecional restrita. Na mesma rede, as consultas levaram de 154 a 223 µs, cerca de cinco vezes menos que a melhor técnica hierárquica anterior (HNR), com pré-processamento de 545 s a 1.734 s nas configurações da Tabela 1. Os próprios autores indicam que o ganho foi medido contra o HNR e não contra o Dijkstra simples, que o método funciona melhor em redes esparsas e estáticas e que a alteração de poucos pesos, como em caso de congestionamento, ainda precisa ser testada.

Tang, Sun e Chen (2016) adaptam o Dijkstra a uma rede de metrô em que há custos também nos nós (entrada, parada, transferência e saída). Em vez de expandir a rede, deslocam o rótulo do nó para a aresta e declaram complexidade O(m log m), contra O(m + n log n) da versão tradicional com heap de Fibonacci. No experimento com a rede de Pequim (227 estações), a versão nova foi mais lenta: 0,042 s por par origem-destino, contra 0,026 s. Os autores sugerem que o tempo poupado ao não expandir a rede poderia compensar a diferença em outras redes, mas não o medem; além disso, o tempo da versão tradicional exclui a expansão, o que favorece essa linha de base. A rede é pequena e os tempos de transferência e de entrada e saída foram estimados.

Os estudos convergem em que não existe ganho de desempenho "gratuito": a otimização mais forte em redes viárias (contração de nós) exige pré-processamento sobre grafo estático, a bidirecional reduz a busca a cerca de metade dos vértices e as estruturas de dados mais sofisticadas nem sempre vencem na prática. Divergem sobre o que a teoria promete e o que a medição mostra (heap de Fibonacci em Verma et al.; versão de Tang et al., mais lenta que a tradicional).

### Eixo 3 — Dijkstra, A*, Bellman-Ford e Floyd-Warshall

Hart, Nilsson e Raphael (1968) formalizam o A*, que usa a função f = g + h, estimada por ĝ + ĥ, e demonstram que ele encontra o caminho ótimo se a heurística ĥ nunca superestimar o custo real (admissibilidade). Demonstram ainda que, sob a condição de consistência, nós já fechados não precisam ser reabertos e que, entre os algoritmos admissíveis que usam a mesma informação, o A* expande o menor número de nós. Reconhecem, porém, que o custo de calcular ĥ a cada nó não é considerado e pode anular o ganho. O artigo é puramente teórico e não cita Dijkstra; a relação entre os dois é uma leitura posterior, que Bast et al. (2016) formulam ao descrever o A* como um Dijkstra cuja prioridade soma a distância percorrida e um potencial que é limite inferior da distância ao destino.

Madkour et al. (2017) e Bast et al. (2016) reúnem as alternativas. O Bellman-Ford tem custo O(nm) (ou O(|V||A|)), aceita pesos negativos e, segundo Madkour et al., detecta ciclos negativos, mas é mais lento que o Dijkstra. O Floyd-Warshall custa O(n³) em tempo e resolve todos os pares; Madkour et al. observam que repetir o Dijkstra a partir de cada vértice só custa menos que ele em grafos esparsos, e Bast et al. que, em grafos suficientemente densos, o Floyd-Warshall supera as |V| execuções do Dijkstra. Quanto ao A*, Madkour et al. o apresentam como busca informada que pode explorar menos vértices que o Dijkstra, mas que não encontra o caminho mínimo sem uma boa heurística, enquanto Bast et al. observam que, em redes viárias, a distância geográfica como potencial dá ganho pequeno ou nulo.

Há, portanto, convergência quanto às complexidades e ao critério de escolha (tipo de peso, densidade, uma origem ou todos os pares) e uma divergência de ênfase sobre a utilidade prática do A*. As limitações são que Hart et al. não medem desempenho, Bast et al. dedicam uma frase a cada algoritmo clássico e Madkour et al. é um *preprint*.

### Síntese crítica

O Quadro 1 reúne as complexidades de tempo reportadas nas fontes lidas. Ele serve para situar os algoritmos, não para compará-los em condições equivalentes, pois nenhum estudo os mede no mesmo experimento.

**Quadro 1 – Complexidade de tempo reportada para os algoritmos estudados**

| Algoritmo | Complexidade de tempo reportada | Observação | Fonte |
|---|---|---|---|
| Dijkstra (implementação simples) | O(n²) | Origem única; pesos não negativos | Madkour et al. (2017) |
| Dijkstra com heap binário | O((\|V\|+\|A\|) log \|V\|) | Origem única | Bast et al. (2016) |
| Dijkstra com heap de Fibonacci | O(n log n + m) | Origem única; limite amortizado | Fredman e Tarjan (1987); Bast et al. (2016) |
| Bellman-Ford | O(nm) | Aceita pesos negativos | Bast et al. (2016); Madkour et al. (2017) |
| Floyd-Warshall | O(n³) | Todos os pares | Bast et al. (2016); Madkour et al. (2017) |
| A* | Não expressa em notação O nas fontes lidas | Depende da heurística; admissível se ĥ nunca superestima o custo real | Hart, Nilsson e Raphael (1968); Madkour et al. (2017); Bast et al. (2016) |

Fonte: elaborado pelos autores com base nos estudos citados.

Os estudos convergem em tratar o Dijkstra como algoritmo de referência para o caminho de menor custo em grafos ponderados e em mostrar que seu desempenho depende de escolhas de implementação: estrutura de dados, direção da busca e pré-processamento. Divergem sobre o que a otimização entrega. O limite teórico do heap de Fibonacci não se confirma nos testes de Verma et al. (2021), a variante de Tang, Sun e Chen (2016) é mais lenta que a tradicional, e as hierarquias de contração (GEISBERGER et al., 2008; BAST et al., 2016) ganham ordens de grandeza, mas em redes viárias estáticas e com pré-processamento caro. A comparação com o A*, o Bellman-Ford e o Floyd-Warshall se apoia em Hart, Nilsson e Raphael (1968), que é teórico, e em Madkour et al. (2017), que é um *preprint*.

Três lacunas se destacam. A primeira é a aplicação: nenhum dos oito estudos trata de roteamento de emergência ou de busca e resgate. O tema aparece só de modo indireto. Madkour et al. (2017) têm seções sobre grafos dinâmicos, dependentes do tempo e caminhos alternativos que evitam uma aresta. A mudança de pesos durante uma operação, como em bloqueios e deslizamentos, é citada por Geisberger et al. (2008) como possibilidade ainda não testada e tratada por Bast et al. (2016) como tema em aberto. A segunda é a comparabilidade: as escalas variam de 227 estações (TANG; SUN; CHEN, 2016) a cerca de 18 milhões de vértices (GEISBERGER et al., 2008; BAST et al., 2016), e nenhum estudo compara Dijkstra, A*, Bellman-Ford e Floyd-Warshall em um mesmo experimento; Verma et al. (2021) comparam apenas variantes do Dijkstra. A terceira é a cobertura do Floyd-Warshall, que depende de uma única fonte com pendência de elegibilidade.

## Considerações finais

A pergunta que orientou o trabalho era como o Dijkstra e suas variações podem apoiar sistemas de recomendação de rotas em grafos de grande escala para busca e resgate e logística de emergência, e quais são suas limitações frente ao A*, ao Bellman-Ford e ao Floyd-Warshall. Pela literatura reunida, o Dijkstra continua sendo a base adequada para o caminho de menor custo com pesos não negativos e admite pesos que dependem do sentido do percurso, o que atende ruas de mão única. Seu desempenho varia com a implementação, de O(n²) a O(n log n + m), e pode ser melhorado por busca bidirecional, por pré-processamento e por adaptações do modelo do grafo, cada qual com custo e escopo próprios. Suas limitações são a restrição a pesos não negativos, o escopo de origem única e a hipótese de grafo estático. Frente às alternativas, o Bellman-Ford é indicado quando há pesos negativos, o Floyd-Warshall quando se precisam de todos os pares em grafos densos, e o A* quando se dispõe de uma heurística que seja limite inferior do custo real.

O principal achado é negativo: a literatura reunida não avalia essas técnicas em roteamento de emergência. Por isso, a resposta ao problema é parcial. Ela descreve o que se sabe sobre desempenho e complexidade, mas não permite afirmar qual técnica é melhor para busca e resgate. Uma hipótese do grupo, a validar, é que, em um grafo pequeno como o de Mogi das Cruzes, o pré-processamento das hierarquias de contração provavelmente não compense, e uma implementação com heap binário, eventualmente bidirecional, seja suficiente. Isso decorre da leitura de Geisberger et al. (2008), Bast et al. (2016) e Verma et al. (2021), que testam grafos de escala muito diferente, e não foi medido.

As limitações do trabalho são: revisão narrativa, sem protocolo sistemático; apenas oito estudos, com quatro anteriores a 2016 por serem obras clássicas; um *preprint* mantido em caráter provisório; dois estudos localizados fora das bases planejadas; fichamento feito por um leitor por artigo; e resultados de terceiros obtidos em máquinas, redes e condições distintas. Como implicações futuras, cabe testar, com os dados do Atlas Global, a mudança de pesos durante a operação (bloqueios e deslizamentos); avaliar o A* com uma heurística que seja de fato limite inferior do custo adotado (se o peso for tempo, a heurística precisaria subestimar o tempo real de deslocamento); e comparar, em um mesmo experimento e em um grafo do porte de uma cidade, o Dijkstra com heap binário, o bidirecional e as demais alternativas.

## Resumo

O problema do caminho mínimo em grafos ponderados sustenta sistemas de navegação e de logística, e o algoritmo de Dijkstra é sua referência, mas não é claro como suas variações e otimizações se comportam quando aplicadas ao roteamento de emergência, em que a escolha da rota afeta o tempo de resposta de buscas e resgates. O objetivo deste artigo é analisar, por revisão narrativa da literatura, como o Dijkstra e suas variações e otimizações são tratados em estudos de roteamento em grafos de grande escala e quais são suas limitações de desempenho e de complexidade computacional frente ao A*, ao Bellman-Ford e ao Floyd-Warshall. A busca, planejada em português e inglês, foi feita em setembro de 2026 no IEEE Xplore, na ACM Digital Library, no Scopus e no Portal de Periódicos CAPES, com critérios de inclusão e exclusão definidos previamente, e resultou em oito estudos lidos na íntegra e comparados em três eixos. Os estudos convergem em que o desempenho do Dijkstra depende da estrutura de dados, da direção da busca e do pré-processamento, mas divergem sobre o ganho real: o limite teórico do heap de Fibonacci não se confirmou em testes empíricos, e as hierarquias de contração ganham ordens de grandeza apenas em redes viárias estáticas e com pré-processamento caro. Nenhum estudo trata de roteamento de emergência nem compara os quatro algoritmos em um mesmo experimento. Conclui-se que o Dijkstra permanece a base adequada para pesos não negativos, que suas otimizações têm custo e escopo próprios, e que a aplicação em busca e resgate, sobretudo com mudança de pesos durante a operação, é uma lacuna a investigar.

## Referências

BAST, H. et al. Route planning in transportation networks. In: *Algorithm Engineering*. Cham: Springer, 2016. p. 19-80. (Lecture Notes in Computer Science, v. 9220). Disponível em: https://dl.acm.org/doi/10.1145/3274895.3282802.

DIJKSTRA, E. W. A note on two problems in connexion with graphs. *Numerische Mathematik*, v. 1, n. 1, p. 269-271, 1959. DOI: 10.1007/BF01386390.

FREDMAN, M. L.; TARJAN, R. E. Fibonacci heaps and their uses in improved network optimization algorithms. *Journal of the ACM*, v. 34, n. 3, p. 596-615, jul. 1987. DOI: 10.1145/28869.28874.

GEISBERGER, R. et al. Contraction hierarchies: faster and simpler hierarchical routing in road networks. In: McGEOCH, C. C. (ed.). *Experimental Algorithms: WEA 2008*. Berlin: Springer, 2008. p. 319-333. (Lecture Notes in Computer Science, v. 5038). Disponível em: https://dl.acm.org/doi/10.5555/1788888.1788912.

HART, P. E.; NILSSON, N. J.; RAPHAEL, B. A formal basis for the heuristic determination of minimum cost paths. *IEEE Transactions on Systems Science and Cybernetics*, v. SSC-4, n. 2, p. 100-107, jul. 1968. Disponível em: https://ieeexplore.ieee.org/document/4082128.

MADKOUR, A. et al. A survey of shortest-path algorithms. *arXiv*, 1705.02044 [cs.DS], 4 maio 2017. Disponível em: https://arxiv.org/abs/1705.02044.

TANG, J.; SUN, Q.; CHEN, Z. A new implementation of Dijkstra's algorithm on urban rail transit network. In: INTERNATIONAL CONFERENCE ON CIVIL, TRANSPORTATION AND ENVIRONMENT (ICCTE 2016), 2016. *Proceedings* [...]. Atlantis Press, 2016. p. 507-513. DOI: 10.2991/iccte-16.2016.85.

VERMA, D. et al. Comparative study of various approaches of Dijkstra algorithm. In: INTERNATIONAL CONFERENCE ON COMPUTING, COMMUNICATION, AND INTELLIGENT SYSTEMS (ICCCIS), 2021. *Proceedings* [...]. IEEE, 2021. p. 328-336. Disponível em: https://ieeexplore.ieee.org/document/9397200.

## Checklist

- [x] A introdução termina com o objetivo.
- [x] A metodologia descreve o processo realmente realizado. 
- [x] A revisão compara os artigos.
- [x] A conclusão responde ao problema. 
- [x] O resumo representa o texto completo.
