# Documentação de Análise da API - ReqRes

## 1. Cenário A: Listar Utilizadores da Página 2
* **Verbo HTTP:** GET
* **URL Completa:** https://reqres.in/api/users?page=2
* **Body da Requisição:** Nenhum
* **Status Code Esperado:** 200 OK
* **Resposta da API (Exemplo do JSON):**
```json
{
    "page": 2,
    "per_page": 6,
    "total": 12,
    "total_pages": 2,
    "data": [
        {
            "id": 7,
            "email": "michael.lawson@reqres.in",
            "first_name": "Michael",
            "last_name": "Lawson",
            "avatar": "[https://reqres.in/img/faces/7-image.jpg](https://reqres.in/img/faces/7-image.jpg)"
        },
        {
            "id": 8,
            "email": "lindsay.ferguson@reqres.in",
            "first_name": "Lindsay",
            "last_name": "Ferguson",
            "avatar": "[https://reqres.in/img/faces/8-image.jpg](https://reqres.in/img/faces/8-image.jpg)"
        }
    ],
    "support": {
        "url": "[https://reqres.in/#support-heading](https://reqres.in/#support-heading)",
        "text": "To keep ReqRes free, contributions towards server costs are appreciated!"
    }
# Pesquisa: Diferença entre API, LIB e SDK

Embora esses três termos sejam fundamentais no desenvolvimento de software e frequentemente usados juntos, eles representam conceitos e escopos completamente diferentes. A principal diferença reside no **tamanho (escopo)** e na **função** que cada um exerce no ecossistema de desenvolvimento.

---

## 1. API (Application Programming Interface)
Uma API (Interface de Programação de Aplicações) é um conjunto de regras, protocolos e definições que permite que duas aplicações de software diferentes se comuniquem entre si. 

* **O que é:** É o "mensageiro" ou o "contrato". Ela não é a implementação do código em si, mas sim a definição de como você pode interagir com esse código.
* **Como funciona:** Você (o desenvolvedor) envia uma requisição estruturada de uma forma específica, e a API devolve uma resposta (geralmente em JSON ou XML) sem que você precise saber como o sistema processou essa informação.
* **Controle:** O sistema remoto dita as regras. Se você não enviar a requisição exatamente como a API exige, ela falha.
* **Exemplos:** ReqRes, Google Maps API, Stripe API.

## 2. LIB (Library / Biblioteca)
Uma Biblioteca é uma coleção de código pré-escrito e reutilizável que os desenvolvedores podem importar para seus próprios projetos para realizar tarefas específicas e comuns, evitando "reinventar a roda".

* **O que é:** É um conjunto de funções e blocos de código focados em resolver um problema específico (como fazer cálculos matemáticos, manipular datas ou criar interfaces visuais).
* **Como funciona:** O seu código "chama" a biblioteca quando precisa dela. 
* **Controle:** **Você está no controle.** Você decide quando, onde e como vai usar os recursos da biblioteca dentro do fluxo do seu programa.
* **Exemplos:** React (interfaces), Axios (requisições HTTP), NumPy (matemática em Python).

## 3. SDK (Software Development Kit)
Um SDK (Kit de Desenvolvimento de Software) é uma caixa de ferramentas completa fornecida por um fabricante de plataforma para permitir que você crie aplicativos especificamente para aquele ambiente.

* **O que é:** É o pacote mais abrangente de todos. Um SDK geralmente **contém** bibliotecas (LIBs) e APIs, mas vai muito além, incluindo compiladores, depuradores (debuggers), documentação e exemplos de código.
* **Como funciona:** Ele fornece tudo o que você precisa para começar e terminar um projeto para uma plataforma específica.
* **Controle:** Ele define as ferramentas base que você vai usar para construir a aplicação inteira.
* **Exemplos:** Android SDK (apps Android), iOS SDK (apps Apple), AWS SDK (serviços Amazon).

---

## O Resumo das Diferenças

Um não substitui o outro; eles se complementam. 

| Característica | API | LIB (Biblioteca) | SDK |
| :--- | :--- | :--- | :--- |
| **Definição Base** | Ponte de comunicação entre sistemas. | Código pré-escrito para funções específicas. | Kit completo de ferramentas para criar software. |
| **O que contém?** | Regras, rotas e protocolos. | Classes, métodos e funções prontas para uso. | APIs, Bibliotecas, compiladores e documentação. |
| **Quem chama quem?** | Seu código faz uma requisição para a API. | Seu código chama as funções da Biblioteca. | Você usa o SDK para construir o seu código. |
| **Nível de Escopo** | Específico (Comunicação). | Específico (Execução de tarefa). | Amplo (Construção completa). |

## Analogia para Fixação

Imagine que você quer construir um móvel de madeira:

1. A **LIB (Biblioteca)** é como uma ferramenta (furadeira ou martelo) que você comprou. Ela faz o trabalho pesado, e você decide quando usá-la.
2. A **API** é como o balcão de atendimento da loja de materiais. Você não pode ir direto ao estoque; precisa preencher um pedido (requisição) para o atendente (API) trazer a madeira exata para você.
3. O **SDK** é como uma "Oficina Completa em uma Caixa" fornecida por uma marca. Lá dentro vem a madeira, os parafusos (bibliotecas), o manual de instruções (documentação) e as ferramentas certas. Tudo para construir aquele projeto.
}
