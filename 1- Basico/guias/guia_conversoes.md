
## **Conversão de Tipo em Python**
A conversão de tipo permite converter dados de um tipo para outro. Python suporta conversões **explícitas** (manuais) e **implícitas** (automáticas).

---

### **1. Conversão Explícita**
Use funções embutidas para forçar uma conversão:

#### **`int()`**: Converter para inteiro
```python
num_str = "123"
num_int = int(num_str)  # String → Inteiro
print(num_int, type(num_int))  # 123 <class 'int'>

float_num = 3.99
truncated = int(float_num)  # Float → Inteiro (trunca decimais)
print(truncated)  # 3
```

#### **`float()`**: Converter para ponto flutuante
```python
num_str = "45.6"
num_float = float(num_str)  # String → Float
print(num_float, type(num_float))  # 45.6 <class 'float'>

int_num = 100
as_float = float(int_num)  # Inteiro → Float
print(as_float)  # 100.0
```

#### **`str()`**: Converter para string
```python
age = 25
age_str = str(age)  # Inteiro → String
print("Idade: " + age_str)  # "Idade: 25"

price = 9.99
price_str = str(price)  # Float → String
print("Preço: $" + price_str)  # "Preço: $9.99"
```

#### **`bool()`**: Converter para booleano
```python
# Números diferentes de zero → True
print(bool(10))  # True
print(bool(0))   # False

# Strings não vazias → True
print(bool("Oi")) # True
print(bool(""))   # False

# Listas não vazias → True
print(bool([1]))  # True
print(bool([]))   # False
```

---

### **2. Conversão Implícita**
Python converte automaticamente os tipos durante as operações:
```python
# Inteiro + Float → Float
result = 5 + 3.14
print(result, type(result))  # 8.14 <class 'float'>

# Inteiro + Booleano → Inteiro (True = 1, False = 0)
total = 10 + True
print(total)  # 11
```

---

### **Casos de Uso Comuns**
#### **Tratamento de Entrada do Usuário**
```python
user_input = input("Digite um número: ")  # Entrada é sempre uma string
num = int(user_input)  # Converter para inteiro para cálculos
```

#### **Formatação de String**
```python
price = 19.99
quantity = 3
message = f"Total: ${price * quantity:.2f}"  # Float → String
print(message)  # "Total: $59.97"
```

---

### **Armadilhas**
#### **Conversões Inválidas**
```python
# Converter strings não numéricas para int/float gera um erro:
int("olá")  # ❌ ValueError
float("abc")  # ❌ ValueError
```

#### **Perda de Precisão**
```python
x = 3.999
y = int(x)  # Trunca para 3 (NÃO arredonda)
```

---

### **Tabela Resumo**
| Função  | Converte Para | Exemplo               |
|---------|---------------|-----------------------|
| `int()` | Inteiro       | `int("123") → 123`    |
| `float()`| Float         | `float(5) → 5.0`      |
| `str()` | String        | `str(3.14) → "3.14"`  |
| `bool()`| Booleano      | `bool("Olá") → True`   |

---

### **Tente Você Mesmo!**
1. Converta `"100.5"` para um float, depois para um inteiro.
2. Combine sua idade (inteiro) e uma string como "Eu tenho [idade] anos de idade".
3. Verifique se uma lista vazia é `False` usando `bool()`.

Me avise se precisar de mais esclarecimentos! 🚀
