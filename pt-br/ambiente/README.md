# Configurando o Ambiente de Desenvolvimento para Rust

## Escolhendo um Editor de Código

### Cursor (Recomendado)
1. Instale o Cursor em https://cursor.com
2. Instale as extensões essenciais:
   - rust-analyzer: Suporte completo à linguagem Rust
   - CodeLLDB: Depurador para Rust
   - Even Better TOML: Suporte para arquivos TOML
   - crates: Gerenciador de dependências visual

## Configurando o rust-analyzer

O rust-analyzer é a ferramenta mais importante para desenvolvimento em Rust. Ele oferece:
- Autocompletar código
- Ir para definição
- Encontrar referências
- Diagnósticos em tempo real
- Refatoração de código
- Formatação automática

### Configurações Recomendadas (Cursor)
```json
{
    "rust-analyzer.checkOnSave.command": "clippy",
    "rust-analyzer.inlayHints.enable": true,
    "rust-analyzer.inlayHints.typeHints": true,
    "rust-analyzer.inlayHints.parameterHints": true
}
```

## Ferramentas Adicionais

### Rustfmt
Formatador de código oficial do Rust:
```bash
rustup component add rustfmt
```
Uso: `cargo fmt`

### Clippy
Linter para Rust com análise estática de código:
```bash
rustup component add clippy
```
Uso: `cargo clippy`

### LLDB
Depurador para Rust:
```bash
# macOS
brew install lldb

# Ubuntu/Debian
sudo apt-get install lldb
```

## Próximos Passos

1. [Primeiro Projeto](../03-primeiro-projeto/README.md)
