# Gerenciamento de Exceções em Python

Este repositório contém exemplos e explicações sobre como trabalhar com exceções em Python.

## O que são Exceções?

Exceções são erros detectados durante a execução de um programa. Em Python, podemos tratá-las para evitar que o programa pare inesperadamente.

## Tratamento de Exceções

O tratamento de exceções em Python é feito com o bloco `try-except`. Exemplo:

```python
try:
    numero = int(input("Digite um número: "))
    resultado = 10 / numero
    print("Resultado:", resultado)
except ZeroDivisionError:
    print("Erro: Divisão por zero não é permitida.")
except ValueError:
    print("Erro: Entrada inválida. Digite um número válido.")
except Exception as e:
    print(f"Erro inesperado: {e}")
```

## Bloco `finally`

O bloco `finally` sempre será executado, independentemente de uma exceção ter ocorrido ou não.

```python
try:
    arquivo = open("dados.txt", "r")
    conteudo = arquivo.read()
except FileNotFoundError:
    print("Erro: Arquivo não encontrado.")
finally:
    print("Encerrando operação.")
```

## Lançando Exceções

Também podemos lançar exceções manualmente com `raise`:

```python
def dividir(a, b):
    if b == 0:
        raise ValueError("O divisor não pode ser zero.")
    return a / b
```

## Contribuições

Sinta-se à vontade para contribuir com este repositório! 😊

---

📌 **Autor:** Joberth Castro
