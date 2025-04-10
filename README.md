# 🧠 Análise de Sentimentos de Avaliações de Call Center com Azure AI

Este projeto simula e analisa **feedbacks reais de clientes** após interações com um call center, utilizando os **serviços de linguagem do Azure Cognitive Services** para identificar sentimentos, emoções e padrões de comportamento.

---

## 📌 Objetivo

Explorar como **IA pode interpretar feedbacks textuais** — mesmo com erros ortográficos, linguagem informal e gírias — e extrair **insights úteis** para empresas de atendimento ao cliente.

---

## 🛠️ Tecnologias e Ferramentas

- 💬 **Azure Cognitive Services – Language Studio**
- ☁️ Azure AI - Análise de Texto (Text Analytics)
- 📄 Linguagem informal e erros propositalmente inseridos
- ✍️ Markdown para documentação
- 📁 JSON com simulações de comentários

---
> 🖼️ *Análise de sentimentos feita no Azure Language Studio com frases simuladas:*

<p align="center">
  <img src="https://github.com/user-attachments/assets/4a84e1db-f4cc-4a6b-988b-11d3bf1f1dbd" alt="Sentença analisada: 'fui mt bem atendido, a moça resolveu rapidinhu, show!'" width="1000"/><br>
  <sub><i>Sentença analisada: "fui mt bem atendido, a moça resolveu rapidinhu, show!" – Classificada como Positiva</i></sub>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/0198b2e9-e6d9-46be-bf4e-798f88e667b2" alt="Sentenças 9 e 10 analisadas" width="1000"/><br>
  <sub><i>Sentenças 9 e 10 – Destaques como "ligação caiu" e "tempo de espera" extraídos como frases-chave</i></sub>
</p>

## 🧪 Como foi feito

### 1. **Simulação de Comentários**
- Criei uma coleção de frases simulando avaliações reais de usuários após ligações para um call center.
- Os comentários possuem **variações naturais** de escrita: gírias, abreviações, erros de português e diferentes tons emocionais (elogios, reclamações, sugestões).

Exemplo de comentários simulados:

```json
[
  "fui mt bem atendido, a moça resolveu rapidinhu, show!",
  "péssimo atendimento. Fiquei esperando e dps desligaram na minha cara. NUNCA mais volto a liga",
  "o atendimento foi educado mas num resolveram meu caso, entaum né... meio a meio"
]

````
### 2. 📤 Upload no Azure Language Studio

- Acessei o [Azure Language Studio](https://language.azure.com/)
- Usei a funcionalidade **"Análise de Sentimentos e Emoções"**
- Copiei os comentários no campo de entrada
- O Azure retornou:
  - ✅ Classificação de **sentimento** (positivo, neutro ou negativo)
  - 💬 **Frases-chave** relacionadas ao conteúdo
  - 📊 **Pontuação de confiança** para cada análise
  
---

### 3. 📊 Análise dos Resultados

- 🟢 Comentários com erros como “resolvero” ou “valeuzao” foram **corretamente interpretados como positivos**
- 🔴 Reclamações com tom negativo foram **detectadas mesmo com abreviações ou erros ortográficos**
- 🧠 O serviço de IA conseguiu **extrair frases-chave úteis** como:
  - `"tempo de espera"`
  - `"ligação caiu"`
  - `"educada"`
  - `"problema resolvido"`
