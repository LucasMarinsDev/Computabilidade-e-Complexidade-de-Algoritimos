# Etapa 6 Leitura e fichamento — Grupo 10 (Atlas Global)

---

## Ficha 1 — DIJKSTRA (1959)

### Identificação do artigo
- Referência completa: DIJKSTRA, E. W. A note on two problems in connexion with graphs. *Numerische Mathematik*, v. 1, p. 269–271, 1959. (Recebido em 11/06/1959; Fredman e Tarjan citam como n. 4, set. 1959.)
- DOI ou URL: https://dl.acm.org/doi/10.1007/BF01386390
- Base de origem: ACM Digital Library 
- Leitor responsável: `[ Vinicius da Silva ]`
- Data da leitura: `[02/10/2026]`

### Fichamento

**Problema investigado:** Dois problemas em grafos com ramos de comprimento conhecido, restritos ao caso em que existe ao menos um caminho entre quaisquer dois nós: (1) construir a árvore de comprimento total mínimo que liga os n nós; (2) achar o caminho de comprimento total mínimo entre dois nós dados, P e Q (p. 269–270).

**Objetivo do estudo:** Apresentar um método para cada problema que dispense ordenar todos os ramos e guardar todos os dados ao mesmo tempo, como exigem as soluções de Kruskal e de Loberman e Weinberger (Problema 1) e a de Ford, descrita por Berge (Problema 2) (p. 269–271).

**Método utilizado:** Procedimento iterativo com conjuntos de nós e de ramos. No Problema 2: todos os nós começam no conjunto C e P passa para A (nós com caminho mínimo já conhecido). A cada passo (Passo 1) examinam-se os ramos que saem do nó recém-transferido; um ramo substitui o anterior se der um caminho mais curto até R. No Passo 2 o nó de menor distância em B passa para A. Repete-se até Q entrar em A (p. 270). Os caminhos mínimos saem "em ordem crescente de comprimento", e o processo para ao alcançar Q.

**Contexto, amostra ou dados:** Trabalho teórico de três páginas, sem dados nem experimentos.

**Principais resultados:** (i) O algoritmo para o Problema 2 funciona também quando o comprimento do ramo depende do sentido de percurso (Observação 1, p. 270). (ii) Só é preciso guardar os dados de, no máximo, n ramos (conjuntos I e II mais o ramo em exame), e "a quantidade de trabalho parece consideravelmente menor" que no método de Ford (p. 271). O artigo **não** apresenta limite de complexidade em notação O nem enuncia explicitamente a exigência de pesos não negativos.

**Limitações apresentadas:** Nenhuma discutida pelo autor. A hipótese de grafo conexo é declarada como restrição (p. 269).

**Contribuição para o nosso artigo:** Fonte primária para o objetivo específico 2 (conceituar o algoritmo de Dijkstra). Mostra também duas características úteis ao Atlas Global: parada ao alcançar o destino e aplicabilidade a pesos direcionais (ruas de mão única ou custos diferentes por sentido).

**Comentário crítico:** A complexidade O(n²), o uso de heaps e a condição de pesos não negativos **não estão** no original: vêm da literatura posterior (Madkour et al., p. 5; Fredman e Tarjan, p. 610). Ao citar esses pontos, atribuir à fonte correta. A comparação com Ford é qualitativa ("parece"), sem medição.

**Citação literal:**
> "in order of increasing length until Q is reached"

Página: 270

### Checklist
- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

## Ficha 2 — HART; NILSSON; RAPHAEL (1968)

### Identificação do artigo
- Referência completa: HART, P. E.; NILSSON, N. J.; RAPHAEL, B. A formal basis for the heuristic determination of minimum cost paths. *IEEE Transactions on Systems Science and Cybernetics*, v. SSC-4, n. 2, p. 100–107, jul. 1968. (Manuscrito recebido em 24/11/1967.)
- DOI ou URL: https://ieeexplore.ieee.org/document/4082128
- Base de origem: IEEE Xplore
- Leitor responsável: `[ Vinicius da Silva ]`
- Data da leitura: `[02/10/2026]`

### Fichamento

**Problema investigado:** Não havia teoria que orientasse a busca eficiente de caminhos de custo mínimo, nem um quadro conceitual para comparar as estratégias heurísticas ad hoc. A abordagem matemática garante o ótimo, mas ignora a viabilidade computacional; a heurística ganha eficiência, mas em geral não garante o caminho mínimo (resumo e p. 100–101).

**Objetivo do estudo:** Incorporar informação heurística do domínio do problema a uma teoria matemática de busca em grafos e demonstrar uma propriedade de otimalidade de uma classe de estratégias de busca (resumo, p. 100).

**Método utilizado:** Formalização com grafos cujos arcos têm custo ≥ δ > 0 ("δ graphs") e geração implícita pelo operador sucessor Γ (p. 101). Define-se f(n) = g(n) + h(n), estimada por f̂(n) = ĝ(n) + ĥ(n) (eq. 1–2, p. 102), e o **algoritmo A\*** em quatro passos (p. 102). Provam-se o Lema 1 e o Teorema 1 (admissibilidade se ĥ ≤ h, p. 103), a hipótese de consistência (desigualdade triangular, eq. 4–5, p. 104), os Lemas 2 e 3 e os Teoremas 2 e 3 (otimalidade em número de nós expandidos, p. 105–106).

**Contexto, amostra ou dados:** Teórico, com exemplos ilustrativos de cidades ligadas por estradas, usando a distância em linha reta como ĥ (p. 101, 104). Sem experimentos.

**Principais resultados:** (i) Se ĥ nunca superestima h, A\* é admissível, isto é, encontra caminho ótimo (Teorema 1, p. 103). (ii) Sob consistência, nós fechados não precisam ser reabertos (Lema 2, p. 104). (iii) Entre os algoritmos admissíveis que usam no máximo a mesma informação, A\* expande o menor número de nós (Teoremas 2–3, p. 105–106). (iv) Com ĥ = 0 não se usa informação do problema; com custos unitários, esse caso equivale aos algoritmos de Moore e de Busacker e Saaty (p. 106). (v) Escolher ĥ maior que o limite admissível reduz a expansão, mas perde a garantia de ótimo (p. 107).

**Limitações apresentadas:** O custo de calcular ĥ a cada nó não é considerado e pode anular o ganho (p. 107). A consistência pode ser violada por regras de cálculo de ĥ que dependam de parâmetros variáveis entre nós (p. 104). A otimalidade é relativa a algoritmos com a mesma informação, e empates críticos podem afetar o resultado (p. 106). O artigo assume arcos com custo mínimo δ > 0.

**Contribuição para o nosso artigo:** Base teórica da comparação Dijkstra × A\* pedida na pergunta de pesquisa (objetivo específico 5). A condição de admissibilidade mostra o que seria necessário para usar A\* no Atlas Global: uma heurística que seja limite inferior do custo real (ex.: distância geográfica, se o peso for distância).

**Comentário crítico:** O artigo **não cita Dijkstra** (a lista de referências, p. 107, traz Pollack e Wiebenson, Busacker e Saaty, Moore e outros). A relação "Dijkstra = A\* com ĥ = 0" é uma leitura posterior: no texto, ĥ = 0 dá f = ĝ, algoritmo atribuído a Minty (p. 106). Para citar essa equivalência, apoiar-se em Bast et al. (p. 5), que descreve A\* como Dijkstra com prioridade dist(s,u) + π(u). Resultado puramente teórico: sem evidência de desempenho em redes reais.

**Citação literal:**
> "If ĥ(n) ≤ h(n) for all n, then A\* is admissible."

Página: 103

### Checklist
- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

## Ficha 3 — FREDMAN; TARJAN (1987)

### Identificação do artigo
- Referência completa: FREDMAN, M. L.; TARJAN, R. E. Fibonacci heaps and their uses in improved network optimization algorithms. *Journal of the ACM*, v. 34, n. 3, p. 596–615, jul. 1987.
- DOI ou URL: https://dl.acm.org/doi/10.1145/28869.28874
- Base de origem: ACM Digital Library
- Leitor responsável: `[Murilo Santiago]`
- Data da leitura: `[30/09/2026]`

### Fichamento

**Problema investigado:** O custo das operações da fila de prioridade (heap) limita o desempenho de vários algoritmos de otimização em redes, entre eles o de Dijkstra (p. 596–598).

**Objetivo do estudo:** Desenvolver uma estrutura de dados para heaps, o *Fibonacci heap* (F-heap), e usá-la para obter limites melhores em problemas de rede (p. 596). O objetivo original era acelerar o algoritmo de Dijkstra (p. 597–598).

**Método utilizado:** Extensão das filas binomiais com árvores ordenadas, fusão preguiçosa, "cortes em cascata" e análise amortizada pelo método do potencial (seção 2, p. 598–604). Prova-se que um nó de posto k tem ao menos F(k+2) ≥ φ^k descendentes (Corolário 1, p. 604), origem do nome. Depois, o F-heap é aplicado ao Dijkstra (seção 4, p. 609–611) e à árvore geradora mínima (seção 5, p. 611–613).

**Contexto, amostra ou dados:** Análise teórica de algoritmos, em grafos com n vértices e m arestas. Sem experimentos.

**Principais resultados:** F-heaps executam *delete min* e *delete* em O(log n) amortizado e as demais operações, inclusive *decrease key*, em O(1) amortizado (Teorema 1, p. 604). Dijkstra de origem única com pesos não negativos roda em **O(n log n + m)**, melhorando o O(m log_(m/n+2) n) de Johnson (p. 596, 610). Também melhoram: caminhos mínimos entre todos os pares, O(n² log n + nm); problema de atribuição; e árvore geradora mínima, O(m β(m,n)) (p. 596).

**Limitações apresentadas:** As melhorias são assintóticas, mais claras para grafos de densidade intermediária (n ≪ m ≪ n²) (p. 598). Os limites das operações são amortizados (a execução total é limitada, não cada operação). *Decrease key* e *delete* pressupõem que a posição do item no heap é conhecida (p. 597). Em um modelo baseado em comparações, Dijkstra exige Ω(n log n + m), então esse limite só pode ser superado por outras abordagens (p. 613).

**Contribuição para o nosso artigo:** Principal referência da complexidade teórica "ótima" do Dijkstra (objetivo específico 5). Sustenta a comparação entre as implementações com lista, heap binário e heap de Fibonacci.

**Comentário crítico:** Não há avaliação empírica nem discussão de constantes. Verma et al. (2021) mostram que, na prática, o F-heap pode ser muito mais lento que o heap binário (centenas de vezes, em alguns casos da Tabela I, p. 334), o que ilustra a diferença entre limite assintótico e desempenho real. A versão original de 1984 foi publicada no FOCS, e o PDF informa isso na primeira página.

**Citação literal:**
> "we obtain an O(n log n + m) running time for Dijkstra's algorithm"

Página: 610

### Checklist
- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

## Ficha 4 — GEISBERGER et al. (2008)

### Identificação do artigo
- Referência completa: GEISBERGER, R.; SANDERS, P.; SCHULTES, D.; DELLING, D. Contraction hierarchies: faster and simpler hierarchical routing in road networks. In: McGEOCH, C. C. (Ed.). *Experimental Algorithms (WEA 2008)*. Lecture Notes in Computer Science, v. 5038. Berlin: Springer, 2008. p. 319–333.
- DOI ou URL: não consta no PDF. https://dl.acm.org/doi/10.5555/1788888.1788912
- Base de origem: ACM Digital Library
- Leitor responsável: `[Murilo Santiago]`
- Data da leitura: `[30/09/2026]`

### Fichamento

**Problema investigado:** Planejar rotas ótimas em redes viárias de escala continental, em que o Dijkstra puro é lento demais para consultas interativas (p. 319).

**Objetivo do estudo:** Propor uma técnica de roteamento hierárquico baseada só no conceito de **contração de nós**, mais simples e rápida que as anteriores (p. 319–320).

**Método utilizado:** (1) Ordenar os nós por "importância" com heurísticas locais (diferença de arestas, vizinhos já removidos, regiões de Voronoi, entre outras) em uma fila de prioridade (seção 3, p. 322–324). (2) Contrair os nós nessa ordem, substituindo caminhos mínimos que passam pelo nó v por **atalhos**, quando o atalho é necessário (seção 2, p. 321–322). (3) Responder consultas com busca bidirecional de Dijkstra: a busca direta só segue arestas para nós mais importantes (grafo G↑) e a reversa só vem de nós mais importantes (G↓), com a técnica *stall-on-demand* (seção 4, p. 324–325).

**Contexto, amostra ou dados:** Rede viária da Europa Ocidental (PTV AG) com 18.029.721 nós e 42.199.587 arestas direcionadas, 13 categorias de via e tempo de viagem como peso. Uma CPU AMD Opteron 270 de 2,0 GHz, 8 GB, C++ (p. 327).

**Principais resultados:** Consultas cerca de 5 vezes mais rápidas que a melhor técnica hierárquica anterior (HNR) e "sobrecarga de espaço negativa" (resumo, p. 319). Na Tabela 1 (p. 328): variante econômica (EDS1235), consulta de 223 µs com 459 nós processados; variante agressiva (EVSQWL), 154 µs com 359 nós, contra 802 µs e 957 nós do HNR. Trocar toda a função de peso (ex.: carro rápido para caminhão lento) reaproveita a ordem dos nós e aumenta em cerca de 30% o tempo de construção (p. 331).

**Limitações apresentadas:** O ganho de espaço só vale sem desempacotar atalhos para recuperar o caminho: com desempacotamento, a sobrecarga é de 5,8 (agressiva) a 10,8 B/nó (econômica) (p. 325, 330). A ordenação de nós é cara (de 545 s a 1.734 s na Tabela 1). Funciona melhor em redes esparsas com alta localidade; em redes mais densas, recomenda-se contração parcial combinada com busca direcionada (p. 331–332). **Alterar só alguns pesos** (ex.: congestionamento) é citado como possibilidade herdada do HNR, mas "ainda precisa ser testado" (p. 325, 332).

**Contribuição para o nosso artigo:** Exemplo central de **otimização do Dijkstra para grafos de grande escala** (pergunta de pesquisa). Mostra o custo da otimização: pré-processamento sobre grafo estático.

**Comentário crítico:** A conexão com emergência é indireta, mas relevante: em busca e resgate as condições mudam (bloqueios, deslizamentos), e o próprio artigo indica que atualizações pontuais de peso não foram avaliadas. Os ganhos são medidos contra o HNR, não contra o Dijkstra simples; para a comparação com o baseline, usar Bast et al., Tabela 1 (p. 23: Dijkstra 2.195.080 µs; CH 110 µs, implementação posterior). Resultados de outros grafos de teste ficam no relatório completo, que o artigo não traz (p. 327). Para o grafo pequeno de Mogi das Cruzes, o pré-processamento provavelmente não compensa (inferência do grupo, a validar).

**Citação literal:**
> "Contracting a node v means replacing shortest paths going through v by shortcuts."

Página: 319

### Checklist
- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

## Ficha 5 — BAST et al. (2016)

### Identificação do artigo
- Referência completa: BAST, H.; DELLING, D.; GOLDBERG, A.; MÜLLER-HANNEMANN, M.; PAJOR, T.; SANDERS, P.; WAGNER, D.; WERNECK, R. F. Route planning in transportation networks. In: *Algorithm Engineering*. Lecture Notes in Computer Science, v. 9220. Springer, 2016. p. 19–80. (Referência da etapa 5.)
- DOI ou URL:https://dl.acm.org/doi/10.1145/3274895.3282802
- Base de origem: ACM Digital Library
- Leitor responsável: `[Gabriel Nascimento de Souza]`
- Data da leitura: `[03/10/2026]`

### Fichamento

**Problema investigado:** Calcular rotas rapidamente em redes de transporte: rodoviárias (estáticas, com tráfego em tempo real), de transporte público (dependentes do tempo e multicritério) e multimodais (p. 1–3).

**Objetivo do estudo:** Apresentar o estado da arte dos algoritmos práticos de roteamento e comparar seus compromissos entre pré-processamento, espaço e tempo de consulta (p. 2).

**Método utilizado:** Revisão da literatura. A Seção 2 descreve técnicas para caminho mínimo em grafos estáticos: Dijkstra, busca bidirecional, Bellman-Ford, Floyd-Warshall, A\*/ALT, *arc flags*, hierarquias de contração, entre outras. A Seção 3 reúne resultados experimentais publicados, em parte reexecutados em máquina de referência (Intel X5680, 3,33 GHz), e escala os demais (p. 3–6, 20–24).

**Contexto, amostra ou dados:** Rede viária da Europa Ocidental (PTV AG), 18,0 milhões de vértices e 42,5 milhões de arcos direcionados, com 13 categorias de via (p. 21).

**Principais resultados:**
- Dijkstra roda em O((|V|+|A|) log |V|) com heap binário e O(|A| + |V| log |V|) com heap de Fibonacci (p. 4).
- A busca bidirecional visita aproximadamente metade dos vértices em redes viárias (p. 4).
- Bellman-Ford é O(|V||A|) no pior caso, corrige rótulos e aceita pesos negativos (p. 4).
- Floyd-Warshall é Θ(|V|³) e supera |V| execuções de Dijkstra em grafos suficientemente densos (p. 4).
- A\* usa uma função potencial que é limite inferior da distância ao destino. Em redes viárias, a distância geográfica dá ganho pequeno ou inexistente (p. 5).
- Tabela 1 (p. 23): Dijkstra processa 9.326.696 vértices em 2.195.080 µs; bidirecional, 4.914.804 vértices e 1.205.660 µs; CH, 280 vértices e 110 µs com 5 min de pré-processamento. Os autores concluem que "não há melhor técnica" (p. 23).
- Algoritmos modernos chegam a ser até sete ordens de grandeza mais rápidos que as soluções padrão (p. 45).

**Limitações apresentadas:** As técnicas rápidas exploram propriedades das redes viárias (hierarquia, separadores, direção ao destino) e exigem pré-processamento (p. 3, 45). O desempenho do CH piora sob restrições realistas, como custos de conversão (p. 24; p. 45). Um planejador multimodal mundial com tráfego em tempo real e personalização "parece além do alcance" dos algoritmos atuais (p. 46).

**Contribuição para o nosso artigo:** Fonte mais completa do conjunto para a pergunta de pesquisa: reúne em um só texto a complexidade do Dijkstra, as variações (bidirecional, A\*, hierarquias) e a comparação com Bellman-Ford e Floyd-Warshall (objetivo específico 5). A Tabela 1 fornece números para comparar Dijkstra com suas otimizações.

**Comentário crítico:** Trata Bellman-Ford e Floyd-Warshall em uma frase cada, então a comparação detalhada precisa de outra fonte. Não há menção a emergência, busca e resgate nem a ambulâncias (busca textual no PDF). A ênfase é em redes continentais; o grafo do Atlas Global é muito menor, e a análise de custo-benefício das otimizações para esse porte é inferência do grupo, a validar. Os tempos de fontes diferentes foram normalizados por fatores de escala (p. 22–23).

**Citação literal:**
> "there is no best technique"

Página: 23

### Checklist
- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

## Ficha 6 — MADKOUR et al. (2017) ⚠️ elegibilidade pendente

### Identificação do artigo
- Referência completa: MADKOUR, A.; AREF, W. G.; REHMAN, F. U.; RAHMAN, M. A.; BASALAMAH, S. A survey of shortest-path algorithms. arXiv:1705.02044v1 [cs.DS], 4 mai. 2017.
- DOI ou URL: https://arxiv.org/abs/1705.02044 
- Base de origem: arXiv (fora das bases planejadas)
- Leitor responsável: `[Gabriel Nascimento de Souza]`
- Data da leitura: `[03/10/2026]`


### Fichamento

**Problema investigado:** Há uma grande quantidade de algoritmos de caminho mínimo, e nenhum resolve todas as variantes do problema por causa das complexidades de espaço e tempo (resumo, p. 1).

**Objetivo do estudo:** Classificar os algoritmos por uma taxonomia proposta e apresentar desafios e soluções de cada categoria (p. 1–2).

**Método utilizado:** Revisão da literatura organizada em uma taxonomia: algoritmos estáticos (origem única, todos os pares, oráculos de distância, direcionados ao destino, hierárquicos), dinâmicos, dependentes do tempo, estocásticos, paramétricos, de caminho de substituição, de caminho alternativo e de regiões ponderadas (p. 2–19).

**Contexto, amostra ou dados:** Revisão, sem experimentos próprios. Define n = |V| e m = |E| para as complexidades (p. 4).

**Principais resultados:**
- Dijkstra: origem única, grafos direcionados com pesos não negativos, O(n²), apenas grafos estáticos (p. 5).
- Fredman e Tarjan (F-heap): O(n log n + m) (p. 5).
- Bellman-Ford: O(nm), aceita pesos negativos e detecta ciclos negativos, mas é mais lento que Dijkstra (p. 5–6).
- Todos os pares: Dijkstra repetido custa O(mn + n² log n); Floyd-Warshall custa O(n³) em tempo e O(n²) em espaço com otimização. O primeiro só é menor que o segundo em grafos esparsos (p. 6).
- A\* é descrito como busca informada que pode explorar menos vértices que Dijkstra, mas não acha o caminho mínimo sem boa heurística (p. 10).
- Hierarquias de contração (Geisberger et al.) são descritas na p. 12.
- Para o contexto de emergência, há seções sobre grafos dinâmicos (p. 14–16), dependentes do tempo (p. 16–17) e **caminhos alternativos que evitam uma aresta indesejada** (p. 19).

**Limitações apresentadas:** O texto aponta que Dijkstra não aceita pesos negativos e só atende grafos estáticos (p. 5). Não há seção de limitações do próprio levantamento.

**Contribuição para o nosso artigo:** Cobre, em um só texto, Dijkstra, Bellman-Ford e Floyd-Warshall com suas complexidades e o critério de escolha por densidade do grafo (objetivo específico 5). Se Madkour for excluído, a cobertura de Floyd-Warshall cai para uma frase em Bast et al. (p. 4), e será necessário outro artigo. As seções sobre grafos dinâmicos e caminhos alternativos conectam o tema ao problema de bloqueios em emergências.

**Comentário crítico:** Cobertura ampla, mas com imprecisões de redação: afirma que Dijkstra "faz busca de força bruta" e que "não precisa investigar todas as arestas" (p. 5), e repete a complexidade O(n²) sem distinguir a implementação com heap. Há também erros de edição (ex.: "Maue2009", p. 11). Por ser preprint, usar com cautela e, para complexidades, preferir as fontes primárias (Dijkstra, Fredman e Tarjan).

**Citação literal:**
> "Dijkstra's algorithm is used over directed graphs with non-negative weights."

Página: 5

### Checklist
- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

## Ficha 7 — TANG; SUN; CHEN (2016)

### Identificação do artigo
- Referência completa: TANG, J.; SUN, Q.; CHEN, Z. A new implementation of Dijkstra's algorithm on urban rail transit network. In: *International Conference on Civil, Transportation and Environment (ICCTE 2016)*. Atlantis Press, 2016. p. 507–513.
- DOI ou URL:https://www.atlantis-press.com/proceedings/iccte-16/25854272 (Fora das bases Planejadas).
- Base de origem: Atlantis Press
- Leitor responsável: `[Lucas Marins de souza Oliveira]`
- Data da leitura: `[05/10/2026]`

### Fichamento

**Problema investigado:** Em redes de metrô, os pesos de tempo ficam também nos nós (tempo de entrada na estação, de parada, de transferência e de saída), e o Dijkstra tradicional, que rotula nós, falha em achar o menor caminho porque não se sabe qual tempo aplicar antes de escolher o próximo nó (p. 507–508).

**Objetivo do estudo:** Propor uma versão do Dijkstra que funcione na rede original, sem expandi-la, e que considere os tempos de entrada e saída da estação (p. 507, 509).

**Método utilizado:** Princípio dual: o rótulo passa do **nó para a aresta**. Os rótulos p_ij representam o tempo total da origem até a aresta e_ij, e a relaxação é p_jk > p_ij + c_ijk + c_jk, em que c_ijk é o tempo de parada ou de transferência (p. 509–510). O algoritmo tem três fases (inicialização, busca e recuperação do caminho, Fig. 3, p. 510) e usa o princípio de subcaminho ótimo da versão para arestas (p. 510). A alternativa tradicional é expandir cada nó em vários nós (Fig. 2, p. 508–509).

**Contexto, amostra ou dados:** Rede de metrô de Pequim em 2014: 227 estações (nós) e 508 arestas direcionadas, que viram 964 nós e 2.292 arestas se expandida; linhas 7 e 14 excluídas; horários da operadora e tempos de transferência e de entrada e saída estimados. Implementação em C++, Windows 7, Intel Core2 de 2,53 GHz e 2 GB. Dez grupos de 100 a 1.000 pares origem-destino aleatórios (p. 511).

**Principais resultados:** Complexidade declarada **O(m log m)**, contra O(m + n log n) do Dijkstra tradicional com heap de Fibonacci (p. 511). Na prática, o novo algoritmo é mais lento: média de 0,042 s por par contra 0,026 s, uma diferença estável de cerca de 0,016 s (Tabela 1 e Fig. 5, p. 512).

**Limitações apresentadas:** O novo algoritmo gasta mais tempo porque verifica o conjunto permanente D a cada iteração e busca os tempos de transferência e parada durante a atualização (p. 512). Os autores dizem que o tempo poupado ao não expandir a rede "pode compensar" o excesso em alguns tipos de rede, mas isso fica para estudo futuro (p. 513).

**Contribuição para o nosso artigo:** Exemplo de adaptação do Dijkstra a um grafo urbano com **custos nos nós**, com análise de complexidade e comparação empírica. Pode inspirar a modelagem do Atlas Global se houver custos associados a pontos (ex.: entrada e saída de bases e hospitais), mas essa conexão é sugestão do grupo.

**Comentário crítico:** Contexto é transporte público, não emergência. O ganho alegado (não expandir a rede) **não foi medido**: o tempo da versão tradicional exclui a expansão e o mapeamento de volta (p. 512), então a comparação favorece o baseline. Em um grafo desse porte, O(m log m) não melhora o limite O(m + n log n) citado pelos próprios autores. Rede pequena, uma só máquina e sem variância. A diferença total "aumenta" com o número de pares apenas porque há mais consultas; por par, é constante.

**Citação literal:**
> "takes more computing time than the Primary Algorithm"

Página: 512

### Checklist
- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

## Ficha 8 — VERMA et al. (2021)

### Identificação do artigo
- Referência completa: VERMA, D.; MESSON, D.; RASTOGI, M.; SINGH, A. Comparative study of various approaches of Dijkstra algorithm. In: *2021 International Conference on Computing, Communication, and Intelligent Systems (ICCCIS)*. IEEE, 2021. p. 328–336.
- DOI ou URL: https://ieeexplore.ieee.org/document/9397200
- Base de origem: IEEE Xplore 
- Leitor responsável: `[Lucas Marins de souza Oliveira]`
- Data da leitura: `[05/10/2026]`

### Fichamento

**Problema investigado:** Aplicar o Dijkstra a redes muito grandes é custoso, e a escolha da estrutura de dados afeta o desempenho em grafos densos e esparsos (resumo e p. 328).

**Objetivo do estudo:** Implementar e comparar quatro abordagens do Dijkstra (lista ligada com força bruta, heap de Fibonacci, heap binário e Dijkstra bidirecional) em dois tipos de grafo, densos e esparsos (resumo, p. 328).

**Método utilizado:** Implementação das quatro abordagens em ANSI C, compiladas com GCC, em um processador Intel i5 de 7ª geração com 8 GB de RAM. Há pseudocódigo e trechos de código de cada variante. Medição do tempo de execução em milissegundos em 18 casos de teste, com a notação N*V (p. 329–334). Densidade definida como |E| = Θ(|V|²) para denso e |E| = O(|V|) para esparso (p. 328).

**Contexto, amostra ou dados:** 18 casos de teste (9 densos e 9 esparsos) com N de 1E4, 5E4 e 1E5 combinado com segundo parâmetro de 500 a 10E5 (Tabela I, p. 334). Os grafos de teste não são descritos além disso (origem, geração, número de repetições).

**Principais resultados:** O bidirecional (BDD) foi o mais rápido, ou empatou, em 16 dos 18 casos (Tabela II, p. 334); o heap binário (BHI) venceu em dois casos esparsos (10 e 11) por 1 ms (p. 335). Em grafos esparsos, a força bruta (BFB) ficou à frente do F-heap (FHI): por exemplo, 16 ms contra 292 ms em 1E4×500 (Tabela III, p. 334). Em grafos densos, o F-heap foi melhor que a força bruta, exceto no caso 7, onde perdeu por 230 ms (p. 334–335). Valores de destaque: no caso 15 (1E5×10E5), BFB 37.172 ms, BHI 94 ms, BDD 3 ms e FHI 7.103 ms (Tabela I). A conclusão é que o bidirecional é o mais eficiente (p. 336).

**Limitações apresentadas:** Não há seção de limitações. Como trabalho futuro, propõem um sistema inteligente que escolha o algoritmo conforme a natureza do problema (p. 336).

**Contribuição para o nosso artigo:** Comparação empírica de implementações do Dijkstra (objetivo específico 5), útil para discutir o efeito de estrutura de dados, densidade do grafo e busca bidirecional.

**Comentário crítico:** (i) A Tabela I mostra o F-heap muito mais lento que o heap binário (ex.: 7.103 ms contra 94 ms), em contradição com a vantagem teórica de Fredman e Tarjan. Os autores citam que F-heaps são lentos na prática (p. 329) mas não analisam o resultado, que pode indicar implementação pouco otimizada. (ii) O texto não esclarece se as variantes unidirecionais param ao alcançar o destino; o bidirecional é por natureza ponto a ponto, então a comparação pode não ser equivalente. (iii) A notação N*V chama de "vértices" o segundo número, e nos casos esparsos (ex.: 1E4×500) ele seria menor que o número de nós, o que sugere tratar-se de arestas; conferir. (iv) Sem repetições nem variância. (v) O texto diz que o bidirecional dobra a velocidade (10^5 para 5×10^4 iterações, p. 329), mas a Tabela V mostra fatores bem maiores. (vi) Escreve "it is proved", embora o resultado seja empírico (p. 336).

**Citação literal:**
> "Bidirectional Dijkstra algorithm comes out to be the most efficient algorithm"

Página: 336

### Checklist
- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

## Síntese: o que cada artigo cobre da pergunta de pesquisa

| Elemento da pergunta | Artigos que cobrem | Observação |
|---|---|---|
| Conceito do Dijkstra (obj. 2) | Dijkstra (1959) | Complexidade e pesos não negativos vêm de fontes posteriores. |
| Complexidade do Dijkstra | Fredman e Tarjan; Bast; Madkour; Verma; Tang | Teoria (F&T, Bast) e prática (Verma, Tang). |
| Variações e otimizações | Geisberger; Bast; Verma; Madkour; Tang | Hierarquias, bidirecional, heaps, rótulos em arestas. |
| A\* | Hart et al.; Bast; Madkour | Hart não cita Dijkstra. |
| Bellman-Ford | Bast (uma frase); Madkour | |
| Floyd-Warshall | Bast (uma frase); Madkour | Depende de Madkour, que tem pendência de elegibilidade. |
| Roteamento de emergência e busca e resgate | **Nenhum** | Só indireto: grafos dinâmicos e caminhos alternativos (Madkour). |
| Redes dinâmicas, bloqueios | Madkour (p. 14–19); Geisberger (p. 325, 332); Bast (p. 24–25) | Tratadas como tema em aberto ou fora do escopo experimental. |
