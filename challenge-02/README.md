// Crie uma função que receba dois argumentos e retorne a soma dos mesmos.
  function soma(x,y){
    return x + y;
  }

// Declare uma variável que receba a invocação da função criada acima, passando dois números quaisquer por argumento, e somando `5` ao resultado retornado da função.
  let nova_soma = soma(10,12);
  nova_soma += 5;

// Qual o valor atualizado dessa variável?
  27

// Declare uma nova variável, sem valor.
  let test ;

/*
Crie uma função que adicione um valor à variável criada acima, e retorne a string:
    O valor da variável agora é VALOR.
Onde VALOR é o novo valor da variável.
*/
  function atualiza(valor){
    test = valor;
    return `O valor da variável agora é ${test}`;
  }

// Invoque a função criada acima.
  atualiza(15);

// Qual o retorno da função? (Use comentários de bloco).
  /*
    O valor da variável agora é 15
  */

/*
Crie uma função com as seguintes características:
1. A função deve receber 3 argumentos;
2. Se qualquer um dos três argumentos não estiverem preenchidos, a função deve retornar a string:
    Preencha todos os valores corretamente!
3. O retorno da função deve ser a multiplicação dos 3 argumentos, somando `2` ao resultado da multiplicação.
*/
  function calculo(x,y,z){
    let calc ;

    if(arguments.length === 3){
      calc = x*y*z;
      return calc + '2'
    }else{
      return 'Preencha todos os valores corretamente!';
    }
  }

// Invoque a função criada acima, passando só dois números como argumento.
  calculo(2,3);

// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).
  // 'Preencha todos os valores corretamente!'

// Agora invoque novamente a função criada acima, mas passando todos os três argumentos necessários.
  calculo(2,3,5);

// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).
  // '302'

/*
Crie uma função com as seguintes características:
1. A função deve receber 3 argumentos.
2. Se somente um argumento for passado, retorne o valor do argumento.
3. Se dois argumentos forem passados, retorne a soma dos dois argumentos.
4. Se todos os argumentos forem passados, retorne a soma do primeiro com o segundo, e o resultado, dividido pelo terceiro.
5. Se nenhum argumento for passado, retorne o valor booleano `false`.
6. E ainda, se nenhuma das condições acima forem atendidas, retorne `null`.
*/
  function calculo2(x,y,z){
    let args = arguments.length;
    
    if(args === 3){ 
      return (x + y) / z; 

    } else if (args === 2){
      return x + y;

    } else if (args === 1){
      return x;

    } else if(args === 0){
      return false;

    }else{
      return null;
    }
  }

// Invoque a função acima utilizando todas as possibilidades (com nenhum argumento, com um, com dois e com três.) Coloque um comentário de linha ao lado da função com o resultado de cada invocação.

  calculo2()        // 'false';
  calculo2(1,2,3,4) // 'null'
  calculo2(1,2,3)   // 1
  calculo2(1,2)     // 3
  calculo2(5)       // 5
