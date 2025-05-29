# 🔧 JavaScript + WebAssembly

Este repositório demonstra como integrar código C com WebAssembly (WASM) em uma aplicação web simples utilizando JavaScript.

---

## 📦 Sobre o projeto

A proposta aqui é mostrar como compilar uma função escrita em C para WebAssembly e utilizá-la dentro de um HTML/JS. Neste exemplo, utilizamos uma função simples `sum(a, b)` que retorna a soma de dois números.

---

## 🚀 Pré-requisitos

Antes de tudo, é necessário ter o [Emscripten SDK (emcc)](https://emscripten.org/docs/getting_started/downloads.html) instalado na sua máquina.

### Passos para instalar (Windows + Git Bash):

```bash
git clone https://github.com/emscripten-core/emsdk.git
cd emsdk
./emsdk install latest
./emsdk activate latest
source ./emsdk_env.sh
```

## 📥 Clonando o repositório

```bash
git clone https://github.com/IGBxDev/javascript-webassembly.git
cd javascript-webassembly
```

## 🛠️ Compilando o código C para WebAssembly

```bash
int sum(int a, int b) {
  return a + b;
}
```

Comando para compilar:

```bash
emcc sum.c -Os -o sum.html
```

## 🌐 Executando no navegador

Abra o arquivo index.html em um navegador moderno:

```bash
# Em sistemas com Python instalado
python3 -m http.server
```
Acesse: http://localhost:8000

O navegador irá carregar o arquivo .wasm e executar a função sum.

## 📁 Estrutura do projeto


```bash
javascript-webassembly/
├── sum.c             # Código C com função a ser compilada
├── sum.wasm          # Arquivo gerado via emcc
├── index.html        # HTML com JS que consome o WASM
└── README.md
```





