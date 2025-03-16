Claro, aqui está a tradução para o português do texto sobre controle de fluxo em Python:

**Controle de Fluxo em Python**

Estruturas de controle de fluxo permitem que você execute código condicionalmente ou repetidamente. As estruturas principais incluem:

1.  **Declarações Condicionais (if, elif, else)**
    * Usadas para executar código baseado em condições booleanas.

    * **Declaração `if` Básica**

        ```python
        idade = 18
        if idade >= 18:
            print("Você é um adulto!")  # Saída: Você é um adulto!
        ```

    * **`if-else`**

        ```python
        temperatura = 30
        if temperatura > 25:
            print("Está quente!")
        else:
            print("Está fresco!")
        ```

    * **`if-elif-else`**

        ```python
        nota = 85
        if nota >= 90:
            print("A")
        elif nota >= 80:
            print("B")  # Saída: B
        elif nota >= 70:
            print("C")
        else:
            print("Reprovado")
        ```

    * **Operador Ternário**

        ```python

        eh_quente = "Quente" if temperatura > 25 else "Não está quente"
        print(f"Clima: {eh_quente}")

        desconto = preco * 0.1 if quantity > 2 else 0
        print(f"Desconto: R${desconto:.2f}")

        categoria = "Alto" if int_num > 90 else "Médio" if int_num > 50 else "Baixo"
        print(f"Categoria: {categoria}")

        mensagem = "Número válido" if (lambda x: x > 0)(int_num) else "Número inválido"
        print(mensagem)

        resultado = "Verificado" if verdadeiro else "Não verificado"
        print(resultado)

        tipo = "Numérico" if isinstance(num_str, int) else "Texto"
        print(f"O valor {num_str} é do tipo: {tipo}")
        ```

**2. Loops**

* **Loop `for`**
    * Itera sobre sequências (listas, strings, intervalos).

        ```python
        # Loop através de uma lista
        frutas = ["maçã", "banana", "cereja"]
        for fruta in frutas:
            print(fruta)  # Saída: maçã → banana → cereja

        # Loop com range()
        for i in range(3):  # 0, 1, 2
            print(i)

        # Loops aninhados
        for x in range(2):      # Loop externo
            for y in range(3):  # Loop interno
                print(f"({x}, {y})")
        ```

* **Loop `while`**
    * Repete o código enquanto uma condição for `True`.

        ```python
        # Contagem regressiva
        contagem = 5
        while contagem > 0:
            print(contagem)  # 5 → 4 → 3 → 2 → 1
            contagem -= 1
        print("Decolar! 🚀")

        # Validação de entrada do usuário
        senha = ""
        while senha != "segredo":
            senha = input("Digite a senha: ")
        print("Acesso concedido!")
        ```

**3. Declarações de Controle de Loop**

* **`break`**
    * Sai do loop imediatamente.

        ```python
        numeros = [1, 2, 3, 4, 5]
        for num in numeros:
            if num == 3:
                break  # Para o loop
            print(num)  # Saída: 1 → 2
        ```

* **`continue`**
    * Pula para a próxima iteração.

        ```python
        for num in range(6):
            if num % 2 == 0:
                continue  # Pula números pares
            print(num)  # Saída: 1 → 3 → 5
        ```

* **`else` em Loops**
    * Executa se o loop completar normalmente (sem `break`).

        ```python
        for n in [2, 4, 6]:
            if n % 2 != 0:
                break
        else:
            print("Todos os números são pares!")  # Saída: Todos os números são pares!
        ```
