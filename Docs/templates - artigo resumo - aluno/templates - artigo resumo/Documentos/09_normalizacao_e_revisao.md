# Etapa 9 Normalização e revisão final

## Solicitação

Revise o conteúdo, as citações, as referências e a formatação antes da entrega.

## Identificação

- Título do artigo: Algoritmo de Dijkstra, otimizações e complexidade computacional: revisão narrativa com foco em roteamento de emergência
- Versão revisada: 1 (primeira versão do artigo, revisada em 17/10/2026)
- Data: 17/10/2026
- Responsável pela conferência final: Murilo Santiago (a confirmar pelo grupo)

> Observação: o rascunho do artigo e esta revisão foram preparados com apoio do Claude (IA), a partir das etapas 1 a 7 do repositório, e conferidos contra as fichas da etapa 6. Os itens sem marcação abaixo dependem de conferência humana do grupo.

## Revisão científica

- [x] Tema, problema e objetivos estão alinhados. (O objetivo do artigo foi reescrito como análise da literatura; ver linha 1 do registro de correções.)
- [x] As conclusões respondem ao problema. (A resposta é parcial, e o texto diz isso.)
- [x] Não existem afirmações sem fonte quando a fonte é necessária. (A única inferência do grupo, sobre o pré-processamento em Mogi das Cruzes, está declarada como hipótese a validar.)
- [x] As limitações do trabalho foram reconhecidas.
- [x] Não foram incluídos resultados inexistentes. (Todos os números do artigo foram localizados nas fichas da etapa 6. Nenhum resultado do sistema Atlas Global é apresentado.)

## Citações e referências

- [x] Toda obra citada aparece nas referências. (Conferido por script: 8 de 8.)
- [x] Toda referência listada foi citada no texto. (Conferido por script: 8 de 8, sem sobras.)
- [x] Citações diretas contêm página. (O artigo não usa citações diretas; todas as citações são indiretas.)
- [ ] Autores, títulos, anos, DOI e links foram conferidos. (Conferidos apenas contra as fichas da etapa 6. Os links e DOI ainda não foram abertos um a um.)
- [ ] O padrão exigido foi aplicado de forma consistente. (O repositório não informa o padrão exigido. Foi usada a ABNT, como nas fichas. Faltam as datas de acesso dos links.)

## Escrita

- [x] O texto possui sequência lógica.
- [ ] Os parágrafos apresentam uma ideia principal.
- [ ] Foram corrigidos ortografia e concordância.
- [ ] Repetições e frases vagas foram eliminadas.
- [ ] O texto diferencia descrição de análise crítica.

## Formatação

- [ ] O template institucional foi respeitado. (O texto está em Markdown. O MODELO RESUMO 2026.docx ainda precisa ser preenchido.)
- [ ] Títulos e subtítulos estão padronizados.
- [x] Tabelas e figuras possuem identificação e fonte. (Quadro 1, com título e fonte.)
- [ ] Margens, fonte, espaçamento e paginação foram conferidos.

## Registro das correções

| Seção | Problema encontrado | Correção realizada | Responsável |
|---|---|---|---|
| Introdução (objetivo) | O objetivo geral da etapa 3 ("desenvolver um sistema") e os objetivos específicos 3 e 4 (modelar e implementar) não cabem em uma revisão bibliográfica. O README do repositório manda voltar à etapa 2 quando o grupo propõe protótipo. | O objetivo do artigo foi escrito como análise da literatura. O Atlas Global aparece só como contexto e nenhum resultado dele é apresentado. **A validar com a orientadora.** | Rascunho: Claude. Validação: Murilo Santiago e grupo |
| Metodologia (triagem) | O repositório não registra como se chegou de 15.889 resultados a 31 registros avaliados (as buscas foram feitas sem filtros). | Marcado como `[PENDENTE]` no texto, sem inventar o critério. | Lucas Marins de Souza Oliveira; Murilo Santiago (responsáveis pela triagem na etapa b) |
| Metodologia (total de resultados) | A etapa 5 informa 15.894 resultados, e a soma das oito buscas é 15.889. | A diferença de 5 foi atribuída à consulta complementar na MDPI (5 resultados, registrada na etapa b). É uma dedução aritmética e precisa de confirmação. | Vinicius da Silva |
| Metodologia (Madkour et al.) | O estudo é um *preprint*, o que contraria o critério de exclusão. A etapa 5 deixou o motivo da inclusão como "A PREENCHER" e a etapa 7 deixou a decisão para o grupo. | Mantido de forma provisória, com justificativa no texto (única fonte do conjunto que reúne Bellman-Ford e Floyd-Warshall) e `[PENDENTE]` para confirmação. | Grupo e orientadora |
| Metodologia | Madkour et al. (arXiv) e Tang, Sun e Chen (Atlantis Press) foram localizados fora das bases planejadas. | Declarado no texto. | Rascunho: Claude |
| Revisão, Eixo 1 | Risco de atribuir ao artigo de 1959 a complexidade e a exigência de pesos não negativos, que não estão nele. | Os dois pontos foram atribuídos a Madkour, Bast e Fredman e Tarjan, e o texto diz que o artigo original não os traz. | Rascunho: Claude |
| Revisão, Eixo 3 | Hart, Nilsson e Raphael (1968) não citam Dijkstra, e a relação entre os dois é uma leitura posterior. | A relação foi atribuída a Bast et al. (2016). | Rascunho: Claude |
| Referências | A lista do levantamento (etapa b) estava incompleta: Hart sem periódico, volume e páginas; Bast sem páginas. | Referências completadas com os dados das fichas da etapa 6. | Rascunho: Claude |
| Citações (Bast et al.) | As páginas citadas nas fichas seguem o PDF do capítulo, e não a paginação impressa (p. 19–80). | O artigo cita Bast pela Tabela 1, sem número de página. | Rascunho: Claude |
| Considerações finais | A ideia de que o pré-processamento não compensa em um grafo como o de Mogi das Cruzes é inferência do grupo (etapas 6 e 7). | Escrita como hipótese a validar, com as fontes que a motivam. | Rascunho: Claude |
| Resumo e palavras-chave | O MODELO RESUMO 2026 pede parágrafo único e três palavras-chave separadas por ponto. | Resumo em parágrafo único (268 palavras). No .docx, usar: Algoritmo de Dijkstra. Caminho mínimo. Complexidade computacional. | Murilo Santiago |
| Referências | Os links não têm data de acesso, e DOI e links não foram abertos nesta revisão. | **Pendente.** | Grupo |

## Pendências antes da entrega

1. Descrever como os 31 registros foram escolhidos entre os resultados das buscas (Metodologia).
2. Confirmar com a orientadora a permanência de Madkour et al. (2017) e a reformulação do objetivo.
3. Abrir cada DOI e link, conferir autores, títulos e anos e incluir a data de acesso.
4. Preencher o MODELO RESUMO 2026.docx. Faltam e-mail, RGM, semestre e a titulação da orientadora. O repositório traz dois nomes para ela ("Profa. Dra. Andréa Ono Sakai" na etapa b e "Professora Andreia" na etapa 2), então é preciso confirmar o nome completo.
5. Fazer a revisão de ortografia, concordância e repetições, e conferir margens, fonte, espaçamento e paginação no template.
