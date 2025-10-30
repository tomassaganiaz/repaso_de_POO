🧩 Cuadro 1: Conceptos Clave de OOP

<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; font-family: Arial, sans-serif; width: 100%;"> <tbody> <tr><td><strong>Encapsulamiento</strong></td><td>Protege los datos internos de una clase, exponiendo solo lo necesario mediante métodos públicos como getters y setters.</td></tr> <tr><td><strong>Herencia</strong></td><td>Permite que una clase hija reutilice atributos y métodos de una clase padre, facilitando la extensión del comportamiento.</td></tr> <tr><td><strong>Polimorfismo</strong></td><td>Permite que diferentes clases respondan de forma distinta a la misma interfaz o método, adaptando su comportamiento.</td></tr> <tr><td><strong>Abstracción</strong></td><td>Oculta la complejidad interna y muestra solo lo esencial, ayudando a modelar entidades del mundo real de forma clara.</td></tr> </tbody> </table>

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

🧱 Cuadro 3: Arquitectura MVC + DAO

<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; font-family: Arial, sans-serif; width: 100%;">
  <thead style="background-color: #f2f2f2;">
    <tr><th colspan="2">🧱 Arquitectura MVC + DAO</th></tr>
  </thead>
  <tbody>
    <tr>
      <td style="width: 25%;"><strong>🔄 MVC (Modelo-Vista-Controlador)</strong></td>
      <td>Es un patrón de arquitectura que divide una aplicación en tres componentes principales para separar responsabilidades y facilitar el mantenimiento.</td>
    </tr>
    <tr>
      <td><strong>📦 Modelo</strong></td>
      <td>
        <ul>
          <li>Gestiona los datos, la lógica de negocio y las reglas del sistema.</li>
          <li>Se comunica con la base de datos (usualmente a través de DAO).</li>
          <li>No depende de la interfaz gráfica.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>🖼️ Vista</strong></td>
      <td>
        <ul>
          <li>Muestra la información al usuario.</li>
          <li>Es la interfaz gráfica o presentación.</li>
          <li>No contiene lógica de negocio.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>🎮 Controlador</strong></td>
      <td>
        <ul>
          <li>Recibe las acciones del usuario (clics, formularios, etc.).</li>
          <li>Interpreta las acciones y coordina entre Modelo y Vista.</li>
          <li>Actúa como intermediario lógico.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>🗃️ DAO (Data Access Object)</strong></td>
      <td>
        <ul>
          <li>Componente que actúa como intermediario entre la aplicación y la base de datos.</li>
          <li>Encapsula las operaciones CRUD (crear, leer, actualizar, eliminar).</li>
          <li>Permite separar la lógica de acceso a datos del resto del código.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

