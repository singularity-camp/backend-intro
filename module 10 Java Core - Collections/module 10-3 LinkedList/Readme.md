<h2>LinkedList</h2>

<p><code>LinkedList</code> - это еще одна реализация интерфейса <code>List</code>.</p>

<p>На интенсиве, мы реализовали методы, создавая свой <code>LinkedList</code>. Однако, мы реализовывали список, где каждый элемент имеет лишь связь к следующему элементу. В классе <code>LinkedList</code>, каждая <code>node</code> имеет ссылки на предыдущий и следующие <code>node</code>.</p>

<p><img alt="" height="197" name="image.png" src="https://ucarecdn.com/940d8279-e343-4d12-bcda-ec1c5e4cb2af/" width="516"></p>

<pre><code>import java.util.LinkedList;

public class Main {
    public static void main(String[] args) {
        LinkedList lList = new LinkedList&lt;&gt;(); // 1

        System.out.println("Adding elements to lList...");

        lList.add("Second"); // 2
        lList.add("Third");
        lList.add("Fourth");

        lList.addFirst("First"); // 3
        lList.addLast("Fifth"); // 4

        lList.add(1, "One and half"); // 5

        System.out.println("Initial lList content:");
        System.out.println(lList);

        System.out.println("Removing elements First, Fifth and One and half...");

        lList.removeFirst(); // 6
        lList.removeLast(); // 7
        lList.remove("One and half"); // 8

        System.out.println("Changing element with value Second");
        lList.set(0, "Changed " + lList.get(0)); // 9

        System.out.println("Final lList content:");
        System.out.println(lList);
    }
}</code></pre>

<ol>
	<li>Инициализируем экземпляр класса <code>LinkedList</code>;</li>
	<li>Добавляем новый элемент в конец списка <code>"Second</code>";</li>
	<li>Добавляем новый элемент в начало списка <code>"First</code>";</li>
	<li>Добавляем новый элемент в конец списка <code>"Fifth</code>";</li>
	<li>Добавляем новый элемент по индексу <code>1</code> со значением <code>"One and half</code>";</li>
	<li>Удаляем первый элемент в списке;</li>
	<li>Удаляем последний элемент в списке;</li>
	<li>Удаляем элемент по значению <code>"One and half"</code>;</li>
	<li>Изменяем значение элемента по индексу <code>0</code> в списке.</li>
</ol>

<p>Вывод программы:</p>

<pre><code>Adding elements to lList...
Initial lList content:
[First, One and half, Second, Third, Fourth, Fifth]
Removing elements First, Fifth and One and half...
Changing element with value Second
Final lList content:
[Changed Second, Third, Fourth]</code></pre>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="http://proglang.su/java/linkedlist-class" rel="nofollow noopener noreferrer">Класс LinkedList</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/LinkedList.html" rel="nofollow noopener noreferrer">Java Oracle Doc</a></li>
</ul>