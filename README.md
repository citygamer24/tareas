# tareas
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>actividad 1</title>
    <link rel="stylesheet" href="">
</head>

<body style="color: rgb(26, 26, 119); font-size: 36px";>
     <h2 style="color: rgb(0, 0, 0); font-size: 36px";>E:1 omar alejandro Ramirez Arias</h2>   
     1<br>
     2<br>
     fizz<br>
     4<br>
     buzz<br>
     fizz<br>
     7<br>
     8<br>
     fizz<br>
     buzz<br>
     11<br>
     fizz<br>
     13<br>
     14<br>
     fizzbuzz<br>
     16<br>
     17<br>
     fizz<br>
     19<br>
     buzz<br>
     fizz<br>
     22<br>
     23<br>
     fizz<br>
     buzz<br>
     26<br>
     fizz<br>
     28<br>
     29<br>
     fizz buzz<br>
     31<br>
     32<br>
     fizz<br>
     34<br>
     buzz<br>
     fizz<br>
     37<br>
     38<br>
     fizz<br>
     buzz<br>
     41<br>
     fizz<br>
     43<br>
     44<br>
     fizz buzz<br>
     46<br>
     47<br>
     fizz<br>
     49<br>
     buzz<br>
     fizz<br>
     52<br>
     53<br>
     fizz<br>
     buzz<br>
     56<br>
     fizz<br>
     58<br>
     59<br>
     fizz buzz<br>
     61<br>
     62<br>
     fizz<br>
     64<br>
     buzz<br>
     fizz<br>
     67<br>
     68<br>
     fizz<br>
     buzz<br>
     71<br>
     fizz<br>
     73<br>
     74<br>
     fizz buzz<br>
     76<br>
     77<br>
     fizz<br>
     79<br>
     buzz<br>
     fizz<br>
     82<br>
     83<br>
     fizz<br>
     buzz<br>
     86<br>
     fizz<br>
     88<br>
     89<br>
     fizz buzz<br>
     91<br>
     92<br>
     fizz<br>
     94<br>
     buzz<br>
     fizz<br>
     97<br>
     98<br>
     fizz<br>
     buzz<br>
     <br>
     <br>
     <br>
     <br>
     <br>
     <br>


     <h1>E:2 Tabla de Multiplicar</h1>
  <label for="numero">Ingresa un número:</label>
  <input type="number" id="numero" value="1">
  <button onclick="mostrarTabla()">Mostrar Tabla</button>
  <div id="tabla"></div>
  <script>
    function mostrarTabla() {
      let numero = document.getElementById("numero").value;
      numero = parseInt(numero);
      if (!isNaN(numero)) {
        let tabla = document.getElementById("tabla");
        tabla.innerHTML = ""; // Limpiar tabla previa
        for (let i = 1; i <= 10; i++) {
          let fila = document.createElement("p");
          fila.textContent = numero + " x " + i + " = " + (numero * i);
          tabla.appendChild(fila);
        }
      } else {
        alert("Por favor, ingresa un número válido.");
      }
    }
    </script>
    <br><br><br><br><br>
     <h1>E:3 Calculo de Circulo</h1>
    <label for="radius">Introduce el radio del circulo:</label>
    <input type="number" id="radius" min="0" required>
    <button onclick="calcular()">Calcular</button>
    <div id="result"></div>
    <script>
        function calcular() {
            const radio = parseFloat(document.getElementById('radius').value);
            const resultDiv = document.getElementById('result');
            resultDiv.innerHTML = ''; // Limpiar resultados anteriores
            if (radio < 0) {
                resultDiv.innerHTML = '<p class="error">Por favor, introduce un radio positivo.</p>';
                return;
            }
            const perimetro = 2 * Math.PI * radio; // Perimetro
            const area = Math.PI * Math.pow(radio, 2); // area
            resultDiv.innerHTML = `
                <p>Perimetro: ${perimetro.toFixed(2)}</p>
                <p>Area: ${area.toFixed(2)}</p>
            `;
        }
    </script>
    <br><br><br><br><br><br>

<h1>E:4 Calculo de factorial</h1>
<label for="factorial">introduce el numero:</label>
<input type="alert" id="factorial" min="0" required>
<button onclick="calcular()">Calcular</button>

<div id="result"></div>
    <h1>E:4 Calculo de factorial</h1>
<label for="factorial">introduce el numero:</label>
<input type="number" id="factorial" min="0" required>
<button onclick="calcular()">Calcular</button>
<div id="result"></div>
<script>
    function calcular() {
        const factorialInput = parseFloat(document.getElementById('factorial').value);
        const resultDiv = document.getElementById('result');
        resultDiv.innerHTML = ''; 
        // Calcular el factorial
        let factorial = 1;
        for (let i = 1; i <= factorialInput; i++) {
            factorial *= i;
        }
        resultDiv.innerHTML = `
            <p>factorial: ${factorial}</p>
        `;
    }
</script>
<br><br><br><br><br>

<h1>E:5 Calculadora de IVA (16%)</h1>
  <label for="costo">Ingresa el costo del artículo:</label>
  <input type="number" id="costo" value="0">
  <button onclick="calcularIVA()">Calcular IVA</button>
  <p id="resultado"></p>
  <script>
    function calcularIVA() {
      let costo = parseFloat(document.getElementById("costo").value);
      let iva = costo * 0.16;
      document.getElementById("resultado").textContent = "El IVA del artículo es: " + iva;
    }
  </script>
  <br><br><br><br><br><br>


<h1>E:6 Determinar si un número es par o impar</h1>
<p>Ingrese un número:</p>
<input type="number" id="numeroInput">
<button onclick="checkParImpar()">Verificar</button>
<p id="resultado"></p>

<script>
function checkParImpar() {
    var numero = parseInt(document.getElementById("numeroInput").value);

    if (numero === 0) {
        document.getElementById("resultado").textContent = "Número no válido, por favor ingrese un número diferente de cero.";
    } else if (numero % 2 === 0) {
        document.getElementById("resultado").textContent = "El número ingresado es par.";
    } else {
        document.getElementById("resultado").textContent = "El número ingresado es impar.";
    }
}
</script>
<br><br><br><br><br><br>
<h1>E:7 Contador Regresivo</h1>
<label for="numero">Ingresa un número entero positivo:</label>
<input type="number" id="numero" value="0">
<button onclick="contarRegresivo()">Contar</button>
<p id="resultado"></p>
<script>
  function contarRegresivo() {
    let numero = parseInt(document.getElementById("numero").value);
    let resultado = document.getElementById("resultado");
    if (numero > 0) {
      let cadena = "";
      for (let i = numero; i > 0; i--) {
        cadena += i + ", ";
      }
      cadena += "0";
      resultado.textContent = cadena;
    } else {
      resultado.textContent = "El número debe ser positivo.";
    }
  }
</script>
<br><br><br><br><br>
<h1 style="">E:8 Calculadora de Hipotenusa</h1>
  <label for="catetoA">Longitud del cateto A:</label>
  <input type="number" id="catetoA" value="0">
  <br>
  <label for="catetoB">Longitud del cateto B:</label>
  <input type="number" id="catetoB" value="0">
  <br>
  <button onclick="calcularHipotenusa()">Calcular Hipotenusa</button>
  <p id="resultado"></p>
  <script>
    function calcularHipotenusa() {
      let catetoA = parseFloat(document.getElementById("catetoA").value);
      let catetoB = parseFloat(document.getElementById("catetoB").value);
      let hipotenusa = Math.sqrt(Math.pow(catetoA, 2) + Math.pow(catetoB, 2));
      document.getElementById("resultado").textContent =
        "La longitud de la hipotenusa es: " + hipotenusa;
    }
  </script>
<h1>E:9 Números Impares</h1>
  <label for="numero">Ingresa un número entero positivo:</label>
  <input type="number" id="numero" value="0">
  <button onclick="mostrarImpares()">Mostrar Impares</button>
  <p id="resultado"></p>
  <script>
    function mostrarImpares() {
      let numero = parseInt(document.getElementById("numero").value);
      let resultado = document.getElementById("resultado");
      if (numero > 0) {
        let cadena = "";
        for (let i = 1; i <= numero; i += 2) {
          cadena += i + ", ";
        }
        cadena = cadena.slice(0, -2); // Elimina la última coma y espacio
        resultado.textContent = cadena;
      } else {
        resultado.textContent = "El número debe ser positivo.";
      }
    }
  </script>
  <h1>E:10 Calculadora de Salarios</h1>
  <form id="wageForm">
    <label for="hoursWorked">Horas Trabajadas:</label>
    <input type="number" id="hoursWorked" name="hoursWorked" required><br><br>
    <label for="hourlyRate">Tasa por Hora:</label>
    <input type="number" id="hourlyRate" name="hourlyRate" required><br><br>
    <button type="button" onclick="calcularSalarios()">Calcular Salarios</button>
  </form>
  <p id="result">Tus salarios totales son: <span id="totalWages"></span></p>
  <script>
    function calcularSalarios() {
      let horasTrabajadas = document.getElementById("hoursWorked").value;
      let tasaPorHora = document.getElementById("hourlyRate").value;
      //  Simulación de cálculo (no es real)
      let totalWages = horasTrabajadas * tasaPorHora;
      document.getElementById("totalWages").innerHTML = "$" + totalWages;
    }
  </script>

     
     
    
    

</body>
</html>
