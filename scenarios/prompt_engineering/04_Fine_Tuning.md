# Exercício 4C: Fine Tuning (Apenas leitura)

## Tópicos

  - [O que é Fine Tuning?](#what-is-fine-tuning)
  - [Quando você consideraria Fine Tuning vs Prompt Engineering?](#when-would-you-consider-fine-tuning-vs-prompt-engineering)
  - [Considerações sobre o custo da operação](#operation-cost-considerations)


---
## O que é Fine Tuning?

O Fine-tuning é o processo de personalizar um modelo de IA existente para uma tarefa ou domínio específico usando dados adicionais. A OpenAI oferece fine-tuning para seus modelos de linguagem, como o GPT-3, que pode gerar textos em linguagem natural para vários fins.

Fine-tuning permite que os usuários criem modelos personalizados que podem produzir resultados mais precisos e relevantes do que os modelos gerais.~

Para ajustar um modelo OpenAI, os usuários precisam preparar seus próprios dados de treinamento e validação, selecionar um modelo base e usar a CLI ou o Studio do OpenAI para iniciar o trabalho de fine-tuning.

O fine-tuning pode melhorar o desempenho e reduzir significativamente as taxas de erro dos modelos OpenAI.

---
## Fine Tuning Dados de treinamento

Os dados de treinamento para ajustar modelos de OpenAI são pares de prompts de entrada e saídas desejadas que refletem a tarefa ou o domínio específico para o qual você deseja personalizar o modelo. Por exemplo, se você quiser ajustar um modelo para gerar avaliações de produtos, seus dados de treinamento poderão ter esta aparência:

```
{"prompt": "Review: I bought this laptop for my online classes and it works great.", "completion": "Rating: 5 stars"}
{"prompt": "Review: The battery life is terrible and the screen is too small.", "completion": "Rating: 2 stars"}
{"prompt": "Review: This is a scam. The product never arrived and the seller did not respond.", "completion": "Rating: 1 star"}
```

Você pode usar o OpenAI CLI ou Studio para preparar, validar e formatar os seus dados de treinamento em um arquivo JSON que pode ser usado para fine-tuning.


**IMPORTANT NOTE**:
É importante notar que, para esperar melhores resultados do que usar Prompt Engineering, você precisará ter um conjunto de dados grande e de alta qualidade que seja relevante para a sua tarefa ou domínio, geralmente algumas centenas de exemplos de alta qualidade.

---
## Quando você consideraria Fine Tuning vs Prompt Engineering?

O Fine-tuning é uma ferramenta poderosa que pode ser usada para personalizar modelos de OpenAI para tarefas ou domínios específicos. No entanto, nem sempre é necessário ajustar um modelo para obter os resultados desejados.

O Fine-tuning e a Prompt Engineering são dois métodos de condicionamento de modelos de linguagem para executar tarefas ou domínios específicos

O Fine-tuning envolve o retreinamento de um modelo existente com novos dados, enquanto a Prompt Engineering envolve projetar e testar instruções de entrada que obtêm o output desejado de um modelo.

### Fine Tuning

Você pode considerar o fine-tuning quando tiver um conjunto de dados grande e de alta qualidade que seja relevante para sua tarefa ou domínio e quiser criar um modelo personalizado que possa produzir ouputs mais precisos e consistentes do que o modelo geral.

### Prompt Engineering

Você pode considerar Prompt Engineering quando tiver um conjunto de dados limitado ou inexistente e quiser aproveitar o conhecimento e os recursos existentes de um modelo geral fazendo as perguntas certas ou fornecendo o contexto certo. 

**NOTA IMPORTANTE**: Ambos os métodos exigem alguma tentativa e erro, mas o fine-tuning geralmente leva mais tempo e recursos do que a Prompt Engineering, e nem sempre é necessário ajustar um modelo para obter os resultados desejados. Portanto, é preferível começar com Prompt Engineering e só considerar o fine-tuning se você não conseguir obter os resultados desejados.

---

## Considerações sobre o custo da operação

Prompt engineering pode ser menos econômica se você precisar fornecer um grande número de instruções para realizar algo semelhante ao que você obteria com um modelo Fine Tuned, pois consumiria tokens a cada solicitação enviada.

Hospedar um modelo Fine Tune também tem seu custo, mas em volumes médios a altos, esse custo seria praticamente irrelevante, então a eficiência de custos operacionais poderia ser um impulsionador do Fine Tuning.

---
## Referências

[OpenAI Fine Tuning](https://platform.openai.com/docs/guides/fine-tuning)

[Fine Tuning no serviço Azure OpenAI](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/how-to/fine-tuning?pivots=programming-language-studio)


---

[Secção Anterior (Conceitos Avançados)](./03_Advanced_Concepts.md)
