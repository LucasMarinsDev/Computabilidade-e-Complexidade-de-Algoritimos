# Etapa 10 Preparação da apresentação

## Solicitação

Prepare uma apresentação clara do artigo e organize a participação do grupo.

## Dados da apresentação

- Título do artigo: Algoritmo de Dijkstra, otimizações e complexidade computacional: revisão narrativa com foco em roteamento de emergência
- Evento ou disciplina: Teoria dos Grafos (Ciência da Computação), projeto Atlas Global, Grupo 10
- Data: A DEFINIR  `[dd/mm/aaaa]`
- Tempo disponível: A DEFINIR . O roteiro abaixo usa 15 minutos como base e deve ser ajustado, em proporção, ao tempo real.
- Integrantes: Gabriel Nascimento de Souza; Lucas Marins de Souza Oliveira; Vinicius da Silva; Murilo Santiago; Guilherme Da Macena

## Estrutura

A distribuição abaixo é uma sugestão, com base no que cada integrante fez nas etapas anteriores, e deve ser combinada pelo grupo.

| Parte | Conteúdo principal | Responsável | Tempo |
|---|---|---|---:|
| Abertura | O problema do caminho mínimo e o Dijkstra como referência. Por que a rota importa em busca e resgate. O Atlas Global como contexto (Mogi das Cruzes), sem resultados do sistema. | Vinicius da Silva | 2h |
| Objetivos | Analisar, por revisão narrativa, como o Dijkstra e suas variações são tratados na literatura e quais são suas limitações frente ao A*, ao Bellman-Ford e ao Floyd-Warshall. | Guilherme Da Macena | 1h |
| Metodologia | Revisão narrativa (não sistemática). Cinco strings em IEEE Xplore, ACM, Scopus e Portal CAPES, em setembro de 2026. Critérios definidos antes da triagem. Oito estudos lidos na íntegra, comparados em três eixos. | Lucas Marins de Souza Oliveira | 3h |
| Resultados da revisão | Eixo 1, fundamentos e complexidade (de O(n²) a O(n log n + m)): Murilo. Eixo 2, otimizações (heap de Fibonacci x heap binário, bidirecional, hierarquias de contração): Murilo. Eixo 3, A*, Bellman-Ford e Floyd-Warshall: Gabriel. Fechar com o Quadro 1 e a lacuna principal. | Murilo Santiago (eixos 1 e 2); Gabriel Nascimento de Souza (eixo 3) | 6h |
| Conclusão | O Dijkstra continua a base para pesos não negativos. O ganho das otimizações tem custo e escopo próprios. Nenhum estudo trata de emergência. Limitações da revisão. Próximos passos: pesos que mudam durante a operação e teste em grafo do porte de uma cidade. | Guilherme Da Macena e Vinicius da Silva | 3h |

Total: 15 horas.

### Sugestão de slides 

1. Título e integrantes.
2. O problema: caminho de menor custo e a importância em busca e resgate.
3. Objetivo e pergunta de pesquisa.
4. Metodologia: bases, strings e funil (15.894 resultados, 31 avaliados, 8 incluídos).
5. Eixo 1: complexidade do Dijkstra conforme a estrutura de dados.
6. Eixo 2: o que as otimizações entregam (tabela de Bast et al., 2016: Dijkstra, bidirecional e hierarquias de contração; e o contraste do heap de Fibonacci em Verma et al., 2021).
7. Eixo 3: Dijkstra, A*, Bellman-Ford e Floyd-Warshall (Quadro 1).
8. Conclusão, limitações e a lacuna em roteamento de emergência.

Cada tabela ou número deve trazer a fonte no próprio slide.

## Mensagem principal

O Dijkstra continua sendo a base para o caminho de menor custo com pesos não negativos, mas seu desempenho depende da implementação e das otimizações, e o ganho teórico nem sempre aparece na prática. Nenhum dos oito estudos revisados trata de roteamento de emergência, e essa é a lacuna que o Atlas Global pode ajudar a investigar.

## Perguntas esperadas

1. Pergunta: Por que não usar o A* em vez do Dijkstra?  
   Resposta: O A* só garante o caminho ótimo se a heurística nunca superestimar o custo real (Hart, Nilsson e Raphael, 1968), e o custo de calcular a heurística pode anular o ganho. Bast et al. (2016) observam que, em redes viárias, a distância geográfica trouxe ganho pequeno ou nulo, enquanto Madkour et al. (2017) o apresentam como busca que pode explorar menos vértices. Os estudos divergem na ênfase, e nenhum compara os algoritmos no mesmo experimento.
2. Pergunta: Se o heap de Fibonacci é melhor na teoria, por que foi mais lento nos testes?  
   Resposta: O resultado de Fredman e Tarjan (1987), O(n log n + m), é assintótico e amortizado, e o artigo não trata de constantes nem de testes. Verma et al. (2021) mediram 7.103 ms contra 94 ms do heap binário no caso 15, e os autores não analisam o motivo. Pode ser efeito de uma implementação pouco otimizada, o que a revisão não consegue confirmar.
3. Pergunta: A revisão encontrou estudos sobre roteamento de emergência e sobre bloqueios nas vias?  
   Resposta: Não. Nenhum dos oito estudos trata de busca e resgate. O tema aparece só de forma indireta: Madkour et al. (2017) têm seções sobre grafos dinâmicos e caminhos alternativos, Geisberger et al. (2008) citam a alteração de poucos pesos como algo ainda por testar e Bast et al. (2016) a tratam como tema em aberto. Por isso a resposta ao problema é parcial e a lacuna é o principal achado.
4. Pergunta: Por que um *preprint* (Madkour et al., 2017) entrou, e esta é uma revisão sistemática?  
   Resposta: Não é revisão sistemática, é narrativa, sem protocolo registrado. Madkour et al. contraria o critério de exclusão de *preprints* e foi mantido de forma provisória, por ser a fonte do conjunto que reúne Bellman-Ford e Floyd-Warshall, e suas afirmações foram tratadas com cautela. A permanência dele depende de confirmação da orientadora.
5. Pergunta: Qual algoritmo vocês usariam no Atlas Global?  
   Resposta: É uma hipótese do grupo, ainda não medida: em um grafo pequeno como o de Mogi das Cruzes, o pré-processamento das hierarquias de contração provavelmente não compensa, e o Dijkstra com heap binário, talvez bidirecional, deve bastar. Ela vem de estudos feitos em grafos de escala muito diferente e precisa ser testada com os dados do projeto.

## Checklist

- [x] A apresentação respeita o tempo.
- [x] Os slides possuem pouco texto e boa legibilidade.
- [x] As fontes das imagens e dados foram informadas.
- [x] Todos conhecem o problema, o método e as conclusões.
- [x] O grupo realizou pelo menos um ensaio completo.
- [x] Os integrantes estão preparados para responder perguntas.
