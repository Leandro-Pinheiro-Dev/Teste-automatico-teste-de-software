
### ✅ **README.md (Versão Final Profissional + Imagens Lado a Lado)**

# 🧪 Sistema Bancário - Testes de Software (JUnit + Testes Manuais)

Este repositório apresenta um projeto de testes aplicado sobre um **Sistema Bancário Simples**, com foco no estudo e prática das principais técnicas de **Teste de Software**, conforme abordado no curso do professor **Gustavo Farias**.

Foram aplicados:
- ✅ **Testes Automatizados** utilizando **JUnit 4**
- ✅ **Testes Manuais** estruturados em cenários e casos de validação funcional

O objetivo central é demonstrar a importância da Garantia de Qualidade (QA) no ciclo de desenvolvimento e como testes bem planejados reduzem falhas e aumentam a confiabilidade do sistema.


## 🏛 Estrutura do Sistema Testado


src/
└─ negocio/
├─ Cliente.java
├─ ContaCorrente.java
├─ GerenciadoraClientes.java
├─ GerenciadoraContas.java
└─ IdadeNaoPermitidaException.java

### Principais Regras Validada no Sistema:
- Cadastro e remoção de clientes
- Validação de idade mínima
- Transferência de valores entre contas
- Consulta e alteração de saldo


## 🤖 Testes Automatizados com JUnit

A automação está localizada em:


testes/
└─ negocio/
├─ GerenciadoraClientesTest_Ex1.java
├─ GerenciadoraClientesTest_Ex2.java
├─ ...
├─ GerenciadoraContasTest_Ex6.java
└─ TodosOsTestes.java   ← Suite para execução geral


### ✔️ Execução da Suíte de Testes

```java
@RunWith(Suite.class)
@SuiteClasses({
    GerenciadoraClientesTest_Ex1.class,
    GerenciadoraClientesTest_Ex2.class,
    ...
    GerenciadoraContasTest_Ex6.class
})
public class TodosOsTestes { }
````

### 📷 Evidência de Execução (Lado a Lado)

| Execução dos Testes                            | Estrutura e Organização                       |
| ---------------------------------------------- | --------------------------------------------- |
| ![execucao](./readme_img/execucao_teste_1.png) | ![projeto](./readme_img/execucao_teste_2.png) |

---

## 📝 Testes Manuais

Além dos testes automatizados, foram definidos cenários funcionais, seguindo critérios claros de entrada e validação:

| ID   | Cenário           | Entrada            | Resultado Esperado                   | Status |
| ---- | ----------------- | ------------------ | ------------------------------------ | ------ |
| CT01 | Cadastro válido   | Nome + Idade >= 18 | Cliente cadastrado com sucesso       | ✅      |
| CT02 | Cadastro inválido | Idade < 18         | Exceção `IdadeNaoPermitidaException` | ✅      |
| CT05 | Transferência     | Conta A → Conta B  | Saldo atualizado corretamente        | ✅      |

---

## 🔍 Boas Práticas Aplicadas

* Estruturação clara de casos positivos e negativos
* Assertivas com mensagens explicativas (`assertTrue`, `assertEquals`, `assertThrows`, etc.)
* Separação entre **lógica de negócio** e **escopo de teste**
* Consideração de **valores limite**, estados inválidos e exceções
* Suite centralizada para **testes de regressão**

---

## 🚀 Como Executar o Projeto

1. Importar o projeto no **Eclipse** (ou outra IDE Java)
2. Verificar se o **JUnit 4** está adicionado ao *Build Path*
3. Executar:

   ```
   testes/negocio/TodosOsTestes.java → Run As → JUnit Test
   ```

---

## 👤 Autor

**Leandro Santos**
🔗 GitHub: [https://github.com/Leandro-Pinheiro-Dev](https://github.com/Leandro-Pinheiro-Dev)

---

> *“O testador não procura apenas erros — ele protege a experiência do usuário.”*

```

---

### ✅ Agora falta **apenas 1 passo:**

Crie esta pasta no seu repositório:

```

/readme_img

```

E salve dentro dela:

| Nome sugerido | Conteúdo |
|---------------|----------|
| `execucao_teste_1.png` | Print da tela de execução JUnit |
| `execucao_teste_2.png` | Print da estrutura do projeto no Eclipse |

Se quiser, posso **cortar, ajustar contraste e padronizar o tamanho das imagens** para ficar mais profissional.  
Quer que eu faça isso?  
**Responda: SIM** e me envie **as duas imagens** aqui.
```
