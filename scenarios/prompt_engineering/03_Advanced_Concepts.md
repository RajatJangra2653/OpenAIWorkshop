# Exercício 4B: Conceitos Avançados (Apenas leitura)

## Tópicos

  - [Introdução](#introduction)
  - [Zero-Shot Prompts](#zero-shot-prompts)
  - [One-Shot Prompts](#one-shot-prompts)
  - [Few-Shot Prompts](#few-shot-prompts)

---

## Introdução

Até este ponto, você experimentou o poder e a flexibilidade dos prompts. Ajustar prompts para obter os resultados desejados é a ideia por trás da Prompt Engineering.

Vamos agora abordar alguns tópicos mais avançados para ajustar os nossos outputs sem introduzir o fine-tuning dos nossos modelos GPT.

Vamos dar um exemplo simples de classificação:

*Prompt:*
```
Classify the sentiment of the text below.

Text: I think this movie was terrible. What a waste of time.
```

*Output:*
```
Negative
```

O resultado parece estar correto, mas poderíamos melhorá-lo fornecendo mais informações ao modelo se quiséssemos uma classificação mais granular. Vamos fazer isso por meio de um prompt Zero-Shot.

---

## Zero-Shot Prompts

Os LLMs GPT são treinados em quantidades tão grandes de dados que são capazes de compreender instruções complexas para levar ao output desejado na maioria dos casos. Isso é chamado de prompt 'Zero-Shot'.

Poderíamos refinar o exemplo abaixo sendo mais descritivos sobre nossas instruções.

*Prompt:*
```
Classify the sentiment of the text below into very negative, negative, neutral, positive, and very positive.

Text: I think this movie was terrible. What a waste of time.
```

*Output:*
```
Very Negative
```

Isso é chamado de Zero-Shot. Uma instrução precisa leva ao output desejado sem quaisquer exemplos.

---

## One-Shot Prompts

Por vezes, pode ser mais fácil fornecer um exemplo do modelo para aprender. Isso é chamado de prompt 'One-Shot'.

Primeiro, vamos fazer um prompt Zero Shot.

*Prompt:*
```
Tell me in which city a university is located.

University: UCLA
```

*Output:*
```
City: Los Angeles, California
```

Digamos que você queria ter um output específico para esse prompt. Você pode fornecer um exemplo para o modelo aprender.

Aqui está um prompt One-Shot que leva ao mesmo output.

*Prompt:*
```
Tell me in which city a university is located.

University: UCLA
City: Los Angeles, CA, USA

University: MIT
```

*Output:*
```
City: Cambridge, MA, USA
```

Observe que você também poderia ter usado o prompt Zero-Shot para este exemplo. Mas os prompts One-Shot são mais flexíveis e podem ser usados para ajustar o modelo às suas necessidades.

Aqui está um equivalente de prompt Zero-Shot.

*Prompt:*
```
Tell me in which city a university is located. Provide the city name, state code and country, comma separated as one line.

University: UCLA
```

*Output:*
```
City: Los Angeles, CA, USA
```

---

## Few-Shot Prompts

Os prompts Few-Shot permitem que você forneça vários exemplos ao modelo para aprender. Isso é útil quando você deseja ajustar o output saída para cenários mais complexos, onde o output pode variar com base na entrada. Também pode ser uma maneira mais simples de definir uma tarefa do que fornecer instruções detalhadas em linguagem natural do que você espera.

Aqui está um exemplo de extração de entidade que é adequado para prompts few-shot.

Vamos tentar primeiro com um prompt Zero-Shot.

*Prompt:*
```
Generate a JSON document that provides the name, position, and company from the text below.

Text: Fred is a serial entrepreneur. Co-founder and CEO of Platform.sh, he previously co-founded Commerce Guys, a leading Drupal e-commerce provider. His mission is to guarantee that as we continue on an ambitious journey to profoundly transform how cloud computing is used and perceived, we keep our feet well on the ground, continuing the rapid growth we have enjoyed up until now.
```

*Output:*
```
{
  "Name": "Fred",
  "Position": "Co-founder and CEO",
  "Company": "Platform.sh, Commerce Guys"
}
```

Não é exatamente o que esperamos (apenas 'Platform.sh' deve estar no campo 'Company'), e pode ser difícil expressar isso em um prompt Zero-Shot. 

Vamos tentar um prompt Few-Shot. Note que vamos deixar cair as instruções e apenas fornecer a saída desejada.

*Prompt:*
```
Text: Fred is a serial entrepreneur. Co-founder and CEO of Platform.sh, he previously co-founded Commerce Guys, a leading Drupal e-commerce provider. His mission is to guarantee that as we continue on an ambitious journey to profoundly transform how cloud computing is used and perceived, we keep our feet well on the ground, continuing the rapid growth we have enjoyed up until now.

JSON:
{
  "Name": "Fred",
  "Position": "Co-founder and CEO",
  "Company": "Platform.sh"
}

Text: Microsoft (the word being a portmanteau of "microcomputer software") was founded by Bill Gates on April 4, 1975, to develop and sell BASIC interpreters for the Altair 8800. Steve Ballmer replaced Gates as CEO in 2000 and later envisioned a "devices and services" strategy.

JSON:
```

*Output:*
```
{
  "Name": "Microsoft",
  "Founder": "Bill Gates",
  "Founded": "April 4, 1975",
  "CEO": "Steve Ballmer",
  "Strategy": "Devices and Services"
}
```

Observe que o output não é o que queremos aqui, mas não houve exemplos suficientes para entender se o objetivo é extrair entidades-chave ou apenas determinadas entidades.

Usando few-shots esclarecerão isso.

*Prompt:*
```
Text: Fred is a serial entrepreneur. Co-founder and CEO of Platform.sh, he previously co-founded Commerce Guys, a leading Drupal e-commerce provider. His mission is to guarantee that as we continue on an ambitious journey to profoundly transform how cloud computing is used and perceived, we keep our feet well on the ground, continuing the rapid growth we have enjoyed up until now.

JSON:
{
  "Name": "Fred",
  "Position": "Co-founder and CEO",
  "Company": "Platform.sh"
}

Text: Microsoft (the word being a portmanteau of "microcomputer software") was founded by Bill Gates on April 4, 1975, to develop and sell BASIC interpreters for the Altair 8800. Steve Ballmer replaced Gates as CEO in 2000 and later envisioned a "devices and services" strategy.

JSON:
{
  "Name": "Bill Gates",
  "Position": "Co-founder and CEO",
  "Company": "Microsoft"
}

Text: Franck Riboud was born on November 7, 1955, in Lyon. He is the son of Antoine Riboud, the previous CEO, who transformed the former European glassmaker BSN Group into a leading player in the food industry. He is the CEO of Danone.

JSON:
```

*Output:*
```
{
  "Name": "Franck Riboud",
  "Position": "CEO",
  "Company": "Danone"
}
```
Agora podemos ver que o modelo entende claramente que queremos extrair apenas três entidades do texto e nada mais.

---

[Secção Anterior (Cenários de exemplo)](./02_Sample_Scenarios/01_Text_Summarization.md)

[Próxima Secção (Fine Tuning)](./04_Fine_Tuning.md)
