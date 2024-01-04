# Task 1 
<p>Реализуйте метод <code>pairs</code>, который принимает <code>List</code> из <code>String</code> в качестве аргумента. Метод, должен создать <code>Map</code> из всех ключей из двух символов в этих словах.</p>

<p>Пример:</p>

<pre><code>["banana", "bends", "i", "mend", "sandy"]
</code></pre>

<p>Результат:</p>

<pre><code>{an=3, ba=1, be=1, ds=1, dy=1, en=2, me=1, na=2, nd=3, sa=1}
</code></pre>

<pre><code>"ba", "an", "na", "an", "na" - banana
"be", "en", "nd", "ds" - bends
"me", "en", "nd" - mend
"sa", "an", "nd", "dy" - sandy
</code></pre>

<pre><code>public static Map&lt;String, Integer&gt; pairCounts(List&lt;String&gt; list) {
    return null;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List&lt;String&gt; list = new ArrayList&lt;String&gt;();

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            list.add(scanner.nextLine());
        }
        scanner.close();

        Map&lt;String, Integer&gt; res = pairCounts(list);
        List&lt;String&gt; keys = new ArrayList&lt;&gt;(res.keySet());
        Collections.sort(keys);
        for (String e : keys)
            System.out.printf("%s: %d; ", e, res.get(e));
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Map.html" rel="nofollow noopener noreferrer">Map</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashMap.html" rel="nofollow noopener noreferrer">HashMap</a></li>
</ul>

# Task 2
<p>Реализуйте метод <code>intersect</code>, который принимает два <code>Map&lt;String, Integer&gt;</code> в качестве параметров и возвращает новый <code>Map&lt;String, Integer&gt;</code>, содержимое которого является пересечением двух <code>Map</code>. Пересечение двух карт определяется здесь как набор ключей и значений, которые существуют в обеих <code>Map</code>. Поэтому, если какой-то ключ K сопоставляется со значением V как в первой, так и во второй <code>Map</code>, включите его в свой результат. Если K не существует в качестве ключа на обеих картах или если K не соответствует одному и тому же значению V на обеих <code>Map</code>, исключите эту пару из вашего результата.</p>

<pre><code>public static HashMap&lt;String, Integer&gt; intersect(Map&lt;String, Integer&gt; map1, Map&lt;String, Integer&gt; map2) {
    return null;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        HashMap&lt;String, Integer&gt; map1 = new HashMap&lt;String, Integer&gt;();
        HashMap&lt;String, Integer&gt; map2 = new HashMap&lt;String, Integer&gt;();

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            map1.put(scanner.nextLine(), Integer.parseInt(scanner.nextLine()));
        }
        int n2 = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n2; i++) {
            map2.put(scanner.nextLine(), Integer.parseInt(scanner.nextLine()));
        }
        scanner.close();

        Map&lt;String, Integer&gt; res = intersect(map1, map2);
        List&lt;String&gt; keys = new ArrayList&lt;&gt;(res.keySet());
        Collections.sort(keys);
        for (String e : keys)
            System.out.printf("%s %d\n", e, res.get(e));
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Map.html" rel="nofollow noopener noreferrer">Map</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashMap.html" rel="nofollow noopener noreferrer">HashMap</a></li>
</ul>

# Task 3
<p>Реализуйте метод <code>rarest</code>, который принимает в качестве параметра <code>Map</code>, ключи которого являются <code>String</code>, а значения — <code>Integer</code>, и возвращает целочисленное значение, которое встречается в <code>Map</code> наименьшее количество раз. Если есть одинаковые наименьшие, верните меньшее целое значение.</p>

<pre><code>public static int rarest(Map&lt;String, Integer&gt; m) {
	return 0;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        HashMap&lt;String, Integer&gt; map = new HashMap&lt;String, Integer&gt;();

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            map.put(scanner.nextLine(), Integer.parseInt(scanner.nextLine()));
        }
        scanner.close();
        System.out.println(rarest(map));
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Map.html" rel="nofollow noopener noreferrer">Map</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashMap.html" rel="nofollow noopener noreferrer">HashMap</a></li>
</ul>

# Task 4
<p>Напишите метод <code>sumsToTarget</code>, который проверяет, существует ли хотя бы одна пара чисел, сумма которых равна <code>target</code>.</p>

<p>Пример:</p>

<pre><code>arr - [1 3 4]
target - 5
true
</code></pre>

<p>arr=[1, 3, 4] и target=5 вернет <code>true</code>, потому что сумма пары (1,4) равна пяти.</p>

<pre><code>public Boolean sumsToTarget(int[] arr, int target) {
    return false;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int m = sc.nextInt();
        int[] array = new int[m];
        for (int i = 0; i &lt; m; i++)
            array[i] = sc.nextInt();
        int target = sc.nextInt();
        sc.close();
        System.out.println(sumsToTarget(array, target));
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Map.html" rel="nofollow noopener noreferrer">Map</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashMap.html" rel="nofollow noopener noreferrer">HashMap</a></li>
</ul>