# Blog Smart Care

Blog comunitário em Jekyll para técnicos, entusiastas e curiosos trocarem dicas, soluções e experiências sobre computadores e softwares. Não é uma página de oferta de serviços.

- Instagram oficial: [@smartcare.campinas](https://www.instagram.com/smartcare.campinas/)
- WhatsApp da comunidade: [conversar pelo WhatsApp](https://wa.me/5519981821478)

## Executar localmente

Requisitos: Ruby e Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Abra http://localhost:4000/smart-care-blog/.

## Publicar no GitHub Pages

1. Crie um repositório chamado `smart-care-blog` e envie os arquivos deste diretório para a raiz da branch `main`.
2. Em **Settings → Pages**, escolha **Deploy from a branch**, branch `main` e pasta `/(root)`.
3. O endereço será `https://wagnersdoliveira.github.io/smart-care-blog/`.
4. Se o nome do repositório ou usuário for diferente, atualize `baseurl` e `url` em `_config.yml`.

Os posts ficam em `_posts/`, com nomes no formato `AAAA-MM-DD-titulo.md`. Use os posts existentes como modelo.

## Imagens

As fotos `computer-repair.jpg` e `laptop-maintenance.jpg` vêm do Wikimedia Commons e estão sob licença [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Os créditos e links para as páginas originais aparecem junto às imagens no site:

- [Computer repair in progress](https://commons.wikimedia.org/wiki/File:Computer_repair_in_progress.jpg), por Vintechcomputerservices.
- [Laptop Maintenance Work Area](https://commons.wikimedia.org/wiki/File:Laptop_Maintenance_Work_Area.jpg), por Giorgio Malvone.
