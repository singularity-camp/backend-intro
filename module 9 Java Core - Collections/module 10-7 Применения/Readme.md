<h1>Применения</h1>

## Пример 1

<p>При работе с данными, нам часто необходимо сохранить и обработать их. Рассмотрим пример с <code>ArrayList</code>.</p>

<p>Для прохождения по каждому элементу есть несколько способов:</p>

<pre><code>import java.util.ArrayList;
import java.util.Iterator;

public class Main {
    public static void main(String[] args) {

        ArrayList&lt;Integer&gt; arrayList = new ArrayList&lt;Integer&gt;(); // 1
        arrayList.add(14); // 2
        arrayList.add(7);
        arrayList.add(39);
        arrayList.add(40);

        System.out.println("For Loop");
        for (int counter = 0; counter &lt; arrayList.size(); counter++) { // 3
            System.out.println(arrayList.get(counter)); // 4
        }

        for (Integer num : arrayList) { // 5
            System.out.println(num); // 6
        }

        int count = 0;
        while (arrayList.size() &gt; count) { // 7
            System.out.println(arrayList.get(count)); // 8
            count++;
        }

        System.out.println("Iterator");
        Iterator&lt;Integer&gt; iter = arrayList.iterator(); // 9
        while (iter.hasNext()) { // 10
            System.out.println(iter.next()); // 11
        }
    }
}</code></pre>

<p>Мы узнали об основных типах данных и их реализаций в <code>Java</code>. В этом уроке мы узнаем, какие из классов коллекций лучше использовать для решения задач.</p>

<p>При решении проблемы, нужно узнать о данных, с которыми нам нужно работать. Если, мы работаем с данными, в которых должны быть пара ключ/значение, мы будем использовать одну из реализаций <code>Map</code>.</p>

## Пример 2

<p>Например, перед нами стоит задача, вывести список всех поступившие на счет за определенный период времени средства. Нам дают данные, где есть iin, дата, сумма (970519000000, 19.05.2022, 510). Мы можем использовать <code>iin</code> как ключ, а значением будет <code>int</code> к которому будем прибавлять новые средства.</p>

<p>Так же, нам необходимо понимать, важна ли очередность элементов для нашей проблемы. Если да, то <code>HashMap</code> не подойдет, и нужно выбирать <code>LinkedHashMap</code>.</p>

<p>В случае, когда для нашей проблемы важна сортировка, мы можем использовать <code>TreeMap</code>, в котором элементы добавляются в отсортированное дерево.</p>

<p><img alt="" height="1775" name="image.png" src="https://ucarecdn.com/7554d557-0412-439f-8697-aee15e2281bb/" width="2253"></p>

<p>Дополнительные материалы:</p>

<ul>
	<li><a href="https://www.programiz.com/dsa/trees" rel="nofollow noopener noreferrer">Tree Data Structure</a></li>
	<li><a href="https://docs.oracle.com/javase/tutorial/collections/index.html" rel="nofollow noopener noreferrer">Java Collection Tutorial</a></li>
	<li><a href="https://javarush.ru/groups/posts/2308-korotko-o-glavnom---java-collections-framework" rel="nofollow noopener noreferrer">Java Collections Ru</a></li>
</ul>