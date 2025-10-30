# repaso_de_POO
<style>
  body { font-family: Arial, sans-serif; background-color: #f9f9f9; padding: 20px; }
  .card { background-color: #ffffff; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); margin-bottom: 20px; padding: 20px; }
  .card h2 { color: #2c3e50; border-bottom: 2px solid #ecf0f1; padding-bottom: 5px; }
  .card ul { list-style: none; padding-left: 0; }
  .card li { margin-bottom: 10px; }
  .highlight { background-color: #ecf0f1; padding: 5px; border-radius: 5px; }
  .code { background-color: #f4f4f4; font-family: monospace; padding: 10px; border-radius: 5px; }
</style>

<div class="card">
  <h2>🧱 Programación Orientada a Objetos (POO)</h2>
  <ul>
    <li><strong>Clase:</strong> Plantilla que define atributos y métodos. <span class="highlight">Ej: class Persona</span></li>
    <li><strong>Objeto:</strong> Instancia concreta de una clase. <span class="highlight">Ej: juan = Persona()</span></li>
    <li><strong>Atributos:</strong> Variables internas. <span class="highlight">Ej: self.nombre</span></li>
    <li><strong>Función:</strong> Bloque de código independiente.</li>
    <li><strong>Método:</strong> Función dentro de una clase.</li>
    <li><strong>Herencia:</strong> Reutilización de atributos y métodos entre clases.</li>
    <li><strong>MRO:</strong> Orden de resolución de métodos en herencia múltiple. <span class="highlight">Ej: Clase.__mro__</span></li>
    <li><strong>Polimorfismo:</strong> Mismo método, comportamiento distinto.</li>
    <li><strong>Encapsulamiento:</strong> Oculta detalles internos. <span class="highlight">Ej: _privado, __muy_privado</span></li>
    <li><strong>Getter / Setter:</strong> Métodos para acceder o modificar atributos.</li>
    <li><strong>Decoradores:</strong> Modifican funciones. <span class="highlight">@staticmethod, @property</span></li>
    <li><strong>Abstracción:</strong> Oculta complejidad. <span class="highlight">ABC, @abstractmethod</span></li>
    <li><strong>Métodos especiales:</strong> Personalizan comportamiento. <span class="highlight">__init__, __str__</span></li>
    <li><strong>Variables:</strong> Espacios de memoria. <span class="code">edad = 25</span></li>
    <li><strong>Variables tipadas:</strong> Definen tipo de dato. <span class="code">int edad = 25; string nombre = "Tomás";</span></li>
  </ul>
</div>

<div class="card">
  <h2>🧩 Principios S.O.L.I.D.</h2>
  <ul>
    <li><strong>SRP:</strong> Una clase = una responsabilidad.</li>
    <li><strong>OCP:</strong> Abierto a extensión, cerrado a modificación.</li>
    <li><strong>LSP:</strong> Subclases deben sustituir sin romper lógica.</li>
    <li><strong>ISP:</strong> Interfaces específicas, no obligatorias.</li>
    <li><strong>DIP:</strong> Depender de abstracciones, no implementaciones.</li>
  </ul>
</div>

<div class="card">
  <h2>🧠 Patrones de Diseño</h2>
  <ul>
    <li><strong>Singleton:</strong> Una sola instancia compartida.
      <div class="code">
        public class Config {<br>
        &nbsp;&nbsp;private static Config instancia;<br>
        &nbsp;&nbsp;private Config() {}<br>
        &nbsp;&nbsp;public static Config getInstance() {<br>
        &nbsp;&nbsp;&nbsp;&nbsp;if (instancia == null) instancia = new Config();<br>
        &nbsp;&nbsp;&nbsp;&nbsp;return instancia;<br>
        &nbsp;&nbsp;}<br>
        }
      </div>
    </li>
    <li><strong>Chain of Responsibility:</strong> Encadena handlers para procesar solicitudes.
      <div class="code">
        abstract class Handler {<br>
        &nbsp;&nbsp;protected Handler siguiente;<br>
        &nbsp;&nbsp;public void setSiguiente(Handler s) { this.siguiente = s; }<br>
        &nbsp;&nbsp;public abstract void manejar(String tipo);<br>
        }
      </div>
    </li>
    <li><strong>Strategy:</strong> Algoritmos intercambiables.
      <div class="code">
        interface Estrategia { void ejecutar(); }<br>
        class EstrategiaA implements Estrategia {<br>
        &nbsp;&nbsp;public void ejecutar() { System.out.println("A"); }<br>
        }<br>
        class EstrategiaB implements Estrategia {<br>
        &nbsp;&nbsp;public void ejecutar() { System.out.println("B"); }<br>
        }
      </div>
    </li>
    <li><strong>Builder:</strong> Construcción paso a paso de objetos complejos.</li>
  </ul>
</div>

<div class="card">
  <h2>🧭 Arquitectura MVC + DAO</h2>
  <ul>
    <li><strong>Modelo:</strong> Lógica de negocio y acceso a datos.</li>
    <li><strong>Vista:</strong> Interfaz gráfica o presentación.</li>
    <li><strong>Controlador:</strong> Coordina acciones entre modelo y vista.</li>
    <li><strong>DAO:</strong> Intermediario entre aplicación y base de datos.</li>
  </ul>
</div>
