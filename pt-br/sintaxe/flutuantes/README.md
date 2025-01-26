# Números de Ponto Flutuante em Rust 🦀

## Tipos de Ponto Flutuante

Rust oferece dois tipos de números de ponto flutuante:

- `f32`: precisão simples (32 bits)
  - 7 dígitos decimais de precisão
  - Menor uso de memória
  - Mais rápido em algumas arquiteturas
  - Comum em gráficos/GPU

- `f64`: precisão dupla (64 bits) - **padrão**
  - 15 dígitos decimais de precisão
  - Maior precisão
  - Padrão quando não especificado
  - Recomendado para cálculos financeiros/científicos

## Declaração e Uso

```rust
fn main() {
    // Declaração explícita
    let pi: f64 = 3.14159265359;
    let e: f32 = 2.71828;
    
    // Inferência de tipo (f64 é o padrão)
    let temperatura = 27.5; // f64
    
    // Notação científica
    let milhao = 1e6; // 1_000_000.0
    let pequeno = 1e-6; // 0.000001
    
    // Separador _ para legibilidade
    let grande = 1_234_567.890_123;
}
```

## Operações Básicas

```rust
fn main() {
    let x = 2.0; // f64
    let y: f32 = 3.0; // f32
    
    // Operações básicas
    let soma = x + 1.0;
    let diferenca = x - 1.0;
    let produto = x * 2.0;
    let quociente = x / 2.0;
    
    // Funções matemáticas
    let raiz = x.sqrt();
    let potencia = x.powi(2); // Potência com expoente inteiro
    let potencia_float = x.powf(2.5); // Potência com expoente float
    let absoluto = (-x).abs();
    
    // Arredondamento
    let arredonda_cima = 3.7_f64.ceil(); // 4.0
    let arredonda_baixo = 3.7_f64.floor(); // 3.0
    let arredonda = 3.7_f64.round(); // 4.0
    let trunca = 3.7_f64.trunc(); // 3.0
}
```

## Precisão e Aritmética

### Cuidados com Precisão
```rust
fn main() {
    let resultado = 0.1 + 0.2;
    println!("{}", resultado); // 0.30000000000000004
    
    // Comparação com tolerância
    let x = 0.1 + 0.2;
    let y = 0.3;
    let eh_igual = (x - y).abs() < f64::EPSILON;
}
```

### Constantes Especiais
```rust
fn main() {
    let infinito = f64::INFINITY;
    let neg_infinito = f64::NEG_INFINITY;
    let nao_numero = f64::NAN;
    
    // Verificações
    assert!(infinito.is_infinite());
    assert!(nao_numero.is_nan());
}
```

## Exercícios Práticos

1. Crie uma função que calcule juros compostos
2. Implemente uma função que converta graus para radianos
3. Faça um programa que calcule a média de uma lista de notas

## Dicas

1. Use `f64` por padrão, a menos que tenha uma razão específica para usar `f32`
2. Cuidado com comparações de igualdade - use tolerância (epsilon)
3. Para cálculos financeiros, considere usar tipos decimais específicos
4. Lembre-se que operações entre `f32` e `f64` precisam de conversão explícita

---

| [⬅️ Números Inteiros](../inteiros/README.md) | [Strings ➡️](../strings/README.md) |
|:------------------------------------------|----------------------------------:| 