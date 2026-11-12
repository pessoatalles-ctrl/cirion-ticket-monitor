# Cirion Ticket Monitor — GitHub Pages (demonstração)

Protótipo estático e **sem dados reais**. A página simula os alertas de inatividade (verde 20–24 min, amarelo 25–29 min, vermelho >=30 min), SLA acumulativo TPA 30 min, TPL 120 min, TPOS 240 min, e escalonamento após vencimento.

## Publicar sem instalar nada

1. No GitHub, crie um repositório **privado** para armazenar o código, caso a política corporativa permita. Atenção: **GitHub Pages pode tornar o site publicamente acessível, mesmo que o repositório seja privado**, conforme plano e configuração.
2. Faça upload do arquivo `index.html` e deste README pelo navegador (Add file → Upload files).
3. Em Settings → Pages, selecione **Deploy from a branch**, branch `main`, pasta `/(root)` e salve, **somente se a publicação pública deste protótipo fictício estiver autorizada**.
4. O endereço usual será `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

## Limites e segurança

- GitHub Pages hospeda arquivos estáticos, não roda FastAPI, SQLite, jobs agendados ou um conector autenticado.
- Não adicione senhas, cookies, tokens, HAR, JSON de tickets reais ou outros dados internos ao repositório ou ao site.
- O histórico do Uberall está em HTML no endpoint `Details/{id}`, mas acesso automatizado exige autenticação e autorização. A integração real requer um backend seguro aprovado pela Cirion.
- Os limites de TPA/TPL/TPOS são um fluxo de equipamento de 4h; o MTTR de fibra de 8h necessita detalhamento adicional.
- A demo usa minutos simulados. A futura versão real precisará distinguir o evento mais recente de eventos operacionais relevantes e considerar etapas concluídas e exceções contratuais.
