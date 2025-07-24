# Teste para Candidato a Analista de Back-end

Prezado(a) desenvolvedor(a),

Bem-vindo(a) ao Teste para Candidato(a) a Analista de Back-end. Este teste tem como objetivo avaliar seu conhecimento geral e velocidade de desenvolvimento. Abaixo, você encontrará os detalhes e requisitos para este teste.

**O Desafio**

Sua tarefa é desenvolver uma API usando Node.js para um sistema de gerenciamento de catálogo de produtos em um aplicativo de marketplace. Você deve analisar e converter as seguintes histórias de usuário em rotas para a aplicação:

**Histórias de Usuário:**

- Como usuário, quero cadastrar um produto com seu proprietário, para que eu possa acessar seus dados no futuro (título, descrição, preço, categoria, ID do proprietário).
- Como usuário, quero cadastrar uma categoria com seu proprietário, para que eu possa acessar seus dados no futuro (título, descrição, ID do proprietário).
- Como usuário, quero associar um produto a uma categoria.
- Como usuário, quero atualizar os dados de um produto ou categoria.
- Como usuário, quero excluir um produto ou categoria do meu catálogo.
- Um produto só pode ser associado a uma categoria por vez.
- Assuma que produtos e categorias pertencem a apenas um proprietário.

- Tenha em mente que este é um catálogo de produtos online, o que significa que haverá múltiplas requisições para edição de itens/categorias por segundo, bem como acesso ao endpoint de busca do catálogo.
- Considere o catálogo de produtos como uma compilação JSON de todas as categorias e itens disponíveis de propriedade de um usuário. Dessa forma, o endpoint de busca do catálogo não precisa buscar informações do banco de dados.
- Sempre que houver uma alteração no catálogo de produtos, publique essa alteração no tópico "catalog-emit" no serviço AWS SQS.
- Implemente um consumidor que escute as alterações do catálogo para um proprietário específico.
- Quando o consumidor receber uma mensagem, procure no banco de dados o catálogo desse proprietário, gere o JSON do catálogo e publique-o em um bucket do serviço AWS S3.

**Você precisa desenvolver este teste usando as seguintes tecnologias:**

- MongoDB para o banco de dados.
- AWS SQS para as notificações de alteração do catálogo.
- AWS S3 para armazenar o JSON do catálogo.
- Node.js para o backend.
- Express.js como o framework web.

---

**Diagrama representando a estrutura final do projeto:** <br><br>
![image](https://github.com/githubanotaai/new-test-backend-nodejs/assets/52219768/504ba448-f128-41db-ae86-18dc19c0dc9d)

---

**Instruções**

**Para iniciar o teste, faça um fork deste repositório, crie uma branch com seu nome completo e nos envie o link para o seu teste concluído (link para o seu repositório). Se você apenas clonar o repositório, não conseguirá fazer push das alterações, tornando o pull request mais complicado.**
- Use sua própria conta AWS para configurar os serviços necessários.
- Atualize o arquivo README com instruções sobre como executar sua aplicação.
- Cole o nome da branch no sistema GUPY e indique a conclusão do teste.
- Sinta-se à vontade para nos fornecer feedback sobre o teste.

**Nossos Critérios de Avaliação**
Avaliaremos os seguintes aspectos da sua solução:

- Conhecimento de JavaScript, Node.js e Express.js.
- Estrutura adequada das camadas da aplicação.
- Tratamento de chamadas de saída (outgoing calls).
- Uso eficaz de variáveis de ambiente.
- Implementação de testes unitários.
- Mecanismos de logging.
- Estratégias de tratamento de erros.
- Qualidade da documentação.
- Organização do código, separação de módulos, legibilidade e comentários.
- Histórico de commits.