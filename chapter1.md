--- 
title_meta  : Chapter 1
title       : Introdução ao básico
description : "Neste capítulo, você dará seus primeiros passos no R. Você irá aprender como usar o console como uma calculadora e como atribuir variáveis. Você também os tipos de dados básicos do R. Vamos começar!"

--- type:NormalExercise xp:100 skills:1 key:15d729634a
## Como Funciona

No editor à direita você deve digitar o código em R para resolver os exercícios. Quando você pressiona o botão 'Submit Answer', cada linha de código é interpretada e executada pelo R e você recebe uma mensagem dizendo se seu código está correto ou não. O resultado de seu código em R é mostrado no console no canto inferior direito.

O R utiliza o sinal `#` para adicionar comentários para que você outros possam entender sobre o que é o código. Igual ao Twitter! Comentários não são executados como código, assim eles não influenciam seu resultado. Por exemplo, _Calcule 3 + 4_ no editor à direita é um comentário.

Você também pode executar comandos em R diretamente no console. É uma boa maneira de experimentar o código em R, enquanto a correção da sua submissão ainda não foi verificada.

*** =instructions
- No editor à direita já há uma amostra de código. Você consegue ver quais linhas são código em R e quais são comentários?
- Adicione uma linha de código que calcule a soma de 6 e 12, e pressione o botão 'Submit Answer'.

*** =hint
Simplesmente adicione uma linha de R que calcule a soma de 6 e 12, igual ao exemplo na amostra de código!

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Calcule 3 + 4
3 + 4

# Calcule 6 + 12

```

*** =solution
```{r}
# Calcule 3 + 4
3 + 4

# Calcule 6 + 12
6 + 12
```

*** =sct
```{r}
test_output_contains("18", incorrect_msg = "Certifique-se de colocar `6 + 12` em uma nova linha. Não comece a linha com `#`, senão o seu código em R não será executado!")
success_msg("Fantástico! Vê como o console mostra o resultado do código em R que você submeteu? Agora que você já está familiarizado com a interface, vamos entrar nesse negócio de R!")
```

--- type:NormalExercise xp:100 skills:1 key:720745eda5
## Aritmética com R

Na sua forma mais básica, o R pode ser usado como uma simples calculadora. Veja os seguinte operadores aritiméticos:

- Adição: `+`
- Subtração: `-`
- Multiplicação: `*`
- Divisão: `/`
- Exponenciação: `^`
- Restante: `%%`

Estes dois últimos talvez demandem alguma explicação:
- O operador `^` eleva o número à sua esquerda à potencia do número à sua direita: por exemplo `3^2` é 9.
- O restante retorna o resto da divisão do número à sua esquerda pelo número à direita, por exemplo: o restante de 5 por 3, ou `5 %% 3` é 2.

Com este conhecimento, siga as instruções abaixo para completar o exercício.

*** =instructions
- Digite `2^5` no editor para calcular 2 elevado à quinta potência.
- Digite `28 %% 6` para calcular o restante da divisão de 28 por 6.
- Clique em 'Submit Answer' e olhe o resultado no que o R imprime no console.
- Note como o símbolo `#` é usado para adicionar comentários ao código em R.

*** =hint
Outro exemplo do operador restante: `9 %% 2` é igual a `1`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Uma adição
5 + 5 

# Uma subtração
5 - 5 

# Uma multiplicação
3 * 5

 # Uma divisão
(5 + 5) / 2 

# Exponenciação


# Restante

```

*** =solution
```{r}
# Uma adição
5 + 5

# Uma subtração
5 - 5 

# Uma multiplicação
3 * 5

# Uma divisão
(5 + 5) / 2 

# Exponenciação
2 ^ 5

# Restante
28 %% 6
```

*** =sct
```{r}
msg = "Não remova os outros exemplos de aritmética!"
test_output_contains("2^5", incorrect_msg = "O exemplo de exponenciação não está correto. Escreva `2 ^ 5` em uma linha nova.")
test_output_contains("28 %% 6", incorrect_msg = "Parece haver um problema no exemplo que calcula o restante. Escreva `28 %% 6` em uma nova linha.")
success_msg("Ótimo! Siga adiante para o próximo exercício.")
```


--- type:NormalExercise xp:100 skills:1 key:5f200ffd43
## Atribuição de variável 

Um conceito básico em programação (estatística) é chamado de **variável**. 

Uma variável permite que armazene um valor (p.ex. 4) ou um objeto (p.ex. a descrição de uma função) em R. Depois você pode usar o nome desta variável para facilmente acessar o valor ou o objeto que está armazenado nela. 

Você pode atribuir o valor 4 à variável `var_minha` com o comando

```
var_minha <- 4
```

*** =instructions
É com você: complete o código no editor de tal forma que ele atribua o valor 42 à variável `x` no editor. Clique 'Submit Answer'. Note que quando você pede para o R imprimir `x`, o valor 42 aparece.

*** =hint
Veja como o valor 4 atribuído à `var_minha` na descrição do exercício. Faça exatamente a mesma coisa no editor, mas agora atribua 42 à variável `x`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Atribua o valor 42 a x
x <- 

# Imprima o valor da variável x
x
```

*** =solution
```{r}
# Atribua o valor 42 a x
x <- 42

# Imprima o valor da variável x
x
```

*** =sct
```{r}
test_object("x", undefined_msg = "Assegure-se de que definiu a variavel `x`.",
            incorrect_msg = "Assegure-se de que atribuiu o valor correto a `x`.") 
success_msg("Bom trabalho! Você notou que o R não mostra no console o valor de uma variável quando você faz a atribuição? `x <- 42` não gerou um resultado, porque R presume que você precisará desta variável no futuro. Se assim não fosse, você não teria armazenado o valor em uma variável, não é? Passe para o próximo exercício!")
```


--- type:NormalExercise xp:100 skills:1 key:c5944b90eb
## Atribuição de Variável (2)

Suponha que você tem uma cesta com cinco maçãs. Como um analista de dados em treinamento, você quer armazenar o número de maçãs em uma variável com o nome `minhas_maças`. 

*** =instructions
- Digite o seguinte código no editor: `minhas_maças <- 5`. Isto atribuirá o valor 5 a `minhas_maças`.
- Digite: `minhas_maças` abaixo do segundo comentário. Isso mostrará no console o valor de `minhas_maças`.
- Clique em 'Submit Answer', e olhe para o console: você verá que o número 5 foi impresso. Assim R conecta a variável `minhas_maças` ao valor 5.

*** =hint
Lembre-se que se você quer atribuir um número ou um objeto a uma variável em R, você pode usar o operador de atribuição `<-`. Como alternativa, você pode usar o `=`, mas `<-` é amplamente preferido pela comunidade de usuários do R.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Atribua o valor 5 à variável minhas_maças


# Imprima o valor da variável minhas_maças

```

*** =solution
```{r}
# Atribua o valor 5 à variável minhas_maças
minhas_maças <- 5

# Imprima o valor da variável minhas_maças
minhas_maças
```

*** =sct
```{r}
test_object("minhas_maças", 
            undefined_msg = "Por favor assegure-se de definir `minhas_maças`.",
            incorrect_msg = "Assegure-se de que você atribuiu o valor correto a `minhas_maças`.")
test_output_contains("minhas_maças", incorrect_msg = "Você disse explicitamente ao R para imprimir a variável `minhas_maças`no console?")
success_msg("Ótimo! Continue para o próximo exercício!")
```


--- type:NormalExercise xp:100 skills:1 key:1c1bd25045
## Atribuição de Variável (3)

Todas as cestas de frutas deliciosas têm laranjas. Por isso você decide adicionar seis laranjas. Como analista de dados, seu reflexo é imediatamente criar a variável `minhas_laranjas` e atribuir o valor 6 a ela. A seguir, você quer calcular quantas unidades de fruta você tem no total. Como você deu nomes significativos a esses valores, você agora pode escrever um código de maneira clara: 

```
minhas_maças + minhas_laranjas
```

*** =instructions
- Atribua a `minhas_laranjas` o valor 6.
- Adicione as variáveis `minhas_maças` e `minhas_laranjas` e faça o R simplesmente imprimir o resultado.
- Atribua o resultado da adição de `minhas_maças` e `minhas_laranjas` a uma nova variável `minhas_frutas`.

*** =hint
`minhas_frutas` é somente a soma de `minhas_maças` e `minhas_laranjas`. Você pode usar o operador `+` para a soma das duas e o `<-` para atribuir o valor à variável `minhas_frutas`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Atribua valores às variáveis minhas_maças e minhas_laranjas
minhas_maças <- 5


# Adicione estas duas variáveis


# Crie a variável minhas_frutas

```

*** =solution
```{r}
# Atribua valores às variáveis minhas_maças e minhas_laranjas
minhas_maças <- 5
minhas_laranjas <- 6

# Adicione estas duas variáveis
minhas_maças + minhas_laranjas

# Create the variable my_fruit
minhas_frutas <- minhas_maças + minhas_laranjas
```

*** =sct
```{r}
test_object("minhas_maças", incorrect_msg = "Mantenha a linha que atribui 5 a `minhas_maças`.")
test_object("minhas_laranjas", incorrect_msg = "Mantenha a linha que atribui 6 a `minhas_laranjas`.")
test_output_contains("minhas_maças + minhas_laranjas",
                     incorrect_msg = "Certifique-se de imprimir o resultado da adição de `minhas_maças` e `minhas_laranjas`. O exemplo de código na descrição já entrega a resposta para esta instrução!")
msg <- "Você usou `minhas_frutas <- minhas_maças + minhas_laranjas` para criar a variável `minhas_frutas`?"
test_object("minhas_frutas", undefined_msg = msg, incorrect_msg = msg)
success_msg("Boa! A grande vantagem de fazer cálculos com variáveis é a possibilidade de reutilização. Se você simplesmente troca `minhas_maças` para 12 no lugar de 5 e reexecuta o script, `minhas_frutas` será automaticamente atualizado também. Continue para o próximo exercício.")
```


--- type:NormalExercise xp:100 skills:1 key:915fcc7c99
## Apples and oranges

Common knowledge tells you not to add apples and oranges. But hey, that is what you just did, no :-)? The `my_apples` and `my_oranges` variables both contained a number in the previous exercise. The `+` operator works with numeric variables in R. If you really tried to add "apples" and "oranges", and assigned a text value to the variable `my_oranges` (see the editor), you would be trying to assign the addition of a numeric and a character variable to the variable `my_fruit`. This is not possible.

*** =instructions
- Click 'Submit Answer' and read the error message. Make sure to understand why this did not work.
- Adjust the code so that R knows you have 6 oranges and thus a fruit basket with 11 pieces of fruit.

*** =hint
You have to assign the numeric value `6` to the `my_oranges` variable instead of the character value `"six"`. Note how the quotation marks are used to indicate that `"six"` is a character.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Assign a value to the variable my_apples
my_apples <- 5 

# Fix the assignment of my_oranges
my_oranges <- "six" 

# Create the variable my_fruit and print it out
my_fruit <- my_apples + my_oranges 
my_fruit
```

*** =solution
```{r}
# Assign a value to the variable my_apples
my_apples <- 5  

# Fix the assignment of my_oranges
my_oranges <- 6

# Create the variable my_fruit and print it out
my_fruit <- my_apples + my_oranges 
my_fruit
```

*** =sct
```{r}
test_error(incorrect_msg = "You can do this by setting the `my_oranges` variable to a numeric value, not a string!")
test_object("my_apples", incorrect_msg = "Make sure that `my_apples` still contains `5`.")
test_object("my_oranges", incorrect_msg = "Make sure that `my_oranges` is equal to `6`.")
test_object("my_fruit", incorrect_msg = "The value of `my_fruit` is not correct. It should be 11, the sum of `my_apples` and `my_oranges`.")
test_output_contains("my_fruit", incorrect_msg = "Don't remove the line that prints out `my_fruit`.")
success_msg("Awesome, keep up the good work! Continue to the next exercise.")
```


--- type:NormalExercise xp:100 skills:1 key:0f23107394
## Basic data types in R

R works with numerous data types. Some of the most basic types to get started are:

- Decimals values like `4.5` are called **numerics**.
- Natural numbers like `4` are called **integers**. Integers are also numerics.
- Boolean values (`TRUE` or `FALSE`) are called **logical**.
- Text (or string) values are called **characters**.

Note how the quotation marks on the right indicate that "some text" is a character.

*** =instructions
Change the value of the:

- `my_numeric` variable to `42`.
- `my_character` variable to `"universe"`. Note that the quotation marks indicate that `"universe"` is a character.
- `my_logical` variable to `FALSE`.

Note that R is case sensitive!

*** =hint 
Replace the values in the editor with the values that are provided in the exercise. For example: 
`my_numeric <- 42` assigns the value 42 to the variable `my_numeric`. 

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Change my_numeric to be 42
my_numeric <- 42.5

# Change my_character to be "universe"
my_character <- "some text"

# Change my_logical to be FALSE
my_logical <- TRUE
```

*** =solution
```{r}
# Change my_numeric to be 42
my_numeric <- 42

# Change my_character to be "universe"
my_character <- "universe"

# Change my_logical to be FALSE
my_logical <- FALSE
```

*** =sct
```{r}
test_object("my_numeric", incorrect_msg = "Have you correctly changed the declaration of `my_numeric` so it contains the value 42?")
test_object("my_character", incorrect_msg = "Have you correctly changed `my_character` to `\"universe\"`? Don't forget the quotes!")
test_object("my_logical", incorrect_msg = "Have you correctly changed `my_logical` to `FALSE`? All letters of `FALSE` should be capitalized!")
success_msg("Great work! Continue to the next exercise.")
```


--- type:NormalExercise xp:100 skills:1 key:99b549229d
## What's that data type?

Do you remember that when you added `5 + "six"`, you got an error due to a mismatch in data types? You can avoid such embarrassing situations by checking the data type of a variable beforehand. You can do this with the `class()` function, as the code on the right shows.

*** =instructions
Complete the code in the editor and also print out the classes of `my_character` and `my_logical`. 

*** =hint
The code that prints the data type of `my_numeric` is already included; do a similar things for `my_character` and `my_logical`. 

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Declare variables of different types
my_numeric <- 42
my_character <- "universe"
my_logical <- FALSE 

# Check class of my_numeric
class(my_numeric)

# Check class of my_character


# Check class of my_logical

```

*** =solution
```{r}
# Declare variables of different types:
my_numeric <- 42
my_character <- "universe"
my_logical <- FALSE

# Check class of my_numeric
class(my_numeric)

# Check class of my_character
class(my_character)

# Check class of my_logical
class(my_logical)
```

*** =sct
```{r}
msg <- "Do not change the declaration of the variables!"
lapply(c("my_numeric", "my_character", "my_logical"), test_object, undefined_msg = msg, incorrect_msg = msg)
patt <- "Have you included `class(%1$s)` to print out the data type of `%1$s`?"
test_output_contains("class(my_numeric)",
                     incorrect_msg = "Do not remove the code that prints out the type of `my_numeric`.")
test_output_contains("class(my_character)",
                     incorrect_msg = sprintf(patt, "my_character"))
test_output_contains("class(my_logical)",
                     incorrect_msg = sprintf(patt, "my_logical"))
success_msg("Congratulations! This was the last exercise for this chapter. Head over to the next chapter to get immersed in the world of vectors!")
```



