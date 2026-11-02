# AFONSO APPS 1.0

Portal estático e responsivo para os aplicativos Afonso, com cinco projetos, páginas individuais, catálogo com filtros, notícias e tema claro/escuro.

## Como abrir

Abra `index.html` em um navegador moderno. Para testar com servidor local, execute na pasta do projeto:

```bash
python -m http.server 8000
```

Depois acesse `http://localhost:8000`.

## Publicar gratuitamente no GitHub Pages

1. Crie um repositório novo, por exemplo `afonso-apps`.
2. Envie **o conteúdo desta pasta** para a raiz do repositório (index.html e pasta assets).
3. Em Settings > Pages, selecione Deploy from a branch, `main`, `/ (root)` e salve.
4. Aguarde a implantação. O endereço esperado terá o formato `https://SEU-USUARIO.github.io/afonso-apps/` (o endereço real depende do repositório).
5. As rotas usam `#/` para funcionar em hospedagem estática, inclusive ao atualizar a página.

## Downloads oficiais

**Não há APK ou instalador incluído neste ZIP.** O Afonso Downloader Mobile 1.0.12+13 é um candidato a lançamento; os demais projetos não receberam links de download não verificados.

Quando o APK estiver pronto para distribuição:

1. Revise requisitos, permissões, privacidade e compatibilidade com dispositivos reais.
2. Hospede o APK assinado original em uma fonte confiável (por exemplo, GitHub Releases).
3. Confirme tamanho e SHA-256 do arquivo.
4. Atualize o objeto correspondente no arquivo `assets/app.js` e substitua o botão de download desabilitado por um link real para o APK verificado. Não invente URLs.
5. Registre a versão e a data de lançamento nas atualizações.

## Personalização

- Conteúdo e aplicativos: `assets/app.js` (array `apps`).
- Visual: `assets/styles.css`.
- Cabeçalho, rodapé e metadados: `index.html`.
- Ícone: `assets/favicon.svg`.

## Observações

- A fonte é obtida do Google Fonts; caso esteja offline, o site utiliza fontes locais do sistema.
- A política de privacidade é preliminar e deve ser revisada antes da publicação oficial.
- A disponibilidade do TikTok no aplicativo Android não foi anunciada como confirmada.
- O projeto não altera nenhum aplicativo ou repositório existente.


## Versão 1.1 — novidades
- Central de downloads com estados de disponibilidade.
- Página ampliada do Afonso Downloader Android (1.0.12+13).
- Guia de instalação e atualização no Android.
- Espaços ilustrativos claramente identificados, para substituir por capturas reais.
- Mantido o design preto/roxo e a navegação do site 1.0.

### Como ativar o download oficial
O APK **não está incluído** neste ZIP. Para publicar:
1. Faça uma cópia do APK **release ARM64 original**, assinado e verificado.
2. Hospede-o em uma URL HTTPS estável (ex.: GitHub Releases do projeto).
3. Calcule o SHA-256 do APK no Windows com `certutil -hashfile arquivo.apk SHA256`.
4. Edite `assets/app.js`, no objeto `releaseAndroid` no início do arquivo:
   - `filename`: nome real do arquivo;
   - `url`: URL HTTPS real do APK;
   - `sha256`: hash de 64 caracteres;
   - `size`: tamanho real (opcional);
   - `minimumAndroid`: versão mínima confirmada (opcional);
   - `published`: `true` somente depois da revisão de distribuição.
5. Confira o download em um dispositivo real antes de publicar o site.

**Nunca** inclua arquivos .jks, key.properties ou senhas de assinatura no repositório público.

### Capturas de tela
Os três cartões visuais são apenas ilustrações. Não são screenshots reais.
Substitua-os somente após receber imagens autorizadas do aplicativo.


## Versão 1.2 — APK incluído
- APK: `downloads/AfonsoDownloaderMobile-2.3-arm64.apk`
- Tamanho: 20,824,659 bytes (20.82 MB)
- SHA-256: `1e6a8fe4951f9c8a84e1ca12b15f78c58d1f41d5cbc8c7c00deabda22dcd9306`
- O botão de download aponta para o APK local do site e funciona após publicação em hospedagem estática que suporte arquivos APK.
- Não foi feita publicação na internet nem alterado o APK original.
- Confirme em aparelhos reais a instalação, a assinatura, as permissões e o comportamento do app antes de divulgação pública.
- TikTok continua indicado como indisponível na base atual, não anunciar suporte sem validação.
- Para testar localmente, abra `index.html` e acesse a página do Afonso Downloader. Caso o navegador restrinja downloads via `file://`, rode `python -m http.server 8000` nesta pasta e acesse `http://localhost:8000`.
- Para GitHub Pages, mantenha `index.html`, `assets/` e `downloads/` juntos na raiz de publicação; evite subir chaves privadas.
