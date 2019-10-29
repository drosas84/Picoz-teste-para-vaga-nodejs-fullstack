
# Picoz - teste para a vaga de desenvolvedor FullStack em NodeJS
Obrigado por disponibilizar o seu tempo para realizar o teste de habilidades como desenvolvedor Fullstack em NodeJS.

## Sobre a Picoz
Picoz é uma startup que auxilia empresas e pessoas a encontrarem espaços para realizarem eventos corporativos e pessoais. Contamos com mais de 70 espaços cadastrados na plataforma e temos auxiliado anfitriões gerenciarem e alocarem os seus espaços.

## Nossa tecnologia
Atualmente nosso sistema está construído com Ruby on Rails e React. Mas estamos migrando todos os serviços em Ruby on Rails para Node.JS.

## Sobre o processo seletivo
1. Nessa primeira etapa queremos te conhecer um pouco mais, saber sobre projetos que já executou e fazer algumas perguntinhas técnicas.
2. Teste técnico, não deve demorar mais do que 3 dias para você realizar esse teste.
3. Proposta de contrato
4. Contratação

## Sobre o teste
### Requisitos:
- Usar o Node.JS na última versão estável
- Você pode utilizar o framework de sua preferência: Express, Hapi ou outros
- Lint Aibnb Style Guide
- API Restful

Crie um aplicativo backend que exporta uma API RESTful de criação de produtos.

Todos os endpoints devem somente aceitar e somente enviar JSONs.
O servidor sempre deverá retornar JSON, quando o endpoint não puder ser encontrado.

O aplicativo deverá persistir dados, você pode usar qualquer banco de dados ou ORM.

Todas as respostas de erro devem retornar o seguinte objeto:

```javascript
{ "erro": "mensagem de erro"}
```

### Criação de produto
Este endpoint deverá receber um produto com os seguintes campos: nome, tipo, preço, lista de lojas.

**Modelo esperado:**

```javascript
{ 
  "nome": "Fonte",
  "tipo": "Eletrônico",
  "preco": 10.40,
  "lojas": [
     {
       "nome": "Picoz",
       "bairro": "Pinheiros"
     }
  ]
}
```

- Utilizar os status codes
- Em caso de sucesso irá retonar um usuário mais os seguintes campos:
  - `id` : id do produto (pode ser o gerado pelo banco ou um GUID)
  - `createdAt` : data de criação do produto
  - `updateAt` : data da última atualização do produto
 - Caso o produto já exista, deverá retornar o erro com a mensagem "Produto já cadastrado"
 
### Adicionar loja
 - Este endpoint irá receber um objeto com `id`, `nome` e `bairro`
 - Caso o id exista deve retornar o endpoint igual ao de criação de produto
 - Não pode existir duas lojas com o mesmo nome no meso bairro.
 
### Buscar produto
- Organizar as rotas para que seja possível:
  - Buscar todos os produtos
  - Buscar produto por id
  - Buscar produto por bairro
  - Buscar produto por nome do produto
  - Buscar produto por nome da loja
  
## Mini Front-end
Possibilitar que o usuário cadastre, veja a lista de produtos e busque um produto.
 
### Requisitos
- Qualquer framework para Javascript
- Separa por componentes
- Testes unitários

## Não obrigatórios
- Busca com unbounce
- Configurar os ambientes de desenvolvimento, homologação e produção
