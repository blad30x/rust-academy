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

## Próximos Passos

1. [Configure seu ambiente de desenvolvimento](../02-ambiente-de-desenvolvimento/README.md) (VS Code, IntelliJ, etc.)
3. [Instale a extensão rust-analyzer](../02-ambiente-de-desenvolvimento/README.md)
