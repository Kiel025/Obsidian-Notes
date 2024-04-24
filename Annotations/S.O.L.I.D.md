## 1. S - Single Responsibility Principle (Princípio da Responsabilidade Única)

O Princípio da Responsabilidade Única implica que uma classe deve ter apenas uma especialização dentro do software, tendo que lidar com apenas uma tarefa.

O SRP não se limita somente a classes, mas tudo que puder realizar mais de uma tarefa, como funções e métodos. 

Cada função/método/classe deve ser responsável por ela mesma, por aquilo que se propõe a fazer, evitando a criação de "God Classes" em que teríamos uma classe que faria de tudo e seria de difícil manutenção.

## 2. O - Open-Closed Principle (Princípio Aberto-Fechado)

O Princípio Aberto-Fechado diz que toda classe deve estar aberta para adição de uma nova funcionalidade mas fechada pra modificação das já existentes.

Esse princípio existe para evitarmos querer alterar um código que já existe e funciona corretamente para adicionar algo novo e talvez quebrar alguma implementação que já funcione normalmente. 

Nesse caso, o que deveríamos fazer? Simples, separar a dependência em interfaces e inverter a dependência, abstraindo o que for possível e viável do código. Com uma interface, podemos simplesmente adicionar um método contrato para que cada classe que implemente essa interface especialize de acordo com sua necessidade, não necessitando assim alterar o código original caso surja uma necessidade de adicionar uma nova implementação para o método já existente.

## 3. L - Liskov Substituition Principle (Princípio da Substituição de Liskov)

## 4. I - Interface Segregation Principle  (Princípio da Segregação da Interface)

## 5. D - Dependency Inversion Principle (Princípio da Inversão de Dependência)