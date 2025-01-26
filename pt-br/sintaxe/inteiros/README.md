# Tipos Numéricos em Rust 🦀

Rust oferece vários tipos numéricos que podem ser usados de acordo com sua necessidade. Vamos entender cada um deles e suas aplicações.

## Tipos de Números Inteiros

### Sem sinal (apenas números positivos)
- `u8`: 0 até 255
- `u16`: 0 até 65.535
- `u32`: 0 até 4.294.967.295
- `u64`: 0 até 18.446.744.073.709.551.615
- `u128`: 0 até 340.282.366.920.938.463.463.374.607.431.768.211.455

### Com sinal (números positivos e negativos)
- `i8`: -128 até 127
- `i16`: -32.768 até 32.767
- `i32`: -2.147.483.648 até 2.147.483.647 (padrão)
- `i64`: -9.223.372.036.854.775.808 até 9.223.372.036.854.775.807
- `i128`: -170.141.183.460.469.231.731.687.303.715.884.105.728 até 170.141.183.460.469.231.731.687.303.715.884.105.727

## Números de Ponto Flutuante
- `f32`: precisão simples (7 dígitos decimais)
- `f64`: precisão dupla (15 dígitos decimais) - padrão

## Declaração e Uso

```rust
fn main() {
    // Inteiros
    let idade: u8 = 25;                    // Sem sinal, 8 bits
    let população: u32 = 1_000_000;        // Underscore para legibilidade
    let saldo: i32 = -1_000;               // Com sinal, negativo
    
    // Ponto flutuante
    let pi: f64 = 3.14159265359;           // Precisão dupla
    let temperatura: f32 = 27.5;           // Precisão simples
    
    // Inferência de tipo
    let número = 42;                       // i32 por padrão
    let decimal = 10.5;                    // f64 por padrão
    
    // Operações básicas
    let soma = 5 + 10;                     // Adição
    let diferença = 95.5 - 4.3;            // Subtração
    let produto = 4 * 30;                  // Multiplicação
    let quociente = 56.7 / 32.2;           // Divisão
    let resto = 43 % 5;                    // Resto
}
```

## Observações Importantes

1. **Tipos Padrão**:
   - Quando não especificado, Rust usa `i32` para inteiros
   - Para decimais, o padrão é `f64`

2. **Legibilidade**:
   - Use `_` para separar números grandes: `1_000_000`
   - Funciona com qualquer tipo numérico: `1_234.567_89`

3. **Constantes**:
   - Tipo é sempre obrigatório em constantes
   - Exemplo: `const MAX_PONTOS: u32 = 100_000;`

4. **Conversão**:
   - Use `as` para converter entre tipos numéricos
   - Exemplo: `let float = 3.9;`
   - `let integer = float as i32; // Resultado: 3`

## Exercícios Práticos

1. Crie uma função que converta temperatura de Celsius para Fahrenheit
2. Calcule a área de um círculo usando pi e o raio
3. Implemente uma função que determine se um número é par ou ímpar

## Dicas

1. Escolha o tipo mais apropriado para sua necessidade
2. Cuidado com overflow em números pequenos
3. Use tipos menores quando precisar economizar memória
4. Prefira `f64` para cálculos que precisam de precisão

---

| [⬅️ Primeiro Projeto](../primeiro-projeto/README.md) | [Variáveis e Controle de Fluxo ➡️](../variaveis-controle/README.md) |
|:------------------------------------------------|----------------------------------------------------------------:|