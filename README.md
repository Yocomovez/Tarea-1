# Tarea-1
Conociendo los Scaffold y widgets mas comunes

El objetivo del ejercicio siguiente es aprender a utilizar los widgets más comunes.

Hubieron diversos problemas al momento de realizar esta actividad aunque dichos inconvenientes fueron en su mayoría técnicos, el preparar el entorno de desarrollo de flutter llegó a ser bastante complicado y tardado debido a que mi computadora no lograba aguantar los programas con facilidad por lo que la elaboración de la actividad sufrió bastantes retrasos, además, el GelyMotion no funcionaba de la mejor manera por lo que se optó por usar Edge haciendo que cada prueba tardara aproximadamente 10 minutos en ejecutar, además no pude encontrar la ubicación de las diapositivas y tampoco los videos de la clase por lo que toda la actividad la resolví con lo que me acordaba y poco más que investigué.

En esta tarea aprendí un poco las bases de lo que vendría siendo la programación a celulares como por ejemplo el uso de los widgets los cuales básicamente son todas las cosas y herramientas que podemos usar, también aprendí a cambiar los colores dependiendo de como se ocupen y a posicionarlos de la mejor manera según me convenga.

![image](https://github.com/Yocomovez/Tarea-1/assets/157529375/c03386ad-2f2c-40ec-b7e5-e10197c6eb84)

![image](https://github.com/Yocomovez/Tarea-1/assets/157529375/e244d3f3-99f6-4b5d-90e5-26f6f798d104)

Código:
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Tarea 1',
      home: const MyHomePage(),
    );
  }
}

class MyHomePage extends StatefulWidget {
  const MyHomePage({Key? key}) : super(key: key);

  @override
  _MyHomePageState createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  bool isStarBlue = false;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Rigoberto Anaya'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text(
              "rigoberto.anayag@iteso.mx",
              textAlign: TextAlign.center,
            ),
            SizedBox(height: 20), // Espacio entre el texto y los íconos
            Row(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                IconButton(
                  onPressed: () {
                    setState(() {
                      isStarBlue = !isStarBlue;
                    });
                  },
                  icon: Icon(
                    Icons.phone,
                    color: isStarBlue ? Colors.blue : Colors.black,
                  ),
                ),
                SizedBox(
                    width:
                        20), // Espacio entre el ícono del celular y el ícono de reloj
                IconButton(
                  onPressed: () {
                    setState(() {
                      isStarBlue = !isStarBlue;
                    });
                  },
                  icon: Icon(
                    Icons.watch,
                    color: isStarBlue ? Colors.blue : Colors.black,
                  ),
                ),
                SizedBox(width: 20), // Espacio después del ícono de reloj
                IconButton(
                  onPressed: () {
                    // Cambiar el color del ícono entre negro y rojo
                    setState(() {
                      isStarBlue = !isStarBlue;
                    });
                  },
                  icon: Icon(
                    Icons.star,
                    color: isStarBlue ? Colors.blue : Colors.black,
                  ),
                ),
              ],
            ),
          ],
        ),
      ),
    );
  }
}
