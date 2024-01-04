# Task 1
<p>Напишите функцию <code>addFirstAndLast</code>, которая принимает <code>ArrayList</code>, <code>String</code>, <code>String</code>. Метод должен добавить переменную <code>first</code> в начало списка <code>list</code>, а переменную <code>last</code> в конец <code>list</code>.</p>

<pre><code>public static void addFirstAndLast(ArrayList&lt;String&gt; list, String first, String last) {
    //
}</code></pre>

<p>Класс <code>Main</code> для теста:</p>

<pre><code>public static void main(String[] args) {
    ArrayList&lt;String&gt; list = new ArrayList&lt;String&gt;();
    Scanner scanner = new Scanner(System.in);

    int n = Integer.parseInt(scanner.nextLine());
    for (int i = 0; i &lt; n; i++) {
        list.add(scanner.nextLine());
    }
    String first = scanner.nextLine();
    String last = scanner.nextLine();
    addFirstAndLast(list, first, last);

    for (int i = 0; i &lt; list.size(); i++) {
        System.out.printf("%s ", list.get(i));
    }
    scanner.close();
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html" rel="nofollow noopener noreferrer">ArrayList</a></li>
</ul>

# Task 2


<p>Реализуйте функцию <code>deleteAt</code>, которая принимает <code>ArrayList</code> и <code>index</code>. Необходимо удалить элемент из <code>ArrayList</code> по индексу <code>index</code>.</p>

<pre><code>public static void deleteAt(ArrayList&lt;String&gt; list, int index) {
    //
}</code></pre>

<p>Класс <code>Main</code> для теста:</p>

<pre><code>public static void main(String[] args) {
    ArrayList&lt;String&gt; list = new ArrayList&lt;String&gt;();
    Scanner scanner = new Scanner(System.in);

    int n = Integer.parseInt(scanner.nextLine());
    for (int i = 0; i &lt; n; i++) {
        list.add(scanner.nextLine());
    }
    int index = Integer.parseInt(scanner.nextLine());
    deleteAt(list, index);

    for (int i = 0; i &lt; list.size(); i++) {
        System.out.printf("%s ", list.get(i));
    }
    scanner.close();
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html" rel="nofollow noopener noreferrer">ArrayList</a></li>
</ul>

# Task 3

<p>Реализуйте функцию <code>update</code>, которая принимает <code>ArrayList</code>, <code>index</code>, <code>newValue</code>. Необходимо заменить элемент в <code>ArrayList</code> по <code>index</code> на <code>newValue</code>.</p>

<pre><code>public static void update(ArrayList&lt;String&gt; list, int index, String newValue) {
    //
}</code></pre>

<p>Класс <code>Main</code> для теста:</p>

<pre><code>public static void main(String[] args) {
    ArrayList&lt;String&gt; list = new ArrayList&lt;String&gt;();
    Scanner scanner = new Scanner(System.in);

    int n = Integer.parseInt(scanner.nextLine());
    for (int i = 0; i &lt; n; i++) {
        list.add(scanner.nextLine());
    }
    int index = Integer.parseInt(scanner.nextLine());
    String newValue = scanner.nextLine();
    update(list, index, newValue);

    for (int i = 0; i &lt; list.size(); i++) {
        System.out.printf("%s ", list.get(i));
    }
    scanner.close();
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html" rel="nofollow noopener noreferrer">ArrayList</a></li>
</ul>


# Task 4


<p>Реализуйте функцию <code>compare</code>, которая принимает два <code>ArrayList</code>. Функция должна вернуть: true: если все элементы в первом <code>ArrayList</code> и втором <code>ArrayList</code> идентичны.</p>

<pre><code>public static boolean compare(ArrayList&lt;String&gt; list1, ArrayList&lt;String&gt; list2) {
    return false;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>public static void main(String[] args) {
    ArrayList&lt;String&gt; list1 = new ArrayList&lt;String&gt;();
    ArrayList&lt;String&gt; list2 = new ArrayList&lt;String&gt;();
    Scanner scanner = new Scanner(System.in);

    int n = Integer.parseInt(scanner.nextLine());
    for (int i = 0; i &lt; n; i++) {
        list1.add(scanner.nextLine());
    }
    int n2 = Integer.parseInt(scanner.nextLine());
    for (int i = 0; i &lt; n2; i++) {
        list2.add(scanner.nextLine());
    }
    System.out.println(compare(list1, list2));
    scanner.close();
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html" rel="nofollow noopener noreferrer">ArrayList</a></li>
</ul>

# Task 5


<p>Реализуйте функцию <code>join</code>, которая принимает два <code>ArrayList</code>. Функция должна объединить два <code>ArrayList</code> и вернуть объединенный <code>ArrayList</code>:</p>

<pre><code>public static ArrayList&lt;String&gt; join(ArrayList&lt;String&gt; list1, ArrayList&lt;String&gt; list2) {
    return null;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>public static void main(String[] args) {
    ArrayList&lt;String&gt; list1 = new ArrayList&lt;String&gt;();
    ArrayList&lt;String&gt; list2 = new ArrayList&lt;String&gt;();
    Scanner scanner = new Scanner(System.in);

    int n = Integer.parseInt(scanner.nextLine());
    for (int i = 0; i &lt; n; i++) {
        list1.add(scanner.nextLine());
    }
    int n2 = Integer.parseInt(scanner.nextLine());
    for (int i = 0; i &lt; n2; i++) {
        list2.add(scanner.nextLine());
    }
    List&lt;String&gt; newList = join(list1, list2);
    for (String e : newList)
        System.out.printf("%s ", e);
    scanner.close();
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html" rel="nofollow noopener noreferrer">ArrayList</a></li>
</ul>

# Task 6

<p>Реализуйте функцию <code>clone</code>, которая принимает <code>ArrayList</code>. Функция должна вернуть копию <code>ArrayList</code>:</p>

<pre><code>public static ArrayList&lt;String&gt; copy(ArrayList&lt;String&gt; list) {
    return null;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>public static void main(String[] args) {
    ArrayList&lt;String&gt; list1 = new ArrayList&lt;String&gt;();
    Scanner scanner = new Scanner(System.in);

    int n = Integer.parseInt(scanner.nextLine());
    for (int i = 0; i &lt; n; i++) {
        list1.add(scanner.nextLine());
    }
    List&lt;String&gt; newList = copy(list1);
    list1.set(0, "nulled)");
    for (String e : newList)
        System.out.printf("%s ", e);
    scanner.close();
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html" rel="nofollow noopener noreferrer">ArrayList</a></li>
</ul>

# Task 7


<p>Реализуйте метод <code>maxOccurrences</code>, который принимает <code>List</code> чисел как параметр. Метод должен найти число, повторяющееся чаще всего, и вернуть количество повторений.</p>

<p>Решите эту проблему, используя <code>Map</code> в качестве вспомогательного хранилища. Если список пуст, вернуть 0.</p>

<p>Пример:</p>

<blockquote>
<p>[1, 1, 2, 3, 4]</p>
</blockquote>

<p>Ответ:</p>

<blockquote>
<p><code>2</code></p>
</blockquote>

<p>Число <code>1</code> встречается чаще всего - 2 раза.</p>

<pre><code>public static int maxOccurrences(List&lt;Integer&gt; list) {
        // todo implement
        return 2;
    }</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>public static void main(String[] args) {
    ArrayList&lt;Integer&gt; list = new ArrayList&lt;Integer&gt;();
    Scanner scanner = new Scanner(System.in);

    int n = Integer.parseInt(scanner.nextLine());
    for (int i = 0; i &lt; n; i++) {
        list.add(scanner.nextInt());
    }
    System.out.println(maxOccurrences(list));
    scanner.close();
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Map.html" rel="nofollow noopener noreferrer">Map</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashMap.html" rel="nofollow noopener noreferrer">HashMap</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html" rel="nofollow noopener noreferrer">ArrayList</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/List.html" rel="nofollow noopener noreferrer">List</a></li>
</ul>

# Task 8 
<p>Реализуйте функцию, которая принимает <code>String</code>, состоящий из имен разделенных пробелами.</p>

<p>Вам необходимо вернуть <code>ArrayList&lt;Person&gt;</code> где имена <code>Person</code> содержат больше 5 символов.</p>

<pre><code>class Person {
    private String firstName;

    Person(String firstName) {
        this.firstName = firstName;
    }

    @Override
    public String toString() {
        return this.firstName;
    }
}</code></pre>

<pre><code>public static List&lt;Person&gt; filterNames(String persons) {
    return nil;
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String persons = scanner.nextLine();
        scanner.close();
        List&lt;Person&gt; names = filterNames(persons);
        for (Person p : names) {
            System.out.printf("%s ", p);
        }
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://www.examclouds.com/ru/java/java-core-russian/method-tostring" rel="nofollow noopener noreferrer">toString</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/Override.html" rel="nofollow noopener noreferrer">Override</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html" rel="nofollow noopener noreferrer">ArrayList</a></li>
</ul>

# Task 9
<p>Перед вами стоит задача отсортировать людей по имени и фамилии:</p>

<p>Напишите класс `Person`, в котором будут следующие параметры и методы:</p>

<ul>
	<li>
	<p><code>firstName</code>:String</p>
	</li>
	<li>
	<p><code>lastName</code>:String</p>
	</li>
	<li>
	<p><code>compareTo</code> - вызывает String.compareTo для <code>firstName</code> объекта <code>Person</code> и передает как параметр сравниваемый <code>Person</code>; </p>
	</li>
	<li>
	<p><code>toString</code> - возвращает строку в формате <code>${firstName} ${lastName}</code>;</p>
	</li>
</ul>

<pre><code>class Person implements Comparable&lt;Person&gt; {
    //
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        List&lt;Person&gt; people = new ArrayList&lt;&gt;();
        Scanner scanner = new Scanner(System.in);
        int n = Integer.parseInt(scanner.nextLine());
        for (int i = 0; i &lt; n; i++) {
            String firstName = scanner.nextLine();
            String lastName = scanner.nextLine();
            people.add(new Person(firstName, lastName));
        }
        scanner.close();

        Collections.sort(people, new Comparator&lt;Person&gt;() {
            @Override
            public int compare(Person o1, Person o2) {
                return o1.compareTo(o2);
            }
        });

        for (Person p : people) {
            System.out.println(p);
        }
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/Override.html" rel="nofollow noopener noreferrer">Override</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Comparator.html" rel="nofollow noopener noreferrer">Comparator</a></li>
</ul>

# Task 10
<p>Реализуйте интерфейс <code>Comparator</code> для сортировки элементов в массиве по второму символу.</p>

<pre><code>class MyComparator implements Comparator&lt;String&gt; {
    // Your override here
}</code></pre>

<p>Класс <code>Main</code> для тестов:</p>

<pre><code>class Main {
    public static void main(String[] args) {
        ArrayList&lt;String&gt; people = new ArrayList&lt;&gt;();
        Scanner scanner = new Scanner(System.in);

        int n = scanner.nextLine();
        for (int i = 0; i &lt; n; i++) {
            people.add(scanner.nextLine());
        }
        Collections.sort(people, new MyComparator());
        for (String s : people) {
            System.out.printf("%s ", s);
        }
    }
}</code></pre>

<p>Материалы для изучения:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Collections.html" rel="nofollow noopener noreferrer">Collections</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/Override.html" rel="nofollow noopener noreferrer">Override</a></li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Comparator.html" rel="nofollow noopener noreferrer">Comparator</a></li>
</ul>

