# Robô caixa fixa

[![Robô caixa fixa](guia/assets/banner.jpg)](https://inematds.github.io/robo-caixa-fixa/guia/)

**[Português](README.md) · [English](README.en.md) · [Español](README.es.md)**

## O que é

Quem quer um robô de mesa costuma esbarrar na parte mecânica: servos, engrenagens e fios. O Robô caixa fixa é um suporte impresso em 3D que transforma o módulo Waveshare ESP32-S3 com tela de 1,54 polegadas numa cabeça fixa sobre uma base. O módulo fica inteiro, com carcaça e eletrônica de fábrica. Você precisa de uma impressora 3D, do Bambu Studio, de filamento, do módulo e de dois parafusos com porca. O desenho foi conferido no computador, mas ainda não foi impresso. O rosto na tela e a conversa por IA ainda não existem: este guia cobre só o suporte.

## Guia e downloads

**https://inematds.github.io/robo-caixa-fixa/guia/**

O guia tem os STL, pacote ZIP, montagem 3D, verificações e passo a passo de fatiamento para a A1. Comece pelo berço. Os arquivos são de estudo e ainda não foram validados fisicamente; não há G-code nem perfil 3MF validado.

## O processo, do início ao fim

Quem faz: 🧠 sessão com o Nei · ⚙️ script · 🤖 `claude -p`.

1. ⚙️ Gerar as peças e a verificação: `../robos-impressos/.venv/bin/python cad/gerar.py` (grava `estudo/`).
2. 🧠 Copiar STL, GLB e `verificacao.json` de `estudo/` para `guia/downloads/` e refazer o ZIP de teste, só quando a geometria mudar.
3. ⚙️ Exportar as peças montadas para o render: `../robos-impressos/.venv/bin/python scripts/exporta_partes.py <pasta>`.
4. ⚙️ Renderizar as imagens do guia no Blender (CPU, ~25 min): `blender -b -P scripts/render_guia.py -- <pasta> <saida>`; converter para `guia/assets/r-*.jpg` e `r-orto-*.webp`.
5. 🧠 Banners PT/EN/ES pelo Codex (`gerar-banner.sh` da skill projetos-landing-guia, estilos live e grade), com o render do conjunto como referência de forma; conferir o texto de cada um.
6. 🧠 Escrever o guia PT (`guia/index.html`); ⚙️ traduzir para `guia/en/` e `guia/es/` com `inema-traduz`.
7. 🤖 Revisor independente; conferir 360 px, imagens e visualizador 3D por HTTP local.
8. 🧠 OK do Nei, commit e push; o GitHub Pages publica sozinho.
9. 🧠 Teste físico do berço na A1 (pendente) antes de liberar STL finais.

## Arquivos do projeto

- [Projeto físico](PROJETO-FISICO.md).
- [Definição e variantes](DEFINICAO.md).
- [Gerador CAD](cad/gerar.py).
- [Verificação](estudo/verificacao.json).

Duas peças e dois parafusos M3 × 16 com porcas, a conferir na bancada. INEMA em relevo de 1,2 mm, engrossado e recuado 4 mm. Programa do rosto e IA ficam para uma etapa futura.

## Vídeo do projeto

https://www.youtube.com/watch?v=BEY94Ag9BWk
