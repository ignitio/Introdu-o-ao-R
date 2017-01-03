--- 
title_meta  : Chapter 2
title       : Vetores
description : "Neste curso gratuito de R, nós levaremos você numa viagem a Las Vegas, onde você aprenderá a analisar os resultados das suas apostas utilizando vetores em R! Depois de completar este capítulo, você estará apto a criar vetores em R, nomeá-los, selecionar elementos deles e compará-los com vetores diferentes."

--- type:NormalExercise xp:100 skills:1 key:d9b453dbdd
## Crie um vetor

Está se sentindo com sorte? Tomara que sim, porque este capítulo leva você numa viagem à Cidade do Pecado, também conhecida como *Paraíso dos Estatísticos*!

Graças ao R e às suas novas habilidades de análise de dados, você aprenderá como aprimorar sua performance nas mesas de jogo e como incendiar sua carreira de apostador profissional. Este capítulo mostrará como você pode facilmente registrar o progresso de suas apostas e como você pode fazer algumas análises simples sobre as suas ações passadas. Próxima parada, Vegas Baby... VEGAS!!

*** =instructions
- Você ainda lembra do que aprendemos no primeiro capítulo? Atribua o valor `"Vamos!"` à variável `vegas`. Lembre-se: R é sensível à caixa ALTA ou baixa!

*** =hint
Só digite a seguinte linha no editor:
```
vegas <- "Vamos!"
```

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Defina a variável vegas
vegas <- 
```

*** =solution
```{r}
# Defina a variável vegas
vegas <- "Vamos!"
```

*** =sct
```{r}
test_object("vegas", incorrect_msg = "Certifique-se de que você atribuiu o valor correto a `vegas`. Não esqueça que o R é sensível à caixa ALTA ou baixa!")
success_msg("Ótimo! Vá adiante para o próximo exercício.")
```



--- type:NormalExercise xp:100 skills:1 key:fd427db76f
## Crie um vetor (2)

Vamos nos concentrar primeiro! 

No seu caminho de pobreza à riqueza, você usará muitos vetores. Vetores são arrays unidimensionais que podem receber dados numéricos, dados em forma de caracteres ou dados lógicos. Em outras palavras, um vetor é uma ferramenta simples para armazenar dados. Por exemplo, você pode armazenar seus ganhos e suas perdas diárias nos cassinos. 

Em R, você pode criar um vetor com função combinar [`c()`](http://www.rdocumentation.org/packages/base/functions/c). Você coloca os elementos do vetor separados por vírgulas dentro dos parênteses. Por exemplo:

```
vetor_numerico <- c(1, 2, 3)
vetor_caracteres <- c("a", "b", "c")
```

Assim que você tenha criado estes vetores no R, pode utilizá-los para fazer cálculos

*** =instructions 
Complete o código de maneira que `vetor_booleano` contenha os três elementos: `TRUE`, `FALSE` e `TRUE` (nessa ordem). 

*** =hint 
Atribua `c(TRUE, FALSE, TRUE)` à variável `vetor_booleano` com o operador `<-`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
vetor_numerico <- c(1, 10, 49)
vetor_caracteres <- c("a", "b", "c")

# Complete o código para o vetor_booleano
vector_booleano <-
```

*** =solution
```{r}
vetor_numerico <- c(1, 10, 49)
vetor_caracteres <- c("a", "b", "c")

# Complete the code for boolean_vector
vetor_booleano <- c(TRUE, FALSE, TRUE)
```

*** =sct
```{r}
msg <- "Não altere o código que definiu o `vetor_numerico` e o `vetor_caracteres`!"
test_object("vetor_numerico", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_caracteres", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_booleano",
            incorrect_msg = "Tenha certeza de que você atribuiu corretamente os valores ao `vetor_booleano`. Use `c(TRUE, FALSE, TRUE)`. Não coloque aspas em `TRUE` e `FALSE`! E também confira se você adotou a mesma ordem listada nas instruções.")
success_msg("Perfeito! Note que adicionando espaço antes das virgulas na função `c()` melhora a legibilidade do seu código. Vamos praticar um pouco mais a criação de vetores no próximos exercício.")
```


--- type:NormalExercise xp:100 skills:1 key:9f41229dbc
## Crie um vetor (3)

Depois de uma semana em Las Vegas ainda sem nenhuma Ferrari na garagem, você decide que hora de começar a usar seus superpoderes de análise de dados.

Antes de fazer a primeira análise, você decide primeiro coletar todas os seus ganhos e suas perdas da última semana: 

Para o `vetor_poker`: 

- Segunda-feira você ganhou $140
- Terça-feira você perdeu $50
- Quarta-ferira você ganhou $20 
- Quinta-feira você perdeu $120
- Sexta-feira você ganhou $240

Para o `vetor_roleta`:

- Segunda-feira você perdeu $24
- Terça-feira você perdeu $50
- Quarta-ferira você ganhou $100 
- Quinta-feira você perdeu $350
- Sexta-feira você ganhou $10

Você só jogou poker e roleta, porque tinha uma delegação de mediums que ocupou as mesas de jogo de dados. Para poder usar estes dados no R, você decide criar as variáveis `vetor_poker` e `vetor_roleta`.

*** =instructions
Atribua as perdas/ganhos na roleta à variável `vetor_roleta`.

*** =hint
Para ajudá-lo com este passo, o editor já contem o código para o criar o `vetor_poker`. Atribua os valores corretos ao `vetor_roleta` baseado nos número do enunciado. Não esqueça que as perdas são números negativos.

*** =sample_code
```{r}
# Ganhos no Poker de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)

# Ganhos na Roleta de segunda a sexta
vetor_roleta <-  
```

*** =solution
```{r}
# Ganhos no Poker de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)

# Ganhos na Roleta de segunda a sexta
vetor_roleta <-  c(-24, -50, 100, -350, 10)
```

*** =sct
```{r}
test_object("vetor_poker",
            incorrect_msg = "Confira se você atribuiu os valores corretos ao `vetor_poker`.")
test_object("vector_roleta",
            incorrect_msg = "Confira se você atribuiu os valores corretos ao `vetor_roleta`. Tenha certeza de que adotou a ordem correta!")
success_msg("Muito bom! Veja o conteúdo dos vetores, lembre-se de você sempre pode simplesmente digitar a variável no console e apertar Enter. Passe para o próximo exercício!")
```


--- type:NormalExercise xp:100 skills:1 key:3b0b80b192
## Nomeando um vetor

Como analista de dados, é importante ter uma visão clara dos dados que você esta usando. Portanto, entender ao que cada elemento se refere é essencial. 

No exercício anterior, nós criamos um vetor com os seus ganhos no decorrer da semana. Cada elemento do vetor se refere a um dia da semana mas é difícil dizer qual elemento pertence a qual dia. Seria bom se você pudesse mostrar isso no próprio vetor.

Você pode dar nome aos elementos de um vetor com a função `names()`. Dê uma olhada neste exemplo:

```
algum_vetor <- c("João Ninguém", "jogador de poker")
names(algum_vetor) <- c("Nome", "Profissão")
```

Este código primeiro cria o vetor `algum_vector` e então dá nomes aos dois elementos. Ao primeiro elemento é atribuído o nome `Nome`, ao passo que o segundo elemento é rotulado `Profissão`. Imprimir o conteúdo no console traz o seguinte resultado:

```
          Nome     Profissão 
    "João Ninguém" "jogador de poker" 
```

*** =instructions
- O código ao lado nomeia os elementos no `vetor_poker` com os dias da semana. Adicione o código para fazer a mesma coisa para o `vetor_roleta`.

*** =hint
Você pode usar `names(vector_roleta)` para colocar nomes na variável `vetor_roleta`. Certifique-se de usar o mesmo vetor com os nomes dos dias da semana. Lembre-se que o R é sensível à caixa ALTA e baixa!

*** =sample_code
```{r}
# Ganhos no Poker de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)

# Ganhos na Roleta de segunda a sexta
vetor_roleta <-  c(-24, -50, 100, -350, 10)

# Atribua dias como nomes do vetor_poker
names(vetor_poker) <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")

# Atribua dias como nomes do vetor_roleta
```

*** =solution
```{r}

# Ganhos no Poker de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)

# Ganhos na Roleta de segunda a sexta
vetor_roleta <-  c(-24, -50, 100, -350, 10)

# Atribua dias como nomes do vetor_poker
names(vetor_poker) <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")

# Atribua dias como nomes do vetor_roleta
names(vetor_roleta) <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
```

*** =sct
```{r}
test_object("vetor_poker",
            incorrect_msg = "Não altere os valores dentro do `vector_poker`; eles já foram codificados por você.")
test_object("vetor_roleta",
            incorrect_msg = "Não altere os valores dentro do `vetor_roleta`; eles já foram codificados por você.")
test_object("vetor_poker",
            eq_condition = "equal",
            incorrect_msg = "Não altere o código que nomeia os elementos do `vetor_poker`; mantenha o foco no `vetor_roleta_vector`!")
test_object("vetor_roleta",
            eq_condition = "equal",
            incorrect_msg = "Verifique se você atribuiu os nomes corretos ao `vetor_roleta`. Use exatamente o mesmo vetor que foi utilizado para nomear o `vetor_poker`.")
success_msg("Muito bem! Continue para o próximo exercício.")
```


--- type:NormalExercise xp:100 skills:1 key:6858c65a4a
## Nomeando um vetor (2)

Se você quer se tornar um bom estatístico, você tem que se tornar preguiçoso. (Se você já é preguiçoso, há uma grande chance de você ser um daqueles excepcionais talentos natos para estatística.)

Nos exercícios anteriores você provavelmente sentiu que é chato frustrante digitar e redigitar informações como dias da semana. Contudo, quando você para isso de uma perspectiva mais ampla, há uma maneira mais eficiente de fazer isso, isto é, de atribuir um vetor de dias da semana a uma **variável**! 

Assim como fez com os resultados no poker e na roleta, você também pode criar uma variável que contenha os dias da semana. Assim você pode usá-la e reusá-la.

*** =instructions
- Uma variável `vetor_dias` que contem os dias da semana já foi criada para você.
- Use o `vetor_dias` para atribuir nomes à `vetor_poker` e `vetor_roleta`.

*** =hint
Você pode usar `names(vetor_poker) <- vetor_dias` para atribuir nomes aos elementos do `vetor_poker`. Faça algo similar para o `vetor_roleta`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Ganhos no Poker de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)

# Ganhos na Roleta de segunda a sexta
vetor_roleta <-  c(-24, -50, 100, -350, 10)

# A variável vetor_dias
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
 
# Atribua os nomes dos dias ao vetor_roleta e ao vetor_poker
names(vetor_poker) <-   
names(vetor_roleta) <-
```

*** =solution
```{r}
# Ganhos no Poker de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)

# Ganhos na Roleta de segunda a sexta
vetor_roleta <-  c(-24, -50, 100, -350, 10)

# A variável vetor_dias
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")

# Atribua os nomes dos dias ao vetor_roleta e ao vetor_poker
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias
```

*** =sct
```{r}
msg <- "Não faça alterações nas variáveis pré-definidas `vetor_poker`, `vetor_roleta` ou `vetor_dias`."
test_object("vetor_poker", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)

test_object("vetor_poker",
            eq_condition = "equal",
            incorrect_msg = "Tenha certeza de que atribuiu o `vetor_dias` aos nomes do `vetor_poker`.")
test_object("vetor_roleta",
            eq_condition = "equal",
            incorrect_msg = "Tenha certeza de que atribuiu o `vetor_dias` aos nomes do `vetor_roleta`.")
success_msg("Boa! Um palavrinha: sempre tente evitar duplicação de código. Continue para o próximo exercício e aprenda como fazer aritmética com vetores!")
```


--- type:NormalExercise xp:100 skills:1 key:da995f099f
## Calculando os ganhos totais

Agora que você os ganhos de poker e roleta armazenados corretamente como vetor nominados, você pode começar a fazer alguma análise de dados mágica. 

Você quer encontrar as seguintes informações:

- Qual tem sido o lucro ou a perda total por dia da semana?
- Vocêm perdeu dinheiro no total da semana?
- Você está ganhando/perdendo dinheiro no poker ou na roleta?

Para conseguir estas respostas, você tem que fazer cálculos aritméticos com vetores. 

É importante saber que se você soma dois vetores em R, ele faz a soma elemento a elemento. Por exemplo, as próximas três linhas são complemente equivalentes:

```
c(1, 2, 3) + c(4, 5, 6)
c(1 + 4, 2 + 5, 3 + 6)
c(5, 7, 9)
```

Você tembém pode fazer cálculos com variáveis que representam vetores:

```
a <- c(1, 2, 3) 
b <- c(4, 5, 6)
c <- a + b
```

*** =instructions
- Faça a soma das variáveis `vetor_A` e `vetor_B` e atribua a `vetor_total`.
- Inspecione o resultado imprimindo no console `vetor_total`.

*** =hint
Use o operador `+` para somar `vetor_A` e `vector_B`. Use `<-` para atribuir o resultado a `vector_total`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
vetor_A <- c(1, 2, 3)
vetor_B <- c(4, 5, 6)

# Faça a soma de vetor_A e vetor_B
vetor_total <- 
  
# Imprima no console o vetor_total

```

*** =solution
```{r}
vetor_A <- c(1, 2, 3)
vetor_B <- c(4, 5, 6)

# Faça a soma de vetor_A e vetor_B
vetor_total <- vetor_A + vetor_B

# Imprima no console o vetor_total
vetor_total
```

*** =sct
```{r}
msg <- "Não altere o conteúdo de `vetor_A` e `vetor_B`!"
test_object("vetor_A", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_B", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_total", incorrect_msg = "Certifique-se de que o `vetor_total` contem a soma de `vetor_A` e `vetor_B`.")
test_output_contains("vetor_total", incorrect_msg = "Não esqueça de imprimir no console o `vetor_total`! Simplesmente escreva `vetor_total` em uma nova linha.")
success_msg("Bom trabalho! Continue para o próximo exercício.")
```


--- type:NormalExercise xp:100 skills:1 key:2969d8ed65
## Calculando os ganhos totais (2)

Agora que você entende como o R faz cálculos aritméticos com vetores, chegou a hora de conseguir aquelas Ferraris para colocar na garagem! Primeiro você precisa entender qual foi seu lucro ou prejuízo diário. Os ganhos totais diários são a soma dos ganhos/perdas que você teve no poker, por dia, e os ganhos/perdas que você teve na roleta, por dia. 

No R, isso é somente a soma de `vetor_roleta` e `vetor_poker`.

*** =instructions
Atribua à variável `total_dia` quanto você ganhou ou perdeu a cada dia (somando poker e roleta).

*** =hint
De forma similar ao exercício anterior, atribuia a soma dos dois vetores à nova variável, `total_dia`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Atribua a total_dia quanto você ganhou/perdeu em cada dia
total_dia <- 
```

*** =solution
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Atribua a total_dia quanto você ganhou/perdeu em cada dia
total_dia <- poker_vector + roulette_vector
```

*** =sct
```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)

test_object("total_dia", incorrect_msg = "Certifique-se de que atribuiu a soma de `vetor_poker` e `vetor_roleta` a `total_dia`.")

success_msg("Ótimo! Continue para o próximo exercício.")
```


--- type:NormalExercise xp:100 skills:1 key:e66a56b9f0
## Calculando os ganhos totais (3)

Beseado na análise anterior, parece que você teve dias bons e dias ruins. Isto não é o que o seu ego esperava, e você começa a pensar que há uma pequena chance de você, no total da semana, ter perdido dinheiro. 

Uma função que ajuda você a responder a essa questão [`sum()`](http://www.rdocumentation.org/packages/base/functions/sum). Ela calcula a soma de todos os elementos de um vetor. Por exemplo, para calcular o valor total em dinheiro que você ganhou/perdeu no poker você digita: 

```
total_poker <- sum(vetor_poker)
```

*** =instructions
- Calcule o valor de dinheiro que você ganhou/perdeu na roleta e atribua à variável `total_roleta`.
- Agora que você já tem os totais para roleta e poker, você pode facilmente calcular `total_semana` (que é a soma de todos os ganhos e perdas da semana).
- Imprima no console `total_semana`.

*** =hint
Use a função [`sum()`](http://www.rdocumentation.org/packages/base/functions/sum) para chegar ao total de `vetor_roleta`. `total_semana`será então a soma de `vetor_roleta` e `vetor_poker`. 

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Ganhos totais com poker
total_poker <- sum(vetor_poker)

# Ganhos totais com roleta
total_roleta <-  

# Ganhos totais
total_semana <- 

# Imprima total_semana no console
  
```

*** =solution
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Ganhos totais com poker
total_poker <- sum(vetor_poker)

# Ganhos totais com roleta
total_roleta <-  sum(vetor_roleta)

# Ganhos totais
total_semana <- total_roleta + total_poker

# Imprima total_semana no console
total_semana
```

*** =sct
```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("total_poker", 
            incorrect_msg = "Tenha certeza de que atribuiu a `total_poker` a soma de `vetor_poker`.")
test_object("total_roleta",
            incorrect_msg = "Tenha certeza de que atribuiu a `total_roleta` a soma de `vetor_roleta`.")
test_object("total_week",
            incorrect_msg = "Tenha certeza de que atribuiu a `total_semana` a soma dos outros dois totais: `total_roleta` e `total_poker`.")

test_output_contains("total_semana", incorrect_msg = "Não esqueça de excrever `total_semana` em uma nova linha para imprimir a variáevel no console.")
success_msg("Muito bem. Essa é uma notícia muito ruim...")
```


--- type:NormalExercise xp:100 skills:1 key:f532f5332d
## Comparando ganhos totais

Oopa, parece que você está perdendo dinheiro. Está na hora de repensar e adaptar a sua estratégia! Isto vai demandar uma análise mais profunda... 

Depois de um rápido brainstorm na jacuzzi do hotel, você percebe que uma possível explicação pode ser que as suas habilidades na roleta não sejam tão desenvolvidas quanto as suas habilidades no poker. Assim, talvez seus ganhos totais no poker sejam mais altos (ou `>` ) do que na roleta.

*** =instructions
- Calcule `total_poker` e `total_roleta` como no exercício anterior. Use a função `sum()` duas vezes.
- Confira se o total de ganhos no poker é maior alto que os da roleta usando uma comparação. Simplesmente imprima no console o resultado desta comparação. O que você conclui? Deveria focar na roleta ou no poker?

*** =hint
- Você já calculou parte desta resposta no exercício anterior!
- Para confirir se 6 é maior que 5, digite `6 > 5`. Isto retorna um valor lógico (`TRUE` ou `FALSE`).

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Ganhos totais com poker e roleta
total_poker <- sum(vetor_poker)
total_roleta <-  sum(vetor_roleta)

# Confira se você atingiu ganhos mais altos no poker do que na roleta 

```

*** =solution
```{r}

# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Ganhos totais com poker e roleta
total_poker <- sum(vetor_poker)
total_roleta <-  sum(vetor_roleta)

# Confira se você atingiu ganhos mais altos no poker do que na roleta 
total_poker > total_roleta
```

*** =sct
```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("total_poker", 
            incorrect_msg = "Tenha certeza de que atribuiu a `total_poker` a soma de `vetor_poker`. Use `sum()`")
test_object("total_roleta",
            incorrect_msg = "Tenha certeza de que atribuiu a `total_roleta` a soma de `vetor_roleta`. Use `sum()`")
test_output_contains("total_poker > total_roleta",
                     incorrect_msg = "Você fez corretamente a comparação? Para conferir se `total_poker` é maior que `total_roleta`, você pode usar `total_poker > total_roleta`.")
success_msg("Bom trabalho! Continue para o próximo exercício.")
```


--- type:NormalExercise xp:100 skills:1 key:8d78be44e9
## Seleção de vetores: bons tempos

Sua intuição parece estar certa. Parece que poker é mais a sua praia do que roleta. 

Outra rota possível de investigaçao é a sua performance no início da semana comparada com o final dela. Você bebeu uma ou duas margaritas no final da semana...

Para responder esta questão, você só quer focar na seleção do `vetor_total`. Em outras palavras, nossa meta é selecionar elementos específicos no vetor. Para selecionar elementos de um vetor (e depois matrizes, data frames, ...), você pode usar colchetes. Entre os colchetes, você indica quais elementos quer selecionar. por exemplo, para selecionar o primeiro elemento de um vetor, você digita `vetor_poker[1]`. Para selecionar o segundo elemento do vetor, você digita `vetor_poker[2]`, etc. Note que o primeiro elemento em um vetor tem o índice 1, não 0 como em muitas outras linguagens de programação.

*** =instructions
Atribuia os resultados de quarta-feira à variável `poker_quarta`.

*** =hint
Quarta-feira é o terceiro elemento do `vetor_poker`, e assim pode ser selecionado com `vetor_poker[3]`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Defina uma nova variável baseada numa seleção
poker_quarta <- 
```

*** =solution
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Defina uma nova variável baseada numa seleção
poker_quarta <- vetor_poker[3]
```

*** =sct
```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("poker_quarta", 
            undefined_msg = "Por favor certifique-se de definir a variável `poker_quarta`.",
            incorrect_msg = "Parece que `poker_quarta` não contem o valor correto extraído de `vetor_poker`.")
success_msg("Ótimo! O R também possibilita selecionar múltiplos elementos de um vetor de uma só vez. Aprenda como no próximo exercício!")
```


--- type:NormalExercise xp:100 skills:1 key:1351521670
## Seleção de vetores: bons tempos (2)

Que tal analisar os resultados do meio da semana? 

Para selecionar vários elementos de um vetor, voê pode colocar colchetes ao final dele. Você pode indicar entre os colchetes quais elementos devem ser selecionados. Por exemplo: suponha que voc queira selecionar o primeiro e o quinto dia da semana: use o vetor `c(1, 5)` entre colchetes. Por exemplo, o código abaixo seleciona o primeiro e o quinto elemento do `vetor_poker`:

```
vetor_poker[c(1, 5)]
```

*** =instructions
Atribua os resultados no poker de terça, quarta e quinta-feira à variável `poker_meio_de_semana`.

*** =hint
Use o vetor `c(2, 3, 4)` entre colchetes para selecionar os elementos corretos do `vetor_poker`. 

*** =pre_exercise_code
```{r}
# no pec
``` 

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Defina uma nova variável baseada em uma seleção
poker_meio_de_semana <- 
```

*** =solution
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Defina uma nova variável baseada em uma seleção
poker_meio_de_semana <- vetor_poker[c(2, 3, 4)]
```

*** =sct
```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("poker_meio_de_semana", 
            incorrect_msg = "Parace que `poker_meio_de_semana` não contem os valores corretos extraídos de `vetor_poker`. Você pode usar o vetor `c(2, 3, 4)` dentro dos colchetes.")
success_msg("Muito bem! Continue para o próximo exercício para aprofundar a especialização em seleção de vetor ainda mais!")
```


--- type:NormalExercise xp:100 skills:1 key:27976b79f4
## Selecão de vetores: bons tempos (3)

Selecionar vários elementos do `vetor_poker` com `c(2, 3, 4)` não é muito conveniente. Muitos estatísticos são pessoas preguiçosas por natureza, ento eles criaram uma maneira mais fácil de fazer isso: `c(2, 3, 4)` pode ser abreviado para `2:4`, que gera um vetor com todos os números naturais de 2 até 4.

Assim, outra maneira de selecionar os resultados do meio da semana é `vetor_poker[2:4]`. Note como o vetor `2:4` é colocado entre colchetes para selecionar os elementos 2 a 4.

*** =instructions
Atribua a `vetor_seleto_roleta` os resultados da roleta de terça a sexta-feira; use `:` se isso facilita as coisas para você.

*** =hint
Atribua a seleção de `vetor_roleta` a `vetor_seleto_roleta` colocando `2:5` entre colchetes.

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Defina uma nova variável baseada em uma seleção
vetor_seleto_roleta <- 
```

*** =solution
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Defina uma nova variável baseada em uma seleção
vetor_seleto_roleta <- vetor_roleta[2:5]
```

*** =sct

```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_seleto_roleta", 
            undefined_msg = "Por favor verifique se est definida a variável `vetor_seleto_roleta`.", 
            incorrect_msg = "Parece que `vetor_seleto_roleta` não contem a seleção correta extraída do `vetor_roleta`. Certifique-se de que usou os índices corretos.")
success_msg("Fantástico! O operador dois pontos (`:`) é extremamente útil e é usado com muita frequência na programação em R, por isso deve ser lembrado. Passe ao próximo exercício.")
```


--- type:NormalExercise xp:100 skills:1 key:e6c263ddee
## Selecão de vetores: bons tempos (4)

Outra forma de resolver o exercício anterior é usar os nomes dos elementos do vetor (Segunda, Terça, ...) ao invés de suas posiçes numéricas. Por exemplo,
```
vetor_poker["Segunda"]
```

selecionará o primeiro elemento do `vetor_poker` uma que `"Segunda"` é o nome do primeiro elemento.

Da mesma forma que você fez no exercício anterior com índices numéricos, pode também pode suar os nomes para selecionar múltiplos elementos, por exemplo:

```
vetor_poker[c("Segunda","Terça")]
```

*** =instructions
- Selecione os primeiros três elementos do `vetor_poker` usando seus nomes: `"Segunda"`, `"Terça"` e `"Quarta"`. Atribua o resultado da seleção a `poker_inicio`.
- Calcule a média dos valores em `poker_inicio` com a função [`mean()`](http://www.rdocumentation.org/packages/base/functions/mean). Simplesmente imprima o resultado no console para inspecioná-lo.

*** =hint
- Você pode usar `c("Segunda", "Terça", "Quarta")` dentro dos colchetes para subdividir o `vetor_poker` de forma adequada.
- Você pode usar `mean(poker_inicio)` para conseguir a média dos elementos em `poker_inicio`. Você não precisa da média de todos os elementos de poker, mas somente dos três primeiros dias.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Selecione os resultados de poker para Segunda, Terça e Quarta
poker_inicio <- 
  
# Calcule a média dos elementos de poker_inicio

```

*** =solution
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Selecione os resultados de poker para Segunda, Terça e Quarta
poker_inicio <- vetor_poker[c("Segunda", "Terça", "Quarta")]
  
# Calcule a média dos elementos de poker_inicio
mean(poker_inicio)
```

*** =sct
```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("poker_inicio", 
            incorrect_msg = "Parece que `poker_inicio` não contem os primeiros três valores do `vetor_poker`. Você pode usar `c(\"Segunda\", \"Terça\", \"Quarta\")` dentro dos colchetes para fazer isso.")
test_output_contains("mean(poker_inicio)", incorrect_msg = "Você calculou corretamente a média dos valores de `poker_inicio` e imprimou o resultado? Use `mean(poker_inicio)`.")
success_msg("Bom trabalho! Além de subdividir vetores com índices ou com nomes, você também pode fazer isso por comparação. O próximo exercício vai lhe mostrar como!");
```


--- type:NormalExercise xp:100 skills:1 key:f0f619c901
## Seleção por comparação - 1º Passo

Ao usar operadores de comparação, nós podemos abordar a questão anterior de forma mais proativa.

Os operadores (lógicos) de comparação conhecidos do R são:

- `<` para menor que
- `>` para maior que
- `<=` para menor ou igual a
- `>=` para maior ou igual a
- `==` para igual a
- `!=` para diferente de

Como vimos no capítulo anterior, submeter `6 > 5` retorna `TRUE`. Uma coisa legal do R é que você pode usar operadores de comparação também com vetores. Por exemplo:

```
> c(4, 5, 6) > 5
[1] FALSE FALSE TRUE
```

Este comando testa para cada elemento do vetor se a condição estabelecida pela comparação é `TRUE` ou `FALSE`.

*** =instructions
- Confira quais elementos no `vetor_poker` são positivos (isto é > 0) e atribua o resultado disso a `vetor_seleção`. 
- Imprima o `vetor_seleção` para que possa inspecioná-lo. Os resultados impressos lhe dizem se você ganhou (`TRUE`) ou perdeu (`FALSE`) dinheiro a cada dia.

*** =hint
Para conferir em quais dias os ganhos no poker são positivos, o R deveria conferir se cada elemento do `vetor_poker` é maior que zero. `algum_vetor > 0` é a forma de dizer ao R o que você está procurando.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Em quais dias você ganhou dinheiro no poker?
vetor_seleção <- 
  
# Imprima o vetor_seleção

```

*** =solution
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Em quais dias você ganhou dinheiro no poker?
vetor_seleção <- vetor_poker > 0
  
# Imprima o vetor_seleção
vetor_seleção
```

*** =sct
```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)

test_object("vetor_seleção", incorrect_msg = "Parece que o `vetor_seleção` não contem o restultado correto. Lembre-se que o R faz as operações com vetores elemento a elemento.")
test_output_contains("vetor_seleção", incorrect_msg = "Não esqueça de imprimir o `vetor_seleção` escrevendo o nome da variável em uma nova linha.")
success_msg("Ótimo!")
```


--- type:NormalExercise xp:100 skills:1 key:2754fc5cd4
## Seleção por comparação - 2º Passo

Trabalhar com comparações facilitará a sua vida de analista de dados. Ao invés de selecionar um subconjunto de dias para você mesmo investigar (como antes), você pode simplesmente pedir ao R para retornar somente os dias em que você teve um retorno positivo no poker.

Na exercício anterior você usou `vetor_seleção <- vetor_poker > 0` para encontrar os dias em que você teve um retorno positivo no poker. Agora, você gostaria de saber não só os dias em que ganhou, mas também quanto ganhou nesses dias.

Você pode selecionar os elementos desejados, colocando entre colchetes o `vetor_seleção` logo após o `vetor_poker`:

```
vetor_poker[vetor_seleção]
```

O R sabe o que fazer quando você passa um vetor lógico entre colchetes: ele irá selecionar somente os elementos que correspondem a `TRUE` no `vetor_seleção`.

*** =instructions
Use o `vetor_seleção` entre colchetes para atribuir as quantias que você ganhou nos dias de lucro à variável `dias_vitoriosos_poker`.

*** =hint
Use `vetor_poker[vetor_seleção]` para selecionar os elementos desejados de `vetor_poker`, e atribua o resultado a `dias_vitoriosos_poker`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Which days did you make money on poker?
selection_vector <- poker_vector > 0

# Select from poker_vector these days
poker_winning_days <- 
```

*** =solution
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Em quais dias você ganhou dinheiro no poker?
vetor_seleção <- vetor_poker > 0

# Selecione estes dias de vetor_poker
dias_vitoriosos_poker <- vetor_poker[vetor_seleção]
```

*** =sct
```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_seleção", incorrect_msg = "Não altere a forma como `vetor_seleção` é calculado.")
test_object("dias_vitoriosos_poker",
incorrect_msg =  "Parece que `dias_vitoriosos_poker` não contem o resultado correto. Use `vetor_poker[vetor_seleção]`.")
success_msg("Bom trabalho! Continue para o próximo exercício.")
```


--- type:NormalExercise xp:100 skills:1 key:59e8dcbbd5
## Advanced selection

Just like you did for poker, you also want to know those days where you realized a positive return for roulette.

*** =instructions
- Create the variable `selection_vector`, this time to see if you made profit with roulette for different days.
- Assign the amounts that you made on the days that you ended positively for roulette to the variable `roulette_winning_days`. This vector thus contains the positive winnings of `roulette_vector`.

*** =hint
Once you've correctly calculated `selection_vector`, you can again use `roulette_vector[selection_vector]` to select the positive results from `roulette_vector`.

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Which days did you make money on roulette?
selection_vector <-

# Select from roulette_vector these days
roulette_winning_days <- 
```

*** =solution
```{r}
# Ganhos no Poker e na Roleta de segunda a sexta
vetor_poker <- c(140, -50, 20, -120, 240)
vetor_roleta <-  c(-24, -50, 100, -350, 10)
vetor_dias <- c("Segunda", "Terça", "Quarta", "Quinta", "Sexta")
names(vetor_poker) <- vetor_dias
names(vetor_roleta) <- vetor_dias

# Which days did you make money on roulette?
selection_vector <- roulette_vector > 0

# Select from roulette_vector these days
roulette_winning_days <- roulette_vector[selection_vector]
```

*** =sct
```{r}
msg = "Não altere nada na definicão e na nomeação de `vetor_poker` e `vetor_roleta`."
test_object("vetor_dias", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_poker", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("vetor_roleta", eq_condition = "equal", undefined_msg = msg, incorrect_msg = msg)
test_object("selection_vector", 
            incorrect_msg = "It looks like `selection_vector` does not contain the correct result. Use `roulette_vector > 0`.")
test_object("roulette_winning_days",
            incorrect_msg = "It looks like `roulette_winning_days` does not contain the correct result. Use `roulette_vector[selection_vector]`.")

success_msg("Great! This exercise concludes the chapter on vectors. The next chapter will introduce you to the two-dimensional version of vectors: matrices.")
```



