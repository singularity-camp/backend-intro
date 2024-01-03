<h1>SE &amp;&amp; EE &amp;&amp; ME &amp;&amp; FX</h1>

<p>При выборе языка <code>Java</code> - вы, возможно столкнулись с тем, что есть <code>Java SE</code>, <code>Java EE</code>. В этой главе мы рассмотрим подробнее каждую платформу разработки.</p>

<p>Платформа <code>Java</code> - это набор <code>JVM</code> и <code>API</code> через которое возможны работы со многими библиотеками для работы с - <code>GUI</code>, <code>Image I/O</code>, <code>HTTP</code>, <code>JSON</code>, <code>XML</code>;</p>

<p>На сегодняшний день, таких платформ 4:</p>

<ol>
	<li><code>SE</code> - Standard Edition - состоит из <code>JVM</code> и <code>API</code>;</li>
	<li><code>EE</code> - Enterprise Edition - состоит из <code>SE</code> и дополнительного расширения для <code>API</code>;</li>
	<li><code>ME</code> - Micro Edition - <code>API</code> и минимальный <code>VM</code>, используется на девайсах со слабой производительностью;</li>
	<li><code>FX</code> - <code>API</code> заточенный под работу с сетевыми протоколами;</li>
</ol>


<h1>Конвенции написания кода на Java</h1>

<p>При написании кода хорошим тоном является следование конвенции. Конвенция написания кода - это набор правил, который описывает то, как должны называться пакеты, переменные, функции, классы, интерфейсы.</p>

<p>Понятные названия пакетов и переменных делают код более читабельным. К тому же, они описывают то, что делает функция без погружения в реализацию.</p>

<p>Познакомимся со списком типов и их правилам:</p>

<table align="center" border="1" cellpadding="1" cellspacing="1" style="width: 900px;">
	<tbody>
		<tr>
			<td>Тип</td>
			<td>Правила</td>
			<td>Пример</td>
		</tr>
		<tr>
			<td>Package                        </td>
			<td>Все должно быть в нижнем регистре<br>
			1. Доменное имя первого уровня: com, kz; <br>
			2. Доменное имя второго уровня или название директории, департамента, проекта, hostname</td>
			<td>edu.cmu.cs.bovik.cheese         <br>
			com.sun.eng <br>
			com.apple.quicktime.v2</td>
		</tr>
		<tr>
			<td>Class</td>
			<td>CamelCase, без сокращения</td>
			<td>
			<pre>
<code>class Raster;
class ImageSprite;</code></pre>
			</td>
		</tr>
		<tr>
			<td>Interface.                         </td>
			<td>Так же как в <code>Class</code></td>
			<td>
			<pre>
<code>interface RasterDelegate;
interface Storing;</code></pre>
			</td>
		</tr>
		<tr>
			<td>Methods</td>
			<td>Глагол<br>
			Начинается с символа в нижнем регистре<br>
			Следующие слова начинаются в верхнем регистре</td>
			<td>
			<pre>
<code>run();
runFast();
getBackground();</code></pre>
			</td>
		</tr>
		<tr>
			<td>Переменные                                                           </td>
			<td>
			<pre>
<code>За исключением переменных, все экземпляры,
классы и константы классов пишутся в
смешанном регистре со строчной первой буквой.
Внутренние слова начинаются с заглавных букв. 
Имена переменных не должны начинаться с 
символа подчеркивания _ или знака доллара $, 
хотя и то, и другое разрешено.
Имена переменных должны быть короткими, 
но осмысленными. Выбор имени переменной должен 
быть мнемоническим, то есть предназначенным 
для того, чтобы указать случайному наблюдателю 
на цель ее использования. Следует избегать 
односимвольных имен переменных, за исключением 
временных «одноразовых» переменных. 
Общие имена для временных 
переменных: i, j, k, m и n для целых 
чисел; c, d и e для символов.</code></pre>
			</td>
			<td>
			<pre>
<code>float myWidth;</code></pre>
			</td>
		</tr>
		<tr>
			<td>Константы</td>
			<td>
			<pre>
<code>Имена переменных, 
объявленных константами 
класса, и констант ANSI 
должны быть все в верхнем 
регистре со словами, разделенными 
символом подчеркивания ("_"). </code></pre>
			</td>
			<td>
			<pre>
<code>static final int MIN_WIDTH = 4;
static final int MAX_WIDTH = 999;
static final int GET_THE_CPU = 1;</code></pre>
			</td>
		</tr>
	</tbody>
</table>

<p> </p>

<p>К примеру, у нас есть функция, которая должно вернуть <code>true</code>, если число положительное.</p>

<blockquote>
<p>Плохая практика</p>
</blockquote>

<pre><code>static boolean a(z int) {
    // ...
}</code></pre>

<p>Представим, что данная функция вызывается из другого файла,</p>

<pre><code>public static main(String[] args) {
    boolean b = a(42);
}</code></pre>

<p>Данный код выглядит максимально непонятно и вам всегда нужно будет переходить в файл с реализацией.</p>

<p>Рассмотрим пример с соблюдением конвенции:</p>

<blockquote>
<p>Хорошая практика</p>
</blockquote>

<pre><code>static boolean isPositive(int num) {
    ...
}</code></pre>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://www.oracle.com/technetwork/java/codeconventions-150003.pdf" rel="nofollow noopener noreferrer">Oracle code convention</a>;</li>
	<li><a href="https://google.github.io/styleguide/javaguide.html" rel="nofollow noopener noreferrer">Google code convention</a>;</li>
	<li><a href="https://codegym.cc/groups/posts/491-java-coding-conventions-which-ones-to-follow-and-why" rel="nofollow noopener noreferrer">Java Coding Conventions. Which Ones to Follow and Why</a>;</li>
</ul>


# Homework
1. Завершить тест по итогам урока в LMS