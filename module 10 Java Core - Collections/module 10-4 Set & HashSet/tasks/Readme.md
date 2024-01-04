# Task 1
<p>Реализуйте функцию <code>create</code>, которая принимает <code>String[]</code>. Функция должна создать <code>HashSet</code> с элементами из <code>String[]</code>:</p>

<pre><code>public static HashSet&lt;String&gt; create(String[] params) {
    return null;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    int n = Integer.parseInt(scanner.nextLine());
    String[] params = new String[n];
    for (int i = 0; i &lt; n; i++) {
        params[i] = scanner.nextLine();
    }

    ArrayList&lt;String&gt; result = new ArrayList&lt;&gt;(create(params));
    Collections.sort(result);
    for (String e : result)
        System.out.printf("%s ", e);
    scanner.close();
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Set.html" rel="nofollow noopener noreferrer">Set</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashSet.html" rel="nofollow noopener noreferrer">HashSet</a></li>
</ul>

# Task 2
<p>Напишите метод <code>maxLength</code>, который принимает набор строк в качестве параметра и возвращает длину самой длинной строки в наборе. Если вашему методу передается пустой набор, он должен вернуть 0.</p>

<pre><code>public static int maxLength(Set&lt;String&gt; set) {
	return 0;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>public static void main(String[] args) {
	Scanner scanner = new Scanner(System.in);
	Set&lt;String&gt; set = new HashSet&lt;String&gt;();
	int n = Integer.parseInt(scanner.nextLine());
	for (int i = 0; i &lt; n; i++) {
		set.add(scanner.nextLine());
	}
	scanner.close();
	System.out.printf("%d", maxLength(set));
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Set.html" rel="nofollow noopener noreferrer">Set</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashSet.html" rel="nofollow noopener noreferrer">HashSet</a></li>
</ul>

# Task 3
<p>Напишите функцию <code>uniqueAdd</code>. Функция принимает массив имен. Имена необходимо добавить в <code>HashSet</code> При добавлении дубликата, функция должна выводить в консоль <code>There is only one &lt;name&gt;</code>, где <code>name</code> - это имя.</p>

<pre><code>public static void uniqueAdd(String[] names) {
    //
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine());
        String[] names = new String[n];
        for (int i = 0; i &lt; n; i++) {
            names[i] = scanner.nextLine();
        }
        scanner.close();
        uniqueAdd(names);
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Set.html" rel="nofollow noopener noreferrer">Set</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashSet.html" rel="nofollow noopener noreferrer">HashSet</a></li>
</ul>

# Task 4
<p>Реализуйте метод <code>isPermutationOf</code>, которая определяет, является ли строка <code>permutation</code> другой строки.</p>

<pre><code>static boolean isPermutationOf(String a, String b) {
    return true;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println(isPermutationOf(scanner.nextLine(), scanner.nextLine()));
        scanner.close();
    }

}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Set.html" rel="nofollow noopener noreferrer">Set</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashSet.html" rel="nofollow noopener noreferrer">HashSet</a></li>
	<li><a href="https://en.wikipedia.org/wiki/Permutation" rel="nofollow noopener noreferrer">Permutation</a></li>
</ul>

# Task 5 
<p>Напишите метод <code>hasOdd</code>, который принимает набор целых чисел в качестве параметра и возвращает значение <code>true</code>, если набор содержит хотя бы одно нечетное целое число, и значение <code>false</code> в противном случае. Если передан пустой набор, ваш метод должен вернуть <code>false</code>.</p>

<pre><code>public static boolean hasOdd(Set&lt;Integer&gt; set) {
    return false;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Set&lt;Integer&gt; set = new HashSet&lt;Integer&gt;();
        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            set.add(scanner.nextInt());
        }
        scanner.close();
        System.out.println(hasOdd(set));
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Set.html" rel="nofollow noopener noreferrer">Set</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashSet.html" rel="nofollow noopener noreferrer">HashSet</a></li>
</ul>

# Task 6

<p>Представьте, что вы преподаватель, которому нужно выставить оценки студентам и рассчитать среднюю оценку в <code>classroom</code>.</p>

<p>Реализуйте классы <code>Student</code> и <code>Classroom</code> на основе функции <code>main</code> и правильных ответов.</p>

<pre><code>class Main {
    public static void main(String[] args) {
        Classroom classroom = new Classroom();
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            String name = scanner.nextLine();
            int points = Integer.parseInt(scanner.nextLine());
            Student s = new Student();
            s.setId(i + 1);
            s.setName(name);
            s.setPoints(points);
            classroom.addStudent(s);
        }
        scanner.close();
        for (Student s : classroom) {
            System.out.println(s);
        }
        System.out.printf("Average: %.2f", classroom.getAverage());
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Set.html" rel="nofollow noopener noreferrer">Set</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/Override.html" rel="nofollow noopener noreferrer">Override</a></li>
	<li><a href="https://www.baeldung.com/java-instanceof" rel="nofollow noopener noreferrer">instance of</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/Iterable.html" rel="nofollow noopener noreferrer">Iterable</a></li>
	<li><a href="http://proglang.su/java/strings-equals" rel="nofollow noopener noreferrer">equals</a></li>
</ul>