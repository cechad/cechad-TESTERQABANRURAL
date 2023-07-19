//los errores encontrados

//dentro del script linea 44 let randomNumber = Math.random() * 10, el codigo genera un número aleatorio entre 0 y 10, 
//y el anunciado solicita que se genere de 1 y 100. Se resuelve utilizando la función Math.floor(Math.random() * 100) + 1.

//La variable esta inicializada en 5 intentos , se modifica en el ATTEMPS = 10 para que se tenga los 10 intentos.

//lowOrHi 
//en la declaración de la constante const lowOrHi = document.querySelector('lowOrHi'); no uso el selector de la clase falta el punto se corrigio de la siguiente forma.
  const lowOrHi = document.querySelector('.lowOrHi');

  //evento Click
  //En la función addEventListener debe estar en mayuscula, se corrije de la siguiente forma. 
  guessSubmit.addEventListener('click', checkGuess); 

  //En el mensaje de felicitaciones! y perdiste!
  //los colores y el orden se encuentran en desorden 
  // en la condición Felicitaciones! adivinaste el número 

  //Felicitaciones
  'Felicitaciones! adivinaste el número!';
      lastResult.style.backgroundColor = 'green';

//Perdiste
lastResult.textContent = '!!!Pérdistes!!!El número correcto era ' + randomNumber;
lastResult.style.backgroundColor = 'red';

//Incorrecto
lastResult.textContent = 'Incorrecto! ';
      lastResult.style.backgroundColor = 'black';

//Validación de ingreso de número entero.
//no esta validado unicamente que ingrese valores enteros, al ingresar un valor diferente puede causar una falla en el juego. 
la cual fue resuelta de la siguiente forma.
if (!Number.isInteger(userGuess)) {

          alert('Por favor, ingresa un número entero.');
          return;
        }

//Número aleatorio 
//En la linea 119 Cuando un jugador pierde desconoce cual era el número el cual debia adivinar , se corrijido de la siguiente forma 
//Antes
randomNumber = Math.floor(Math.random()) + 1;
//Corregido 
 randomNumber = Math.floor(Math.random() * 100) + 1;