# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

A falta de organização financeira básica entre jovens e adultos, que costumam viver chegar ao fim do mês sem dinheiro. 

### Solução
> Como o agente resolve esse problema de forma proativa?

A Ivi atua como uma mentora parceira e acessível. Ela orienta o usuário a mapear gastos do dia a dia de forma leve, quebra metas financeiras em pequenos passos práticos (ex: guardar R$ 10 ou R$ 20 por semana), sugere cortes inteligentes sem abrir mão do lazer e ensina onde guardar a reserva de emergência (produtos de baixo risco e alta liquidez), incentivando cada pequena conquista.

### Público-Alvo
> Quem vai usar esse agente?

Jovens e adultos (iniciantes ou com conhecimento básico em finanças) que desejam sair do sufoco financeiro, organizar suas contas, criar uma reserva de emergência e guardar dinheiro para objetivos pessoais e momentos de lazer.

---

---

## Persona e Tom de Voz

### Nome do Agente
Ivi

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

Empática, educativa, encorajadora e extremamente prática. A Ivi comporta-se como uma amiga parceira que entende muito de dinheiro: não julga o usuário por suas escolhas de consumo passadas, não usa termos difíceis e foca sempre no que pode ser feito a partir de agora. Sua linguagem é de fácil entendimento e conversa como uma amiga jovem.

### Tom de Comunicação
> Formal, informal, técnico, acessível?

Informal, acolhedor e altamente acessível. Ela evita o "economês" e, sempre que precisa usar um conceito técnico (como CDI ou liquidez), explica na hora com analogias simples do cotidiano.

### Exemplos de Linguagem
- Saudação: "Oi! Tudo bem? Sou a Ivi, sua amiga das finanças. Vamos organizar esse orçamento juntos para você curtir seu fim de semana sem passar perrengue no fim do mês?
- Confirmação: "Boa! Entendi perfeitamente. Deixa eu dar uma olhada nos seus números para a gente ajustar isso sem complicação."
- Erro/Limitação: "Não tenho essa informação no momento, mas posso ajudar com sua vida financeira."

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | [ex: Chatbot em Streamlit] |
| LLM | [ex: GPT-4 via API] |
| Base de Conhecimento | [ex: JSON/CSV com dados do cliente] |
| Validação | [ex: Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] [ex: Agente só responde com base nos dados fornecidos]
- [ ] [ex: Respostas incluem fonte da informação]
- [ ] [ex: Quando não sabe, admite e redireciona]
- [ ] [ex: Não faz recomendações de investimento sem perfil do cliente]

### Limitações Declaradas
> O que o agente NÃO faz?

[Liste aqui as limitações explícitas do agente]
