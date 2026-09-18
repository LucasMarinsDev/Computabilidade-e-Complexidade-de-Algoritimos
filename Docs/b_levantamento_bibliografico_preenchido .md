# Etapa (b) — Levantamento Bibliográfico

> **Como preencher:** este documento deve ser preenchido **em conjunto pelo grupo**, mas com registro individualizado da contribuição de cada integrante em cada passo. *Não apague as instruções em itálico — elas ajudam na avaliação do orientador.*
>
> **Legenda desta versão (pós-parecer):** itens marcados como **PENDENTE** dependem de trabalho real que só o grupo pode registrar (execução das buscas, contagens, datas, tempo dedicado, evidências e percentuais). Nenhum desses dados foi inventado. Preencha-os somente com o que de fato foi feito.

---

## 1. Identificação do Grupo

| Campo | Informação |
|---|---|
| Curso / Disciplina | Ciência da Computação / Teoria dos Grafos |
| Projeto de Pesquisa / IC | Atlas Global — Sistema Inteligente de Rotas com Teoria dos Grafos |
| Orientador(a) | Profa. Dra. Andréa Ono Sakai |
| Data de entrega desta etapa | Entrega original: 01/09/2026 · Reenvio após parecer: até 20/09/2026 |
| Integrantes do grupo | Vinicius da Silva; Gabriel Nascimento de Souza; Lucas Marins de Souza Oliveira; Murilo Santiago; Guilherme Da Macena |
| Tema (da etapa "a") | Algoritmo de Dijkstra (caminho de menor custo em grafos ponderados) aplicado ao roteamento de emergência (busca e resgate, recorte Mogi das Cruzes), com foco em análise bibliográfica de complexidade computacional |

---

## FASE 1 — Planejamento da Busca

### Passo 1 — Pergunta de pesquisa e palavras-chave

**1.1 Problema/pergunta de pesquisa (versão de trabalho)**
*Ainda não precisa ser a versão final (isso vem na etapa "c"), mas deve orientar a busca desta fase.*

> Segundo a literatura dos últimos dez anos (e obras fundamentais), quais são a complexidade computacional e os limites de desempenho do algoritmo de Dijkstra e de suas principais otimizações (filas de prioridade/heaps, *contraction hierarchies*) quando aplicado ao roteamento de emergência em redes viárias de grande escala?

*Observação de escopo:* A*, Bellman-Ford e Floyd-Warshall entram **apenas como referência de comparação de complexidade**, não como foco da revisão. O foco é um algoritmo principal (Dijkstra) e métricas de complexidade. Isso atende à orientação de recortar o tema e de tratar esta etapa como **análise bibliográfica**, e não como desenvolvimento de sistema. BFS foi retirado do escopo, conforme orientação recebida.

**1.2 Conceitos-chave e sinônimos**
*Liste os conceitos centrais da pergunta e seus sinônimos, em português e inglês.*

| Conceito-chave | Sinônimos / termos relacionados (PT) | Sinônimos / termos relacionados (EN) |
|---|---|---|
| Algoritmo de Dijkstra | algoritmo do menor caminho, busca de caminho mínimo | Dijkstra's algorithm, shortest path algorithm |
| Grafos ponderados | grafo com pesos, rede ponderada, grafo direcionado | weighted graph, directed graph, weighted network |
| Otimização de rotas | planejamento de rotas, roteamento inteligente, sistema de navegação | route planning, route optimization, intelligent routing, navigation system |
| Complexidade computacional | eficiência algorítmica, desempenho de algoritmos | computational complexity, algorithm efficiency, time complexity |
| Roteamento de emergência | busca e resgate, despacho de ambulâncias, resposta a emergências | emergency routing, emergency response, ambulance routing, search and rescue |
| Otimizações do Dijkstra | fila de prioridade, heap de Fibonacci, hierarquias de contração | priority queue, Fibonacci heap, contraction hierarchies, bidirectional search |

*Responsável por este passo: Vinicius da Silva*

---

### Passo 2 — Strings de busca

*Combine os termos do passo 1 com operadores booleanos (`AND`, `OR`, `NOT`). Use aspas para termos compostos e truncamento (`*`) quando a base permitir.*

| Nº | String de busca | Base(s) em que será usada | Elaborada por |
|---|---|---|---|
| 1 | `("Dijkstra" OR "Dijkstra's algorithm") AND ("shortest path" OR "shortest-path" OR "minimum path")` | IEEE Xplore; ACM Digital Library | Gabriel Nascimento de Souza |
| 2 | `("shortest path algorithm*" OR "route optimization" OR "intelligent routing") AND ("graph theory" OR "weighted graph") AND ("efficiency" OR "computational complexity")` | Scopus | Lucas Marins de Souza Oliveira |
| 3 | `("algoritmo de Dijkstra" OR "caminho mínimo") AND ("otimização de rotas" OR "roteamento inteligente" OR "sistema de navegação")` | Portal de Periódicos CAPES | Murilo Santiago |
| 4 | `("Dijkstra" AND ("A*" OR "Bellman-Ford" OR "Floyd-Warshall")) AND ("comparison" OR "comparative study" OR "performance evaluation")` | IEEE Xplore; Scopus | Guilherme Da Macena |
| 5 *(nova, alinhada ao recorte de emergência)* | `("Dijkstra" OR "shortest path") AND ("emergency routing" OR "emergency response" OR "ambulance routing" OR "search and rescue")` | IEEE Xplore; Scopus | A definir pelo grupo |

*Ajuste feito:* a string 2 citava o Google Scholar, que não consta entre as bases escolhidas no Passo 3. Foi mantida apenas no Scopus para manter a coerência entre os passos. A string 5 foi adicionada porque as strings 1–4 não continham nenhum termo de emergência, e o recorte do tema exige isso.

---

### Passo 3 — Bases de dados escolhidas

*Selecione de 2 a 4 bases relevantes ao tema. Registre a justificativa — isso vai para a seção de metodologia do artigo/relatório de IC.*

| Base de dados | Por que foi escolhida | Responsável pela busca nesta base |
|---|---|---|
| IEEE Xplore | Base de referência em Ciência da Computação e Engenharia, com forte cobertura de algoritmos, redes e sistemas de roteamento/navegação. | Lucas Marins de Souza Oliveira |
| ACM Digital Library | Principal base da área de Computação, indexando conferências e periódicos relevantes sobre estruturas de dados e algoritmos de grafos. | Lucas Marins de Souza Oliveira |
| Scopus | Ampla cobertura multidisciplinar, útil para localizar aplicações do algoritmo em áreas correlatas (logística, GIS, robótica, emergência). | Gabriel Nascimento de Souza |
| Portal de Periódicos CAPES | Acesso institucional gratuito e agregador de diversas bases (incluindo IEEE e Scopus), além de produção nacional em português sobre o tema. | Gabriel Nascimento de Souza |

*Ajuste feito:* foi removida uma linha incompleta que estava no final da tabela. O limite de 4 bases foi respeitado.

---

### Passo 4 — Critérios de inclusão e exclusão

**Critérios de inclusão:**
- Artigos publicados nos últimos 10 anos (2016–2026), salvo obras clássicas/fundamentais (ex.: Dijkstra, 1959; Hart, Nilsson e Raphael, 1968; Fredman e Tarjan, 1987; Geisberger et al., 2008 — trabalhos seminais de complexidade e de otimização de roteamento)
- Revisados por pares (periódicos ou anais de conferência indexados)
- Publicados em português ou inglês
- Disponíveis na íntegra (texto completo, via acesso institucional ou aberto)
- Abordam diretamente o algoritmo de Dijkstra, suas variações/otimizações, ou comparações de complexidade com outros algoritmos de caminho mínimo

**Critérios de exclusão:**
- Resumos (abstracts) sem texto completo disponível
- Duplicatas entre bases
- Artigos fora do escopo (ex.: uso do termo "Dijkstra" apenas como citação secundária, sem foco no algoritmo)
- Não revisados por pares (blogs, posts não acadêmicos, *preprints* sem publicação posterior, materiais didáticos informais)
- Trabalhos de divulgação sem contribuição técnica ou científica clara

*Definidos em conjunto por: Vinicius da Silva; Gabriel Nascimento de Souza; Lucas Marins de Souza Oliveira; Murilo Santiago; Guilherme Da Macena*

---

## FASE 2 — Execução da Busca e Triagem

> **PENDENTE (Fase 2 inteira):** os campos abaixo só podem ser preenchidos depois que as buscas forem executadas de verdade nas bases. Não estimar nem inventar números. Registre exatamente o que cada base devolveu, com a data.

### Passo 5 — Execução das buscas e registro dos resultados

*Anote quantos resultados cada string trouxe em cada base (útil para o fluxograma tipo PRISMA, se o projeto exigir). Exporte as referências (BibTeX, RIS, CSV) para um gerenciador de referências.*

| Base | String usada (nº) | Data da busca | Nº de resultados | Executada por |
|---|---|---|---|---|
| IEEE Xplore | 1 | PENDENTE | PENDENTE | PENDENTE (Passo 3 indica Lucas) |
| ACM Digital Library | 1 | PENDENTE | PENDENTE | PENDENTE (Passo 3 indica Lucas) |
| Scopus | 2 | PENDENTE | PENDENTE | PENDENTE (Passo 3 indica Gabriel) |
| Portal CAPES | 3 | PENDENTE | PENDENTE | PENDENTE (Passo 3 indica Gabriel) |
| IEEE Xplore | 4 | PENDENTE | PENDENTE | PENDENTE |
| Scopus | 4 | PENDENTE | PENDENTE | PENDENTE |
| IEEE Xplore | 5 | PENDENTE | PENDENTE | PENDENTE |
| Scopus | 5 | PENDENTE | PENDENTE | PENDENTE |

*(A string 4 foi separada por base para que cada busca tenha sua própria contagem.)*

**Total de resultados brutos (soma de todas as buscas):** PENDENTE

**Gerenciador de referências utilizado:** Zotero *(sugerido: gratuito e com plugin de captura; confirme se é o que o grupo usou)*
**Formato de exportação:** BibTeX *(sugerido; confirme)*

---

### Passo 6 — Triagem por título e resumo (1ª filtragem)

*Leia apenas título e resumo de cada resultado. Classifique: incluir / excluir / dúvida. Remova duplicatas entre bases.*

| Item de controle | Quantidade |
|---|---|
| Total de resultados antes da triagem | PENDENTE |
| Duplicatas removidas | PENDENTE |
| Classificados como "Incluir" | PENDENTE |
| Classificados como "Excluir" | PENDENTE |
| Classificados como "Dúvida" | PENDENTE |

*A triagem detalhada, artigo por artigo, deve ser registrada na planilha de controle do projeto (aba "Triagem de Artigos"). Aqui, registre apenas o resumo quantitativo.*

**Como as dúvidas foram resolvidas?**
Protocolo definido: (1) discussão em reunião de grupo; (2) persistindo a dúvida, decisão por votação simples entre os integrantes; (3) em caso de empate ou dúvida sobre pertinência ao tema, consulta à orientadora. *Registrar data da reunião e artigos discutidos: PENDENTE.*

*Responsável(is) por esta triagem: Lucas Marins de Souza Oliveira; Murilo Santiago*

---

### Passo 7 — Triagem por leitura completa (2ª filtragem)

*Para os artigos que passaram na primeira filtragem, leia introdução e conclusão. Aplique os critérios de inclusão/exclusão (passo 4) de forma mais rigorosa.*

| Item de controle | Quantidade |
|---|---|
| Total de artigos que entraram nesta filtragem | PENDENTE |
| Aprovados (conjunto definitivo para fichamento) | PENDENTE (meta: 6 a 8, conforme parecer) |
| Excluídos nesta etapa | PENDENTE |

**Principais motivos de exclusão nesta filtragem:**
- Artigo trata de outro algoritmo/tema e cita Dijkstra apenas tangencialmente
- Contribuição metodológica insuficiente ou não verificável (sem validação experimental)
- Não revisado por pares (*preprint* sem publicação posterior)

*Responsável(is) por esta triagem: Guilherme Da Macena*

---

## 3. Lista Final de Artigos Selecionados (Conjunto Definitivo)

*Liste aqui os artigos que passaram por todas as filtragens e seguirão para o fichamento (etapa "j"). Referência completa no formato ABNT/APA definido pelo projeto.*

> **Status: pré-seleção (8 itens, dentro da meta de 6–8 do parecer).** A lista só vira "conjunto definitivo" depois de os Passos 5–7 serem executados. Os itens 1–4 são fundamentos aprovados no parecer ou clássicos consolidados. Os itens 5–8 precisam ser conferidos na fonte (existência, DOI, páginas, revisão por pares).

1. DIJKSTRA, E. W. A note on two problems in connexion with graphs. *Numerische Mathematik*, v. 1, n. 1, p. 269–271, 1959. DOI: 10.1007/BF01386390. *(artigo original — referência fundacional; aprovado no parecer)*
2. HART, P. E.; NILSSON, N. J.; RAPHAEL, B. A formal basis for the heuristic determination of minimum cost paths. *IEEE Transactions on Systems Science and Cybernetics*, v. 4, n. 2, p. 100–107, 1968. DOI: 10.1109/TSSC.1968.300136. *(A*, usado como comparação; aprovado no parecer)*
3. FREDMAN, M. L.; TARJAN, R. E. Fibonacci heaps and their uses in improved network optimization algorithms. *Journal of the ACM*, v. 34, n. 3, p. 596–615, 1987. DOI: 10.1145/28869.28874. *(complexidade de Dijkstra com heap de Fibonacci; aprovado no parecer)*
4. GEISBERGER, R. et al. Contraction hierarchies: faster and simpler hierarchical routing in road networks. In: *Experimental Algorithms (WEA 2008)*. Berlin: Springer, 2008. p. 319–333. *(otimização para redes viárias; aprovado no parecer; conferir DOI)*
5. BAST, H. et al. Route planning in transportation networks. In: *Algorithm Engineering*. Cham: Springer, 2016. (LNCS 9220). *(revisão de técnicas de roteamento em redes viárias — sugestão do assistente; conferir páginas e DOI)*
6. MADKOUR, A. et al. A survey of shortest-path algorithms. *arXiv preprint arXiv:1705.02044*, 2017. *(atenção: é *preprint*, o que conflita com o critério de exclusão do Passo 4. Verificar se houve publicação em periódico; do contrário, justificar como exceção ou substituir)*
7. TANG, J.; SUN, Q.; CHEN, Z. A new implementation of Dijkstra's algorithm on urban rail transit network. In: *International Conference on Civil, Transportation and Environment*. Atlantis Press, 2016. p. 507–513. *(sinalizado "Verificar" no parecer: confirmar existência, DOI e páginas)*
8. VERMA, D. et al. Comparative study of various approaches of Dijkstra algorithm. In: *2021 International Conference on Computing, Communication, and Intelligent Systems (ICCCIS)*. IEEE, 2021. p. 328–336. *(confirmar DOI e páginas no IEEE Xplore)*

*Referências do repositório que o parecer citou e que não estão neste arquivo (ex.: nº 17, Barkund, JJTU Journal 2022, classificada como "fraca") foram deixadas de fora desta lista. A lista de 31 itens do repositório deve ser reduzida aos 6–8 aprovados na triagem real.*

---

## 4. Contribuição Individual dos Integrantes

> **Importante:** cada integrante deve descrever, com suas próprias palavras, o que efetivamente fez em cada passo desta etapa. Contribuições genéricas como "ajudei em tudo" não serão aceitas. Use verbos de ação e seja específico (ex.: "executei a busca no IEEE Xplore com a string 2 e obtive 84 resultados; fiz a triagem por título/resumo de 40 desses").
>
> Em cada integrante abaixo, a linha **"Registrado no documento"** traz apenas o que o próprio arquivo já comprova (autoria de strings, responsabilidade por passos). A linha **"Execução"** deve ser escrita por cada pessoa.

### Integrante 1 — Vinicius da Silva
- **Passo(s) em que atuou:** Passos 1 e 5
- **Registrado no documento:** elaborou a pergunta de trabalho e a tabela de conceitos-chave e sinônimos (Passo 1).
- **Execução (Passo 5):** PENDENTE — descrever base, string, data e nº de resultados das buscas que executou.
- **Tempo dedicado (aprox.):** PENDENTE
- **Evidência da contribuição:** PENDENTE — link ou descrição (print da busca, exportação BibTeX etc.)

### Integrante 2 — Gabriel Nascimento de Souza
- **Passo(s) em que atuou:** Passos 2 e 5
- **Registrado no documento:** elaborou a string de busca 1 (IEEE Xplore; ACM); é o responsável pelas buscas no Scopus e no Portal CAPES (Passo 3).
- **Execução (Passo 5):** PENDENTE — descrever base, string, data e nº de resultados.
- **Tempo dedicado (aprox.):** PENDENTE
- **Evidência da contribuição:** PENDENTE

### Integrante 3 — Lucas Marins de Souza Oliveira
- **Passo(s) em que atuou:** Passos 2 e 6
- **Registrado no documento:** elaborou a string de busca 2 (Scopus); é o responsável pelas buscas no IEEE Xplore e na ACM (Passo 3).
- **Execução (Passo 6):** PENDENTE — descrever quantos títulos/resumos triou e com que resultado.
- **Tempo dedicado (aprox.):** PENDENTE
- **Evidência da contribuição:** PENDENTE

### Integrante 4 — Murilo Santiago
- **Passo(s) em que atuou:** Passos 3 e 6
- **Registrado no documento:** elaborou a string de busca 3 (Portal CAPES); conduziu a escolha e a justificativa das bases de dados (Passo 3).
- **Execução (Passo 6):** PENDENTE — descrever quantos títulos/resumos triou e com que resultado.
- **Tempo dedicado (aprox.):** PENDENTE
- **Evidência da contribuição:** PENDENTE

### Integrante 5 — Guilherme Da Macena
- **Passo(s) em que atuou:** Passos 4 e 7
- **Registrado no documento:** elaborou a string de busca 4 (comparações entre algoritmos); definiu os critérios de inclusão e exclusão (Passo 4).
- **Execução (Passo 7):** PENDENTE — descrever quantos artigos leu na íntegra e quantos aprovou/excluiu.
- **Tempo dedicado (aprox.):** PENDENTE
- **Evidência da contribuição:** PENDENTE

### 4.1 Quadro-resumo de participação por passo

| Passo | Responsável(is) | % estimado de participação de cada um |
|---|---|---|
| 1. Pergunta e palavras-chave | Vinicius da Silva | PENDENTE |
| 2. Strings de busca | Gabriel Nascimento de Souza; Lucas Marins de Souza Oliveira (strings 3 e 4 também por Murilo Santiago e Guilherme Da Macena) | PENDENTE |
| 3. Bases de dados | Murilo Santiago | PENDENTE |
| 4. Critérios de inclusão/exclusão | Guilherme Da Macena | PENDENTE |
| 5. Execução das buscas | Vinicius da Silva; Gabriel Nascimento de Souza *(ver observação abaixo)* | PENDENTE |
| 6. Triagem título/resumo | Lucas Marins de Souza Oliveira; Murilo Santiago | PENDENTE |
| 7. Triagem texto completo | Guilherme Da Macena | PENDENTE |

*Observação: o Passo 3 atribui as buscas no IEEE Xplore/ACM a Lucas, mas este quadro atribui a execução (Passo 5) a Vinicius e Gabriel. O grupo deve confirmar quem realmente executou cada busca e deixar as duas seções consistentes.*

### 4.2 Quadro-resumo geral de participação na etapa

| Integrante | % estimado de participação total nesta etapa |
|---|---|
| Vinicius da Silva | PENDENTE |
| Gabriel Nascimento de Souza | PENDENTE |
| Lucas Marins de Souza Oliveira | PENDENTE |
| Murilo Santiago | PENDENTE |
| Guilherme Da Macena | PENDENTE |

*A soma das porcentagens deve ser igual a 100%. Divergências de percepção sobre a participação devem ser discutidas em grupo antes do envio — o orientador pode solicitar esclarecimentos individuais em caso de disparidade relevante. Não use 20% para todos por padrão: registre a divisão real.*

---

## 5. Checklist Final da Etapa

**Fase 1 — Planejamento**
- [x] Pergunta de pesquisa de trabalho definida (reformulada conforme o parecer)
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

**Ajustes obrigatórios do parecer**
- [x] Arquivo renomeado para o padrão (`b_levantamento_bibliografico_preenchido.md`, sem espaço)
- [x] Nenhum `[preencher]` remanescente (o que depende de dados reais está marcado como PENDENTE)
- [x] Objetivo/pergunta reformulados para análise bibliográfica de complexidade
- [ ] Passos 5–7 executados de fato e lista reduzida a 6–8 artigos
- [ ] Contribuições e percentuais preenchidos com dados reais

---

## 6. Registro de ajustes feitos após o parecer

- Tema e pergunta de pesquisa recortados para Dijkstra em roteamento de emergência (análise bibliográfica); BFS removido.
- Adicionados dois conceitos (roteamento de emergência; otimizações do Dijkstra) e a string de busca 5.
- Corrigida inconsistência do Google Scholar (string 2) e removida linha truncada da tabela do Passo 3.
- Critérios de inclusão: clássicos explicitados; preprints incluídos nos critérios de exclusão.
- Passo 5: tabela expandida para cobrir todas as combinações string × base.
- Lista de artigos reorganizada em pré-seleção de 8 itens, com alertas sobre o preprint (Madkour) e os itens a verificar (Tang, Verma).
- Seção de contribuições: mantido apenas o que o documento comprova; execução, tempo, evidências e percentuais ficam para o grupo.
