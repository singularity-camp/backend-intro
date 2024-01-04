<h1>Set</h1>

<p>Set — коллекция, которая не может содержать повторяющиеся элементы.</p>

<p>В <code>java</code> имеется три реализации данного интерфейса: <code>HashSet</code>, <code>TreeSet</code>, <code>LinkedHashSet</code>.</p>

<h2>HashSet</h2>

<p><code>HashSet</code> - это набор уникальных данных, для хранения данных используется хэширование (создание уникального идентификатора на основе значение элемента). Результат хэш-функции является хэш-код.</p>

<p>В отличие от обычного <code>ArrayList</code> или <code>LinkedList</code> поиск элемента в <code>HashSet</code> занимает 1 операцию. Это достигается благодаря <code>hash</code> функции, которая работает под капотом и позволяет сохранять и добавлять данные по хэш-значению.</p>

<p><code>HashSet</code> - не сортируется под капотом, при каждой попытке вывести весь <code>set</code> мы будем получать разную последовательность значений. В <code>HashSet</code> добавление и удаление элементов проходит быстро.</p>

<pre><code>import java.util.HashSet;

public class Main {
    public static void main(String[] args) {
        HashSet hashSet = new HashSet&lt;String&gt;();

        System.out.println("Adding element into hashSet...");
        hashSet.add("Charlie");
        hashSet.add("Delta");
        hashSet.add("Alpha");
        hashSet.add("Echo");
        hashSet.add("Bravo");

        hashSet.remove("Alpha");

        Iterator&lt;String&gt; i = hashSet.iterator();
        while (i.hasNext())
            System.out.println(i.next());
    }
}</code></pre>

<p>Вывод программы:</p>

<pre><code>/*Some System Messages*/

Adding element into hashSet...
Delta
Echo
Charlie
Bravo
</code></pre>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashSet.html" rel="nofollow noopener noreferrer">Java Oracle Doc HashSet</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Set.html" rel="nofollow noopener noreferrer">Java Oracle Doc Set</a></li>
	<li><a href="https://www.baeldung.com/java-hashset" rel="nofollow noopener noreferrer">HashSet</a></li>
	<li><a href="https://javarush.ru/groups/posts/2147-hashset-v-java" rel="nofollow noopener noreferrer">HashSet Ru</a></li>
</ul>