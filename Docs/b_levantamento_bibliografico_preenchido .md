# Etapa (b) — Levantamento Bibliográfico

> **Como preencher:** este documento deve ser preenchido **em conjunto pelo grupo**, mas com registro individualizado da contribuição de cada integrante em cada passo. Substitua os campos entre `[ ]` pelas informações do seu grupo. Não apague as instruções em itálico — elas ajudam na avaliação do orientador.

---

## 1. Identificação do Grupo

| Campo | Informação |
|---|---|
| Curso / Disciplina | Ciência da Computação / Teoria dos Grafos |
| Projeto de Pesquisa / IC | Atlas Global — Sistema Inteligente de Rotas com Teoria dos Grafos |
| Orientador(a) | Profa. Dra. Andréa Ono Sakai |
| Data de entrega desta etapa | `01/09/2026` |
| Integrantes do grupo | Vinicius da Silva; Gabriel Nascimento de Souza; Lucas Marins de Souza Oliveira; Murilo Santiago; Guilherme Da Macena |
| Tema (da etapa "a") | Teoria dos Grafos, com foco em algoritmos clássicos de caminho mínimo e exploração de conectividade — especificamente o algoritmo de Dijkstra (busca de caminho de menor custo em grafos ponderados) |

---

## FASE 1 — Planejamento da Busca

### Passo 1 — Pergunta de pesquisa e palavras-chave

**1.1 Problema/pergunta de pesquisa (versão de trabalho)**
*Ainda não precisa ser a versão final (isso vem na etapa "c"), mas deve orientar a busca desta fase.*

> Como o algoritmo de Dijkstra e suas variações/otimizações podem ser aplicados no desenvolvimento de sistemas inteligentes de recomendação de rotas em grafos de grande escala (ex.: redes viárias e mapas urbanos), e quais são suas principais limitações de desempenho e complexidade computacional frente a alternativas como A*, Bellman-Ford e Floyd-Warshall?

> *Nota: esta é a versão de trabalho da Fase de planejamento. Recomendamos revisar/refinar junto com o orientador antes de consolidar a versão definitiva na etapa "c".*

**1.2 Conceitos-chave e sinônimos**
*Liste os conceitos centrais da pergunta e seus sinônimos, em português e inglês.*

| Conceito-chave | Sinônimos / termos relacionados (PT) | Sinônimos / termos relacionados (EN) |
|---|---|---|
| Algoritmo de Dijkstra | algoritmo do menor caminho, busca de caminho mínimo | Dijkstra's algorithm, shortest path algorithm |
| Grafos ponderados | grafo com pesos, rede ponderada, grafo direcionado | weighted graph, directed graph, weighted network |
| Otimização de rotas | planejamento de rotas, roteamento inteligente, sistema de navegação | route planning, route optimization, intelligent routing, navigation system |
| Complexidade computacional | eficiência algorítmica, desempenho de algoritmos | computational complexity, algorithm efficiency, time complexity |

*Responsável por este passo: `[Vinicius da Silva]`*

---

### Passo 2 — Strings de busca

*Combine os termos do passo 1 com operadores booleanos (`AND`, `OR`, `NOT`). Use aspas para termos compostos e truncamento (`*`) quando a base permitir.*

| Nº | String de busca | Base(s) em que será usada | Elaborada por |
|---|---|---|---|
| 1 | `("Dijkstra" OR "Dijkstra's algorithm") AND ("shortest path" OR "shortest-path" OR "minimum path")` | IEEE Xplore; ACM Digital Library | `[Gabriel Nascimento de Souza]` |
| 2 | `("shortest path algorithm*" OR "route optimization" OR "intelligent routing") AND ("graph theory" OR "weighted graph") AND ("efficiency" OR "computational complexity")` | Scopus; Google Scholar | `[Lucas Marins de Souza Oliveira]` |
| 3 | `("algoritmo de Dijkstra" OR "caminho mínimo") AND ("otimização de rotas" OR "roteamento inteligente" OR "sistema de navegação")` | Portal de Periódicos CAPES | `[Murilo Santiago]` |
| 4 | `("Dijkstra" AND ("A*" OR "Bellman-Ford" OR "Floyd-Warshall")) AND ("comparison" OR "comparative study" OR "performance evaluation")` | IEEE Xplore; Scopus | `[Guilherme Da Macena]` |

---

### Passo 3 — Bases de dados escolhidas

*Selecione de 2 a 4 bases relevantes ao tema. Registre a justificativa — isso vai para a seção de metodologia do artigo/relatório de IC.*

| Base de dados | Por que foi escolhida | Responsável pela busca nesta base |
|---|---|---|
| IEEE Xplore | Base de referência em Ciência da Computação e Engenharia, com forte cobertura de algoritmos, redes e sistemas de roteamento/navegação. | `[Lucas Marins de Souza Oliveira]` |
| ACM Digital Library | Principal base da área de Computação, indexando conferências e periódicos relevantes sobre estruturas de dados e algoritmos de grafos. | `[Lucas Marins de Souza Oliveira]` |
| Scopus | Ampla cobertura multidisciplinar, útil para localizar aplicações do algoritmo em áreas correlatas (logística, GIS, robótica). | `[Gabriel Nascimento]` |
| Portal de Periódicos CAPES | Acesso institucional gratuito e agregador de diversas bases (incluindo IEEE e Scopus), além de produção nacional em português sobre o tema. | `[Gabriel Nascimento]` |
| 

---

### Passo 4 — Critérios de inclusão e exclusão

**Critérios de inclusão:**
- Artigos publicados nos últimos 10 anos (2016–2026), salvo obras clássicas/fundamentais (ex.: o artigo original de Dijkstra, 1959, e trabalhos seminais de complexidade)
- Revisados por pares (periódicos ou anais de conferência indexados)
- Publicados em português ou inglês
- Disponíveis na íntegra (texto completo, via acesso institucional ou aberto)
- Abordam diretamente o algoritmo de Dijkstra, suas variações/otimizações, ou comparações com outros algoritmos de caminho mínimo

**Critérios de exclusão:**
- Resumos (abstracts) sem texto completo disponível
- Duplicatas entre bases
- Artigos fora do escopo (ex.: uso do termo "Dijkstra" apenas como citação secundária, sem foco no algoritmo)
- Não revisados por pares (blogs, posts não acadêmicos, materiais didáticos informais)
- Trabalhos de divulgação sem contribuição técnica ou científica clara

*Definidos em conjunto por: Vinicius da Silva; Gabriel Nascimento de Souza; Lucas Marins de Souza Oliveira; Murilo Santiago; Guilherme Da Macena*

---

## FASE 2 — Execução da Busca e Triagem


### Passo 5 — Execução das buscas e registro dos resultados

*Anote quantos resultados cada string trouxe em cada base (útil para o fluxograma tipo PRISMA, se o projeto exigir). Exporte as referências (BibTeX, RIS, CSV) para um gerenciador de referências.*

| Base | String usada (nº) | Data da busca | Nº de resultados | Executada por |
|---|---|---|---|---|
| IEEE Xplore | 1 | `[dd/mm/aaaa]` | `[preencher após execução]` | `[Nome]` |
| ACM Digital Library | 1 | `[dd/mm/aaaa]` | `[preencher após execução]` | `[Nome]` |
| Scopus | 2 | `[dd/mm/aaaa]` | `[preencher após execução]` | `[Nome]` |
| Portal CAPES | 3 | `[dd/mm/aaaa]` | `[preencher após execução]` | `[Nome]` |
| IEEE Xplore / Scopus | 4 | `[dd/mm/aaaa]` | `[preencher após execução]` | `[Nome]` |

**Total de resultados brutos (soma de todas as buscas):** `[preencher após execução]`

**Gerenciador de referências utilizado:** `[ex.: Zotero, Mendeley — recomenda-se Zotero por ser gratuito e ter plugin de captura de páginas]`
**Formato de exportação:** `[BibTeX / RIS / CSV]`

---

### Passo 6 — Triagem por título e resumo (1ª filtragem)

*Leia apenas título e resumo de cada resultado. Classifique: incluir / excluir / dúvida. Remova duplicatas entre bases.*

| Item de controle | Quantidade |
|---|---|
| Total de resultados antes da triagem | `[]` |
| Duplicatas removidas | `[]` |
| Classificados como "Incluir" | `[]` |
| Classificados como "Excluir" | `[]` |
| Classificados como "Dúvida" | `[]` |

*A triagem detalhada, artigo por artigo, deve ser registrada na planilha de controle do projeto (aba "Triagem de Artigos"). Aqui, registre apenas o resumo quantitativo.*

**Como as dúvidas foram resolvidas?** *(ex.: discussão em grupo, consulta ao orientador)*

*Responsável(is) por esta triagem: `[Nome(s)]`*

---

### Passo 7 — Triagem por leitura completa (2ª filtragem)

*Para os artigos que passaram na primeira filtragem, leia introdução e conclusão. Aplique os critérios de inclusão/exclusão (passo 4) de forma mais rigorosa.*

| Item de controle | Quantidade |
|---|---|
| Total de artigos que entraram nesta filtragem | `[]` |
| Aprovados (conjunto definitivo para fichamento) | `[]` |
| Excluídos nesta etapa | `[]` |

**Principais motivos de exclusão nesta filtragem:**
- Artigo trata de outro algoritmo/tema e cita Dijkstra apenas tangencialmente
- Contribuição metodológica insuficiente ou não verificável (sem validação experimental)

*Responsável(is) por esta triagem: `[Nome(s)]`*

---

## 3. Lista Final de Artigos Selecionados (Conjunto Definitivo)

*Liste aqui os artigos que passaram por todas as filtragens e seguirão para o fichamento (etapa "j"). Referência completa no formato ABNT/APA definido pelo projeto.*


**a) Referências já constantes no documento original**

1. DIJKSTRA, E. W. A note on two problems in connexion with graphs. *Numerische Mathematik*, v. 1, n. 1, p. 269–271, 1959. (artigo original — referência fundacional)
2. MADKOUR, A. et al. A survey of shortest-path algorithms. *arXiv preprint arXiv:1705.02044*, 2017.
3. TANG, J.; SUN, Q.; CHEN, Z. A new implementation of Dijkstra's algorithm on urban rail transit network. In: *International Conference on Civil, Transportation and Environment*. Atlantis Press, 2016. p. 507–513.
4. VERMA, D. et al. Comparative study of various approaches of Dijkstra algorithm. In: *2021 International Conference on Computing, Communication, and Intelligent Systems (ICCCIS)*. IEEE, 2021. p. 328–336.

**b) Referências complementares levantadas nesta atualização (27 novas referências)**

*b.1 — Trabalhos fundacionais / algoritmos clássicos de caminho mínimo*

5. HART, P. E.; NILSSON, N. J.; RAPHAEL, B. A formal basis for the heuristic determination of minimum cost paths. *IEEE Transactions on Systems Science and Cybernetics*, v. 4, n. 2, p. 100–107, 1968. (artigo original do algoritmo A*)
6. BELLMAN, R. On a routing problem. *Quarterly of Applied Mathematics*, v. 16, n. 1, p. 87–90, 1958. (base teórica do algoritmo Bellman-Ford)
7. FORD, L. R. *Network flow theory*. Santa Monica: The RAND Corporation, 1956. (Report P-923).
8. FLOYD, R. W. Algorithm 97: shortest path. *Communications of the ACM*, v. 5, n. 6, p. 345, 1962.
9. WARSHALL, S. A theorem on Boolean matrices. *Journal of the ACM*, v. 9, n. 1, p. 11–12, 1962. (com Floyd, 1962, fundamenta o algoritmo Floyd-Warshall)
10. JOHNSON, D. B. Efficient algorithms for shortest paths in sparse networks. *Journal of the ACM*, v. 24, n. 1, p. 1–13, 1977.
11. YEN, J. Y. Finding the k shortest loopless paths in a network. *Management Science*, v. 17, n. 11, p. 712–716, 1971.
12. FREDMAN, M. L.; TARJAN, R. E. Fibonacci heaps and their uses in improved network optimization algorithms. *Journal of the ACM*, v. 34, n. 3, p. 596–615, 1987. (otimização de Dijkstra com heaps)
13. MOORE, E. F. The shortest path through a maze. In: *Proceedings of the International Symposium on the Theory of Switching*, Part II. Cambridge: Harvard University Press, 1959. p. 285–292.
14. DINITZ, Y.; ITZHAK, R. Hybrid Bellman-Ford-Dijkstra algorithm. *Journal of Discrete Algorithms*, v. 42, p. 35–44, 2017.

*b.2 — Estudos comparativos e revisões (survey)*

15. RACHMAWATI, D.; GUSTIN, L. Analysis of Dijkstra's algorithm and A* algorithm in shortest path problem. *Journal of Physics: Conference Series*, v. 1566, 012061, 2020.
16. ABUSALIM, S. W. G.; IBRAHIM, R.; SARINGAT, M. Z.; JAMEL, S.; WAHAB, J. A. Comparative analysis between Dijkstra and Bellman-Ford algorithms in shortest path optimization. *IOP Conference Series: Materials Science and Engineering*, v. 917, 012077, 2020.
17. BARKUND, S. H. Survey of shortest path algorithms. *JJTU Journal (International Research Journal)*, p. 56 et seq., 2022.
18. TOROSLU, I. H. The Floyd-Warshall all-pairs shortest paths algorithm for disconnected and very sparse graphs. *Software: Practice and Experience*, v. 53, n. 5, p. 1287–1300, 2023.
19. LEWIS, R. A comparison of Dijkstra's algorithm using Fibonacci heaps, binary heaps, and self-balancing binary trees. *arXiv preprint arXiv:2303.10034*, 2023.
20. ABURYASH, H. Comparison studies for different shortest path algorithms. *International Journal of Computers & Technology*, v. 14, n. 8, p. 5979–5986, 2015. DOI: 10.24297/ijct.v14i8.1857.

*b.3 — Técnicas de aceleração, paralelização e otimização*

21. GEISBERGER, R.; SANDERS, P.; SCHULTES, D.; DELLING, D. Contraction hierarchies: faster and simpler hierarchical routing in road networks. In: *International Workshop on Experimental Algorithms (WEA)*, 2008, Provincetown. Proceedings [...]. Berlin: Springer, 2008. p. 319–333.
22. DELLING, D.; SANDERS, P.; SCHULTES, D.; WAGNER, D. Engineering route planning algorithms. In: LERNER, J.; WAGNER, D.; ZWEIG, K. A. (Ed.). *Algorithmics of Large and Complex Networks*. Berlin: Springer, 2009. p. 117–139. (Lecture Notes in Computer Science, v. 5515).
23. HARISH, P.; NARAYANAN, P. J. Accelerating large graph algorithms on the GPU using CUDA. In: *International Conference on High Performance Computing (HiPC)*, 14., 2007. Proceedings [...]. Berlin: Springer, 2007. p. 197–208.
24. SONG, B. High-performance parallelization of Dijkstra's algorithm using MPI and CUDA. *arXiv preprint arXiv:2504.03667*, 2025.

*b.4 — Aplicações em transportes, roteamento e sistemas de navegação*

25. ZILIASKOPOULOS, A. K.; MAHMASSANI, H. S. Time-dependent, shortest-path algorithm for real-time intelligent vehicle highway system applications. *Transportation Research Record*, n. 1408, p. 94–100, 1993.
26. FU, L.; SUN, D.; RILETT, L. R. Heuristic shortest path algorithms for transportation applications: state of the art. *Computers & Operations Research*, v. 33, n. 11, p. 3324–3343, 2006.
27. CONSTANTINOU, C. K.; ELLINAS, G.; PANAYIOTOU, C.; POLYCARPOU, M. Fast shortest path routing in transportation networks with time-dependent road speeds. *arXiv preprint arXiv:1408.4113*, 2014.
28. CHEN, K. Y. An improved A* search algorithm for road networks using new heuristic estimation. *arXiv preprint arXiv:2208.00312*, 2022.

*b.5 — Aplicações em robótica e sistemas embarcados*

29. WANG, H. Application of Dijkstra algorithm in robot path-planning. In: *International Conference on Mechanic Automation and Control Engineering (MACE)*, 2011. Proceedings [...]. IEEE, 2011. DOI: 10.1109/MACE.2011.5987118.
30. DIRIK, M.; KOCAMAZ, A. F. RRT-Dijkstra: an improved path planning algorithm for mobile robots. *Journal of Soft Computing and Artificial Intelligence*, v. 1, n. 2, p. 69–77, 2020.
31. LI, X. Path planning of intelligent mobile robot based on Dijkstra algorithm. *Journal of Physics: Conference Series*, v. 2083, 042034, 2021.

*(Total: 4 referências originais + 27 referências complementares = 31 referências. Adicione quantas linhas forem necessárias caso novos itens sejam incorporados após a triagem das etapas 6 e 7.)*

> **Observação metodológica:** as referências complementares acima foram localizadas via busca orientada pelas strings definidas no Passo 2 (adaptadas para bases de acesso aberto/indexadores gerais, já que o acesso direto às bases institucionais como IEEE Xplore, Scopus e Portal CAPES depende de credenciais da instituição). Antes de compor o conjunto definitivo do Passo 7, o grupo deve: (i) confirmar a existência e os dados completos de cada referência diretamente na base de origem; (ii) obter o texto integral; e (iii) aplicar os critérios de inclusão/exclusão do Passo 4 a cada uma delas, registrando o resultado na planilha de triagem.

---

## 4. Contribuição Individual dos Integrantes

> **Importante:** cada integrante deve descrever, com suas próprias palavras, o que efetivamente fez em cada passo desta etapa. Contribuições genéricas como "ajudei em tudo" não serão aceitas. Use verbos de ação e seja específico (ex.: "executei a busca no IEEE Xplore com a string 2 e obtive 84 resultados; fiz a triagem por título/resumo de 40 desses").


### Integrante 1 — Vinicius da Silva
- **Passo(s) em que atuou:** `[Passos 1 e 5]`
- **O que fez em cada passo:** `[preencher]`
- **Tempo dedicado (aprox.):** `[ex.: 5h]`
- **Evidência da contribuição** *(print de busca, planilha de triagem, exportação BibTeX, etc.)*: `[link ou descrição]`

### Integrante 2 — Gabriel Nascimento de Souza
- **Passo(s) em que atuou:** `[Passos 2 e 5]`
- **O que fez em cada passo:** `[preencher]`
- **Tempo dedicado (aprox.):** `[ex.: 5h]`
- **Evidência da contribuição:** `[link ou descrição]`

### Integrante 3 — Lucas Marins de Souza Oliveira
- **Passo(s) em que atuou:** `[Passos 2 e 6]`
- **O que fez em cada passo:** `[preencher]`
- **Tempo dedicado (aprox.):** `[ex.: 5h]`
- **Evidência da contribuição:** `[link ou descrição]`

### Integrante 4 — Murilo Santiago
- **Passo(s) em que atuou:** `[Passos 3 e 6]`
- **O que fez em cada passo:** `[preencher]`
- **Tempo dedicado (aprox.):** `[ex.: 5h]`
- **Evidência da contribuição:** `[link ou descrição]`

### Integrante 5 — Guilherme Da Macena
- **Passo(s) em que atuou:** `[Passos 4 e 7]`
- **O que fez em cada passo:** `[preencher]`
- **Tempo dedicado (aprox.):** `[ex.: 5h]`
- **Evidência da contribuição:** `[link ou descrição]`

### 4.1 Quadro-resumo de participação por passo

| Passo | Responsável(is) | % estimado de participação de cada um |
|---|---|---|
| 1. Pergunta e palavras-chave | Vinicius da Silva | `[ ]` |
| 2. Strings de busca | Gabriel Nascimento de Souza; Lucas Marins de Souza Oliveira | `[ ]` |
| 3. Bases de dados | Murilo Santiago | `[ ]` |
| 4. Critérios de inclusão/exclusão | Guilherme Da Macena | `[ ]` |
| 5. Execução das buscas | Vinicius da Silva; Gabriel Nascimento de Souza | `[ ]` |
| 6. Triagem título/resumo | Lucas Marins de Souza Oliveira; Murilo Santiago | `[ ]` |
| 7. Triagem texto completo | Guilherme Da Macena | `[ ]` |

### 4.2 Quadro-resumo geral de participação na etapa

| Integrante | % estimado de participação total nesta etapa |
|---|---|
| Vinicius da Silva | `[ex.: 20%]` |
| Gabriel Nascimento de Souza | `[ex.: 20%]` |
| Lucas Marins de Souza Oliveira | `[ex.: 20%]` |
| Murilo Santiago | `[ex.: 20%]` |
| Guilherme Da Macena | `[ex.: 20%]` |

*A soma das porcentagens deve ser igual a 100%. Divergências de percepção sobre a participação devem ser discutidas em grupo antes do envio — o orientador pode solicitar esclarecimentos individuais em caso de disparidade relevante.*

---

## 5. Checklist Final da Etapa

**Fase 1 — Planejamento**
- [x] Pergunta de pesquisa de trabalho definida
- [x] Conceitos-chave e sinônimos (PT/EN) listados
- [x] Strings de busca elaboradas com operadores booleanos
- [x] Bases de dados escolhidas e justificadas
- [x] Critérios de inclusão e exclusão definidos

**Fase 2 — Execução e triagem**
- [ ] Buscas executadas e resultados registrados por base/string
- [ ] Referências exportadas para o gerenciador de referências
- [ ] Triagem por título/resumo concluída (com duplicatas removidas)
- [ ] Triagem por texto completo (introdução/conclusão) concluída
- [ ] Conjunto definitivo de artigos para fichamento compilado

**Documentação**
- [ ] Contribuição individual de cada integrante registrada por passo
- [ ] Quadro-resumo de participação preenchido (soma = 100%)

---
