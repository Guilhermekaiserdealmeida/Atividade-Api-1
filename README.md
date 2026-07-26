1) Criar um projeto Springboot (https://start.spring.io)

Adicionar as dependencias:

Springweb e Lombok



2) Criar a estrutura de pasta:



Controller

Service

Entity





3) Criar uma API REST que receba os dados de uma pessoa e informe se ela possui direito a atendimento prioritário



Controller e Service atendimentos



Endpoint

POST /api/atendimentos/classificar (@PostMapping("classificar"))



Fazer a entidade Entradas que atenda os campos com Lombok:

{
 "nome": "Maria", // String
 "idade": 65,          // Integer
 "gestante": false, // Boolean
 "pessoaComDeficiencia": false // Boolean
}


Regra de negócio:

O atendimento será PRIORITARIO quando:
A idade for maior ou igual a 60 anos;
A pessoa estiver gestante;
A pessoa possuir alguma deficiência.


Fazer a entidade Saidas que atenda os campos com Lombok:

{
  "nome": "Maria", //String
  "tipoAtendimento": "PRIORITARIO", //String
  "mensagem": "Pessoa com direito a atendimento prioritário." //String
}                                                                     


Estrutura obrigatoria:

AtendimentoController: recebe o POST.
AtendimentoService: aplica a regra de negócio.
Entidade Entrada e Saida: representa os dados de entrada e saída.
