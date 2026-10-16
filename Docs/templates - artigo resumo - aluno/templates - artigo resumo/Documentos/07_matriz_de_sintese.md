# Etapa 7 Matriz de síntese e organização da revisão

## Solicitação

Compare os artigos e organize a revisão por temas ou eixos. Não produza apenas uma sequência de resumos.

## Eixos da revisão

1. Fundamentos do algoritmo de Dijkstra e sua complexidade
2. Otimizações e variações do Dijkstra: estruturas de dados, busca bidirecional, pré-processamento e adaptação do modelo do grafo
3. Comparação do Dijkstra com A*, Bellman-Ford e Floyd-Warshall

> Referência: os eixos seguem os assuntos da etapa c (grafos ponderados; Dijkstra e suas variações/otimizações; comparação com A*, Bellman-Ford e Floyd-Warshall) e a síntese final da etapa 6. A aplicação em roteamento de emergência não virou eixo porque nenhum dos 8 artigos a trata diretamente; aparece como lacuna na síntese crítica. Os eixos devem ser confirmados pelo grupo.

## Matriz de síntese

| Eixo | Artigos relacionados | Convergências | Divergências | Limitações | Lacunas |
|---|---|---|---|---|---|
| 1. Fundamentos do Dijkstra e sua complexidade | DIJKSTRA (1959); FREDMAN; TARJAN (1987); BAST et al. (2016); MADKOUR et al. (2017, elegibilidade pendente) | Madkour (p. 5) descreve o Dijkstra como algoritmo de origem única para grafos com pesos não negativos e estáticos. Bast (p. 4) e Fredman e Tarjan (p. 610) dão a complexidade com heaps: O((\|V\|+\|A\|) log \|V\|) com heap binário e O(n log n + m) com heap de Fibonacci | O artigo original não traz limite de complexidade em notação O nem enuncia pesos não negativos; isso vem da literatura posterior. A complexidade varia com a implementação: O(n²) em Madkour, O(n log n + m) em Fredman e Tarjan | Dijkstra (1959): supõe grafo conexo e compara com o método de Ford só de forma qualitativa. Madkour: preprint, com imprecisões de redação (ex.: repete O(n²) sem distinguir o heap). Fredman e Tarjan: resultados assintóticos, sem avaliação empírica | Nenhum desses textos trata de roteamento de emergência. Ao citar complexidade e pesos não negativos, é preciso atribuir à fonte correta, e não ao artigo de 1959 |
| 2. Otimizações e variações do Dijkstra | FREDMAN; TARJAN (1987); VERMA et al. (2021); GEISBERGER et al. (2008); TANG; SUN; CHEN (2016); BAST et al. (2016); MADKOUR et al. (2017) | O desempenho do Dijkstra depende de estrutura de dados, direção da busca e pré-processamento. Verma: o bidirecional foi o mais rápido ou empatou em 16 de 18 casos. Bast (Tabela 1): Dijkstra 2.195.080 µs, bidirecional 1.205.660 µs e CH 110 µs, na rede da Europa Ocidental. Geisberger: consultas cerca de 5 vezes mais rápidas que o HNR | O F-heap é o melhor em teoria (Fredman e Tarjan), mas em Verma fica muito atrás do heap binário (7.103 ms contra 94 ms no caso 15) e, em grafos esparsos, atrás da força bruta (292 ms contra 16 ms). A versão de Tang é mais lenta que a tradicional (0,042 s contra 0,026 s por par) | Geisberger: pré-processamento caro (545 s a 1.734 s), ganho medido contra o HNR e não contra o Dijkstra simples, e atualização de poucos pesos ainda por testar. Tang: rede pequena (227 estações), tempos estimados e baseline sem custo de expansão. Verma: sem repetições, grafos pouco descritos, F-heap possivelmente mal otimizado | Escalas muito diferentes entre os estudos (18 milhões de nós em Geisberger e Bast; 227 estações em Tang), sem comparação direta entre as técnicas. Ninguém testa as otimizações em roteamento de emergência. Para um grafo pequeno como o de Mogi das Cruzes, o pré-processamento provavelmente não compensa (inferência do grupo, a validar) |
| 3. Comparação com A*, Bellman-Ford e Floyd-Warshall | HART; NILSSON; RAPHAEL (1968); BAST et al. (2016); MADKOUR et al. (2017, elegibilidade pendente); VERMA et al. (2021, só variantes do Dijkstra) | A* é admissível se a heurística nunca superestima o custo real (Hart, p. 103) e pode explorar menos vértices (Madkour, p. 10). Bellman-Ford: O(nm), aceita pesos negativos (Bast e Madkour). Floyd-Warshall: O(n³) (Bast e Madkour) e só é superado por Dijkstra repetido em grafos esparsos (Madkour, p. 6) | Hart não cita Dijkstra; a relação "Dijkstra = A* com ĥ = 0" é leitura posterior, apoiada em Bast (p. 5). Madkour apresenta o A* como mais rápido, enquanto Bast observa ganho pequeno ou inexistente com distância geográfica em redes viárias | Hart é puramente teórico, sem desempenho medido, e não considera o custo de calcular ĥ. Bast trata Bellman-Ford e Floyd-Warshall em uma frase cada. Madkour é preprint | Nenhum artigo compara os quatro algoritmos em um mesmo experimento. Verma compara só variantes do Dijkstra. A cobertura de Floyd-Warshall depende de Madkour, cuja elegibilidade está pendente |

**Lacuna transversal (aplicação em emergência):** nenhum dos 8 artigos trata de roteamento de emergência ou de busca e resgate. O tema aparece só de forma indireta: seções de Madkour sobre grafos dinâmicos (p. 14–16), dependentes do tempo (p. 16–17) e caminhos alternativos que evitam uma aresta (p. 19); Geisberger, que cita a mudança de alguns pesos como possibilidade ainda não testada (p. 325, 332); e Bast (p. 24–25), que trata a dinâmica como tema em aberto.

## Roteiro da revisão da literatura

### Eixo 1

- Ideia principal: o algoritmo de Dijkstra é a base do caminho de menor custo em grafos ponderados, e sua complexidade depende da implementação.
- Evidências que serão usadas: procedimento do Problema 2, com parada ao alcançar o destino e comprimentos que podem depender do sentido (Dijkstra, p. 270); descrição como algoritmo de origem única para pesos não negativos e O(n²) (Madkour, p. 5); O(n log n + m) com F-heap (Fredman e Tarjan, p. 610); O((|V|+|A|) log |V|) com heap binário (Bast, p. 4).
- Comparação entre estudos: o artigo original apresenta o método sem analisar a complexidade, e os textos posteriores acrescentam a análise e a condição de pesos não negativos. Cada afirmação deve ser atribuída à sua fonte.
- Ligação com o problema: sustenta o objetivo de conceituar o Dijkstra e a parte da pergunta sobre complexidade computacional. A característica de permitir pesos por sentido é útil para ruas de mão única no Atlas Global.

### Eixo 2

- Ideia principal: o desempenho do Dijkstra em grafos grandes melhora com estruturas de dados, busca bidirecional, pré-processamento e adaptação do modelo, mas cada técnica tem custo e escopo próprios, e o limite teórico nem sempre se confirma na prática.
- Evidências que serão usadas: Fredman e Tarjan (limite teórico); Verma (18 casos, Tabelas I a III); Bast (Tabela 1, p. 23); Geisberger (Tabela 1, p. 328, e limitações da p. 325 a 332); Tang (O(m log m) e 0,042 s contra 0,026 s, p. 511–512).
- Comparação entre estudos: o ganho teórico do F-heap contrasta com seu desempenho em Verma. O bidirecional aparece como vencedor prático em Verma e como redução de cerca de metade dos vértices em Bast. A contração de nós dá o maior ganho em redes viárias, ao custo de pré-processamento sobre grafo estático. A variante de Tang é mais lenta, mas dispensa expandir a rede.
- Ligação com o problema: responde à parte da pergunta sobre variações, otimizações e limitações de desempenho em grafos de grande escala.

### Eixo 3

- Ideia principal: A*, Bellman-Ford e Floyd-Warshall resolvem variantes do problema com compromissos diferentes de heurística, tipo de peso e escopo (uma origem ou todos os pares).
- Evidências que serão usadas: admissibilidade e otimalidade do A* (Hart, p. 103–106); descrição do A* e de suas limitações (Madkour, p. 10; Bast, p. 5); complexidades do Bellman-Ford e do Floyd-Warshall (Bast, p. 4; Madkour, p. 5–6).
- Comparação entre estudos: Hart dá a base teórica do A*, Madkour reúne as complexidades das alternativas, e Bast mostra que, em redes viárias, a heurística geográfica traz pouco ganho.
- Ligação com o problema: responde à parte da pergunta sobre a comparação com A*, Bellman-Ford e Floyd-Warshall. Para usar o A* no Atlas Global, seria preciso uma heurística que seja limite inferior do custo real.

## Síntese crítica provisória

Os artigos selecionados convergem em tratar o Dijkstra como algoritmo de referência para caminho de menor custo em grafos ponderados e em mostrar que seu desempenho depende de escolhas de implementação: estrutura de dados, direção da busca e pré-processamento. Divergem sobre o que a otimização entrega: o limite teórico do heap de Fibonacci não se confirma nos testes de Verma, a variante de Tang é mais lenta que a tradicional, e as hierarquias de contração (Geisberger; Bast) ganham ordens de grandeza, mas em redes viárias estáticas e com pré-processamento caro. A comparação com A*, Bellman-Ford e Floyd-Warshall se apoia em Hart (teórico) e em Madkour (preprint), e nenhum artigo compara os quatro em um mesmo experimento. A principal lacuna é a aplicação: nenhum dos 8 artigos trata de roteamento de emergência, e a mudança de pesos durante uma operação, como bloqueios, aparece só como tema em aberto. Para a síntese final, o grupo precisa decidir se mantém Madkour, porque dele dependem a cobertura de Floyd-Warshall e parte da comparação.

## Checklist

- [ ] Os artigos foram agrupados por ideias.
- [ ] Há comparações entre estudos.
- [ ] As divergências foram registradas.
- [ ] As lacunas são específicas e sustentadas pelas leituras.
