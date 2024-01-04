<h1>Интерфейсы</h1>

<p>Интерфейсы в&nbsp;<code>Java</code>&nbsp;являются конструкцией, которая позволяет объявлять методы для классов, которые его реализуют. В двух словах - это свод правил, который должны соблюдать классы, которые используют интерфейс для реализации.</p>

<p>В&nbsp;<code>Java</code>&nbsp;класс может наследоваться лишь от одного&nbsp;<code>superclass</code>, но может реализовывать неограниченное количество&nbsp;<code>interface</code>.</p>

<p>В своей наиболее распространенной форме&nbsp;<code>interface</code>&nbsp;представляет собой группу методов с пустыми телами.</p>

<p>Рассмотрим пример:</p>

<p>У нас есть простой класс&nbsp;<code>Book</code>&nbsp;у которого есть метод&nbsp;<code>open</code>. Метод&nbsp;<code>open</code>&nbsp;в свою очередь принимает&nbsp;<code>interface</code>&nbsp;<code>Reader</code>, который уже может быть реализован любым классом, тем самым, позволяя, отправлять классы, с разной реализацией метода&nbsp;<code>read</code>. В нашем случае, его реализовывает класс&nbsp;<code>Standard</code>.</p>

<pre>
<code>interface Reader {
    public void read();
}

interface Watcher {
    public void watch();
}

public class Standard implements Reader, Watcher {

    public void read() {
        System.out.println("reading data");
    }

    public void watch() {
        System.out.println("watching");
    }

}
public class Main {

    public static class Book {
        public void open(Reader reader) {
            reader.read();
        }
    }

    public static class BigBrother {
        public void observe(Watcher watcher) {
            watcher.watch();
        }
    }

    public static void main(String[] args) {
        Standard standard = new Standard();

        BigBrother bigBrother = new BigBrother();
        Book book = new Book();

        bigBrother.observe(standard);
        book.open(standard);
    }
}</code></pre>

<p>Реализация&nbsp;<code>interface</code>&nbsp;позволяет классу стать более формальным в отношении поведения, которое он обещает обеспечить. Интерфейсы образуют контракт между классом и внешним миром, и этот контракт применяется компилятором во время сборки. Если ваш класс утверждает, что реализует интерфейс, все методы, определенные этим интерфейсом, должны появиться в его исходном коде прежде чем класс будет успешно скомпилирован.</p>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://docs.oracle.com/javase/tutorial/java/IandI/createinterface.html" rel="nofollow noopener noreferrer">Interface</a></li>
</ul>

<h1>Наследование</h1>

<p>Различные виды объектов часто имеют определенное количество общего друг с другом.</p>

<p>Например, в организации - есть менеджеры и программисты - они имеют общие характеристики (имя, фамилия).</p>

<p>Тем не менее, каждый из них также имеет свои особенности:</p>

<ul>
	<li>Менеджер управляет командой разработчиков.</li>
	<li>Разработчик пишет код на определенном ЯП.</li>
</ul>

<p>Объектно-ориентированное программирование позволяет классам наследовать часто используемые состояния и поведение от других классов.</p>

<p>В этом примере <code>User</code> теперь становится надклассом <code>Manager</code>, <code>Programmer</code>. В языке программирования <code>Java</code> каждому классу разрешено иметь один прямой <code>superclass</code>, и каждый <code>superclass</code> может иметь неограниченное количество подклассов:</p>

<p><img alt="" height="497" name="image.png" src="https://ucarecdn.com/cc1dfa77-43d9-45b3-931e-eacd63011ec7/" width="596"></p>

<p>Для создания наследующего класса, достаточно добавить ключевое слово <code>extends</code>.</p>

<pre><code>// Manager.java
class Manager extends User {
    private Programmer[] programmers;

    Manager(String firstName, String lastName) {
        super(firstName, lastName); // 1
    }
}

// Programmer.java
class Programmer extends User {
    private String language;

    Programmer(String firstName, String lastName) {
        super(firstName, lastName)
    }
}

// Main.java
class Main {
    public static void main(String[] args) {
        Manager manager = new Manager("John", "Doe");
        Programmer programmer = new Programmer("Adam", "Smith");
    }
}</code></pre>

<p>Функция <code>super</code> вызывает конструктор класса - родителя.</p>

<h3>Что вы можете делать в подклассе</h3>

<p>Подкласс наследует все общедоступные и защищенные члены своего родителя, независимо от того, в каком пакете находится подкласс.</p>

<p>Если подкласс находится в том же пакете, что и его родитель, он также наследует закрытые для пакета члены родителя.</p>

<p>Вы можете использовать унаследованные члены как есть, заменять их, скрывать или дополнять новыми членами:</p>

<ul>
	<li>Унаследованные поля можно использовать напрямую, как и любые другие поля.</li>
	<li>Вы можете объявить новые поля в подклассе, которых нет в <code>superclass</code>.</li>
	<li>Унаследованные методы можно использовать напрямую, как они есть.</li>
	<li>Вы можете написать новый метод экземпляра в подклассе, который имеет ту же сигнатуру, что и метод в <code>superclass</code>, тем самым переопределив его.</li>
	<li>Вы можете написать новый статический метод в подклассе, который будет иметь ту же сигнатуру, что и в <code>superclass</code>, тем самым скрыв его.</li>
	<li>Вы можете объявлять новые методы в подклассе, которых нет в <code>superclass</code>.</li>
	<li>Вы можете написать конструктор подкласса, который вызывает конструктор <code>superclass</code> либо неявно, либо с помощью ключевого слова super.</li>
</ul>