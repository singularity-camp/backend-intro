<h1>Map</h1>

<p>Map — объект, с парами ключ-значение. <code>Map</code> не может содержать повторяющиеся ключи; каждый ключ может соответствовать не более чем одному значению.</p>

<h2>HashMap</h2>

<p>Класс HashMap имплементирует интерфейс Map и использует хэш-таблицу. Обеспечивает постоянное время для записи и доступа к элементам.</p>

<p>Для понимания того, как это работает на практике, рассмотрим пример:</p>

<pre>import java.util.HashMap;

class Main {
  public static void main(String[] args) {

    HashMap&lt;Integer, String&gt; languages = new HashMap&lt;&gt;(); // 1
    languages.put(1, "Java"); // 2
    languages.put(2, "Python");
    languages.put(3, "JavaScript");
    System.out.println("Original HashMap: " + languages);

    // change element with key 2
    languages.replace(2, "C++"); // 3
    System.out.println("HashMap using replace(): " + languages);
  }
}</pre>

<ol>
	<li>Создание <code>HashMap</code>, где ключ это <code>Integer</code>, а значение - <code>String</code>;</li>
	<li>Добавление элемента;</li>
	<li>Изменение элемента по ключу;</li>
</ol>

<pre><code>Original HashMap: {1=Java, 2=Python, 3=JavaScript}
HashMap using replace(): {1=Java, 2=C++, 3=JavaScript}
</code></pre>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://www.programiz.com/dsa/hash-table" rel="nofollow noopener noreferrer">hash table</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashMap.html" rel="nofollow noopener noreferrer">Java Oracle Doc HashMap</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Map.html" rel="nofollow noopener noreferrer">Java Oracle Doc Map</a></li>
	<li><a href="https://javarush.ru/groups/posts/1940-klass-hashmap-" rel="nofollow noopener noreferrer">HashMap Ru</a></li>
</ul>