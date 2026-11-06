# 🚀 AuditaIA — Consultoria em Transformação Digital

🔗 **Acesse o Aplicativo Online (GitHub Pages):** [Clique aqui para abrir o App](https://bonfimarthur885-ship-it.github.io/auditaia-consultoria/)

## 👥 Especialistas Responsáveis (Autores)
- **Arthur Bonfim**
- **Unidade Curricular:** Exploração Digital e Fundamentos Tecnológicos (Objetos de Conhecimento 05 e 06)

---

## 🎯 1. O Problema Empresarial e Objetivo do Aplicativo
Muitas pequenas e médias empresas perdem horas toda semana com tarefas manuais e repetitivas: copiar dados entre planilhas, responder as mesmas dúvidas de clientes, montar relatórios e emitir cobranças. Elas sabem que a IA e as ferramentas No-Code podem ajudar, mas não sabem **quanto vão economizar** nem **quais riscos** correm ao usar IA sem regras (vazamento de dados, senhas compartilhadas, descumprimento da LGPD). O **AuditaIA** (Opção C — Auditor de Automação com IA, Produtividade & Governança LGPD) calcula as horas e os reais que a empresa pode economizar automatizando processos e cruza esse ganho com um checklist de segurança e LGPD. O resultado é um laudo que diz **o que automatizar primeiro e o que precisa ser corrigido antes**.

## 🏛 2. Os 4 Pilares de Boas Práticas Aplicados no Diagnóstico
- **☁ Infraestrutura e Migração para a Nuvem:** avalia onde ficam os sistemas e como é feito o backup. Recomenda SaaS (Google Workspace, Microsoft 365, ERP em nuvem) para a gestão do dia a dia e IaaS/PaaS (AWS, Azure, GCP) só para sistemas próprios ou legados, além da Regra de Backup 3-2-1, link de internet redundante e FinOps.
- **🔄 Sistemas Empresariais (ERP/CRM) e Fluxo de Dados:** verifica se a empresa ainda usa planilhas soltas e se os sistemas têm API. Recomenda integrar ERP e CRM, definir a Fonte Única da Verdade, exigir API aberta e criar um dashboard gerencial.
- **🤖 IA Generativa e Automação No-Code:** a calculadora estima as horas/mês e os R$/ano economizados por tarefa, desconta o custo das ferramentas (ROI) e monta um ranking de oportunidades, do maior ganho para o menor. Recomenda ferramentas No-Code (Make, Zapier, n8n), um piloto de 30 dias e revisão humana (Human-in-the-Loop).
- **🛡 Governança, Ética e Segurança Digital (LGPD):** um checklist de 8 controles (MFA, senhas individuais, menor privilégio, política de uso ético de IA, dados fora de IAs públicas, mapeamento LGPD + DPO, treinamento e anonimização), cada um com status Ativo/Pendente. Se o ganho for alto e a governança baixa, o app alerta para **corrigir a segurança antes de automatizar**.

## 🛠 3. IAs Generativas e Ferramentas Utilizadas
| Ferramenta / IA | Como foi utilizada no projeto |
| :--- | :--- |
| **Claude (Anthropic)** | Leitura dos requisitos (ERS), adaptação do Prompt Mestre para a Opção C, definição das regras de negócio e das fórmulas, pesquisa de referências visuais e geração do código HTML/JS. |
| **Pinterest + pesquisa de mercado** | Referências visuais (dashboards SaaS) e análise de plataformas reais do mesmo segmento: Vanta e Drata (compliance), UiPath Insights (ROI de automação) e Celonis (auditoria de processos). |
| **TailwindCSS & Chart.js (CDN)** | Estilização executiva responsiva e gráficos dinâmicos (radar dos 4 pilares e barras de horas por tarefa). |
| **GitHub & GitHub Pages** | Versionamento de código e publicação em nuvem estática (PaaS/CDN). |

## 🧠 4. Diário de Construção: Como Construímos e Refinamos o App
1. **Concepção e Engenharia de Prompt:** partimos do Prompt Mestre da aula e o adaptamos para a Opção C (prompt completo abaixo). A estratégia foi dar à IA um papel de especialista, o contexto dos 4 pilares e uma lista numerada de requisitos obrigatórios, pedindo um único arquivo `index.html`.
2. **Ajustes e Refinamentos Técnicos:** depois do primeiro teste, pedimos para (a) diferenciar quando usar SaaS e quando usar IaaS/PaaS; (b) descontar o custo das ferramentas para mostrar o ganho **líquido**; (c) criar um "veredito" que cruza o ganho com a nota de segurança; (d) corrigir os gráficos, que saíam em branco no PDF; (e) validar os campos obrigatórios antes de gerar o laudo.
   - **Rodada de revisão das regras de negócio:** revisando o app com olhar de especialista, encontramos e corrigimos falhas de lógica. O alerta de governança agora aparece sempre que a nota de segurança fica abaixo de 50%, qualquer que seja o ganho. O que conta como "ganho alto" passou a depender do porte da empresa. O pilar de IA deixou de ganhar pontos sem nenhuma tarefa informada. A pergunta sobre revisão da IA passou a pontuar "IA sem revisão" como o pior caso. O app agora bloqueia horas acima da capacidade da equipe e recalcula o laudo ao vivo a cada mudança. Também incluímos cards com a nota de cada pilar, o score em % (como pede o enunciado) e um ícone diferente para cada tipo de veredito.
3. **Identidade visual:** criamos 5 direções visuais. Partimos de referências do Pinterest (dashboards escuros com verde-limão) e depois pesquisamos plataformas reais do segmento. A versão final usa fundo claro e limpo (padrão Vanta/Drata, que passa **confiança**), uma barra lateral azul-noite com as etapas da auditoria, números grandes de economia com contexto (padrão UiPath, que mostra **resultado**) e verde-limão só na marca e no ganho líquido. A fonte é a Inter.
4. **Principal Aprendizado:** automatizar com IA sem governança só acelera o risco. O ganho de produtividade é real e mensurável, mas depende de dados organizados (ERP/CRM integrados), infraestrutura confiável (nuvem e backup) e regras claras de segurança e LGPD.

### Prompt Mestre adaptado (Opção C)
```
Atue como um Engenheiro de Software Sênior e Consultor Especialista em Transformação
Digital, Automação com IA e Governança de Dados (LGPD).

Preciso criar um Aplicativo Web Interativo completo em um ÚNICO arquivo chamado
`index.html` (HTML5, TailwindCSS via CDN, Chart.js via CDN e JavaScript Vanilla)
para publicação direta no GitHub Pages.

CONTEXTO DO APLICATIVO:
O app se chama 'AuditaIA' (Opção C — Auditor de Automação com IA, Produtividade &
Governança LGPD). Ele estima quantas horas e quantos reais uma empresa pode economizar
automatizando processos com IA e No-Code, e cruza esse ganho com um checklist de
segurança da informação, ética e LGPD. O diagnóstico cobre 4 Pilares:
1. Infraestrutura Digital e Nuvem (SaaS x IaaS/PaaS, backup 3-2-1, disponibilidade).
2. Sistemas Empresariais e Fluxo de Dados (ERP/CRM integrados, APIs, fim das planilhas soltas).
3. IA Generativa e Automação No-Code (tarefas repetitivas, Human-in-the-Loop, ROI).
4. Governança, Ética e Segurança (LGPD, MFA, menor privilégio, política de uso de IA, anonimização).

REQUISITOS OBRIGATÓRIOS:
1. Cabeçalho executivo com identidade visual de consultoria tecnológica.
2. Identificação: Nome da Empresa, Setor e Nº de Colaboradores.
3. Calculadora de economia: custo médio da hora (R$) e 6 tarefas manuais repetitivas,
   cada uma com checkbox e slider de horas/semana, % automatizável e sugestão de automação.
4. Diagnóstico: 6 perguntas de múltipla escolha (2 de Nuvem, 2 de ERP/CRM, 2 de IA)
   + checklist de 8 controles de Segurança/LGPD.
5. Motor de cálculo em JavaScript, sem recarregar a página: horas economizadas/mês,
   economia/ano, custo das ferramentas, ganho líquido (ROI), nota 0–100 por pilar e
   Score Geral com selo (Risco Alto, Em Transição, Estruturada, Líder Digital).
6. Veredito que cruza ganho x risco: se o ganho for alto e a governança baixa, alertar
   para corrigir a segurança ANTES de automatizar.
7. Dashboard com Chart.js: Radar dos 4 pilares e Barras de horas/mês por tarefa.
8. Ranking de oportunidades de automação e Guia de Boas Práticas personalizado por pilar.
9. Botão 'Carregar Caso Exemplo (Demo)' que preenche uma empresa fictícia e gera o laudo.
10. Botão 'Imprimir / Exportar Laudo em PDF' com window.print() e formatação limpa.
11. Rodapé: 'Privacy by Design (LGPD): Todos os cálculos são processados localmente no
    seu navegador.' e o nome do especialista autor.
12. Layout responsivo (computador e celular).

Gere o código `index.html` completo, sem abreviações, totalmente funcional e estilizado.
```

## 🧮 Como o cálculo funciona
- **Horas liberadas/mês** = horas por semana × 4,33 × % automatizável da tarefa (de 55% a 80%, conforme a tarefa).
- **Economia bruta/ano** = horas liberadas × custo da hora × 12.
- **Ganho líquido/ano** = economia bruta − custo estimado das ferramentas (R$ 150/mês por tarefa automatizada).
- **Pontuação das respostas:** cada opção vale de 0 a 4 pontos, na ordem em que aparece. A exceção é a pergunta "Alguém revisa o que a IA produz…", que usa um mapa próprio: "Não, vai direto" vale **0** (usar IA sem revisão é o maior risco), "Não usamos IA" vale **1**, e as demais valem 2, 3 e 4.
- **Notas por pilar (0–100%):**
  - Nuvem e ERP/CRM: média das respostas do pilar.
  - IA: 60% maturidade de uso (perguntas de IA) + 40% automação já aproveitada (menos horas manuais por pessoa = nota maior). **Se nenhuma tarefa manual for informada**, o aproveitamento não pode ser medido e a nota usa só as perguntas de IA (100% do peso).
  - Governança: % dos 8 controles de segurança ativos.
- **Score geral** = média dos 4 pilares, em %. Faixas: Risco alto (< 40%), Em transição (40–59%), Estruturada (60–79%) e Líder digital (80%+).
- **Veredito (ganho x risco):**
  - Se a Governança estiver **abaixo de 50%**, o alerta "corrija a segurança antes de automatizar" aparece **sempre**, com o texto adaptado ao tamanho do ganho.
  - O **limite de "ganho alto"** é proporcional ao porte: **R$ 1.000 por colaborador por ano, com mínimo de R$ 5.000** (ex.: 22 colaboradores → R$ 22.000; 3 colaboradores → R$ 5.000).
  - Com governança adequada: ganho acima do limite = sinal verde; ganho positivo abaixo do limite = moderado; ganho zero ou negativo = neutro.
- **Validação de horas:** o total de horas/semana das tarefas não pode passar de **colaboradores × 44 h** (jornada semanal). Se passar, o app avisa e não gera o laudo.
