<h2>JVM</h2>

<p><code>JVM</code> это виртуальная машина, которая исполняет принятые ею <code>байт код</code> команды.</p>

<p><code>JVM</code> не понимает файлы с расширением <code>.java</code>, поэтому нам нужно скомпилировать программу в формате, который будет запускаться на <code>JVM</code>.</p>

<p><img alt="" height="471" name="image.png" src="https://ucarecdn.com/9bab6d35-5fa9-449c-aa1b-a9d355fa5944/" width="533"></p>

<ul>
	<li><code>Class loader</code> - загружает <code>class</code> в <code>JVM</code>;</li>
	<li><code>Method area</code> - хранит константы, локальные данные методов, код метода, конструктор;</li>
	<li><code>Heap</code> - область памяти где хранятся динамически созданные объекты;</li>
	<li><code>Stack</code> - область памяти где хранятся предварительно декларированные переменные;</li>
	<li><code>Program Register</code> - указатель на текущую выполняемую операцию;</li>
	<li><code>Native Method Stack</code> - область памяти, где хранятся встроенные методы, классы;</li>
	<li><code>Execution Engine</code> - выполняет операции и позволяет запускать вашу программу на любой ОС;</li>
	<li><code>Native Method Interface</code> - создает интерфейс между вашим кодом и встроенным стэком;</li>
	<li><code>Native Method Library</code> - хранит файлы для запуска встроенного кода;</li>
</ul>

<p><code>JVM</code> контролирует процесс работы программы. Он занимается очисткой <code>heap</code> и обработкой исключений.</p>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://docs.oracle.com/javase/specs/jvms/se8/html/jvms-2.html" rel="nofollow noopener noreferrer">JVM doc</a>;</li>
	<li><a href="https://www.geeksforgeeks.org/jvm-works-jvm-architecture/" rel="nofollow noopener noreferrer">How JVM works</a>;</li>
</ul>

# Homework
1. Завершить тест по итогам урока в LMS