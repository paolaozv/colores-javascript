# Máquina Inservible

![](http://2.1m.yt/4pDMirC.png)

* Con el botón "Click" se logrará que los bordes de los círculos se pinten primero el morado, luego el amarillo y finalmente el verde,
es por eso que se inicializa un evento y se declara un contador para que realice las acciones cada vez que hacemos click, el primer if
es para cuando haga el primer click añada el borde al primer círculo con la propiedad classList.add añado la clase border-purple.
Luego se realiza el segundo click y remueve la clase border-purple y añade el border-yellow y así para el tercer click y en ese momento
el contador vuelve a cero para que pueda realizar de nuevo las acciones arriba mencionadas.

``` javascript

window.addEventListener("load", function() {
	var boton = document.getElementById("cri");
	var contador = 1;
	boton.addEventListener("click", function() {
		if(contador == 1) {
			document.getElementById("color").value = "Morado";
			document.getElementById("purple").classList.add("border-purple");
			document.getElementById("green").classList.remove("border-green");
		}
		if(contador == 2) {
			document.getElementById("color").value = "Amarillo";
			document.getElementById("yellow").classList.add("border-yellow");
			document.getElementById("purple").classList.remove("border-purple");
		}
		if(contador == 3) {
			document.getElementById("color").value = "Verde";
			document.getElementById("green").classList.add("border-green");
			document.getElementById("yellow").classList.remove("border-yellow");
			contador = 0;
		}
		contador++;
	});
	
});

```

* Con el botón "Super Click" al ingresar los colores de los círculos, el borde de cada círculo se pintará del color del círculo, es por
ello que se usan tres if, uno para cada nombre del color.

``` javascript

window.addEventListener("load", function() {
	var boton = document.getElementById("superCri");
	boton.addEventListener("click", function() {
		var color = document.getElementById("color").value;
		if (color == "morado") {
			document.getElementById("purple").classList.add("border-purple");
			document.getElementById("yellow").classList.remove("border-yellow");
			document.getElementById("green").classList.remove("border-green");
		} else if (color == "amarillo") {
			document.getElementById("yellow").classList.add("border-yellow");
			document.getElementById("purple").classList.remove("border-purple");
			document.getElementById("green").classList.remove("border-green");
		} else if (color == "verde") {
			document.getElementById("green").classList.add("border-green");
			document.getElementById("yellow").classList.remove("border-yellow");
			document.getElementById("purple").classList.remove("border-purple");
		}
	});
});

```

