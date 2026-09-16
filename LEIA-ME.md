# Laquiatto Veterinária · página principal

Recriação das pranchetas **Desktop V1** (1440 px) e **Mobile V1** (390 px) do arquivo
"Landingpages Layout Premium" no Paper, com a copy de laquiattovet.petvidaeamor.com.
Publicada na raiz em 16/09/2026 no lugar da LP antiga, que continua no histórico do Git (commit 3780da8).

## Integrações
- WhatsApp +55 11 96452-3795, mensagem "Olá encontrei vocês pelo Google, gostaria de atendimento." (o número nunca aparece na página)
- Google Tag Manager `GTM-P57PTHT3` e Microsoft Clarity `xys5jimy4h`: carregam na primeira interação (clique, toque, rolagem ou tecla) ou após 3,5 s
- Mapa do Google: o embed enviado, que só carrega quando a dobra de contato se aproxima

## Falta
- Fotos da seção **etapas**: `img/etapa-1.webp` … `etapa-4.webp` (horizontais, ~740×440).
  Até chegarem, cada card mostra um bloco lilás com o ícone da etapa. Para trocar, substitua
  `<div class="et-img et-img--vazio"><svg …></svg><span class="et-n">01</span></div>` por
  `<div class="et-img"><img src="img/etapa-1.webp" width="740" height="440" alt="…" loading="lazy" decoding="async" /><span class="et-n">01</span></div>`.

## Imagens
- `avaliacao-1..5.webp`: prints reais do Google (os mesmos da raiz)
- `logo.webp`: logo reduzida para 160 px (5 KB)
- `hero-cao-*`, `destaque-*`, `card-caes`, `card-gatos`: fotos do template, sem marca de terceiros
- Ficaram fora: as fotos de etapas da Patinhas (têm a marca dela) e a do cão atropelado da linha "Emergência" (a Laquiatto não anuncia emergência)

## Cores (template turquesa → Laquiatto)
| Papel | Template | Laquiatto |
|---|---|---|
| cor principal / ícones | `#0BA5C7` | `#9333EA` |
| texto de destaque / botões escuros | `#0A7E9B` | `#7E22CE` |
| linha de destaque do título do hero | `#69CADB` | `#F2ED5C` (amarelo da logo) |
| fundo suave (serviços) | `#E6F6FA` | `#F4ECFD` |
| rodapé | `#0D3440` | `#2A0E45` |
| degradê do hero | `#075F76 → #69CADB` | `#3B0F66 → #C084FC` |

Botões de WhatsApp sempre no verde `#25D366`.

## Desempenho (Lighthouse 12 local, servidor com gzip)
| | Performance | Acessibilidade | Boas práticas | SEO |
|---|---|---|---|---|
| Desktop | 100 | 93 | 100 | 100 |
| Mobile (tags no timer de 3,5 s, atual) | 93 | 93 | 79 | 100 |
| Mobile (tags só na primeira interação) | 97 | 93 | 100 | 100 |

- Acessibilidade 93 vem do bloqueio de zoom no celular, que é requisito do projeto.
- No mobile, a nota de Boas Práticas cai por causa dos cookies de terceiros do Clarity quando o timer dispara durante o teste.
- Fontes Manrope e Montserrat servidas localmente (subset latin), sem CSS externo.

## Hero (15/09/2026)
O hero foi trocado pelo layout da referência "Neovet Clinic" enviada pelo usuário, com copy e cores da Laquiatto:
cartão branco com o menu e o nome gigante "Laquiatto Vet" (pingo do i no amarelo da logo), painel roxo com o golden
sobrepondo as letras, "+150 avaliações" à esquerda e título + botão de WhatsApp à direita. No mobile, o cão fica entre
o nome e o texto, com o peito se dissolvendo no roxo. O hero não tem animação de entrada (melhor para o PageSpeed) e os
cards "#1 #2 #3" passaram a ficar logo abaixo dele, sem sobrepor. As demais dobras seguem as pranchetas do Paper.
Lighthouse depois da troca: desktop 100 / 93 / 100 / 100 e mobile 96 / 93 / 100 / 100.

## "O que fazemos" (15/09/2026)
A dobra foi trocada pelo layout de uma referência enviada pelo usuário, com as informações e cores da Laquiatto:
faixa roxa com 4 cards claros (01 Exames, 02 Cirurgias, 03 Consultas, 04 Vacinação). Cada card fechado mostra a
pílula do serviço, a seta e o número grande; o card aberto fica mais alto, com foto, título e texto, pílula em
amarelo e seta virada. Cirurgias fica aberto em repouso; no desktop o card sob o mouse abre, no celular abre o card tocado.

## Depoimentos (15/09/2026)
A dobra de avaliações foi trocada pelo layout de uma referência enviada pelo usuário, com informações e cores da Laquiatto:
faixa roxa com ícone de pata, título "Depoimentos." (ponto amarelo) e nota "4,9 ★★★★★ · com base em +150 avaliações no Google";
à esquerda, fotos do depoimento anterior, atual e próximo; à direita, card claro com nome, "Laquiatto · Rudge Ramos", texto e estrelas.
Os 5 depoimentos foram transcritos exatamente dos prints do Google (inclusive os cortes "…" e a grafia original dos nomes), e as
miniaturas `img/depo-1..5.webp` são as fotos recortadas desses prints. Troca sozinho a cada 7 s, pausa com o mouse em cima,
e aceita clique nas fotos e arraste no celular. Os prints `avaliacao-1..5.webp` continuam na pasta, mas não são mais usados na página.

## Imagens do cliente (15/09/2026)
- Etapas: `etapa-01..04.webp` (fotos do cliente, reduzidas para ~800 px; os blocos lilás saíram).
- Serviços, linha Dermatologia: `servicos-dermatologia.webp` (o arquivo enviado tinha "ç" no nome e 6000 px; foi renomeado e reduzido para 800 px).
- `destaque-exames.webp` (filhote de gato em consulta), `card-caes.webp` e `card-gatos.webp` substituídos pelo cliente; os cards foram reduzidos para 1000 px.
- Os originais em alta ficaram guardados fora da pasta publicada.

## Imagem do hero (15/09/2026)
O golden foi trocado pela imagem nova do cliente ("hero novo.png", cachorro branco recortado, 2,2 MB).
Ela foi convertida em AVIF (principal) com WebP de reserva, em duas larguras:
`hero-pet-1200.avif` (53 KB) / `hero-pet-1200.webp` (132 KB) no desktop e `hero-pet-720.avif` (22 KB) / `hero-pet-720.webp` (36 KB) no celular.
O PNG original e o golden antigo ficaram guardados fora da pasta publicada.

## Depoimentos revertidos (16/09/2026)
O usuário não gostou do layout novo de depoimentos: a dobra voltou a ser o carrossel contínuo com os 5 prints reais do Google
(`avaliacao-1..5.webp`), como estava antes. As miniaturas recortadas (`depo-1..5.webp`) saíram da pasta.

## Rodapé removido e cards novos (16/09/2026)
- O rodapé saiu a pedido do usuário; a página termina no card de contato (com respiro embaixo para o botão flutuante).
- `card-caes.webp` (rottweiler, 1000 px) e `card-gatos.webp` (gato cinza, vertical 900 x 1350) foram trocados pelo cliente e recomprimidos;
  o gato usa enquadramento no alto (`object-position: 50% 8%`). Os originais ficaram fora da pasta publicada.

## Blocos abaixo do hero (16/09/2026)
Os 3 cards brancos (#1 #2 #3) viraram um "bento" nas cores da logo: roxo com a nota 4,9/5 e estrelas, amarelo com
"Veterinário dermatologista" e preto pontilhado (textura de mapa) com "Rudge Ramos", que leva ao mapa do contato.
Desktop: 3 lado a lado. Celular: 2 em cima e o de localização embaixo; abaixo de 372 px os três empilham.
