<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; font-family: Arial, sans-serif; width: 100%;">
  <thead style="background-color: #f2f2f2;">
    <tr>
      <th colspan="2">📘 Repaso de conceptos clave en Programación Orientada a Objetos (OOP)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Clase</strong></td>
      <td>Plantilla que define atributos (datos) y métodos (comportamientos).<br><em>Ej:</em> <code>class Persona</code></td>
    </tr>
    <tr>
      <td><strong>Objeto</strong></td>
      <td>Instancia concreta de una clase.<br><em>Ej:</em> <code>juan = Persona()</code></td>
    </tr>
    <tr>
      <td><strong>Atributo</strong></td>
      <td>Variable que pertenece a una clase u objeto.<br><em>Ej:</em> <code>self.nombre</code>, <code>self.edad</code></td>
    </tr>
    <tr>
      <td><strong>Función</strong></td>
      <td>Bloque de código que realiza una tarea específica. Puede estar fuera de una clase.</td>
    </tr>
    <tr>
      <td><strong>Método</strong></td>
      <td>Función definida dentro de una clase. <br><em>Ej:</em> <code>def saludar(self):</code></td>
    </tr>
    <tr>
      <td><strong>Encapsulamiento</strong></td>
      <td>Oculta detalles internos usando atributos privados y métodos de acceso.<br><em>Ej:</em> <code>_nombre</code>, <code>__edad</code></td>
    </tr>
    <tr>
      <td><strong>Getter / Setter</strong></td>
      <td>
        <ul>
          <li><strong>Getter:</strong> Devuelve el valor de un atributo.</li>
          <li><strong>Setter:</strong> Modifica el valor de un atributo.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>Decoradores</strong></td>
      <td>Funciones que modifican el comportamiento de otras funciones o métodos.<br><em>Ej:</em> <code>@staticmethod</code>, <code>@property</code></td>
    </tr>
    <tr>
      <td><strong>Métodos especiales (dunder)</strong></td>
      <td>Métodos con doble guión bajo que personalizan el comportamiento de objetos.<br><em>Ej:</em> <code>__init__</code>, <code>__str__</code></td>
    </tr>
    <tr>
      <td><strong>Variable</strong></td>
      <td>Espacio de memoria para guardar datos.<br><em>Ej:</em> <code>edad = 25</code>, <code>nombre = "Tomás"</code></td>
    </tr>
    <tr>
      <td><strong>Variable tipada</strong></td>
      <td>Variable con tipo de dato definido.<br><em>Ej:</em> <code>int edad = 25;</code>, <code>string nombre = "Tomás";</code></td>
    </tr>
  </tbody>
</table>


<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; font-family: Arial, sans-serif;">
  <thead style="background-color: #f2f2f2;">
    <tr>
      <th colspan="2">¿Qué es la Programación Orientada a Objetos (OOP)?</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Definición</strong></td>
      <td>OOP es un paradigma de programación que organiza el software en <em>objetos</em>, que combinan datos (atributos) y comportamientos (métodos).</td>
    </tr>
    <tr>
      <td><strong>Objetivo</strong></td>
      <td>Facilitar la reutilización, escalabilidad y mantenimiento del código mediante la abstracción y modelado de entidades del mundo real.</td>
    </tr>
    <tr>
      <td><strong>Principales pilares</strong></td>
      <td>
        <ul>
          <li><strong>Encapsulamiento:</strong> Oculta los detalles internos y expone solo lo necesario.</li>
          <li><strong>Herencia:</strong> Permite crear nuevas clases basadas en otras existentes.</li>
          <li><strong>Polimorfismo:</strong> Permite que diferentes clases respondan a la misma interfaz de forma distinta.</li>
          <li><strong>Abstracción:</strong> Modela solo los aspectos relevantes de una entidad.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>Ejemplo simple</strong></td>
      <td>
        <pre style="background-color: #f9f9f9; padding: 10px; border: 1px solid #ccc;">
class Persona {
  constructor(nombre) {
    this.nombre = nombre;
  }

  saludar() {
    console.log(`Hola, soy ${this.nombre}`);
  }
}
        </pre>
      </td>
    </tr>
    <tr>
      <td><strong>Ventajas</strong></td>
      <td>
        <ul>
          <li>Mayor modularidad y organización del código</li>
          <li>Facilidad para mantener y escalar proyectos</li>
          <li>Reutilización de componentes</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
