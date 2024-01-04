<h1>List</h1>

<p>List - последовательный список. Списки могут содержать повторяющиеся элементы. Пользователь списка обычно имеет точный контроль над тем, где в списке вставлен каждый элемент, и может получить доступ к элементам по их целочисленному индексу (позиции).</p>

<h2>ArrayList</h2>

<p>ArrayList - это класс, реализующий интерфейс&nbsp;<code>List</code>.&nbsp;<code>ArrayList</code>&nbsp;похож на статический&nbsp;<code>Array</code>, однако,&nbsp;<code>ArrayList</code>&nbsp;является динамическим. Это значит, что у него легко изменяется длина, можно добавлять и удалять элементы, вызывая встроенные методы&nbsp;<code>add()</code>&nbsp;и&nbsp;<code>remove()</code>.</p>

<p><img alt="" height="1132" name="image.png" src="https://ucarecdn.com/4fc24c0b-2559-41ca-a0ee-291fba3dfa99/" width="3531" /></p>

<pre>
<code>import java.util.ArrayList;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List myList = new ArrayList&lt;&gt;(); // 1

        myList.add("One"); // 2
        myList.add("Two");
        myList.add("Three");

        System.out.println("size of myList: " + myList.size()); // 3
        System.out.println("myList content: " + myList); // 4

        myList.remove("One"); // 5
        myList.remove(1); // 6

        System.out.println("size of myList: " + myList.size()); 
        System.out.println("myList content: " + myList);
    }
}</code></pre>

<ol>
	<li>Инициализируем экземпляр класса&nbsp;<code>ArrayList</code>;</li>
	<li>Добавляем новый элемент&nbsp;<code>&quot;One</code>&quot;;</li>
	<li>Выводим длину&nbsp;<code>myList</code>;</li>
	<li>Выводим значения в&nbsp;<code>myList</code>;</li>
	<li>Удаляем элемент по значению&nbsp;<code>One</code>;</li>
	<li>Удаляем элемент по индексу;</li>
</ol>

<p>Вывод программы:</p>

<pre>
<code>size of myList: 3
myList content: [One, Two, Three]
size of myList: 1
myList content: [Two]</code></pre>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://metanit.com/java/tutorial/5.2.php" rel="nofollow noopener noreferrer">Класс ArrayList</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html" rel="nofollow noopener noreferrer">Java Oracle Doc</a></li>
</ul>
