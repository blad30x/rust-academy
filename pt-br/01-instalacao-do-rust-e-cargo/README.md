# Instalação do Rust e Cargo

## Instalando o Rust

Para instalar o Rust, você pode usar o rustup, o instalador oficial da linguagem.

### No macOS e Linux

Abra o terminal e execute o seguinte comando:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### No Windows

1. Baixe o instalador do rustup em: https://rustup.rs/
2. Execute o arquivo baixado (rustup-init.exe)
3. Siga as instruções do instalador
4. Você precisará ter o [Microsoft C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/) instalado

## Verificando a Instalação

Após a instalação, abra um novo terminal e verifique se o Rust foi instalado corretamente:

```bash
rustc --version
cargo --version
```

## O que é o Cargo?

Cargo é o gerenciador de pacotes do Rust. Ele é instalado automaticamente junto com o Rust e permite:
- Criar novos projetos
- Gerenciar dependências
- Compilar projetos
- Executar testes
- Gerar documentação

## Comandos Básicos do Cargo

- Criar novo projeto: `cargo new nome_do_projeto`
- Compilar: `cargo build`
- Executar: `cargo run`
- Verificar se compila: `cargo check`

## Criando seu Primeiro Projeto

1. Crie um novo projeto:
```bash
cargo new hello_world
cd hello_world
```

2. O Cargo já cria um programa "Hello, World!" em `src/main.rs`
3. Execute o projeto:
```bash
cargo run
```

## Próximos Passos

1. Configure seu editor de código (VS Code, IntelliJ, etc.)
2. Instale a extensão rust-analyzer
3. Comece a estudar a sintaxe básica do Rust
4. Pratique criando pequenos programas 