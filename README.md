# Beyond Masterclass — Página de obrigado

Página estática da Masterclass Arquitetura do Sucesso™, preparada para publicação na Vercel.

## Estrutura

- `index.html` — página completa, incluindo a visualização de obrigado e o formulário de inscrição.
- `vercel.json` — headers de segurança e URLs limpas.

## Configuração antes da publicação

No fim de `index.html`, no objeto `CONFIG`, substitua os valores vazios pelos endereços oficiais:

```js
const CONFIG = {
  webhookUrl: 'https://seu-webhook.example/lead',
  grupoVipUrl: 'https://chat.whatsapp.com/seu-convite'
};
```

`webhookUrl` deve aceitar `POST` com JSON e permitir CORS a partir do domínio publicado. `grupoVipUrl` deve ser o convite HTTPS oficial do Grupo VIP. Não coloque tokens, chaves privadas ou credenciais neste ficheiro.

A página abre inicialmente no modo visual de obrigado. Para voltar ao fluxo de inscrição, use o botão “Voltar à inscrição”. O parâmetro `?preview=obrigado` é mantido como referência de pré-visualização.

## Deploy na Vercel

1. Importe este repositório na Vercel.
2. Escolha **Other** como Framework Preset.
3. Deixe o Root Directory como a raiz do repositório.
4. Não é necessário Build Command nem Output Directory.
5. Faça o deploy.

Como o projeto é HTML/CSS/JavaScript puro, a Vercel pode servi-lo sem build. Depois de configurar os dois URLs no `index.html`, faça um novo commit e redeploy.
