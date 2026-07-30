# Doce Acaso RS — PDV (versão instalável / PWA)

Este pacote transforma o PDV num app que se instala no **Chrome do Android** com ícone
na tela inicial, tela cheia (sem barra do navegador) e funcionamento offline.

## Arquivos
- `index.html` — o app inteiro (PDV, produtos, clientes, tabela de preços, vendas, exportar Excel)
- `manifest.json` — configura nome, ícone e modo "standalone" do app
- `sw.js` — service worker (cache offline)
- `icon-192.png` / `icon-512.png` — ícone do app

## Por que precisa hospedar online
O Chrome só oferece a opção "Instalar app" quando o site é servido via **HTTPS**
(abrir o `index.html` direto do celular, tipo arquivo local, não ativa o botão de instalar).
A boa notícia: hospedar é grátis e leva 2 minutos.

## Passo a passo — GitHub Pages (recomendado, grátis)
1. Crie uma conta em github.com (se ainda não tiver).
2. Crie um repositório novo, público, ex: `doce-acaso-rs`.
3. Faça upload dos 5 arquivos deste pacote (arraste e solte na página do repositório, "Add file → Upload files").
4. Vá em **Settings → Pages**, em "Source" escolha a branch `main` e pasta `/ (root)`, salve.
5. Em 1–2 minutos seu app estará em algo como:
   `https://SEU-USUARIO.github.io/doce-acaso-rs/`

## Passo a passo — Netlify (alternativa, ainda mais rápido)
1. Acesse app.netlify.com/drop
2. Arraste a pasta com os 5 arquivos direto no navegador
3. Pronto — Netlify te dá um link `https://algumnome.netlify.app` já em HTTPS

## Instalando no Android
1. No celular Android, abra o link (GitHub Pages ou Netlify) no **Chrome**.
2. Toque nos três pontinhos (⋮) no canto superior direito.
3. Toque em **"Instalar app"** (ou "Adicionar à tela inicial").
4. O ícone "Doce Acaso RS" aparece na tela inicial e abre em tela cheia, como um app nativo.

## Sobre gerar um .apk de verdade
Se além do PWA você quiser um arquivo `.apk` para instalar manualmente ou publicar na
Play Store, depois de hospedar o site você pode usar o **PWABuilder** (gratuito):
1. Acesse https://www.pwabuilder.com
2. Cole a URL do seu site hospedado (GitHub Pages/Netlify)
3. Clique em "Package for stores" → Android → baixa um `.apk`/`.aab` pronto

## Sobre os dados
Os dados (produtos, clientes, vendas) ficam salvos no armazenamento local do navegador
do próprio celular. Se limpar os dados do Chrome ou trocar de aparelho, os dados não
acompanham — use o botão "Baixar Planilha Excel" com frequência para manter backup.
