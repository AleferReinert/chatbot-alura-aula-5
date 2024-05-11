# Imersão IA - Alura/Google - Aula 5

Chatbot que entrega respostas baseadas em documentos específicos (passados por mim). Ou seja, tenho total controle do conteúdo gerado.

## Como funciona
### Busca semântica
1. É feito uma comparação entre o **texto digitado pelo usuário** e todas as **respostas no conteúdo do documento**.
2. A **resposta do conteúdo** que tiver maior semelhança com o **texto digitado pelo usuário** será retornada.
3. A resposta retornada será exatamente igual está no documento.

#### Exemplo
##### Meu documento:
|Título|Conteúdo|
|------|--------|
|Abordagens|As abordagens mais populares da psicologia são TCC, terapia do Esquema...|
|Respiração diafragmática|Para fazer a respiração diafragmática você deve seguir...|
|Receitas|Para fazer um bolo de cenoura é necessário...|

**Texto digitado pelo usuário:** *Como faço um bolo?*

**Texto retornado:** *Para fazer um bolo de cenoura é necessário...*

### Personalização
Agora que temos uma resposta escolhida para devolver ao usuário, é feito um **prompt** através do Gemini para modifica-lá.

#### Exemplo
```
resposta = 'Para fazer um bolo de cenoura é necessário...'

prompt = f'Reescreva o texto de forma descontraida, sem adicionar informações que não façam parte do texto: {resposta}'
```

**Texto retornado:** *Bolo de cenoura: Missão Impossível? Nah, só precisa de...*
