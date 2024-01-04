# Task 1
<p>Реализуйте функцию <code>addToEnd</code>, которая принимает <code>LinkedList</code>, <code>newValue</code>. Необходимо добавить <code>newValue</code> в конец <code>LinkedList</code>.</p>

<pre><code>public static void addToEnd(LinkedList&lt;String&gt; list, String newValue) {
    //
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        LinkedList&lt;String&gt; list = new LinkedList&lt;String&gt;();
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            list.add(scanner.nextLine());
        }
        String newValue = scanner.nextLine();
        addToEnd(list, newValue);

        for (int i = 0; i &lt; list.size(); i++) {
            System.out.printf("%s ", list.get(i));
        }
        scanner.close();
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/LinkedList.html" rel="nofollow noopener noreferrer">LinkedList</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
</ul>

# Task 2
<p>Реализуйте функцию <code>addToFront</code>, которая принимает <code>LinkedList</code>, <code>newValue</code>. Необходимо добавить <code>newValue</code> в начало <code>LinkedList</code>.</p>

<pre><code>public static void addToFront(LinkedList&lt;String&gt; list, String newValue) {
    //
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        LinkedList&lt;String&gt; list = new LinkedList&lt;String&gt;();
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            list.add(scanner.nextLine());
        }
        String newValue = scanner.nextLine();
        addToFront(list, newValue);

        for (int i = 0; i &lt; list.size(); i++) {
            System.out.printf("%s ", list.get(i));
        }
        scanner.close();
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/LinkedList.html" rel="nofollow noopener noreferrer">LinkedList</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
</ul>

# Task 3
<p>Реализуйте функцию <code>reverseIter</code>, которая принимает <code>LinkedList</code>. Необходимо вывести в консоль все элементы в обратном порядке.</p>

<pre><code>public static void reverseIter(LinkedList&lt;String&gt; list) {
    //
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        LinkedList&lt;String&gt; list = new LinkedList&lt;String&gt;();
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            list.add(scanner.nextLine());
        }
        reverseIter(list);
        scanner.close();
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/LinkedList.html" rel="nofollow noopener noreferrer">LinkedList</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Iterator.html" rel="nofollow noopener noreferrer">Iterator</a></li>
</ul>

# Task 4
<p>Реализуйте функцию <code>replace</code>, которая принимает <code>LinkedList</code>, <code>index</code>, <code>newValue</code>. Необходимо изменить элемент, который находится в <code>index</code> на <code>newValue</code>.</p>

<pre><code>public static void replace(LinkedList&lt;String&gt; list, int index, String newValue) {
    //
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        LinkedList&lt;String&gt; list = new LinkedList&lt;String&gt;();
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            list.add(scanner.nextLine());
        }
        int index = Integer.parseInt(scanner.nextLine());
        String newValue = scanner.nextLine();
        replace(list, index, newValue);

        for (int i = 0; i &lt; list.size(); i++) {
            System.out.printf("%s ", list.get(i));
        }
        scanner.close();
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/LinkedList.html" rel="nofollow noopener noreferrer">LinkedList</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
</ul>

# Task 5
<p>Реализуйте функцию <code>isPalindrome</code>, которая принимает <code>LinkedList</code>. Необходимо вернуть <code>true</code>, если список является <code>palindrome</code>, в другом случае, вернуть <code>false</code>.</p>

<pre><code>public static boolean isPalindrome(LinkedList&lt;Integer&gt; list) {
    return false;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        LinkedList&lt;Integer&gt; list = new LinkedList&lt;Integer&gt;();
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            list.add(scanner.nextInt());
        }
        System.out.println(isPalindrome(list));
        scanner.close();
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/LinkedList.html" rel="nofollow noopener noreferrer">LinkedList</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
</ul>

# Task 6

<p>Реализуйте функцию <code>oddEvenOrder</code>, которая принимает <code>LinkedList</code> - <code>list</code>. Создайте новый список, где вначале будут находиться элементы с нечетным индексом из параметра <code>list</code>, за которым будут находиться элементы с четными индексами.</p>

<p>Первый узел считается нечетным, второй — четным и так далее.</p>

<pre><code>public static LinkedList&lt;Integer&gt; oddEvenOrder(LinkedList&lt;Integer&gt; list) {
    // 
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        LinkedList&lt;Integer&gt; list = new LinkedList&lt;Integer&gt;();
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            list.add(scanner.nextInt());
        }
        LinkedList&lt;Integer&gt; list2 = oddEvenOrder(list);
        for (int i = 0; i &lt; list2.size(); i++) {
            System.out.printf("%s ", list2.get(i));
        }
        scanner.close();
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/LinkedList.html" rel="nofollow noopener noreferrer">LinkedList</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
</ul>

