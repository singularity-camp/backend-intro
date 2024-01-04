<h1>Введение</h1>

<p>Java достаточно взрослый язык, он существует с 1995 года. За время существования он улучшался и на сегодняшний день (февраль 2022 года) вышла Java версии 17. Со списком всех версий вы можете познакомиться <a href="https://ru.wikipedia.org/wiki/%D0%98%D1%81%D1%82%D0%BE%D1%80%D0%B8%D1%8F_%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B9_Java_SE" rel="nofollow noopener noreferrer">здесь</a>.</p>

<p>В этом уроке мы рассмотрим основные понятия, необходимые для разработки на <code>Java</code> на вашем компьютере.</p>

<p>Мы напишем простую программу, скомпилируем ее и запустим. Программа выведет в терминал <code>Hello World!</code>.</p>

<h2>Создание файла</h2>

<p>Для начала создадим папку <code>helloworld</code> и в ней создадим файл <code>HelloWorld.java</code>.</p>

<pre><code>mkdir helloworld
cd helloworld
touch HelloWorld.java</code></pre>

<p>В созданный файл напишем:</p>

<pre><code>public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}</code></pre>

<p>Любая программа должна иметь точку входа (место, где начинается выполнение программы).</p>

<p>В <code>Java</code> точкой входа является функция <code>main</code></p>

<pre><code>public static void main(String[] args) { }</code></pre>

<p>Давайте рассмотрим каждое ключевое слово:</p>

<ul>
	<li><code>public</code> - это модификатор доступа, означает, что его можно вызывать вне пакета;</li>
	<li><code>static</code> - метод может быть вызван без создания экземпляра класса;</li>
	<li><code>void</code> - данная функция ничего не вернет;</li>
	<li><code>main</code> - название функции;</li>
	<li><code>String[] args</code> - массив параметров с которыми была запущена программа <code>java HelloWorld foo bar</code>;</li>
</ul>


# Homework
1. Завершить тест по итогам урока в LMS