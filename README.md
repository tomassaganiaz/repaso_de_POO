🧩 Cuadro 1: Conceptos Clave de OOP

<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; font-family: Arial, sans-serif; width: 100%;">
  <thead style="background-color: #f2f2f2;">
    <tr><th colspan="2">📘 Conceptos Clave en Programación Orientada a Objetos (OOP)</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>Clase</strong></td><td>Plantilla que define atributos y métodos. <code>class Persona</code></td></tr>
    <tr><td><strong>Objeto</strong></td><td>Instancia concreta de una clase. <code>juan = Persona()</code></td></tr>
    <tr><td><strong>Atributo</strong></td><td>Variable que pertenece a una clase u objeto. <code>self.nombre</code>, <code>self.edad</code></td></tr>
    <tr><td><strong>Función</strong></td><td>Bloque de código que realiza una tarea específica. Puede estar fuera de una clase.</td></tr>
    <tr><td><strong>Método</strong></td><td>Función definida dentro de una clase. <code>def saludar(self):</code></td></tr>
    <tr><td><strong>Encapsulamiento</strong></td><td>Oculta detalles internos usando atributos privados y métodos de acceso. <code>_nombre</code>, <code>__edad</code></td></tr>
    <tr><td><strong>Getter / Setter</strong></td><td><ul><li><strong>Getter:</strong> Devuelve el valor de un atributo.</li><li><strong>Setter:</strong> Modifica el valor de un atributo.</li></ul></td></tr>
    <tr><td><strong>Decoradores</strong></td><td>Funciones que modifican el comportamiento de otras funciones o métodos. <code>@staticmethod</code>, <code>@property</code></td></tr>
    <tr><td><strong>Métodos especiales (dunder)</strong></td><td>Métodos con doble guión bajo que personalizan el comportamiento de objetos. <code>__init__</code>, <code>__str__</code></td></tr>
    <tr><td><strong>Variable</strong></td><td>Espacio de memoria para guardar datos. <code>edad = 25</code>, <code>nombre = "Tomás"</code></td></tr>
    <tr><td><strong>Variable tipada</strong></td><td>Variable con tipo de dato definido. <code>int edad = 25;</code>, <code>string nombre = "Tomás";</code></td></tr>
    <tr><td><strong>¿Qué es la OOP?</strong></td><td>Paradigma que organiza el software en objetos que combinan datos y comportamientos.</td></tr>
    <tr><td><strong>Objetivo</strong></td><td>Facilitar la reutilización, escalabilidad y mantenimiento del código.</td></tr>
    <tr><td><strong>Principales pilares</strong></td><td><ul><li>Encapsulamiento</li><li>Herencia</li><li>Polimorfismo</li><li>Abstracción</li></ul></td></tr>
    <tr><td><strong>Ejemplo simple</strong></td><td><pre>
class Persona {
  constructor(nombre) {
    this.nombre = nombre;
  }
  saludar() {
    console.log(`Hola, soy ${this.nombre}`);
  }
}
    </pre></td></tr>
    <tr><td><strong>Ventajas</strong></td><td><ul><li>Mayor modularidad</li><li>Facilidad de mantenimiento</li><li>Reutilización de componentes</li></ul></td></tr>
  </tbody>
</table>
