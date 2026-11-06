# Instrução para criar a skill: "mapa-interativo-caso-penal"

## 1. Objetivo da skill

Criar uma skill que transforma um processo penal já tramitado e julgado (sentença, acórdão, denúncia, peças e documentos anexados pelo usuário) em UM ÚNICO arquivo HTML interativo, autocontido, que funcione como mapa mental navegável do caso. O arquivo decompõe o caso em partes juridicamente analisáveis e pedagogicamente úteis, para estudo, estratégia de atuação e ensino (ex.: workshops de IA aplicada ao Direito).

O artefato não é um resumo ilustrado. É uma ferramenta de raciocínio: o usuário deve conseguir rastrear relações (fato → prova → argumento → artigo → decisão), comparar perspectivas (acusação, defesa, julgador) e identificar pontos de inflexão do caso.

## 2. Quando acionar

Acionar sempre que o usuário pedir: mapa mental/interativo de processo, "quebrar" ou decompor um caso penal, visualizar estratégia processual, material didático a partir de sentença ou acórdão penal, fluxo interativo de um caso julgado, ou anexar peças processuais pedindo análise estruturada. Não acionar para: petições, pareceres, resumos em texto corrido, jurisprudência comparada, processos cíveis ou trabalhistas.

## 3. Entradas e tratamento

- Aceitar PDF, DOCX, TXT, imagens (OCR) ou texto colado. Ler o material completo antes de qualquer geração.
- Se houver só a sentença ou só o acórdão, construir o mapa com o que existe e marcar as lacunas. Nunca preencher a lacuna com suposição.
- Se o usuário não tiver caso, oferecer um caso-modelo FICTÍCIO, declarado como fictício na página inteira, para demonstração.
- Anonimização (obrigatória por padrão): antes de gerar, perguntar se os nomes das partes devem ser substituídos por papéis ou iniciais (ex.: "Acusado A", "Vítima V"). Em caso de segredo de justiça, menor de idade, crimes sexuais ou violência doméstica, anonimizar sem perguntar e avisar. Não incluir CPF, endereços, telefones ou dados sensíveis. Lembrar o usuário da LGPD e de eventual sigilo antes de projetar o material em público.
- Perguntar no máximo duas coisas quando faltar informação decisiva: (a) público (advogados experientes ou misto), (b) foco (defesa, acusação ou neutro). Se o usuário não responder, usar "misto" e "neutro" e seguir.

## 4. Fidelidade jurídica (regras inegociáveis)

1. Todo conteúdo vem dos autos. Não inventar fatos, falas, provas, datas, artigos ou decisões.
2. Cada nó factual, probatório ou decisório traz a fonte (peça e, se disponível, folha/página/evento). Sem fonte localizável, marcar "fonte não localizada".
3. Distinguir sempre: o que a denúncia narra, o que a instrução provou e o que ficou controvertido.
4. Distinguir o que as partes alegaram do que o julgador acolheu. Nunca apresentar tese de parte como fato.
5. Citar dispositivos legais com precisão (lei, artigo, inciso, parágrafo). Em caso de dúvida sobre redação ou vigência à época do fato, sinalizar "verificar vigência" em vez de afirmar.
6. A camada de estratégia e "e se...?" é análise do autor do mapa, não dos autos. Rotulá-la visivelmente como "Análise (não consta nos autos)" e com estilo visual distinto.
7. Não emitir juízo de culpa ou inocência. Avaliar solidez de argumentos e provas, não a pessoa.
8. Incluir aviso fixo: material didático e analítico, não substitui a leitura integral dos autos nem constitui parecer.

## 5. Estrutura obrigatória do artefato (10 seções = 10 ramos do mapa)

Cada seção é um ramo do mapa mental e também uma aba/painel. Cada nó tem: título curto, descrição, fonte, tags e ligações.

1. Identidade do caso: nó central. Número (ou identificador anonimizado), órgão julgador, tipo penal, fase, resultado final, data do fato e do trânsito em julgado.
2. Partes e atores: acusado, vítima, MP, defesa, juiz, testemunhas, peritos, assistente de acusação. Para cada um: papel e interesse/posição no processo.
3. Linha do tempo processual (fluxo): fato → investigação/inquérito → denúncia → recebimento → resposta → instrução → alegações finais → sentença → recursos → trânsito. Cada etapa é clicável e abre o que ocorreu, os atos relevantes e as decisões.
4. Fatos: três camadas rotuladas por cor e ícone: narrado (denúncia), provado (instrução) e controvertido. Cada fato aponta para as provas que o sustentam ou o enfraquecem.
5. Provas e cadeia probatória: testemunhal, pericial, documental, digital, indiciária. Para cada prova: origem, legalidade (licitude, cadeia de custódia, contraditório), força probatória, quem a utilizou e para provar o quê.
6. Tipificação e fundamentos legais: tipo penal, qualificadoras, majorantes e minorantes, excludentes, normas processuais e constitucionais invocadas. Cada dispositivo liga aos argumentos e decisões que o usaram.
7. Teses e argumentos da acusação: tese central, argumentos de sustentação, fundamentos legais, provas mobilizadas.
8. Teses e argumentos da defesa: mesma estrutura, mais teorias alternativas (negativa de autoria, atipicidade, excludente, desclassificação, nulidades, prescrição, etc.).
9. Embate: argumento × contra-argumento: cadeias ligadas (tese → objeção → réplica → resolução do julgador). Indicar quem prevaleceu em cada embate e por quê.
10. Decisões e fundamentação: cada decisão relevante (recebimento da denúncia, cautelares, sentença, acórdãos, embargos), com o que decidiu, a base legal, argumentos acolhidos e rejeitados. Incluir a dosimetria da pena como sub-fluxo passo a passo (pena-base, circunstâncias, agravantes/atenuantes, causas de aumento/diminuição, regime, substituição/sursis), quando houver condenação.

Camadas transversais (presentes em todas as seções, ativáveis por filtro):

- Estratégia e pontos de inflexão: decisões táticas das partes, momentos em que o caso poderia ter virado, alternativas de atuação ("e se...?"), com rótulo de análise, conforme a regra 6.
- Ligações: relações tipadas entre nós (sustenta, enfraquece, fundamenta, contradiz, decide, refuta, depende de).

## 6. Interações obrigatórias

- Mapa mental navegável: nó central, 10 ramos, expansão e recolhimento de nós, zoom e arrastar (pan).
- Painel de detalhes ao clicar em qualquer nó, com descrição, fonte, tags e lista de conexões clicáveis.
- Destaque de dependências: ao clicar em um artigo, fato, prova ou argumento, realçar tudo o que se liga a ele e esmaecer o restante.
- Rastreio de caminho: escolher um fato e seguir a cadeia fato → prova → argumento → dispositivo → decisão, e o inverso (a partir de uma decisão, voltar até os fatos).
- Filtro de perspectiva: Acusação, Defesa, Julgador, Neutro. Muda o realce e o que fica em primeiro plano.
- Modo "O que falhou?": destaca elos fracos (prova ilícita ou frágil, argumento rejeitado, nulidade não arguida, lacuna de fundamentação).
- Alternância de visualizações: mapa mental, linha do tempo/fluxo, e quadro de embates (tese × objeção × réplica).
- Busca por texto com realce, e filtros por tipo de nó e por camada (fatos, provas, leis, argumentos, decisões, estratégia).
- Modo apresentação (para workshop): percurso guiado por etapas, avançando pelos 10 ramos com narrativa curta por etapa, teclas de seta para navegar.
- Legenda fixa de cores, ícones e tipos de ligação.
- Botão de exportar/imprimir o mapa (CSS de impressão limpo) e botão de redefinir visualização.

## 7. Modelo de dados (separar conteúdo de apresentação)

Dentro do próprio HTML, manter todo o conteúdo em um único objeto JSON em uma constante JavaScript, no início do script, para que o usuário (ou a skill) possa regenerar o caso trocando apenas os dados. Estrutura mínima:

- meta: identificador, aviso de anonimização, indicação de caso real ou fictício, data de geração.
- nodes: id, seção (1–10), tipo (fato, prova, lei, argumento, contra-argumento, decisão, ator, etapa, estratégia), título, descrição, fonte, perspectiva (acusação/defesa/julgador/neutro), nível de solidez (quando aplicável), flag de análise (true se não consta nos autos).
- edges: origem, destino, tipo de relação (sustenta, enfraquece, fundamenta, contradiz, decide, refuta, depende), nota opcional.
- timeline: ordem, etapa, data (se houver), nós associados.
- debates: tese, objeção, réplica, resolução, vencedor.
Validar a integridade antes de entregar: nenhuma aresta com id inexistente, nenhum nó órfão, toda seção com ao menos um nó.

## 8. Requisitos técnicos do HTML

- Arquivo único, autocontido, funcional offline: HTML + CSS + JavaScript puro (vanilla). Sem frameworks, sem CDN, sem fontes externas, sem requisições de rede. Usar fontes do sistema.
- Mapa renderizado em SVG (ou canvas) com layout próprio (radial ou em árvore) e roteamento de arestas legível. Evitar sobreposição de rótulos.
- Responsivo (desktop e projetor primeiro; tablet utilizável). Alto contraste, legível a distância em sala.
- Acessibilidade: navegação por teclado (Tab, Enter, setas, Esc), foco visível, atributos ARIA nos painéis e nós, cor nunca como único canal de informação (usar ícone e forma além da cor), respeito a prefers-reduced-motion.
- Desempenho: fluido com até cerca de 150 nós.
- Sem armazenamento persistente obrigatório; se usar estado, que seja só em memória.
- Sem scripts que enviem dados para fora. Nenhum dado do caso sai do arquivo.

## 9. Direção visual

- Estética sóbria, editorial e jurídica, mas moderna; evitar aparência genérica de template. Paleta coerente com cor semântica estável: um matiz por tipo de nó (fato, prova, lei, argumento da acusação, argumento da defesa, decisão, estratégia/análise).
- Hierarquia tipográfica clara; nó central visualmente dominante; animações curtas e funcionais (expandir, destacar), nunca decorativas.
- Camada "Análise (não consta nos autos)" sempre distinguível (borda tracejada ou selo).
- Cabeçalho com identificação do caso, selo de anonimização e aviso didático; rodapé com data de geração.

## 10. Fluxo de trabalho da skill

1. Ler todo o material anexado; identificar o que há e o que falta.
2. Fazer as perguntas de anonimização, público e foco (ver seção 3); seguir com padrões se não houver resposta.
3. Extrair os dados em estrutura intermediária (JSON) seção a seção, com fontes. Revisar contra os autos: nenhum fato, artigo ou decisão sem lastro.
4. Construir as arestas e os embates; marcar solidez e a camada de análise.
5. Gerar o HTML a partir do JSON e dos requisitos das seções 6 a 9.
6. Verificar: abrir o arquivo, testar cada interação listada na seção 6, conferir integridade do JSON, contraste, navegação por teclado e impressão. Corrigir antes de entregar.
7. Entregar o arquivo .html e, em no máximo cinco linhas: o que foi mapeado, lacunas encontradas nos autos, itens marcados "verificar vigência" ou "fonte não localizada", e lembrete de anonimização.

## 11. Critérios de qualidade (checklist final)

- Cada fato, prova e decisão tem fonte ou marca de lacuna.
- Nada na página afirma culpa ou inocência.
- Análise do autor claramente separada do conteúdo dos autos.
- Todas as interações funcionam; o caminho fato → decisão é rastreável nos dois sentidos.
- Nenhuma dependência externa; funciona offline em um duplo clique.
- Dados pessoais tratados conforme a seção 3.
- Linguagem jurídica precisa, em português do Brasil, sem floreio.
