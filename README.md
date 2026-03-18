# Dra. Alessandra Miyake — Portal & Escritório Digital
**OAB/SP 433.727 · Homologação de Sentença Estrangeira · Atendimento 100% Online**

---

## ÍNDICE
1. [Estrutura dos arquivos](#estrutura)
2. [Publicar no Vercel](#vercel)
3. [Configurar Google Sheets](#sheets)
4. [Como enviar acesso ao cliente](#cliente)
5. [Atualizar os arquivos](#atualizar)
6. [Links após publicação](#links)
7. [Inventário completo de arquivos](#inventario)

---

## 1. ESTRUTURA DOS ARQUIVOS {#estrutura}

Organize os arquivos nesta estrutura antes de subir no Vercel:

```
portal-miyake/
│
├── index.html                  ← Portal do cliente (login por CPF)
├── dashboard.html              ← Dashboard do escritório
├── checklist.html              ← Checklist interativo de documentos
├── links-instagram.html        ← Bio link do Instagram
├── links-tiktok.html           ← Bio link do TikTok
├── proposta.html               ← Proposta visual interativa
│
└── README.md                   ← Este arquivo
```

**Como renomear:**

| Arquivo original              | Renomear para            |
|-------------------------------|--------------------------|
| portal_cliente_cpf.html       | index.html               |
| dashboard_conectado.html      | dashboard.html           |
| checklist_documentos.html     | checklist.html           |
| links_instagram.html          | links-instagram.html     |
| links_tiktok.html             | links-tiktok.html        |
| proposta_visual.html          | proposta.html            |

---

## 2. PUBLICAR NO VERCEL {#vercel}

### Opção A — Deploy direto (sem GitHub)

1. Acesse **vercel.com** e crie conta com Google
2. Clique em **Add New → Project**
3. Arraste a pasta `portal-miyake` completa
4. Clique em **Deploy**
5. Em 30 segundos o site está no ar

### Opção B — Via GitHub (recomendada)

> Permite atualizar os arquivos e publicar automaticamente

1. Crie conta em **github.com**
2. Crie repositório novo: `portal-miyake` (público ou privado)
3. Suba todos os arquivos para o repositório
4. No Vercel: **Add New → Project → Import Git Repository**
5. Selecione o repositório `portal-miyake`
6. Clique em **Deploy**

**Para atualizar depois:** edite o arquivo no GitHub → Vercel publica automaticamente em 30 segundos.

### Personalizar o domínio

1. No painel do Vercel: **Settings → Domains**
2. Digite o nome desejado: `alessandramiyake.vercel.app`
3. Clique em **Add** — gratuito, sem custo adicional

---

## 3. CONFIGURAR GOOGLE SHEETS {#sheets}

### Tornar a planilha pública (obrigatório)

1. Abra a planilha: `https://docs.google.com/spreadsheets/d/1OGQP1ZWvN9yQiBeVYP3FwUZN2iRN6sJdcARwiMuPqMA`
2. Clique em **Compartilhar** (canto superior direito)
3. Em "Acesso geral" → **Qualquer pessoa com o link**
4. Permissão: **Leitor**
5. Clique em **Copiar link** e feche

### Adicionar coluna CPF (obrigatório para o portal)

1. Abra a aba **CRM**
2. Adicione uma coluna chamada **CPF**
3. Preencha o CPF de cada cliente (somente números ou com pontuação — o portal aceita ambos)

### Estrutura esperada das abas

| Aba          | Conteúdo                                    |
|--------------|---------------------------------------------|
| Casos        | ID, Cliente, Categoria, Tipo, País, Status, Data, Honorários |
| Recebimentos | Cliente, Valor, Canal, Taxa, Líquido, Status, Parcela |
| Gastos       | Data, Categoria, Descrição, Valor, Status   |
| Horas        | Data, Processo/Cliente, Atividade, Início, Fim |
| CRM          | Nome, Email, Telefone, Origem, País, CPF, NPS |
| Financeiro   | Total Recebido, Total Gastos, Lucro         |
| Metas        | Mês, Meta de Faturamento, Meta de Casos     |

---

## 4. COMO ENVIAR ACESSO AO CLIENTE {#cliente}

### Mensagem WhatsApp — Portal do cliente

```
Oi [Nome]! 😊

Seu portal de acompanhamento do processo está disponível:
🔗 alessandramiyake.vercel.app

Para acessar, use seu CPF como senha.

Qualquer dúvida, é só me chamar!
```

### Mensagem WhatsApp — Checklist de documentos

```
Oi [Nome]! Segue a lista interativa com os documentos
que você precisa reunir para o seu caso:

🔗 alessandramiyake.vercel.app/checklist.html

Vai marcando conforme reunir. Qualquer dúvida, me chama! 🙂
```

---

## 5. ATUALIZAR OS ARQUIVOS {#atualizar}

### Se usou Opção A (sem GitHub)

1. Vercel → seu projeto → **Deployments**
2. Clique nos três pontos → **Redeploy** ou **Upload**
3. Arraste os arquivos atualizados

### Se usou Opção B (com GitHub)

1. Edite o arquivo no GitHub (botão de lápis)
2. Clique em **Commit changes**
3. O Vercel detecta automaticamente e publica em ~30 segundos

### Atualizar dados dos clientes

Basta editar a planilha Google Sheets normalmente.
O dashboard e o portal lêem os dados em tempo real — nenhuma ação adicional necessária.

---

## 6. LINKS APÓS PUBLICAÇÃO {#links}

| Página                | URL                                              | Quem acessa       |
|-----------------------|--------------------------------------------------|-------------------|
| Portal do cliente     | `alessandramiyake.vercel.app`                    | Clientes          |
| Dashboard escritório  | `alessandramiyake.vercel.app/dashboard.html`     | Somente você      |
| Checklist documentos  | `alessandramiyake.vercel.app/checklist.html`     | Clientes / leads  |
| Bio link Instagram    | `alessandramiyake.vercel.app/links-instagram.html` | Público          |
| Bio link TikTok       | `alessandramiyake.vercel.app/links-tiktok.html`  | Público           |
| Proposta visual       | `alessandramiyake.vercel.app/proposta.html`      | Leads / clientes  |

> ⚠️ O dashboard contém dados do escritório. Não divulgue o link publicamente.
> Para maior segurança, você pode adicionar uma senha simples no arquivo HTML do dashboard.

---

## 7. INVENTÁRIO COMPLETO DE ARQUIVOS {#inventario}

### Páginas Web (subir no Vercel)

| Arquivo                    | Descrição                                    |
|----------------------------|----------------------------------------------|
| portal_cliente_cpf.html    | Portal do cliente com login por CPF          |
| dashboard_conectado.html   | Dashboard do escritório (Google Sheets)      |
| checklist_documentos.html  | Checklist interativo por tipo de caso        |
| links_instagram.html       | Página de bio link do Instagram              |
| links_tiktok.html          | Página de bio link do TikTok                 |
| proposta_visual.html       | Proposta comercial visual interativa         |
| identidade_visual.html     | Guia completo de identidade visual           |

### Documentos Word (.docx)

| Arquivo                        | Descrição                                        |
|--------------------------------|--------------------------------------------------|
| proposta_comercial_v2.docx     | Proposta de honorários sem assinatura            |
| contrato_honorarios.docx       | Contrato completo com 8 cláusulas                |
| guia_completo_conteudo.docx    | 12 roteiros IG + 12 TikTok + 8 mensagens direct  |
| cronograma_formatos.docx       | 5 carrosséis + 4 quiz + 6 enquetes + cronograma  |
| roteiros_corrigidos_OAB.docx   | Roteiros revisados conforme Provimento 205/2021  |
| estrategia_tiktok.docx         | Estratégia TikTok completa                       |
| video_apresentacao.docx        | Roteiro do vídeo de apresentação (bio link)      |
| roteiro_onboarding.docx        | Reunião de onboarding pós-contrato (30 min)      |
| roteiro_conversa_inicial.docx  | Conversa inicial pré-proposta (30 min)           |
| fluxo_documentos.docx          | Fluxo completo de recebimento de documentos      |
| tipografia_juridica.docx       | Template de tipografia para documentos jurídicos |
| plano_conteudo_dralessandra.docx | Plano completo de conteúdo digital             |

### PDF

| Arquivo                    | Descrição                                    |
|----------------------------|----------------------------------------------|
| checklist_documentos.pdf   | Checklist para enviar pelo WhatsApp          |
| proposta_visual.pdf        | Proposta visual para enviar por e-mail       |

### Imagens

| Arquivo                    | Descrição                                    |
|----------------------------|----------------------------------------------|
| fundo_meet.png             | Fundo Google Meet — gradiente vinho/terracota|
| fundo_meet_homeoffice.png  | Fundo Google Meet — home office ilustrado    |
| papel_timbrado_lateral.png | Papel timbrado com faixa lateral vinho       |

### Logos e SVG

| Arquivo                        | Descrição                                |
|--------------------------------|------------------------------------------|
| logo_AM_organico_principal.svg | Logo AM principal com elementos orgânicos|
| logo_AM_organico_claro.svg     | Versão clara do logo                     |
| logo_AM_louro_principal.svg    | Logo com ramos de louro                  |
| logo_AM_horizontal.svg         | Logo versão horizontal                   |
| logo_nova_final.svg            | Logo final refinado                      |
| logo_cursiva_v2.html           | Logo com iniciais AM cursivas (HTML)     |
| logo_final.html                | Logo final completo (HTML)               |
| papel_timbrado.html            | Papel timbrado (HTML para edição)        |

---

## CONFIGURAÇÕES IMPORTANTES

### ID da planilha Google Sheets
```
1OGQP1ZWvN9yQiBeVYP3FwUZN2iRN6sJdcARwiMuPqMA
```

### Contato configurado nos arquivos
```
WhatsApp: 5511957221668
E-mail:   alessandrarmiyake@oabsp.adv.br
Instagram: @dralessandramiyake
OAB/SP:   433.727
```

### Nomes das abas esperados no Google Sheets
```
Casos · Recebimentos · Gastos · Horas · CRM · Financeiro · Metas
```

> Se os nomes das suas abas forem diferentes, acesse
> `alessandramiyake.vercel.app/dashboard.html` → aba ⚙️ Configurar
> e atualize os nomes antes de carregar os dados.

---

## SUPORTE E MANUTENÇÃO

- **Planilha:** edite normalmente no Google Sheets — os dashboards atualizam automaticamente
- **Portal:** clientes acessam com CPF cadastrado na aba CRM
- **Arquivos:** atualize no GitHub ou faça redeploy no Vercel
- **Novos clientes:** adicione na aba CRM com nome e CPF

---

*Dra. Alessandra Miyake · Advogada · OAB/SP 433.727*
*alessandrarmiyake@oabsp.adv.br · (11) 95722-1668 · @dralessandramiyake*
