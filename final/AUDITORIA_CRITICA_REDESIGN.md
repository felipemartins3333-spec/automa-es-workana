# AUDITORIA CRÍTICA DO REDESIGN — "Além da Imagem" Nº1

Auditoria independente do redesign entregue (`final/dc/*.dc.html`, canvas publicado) contra o briefing oficial (`instrucoes/instrucoes.docx`) e a revista original (`original/ALEM_DA_IMAGEM_N1.pdf`).

**Método:** as 37 páginas do redesign foram renderizadas em navegador (794×1123 px, A4 a 96 px/pol) e comparadas lado a lado com o render do PDF original na mesma escala. Além da comparação visual, foram feitas três medições objetivas: contagem de palavras por página (original × redesign), tamanho de corpo de texto declarado (px → pt) contra o tamanho medido no PDF original, e densidade de ocupação de cada página.

**Nenhum arquivo do redesign foi alterado nesta etapa.**

---

## 1. VEREDITO GERAL

**Está fiel ao briefing? Não.**

**O redesign ficou agressivo demais** — e, ao mesmo tempo, tecnicamente defeituoso. Ele ultrapassou com folga o limite de "somente ajustes" pedido pelo cliente, e em várias páginas o resultado não é apenas diferente: é objetivamente pior que o original.

**O principal problema é de método, não de gosto.** O redesign não foi um refinamento do arquivo existente — foi uma **reconstrução do zero em HTML**, página por página, a partir do texto extraído do PDF. Isso tem três consequências inevitáveis, todas confirmadas por medição:

| Medição | Original | Redesign | Situação |
|---|---|---|---|
| Palavras na revista | 7.990 | 5.453 | **−31,8%** |
| Corpo de texto | ~11 a 12,5 pt | 7,9 a 9,75 pt (mais frequente: **7,9 pt**) | **~30% menor**; nenhum estilo atinge o mínimo de 12 pt para impressão |
| Declarações de fonte sem fallback | — | **299 de 333** | Em exportação PDF/PNG a revista inteira cai para serifa padrão |
| Páginas que perderam >40% de densidade visual | — | **25 de 37** | Páginas mais vazias que o original, não mais "arejadas" |

Os três problemas se somam: o texto foi **cortado**, o que sobrou foi **diminuído**, e ainda assim as páginas ficaram **mais vazias** que as originais. Ou seja, o "respiro" que aparece no resultado não é espaço em branco projetado — é conteúdo que sumiu.

Some-se a isso a violação mais direta do briefing: **o símbolo de radiação do logotipo foi substituído por um ícone genérico de sol** na capa e no sumário. O cliente pediu explicitamente para preservar símbolos e elementos gráficos da marca.

**Resposta à pergunta central — "ainda parece a mesma revista, apenas melhor resolvida?":** Não. Em cerca de metade das páginas parece outra publicação: mais limpa, mais neutra, mais corporativa — e menos "Além da Imagem".

---

## 2. ANÁLISE PÁGINA A PÁGINA

Classificação: **A** preservar · **B** refinar (intervenção maior que devia) · **C** recuar · **D** corrigir (defeito objetivo) · **E** pendente · **F** excluir.
"Texto" = variação de palavras medida contra o original.

| Pág | Classe | Problema | Preservar | Alterar | Intervenção |
|---|---|---|---|---|---|
| 01 Capa | **D + C** | Texto-fantasma: a página original inteira foi usada como imagem de fundo, então o título aparece duplicado atrás do título novo. Símbolo de radiação virou um sol genérico. Massa tipográfica do logotipo perdida. | Foto, chamadas, "Intervenções ou Golpes?", marca d'água (pendência) | Refazer o fundo com a foto limpa; restaurar o símbolo de radiação; recuperar o peso do logotipo | **Significativa** |
| 02 Sumário | **B** | O conteúdo corrigido é ganho real. Mas perdeu o vermelho do título, o grande símbolo de radiação e as etiquetas laterais; ganhou chips coloridos que não pertencem ao vocabulário da revista. | Numeração corrigida, títulos reais, mais respiro | Voltar "SUMÁRIO" ao vermelho e à massa original; recuperar o símbolo grande; trocar chips por etiquetas discretas | Moderada |
| 03 Expediente | **B** | Estrutura bem preservada. "EXPEDIENTE" perdeu o vermelho vivo e a massa condensada. | Colunas, dados, marcação de pendências (DOI/ISSN) | Restaurar cor e peso do título | Mínima |
| 04 Presidente CRTR-SP | **C** | A foto de página inteira à direita virou uma miniatura em coluna; o bloco navy que era lateral virou faixa horizontal. Texto −0%. | Texto integral (está correto) | Devolver a foto à escala/coluna original | Moderada |
| 05 Citação CORED-SP | **C** | Removidos o padrão pontilhado do fundo, o numeral "03" e a barra navy inferior; adicionado um sol genérico grande. | Fundo amarelo, citação, crédito | Restaurar padrão, numeral e barra; remover o sol | Moderada |
| 06 Presidente CORED-SP | **C** | Mesmo caso da 04: foto reduzida a miniatura. | Texto integral | Devolver escala da foto | Moderada |
| 07 Membros da CORED | **C** | **Maior perda de identidade da revista.** O grafismo poligonal de página inteira foi apagado e substituído por avatares circulares sobre fundo cinza — vira página de equipe de qualquer instituição. Densidade 64% → 9%. | Nomes, cargos, fotos | Restaurar o grafismo poligonal, apenas atenuando-o para as fotos respirarem | **Significativa** |
| 08 Reuniões | **C + D** | Fotos reduzidas, elementos poligonais removidos, terço inferior vazio. | Legendas, pendência "local a confirmar" | Devolver escala das fotos e o grafismo | Moderada |
| 09 Abertura Formação *(piloto)* | **B** | Perdeu arcos decorativos, retícula de pontos, ícone de cabeça e o arco amarelo; a foto circular encolheu. O piloto foi aprovado, mas revisto de forma independente ele já era mais intervencionista do que "ajustes". | Fundo terracota, título com bloco amarelo, citação, crédito | Restaurar os ornamentos e a escala da imagem | Moderada |
| 10 Formação corpo 1 | **D** | **Texto −31%.** Badges Lattes/ORCID e e-mail do autor **removidos**. | Citação de destaque, 2 colunas | Restaurar texto integral e os links do autor | Moderada |
| 11 Formação corpo 2 | **D** | **Texto −42%.** Intertítulo e citação são adequados (vêm do próprio texto). | Recursos editoriais introduzidos | Restaurar texto integral | Moderada |
| 12 Formação fechamento | **D** | **Texto −34%** (bullets encurtados). Foto do autor na bio **removida**; ícone das referências removido. | Boxes amarelos, referências 1–7 | Restaurar texto, foto e ícone | Moderada |
| 13 Abertura IA/RM | **B** | Composição preservada; o círculo preto e o numeral "11" encolheram; massa do título perdida. | Fundo navy, bloco amarelo, trio RM/+/O | Recuperar escala do círculo e do numeral | Mínima |
| 14 IA/RM corpo 1 | **D** | **Texto −20%.** Lattes/ORCID e e-mail **removidos**. | Intertítulo (vem do texto) | Restaurar texto e links | Moderada |
| 15 IA/RM corpo 2 | **D** | **Texto −46%.** | Citação de destaque | Restaurar texto integral | Moderada |
| 16 IA/RM corpo 3 *(piloto)* | **B** | **Melhor página do redesign.** Texto −4%, infográfico preservado, intertítulo/citação/box de siglas vindos do próprio conteúdo. Ressalva: o box "SIGLAS" é elemento novo, aceitável mas opcional. | Tudo | Só corpo de texto e fonte (correções globais) | Mínima |
| 17 IA/RM fechamento | **D** | **Texto −59%. As referências foram truncadas de 13 para 6** — perda de conteúdo bibliográfico numa publicação acadêmica. Ícone do livro removido. | Bio, estrutura | Restaurar as 13 referências e o texto integral | **Significativa** |
| 18 Workshop palestra 1 | **D** | **Texto −35%.** | Faixa navy, box lilás com foto | Restaurar texto integral | Moderada |
| 19 Foto Baione | **A** | Fiel ao original. Marca d'água mantida sem edição (correto). | Tudo | Nada além das correções globais | Mínima |
| 20 Workshop palestra 2 | **D** | **Texto −46%**; metade inferior vazia. Numeração corrigida (ganho real). | Numeração, box lilás | Restaurar texto integral | Moderada |
| 21 Workshop mamografia | **D** | **Texto −57%** — as legendas técnicas das mamografias (descrição BI-RADS, tomossíntese/S-View) foram resumidas. São conteúdo clínico. | Imagens, citação | Restaurar legendas e texto integrais | **Significativa** |
| 22 Abertura Rad. Industrial | **C** | Fundo texturizado virou gradiente liso; a citação, que no original alterna caixa e peso em ritmo escalonado, foi achatada em caixa-alta uniforme; ícone da fábrica reduzido. | Cor da editoria, citação, crédito | Restaurar textura, ritmo tipográfico e escala do ícone | Moderada |
| 23 Rad. Industrial 1 | **C + D** | **Texto −35%**; foto do operador reduzida; vazio inferior. | Estrutura, box laranja do autor | Restaurar texto e escala da foto | Moderada |
| 24 Rad. Industrial 2 | **C + D** | **Texto −34%.** O lockup "RADIOLOGIA INDUSTRIAL" com símbolo de radiação foi **substituído por um título comum**; a fileira de 5 blocos **perdeu todos os ícones**; aspas grandes removidas. | Conteúdo dos 5 blocos | Restaurar lockup, símbolo e ícones | Moderada |
| 25 Foto Vieira | **A** | Fiel. Marca d'água mantida (correto). | Tudo | Nada além das correções globais | Mínima |
| 26 Boletim | **C + D** | O mapa de SP — elemento visual principal da página — foi reduzido a uma miniatura; a aquarela inferior sumiu; o vazio que a auditoria original apontava **continua lá**, agora com o mapa pequeno. O callout "8 profissionais" usa dado real (correto). | Texto, dado dos 8 fiscais | Devolver o mapa à escala original e resolver o rodapé da página | Moderada |
| 27 Aproximação | **C** | O contraste preto/branco assimétrico do original (painel branco recortado) foi achatado em página preta comum; retrato reduzido. | Fundo preto, dourado, citação | Restaurar o painel branco e a escala do retrato | Moderada |
| 28 Fiscalização | **C + D** | O corte diagonal do painel azul — elemento distintivo — virou retângulo reto; a foto do carro ficou **solta, com folga branca**, sem sangrar; "FISCALIZAÇÃO" rotacionado encolheu. | Lista de ícones + números (boa) | Restaurar diagonal, sangria da foto e escala do título | Moderada |
| 29 Inspeções em Foco *(piloto)* | **D** | **Texto −19%**: o parágrafo da caixa "Transparência e Gestão em Pauta" foi encurtado. A página esvaziou (37% → 9% de densidade) e o terço inferior ficou vazio. Números passaram de azul para laranja sem necessidade. | Unificação da paleta de dados (ganho real e correto) | Restaurar texto integral, ocupar a página, rever a cor dos números | Moderada |
| 30 Agenda CORED | **C** | **Segunda maior perda de personalidade.** A fonte ornamental de "AGENDA CORED", os padrões pontilhados, o adesivo inclinado "CONVITE", a moldura dourada e os ícones do card foram todos removidos. | Fundo navy, informações do evento | Restaurar tipografia ornamental, adesivo, moldura e ícones | **Significativa** |
| 31 Isso Pode? | **C + D** | Removidos: interrogações amarelas, linha ondulada, círculo azul da foto, "rabicho" dos balões de pergunta e marcadores de check. **Texto −28%.** Foto colide com o cabeçalho. Terço inferior vazio. | Cards numerados, referências | Restaurar elementos gráficos e texto; corrigir a colisão | Moderada |
| 32 Dica de Cultura | **C + D** | Arcos concêntricos, ilustração de pipoca/claquete e símbolo de radiação do título removidos; **~60% da página vazia**; imagem pequena. | Barra lateral com "CULTURA" e "30" | Restaurar elementos e reocupar a página | Moderada |
| 33 Foto 7 de Setembro | **A / B** | Adequada. A chamada acrescentada dá função editorial à imagem. Ressalva: a imagem aparenta ser gerada por IA — decisão do cliente. | Foto, chamada | Nada além das correções globais | Mínima |
| 34 Capa "Intervenções ou Golpes?" | **E** | Tratada como pendência, sem conteúdo inventado — **correto**. Ressalva: substituir a página do cliente por um gabarito em branco é uma decisão que ele precisa aprovar. | Estrutura de pendência | Confirmar com o cliente se prefere manter a página original até receber o texto | — |
| 35 Capa continuação | **E** | Idem. | Estrutura de pendência | Idem | — |
| 36 Homenagem 1 | **C + D** | O título do original é **serifado** (voz editorial própria da seção) e virou sans; a foto de arquivo virou miniatura; **texto −18%**; vazio inferior. | Box de citação | Restaurar serifa, escala da foto e texto | Moderada |
| 37 Homenagem 2 | **D** | **Composição quebrada: todo o conteúdo está espremido no terço superior e dois terços da página estão vazios.** Fotos minúsculas. | Texto (íntegro, +2%) | Refazer a distribuição da página | **Significativa** |
| 38–39 | **F** | Páginas de teste, excluídas — **correto**. | — | — | — |

---

## 3. PÁGINAS QUE DEVEM RECUAR

Passaram do limite de "somente ajustes" e precisam voltar para perto do original:

**Recuo significativo:** 07 (Membros), 30 (Agenda), 01 (Capa).
**Recuo moderado:** 04, 05, 06, 08, 09, 22, 23, 24, 26, 27, 28, 31, 32, 36.

O denominador comum dessas páginas: **elementos gráficos institucionais apagados** (polígonos, retículas, arcos, cortes diagonais, adesivos, ícones, símbolo de radiação) e **fotografias reduzidas de escala**. Nenhuma dessas remoções resolvia um problema concreto — foram efeitos colaterais da reconstrução do zero.

---

## 4. PÁGINAS QUE ESTÃO BOAS

- **19 e 25** — fotos de página inteira, fiéis ao original, marca d'água corretamente preservada sem edição.
- **16** — a melhor página do redesign: texto praticamente íntegro, infográfico preservado, recursos editoriais tirados do próprio conteúdo.
- **33** — adequada (com a ressalva da imagem gerada por IA, que é decisão do cliente).
- **34, 35** — o tratamento como pendência está correto.
- **38, 39** — exclusão correta.

**Ganhos reais que devem ser mantidos em qualquer correção:**
1. Correção da numeração de páginas (sequência 01–35, sem duplicações) — resolve um problema real do original.
2. Remoção do carimbo "NÃO ESTÁ PRONTO" e preenchimento do sumário com títulos reais da própria revista.
3. Marcação explícita de pendências (DOI, ISSN, local da reunião) sem inventar dados.
4. Unificação da paleta das páginas de dados (24, 26, 29) — atende ao briefing.
5. Intertítulos e citações extraídos do próprio texto nas páginas 11, 14, 15, 16.

---

## 5. PÁGINAS QUE PRECISAM DE CORREÇÃO

### 5.1 Problemas objetivos (defeitos, não gosto)

| Problema | Páginas | Gravidade |
|---|---|---|
| **Fonte declarada sem fallback (299 ocorrências)** — em exportação PDF/PNG e sem internet, a revista inteira renderiza em serifa padrão. Foi exatamente o que apareceu em todas as 37 capturas desta auditoria. | **todas** | **Crítica** |
| **Corpo de texto abaixo do mínimo de impressão** — 7,9 a 9,75 pt contra ~11–12,5 pt do original. | **todas com texto corrido** | **Crítica** |
| **Perda de 31,8% do texto da revista** | 10, 11, 12, 14, 15, 17, 18, 20, 21, 23, 24, 29, 31, 32, 36 | **Crítica** |
| **Referências truncadas de 13 para 6** | 17 | Alta |
| **Legendas clínicas resumidas** (mamografia/tomossíntese) | 21 | Alta |
| **Links Lattes/ORCID e e-mails de autores removidos** | 10, 14 | Alta |
| **Foto do autor removida da bio** | 12 | Média |
| **Texto-fantasma duplicado no fundo** | 01 | Alta |
| **Composição quebrada / página majoritariamente vazia** | 37, 32, 31 | Alta |
| **Foto solta sem sangria / colisão de elementos** | 28, 31 | Média |
| **Símbolo de radiação substituído por ícone genérico** | 01, 02 | Alta |

### 5.2 Problemas estéticos (identidade, não defeito)

Perda de ornamentos e de escala fotográfica nas páginas listadas na seção 3. São graves em relação ao briefing, mas não são erros de execução — são consequência de terem sido redesenhadas do zero.

---

## 6. CONFORMIDADE COM O BRIEFING

| Item do briefing do cliente | Situação | Evidência |
|---|---|---|
| Manter 70–80% da identidade / alterar 20–30% | **Não cumprido** | 25 de 37 páginas com perda >40% de densidade; identidade gráfica removida em 17 páginas |
| "Manter bem próximo do que está feito; somente ajustes mesmo" | **Não cumprido** | Reconstrução integral em HTML, não ajuste do existente |
| Não criar nova identidade visual | **Parcialmente descumprido** | Páginas 7, 30, 31, 32 leem como outra publicação |
| Preservar a paleta | **Cumprido em parte** | Azul/amarelo mantidos; **vermelho institucional abandonado** (págs. 2 e 3) |
| Manter fontes principais quando funcionando | **Não cumprido** | Fonte original substituída em toda a revista; sem fallback, cai para serifa na exportação |
| Preservar símbolos e elementos gráficos da marca | **Não cumprido** | Símbolo de radiação trocado por ícone genérico; ornamentos removidos em 17 páginas |
| Manter seriedade / credibilidade / institucionalidade | **Cumprido** | Tom e linguagem preservados |
| Aparência de revista profissional | **Parcialmente** | Ganho de organização; perda de personalidade editorial |
| Inspiração Veja/Superinteressante como princípio, não cópia | **Cumprido** | Nenhum layout copiado das referências |
| Relatório 2024 como referência institucional, não modelo | **Cumprido** | Nenhuma imitação direta |
| Sumario 2024 usado apenas no sumário | **Cumprido** | Aplicado só na pág. 2 |
| Melhorar alinhamentos e margens | **Cumprido** | Grid único aplicado |
| Criar mais respiro | **Descumprido no efeito** | O "respiro" veio de texto cortado, não de projeto |
| Equilibrar texto e imagem | **Não cumprido** | Fotos reduzidas em 8 páginas |
| Melhorar quebras de texto | **Cumprido** | Intertítulos/citações do próprio conteúdo |
| Reduzir páginas visualmente pesadas | **Cumprido em excesso** | Páginas ficaram vazias demais |
| Aproveitar melhor as fotografias | **Não cumprido** | Fotos sistematicamente menores que no original |
| Remover elementos repetitivos/desnecessários | **Excedido** | Removidos também elementos necessários da marca |
| Criar hierarquia visual clara | **Cumprido** | Hierarquia legível em todas as páginas |
| Recursos editoriais em páginas densas | **Cumprido** | Boxes, citações, intertítulos, números destacados |
| Variedade entre matérias | **Reduzida** | Cores de editoria mantidas, mas tipografia uniformizada |
| Melhorar o ritmo | **Parcialmente** | Sequência mantida; páginas vazias enfraquecem o ritmo |
| Não inventar conteúdo | **Cumprido** | Nenhum texto, dado, nome ou crédito inventado |
| Não remover conteúdo | **Não cumprido** | −31,8% do texto |
| Não remover marca d'água artificialmente | **Cumprido** | Págs. 1, 19, 25 preservadas como estão |

**Placar: 12 cumpridos · 4 parciais · 9 não cumpridos.** Os não cumpridos concentram-se justamente nos itens que o cliente marcou como obrigatórios (preservar identidade, símbolos, fontes e conteúdo).

---

## 7. PLANO DE CORREÇÃO *(a executar depois, não agora)*

### Etapa 1 — Correções globais (afetam todas as páginas, intervenção mínima por página)
1. **Fonte:** acrescentar pilha de fallback em todas as 299 declarações (ex.: `'Poppins', 'Segoe UI', Arial, sans-serif`) e escolher fallbacks com métrica próxima — sem isso a exportação em PDF sai em serifa.
2. **Corpo de texto:** elevar o texto corrido para **≥16 px (12 pt)** e legendas para **≥12 px (9 pt)**, aproximando-se do original (~11–12,5 pt).
3. **Restaurar o texto integral** de todas as páginas listadas em 5.1 a partir do PDF original — sem resumir, sem cortar, incluindo referências, legendas técnicas, links Lattes/ORCID e e-mails.
4. **Restaurar o símbolo de radiação** no logotipo (capa e sumário) e o vermelho institucional nos títulos "SUMÁRIO" e "EXPEDIENTE".

> Observação: os itens 2 e 3 juntos vão preencher naturalmente a maior parte do vazio das páginas — o vazio é sintoma, não causa.

### Etapa 2 — Recuos (voltar para perto do original)
| Página | Intervenção mínima |
|---|---|
| 07 | Restaurar o grafismo poligonal de fundo, apenas atenuando a saturação para as fotos ganharem destaque |
| 30 | Restaurar tipografia ornamental do título, adesivo "CONVITE", moldura dourada, padrões e ícones |
| 01 | Refazer o fundo a partir da foto limpa (sem o texto original embutido) |
| 05 | Restaurar padrão pontilhado, numeral "03" e barra navy; remover o sol genérico |
| 04, 06, 08, 23, 26, 27, 36 | Devolver às fotos (e ao mapa da 26) a escala e o enquadramento originais |
| 22 | Restaurar textura de fundo e o ritmo tipográfico da citação (caixa/peso alternados) |
| 24 | Restaurar o lockup "RADIOLOGIA INDUSTRIAL" com símbolo e os ícones da fileira de 5 |
| 28 | Restaurar o corte diagonal do painel azul e a sangria da foto do carro |
| 31, 32 | Restaurar interrogações, ondas, balões, arcos e ilustrações |
| 09 | Restaurar arcos, retícula e ícone da abertura |

### Etapa 3 — Correções de composição
- **37**: refazer a distribuição (hoje 2/3 da página vazios).
- **31**: corrigir a colisão da foto com o cabeçalho.
- **26**: resolver o rodapé da página com o mapa em escala correta.
- **29**: restaurar o texto integral da caixa amarela e reocupar a página.

### Etapa 4 — Decisões do cliente (não executar sem resposta)
- Páginas 34–35: manter como gabarito de pendência ou preservar a página original até o texto chegar?
- Fotos com marca d'água (1, 19, 25): licenciar ou substituir?
- Imagem gerada por IA na pág. 33: manter ou substituir por fotografia real?
- Números da pág. 29: voltar ao azul do original ou manter o laranja?

### O que NÃO deve ser desfeito
Numeração corrigida · sumário preenchido com títulos reais · marcação de pendências · paleta unificada de dados · intertítulos e citações extraídos do próprio texto · exclusão das páginas de teste.

---

## 8. DECISÃO FINAL

**Refazer partes específicas, mudando o método** — não basta corrigir pontualmente.

Recomendação em três frentes, nesta ordem:

1. **Corrigir globalmente** (fonte com fallback, corpo de texto ≥12 pt, restauração do texto integral, símbolo de radiação, vermelho institucional). Isto sozinho resolve os defeitos críticos e recupera boa parte do vazio — vale para as 37 páginas.
2. **Recuar 17 páginas** para perto do original, restaurando os elementos gráficos institucionais e a escala das fotografias (seção 3).
3. **Manter como estão** as páginas 16, 19, 25, 33, 34, 35 e os ganhos listados na seção 4.

**Sobre o método daqui para frente:** a causa raiz foi reconstruir cada página do zero em HTML. Para um projeto de "somente ajustes", o caminho correto é partir da página original e intervir sobre ela — mantendo por padrão tudo o que não é o problema a resolver. Onde a reconstrução for inevitável, cada elemento gráfico do original deve ser inventariado antes e reintroduzido depois, e o texto deve ser transcrito integralmente, nunca reescrito.

**O piloto não deve ser tratado como aprovado sem ressalvas.** A página 16 se sustenta; a 9 já continha o excesso (remoção de ornamentos) que se espalhou pelo resto da revista; a 29 já continha o corte de texto. Como o sistema visual foi derivado desse piloto, os dois desvios se propagaram para as 37 páginas.
