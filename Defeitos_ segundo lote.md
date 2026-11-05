Você vai escrever defeitos para um estudo sobre testes automatizados de áudio no tapSynth. Siga o guia do autor de defeitos:
https://claude.ai/artifact/UjaHLLNfWt2TAvmLonCqCo

Todas as regras do guia continuam valendo, em especial as regras de isolamento: trabalhe só neste repositório, não procure o repositório original do estudo nem outras cópias do tapSynth, não escreva nem rode testes, validadores ou medições de áudio, e não escolha, descarte nem ajuste um defeito por ele ser fácil ou difícil de perceber.

ADENDO: ESTE É O SEGUNDO LOTE

Estas regras substituem as do guia onde divergirem:

1. Identificadores: comece em F12 (F12, F13, ...). Os ids F01 a F11 já existem.
2. Quantidade: meta de 40 defeitos (no lugar de 10 a 15). Se não encontrar 40 bugs reais com equivalente no tapSynth, entregue os que encontrar e diga quantos faltaram. Não force adaptações para chegar a 40. Pode trabalhar em várias etapas; não pare de procurar só porque as primeiras fontes se esgotaram.
3. Não escreva alterações inofensivas (H) neste lote.
4. Não use estas correções, já usadas no primeiro lote. Outros commits dos mesmos projetos podem ser usados.
- https://github.com/TheWaveWarden/odin2/commit/8cd9fa4002548b9095531ba49757b9f9d33eee28
- https://github.com/juce-framework/JUCE/commit/3a2be25b9b404cb6941ab06c2b035e7001951bf1
- https://github.com/juce-framework/JUCE/commit/088dd14037cb571ba4f08dcf0fd05a1c754ade68
- https://github.com/juce-framework/JUCE/commit/dd9802e265fc9e90f8bd7b2bc3a7160b69111508
- https://github.com/sweetorange1/Organic-Chemistry/commit/ddbe96c95f11ea63a27a3655efa1f765db7ab80a
- https://github.com/asb2m10/dexed/commit/a428fe8a51edc23cca33ac42b410a9c470031576
- https://github.com/juce-framework/JUCE/commit/a933d7c4d0a9979de941475b02892b1c756e25e1
- https://github.com/juce-framework/JUCE/commit/7273838d8db2ff60b6112fda9f15bc19368629b9
- https://github.com/juce-framework/JUCE/commit/3262a3c5480dbefdc09776c805e18e23e9abe806
- https://github.com/juce-framework/JUCE/commit/9a130f2810284cfee42a2f81c926303b152e4af5
- https://github.com/diamondjirapat/LufsNormalizer/commit/8d38625b518ebf3c642c07904a68deadeebdbac9
5. Fontes ampliadas: além do JUCE e de plugins feitos com JUCE, vale a correção publicada de qualquer software de áudio open source em C ou C++ (plugins, sintetizadores, bibliotecas de DSP, frameworks de áudio), desde que o bug tenha equivalente no código do tapSynth ou nas classes do JUCE que ele usa. Continua valendo: todo defeito reintroduz uma correção real, e todo link de fonte foi aberto por você e mostra a correção. A coluna "origem" continua dizendo onde o patch se aplica (projeto ou juce), não de onde veio o bug.
6. Cobertura: como no guia, pelo menos um defeito por categoria e as duas origens (projeto e JUCE) representadas.
7. Entrega: os patches (experiment/faults/F12-....patch etc.) e as linhas novas do INDEX.md, no mesmo formato do guia (id, categoria, origem, arquivo alvo, fonte). No relatório final, diga quantos patches entregou, quais bugs encontrou e deixou de fora (e por quê), e qualquer adaptação que se afastou do bug original.

Antes de entregar, confira a lista do guia: todo patch tem o cabeçalho completo, todo link de fonte foi aberto por você e mostra a correção descrita, todo patch aplica sozinho sobre o código limpo e o plugin compila, e nenhum teste, validador ou medição de áudio foi usado.
