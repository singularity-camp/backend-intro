<h1>Annotations</h1>

<p>В прошлых задачах, мы оборачивали методы используя ключевое слово <code>@Override</code>.</p>

<p>Данная конструкция сообщает компилятору, что элемент предназначен для переопределения элемента, объявленного в классе родителя.</p>

<p>Аннотация не является частью самой программы, это метаданные, которые могут быть использованы как:</p>

<ul>
	<li>инструкции для компилятора;</li>
</ul>

<pre><code>@SuppressWarnings - отключает вывод предупреждений компилятора, которые касаются элемента над которым она указана
@Override
@Deprecated
</code></pre>

<ul>
	<li>инструкции во время компиляции;</li>
</ul>

<pre><code>используются `javac` для генерации кода.
</code></pre>

<ul>
	<li>инструкции во время работы программы;</li>
</ul>

<pre><code>@Retention
@Target
</code></pre>

<p>Более подробно об аннотациях можно ознакомиться в данном видео:</p>

<p><iframe allowfullscreen="" height="315" src="https://www.youtube.com/embed/_kmh1m0BH3s?start=1937" width="560"></iframe></p>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://docs.oracle.com/javase/tutorial/java/annotations/index.html" rel="nofollow noopener noreferrer">Java Annotations</a></li>
</ul>

<h1>Generics</h1>

<p>Generics - это инструмент для абстракции от системы типов в <code>Java</code>.</p>

<p>Дженерики - усовершенствование системы типов, которое позволяет типу или методу работать с объектами различных типов, обеспечивая при этом безопасность типов во время компиляции. Дженерики добавляют безопасность типов во время компиляции в <code>Collections Framework</code> и устраняют нудную работу по приведению типов.</p>

<p>Рассмотрим пример:</p>

<p>Нам необходимо создать список, хранящий данные типа <code>Integer</code>:</p>

<p>Код будет выглядеть так:</p>

<pre><code>List list = new LinkedList();
list.add(new Integer(1)); 
Integer i = list.iterator().next();</code></pre>

<p>Последняя строка будет вызывать ошибку, компилятор требует от нас явного приведения типа.</p>

<pre><code>Integer i = (Integer) list.iterator.next();</code></pre>

<p>Давайте усовершенствуем наш код, используя дженерики:</p>

<pre><code>List&lt;Integer&gt; 
    myIntList = new LinkedList&lt;Integer&gt;(); // 1
myIntList.add(new Integer(1));
Integer x = myIntList.iterator().next(); // 2</code></pre>

<ol>
	<li>Мы явно указываем тип нашего списка в знаки <code>&lt;&gt;</code>, тем самым, даем информацию для компилятора о типе данных с которыми мы собираемся работать.</li>
	<li>Мы без явного приведения получаем элемент из нашего списка.</li>
</ol>

<h2>Обобщенные классы</h2>

<pre><code>class Struct&lt;T, S&gt; { // 1
    public T id; // 2
    public S value; // 3

    Struct(T id, S value) { // 4
        this.id = id;
        this.value = value;
    }
}

class Main {
    public static void main(String[] args) {
        Struct&lt;String, Integer&gt; one = new Struct&lt;String, Integer&gt;("id", 2); // 5
        Struct&lt;Integer, Integer&gt; two = new Struct&lt;Integer, Integer&gt;(3, 3); // 5
        String oneId = one.id;
        Integer twoId = two.id;
        System.out.println(oneId);
        System.out.println(twoId);
    }
}</code></pre>

<ol>
	<li>Указываем, что структура имеет два обобщенных значения, которые задаются в шаге <code>5</code></li>
	<li>Создание обобщенной переменной <code>id</code></li>
	<li>Создание обобщенной переменной <code>value</code></li>
	<li>Конструктор</li>
</ol>

<h2>Обобщенные методы</h2>

<p>Мы можем создавать свои методы, для работы с разными типами данных:</p>

<p>Синтаксис таких методов выглядит так:</p>

<pre><code>public &lt;T&gt; List&lt;T&gt; fromArrayToList(T[] a) {   
    return Arrays.stream(a).collect(Collectors.toList());
}</code></pre>

<p>Конструкция <code>&lt;T&gt;</code> указывает на то, что метод взаимодействует с различными типами данных.</p>

<pre><code>Integer[] a = new Integer[2];
a[0] = 2;
a[1] = 3;
List&lt;Integer&gt; list = fromArrayToList(a);</code></pre>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://www.baeldung.com/java-generics" rel="nofollow noopener noreferrer">Basic of generics</a></li>
	<li><a href="https://docs.oracle.com/javase/tutorial/extra/generics/index.html" rel="nofollow noopener noreferrer">Java Generics</a></li>
</ul>