# Primeiro Projeto em Rust

## Criando um Novo Projeto

Para criar um novo projeto em Rust, use o comando:
```bash
cargo new hello_world
cd hello_world
```

Este comando cria a seguinte estrutura:
```
hello_world/
├── Cargo.toml
└── src/
    └── main.rs
```

### Entendendo a Estrutura

1. `Cargo.toml`: O manifesto do projeto
```toml
[package]
name = "hello_world"
version = "0.1.0"
edition = "2021"

[dependencies]
```

2. `src/main.rs`: O código fonte principal
```rust
fn main() {
    println!("Hello, World!");
}
```

## Comandos Básicos do Cargo

1. Compilar o projeto:
```bash
cargo build
```

2. Executar o projeto:
```bash
cargo run
```

3. Verificar se compila (mais rápido que build):
```bash
cargo check
```

## Melhorando o Hello World

Vamos fazer algumas modificações para explorar mais funcionalidades:

```rust
// Definindo uma função para cumprimentar
fn cumprimentar(nome: &str) {
    println!("Olá, {}!", nome);
}

fn main() {
    // Variável com seu nome
    let nome = "Desenvolvedor Rust";
    
    // Chamando a função
    cumprimentar(nome);
    
    // Usando formatação de strings
    println!("Bem-vindo ao mundo do {}!", "Rust");
    
    // Múltiplas linhas
    println!("Algumas coisas que você vai aprender:
    1. Sintaxe da linguagem
    2. Gerenciamento de memória
    3. Programação segura
    4. E muito mais!");
}
```

## Adicionando uma Dependência

Vamos adicionar cor ao nosso output. Edite o `Cargo.toml`:
```toml
[package]
name = "hello_world"
version = "0.1.0"
edition = "2021"

[dependencies]
colored = "2.0"
```

Agora modifique `src/main.rs`:
```rust
use colored::*;

fn main() {
    println!("{}", "Olá, Mundo Colorido!".green().bold());
    println!("{}", "Rust é {}!".blue().bold(), "incrível".red());
}
```

## Dicas de Desenvolvimento

1. Use `cargo doc --open` para ver a documentação das dependências
2. Experimente o autocompletar do rust-analyzer
3. Use `cargo fmt` para formatar o código
4. Execute `cargo clippy` para ver sugestões de melhorias

## Próximos Passos

Sintaxe básica
