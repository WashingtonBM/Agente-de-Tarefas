# 🤖 AGENTE DE TAREFAS TRELLO COM PYTHON

Sistema automatizado de gerenciamento de tarefas utilizando Python e API do Trello.
O agente monitora cards continuamente, classifica prioridades automaticamente e move tarefas entre listas do board em tempo real.

---
## 💻 Sobre o Projeto:

# 🚀 Funcionalidades

✅ Monitoramento contínuo do Trello
✅ Integração com API REST do Trello
✅ Classificação automática de tarefas
✅ Movimentação automática de cards
✅ Execução em loop contínuo
✅ Tratamento de erros
✅ IA local sem custo
✅ Sem dependência de APIs pagas
✅ Estrutura pronta para produção

---

# 🧠 Como o Agente Funciona

O agente:

1. Consulta os cards do board
2. Analisa nome e descrição da tarefa
3. Classifica a prioridade automaticamente
4. Move o card para a lista correspondente
5. Aguarda alguns segundos
6. Reinicia o ciclo automaticamente

---

# 📌 Estrutura de Prioridades

| Palavra-chave                 | Prioridade |
| ----------------------------- | ---------- |
| urgente, erro, falha, crítico | Alta       |
| teste, revisar, ajustar       | Média      |
| demais tarefas                | Baixa      |

---

# 📂 Estrutura do Projeto

```bash
AGENTE_DE_TAREFAS/
│
├── app.py
├── README.md
├── venv/
```

---

# 🛠 Tecnologias Utilizadas

* Python 3
* Requests
* API REST Trello

---

# 🔐 Configuração do Trello

## 1. Gerar API KEY

Acesse:

```bash
https://trello.com/app-key
```

Copie sua:

* API KEY

---

## 2. Gerar TOKEN

Abra no navegador:

```bash
https://trello.com/1/authorize?expiration=never&name=AgentePython&scope=read,write&response_type=token&key=SUA_KEY
```

Copie o token gerado.

---

# ⚙️ Configuração do Projeto

No arquivo `app.py`:

```python
TRELLO_KEY = "SUA_KEY"
TRELLO_TOKEN = "SEU_TOKEN"
BOARD_ID = "SEU_BOARD_ID"
```

---

# ▶️ Como Executar

## 1. Criar ambiente virtual

```bash
python -m venv venv
```

---

## 2. Ativar ambiente virtual

### Windows

```bash
venv\Scripts\activate
```

### Linux / Mac

```bash
source venv/bin/activate
```

---

## 3. Instalar dependências

```bash
pip install requests
```

---

## 4. Executar o agente

```bash
python app.py
```

---

# 📋 Exemplo de Execução

```bash
🤖 AGENTE INICIADO...

STATUS LISTS: 200
STATUS CARDS: 200

📌 Card: Corrigir erro no sistema
🧠 Categoria: alta_prioridade
🎉 Card movido com sucesso!

⏳ Aguardando 15 segundos...
```

---

# 🧠 Lógica de Classificação

```python
def classificar_com_ia(nome, descricao=""):
    texto = (nome + " " + descricao).lower()

    if any(x in texto for x in ["urgente", "erro", "falha", "crítico"]):
        return "alta_prioridade"

    if any(x in texto for x in ["teste", "revisar", "ajustar"]):
        return "media_prioridade"

    return "baixa_prioridade"
```

---

# 🔄 Fluxo do Sistema

```text
Trello → Leitura de Cards
        ↓
Classificação Inteligente
        ↓
Movimentação Automática
        ↓
Loop Contínuo
```

---

# 🛡 Tratamento de Erros

O sistema possui:

* validação de resposta da API
* logs automáticos
* retry automático
* proteção contra falhas do Trello

---

# 📈 Melhorias Futuras

* Dashboard web
* Integração com WhatsApp
* Notificações Telegram
* Banco de dados
* Deploy em nuvem
* Multiagentes
* IA avançada

---

# 👨‍💻 Autor

Projeto desenvolvido por Washington Brito.

---

# 📄 Licença

Este projeto é livre para estudos, melhorias e adaptações.

----------------------------------------------------------
---------

## 📚 Pré-requisitos de Habilidades e Níveis de Conhecimento

Antes de ingressar neste conteúdo, é necessário possuir conhecimento prévio nas seguintes áreas:

- [habilidades ou conhecimentos prévios necessários] | [Básico, Intermediário, Avançado ou Especialista]

- _Exemplo_:

  - Java | Básico
  - Gerenciamento de pacotes | Básico
  -

- [Outros pré-requisitos, se aplicável]

- _Exemplo_:
  - Lógica de programação
  - Javascript

## 🛠️ Habilidades e Sub-habilidades que vamos aprender neste conteúdo

- [Lista das habilidades principais a serem desenvolvidas]

  - [Subhabilidades relacionadas, se aplicável]

- _Exemplo_:
  - Java
    - Api Rest

## 🎯 Objetivos e Resultados Esperados

Após a conclusão do curso/projeto, os estudantes estarão aptos a:

- [Descrição do que os estudantes serão capazes de fazer]
- [Projetos ou soluções que os estudantes estarão aptos a construir]

<!--START_SECTION:footer-->

<br />
<br />

<p align="center">
  <a href="https://www.dio.me/" target="_blank">
    <img align="center" src="https://raw.githubusercontent.com/digitalinnovationone/template-github-trilha/main/.github/assets/footer.png" alt="banner"/>
  </a>
</p>
