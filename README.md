# S.O.L.I.D

### Considerações

Esta aula tem como objetivo ensinar o conteúdo referente aos princípios do <strong>SOLID</strong>, especificamente os princípios: ***Single Responsibility*** e ***Interface Segregation***. Além das referências mencionadas ao final, esta aula também utilizou como referência a formatação e conteúdo contidos no Curso de Desenvolvimento Web da [Trybe](https://www.betrybe.com/).

<details>
<summary><h3>O que vamos aprender?</h3></summary>

<p align="justify">
É fundamental que nos preocupemos com a qualidade do nosso código, desenvolvendo-o, para que se torne mais limpo, conciso, performático e desacoplado (com menos dependência entre componentes). Com este objetivo, estudaremos, na aula de hoje, dois dos princípios do <strong>SOLID</strong>, as letras S e I!

Os princípios do <strong>SOLID</strong>, são um conjunto de boas práticas, que tem, como objetivo, tornar mais fácil a legibilidade, testabilidade, manutenção, extensão e organização do código.

Já está animado(a)? Vamos com tudo para o conteúdo do dia, que nos deixará um passo mais perto de nos tornar profissionais de excelência! :rocket:
</p>

### Você será capaz de:

<p align="justify">

- Escrever funções e classes que tenham apenas uma única responsabilidade.

- Escrever classes que não forcem a utilização de métodos que não serão utilizados, através da criação de interfaces específicas, ao invés de uma que englobe todos os propósitos.
</p>

</details>

<details>
<summary><h3>Por que isso é importante?</h3></summary>

<p align="justify">
Na programação, <strong>nem sempre o mais difícil é resolver o problema</strong>. Analisar um código já existente e fazer sua <strong>manutenção</strong> ou <strong>refatoração comumente é mais desafiador</strong>.

Surge então a necessidade de se escrever códigos com qualidade. Alguns aspectos que trazem qualidade ao nosso código são:

- Clareza / legibilidade.
- Simplicidade.
- Cobertura de testes.
- Performance.
</p>

<p align="justify">
Os princípios do <strong>SOLID</strong> nos norteiam para que escrevamos códigos mais limpos, diminuindo acoplamento (medida de interdependência entre os componentes), facilitando a refatoração, elaboração de testes e estimulando o reaproveitamento de código.
</p>

> Cada um dos princípios representa uma técnica de design de código criada para evitar problemas já conhecidos.

<p align="justify">
<strong>SOLID</strong> é amplamente utilizado pelo mercado de trabalho, visto que as aplicações se tornam mais simples de se compreender e manter ao longo do tempo. Apesar <strong>destes princípios serem específicos para Programação Orientada a Objetos, ainda se pode aplicar alguns deles a códigos que seguem outros paradigmas</strong>.
</p>

<p align="justify">
Como profissionais de desenvolvimento de softwares, <strong>devemos almejar sempre a excelência do nosso código</strong>, pois impacta diretamente no andamento do projeto no longo prazo. Podemos lembrar da máxima de que: <strong>um bom código escrito agora, vai facilitar, ou evitar, a refatoração de amanhã</strong>.
</p>

<p align="justify">
Escrever códigos simples, legíveis e limpos requer prática e demanda mais tempo no início, mas não seguir as boas práticas e princípios pode ocasionar problemas no longo prazo, que também vão demandar tempo e pode impossibilitar refatorar algum trecho sem fazer outra coisa parar de funcionar. Por isso devemos sempre buscar aprimorar a qualidade do nosso código, para evitar dores de cabeça no futuro. :relieved:
</p>

</details>

<details>
<summary><h3>Conteúdos</h3></summary><blockquote>

<details>
<summary><h3>Princípios S.O.L.I.D</h3></summary><blockquote>

<p align="justify">
No contexto de programação orientada a objetos, o acrônimo <strong>SOLID</strong>, refere-se a cinco princípios que visam facilitar o desenvolvimento, compreensão e manutenção de códigos. A adoção destas práticas ao programar, leva a diminuição de bugs no software, evita futuras refatorações e contribui para um desenvolvimento ágil e adaptativo. Isto gera impactos fundamentais na nossa produtividade e eficiência como desenvolvedores.

Cada letra de <strong>SOLID</strong> representa a inicial de um princípio, conforme tabela abaixo:

</p>

| Letras |                    Princípio                    |                                                                                   Descrição                                                                                   |
| :----: | :---------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|   S    | Single Responsibility (Responsabilidade Única)  |                                            Uma entidade (classe, método, função, etc) deve ter apenas uma única responsabilidade.                                             |
|   O    |          Open-Closed (Aberto-Fechado)           |                                             Entidades de software devem ser abertas para extensão, mas fechadas para modificação.                                             |
|   L    |  Liskov Substitution (Substituição de Liskov)   |                           Objetos em um programa devem ser substituíveis por instâncias de seus subtipos, sem alterar a funcionalidade do programa.                           |
|   I    | Interface Segregation (Segregação de Interface) |                                               Ter muitas interfaces específicas é melhor do que ter uma para todos propósitos.                                                |
|   D    | Dependency Inversion (Inversão de dependência)  | Entidades devem depender de abstrações, não de objetos concretos. Então as entidades de alto nível não devem depender das de baixo nível, ambas devem depender de abstrações. |

<p align="justify">
⚠️ <strong>Aviso</strong>: É importante lembrar que ao falar de <strong>SOLID</strong>, estamos tratando de <strong>princípios</strong>. Desta forma, devemos utilizar estes conceitos para nortear a escrita do nosso código e <strong>não entender que estas regras são obrigatórias em todos os projetos</strong>. Fica a nosso critério, ou da equipe, aplicar ou flexibilizar os princípios que fazem sentido e ajudam efetivamente no desenvolvimento do projeto. Temos que ter o cuidado para não seguir muito à risca e isto atrapalhar o desenvolvimento, o que iria na contramão do objetivo do <strong>SOLID</strong>, que é facilitar nossa vida ao escrever e fazer a manutenção do código. Importante sempre refletir o porquê de estarmos usando ou fazendo algo. Sintetizando:
</p>

> Ao escrever um código, o objetivo é torná-lo fácil de ser entendido e mantido. Portanto, princípio nenhum deve piorar a legibilidade ou a manutenibilidade do seu código.

<p align="justify">
Escrever um bom código não é intuitivo, requer muita prática e estudo. Assim, princípios como os do <strong>SOLID</strong> e as regras do <strong>ESLint</strong> (que já estamos usando desde o bloco de fundamentos), são algumas das ferramentas que nos auxiliam nesta tarefa de melhorar a qualidade do nosso código.
</p>

<p align="justify">
Caso não tenha entendido a descrição de algum princípio, não se preocupe, vamos nos aprofundar em cada um deles, iniciando hoje pelas letras <strong>S</strong> e <strong>I</strong>!
</p>

</details>

<details>
<summary><h3>Single Responsibility Principle</h3></summary><blockquote>

<p align="justify">
Este princípio nos instrui no sentido de que uma classe deve ter apenas uma razão para mudar, deve fazer apenas uma função, ter apenas uma responsabilidade. Além de classes, também podemos extender esta orientação para métodos, funções, módulos, arquivos, dentro outros. Mas o que queremos dizer por apenas uma responsabilidade?

</p>

<p align="justify">
Trazendo para a prática: imagine que você está responsável por estruturar o código que representa um sistema de delivery. Poderiamos estruturar o código desta maneira:

</p>

```
// order.ts

class Order {
  // Aqui armazenaremos nome do cliente e seu endereço, além do nome e preço do produto pedido.
  public _name: string;
  public _price: number;
  public _costumer: string;
  public _address: string;

  constructor(name: string, price: number, costumer: string, address: string) {
    this._name = name;
    this._price = price;
    this._costumer = costumer;
    this._address = address;
  }

  deliver(): void {
    console.log(`${ this._costumer }, seu pedido de ${ this._name }, no total de R$: ${ this._price }, já está a caminho para o endereço: ${ this._address }!`)
  }
}

// Criamos o pedido.
const orderA = new Order('Pizza', 10, 'Maria', 'Rua Abbey Road');

// Iniciamos a entrega.
orderA.deliver();
```

<p align="justify">
Agora, vamos fazer este código se adequar ao princípio da Responsabilidade Única. Para isso, devemos pensar o seguinte: será que meus componentes estão fazendo apenas uma função? No caso da classe Order, ela está fazendo mais de uma função: <strong>registra informações do cliente</strong>, <strong>registra informações do pedido</strong> e tem um método que <strong>realiza a entrega</strong>. Podemos então perceber três responsabilidades distintas. Vamos separar estas funções da seguinte maneira:

</p>

```
// costumer.ts

class Costumer {
  // Ao omitir o modificador de acesso, por padrão o atributo da classe no TypeScript será public.
  _name: string;
  _address: string;

  constructor(name: string, address: string) {
    this._name = name;
    this._address = address;
  }
}

export default Costumer;
```

```
// product.ts

class Product {
  _name: string;
  _price: number;

  constructor(name: string, price: number) {
    this._name = name;
    this._price = price;
  }
}

export default Product;
```

```
// interfaces.ts

import Costumer from "./costumer";
import Product from "./product";

interface IDelivery {
  deliver(costumer: Costumer, product: Product): void;
}

export default IDelivery;
```

```
// delivery.ts

import IDelivery from "./interfaces";
import Costumer from "./costumer";
import Product from "./product";

class Delivery implements IDelivery {

  deliver(costumer: Costumer, product: Product): void {
    console.log(`${ costumer._name }, seu pedido de ${ product._name }, no total de R$: ${ product._price }, já está a caminho para o endereço: ${ costumer._address }.`);
  }
}

const myDelivery = new Delivery();
const costumerMaria = new Costumer('Maria', 'Rua Abbey Road');
const pizza = new Product('Pizza', 10);

myDelivery.deliver(costumerMaria, pizza);
```

<p align="justify">
Dividimos então a antiga "God Class" Order, que fazia todas as funções em um únio arquivo, em três classes distintas, mais específicas, que desempenham responsabilidades únicas, em arquivos diferentes. Isto permite o reaproveitamento do código, podendo criar múltiplos clientes, produtos e até múltiplos sistemas de delivery, além de facilitar a testabilidade deste código. Também criamos uma interface IDelivery que vai conter o "contrato" que foi implementado na classe Delivery.

</p>

<p align="justify">
⚠️ <strong>Aviso</strong>: A tarefa de identificar e delimitar as responsabilidades de funções, classes, arquivos e etc, sempre é dotada de certa subjetividade. A depender de como pensamos, seria possível ir quebrando nossas classes e funções em partes cada vez menores. Então lembre-se que <strong>o princípio da Responsabilidade Única é uma orientação, não se torne refém dele</strong>. O objetivo aqui é tornar o nosso código <strong>mais simples e legível</strong>. Temos que aplicar as orientações com razoabilidade, sempre para facilitar a nossa interação com o código.

</p>

</blockquote></details>

<details>
<summary><h3>Interface Segregation Principle</h3></summary>

<p align="justify">
Com este princípio, dividimos interfaces maiores em interfaces menores e mais específicas, para que as classes que as implementem só precisem criar os métodos que lhe sejam pertinentes.

</p>

> Nenhum cliente deve ser forçado a depender de métodos que não utiliza.

<p align="justify">
Vamos imaginar o seguinte cenário. Queremos criar classes de diferentes relógios, que possuirão funcionalidades (métodos) diferentes a depender de qual seja o relógio. Para isso, faremos o seguinte:

</p>

```
// interfaces.ts

interface IWatch {
  time(): void;
  timer(): void;
  stopwatch(): void;
  gps(location: string): void;
  call(number: string): void;
  music(song: string): void;
}

export default IWatch;
```

```
// smartwatch.ts

import IWatch from "./interfaces";

class SmartWatch implements IWatch {
  time(): void {
    console.log('São 12:00 horas');
  }

  timer(): void {
    console.log('Timer iniciado');
  }

  stopwatch(): void {
    console.log('Cronômetro iniciado');
  }

  gps(location: string): void {
    console.log(`Rota para ${ location }`);
  }

  call(number: string): void {
    console.log(`Ligando para ${ number }`);
  }

  music(song: string): void {
    console.log(`Tocando ${ song }`);
  }

  checkHeartbeat(): void {
    console.log('Sua frequência cardíaca está em 80 bpm');
  }
}
```

<p align="justify">
Se quiséssemos criar uma classe MechanicalWatch (relógio mecânico), implementando a interface IWatch, teríamos o seguinte problema: o nosso relógio mecânico seria obrigado a implementar métodos de funcionalidades que não possui, como as funções de GPS, ligar, ouvir música e batimentos cardíacos.

</p>

<p align="justify">
Desta forma, o <strong>princípio da Segregação de Interface nos orienta para que criemos mais interfaces, menores e mais específicas</strong>. Para nosso código ficar em conformidade com o princípio, vamos fazer a seguinte refatoração:

</p>

```
// interfaces.ts

interface IWatch {
  time(): void;
  timer(): void;
  stopwatch(): void;
}

interface IGPS {
  gps(location: string): void;
}

interface ICall {
  call(number: string): void;
}

interface IMusic {
  music(song: string): void;
}

interface IHeartbeat {
  checkHeartbeat(): void;
}

export {
  IWatch,
  IGPS,
  ICall,
  IMusic,
  IHeartbeat,
};
```

```
// smartwatchsuperpro.ts

import { ICall, IGPS, IHeartbeat, IMusic, IWatch } from "./interfaces";

class SmartWatchSuperPro implements IWatch, IGPS, ICall, IMusic, IHeartbeat {
  time(): void {
    console.log('São 12:00 horas');
  }

  timer(): void {
    console.log('Timer iniciado');
  }

  stopwatch(): void {
    console.log('Cronômetro iniciado');
  }

  gps(location: string): void {
    console.log(`Rota para ${ location }`);
  }

  call(number: string): void {
    console.log(`Ligando para ${ number }`);
  }

  music(song: string): void {
    console.log(`Tocando ${ song }`);
  }

  checkHeartbeat(): void {
    console.log('Sua frequência cardíaca está em 80 bpm');
  }
}
```

```
// smartwatch.ts

import { IGPS, IMusic, IWatch } from "./interfaces";

class SmartWatch implements IWatch, IGPS, IMusic {
  time(): void {
    console.log('São 12:00 horas');
  }

  timer(): void {
    console.log('Timer iniciado');
  }

  stopwatch(): void {
    console.log('Cronômetro iniciado.');
  }

  gps(location: string): void {
    console.log(`Rota para ${ location }`);
  }

  music(song: string): void {
    console.log(`Tocando ${ song }`);
  }
}
```

```
// mechanicalwatch.ts

import { IWatch } from "./interfaces";

class MechanicalWatch implements IWatch {
  time(): void {
    console.log('São 12:00 horas');
  }

  timer(): void {
    console.log('Timer iniciado');
  }

  stopwatch(): void {
    console.log('Cronômetro iniciado');
  }
}
```

<p align="justify">
Perceba que agora a interface IWatch contém funcionalidades básicas que são comuns entre os tipos de relógio, assim, nossa classe MechanicalWatch precisa implementar apenas os métodos que são pertinentes a este tipo de relógio. Como criamos interfaces específicas para cada uma das funcionalidades, conseguimos também criar diferentes smartwatches que implementam apenas os métodos das funcionalidades que cada um possui.
</p>

</blockquote></details>
</blockquote></details>

<details>
<summary><h3>Agora a prática</h3></summary>

> Single Responsibility: o código a seguir será usado para os exercícios 1, 2 e 3.

```
// task.ts

class Task {
  _taskName: string;
  _taskContent: string;
  _taskStatus: string;

  constructor(taskName: string, taskContent: string, taskStatus: string) {
    this._taskName = taskName;
    this._taskContent = taskContent;
    this._taskStatus = taskStatus;
  }

  saveTask(): void {
    console.log('Tarefa salva com sucesso!');
  }
}
```

<p align="justify">
<strong>Exercício 1</strong>: Refatore a classe Task para que ela contenha e inicialize, <strong>apenas</strong>, os atributos de uma Task (nome, conteúdo e status).

</p>

<p align="justify">
<strong>Exercício 2</strong>: Crie uma interface ITaskList, com um método saveTask, que simula uma função de salvar tarefas em um banco de dados. O método saveTask deve receber como parâmetro uma task do tipo Task.

</p>

<p align="justify">
<strong>Exercício 3</strong>: Crie uma classe TaskList, que deverá implementar a interface ITaskList. Em seguida, crie um organizador de tarefas chamado myTaskList, usando a classe TaskList e use o método saveTask para salvar uma tarefa.

</p>

> Interface Segregation: o código a seguir será usado para os exercícios 4, 5, 6 e 7.

```
// interfaces.ts

interface IVehicle {
  fly(): void;
  drive(): void;
  pilot(): void;
}

export default IVehicle;
```

```
// boat.ts

import IVehicle from "./interfaces";

class Boat implements IVehicle {
  fly(): void {
    console.log('Não posso voar');
  }

  drive(): void {
    console.log('Não sou terrestre');
  }

  pilot(): void {
    console.log('Navegando pelo mar');
  }
}
```

<p align="justify">
<strong>Exercício 4</strong>: Refatore a interface IVehicle para que seja possível implementarmos um carro, um avião e um barco, cada uma com sua própria interface.

</p>

<p align="justify">
<strong>Exercício 5</strong>: Refatore a classe Boat para que ela precise implementar apenas o método para navegar o barco.

</p>

<p align="justify">
<strong>Exercício 6</strong>: Crie uma classe Plane que deverá implementar apenas o método de voar.

</p>

<p align="justify">
<strong>Exercício 7</strong>: Crie uma classe Car que deverá implementar apenas o método de dirigir.

</p>

</details>

<details>
<summary><h3>Gabarito</h3></summary>

<p align="justify">
<strong>Exercício 1</strong>: Refatore a classe Task para que ela contenha e inicialize, <strong>apenas</strong>, os atributos de uma Task (nome, conteúdo e status).

<p align="justify">

```
// task.ts

class Task {
  _taskName: string;
  _taskContent: string;
  _taskStatus: string;

  constructor(taskName: string, taskContent: string, taskStatus: string) {
    this._taskName = taskName;
    this._taskContent = taskContent;
    this._taskStatus = taskStatus;
  }
}

export default Task;
```

<p align="justify">
<strong>Exercício 2</strong>: Crie uma interface ITaskList, com um método saveTask, que simula uma função de salvar tarefas em um banco de dados. O método saveTask deve receber como parâmetro uma task do tipo Task.

<p align="justify">

```
// interfaces.ts

import Task from "./test";

interface ITaskList {
  saveTask(task: Task): void;
}

export default ITaskList;
```

<p align="justify">
<strong>Exercício 3</strong>: Crie uma classe TaskList, que deverá implementar a interface ITaskList. Em seguida, crie um organizador de tarefas chamado myTaskList, usando a classe TaskList e use o método saveTask para salvar uma tarefa.

<p align="justify">

```
// taskList.ts

import ITaskList from "./interfaces";
import Task from "./task";

class TaskList implements ITaskList {
  saveTask(task: Task): void {
    console.log(`A tarefa ${ task._taskName }`)
  }
}

const myTaskList = new TaskList();

const task = new Task('Projeto A', 'Refatorar o projeto para utilizar os princípios S.O.L.I.D', 'Em andamento');

myTaskList.saveTask(task);
```

<p align="justify">
<strong>Exercício 4</strong>: Refatore a interface IVehicle para que seja possível implementarmos um carro, um avião e um barco, cada uma com sua própria interface.

<p align="justify">

```
// interfaces.ts

interface IPlane {
  fly(): void;
}

interface ICar {
  drive(): void;
}

interface IBoat {
  pilot(): void;
}

export {
  IPlane,
  ICar,
  IBoat,
};
```

<p align="justify">
<strong>Exercício 5</strong>: Refatore a classe Boat para que ela precise implementar apenas o método para navegar o barco.

<p align="justify">

```
// boat.ts

import { IBoat } from "./interfaces";

class Boat implements IBoat {
  pilot(): void {
    console.log('Navegando pelo mar');
  }
}
```

<p align="justify">
<strong>Exercício 6</strong>: Crie uma classe Plane que deverá implementar apenas o método de voar.

<p align="justify">

```
// plane.ts

import { IPlane } from "./interfaces";

class Plane implements IPlane {
  fly(): void {
    console.log('Voando alto!');
  }
}
```

<p align="justify">
<strong>Exercício 7</strong>: Crie uma classe Car que deverá implementar apenas o método de dirigir.

</p>

```
// car.ts

import { ICar } from "./interfaces";

class Car implements ICar {
  drive(): void {
  console.log('Dirigindo pela cidade');
  }
}

```

</details>

<details>
<summary><h3>Recursos adicionais e referências</h3></summary>

- [O que é SOLID: O guia completo para você entender os 5 princípios da POO](https://medium.com/desenvolvendo-com-paixao/o-que-%C3%A9-solid-o-guia-completo-para-voc%C3%AA-entender-os-5-princ%C3%ADpios-da-poo-2b937b3fc530)
- [Princípios SOLID com TypeScript](https://medium.com/@matheusbessa_44838/princ%C3%ADpios-solid-com-typescript-4f8a9d5d1ef8)
- [SOLID fica FÁCIL com estas ilustrações - Filipe Deschamps](https://www.youtube.com/watch?v=6SfrO3D4dHM)
- [SOLID: The First 5 Principles of Object Oriented Design](https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)
- [Arquitetura - O Princípio da responsabilidade única](https://www.devmedia.com.br/arquitetura-o-principio-da-responsabilidade-unica/18700)
- [SOLID Design Principles Explained: The Single Responsibility Principle](https://stackify.com/solid-design-principles/)
- [Os Princípios do SOLID — ISP Princípio de segregação da interface](https://medium.com/xp-inc/os-princ%C3%ADpios-do-solid-isp-princ%C3%ADpio-de-segrega%C3%A7%C3%A3o-da-interface-1822ebc802fd)

</details>
