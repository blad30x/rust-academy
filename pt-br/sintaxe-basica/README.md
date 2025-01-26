# Sintaxe Básica do Rust 🦀

## Variáveis e Tipos

### Declaração de Variáveis
```rust
// Variável imutável (padrão)
let x = 5;

// Variável mutável
let mut y = 10;

// Constante
const MAX_POINTS: u32 = 100_000;
```

### Tipos Básicos
```rust
// Inteiros
let i: i32 = 42;        // com sinal, 32 bits
let u: u64 = 42;        // sem sinal, 64 bits

// Ponto flutuante
let f: f64 = 3.14;      // 64 bits

// Booleano
let ativo: bool = true;

// Caractere
let letra: char = 'a';  // Unicode

// String
let texto: String = String::from("Olá, Rust!");
let slice: &str = "Olá!";
```

## Estruturas de Controle

### Condicionais
```rust
let numero = 7;

if numero < 5 {
    println!("número é menor que 5");
} else if numero > 5 {
    println!("número é maior que 5");
} else {
    println!("número é igual a 5");
}
```

### Loops
```rust
// loop infinito
loop {
    println!("para sempre!");
    break; // sai do loop
}

// while
let mut n = 0;
while n < 5 {
    println!("n = {}", n);
    n += 1;
}

// for
for i in 0..5 {
    println!("i = {}", i);
}
```

## Funções

```rust
// Função simples
fn saudacao(nome: &str) {
    println!("Olá, {}!", nome);
}

// Função com retorno
fn soma(a: i32, b: i32) -> i32 {
    a + b  // retorno implícito (sem ponto-e-vírgula)
}

// Função com múltiplos retornos usando tupla
fn minmax(lista: &[i32]) -> (i32, i32) {
    let min = *lista.iter().min().unwrap();
    let max = *lista.iter().max().unwrap();
    (min, max)
}
```

## Exercícios Práticos

1. Crie uma função que receba uma temperatura em Celsius e retorne em Fahrenheit
2. Implemente um programa que conte quantas vogais existem em uma string
3. Faça uma função que calcule o n-ésimo número da sequência de Fibonacci

## Dicas Importantes

1. Rust é uma linguagem fortemente tipada, mas possui inferência de tipos
2. Por padrão, variáveis são imutáveis (use `mut` para torná-las mutáveis)
3. Funções podem retornar valores de forma implícita (última expressão)
4. O compilador do Rust é seu amigo: preste atenção nas mensagens de erro!

---

| [⬅️ Primeiro Projeto](../primeiro-projeto/README.md) | [Tipos de Dados ➡️](../tipos-de-dados/README.md) |
|:------------------------------------------------|----------------------------------------------:| 