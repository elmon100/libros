
==========
Ejercicios
==========

-------------------------------
 *Tema 6:* Control de calidad
-------------------------------

Análsis estático
~~~~~~~~~~~~~~~~

#. Corrige el programa `ugly.py <ugly.py.txt>`__ para que pase todas
   las pruebas de PyLint sin pasar parámetros especiales por la linea
   de comandos, aunque se permite deshabilitar alguna opción mediante
   directivas. Además, el código tiene algunos problemas con casos
   esquina y de calidad del algoritmo, arréglalo para que funcione
   bien siempre e indique al usuario los errores por consola.

   .. hint:: Mete el código en una función para que no se queje del
      uso de variables globales.

   .. hint:: Usa una directiva ``disable=W0402`` para evitar el
      *warning* por usar el módulo ``string``, que es apropiado usar.

   `Solución <good.py.txt>`__

#. Modifica el programa anterior para que pase los controles de
   PyChecker. También puedes usar alguna directiva dentro del código
   para deshabilitar cosas que no son erráticas.

   .. hint:: La directiva `no-stringiter` puede ser de utilidad.

   `Solución <good.py.txt>`__

Pruebas de unidad
~~~~~~~~~~~~~~~~~

#. Escribe algunas pruebas de unidad con ``doctest`` para la clase
   ``Racional`` que programamos en el tema de orientación a
   objetos. Recuerda que en la vida real, usaríamos la clase
   `Fractional <http://docs.python.org/library/fractions.html>`__.

   .. hint:: Programar ``__repr__`` será necesario para poder evaluar
      el estado del objeto de forma sencilla. No hace falta que el
      objeto sea sintácticamente Python, como tampoco lo es la
      representación por defecto.

   .. hint:: Llama a los tests en ``if __name__ == "__main__"``.

   `Solución <racional.py.txt>`__

#. Escribe algunas pruebas de unidad con ``unittest`` para las clase
   ``Racional`` anterior.

   .. hint:: Si el fichero de la clase ``Racional`` se llama
      ``racional.py``, llama al nuevo fichero ``test_racional.py`` y
      crea otro fichero ``runtests.py`` que ejecute este test y el de
      los siguientes ejercicios.

   .. hint:: Importar las clases de pruebas en ``runtests.py`` e
      invocar ``unittest.main ()`` debe ser suficiente.

   .. hint:: Para probar con ``assertRaises`` que acceder a ``entero``
      tira una excepción en los casos que debe, envuelve el acceso al
      atributo en una ``lambda``. Esto es así porque esa aserción
      espera que le pases una función para ella ejecutarla
      controladamente y realizar la comprobación.

   `Solución <test_racional.py.txt>`__

#. Escribe algunas pruebas de unidad con ``unittest`` para alguna de
   las clases del ejercicio del tema de orientación a
   objetos. Usa un *mockup* del fichero para probar la entrada
   y salida. Un *mockup* es una clase que da una implementación
   ficticia de otro objeto lo suficientemente completa para probar el
   objeto que nos interesa. La clase `StringIO
   <http://docs.python.org/library/stringio.html>`__ es un ``mockup``
   sobradamente completo para este propósito.

   .. hint:: Crea el *mockup* en el *fixture* del objeto.
   
   `Solución <test_personas.py.txt>`__

#. Juega con las pruebas de unidad anteriores desde la consola
   utilizando el método ``TestCase.debug ()``.
