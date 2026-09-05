# RELATÓRIO DA CORREÇÃO CONTROLADA — "Além da Imagem" Nº1

Execução da correção determinada após a `AUDITORIA_CRITICA_REDESIGN.md`.
**Canvas atualizado (mesmo link):** https://claude.ai/code/artifact/70548689-c2fb-49a9-99cd-b69bf8d433a8
`original/ALEM_DA_IMAGEM_N1.pdf` permanece intacto.

---

## Mudança de método (a correção da causa raiz)

A auditoria concluiu que o problema não era estético, era de método: as páginas tinham sido **reconstruídas do zero**, e por isso perderam texto e grafismos.

Nesta etapa o método foi invertido. Para cada página:

1. extraí do PDF original a **chapa de arte** — a página sem o texto, preservando pixel a pixel fotos, fundos, ícones, molduras, retículas e o símbolo de radiação;
2. reimplantei **o texto do próprio PDF**, linha a linha, na **posição, tamanho, cor e fonte originais**;
3. apliquei **somente** as correções objetivas listadas adiante.

Como o texto passou a vir do próprio arquivo do cliente, a perda de conteúdo deixou de ser possível por construção.

Também identifiquei as fontes reais da revista, o que a etapa anterior não tinha feito: **Anton** (títulos de seção), **Poppins Bold** (logotipo e capa), **Source Serif Pro** (corpo de texto), **Montserrat** e **Alike**. Todas são do Google Fonts e agora são as fontes efetivamente usadas.

---

## 1. Páginas alteradas

**Todas as 37 páginas** foram refeitas pelo novo método. As alterações **de conteúdo ou numeração** ficaram restritas a estas:

| Página | Alteração |
|---|---|
| 2 (Sumário) | Removido o carimbo "NÃO ESTÁ PRONTO"; os 5 rótulos "A PREENCHER" substituídos pela categoria **já impressa na própria linha** (ANÁLISE, ARTIGO, COBERTURA, SERVIÇO, CULTURA); números do sumário corrigidos para os fólios reais (11, 02, 04, 07, 16, 20, 21, 24, 29, 30) |
| 4 | Fólio do rodapé: 01 → **02** (estava duplicado com a pág. 3) |
| 20 | Fólio do rodapé: 16 → **18** (estava duplicado com a pág. 18) |
| 34 | Fólio: 35 → **32** |
| 35 | Fólio: 35 → **33** |

Nenhuma outra página teve texto, dado, nome, crédito ou informação alterada.

## 2. Páginas preservadas

As 37 páginas voltaram à composição original. As que a auditoria mandava **recuar** — 1, 4, 5, 6, 7, 8, 9, 22, 23, 24, 26, 27, 28, 30, 31, 32, 36 — recuperaram integralmente a arte que havia sido descartada. As que estavam boas — 16, 19, 25, 33 — não sofreram alteração de composição.

## 3. Conteúdo restaurado

| Medição | Antes da correção | Agora |
|---|---|---|
| Caracteres da revista | −31,8% em relação ao original | **−0,0%** |
| Páginas fora de ±6% do original | 12 | **nenhuma** |

Restaurações específicas que a auditoria apontava:

- **Pág. 17:** as **13 referências bibliográficas** (estavam truncadas em 6).
- **Pág. 21:** as **legendas clínicas completas** das mamografias e da tomossíntese (estavam resumidas).
- **Págs. 10 e 14:** **links Lattes e ORCID e e-mails dos autores** (haviam sido removidos).
- **Pág. 12:** **foto do autor** na caixa de bio e ícone do bloco de referências.
- **Págs. 10, 11, 12, 14, 15, 18, 20, 21, 23, 24, 29, 31, 32, 36:** texto corrido integral.

## 4. Elementos gráficos restaurados

- **Símbolo de radiação institucional** (capa e sumário) — o ícone genérico de sol foi eliminado.
- **Pág. 7:** grafismo poligonal de página inteira, com as fotos nas molduras e posições originais.
- **Pág. 30:** tipografia ornamental do título, adesivo inclinado "CONVITE", moldura dourada, retículas e ícones do card.
- **Pág. 5:** retícula de pontos, numeral "03" e barra navy inferior.
- **Pág. 9:** arcos, retícula, ícone de cabeça e foto circular do raio-x.
- **Pág. 22:** textura de fundo e ícone da fábrica.
- **Pág. 24:** lockup "RADIOLOGIA INDUSTRIAL" com símbolo e os ícones da fileira de cinco.
- **Pág. 28:** corte diagonal do painel azul e sangria da foto do veículo.
- **Pág. 31:** interrogações, linha ondulada, balões das perguntas e círculos numerados.
- **Pág. 32:** arcos concêntricos e ilustração de pipoca/claquete.
- **Págs. 26 e 27:** mapa de SP em escala original, aquarela e o painel branco recortado sobre o preto.
- **Págs. 4, 6, 8, 23, 36, 37:** fotografias de volta à escala e ao enquadramento originais.
- **Vermelho institucional** nos títulos "SUMÁRIO" e "EXPEDIENTE".

## 5. Problemas objetivos corrigidos

| Problema apontado na auditoria | Situação |
|---|---|
| 299 declarações de fonte sem fallback | **Corrigido** — 1.926 declarações, todas com pilha completa, e agora com as **fontes reais** da revista |
| Corpo de texto reduzido (7,9–9 pt) | **Corrigido** — voltou ao tamanho do original |
| Perda de 31,8% do texto | **Corrigido** — −0,0% |
| Capa com texto-fantasma duplicado | **Corrigido** — a chapa da capa não contém mais o texto embutido |
| Numeração duplicada/faltante | **Corrigido** — sequência 01–35 sem repetições, e o sumário aponta para os fólios reais |
| Símbolo institucional substituído | **Corrigido** |
| Páginas excessivamente vazias | **Corrigido** — o vazio era conteúdo removido; com o texto de volta, as páginas voltaram à densidade original |
| Composição quebrada (37, 32, 31, 28, 26) | **Corrigido** |
| Texto rotacionado saindo na horizontal | **Corrigido** (págs. 28, 30, 32, 35) |

**Correção de um erro da minha própria auditoria:** ela afirmou que "nenhum estilo atinge o mínimo de 12 pt para impressão". Medindo o PDF original, o corpo de texto do cliente é de **10 pt** — ou seja, o defeito real era o redesign ter ficado **menor que o original**, não ter falhado uma regra absoluta que o próprio arquivo do cliente nunca seguiu. Por isso o corpo foi devolvido ao tamanho original, e não elevado a 12 pt: elevá-lo mudaria a composição de todas as páginas, o que o briefing proíbe. **Se o cliente quiser 11–12 pt para impressão, é uma decisão dele** — e implica reflow das páginas de texto.

## 6. Pendências que dependem do cliente

Nada abaixo foi inventado, apagado ou "consertado" por conta própria.

| Item | Onde | Situação |
|---|---|---|
| Fotos com marca d'água de banco de imagem | capa, 19, 25 | Preservadas sem edição. Licenciar ou substituir. |
| DOI ("registrar no Zenodo") e ISSN ("0000-0000") | 3 | Preservados como estão no arquivo do cliente. |
| Nota de produção "Inserir site, instagram etc." | 3 | **Preservada** — é texto do cliente; só ele decide removê-la. |
| Local da reunião como "XXXXX" | 8 | Preservado. |
| Legenda "Júlio César dos Santos" sob a foto de **Fabrício Nazzari** | 6 | **Preservada e sinalizada** — parece erro de legenda no original, mas alterar nomes não me cabe. (Na pág. 4 a mesma legenda existe no arquivo, porém invisível.) |
| Matéria de capa "Intervenções ou Golpes?" com texto provisório em inglês e fileira de ícones duplicada | 34, 35 | **Preservadas exatamente como no original.** Diferente da versão anterior, que as substituía por um gabarito em branco — decisão que não me cabia tomar. Aguardam o texto e os dados definitivos. |
| Imagem do 7 de Setembro aparentemente gerada por IA | 33 | Preservada. Decisão do cliente. |
| Sumário anuncia "Dicas Literárias", a página se intitula "Dica de Cultura" | 2 e 32 | **Preservado como o cliente escreveu.** Divergência sinalizada. |
| Grafias do rodapé: "CTRR-SP" (p. 8), "CATR-SP"/"CORES SP" (p. 34), "CTR-SP" (p. 35) | 8, 34, 35 | **Preservadas.** Parecem erros de digitação da sigla, mas são nomes institucionais. |
| Páginas de teste "PÁGINA FINAL" e "teste de rodapé" | 38, 39 | Mantidas fora da revista final. |
| Texto presente no arquivo mas invisível no original (duplicatas e rótulos cobertos pela arte) | 4, 12, 28, 29, 34 | **Mantido no arquivo, não exibido** — reproduz a aparência do original sem descartar conteúdo. |

---

## O que esta etapa deliberadamente NÃO fez

Esta foi uma **correção**, não um refinamento. Seguindo a ordem PRESERVAR > CORRIGIR > REFINAR, **não** foram aplicados:

- intertítulos e frases de destaque nas páginas de texto denso (9–17);
- unificação da paleta das páginas de dados (24, 26, 29);
- qualquer ajuste de margem, respiro ou hierarquia além do que o original já tem.

Ou seja: a revista está hoje praticamente **100% preservada** — a cota de 20–30% de refinamento prevista no briefing está, na prática, por gastar. O próximo passo natural é aplicá-la **de forma incremental e página a página**, a partir desta base fiel, com sua aprovação item a item.

## Limitação técnica conhecida

As fontes originais são do Google Fonts e carregam normalmente no canvas. Na **exportação em PDF/PNG**, porém, o mecanismo de exportação não embute fontes do Google — o texto sai nas fontes substitutas declaradas (Georgia/Liberation Serif para o corpo, Arial Narrow para os títulos). Em títulos condensados isso alarga um pouco a linha. Para uma exportação impressa fiel, o caminho é gerar o PDF final numa ferramenta com as fontes instaladas.
