# Etapa (a) — Escolha do Tema

> **Como preencher:** este documento deve ser preenchido **em conjunto pelo grupo**, mas com registro individualizado da contribuição de cada integrante. Substitua os campos entre `[ ]` pelas informações do seu grupo. Não apague as instruções em itálico — elas ajudam na avaliação do orientador.

---

## 1. Identificação do Grupo

| Campo | Informação |
|---|---|
| Curso / Disciplina | Ciência da Computação / Teoria dos Grafos |
| Projeto de Pesquisa / IC | Atlas Global — Sistema Inteligente de Rotas com Teoria dos Grafos |
| Orientador(a) | Profa. Dra. Andréa Ono Sakai |
| Data de entrega desta etapa | `[não informada no projeto ATLAS — preencher com a data real do grupo]` |
| Integrantes do grupo | Gabriel Nascimento de Souza (RA 39130819); Lucas Marins de Souza Oliveira (RA 47992603); Cauan Gonçalves de Jesus (RA `[não informado no projeto ATLAS]`) |

---

## 2. Tema Escolhido

### 2.1 Área geral de interesse
*Qual grande área do conhecimento/disciplina motivou a escolha (ex.: complexidade dos algoritmos, classes de problemas P, NP, Algoritmos Gulosos, Programação Dinâmica, Divisão e conquista)?*

Teoria dos Grafos, com foco em algoritmos clássicos de caminho mínimo e exploração de conectividade — especificamente o algoritmo de Dijkstra (busca de caminho de menor custo em grafos ponderados) e a Busca em Largura/BFS (exploração de conexões e verificação de acessibilidade).

### 2.2 Tema delimitado (versão final)
*Escreva o tema já delimitado, de forma específica — não o tema amplo. Lembre-se: o tema deve ser enunciado em 1 a 2 frases, como um assunto (ainda não é uma pergunta de pesquisa, isso vem na etapa "c").*

> **Tema:** Modelagem de um sistema inteligente de rotas baseado em teoria dos grafos, utilizando os algoritmos de Dijkstra e Busca em Largura (BFS) para calcular caminhos mínimos e apoiar operações de busca e resgate, deslocamento urbano e logística em situações de emergência.

### 2.3 Do amplo ao específico
*Mostre o raciocínio de delimitação — como vocês chegaram do tema amplo ao tema específico.*

| Tema amplo (ponto de partida) | Tema delimitado (ponto de chegada) |
|---|---|
| Teoria dos Grafos e algoritmos de caminho mínimo | Sistema de rotas em grafo ponderado (Dijkstra + BFS) aplicado a operações de busca e resgate e apoio logístico em emergências, com pontos estratégicos (bases de apoio, hospitais, áreas de desastre, pontos de resgate) representados como vértices e os custos de deslocamento (tempo, distância, dificuldade do trajeto) representados como pesos das arestas |

---

## 3. Justificativa da Escolha

### 3.1 Relevância
*Por que esse tema é importante ou atual? Para quem ele importa (academia, mercado, sociedade)?*

Segundo a documentação do projeto Atlas (arquivo `docs/E1_Template.md`), a motivação central é que, em operações de busca e resgate — especialmente em áreas isoladas, trilhas, regiões rurais ou locais de acesso comprometido —, a escolha do caminho interfere diretamente no tempo de resposta da equipe. Em cenários de pressão, baixa visibilidade do terreno e informações incompletas, a definição da rota tende a ser feita no improviso, o que aumenta o risco da operação e atrasa a chegada ao ponto de resgate. Nem sempre o caminho aparentemente mais curto é o melhor, pois um trecho pode ter maior dificuldade, apresentar obstáculos ou consumir mais tempo do que uma rota alternativa. O sistema é voltado a equipes de busca e resgate, brigadistas, defesa civil e bombeiros. O caráter aplicado do projeto é reforçado pelos dados reais utilizados em `data/grafo.json`, que representam pontos como Corpo de Bombeiros (Centro), UPA Mogilar e ocorrências (deslizamento, acidente de rodovia, chamados de emergência), tornando o tema relevante tanto para a academia (aplicação prática de algoritmos clássicos de grafos) quanto para cenários reais de apoio a operações de emergência.

### 3.2 Viabilidade
*O grupo avaliou se tem tempo, recursos, acesso a dados/fontes e domínio mínimo do assunto para desenvolver esse tema até o fim do projeto?*

| Critério | Avaliação (Sim/Parcial/Não) | Observação |
|---|---|---|
| Tempo disponível é suficiente | `[não informado no projeto ATLAS — preencher com a avaliação real do grupo]` | `[ ]` |
| Há acesso a fontes/dados necessários | Sim | O projeto já possui uma base de dados própria em `data/grafo.json`, com vértices e arestas ponderadas baseados em pontos reais da região (bombeiros, UPA, ocorrências), o que indica que o grupo já dispunha de dados estruturados para o desenvolvimento. |
| O grupo já tem domínio mínimo do tema | Sim | O grupo implementou funcionalmente o algoritmo de Dijkstra (`src/algorithms/dijkstra.py`) e a Busca em Largura (`src/algorithms/bfs.py`), além de testes automatizados (`tests/test_graph.py`), o que demonstra domínio técnico mínimo já alcançado. |
| Recursos técnicos necessários estão disponíveis | Sim | O projeto foi desenvolvido com Python, Flask, SQLite, HTML/CSS e estrutura JSON — tecnologias de acesso livre e já dominadas pelo grupo, conforme README do repositório. |

### 3.3 Originalidade / Não-redundância
*O grupo verificou rapidamente (via um levantamento preliminar) se o tema já é excessivamente explorado ou se existe um ângulo próprio a ser explorado?*

`[não informado no projeto ATLAS — a documentação disponível (README e templates E1/E2/E3) não registra um levantamento preliminar de originalidade; este item deve ser preenchido pelo grupo]`

---

## 4. Validação com o Orientador

| Campo | Informação |
|---|---|
| Data da conversa/validação | `[não informada no projeto ATLAS]` |
| Tema aprovado pelo orientador? | `[não informado no projeto ATLAS]` |
| Observações ou ajustes solicitados pelo orientador | `[não informado no projeto ATLAS]` |

*Observação: a documentação do Atlas identifica a orientadora da disciplina (Profa. Dra. Andréa Ono Sakai, Teoria dos Grafos), mas não traz registro de data, aprovação formal ou ajustes solicitados para a etapa de escolha do tema.*

---

## 5. Contribuição Individual dos Integrantes

> **Importante:** cada integrante deve descrever, com suas próprias palavras, o que efetivamente fez nesta etapa. Contribuições genéricas como "ajudei em tudo" não serão aceitas. Use verbos de ação e seja específico (ex.: "pesquisei 5 temas candidatos e apresentei prós/contras ao grupo").

*A documentação do projeto Atlas não registra, por integrante, o que cada um efetivamente fez na etapa de escolha do tema (não há prints, e-mails ou rascunhos anexados a este respeito nos arquivos do repositório). Os campos abaixo devem ser preenchidos pelo grupo com informações reais — não foram inventados aqui.*

### Integrante 1 — Gabriel Nascimento de Souza
- **O que fez nesta etapa:** `[preenchimento]`
- **Tempo dedicado (aprox.):** `[3h]`
- **Evidência da contribuição** *(print de conversa, rascunho, e-mail, documento compartilhado etc.)*: `[preencher]`

### Integrante 2 — Lucas Marins de Souza Oliveira
- **O que fez nesta etapa:** `[preenchimento]`
- **Tempo dedicado (aprox.):** `[3h]`
- **Evidência da contribuição:** `[]`

### Integrante 3 — Vinicius Da Silva
- **O que fez nesta etapa:** `[pesquisa]`
- **Tempo dedicado (aprox.):** `[3h]`
- **Evidência da contribuição:** `[preencher]`

### Integrante 4 — Murilo Santiago
- **O que fez nesta etapa:** `[pesquisa]`
- **Tempo dedicado (aprox.):** `[3h]`
- **Evidência da contribuição:** `[preencher]`

### Integrante 5 — Guilherme Da Macena
- **O que fez nesta etapa:** `[pesquisa]`
- **Tempo dedicado (aprox.):** `[3h]`
- **Evidência da contribuição:** `[preencher]`

*(Copie o bloco acima para cada integrante adicional do grupo, caso haja.)*

### 5.1 Quadro-resumo de participação

| Integrante | Contribuição principal | % estimado de participação nesta etapa |
|---|---|---|
| Gabriel Nascimento de Souza | `[preencher]` | `[preencher]` |
| Lucas Marins de Souza Oliveira | `[preencher]` | `[preencher]` |
| Vinicius  | `[preencher]` | `[preencher]` |

*A soma das porcentagens deve ser igual a 100%. Divergências de percepção sobre a participação devem ser discutidas em grupo antes do envio — o orientador pode solicitar esclarecimentos individuais em caso de disparidade relevante.*

---

## 6. Checklist Final da Etapa

- [x] Tema delimitado e redigido em 1-2 frases
- [x] Justificativa de relevância escrita
- [ ] Viabilidade avaliada pelo grupo *(3 dos 4 critérios puderam ser sustentados com evidências do repositório Atlas; "tempo disponível" depende de avaliação do grupo)*
- [ ] Verificação preliminar de originalidade realizada *(não há registro disso no Atlas)*
- [ ] Tema validado com o orientador *(não há registro de data/aprovação no Atlas)*
- [ ] Contribuição individual de cada integrante registrada *(não há registro disso no Atlas)*
- [ ] Quadro-resumo de participação preenchido (soma = 100%) *(não há registro disso no Atlas)*

---

**Nota sobre o preenchimento:** as seções 2 (Tema Escolhido) e 3.1/3.2 foram preenchidas com base em informações reais e verificáveis no repositório do projeto Atlas Global (README.md, docs/E1_Template.md e data/grafo.json). Os campos marcados como `[não informado no projeto ATLAS]` ou `[preencher]` não possuem essa informação disponível na documentação do projeto e precisam ser completados pelo grupo com dados reais, para não constar informação falsa neste documento.
