<h1>Полиморфизм</h1>

<p>Словарное определение полиморфизма относится к принципу биологии, согласно которому организм или вид могут иметь множество различных форм или стадий. Этот принцип можно также применить к объектно-ориентированному программированию и таким языкам как Java. Подклассы класса могут определять свое собственное уникальное поведение и при этом использовать некоторые из тех же функций родительского класса.</p>

<pre><code>// User.java
class User {
    private String firstName;
    private String lastName;

    User(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
    
    public void describe() { // 1
        System.out.printf("%s %s\n", this.firstName, this.lastName);
    }
}

// Manager.java
class Manager extends User {
    private Programmer[] programmers;

    Manager(String firstName, String lastName) {
        super(firstName, lastName); // 2
    }

    public void describe() {
        System.out.printf("Manager: ");
        super.describe(); // 3
    }

}

// Programmer.java
class Programmer extends User {
    private String language;

    Programmer(String firstName, String lastName) {
        super(firstName, lastName) // 2
    }

    public void describe() {
        System.out.printf("Programmer: ");
        super.describe(); // 3
    }
}

// Main.java
class Main {
    public static void main(String[] args) {
        Manager manager = new Manager("John", "Doe");
        Programmer programmer = new Programmer("Adam", "Smith");
        manager.describe();
        programmer.describe();
    }
}</code></pre>

<p>Вывод программы:</p>

<pre><code>Manager: John Doe
Programmer: Adam Smith
</code></pre>

<ol>
	<li>Реализация метода <code>describe</code> для класса <code>User</code>;</li>
	<li>Вызов конструктора у <code>superclass</code>;</li>
	<li>Вызов метода <code>describe</code> на <code>subclass</code>;</li>
</ol>

<p><code>super</code> - это ключевое слово, которое позволяет обращаться к <code>superclass</code>.</p>

<p>В <code>Java</code> вы можете декларировать переменную родительского класса, при этом задать ей значение класса наследника:</p>

<pre><code>User manager = new Manager("John", "Doe");
manager.describe(); // John Doe</code></pre>

<p>Мы создали экземпляр класса <code>Manager</code> и присвоили его переменной типа <code>User</code>. Нам будут доступны только методы класса <code>User</code>. Несмотря на это, мы можем преобразовать <code>superclass</code> и <code>subclass</code>:</p>

<pre><code>User user = new Manager("John", "Doe");
Manager manager = (Manager)user;
manager.describe(); // Manager: John Doe</code></pre>