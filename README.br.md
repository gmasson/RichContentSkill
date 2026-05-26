#  RichContentSkill 0.1

Uma habilidade de escrita agnóstica em relação à linguagem que aplica padrões de qualidade em 15+ tipos de conteúdo — desde posts de blog e copy de vendas até documentos legais e scripts de vídeo. Funciona em qualquer idioma: a habilidade detecta o idioma do usuário e escreve inteiramente nele.

Jogue em qualquer conversa e todo conteúdo escrito segue regras consistentes e opinadas, projetadas para eliminar enchimento, aberturas fracas, alegações vagas e tom genérico de IA.

> [English](README.md) | Português

## O Que Faz

RichContent funciona como uma camada de qualidade automática. Quando você pede a Claude para escrever qualquer texto que não seja código, a habilidade:

1. **Roteia** a solicitação para o tipo de conteúdo correto (blog, email, landing page, legal, etc.)
2. **Carrega** apenas as regras relevantes — sem contexto inchado
3. **Aplica** princípios universais (sem aberturas fracas, especificidade sobre vagueza, persuasão ética)
4. **Auto-verifica** antes de entregar

### Tipos de Conteúdo Suportados

| # | Tipo | Cobre |
|---|---|---|
| 1 | Blog & Informativo | Artigos, guias, posts educacionais |
| 2 | Copy de Vendas | Texto persuasivo, anúncios, copy de conversão |
| 3 | Descrição de Produtos | Listagens e-commerce, fichas técnicas |
| 4 | Scripts de Vídeos e Reels | YouTube, TikTok, Reels, Stories |
| 5 | Técnico & Tutoriais | Documentação, how-tos, guias passo a passo |
| 6 | E-books & Conteúdo Longo | Capítulos, whitepapers, análises profundas |
| 7 | Institucional / Sobre | Páginas da empresa, declarações de missão |
| 8 | Redes Sociais | LinkedIn, Instagram, Twitter/X, TikTok |
| 9 | Newsletters & Email | Email marketing, campanhas de drip |
| 10 | Press Releases | Anúncios de mídia, comunicados oficiais |
| 11 | Landing Pages | Páginas de conversão, captura de leads |
| 12 | Estudos de Caso | Histórias de sucesso de clientes, narrativas de ROI |
| 13 | Seções FAQ | Páginas de suporte, bases de conhecimento |
| 14 | Notícias & Atualidades | Jornalismo, cobertura de eventos |
| 15 | Conteúdo Legal | Contratos, termos de uso, políticas de privacidade, petições |

## Instalação

Baixe o projeto na versão mais recente em [Releases](https://github.com/gmasson/RichContentSkill/releases) e arraste para qualquer conversa do Claude, dentro da pasta /skills. Pronto — sem configuração, sem dependências.

## Princípios Universais

Estes se aplicam a todos os tipos de conteúdo, sem exceções:

1. **Cada Frase Precisa Merecer Seu Lugar** — se remover não perde nada, remova
2. **Nada de Aberturas Fracas** — nunca comece com "nos dias de hoje..." ou rolhas
3. **Mostre, Não Declare** — substitua afirmações abstratas por evidências concretas
4. **Ênfase É Rara** — negrito/itálico usado com precisão, não decorativamente
5. **Linguagem Consciente da Audiência** — adeque vocabulário e profundidade ao leitor
6. **Credibilidade através da Especificidade** — números, datas e fontes sobre adjetivos vagos
7. **Estrutura Serve o Leitor** — formato escolhido para consumo, não estética
8. **Um Objetivo por Peça** — todo texto tem um objetivo primário que nada compete
9. **Consistência de Linguagem** — saída corresponde ao idioma do usuário em toda parte
10. **Persuasão Ética** — sem depoimentos fabricados, urgência fake ou escassez inventada

## Decisões de Design

- **Arquitetura de duas camadas**: SKILL.md se mantém sob 100 linhas para carregar rápido sem inchar o contexto. Regras detalhadas vivem em arquivo de referência carregado apenas quando necessário.
- **Abordagem router-first**: uma tabela de lookup mapeia gatilhos de linguagem natural (em inglês e português) para a seção de conteúdo correta, então a habilidade funciona independentemente de como o usuário frasa a solicitação.
- **Anti-padrões sobre princípios**: cada seção inclui listas explícitas de "Evitar" e "Frases Proibidas". Restrições negativas são mais fáceis para modelos seguirem que orientação abstrata.
- **Templates estruturais**: todo tipo de conteúdo inclui um bloco de padrão concreto (ex: Gancho → Contexto → Explicação → Exemplo → Aprendizado) para que o modelo tenha um esqueleto, não apenas filosofia.
- **Acionamento agressivo**: a descrição da habilidade é intencionalmente ampla para evitar subativação — ativa para qualquer solicitação de escrita, não apenas quando o usuário diz "RichContent".

## Contribuindo

Contribuições são bem-vindas. Se você quer adicionar um novo tipo de conteúdo, melhorar regras existentes ou corrigir algo:

1. Faça fork do repositório
2. Crie uma branch (`git checkout -b feat/new-content-type`)
3. Edite os arquivos relevantes em `richcontent/`
4. Envie um pull request com descrição clara do que mudou e por quê

Directrizes para contribuições:

- Mantenha SKILL.md sob 120 linhas — se crescer, mova detalhe para o arquivo de referência
- Toda regra deve ser acionável, não filosófica
- Inclua padrões de "Evitar" junto com orientação positiva
- Teste com prompts reais antes de enviar

## Licença

[MIT](LICENSE)
