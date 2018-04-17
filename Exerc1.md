//1. Construir um algoritmo que leia 2 números e efetue a adição. Caso o valor
somado seja maior que 20, este deverá ser apresentando somando-se a ele
mais 8; caso o valor somado seja menor ou igual a 20, este deverá ser
apresentado subtraindo-se 5.//
<!DOCTYPE html>
<html>
	<head>
		<title>Exercicio PHP 01</title>
		<style>
			form { width: 200px; height: auto; margin: 0 auto; }
			label, input { width: 100%; height: auto; display: block; float:left; margin: 5px 0; }
		</style>
	</head>
	<body>
	<form action="#" method="post">
		<fieldset>
			<label>Digite o num1:</label>
            <input type="number" name="num1" value="" />
			<label>Digite o num2:</label>
            <input type="number" name="num2" value="" />
			<input type="submit" value="Enviar" />
        </fieldset>
    </form>
	<?php
	if (count($_POST)>0){
	$num1 = (isset($_POST['num1']) ? $_POST['num1'] : null);
	$num2 = (isset($_POST['num2']) ? $_POST['num2'] : null);
	$soma = $num1 + $num2;
	$result1 = $soma + 8;
	$result2 = $soma - 5;
		if ($soma > 20) {
			echo "<h1 align='center'>A soma de $num1 + $num2 é maior que 20, então ao resultado ($soma) deve-se somar 8 = $result1</h1>";
		}else{
			echo "<h1 align='center'>A soma de $num1 + $num2 é menor ou igual a 20, então do resultado ($soma) deve-se subtrair 5 = $result2</h1>";
		}
	}
	?>
	</body>
</html>
