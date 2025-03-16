
1.  **Inteiros (int):** Representam números inteiros, positivos ou negativos, sem casas decimais.

    ```python
    idade = 30
    ```

2.  **Números de Ponto Flutuante (float):** Representam números reais com casas decimais.

    ```python
    preco = 99.99
    ```

3.  **Strings (str):** Representam texto. Strings são imutáveis e podem ser delimitadas por aspas simples ou duplas.

    ```python
    # Concatenação
    saudacao = "Olá, " + nome + "!"
    print(saudacao)  # Saída: Olá, Python!

    # Repetição
    repeticao = nome * 3
    print(repeticao)  # Saída: PythonPythonPython

    # Indexação e fatiamento
    print(nome[0])      # Saída: P (primeiro caractere)
    print(nome[-1])     # Saída: n (último caractere)
    print(nome[0:3])    # Saída: Pyt (do índice 0 ao 2)
    print(nome[2:])     # Saída: thon (do índice 2 até o final)

    # Métodos de string comuns
    print(nome.upper())         # Saída: PYTHON
    print(nome.lower())         # Saída: python
    print(frase.replace("é", "pode ser"))  # Saída: Programação pode ser divertida
    print(frase.split())        # Saída: ['Programação', 'é', 'divertida']
    print(len(nome))            # Saída: 6 (comprimento da string)

    # Verificações
    print("Py" in nome)         # Saída: True
    print(nome.startswith("Py")) # Saída: True
    print(frase.endswith("!"))  # Saída: False
    ```

4.  **Booleanos (bool):** Representam valores lógicos `True` ou `False`.

    ```python
    # Exemplos básicos de manipulação de booleanos
    verdadeiro = True
    falso = False

    # Operações lógicas
    e_logico = verdadeiro and falso  # E lógico (AND)
    ou_logico = verdadeiro or falso  # OU lógico (OR)
    nao_logico = not verdadeiro      # NÃO lógico (NOT)

    # Comparações que resultam em booleanos
    maior_que = 10 > 5
    igual = 7 == 7
    diferente = "Python" != "Java"

    # Exibindo os resultados
    print(f"True and False = {e_logico}")
    print(f"True or False = {ou_logico}")
    print(f"not True = {nao_logico}")
    print(f"10 > 5 = {maior_que}")
    print(f"7 == 7 = {igual}")
    print(f"'Python' != 'Java' = {diferente}")

    # Uso de booleanos em estruturas condicionais
    if verdadeiro:
        print("Esta condição é verdadeira")

    # Conversão de outros tipos para bool
    print("\nConversão para bool:")
    print(f"bool(0) = {bool(0)}")           # False
    print(f"bool(1) = {bool(1)}")           # True
    print(f"bool('') = {bool('')}")         # False - string vazia
    print(f"bool('texto') = {bool('texto')}") # True - string não vazia
    ```

5.  **Listas (list):** São coleções ordenadas e mutáveis de itens. Podem conter itens de tipos diferentes.

    ```python
    # Criando uma lista vazia
    lista_vazia = []

    # Criando uma lista com elementos diversos
    lista_mista = [1, "dois", 3.0, True]

    # Criando uma lista de números
    numeros = [1, 2, 3, 4, 5]

    # Acessando elementos por índice (o primeiro elemento é 0)
    primeiro_elemento = numeros[0]  # Resultado: 1
    ultimo_elemento = numeros[-1]   # Resultado: 5

    # Fatiamento de listas (slicing)
    parte_da_lista = numeros[1:4]   # Resultado: [2, 3, 4]

    # Adicionando elementos
    numeros.append(6)               # Adiciona ao final: [1, 2, 3, 4, 5, 6]
    numeros.insert(0, 0)            # Insere no índice 0: [0, 1, 2, 3, 4, 5, 6]

    # Removendo elementos
    numeros.remove(3)               # Remove o valor 3: [0, 1, 2, 4, 5, 6]
    elemento_removido = numeros.pop(1)  # Remove e retorna o elemento no índice 1: [0, 2, 4, 5, 6]

    # Outras operações úteis
    tamanho = len(numeros)          # Tamanho da lista: 5
    numeros.sort()                  # Ordena a lista: [0, 2, 4, 5, 6]
    numeros.reverse()               # Inverte a lista: [6, 5, 4, 2, 0]

    # Verificando se um elemento existe na lista
    existe = 4 in numeros           # Resultado: True

    print("Lista mista:", lista_mista)
    print("Números após manipulações:", numeros)
    print("Tamanho da lista de números:", tamanho)
    print("4 está na lista?", existe)
    ```

6.  **Tuplas (tuple):** São coleções ordenadas e imutáveis de itens.

    ```python
    # Exemplos básicos de tuplas
    coordenadas = (10, 20)
    cores_rgb = (255, 0, 0)  # Vermelho em RGB
    pessoa = ("João", 25, "Engenheiro")

    # Acessando elementos da tupla
    print(f"Coordenada x: {coordenadas[0]}")
    print(f"Coordenada y: {coordenadas[1]}")

    # Tuplas são imutáveis
    # Isso geraria um erro: coordenadas[0] = 15

    # Tupla com um único elemento precisa de vírgula
    tupla_unica = (42,)

    # Desempacotamento de tupla
    nome, idade, profissao = pessoa
    print(f"{nome} tem {idade} anos e é {profissao}")

    # Tuplas são úteis para retornar múltiplos valores de uma função
    def obter_dimensoes():
        return (1920, 1080)

    largura, altura = obter_dimensoes()
    print(f"Resolução: {largura}x{altura}")
    ```

7.  **Dicionários (dict):** São coleções de pares chave-valor. As chaves devem ser únicas e imutáveis.

    ```python
    # Criando um dicionário vazio
    meu_dicionario = {}

    # Criando um dicionário com alguns pares chave-valor
    pessoa = {
        "nome": "Ana",
        "idade": 28,
        "profissao": "Engenheira"
    }

    # Acessando valores através das chaves
    print(f"Nome: {pessoa['nome']}")

    # Adicionando novos pares chave-valor
    pessoa["cidade"] = "São Paulo"

    # Modificando valores existentes
    pessoa["idade"] = 29

    # Removendo pares chave-valor
    del pessoa["profissao"]

    # Verificando se uma chave existe
    if "nome" in pessoa:
        print("A chave 'nome' existe")

    # Obtendo todas as chaves e valores
    print("Chaves:", list(pessoa.keys()))
    print("Valores:", list(pessoa.values()))
    print("Itens:", list(pessoa.items()))

    # Utilizando o método get() para acessar valores com segurança
    # Se a chave não existir, retorna o valor padrão especificado
    print(pessoa.get('nome', 'Não informado'))
    print(pessoa.get('endereco', 'Não informado'))  # Essa chave nunca existiu
    ```

8.  **Conjuntos (set):** São coleções não ordenadas de itens únicos.

    ```python
    # Creating a set
    meus_numeros = {1, 2, 3, 4, 5}

    # Creating a set with duplicate elements (duplicates are automatically removed)
    cores = {"vermelho", "azul", "verde", "azul", "amarelo"}
    print(f"Set cores: {cores}")  # Will print without duplicates

    # Empty set (must use set(), not {} which creates an empty dictionary)
    conjunto_vazio = set()

    # Adding elements to a set
    meus_numeros.add(6)
    print(f"After adding 6: {meus_numeros}")

    # Set operations
    set_a = {1, 2, 3, 4, 5}
    set_b = {4, 5, 6, 7, 8}

    # Union
    uniao = set_a | set_b  # or set_a.union(set_b)
    print(f"União: {uniao}")

    # Intersection
    intersecao = set_a & set_b  # or set_a.intersection(set_b)
    print(f"Interseção: {intersecao}")

    # Difference
    diferenca = set_a - set_b  # or set_a.difference(set_b)
    print(f"Diferença (A-B): {diferenca}")

    # Symmetric difference
    dif_simetrica = set_a ^ set_b  # or set_a.symmetric_difference(set_b)
    print(f"Diferença simétrica: {dif_simetrica}")

    # Check if an element is in a set
    print(f"3 está em set_a: {3 in set_a}")
    print(f"6 está em set_a: {6 in set_a}")
    ```


9. **Comparação entre Listas, Tuplas, Conjuntos e Dicionários**

    | Característica       | Lista          | Tupla          | Conjunto       | Dicionário       |
    |----------------------|----------------|----------------|----------------|------------------|
    | Mutabilidade         | Mutável        | Imutável       | Mutável        | Mutável          |
    | Ordenação            | Ordenada       | Ordenada       | Não ordenada   | Não ordenada     |
    | Duplicação de Itens  | Permite        | Permite        | Não permite    | Chaves únicas    |
    | Tipos de Itens       | Qualquer tipo  | Qualquer tipo  | Qualquer tipo  | Chave-valor      |
    | Sintaxe de Criação   | `[1, 2, 3]`    | `(1, 2, 3)`    | `{1, 2, 3}`    | `{'a': 1, 'b': 2}` |

10. exemplo lista vs tupla
    ```python

    print("DEMONSTRAÇÃO DE MUTABILIDADE:")

    # Demonstração com Lista (mutável)
    print("\nCom Lista:")
    frutas_lista = ["maçã", "banana", "laranja"]
    print("Lista original:", frutas_lista)

    # Modificando a lista
    frutas_lista[0] = "morango"  # Substituindo um elemento
    frutas_lista.append("uva")   # Adicionando um elemento
    frutas_lista.remove("banana") # Removendo um elemento
    print("Lista após modificações:", frutas_lista)

    # Demonstração com Tupla (imutável)
    print("\nCom Tupla:")
    frutas_tupla = ("maçã", "banana", "laranja")
    print("Tupla original:", frutas_tupla)

    try:
        frutas_tupla[0] = "morango"  # Isso causará um erro
    except TypeError as e:
        print(f"Erro ao tentar modificar tupla: {e}")

    # Não podemos modificar a tupla, precisamos criar uma nova
    nova_tupla = ("morango",) + frutas_tupla[1:]
    print("Nova tupla criada a partir da original:", nova_tupla)
    print("Tupla original permanece inalterada:", frutas_tupla)
    ```
    
