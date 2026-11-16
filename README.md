# Robô caixa fixa

Novo projeto de robô de mesa com uma única placa controladora e rosto na tela, derivado do cubo de robos-impressos.

Estado: primeiro estudo mecânico gerado e conferido por geometria. Duas peças para sustentar o módulo completo; sem firmware, fatiamento ou teste físico. STL de estudo, ainda não liberados para impressão final.

## Escopo pedido

- Caixa/cabeça fixa, sem rodas e sem movimento do pescoço.
- Uma única placa no robô: ESP32-S3 com LCD de 1,54 polegadas, do anúncio AliExpress 1005011874532154, escolhido pelo Nei. Sem Raspberry Pi nem Arduino auxiliar.
- Reaproveitar o que for útil do cubo original, redesenhando a fixação e o interior para a placa escolhida.

O foco atual é exclusivamente físico. Há opções com/sem bateria e com/sem toque; o suporte deve preservar acesso a USB, áudio, botões e frente. IA pelo computador ou direto por API fica para o software depois. Nenhuma API externa foi autorizada.

Veja [DEFINICAO.md](DEFINICAO.md) e [referencias/proveniencia.json](referencias/proveniencia.json).

Os STL em referencias/ pertencem à cabeça móvel original. Servem para estudar formato e medidas; não imprimir como se fossem a versão fixa.

## Primeiro desenho

[Projeto físico](PROJETO-FISICO.md) · [Prancha](estudo/prancha-ESTUDO.png) · [Montagem 3D](estudo/montagem-ESTUDO.glb) · [Verificação](estudo/verificacao.json)
