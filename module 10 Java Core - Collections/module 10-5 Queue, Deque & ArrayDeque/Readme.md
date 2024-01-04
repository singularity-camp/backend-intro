<h1>Queue &amp; Deque</h1>

<p><code>Queue</code> — коллекция, используемая для хранения нескольких элементов перед обработкой. Помимо основных операций с коллекцией, очередь предоставляет дополнительные операции вставки, извлечения и проверки. Очереди обычно, но не обязательно, упорядочивают элементы в порядке FIFO (первым поступил, первым обслужен). Среди исключений есть очереди с приоритетом, которые упорядочивают элементы в соответствии с предоставленным компаратором или естественным порядком элементов. Какой бы порядок ни использовался, глава очереди — это элемент, который будет удален вызовом remove или poll. В очереди FIFO все новые элементы вставляются в конец очереди. Другие виды очередей могут использовать другие правила размещения. Каждая реализация Queue должна указывать свои свойства упорядочения.</p>

<p><img alt="" height="196" name="image.png" src="https://ucarecdn.com/a3c131d9-a57c-437c-9e24-e55de2c3d20c/" width="529"></p>

<p><code>Deque</code> — коллекция, используемая для хранения нескольких элементов перед обработкой. Помимо основных операций Collection, Deque предоставляет дополнительные операции вставки, извлечения и проверки. Deque может использоваться как в порядке FIFO (первый пришел, первый ушел), так и LIFO (последний пришел, первый ушел). В deque все новые элементы могут быть вставлены, извлечены и удалены с обоих концов. Особенным отличием от других структур данных, является то, что в его реализации не должно быть добавления, получения элемента по индексу, что значит, что можно добавлять либо в начало или конец, аналогично с получением и удалением элемента.</p>

<p><img alt="" height="175" name="image.png" src="https://ucarecdn.com/da09a9cb-7216-42c6-b6c3-48a741f9520f/" width="505"></p>

<h2> </h2>

<ul>
</ul>


<h2>ArrayDeque</h2>

<p>ArrayDeque - это класс, который работает по принципу стека и очереди (LIFO - FIFO).</p>

<p>Это значит, что элементы можно добавлять как в начало, так и в конец. То же самое относится к удалению элементов.</p>

<p>ArrayDeque - класс, в котором реализованы методы для работы с данными по типу структуры <code>deque</code>.</p>

<pre><code>import java.util.ArrayDeque;
import java.util.Iterator;

class Main {
    public static void main(String[] args) {
        ArrayDeque&lt;String&gt; animals= new ArrayDeque&lt;String&gt;(); // 1

        animals.add("Dog"); // 2

        animals.addFirst("Cat"); // 3

        animals.addLast("Horse"); // 4

        String element = animals.peek(); // 5
        System.out.println("Head Element: " + element);

        String firstElement = animals.peekLast(); // 6
        System.out.println("First Element: " + firstElement);

        Iterator&lt;String&gt; iterate = animals.iterator(); // 7
        while(iterate.hasNext()) { // 8
            System.out.print(iterate.next()); // 9
            System.out.print(", ");
        }
    }
}</code></pre>

<ol>
	<li>Создание экземпляра класса <code>ArrayDeque</code>;</li>
	<li>Добавление в начало элемента <code>"Dog"</code>;</li>
	<li>Добавление в начало элемента <code>"Cat"</code>;</li>
	<li>Добавление в конец элемента <code>"Horse"</code>;</li>
	<li>Получение первого элемента;</li>
	<li>Получение последнего элемента;</li>
	<li>Создание <code>Iterator</code>, для прохождения по элементам;</li>
	<li>Проверка на наличие элемента;</li>
	<li>Получение значения;</li>
</ol>

<p>Вывод программы:</p>

<pre><code>Head Element: Cat
First Element: Horse
Cat, Dog, Horse,</code></pre>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://www.programiz.com/dsa/queue" rel="nofollow noopener noreferrer">queue</a></li>
	<li><a href="https://www.programiz.com/dsa/deque" rel="nofollow noopener noreferrer">deque</a></li>
	<li><a href="https://www.programiz.com/dsa/stack" rel="nofollow noopener noreferrer">stack</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayDeque.html" rel="nofollow noopener noreferrer">Java Oracle Doc ArrayDeque</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Queue.html" rel="nofollow noopener noreferrer">Java Oracle Doc Queue</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Deque.html" rel="nofollow noopener noreferrer">Java Oracle Doc Deque</a></li>
</ul>