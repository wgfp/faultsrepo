# tapSynth

Sintetizador subtrativo em JUCE 8.0.9 (VST3; AU no macOS) com um recurso de IA que transforma uma descrição de timbre em parâmetros do plugin.

Esta é uma cópia de trabalho do tapSynth usada para preparar os defeitos de um estudo de TCC sobre testes automatizados de áudio em plugins. Os testes do estudo não fazem parte desta cópia, de propósito.

## Créditos

- **Tutorial original:** tapSynth, de The Audio Programmer (Joshua Hodge, 2021), <https://github.com/TheAudioProgrammer/tapSynth>. Os cabeçalhos em `Source/Data/` vêm desse tutorial.
- **Extensões:** FM, modulação do filtro, nova interface e o recurso de IA, por _[nome do colega]_.
- **Estudo de testes:** testes, pipeline e avaliação, por _[seu nome]_ (TCC, _[instituição]_).
- **Defeitos:** preparados com um agente de IA sem acesso aos testes, a partir de correções reais em plugins JUCE open source, e revisados por _[seu nome]_.

## Compilar

Requer CMake 3.22+ e um compilador C++17. O JUCE é baixado na configuração (use `-DTAPSYNTH_JUCE_DIR=/caminho/para/JUCE` para uma cópia local).

```bash
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Release
cmake --build build
```

O VST3 fica em `build/tapSynth_artefacts/Release/VST3/`. No Linux, as dependências estão em `.github/workflows/build.yml`.

## Defeitos

O trabalho desta cópia segue `GUIA_DEFEITOS.md`. Cada defeito é um patch em `experiment/faults/` e cada alteração inofensiva é um patch em `experiment/harmless/`, sempre sobre o código limpo. O código em `Source/` não é alterado nos commits.

Para defeitos no código do JUCE, clone o JUCE 8.0.9 e compile apontando para ele:

```bash
git clone --branch 8.0.9 --depth 1 https://github.com/juce-framework/JUCE.git tools/JUCE
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Release -DTAPSYNTH_JUCE_DIR=tools/JUCE
```

## Recurso de IA

Defina a variável de ambiente `GEMINI_API_KEY` antes de abrir o host. A chave nunca é gravada no repositório.

## Licença

_Pendente._ O repositório do tutorial original não declara licença, e o JUCE 8 é distribuído sob AGPLv3 ou licença comercial.
