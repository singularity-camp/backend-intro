v<h1>Исключения</h1>

<p>Во время работы программы, возможны ситуации, когда происходит непредвиденное поведение: деление на ноль. мы знаем из уроков математики, что на&nbsp;<code>ноль</code>&nbsp;делить нельзя.&nbsp;<code>Java</code>&nbsp;обрабатывает подобные случаи, выбрасывая исключения.</p>

<pre>
<code>class UncaughtException
{
    public static void main(String args[]) {
        int a = 0;
        int b = 7/a;     // Произойдет исключение
    }
}</code></pre>

<p><code>Исключение</code>&nbsp;&mdash; это состояние, возникающее во время выполнения программы и приводящее к аварийному завершению программы. Может быть несколько причин, которые могут привести к исключениям, в том числе ошибка программиста, аппаратные сбои,исчерпание ресурсов и т. д.</p>

<p>Предположим, мы запускаем программу для чтения данных из файла, и если файл недоступен, программа остановит выполнение и завершит программу, сообщив об исключении.</p>

<p>Проблема с исключением заключается в том, что оно&nbsp;<code>завершает</code>&nbsp;программу и пропускает оставшуюся часть выполнения, что означает, что если программа имеет 100 строк кода и в строке 10 возникает исключение, программа немедленно завершится, пропустив выполнение остальных 90 строк кода.</p>

<h2>Обработка исключений</h2>

<p>Чтобы справиться с этой проблемой, мы используем&nbsp;<code>обработку исключений</code>, которая позволяет&nbsp;<code>избежать завершения программы</code>&nbsp;и продолжить выполнение, пропуская код исключения.</p>

<p><code>Обработка исключений Java</code>&nbsp;предоставляет пользователю осмысленное сообщение о проблеме, а не системное сообщение, которое может быть непонятно пользователю.</p>

<p>Рассмотрим пример с обработкой исключения:</p>

<pre>
<code>public class Main {
    public static void main(String[] args) {
        try { // 1
            int a = 0;
            int b = 2 / a;
        } catch (ArithmeticException e) { // 2
            System.out.println(e); // 3
        }
    }
}</code></pre>

<ol>
	<li>Обертка блока кода, где возможно появление исключения;</li>
	<li>Обработка исключения;</li>
	<li>Вывод ошибки;</li>
</ol>

<pre>
<code>java.lang.ArithmeticException: / by zero
</code></pre>

<p>В данном примере, программа продолжит работу, благодаря обработке исключения.</p>

<p>Если мы не знаем тип выводимого исключения, мы можем использовать класс обертку&nbsp;<code>Exception</code>.</p>

<pre>
<code>try {
    int a = 0;
    int b = 2 / a;
} catch (Exception e) {
    System.out.println(e);
}</code></pre>

<p>В&nbsp;<code>Java</code>&nbsp;имеется список встроенных исключений, которые выбрасываются при обращении к значению в массиве по индексу, которого нет, со списком можно ознакомиться&nbsp;<a href="https://www.tutorialspoint.com/java/java_builtin_exceptions.htm" rel="nofollow noopener noreferrer">здесь</a>. Дополнительно, вы можете создавать свои исключения.</p>

<pre>
<code>class MyException extends Exception { // 1
    int a;

    MyException(int b) { // 2
        a = b;
    }

    public String toString() { // 3
        return ("Exception Number =  " + a);
    }
}

public class Main {
    public static void main(String[] args) {
        try {
            throw new MyException(1); // 4
        } catch (MyException e) { // 5
            System.out.println(e); // Exception Number =  1
        }
    }
}</code></pre>

<ol>
	<li>Декларация&nbsp;<code>MyException</code>, который расширяет класс&nbsp;<code>Exception</code>;</li>
	<li>Объявление конструктора;</li>
	<li>Переопределение метода&nbsp;<code>toString()</code>;</li>
	<li>Вызов исключения - экземпляра исключения MyException;</li>
	<li>Обработка исключения;</li>
</ol>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://docs.oracle.com/javase/tutorial/essential/exceptions/definition.html" rel="nofollow noopener noreferrer">Java exceptions</a>;</li>
	<li><a href="https://javarush.ru/groups/posts/isklyucheniya-java" rel="nofollow noopener noreferrer">Исключения в java</a>;</li>
</ul>

<h1>IO</h1>

<p>Создавая программы, мы учитываем то, что им будет пользоваться человек или другая машина.</p>

<p>Программа в <code>Java</code> может коммуницировать через поток ввода-вывода данных. <code>Поток</code> - может представлять различные источники и адресаты, включая файлы на диске, другие программы и массивы в памяти.</p>

<p>Простой пример - мы разрабатываем приложение для сохранения заметок, которое будет принимать от пользователя данные и будет сохранять их в <code>файл</code>. В поток ввода - <code>Stdin</code> будут отправляться данные, введенные пользователем.</p>

<p>Потоками вывода будут - <code>терминал</code> и <code>файл</code>. В терминал будет выводиться статус добавления, а в файл - введенные пользователем данные.</p>

<p>Пример работы программы:</p>

<pre><code>&gt; Сходить к врачу
Добавлено
&gt; Оплатить налоги
Добавлено
</code></pre>

<p>При работе программы всегда есть заранее продекларированные потоки:</p>

<ul>
	<li>stdin - стандартный ввод. Имеет значение файлового дескриптора - 0;</li>
	<li>stdout - стандартный вывод. ФД - 1;</li>
	<li>stderr - вывод для ошибок. ФД - 2;</li>
</ul>

<p>Файловый дескриптор — это неотрицательное число, которое является идентификатором потока ввода-вывода.</p>

<p>Дескриптор может быть связан с файлом, каталогом, сокетом.</p>

<p>Например, когда вы открываете или создаете новый файл, операционная система формирует для себя запись для представления этого файла и хранения информации о нем. У каждого файла индивидуальный файловый дескриптор Linux. Открыли 100 файлов — где-то в ядре появились 100 записей, представленных целыми числами.</p>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://stackoverflow.com/questions/5256599/what-are-file-descriptors-explained-in-simple-terms" rel="nofollow noopener noreferrer">Файловые дескрипторы простыми словами</a>;</li>
	<li><a href="https://metanit.com/java/tutorial/6.1.php" rel="nofollow noopener noreferrer">Потоки ввода-вывода</a>;</li>
	<li><a href="https://ru.wikipedia.org/wiki/%D0%A4%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2%D1%8B%D0%B9_%D0%B4%D0%B5%D1%81%D0%BA%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D1%80" rel="nofollow noopener noreferrer">Wiki</a>;</li>
</ul>

<h1>Запись в файл</h1>

<p>Для начала, создадим наш проект в <code>IDE</code>.</p>

<p>Названием нашего приложения будет <code>todo-app</code>.</p>

<pre><code>import java.io.*;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        try {
            FileWriter file = new FileWriter("todo.txt", true); // 1
            Scanner scanner = new Scanner(System.in); // 2
            System.out.printf("&gt; ");
            while (true) { // 3
                String line = scanner.nextLine(); // 4
                if (line.equals("Выход")) { // 5
                    file.close(); // 6
                    return;
                }
                file.write(line + "\n"); // 7
                System.out.printf("Добавлено\n&gt; ");
            }
        } catch (Exception e) { // 8
            System.out.printf("%s", e);
            return;
        }
    }
}</code></pre>

<ol>
	<li>Создание объекта <code>FileWriter</code>, первый параметр - название файла, второй параметр - добавлять ли линии к уже существующим файлы или начать сначала; Создавая экземпляр данного класса, мы создаем новый <code>поток</code>, через который можно записывать данные.</li>
	<li>Создание объекта типа <code>Scanner</code> для чтения данных от пользователя;</li>
	<li>Цикл для чтения данных от пользователя;</li>
	<li>Чтение линии до <code>\n</code>;</li>
	<li>Условие выхода из программы;</li>
	<li>Закрытие потока;</li>
	<li>Запись данных в файл;</li>
	<li>Обработка исключений;</li>
</ol>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/io/FileWriter.html" rel="nofollow noopener noreferrer">FileWriter</a>;</li>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Scanner.html" rel="nofollow noopener noreferrer">Scanner</a>;</li>
	<li><a href="https://vertex-academy.com/tutorials/ru/rabota-so-skannerom-v-java/" rel="nofollow noopener noreferrer">О Scanner</a>;</li>
</ul>

<h1>Чтение из файла</h1>

<p>В прошлом уроке мы написали программу, которая записывает данные в файл.</p>

<p>В этой главе мы познакомимся с чтением данных из файлов.</p>

<p>Для начала, создадим файл:</p>

<pre><code>echo "Ехал грека через реку\nВидит грека в реке рак\n" &gt; /tmp/readme.txt</code></pre>

<p>Для чтения файла напишем простую программу.</p>

<pre><code>import java.io.*;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        try { // 1
            File file = new File("/tmp/readme.txt"); // 2
            Scanner obj = new Scanner(file); // 3
            while (obj.hasNextLine()) { // 4
                System.out.println(obj.nextLine()); // 5
            }
        } catch (Exception e) {
            System.out.printf("%s", e);
            return;
        }
    }
}</code></pre>

<ol>
	<li>Обертка блока кода, где возможно появление исключения;</li>
	<li>Откроем файл;</li>
	<li>Создаем <code>Scanner</code>, имеющий методы для чтения - <code>nextLine()</code>;</li>
	<li>Вызываем метод, который проверяет наличие следующей линии;</li>
	<li>Выводим прочитанную из файла линию;</li>
</ol>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/nio/file/Files.html" rel="nofollow noopener noreferrer">File</a>;</li>
	<li><a href="https://www.studytonight.com/java/file-handling.php" rel="nofollow noopener noreferrer">Примеры</a>;</li>
</ul>