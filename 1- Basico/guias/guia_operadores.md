## **Operadores Lógicos em Python**

Operadores lógicos são usados para combinar declarações condicionais e avaliar se as expressões são `True` (Verdadeiro) ou `False` (Falso).

---

### **1. Operador `and` (e)**

-   **Definição**: Retorna `True` **somente se ambas as condições forem verdadeiras**.
-   **Tabela Verdade**:
    | A     | B     | A `and` B |
    | :---- | :---- | :-------- |
    | True  | True  | **True** |
    | True  | False | False     |
    | False | True  | False     |
    | False | False | False     |

#### **Exemplo**:

```python
    # Exemplos práticos do operador AND

    # Exemplo 1: Comparações básicas
    print("Exemplo 1: Comparações básicas")
    print(True and True)    # True
    print(True and False)   # False
    print(False and True)   # False
    print(False and False)  # False
    print()

    # Exemplo 2: Expressões com variáveis
    print("Exemplo 2: Expressões com variáveis")
    idade = 25
    possui_carteira = True

    pode_dirigir = idade >= 18 and possui_carteira

    # Exemplo 3: Verificações de intervalo
    print("Exemplo 3: Verificações de intervalo")
    nota = 75
    if nota >= 60 and nota <= 80:
        print("Nota está entre 60 e 80")
    else:
        print("Nota está fora do intervalo 60-80")
    print()

    # Exemplo 4: Short-circuit evaluation
    print("Exemplo 4: Short-circuit evaluation")
    x = 5
    print("Resultado:", x > 10 and x/0 > 0)  # A segunda parte não é avaliada quando a primeira é False
    # Não causa erro de divisão por zero devido ao short-circuit
```

---

### **2. Operador `or` (ou)**

-   **Definição**: Retorna `True` **se pelo menos uma condição for verdadeira**.
-   **Tabela Verdade**:
    | A     | B     | A `or` B |
    | :---- | :---- | :------- |
    | True  | True  | **True** |
    | True  | False | **True** |
    | False | True  | **True** |
    | False | False | False    |

#### **Exemplo**:

```python
dia = "Sábado"
eh_feriado = False

# Verifica se é fim de semana OU feriado
eh_dia_de_folga = (dia == "Sábado" or dia == "Domingo") or eh_feriado
print(eh_dia_de_folga)  # Saída: True (porque é Sábado)
```

---

### **3. Operador `not` (não)**

-   **Definição**: Inverte o valor booleano (`True` se torna `False`, e vice-versa).
-   **Tabela Verdade**:
    | A     | `not` A |
    | :---- | :------ |
    | True  | False   |
    | False | **True** |

#### **Exemplo**:

```python
eh_admin = False

# Concede acesso se o usuário NÃO é um admin
acesso_concedido = not eh_admin
print(acesso_concedido)  # Saída: True
```

---

### **Combinando Operadores**

Você pode combinar `and`, `or` e `not` para criar condições complexas.

#### **Exemplo**:

```python
temperatura = 28
esta_ensolarado = True

# Verifica se é um bom dia para a praia:
# Temperatura > 25 E ensolarado, OU é fim de semana
bom_dia_de_praia = (temperatura > 25 and esta_ensolarado) or (dia == "Sábado")
print(bom_dia_de_praia)  # Saída: True
```

---

### **Cenários do Mundo Real**

1.  **Sistema de Login**:
    ```python
    nome_usuario = "usuario123"
    senha = "senha123"
    # Verifica se tanto o nome de usuário quanto a senha estão corretos
    login_sucesso = (nome_usuario == "usuario123") and (senha == "senha123")
    ```