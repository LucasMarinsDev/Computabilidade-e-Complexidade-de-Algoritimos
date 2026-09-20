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
//Etapa C//


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
| 5 | `("Dijkstra" OR "shortest path") AND ("emergency routing" OR "emergency response" OR "ambulance routing" OR "search and rescue")` | IEEE Xplore; Scopus | A definir pelo grupo |


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


### Passo 5 — Execução das buscas e registro dos resultados


| Base | String usada (nº) | Data da busca | Nº de resultados | Executada por |
|---|---|---|---|---|
| IEEE Xplore | 1 | 19/09/2026 | 1.622 | Lucas Marins de Souza Oliveira |
| ACM Digital Library | 1 | 19/09/2026 | 10.550 | Lucas Marins de Souza Oliveira |
| Scopus | 2 |19/09/2026 | 3.517 | Gabriel Nascimento de Souza |
| Portal CAPES | 3 | 18/09/2026 | 23 | Gabriel Nascimento de Souza|
| IEEE Xplore | 4 | 18/09/2026 | 10 | Lucas Marins de Souza Oliveira |
| Scopus | 4 | 18/09/2026 | 0 | Gabriel Nascimento de Souza |
| IEEE Xplore | 5 | 17/09/2026 | 126 | Gabriel Nascimento de Souza |
| Scopus | 5 | 17/09/2026 | 41 | Lucas Marins de Souza Oliveira |

---

### Passo 6 — Triagem por título e resumo (1ª filtragem)


| Item de controle | Quantidade |
|---|---|
| Total de resultados antes da triagem | 31 |
| Duplicatas removidas | 11 |
| Classificados como "Incluir" | 8 |
| Classificados como "Excluir" | 23 |
| Classificados como "Dúvida" | 0 |


*Responsável(is) por esta triagem: Lucas Marins de Souza Oliveira; Murilo Santiago*

---

### Passo 7 — Triagem por leitura completa (2ª filtragem)

| Item de controle | Quantidade |
|---|---|
| Total de artigos que entraram nesta filtragem | 31 |
| Aprovados (conjunto definitivo para fichamento) | 8 |
| Excluídos nesta etapa | 23 |

*Responsável(is) por esta triagem: Lucas Marins de Souza Oliveira*

---

## 3. Lista Final de Artigos Selecionados (Conjunto Definitivo)

*Liste aqui os artigos que passaram por todas as filtragens e seguirão para o fichamento (etapa "j"). Referência completa no formato ABNT/APA definido pelo projeto.*

1. DIJKSTRA, E. W. A note on two problems in connexion with graphs. *Numerische Mathematik*, v. 1, n. 1, p. 269–271, 1959. DOI: 10.1007/BF01386390.
2. HART, P. E.; NILSSON, N. J.; RAPHAEL, B. A formal basis for the heuristic determination of minimum cost paths.
3. FREDMAN, M. L.; TARJAN, R. E. Fibonacci heaps and their uses in improved network optimization algorithms. *Journal of the ACM*, v. 34, n. 3, p. 596–615, 1987. DOI: 10.1145/28869.28874.
4. GEISBERGER, R. et al. Contraction hierarchies: faster and simpler hierarchical routing in road networks. In: *Experimental Algorithms (WEA 2008)*. Berlin: Springer, 2008. p. 319–333.
5. BAST, H. et al. Route planning in transportation networks. In: *Algorithm Engineering*. Cham: Springer, 2016. (LNCS 9220). 
6. MADKOUR, A. et al. A survey of shortest-path algorithms. *arXiv preprint arXiv:1705.02044*, 2017.
7. TANG, J.; SUN, Q.; CHEN, Z. A new implementation of Dijkstra's algorithm on urban rail transit network. In: *International Conference on Civil, Transportation and Environment*. Atlantis Press, 2016. p. 507–513.
8. VERMA, D. et al. Comparative study of various approaches of Dijkstra algorithm. In: *2021 International Conference on Computing, Communication, and Intelligent Systems (ICCCIS)*. IEEE, 2021. p. 328–336. *

---

## 4. Contribuição Individual dos Integrantes

### Integrante 1 — Vinicius da Silva
- **Passo(s) em que atuou:** Passos 1 e 5
- **Registrado no documento:** Elaborou a pergunta de trabalho e a tabela de conceitos-chave e sinônimos (Passo 1).
- **Execução (Passo 5):** Realizada pesquisa na base de dados científica MDPI via web/link (URL: `https://www.mdpi.com/2076-3417/15/8/4162`), na qual foram obtidos 5 resultados de artigos em língua inglesa. Destaca-se 1 resultado principal referente ao estudo *"Roteamento Otimizado em Redes Viárias Urbanas: Uma Abordagem Baseada em Grafos Utilizando o Algoritmo de Dijkstra"*, focado na eficiência e complexidade computacional do algoritmo aplicado a grafos.
- **Tempo dedicado (aprox.):** 1h30min
- **Evidência da contribuição:** Imagem anexada no repositório no caminho `evidencias/evidencia-Vinicius.png` (registro do envio e da consulta do artigo).

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
| 1. Pergunta e palavras-chave | Vinicius da Silva | 14.29% |
| 2. Strings de busca | Gabriel Nascimento de Souza; Lucas Marins de Souza Oliveira (strings 3 e 4 também por Murilo Santiago e Guilherme Da Macena) | 14.29% |
| 3. Bases de dados | Murilo Santiago | 14.29% |
| 4. Critérios de inclusão/exclusão | Guilherme Da Macena | 14.29% |
| 5. Execução das buscas | Lucas Marins de Souza Oliveira ; Gabriel Nascimento de Souza | 14.29% |
| 6. Triagem título/resumo | Lucas Marins de Souza Oliveira; Murilo Santiago | 14.29% |
| 7. Triagem texto completo | Guilherme Da Macena | 14.29% |


### 4.2 Quadro-resumo geral de participação na etapa

| Integrante | % estimado de participação total nesta etapa |
|---|---|
| Vinicius da Silva | 20% |
| Gabriel Nascimento de Souza | 20% |
| Lucas Marins de Souza Oliveira | 20% |
| Murilo Santiago | 20% |
| Guilherme Da Macena | 20% |


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
