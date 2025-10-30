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

🧩 Cuadro 2: Patrones de Diseño + Principios SOLID

<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; font-family: Arial, sans-serif; width: 100%;">
  <thead style="background-color: #f2f2f2;">
    <tr><th colspan="2">🧩 Patrones de Diseño + Principios SOLID</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>🔒 Singleton</strong></td><td><p>Limita la creación de múltiples instancias.</p><ul><li>Útil para configuración global, logs, conexiones.</li><li>Implementación: constructor privado, instancia estática, método <code>getInstance()</code>.</li><li>Beneficios: control centralizado, evita duplicación.</li></ul><pre>
public class Config {
  private static Config instancia;
  private Config() {}
  public static Config getInstance() {
    if (instancia == null) instancia = new Config();
    return instancia;
  }
}
    </pre></td></tr>
    <tr><td><strong>🔗 Chain of Responsibility</strong></td><td><p>Encadena objetos para procesar solicitudes.</p><ul><li>Componentes: Client, Handler abstracto, Handlers concretos.</li><li>Ideal para validaciones, filtros, errores.</li></ul><pre>
abstract class Handler {
  protected Handler siguiente;
  public void setSiguiente(Handler s) { this.siguiente = s; }
  public abstract void manejar(String tipo);
}
    </pre></td></tr>
    <tr><td><strong>🧠 Strategy</strong></td><td><p>Encapsula algoritmos intercambiables.</p><ul><li>Evita <code>switch</code> y <code>if-else</code>.</li><li>Ideal para lógica variable.</li></ul><pre>
interface Estrategia { void ejecutar(); }
class EstrategiaA implements Estrategia { public void ejecutar() { System.out.println("A"); } }
class EstrategiaB implements Estrategia { public void ejecutar() { System.out.println("B"); } }
    </pre></td></tr>
    <tr><td><strong>🏗️ Builder</strong></td><td><p>Construye objetos complejos paso a paso.</p><ul><li>Útil cuando hay muchos atributos opcionales.</li><li>Evita constructores largos.</li></ul><pre>
public class Pizza {
  private String masa, salsa, relleno;
  private Pizza(Builder builder) {
    this.masa = builder.masa;
    this.salsa = builder.salsa;
    this.relleno = builder.relleno;
  }
  public static class Builder {
    private String masa, salsa, relleno;
    public Builder setMasa(String masa) { this.masa = masa; return this; }
    public Builder setSalsa(String salsa) { this.salsa = salsa; return this; }
    public Builder setRelleno(String relleno) { this.relleno = relleno; return this; }
    public Pizza build() { return new Pizza(this); }
  }
}
Pizza pizza = new Pizza.Builder()
  .setMasa("fina")
  .setSalsa("tomate")
  .setRelleno("queso")
  .build();
    </pre></td></tr>
    <tr><td><strong>🧠 Principios SOLID</strong></td><td><ul>
      <li><strong>S - SRP:</strong> Una clase debe tener una única responsabilidad.</li>
      <li><strong>O - OCP:</strong> Abierto para extensión, cerrado para modificación.</li>
      <li><strong>L - LSP:</strong> Las subclases deben sustituir a sus clases base sin alterar el comportamiento.</li>
      <li><strong>I - ISP:</strong> Interfaces específicas, sin métodos innecesarios.</li>
      <li><strong>D - DIP:</strong> Depender de abstracciones, no de implementaciones concretas.</li>
    </ul></td></tr>
  </tbody>
</table>
