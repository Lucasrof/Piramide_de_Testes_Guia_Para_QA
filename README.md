# O que é a Pirâmide de Testes? Um guia para Qualidade no Desenvolvimento de Software

Bem-vindo ao guia da Pirâmide de Testes, um conceito essencial para estruturar testes de software de forma eficiente, garantindo qualidade, velocidade e baixo custo.

---

## Sobre

A **Pirâmide de Testes** é um modelo que organiza os testes de software em camadas.
A ideia é simples, criar uma base ampla de testes rápidos e baratos (como **testes unitários**) e reduzir a quantidade à medida que os testes ficam mais complexos (como **testes de UI ou manuais**).

Esse conceito é amplamente usado em equipes ágeis para entregar software robusto sem sacrificar a velocidade.

---

## Objetivos

- Entender a estrutura da pirâmide de testes;
- Aprender como cada camada contribui para a qualidade do software;
- Aplicar boas práticas para evitar problemas comuns;
- Implementar a pirâmide em projetos reais com exemplos práticos.

---

## Estrutura da Pirâmide de Testes

A pirâmide é organizada em **camadas**, de sua base (testes rápidos e numerosos, geralmente **automatizados**) ao topo (testes complexos e escassos, geralmente **manuais**).

### Testes Unitários

* **O que são?** Testes que verificam unidades individuais de código, como funções ou métodos.
* **Por que são importantes?** São rápidos, baratos e ajudam a identificar bugs logo no início.
* **Exemplo:** Função de desconto retorna `80` para entrada `100` com `20%`.
* **Quantidade:** Muitos (centenas ou milhares).
* **Ferramentas:** JUnit, pytest, Jest.
* **Boa prática:** Utilize *mocks* ou *stubs* para isolar dependências externas.

### Testes de Integração

* **O que são?** Validam a interação entre diferentes módulos ou serviços.
* **Por que são importantes?** Garantem que os componentes funcionam corretamente quando integrados.
* **Exemplo:** API REST salva pedido no banco de dados e retorna a resposta esperada.
* **Quantidade:** Menos que os testes unitários, mas ainda significativos.
* **Ferramentas:** Testcontainers, WireMock.
* **Boa prática:** Concentre-se nas interações entre componentes.

### Testes de API/Serviço

* **O que são?** Validam o comportamento de APIs ou serviços, simulando chamadas de clientes.
* **Por que são importantes?** Garantem que APIs respondem corretamente a diferentes cenários.
* **Exemplo:** POST `/api/usuarios` retorna `201`.
* **Quantidade:** Menor que os de integração.
* **Ferramentas:** Postman, RestAssured, Supertest.
* **Boa prática:** Use contratos (ex.: OpenAPI).

### Testes de Interface do Usuário (UI)

* **O que são?** Simulam interações do usuário na interface, como cliques ou formulários.
* **Por que são importantes?** Validam a experiência real do usuário.
* **Exemplo:** Verificar se formulário exibe mensagem de sucesso após envio.
* **Quantidade:** Poucos, devido à fragilidade e tempo de execução.
* **Ferramentas:** Selenium, Cypress, Playwright.
* **Boa prática:** Reserve para fluxos críticos (ex.: checkout de e-commerce).

### Testes Manuais

* **O que são?** Testes realizados por humanos (exploratórios ou de usabilidade).
* **Por que são importantes?** Capturam nuances que automatizados não conseguem.
* **Exemplo:** Avaliar se a experiência de um formulário é intuitiva.
* **Quantidade:** Muito poucos, devido ao alto custo e demora.
* **Boa prática:** Use apenas em cenários que exigem julgamento humano.

---

## Benefícios da Pirâmide

* **Velocidade:** Testes unitários rodam em milissegundos.
* **Custo:** Testes da base são baratos de criar e manter.
* **Estabilidade:** Testes unitários e de integração quebram menos.
* **Confiança:** Base sólida reduz dependência de testes manuais.

---

## Como Implementar

1. **Construa a Base:** Escreva testes unitários para as principais funcionalidades.
2. **Planeje Camadas Intermediárias:** Crie testes de integração e API para pontos críticos.
3. **Automatize:** Minimize testes manuais, reservando-os para casos específicos.
4. **Integre ao CI/CD:** Configure pipelines (GitHub Actions, Jenkins, CircleCI).
5. **Monitore:** Use métricas de cobertura (ex.: 80% para unitários).

---

## Dúvidas, contato ou sugestões? 
-- 💼 **LinkedIn**: [Lucas Rosa](https://www.linkedin.com/in/lucasrosaf)
