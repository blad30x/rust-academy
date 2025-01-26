# Strings em Rust 🦀

Rust tem dois tipos principais de strings:
- `String`: tipo dinâmico, pode ser modificado
- `&str`: fatia de string, imutável e tamanho fixo

## String Literal (&str)

```rust
fn main() {
    // String literal (str)
    let texto: &str = "Olá, Rust!";
    
    // Múltiplas linhas
    let poema = "Rust é veloz,
                 Seguro e divertido,
                 Código feliz.";
    
    // Caracteres especiais
    let caminho = "C:\\Program Files\\Rust";
    let raw_string = r"C:\Program Files\Rust"; // String crua (raw)
    
    // Unicode
    let emoji = "🦀";
    let portugues = "Olá, món∂o!";
}
```

## String Dinâmica (String)

```rust
fn main() {
    // Criando String vazia
    let mut s = String::new();
    
    // De literal
    let s = String::from("Olá");
    let s = "Olá".to_string();
    
    // Modificando
    let mut s = String::from("Olá");
    s.push_str(", Mundo!"); // Adiciona string
    s.push('!');           // Adiciona caractere
    
    // Concatenação
    let s1 = String::from("Olá, ");
    let s2 = String::from("Mundo!");
    let s3 = s1 + &s2; // s1 foi movida aqui
}
```

## Operações com Strings

### Concatenação e Formatação
```rust
fn main() {
    // Usando format!
    let nome = "Rust";
    let saudacao = format!("Olá, {}!", nome);
    
    // Concatenação com +
    let s1 = "Olá".to_string();
    let s2 = ", ".to_string();
    let s3 = "Mundo!".to_string();
    let mensagem = s1 + &s2 + &s3;
    
    // Usando push_str
    let mut mensagem = String::from("Olá");
    mensagem.push_str(", ");
    mensagem.push_str("Mundo!");
}
```

### Fatiamento e Indexação
```rust
fn main() {
    let texto = String::from("Rust é incrível!");
    
    // Fatiamento
    let rust = &texto[0..4];
    let incrivel = &texto[7..];
    
    // Iterando sobre caracteres
    for c in texto.chars() {
        println!("{}", c);
    }
    
    // Iterando sobre bytes
    for b in texto.bytes() {
        println!("{}", b);
    }
}
```

### Métodos Úteis
```rust
fn main() {
    let texto = String::from("  Rust é Incrível!  ");
    
    // Remoção de espaços
    let limpo = texto.trim();
    
    // Substituição
    let novo = texto.replace("Rust", "Rust🦀");
    
    // Divisão
    let palavras: Vec<&str> = texto.split_whitespace().collect();
    
    // Verificações
    let contem = texto.contains("Rust");
    let comeca = texto.starts_with(" ");
    let termina = texto.ends_with("!");
}
```

## Exercícios Práticos

1. Crie uma função que inverta uma string
2. Implemente um contador de palavras
3. Faça um programa que verifique se uma string é um palíndromo

## Dicas

1. Use `String` quando precisar modificar o texto
2. Use `&str` para referências a strings
3. Cuidado com caracteres Unicode ao fatiar strings
4. Prefira `format!` para concatenações complexas

---

| [⬅️ Números de Ponto Flutuante](../flutuantes/README.md) | [Variáveis e Controle de Fluxo ➡️](../../variaveis-controle/README.md) |
|:-----------------------------------------------------|--------------------------------------------------------------------:| 