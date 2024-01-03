<h1>Linux cmd lines</h1>

<h1>first-touch</h1>

<h3>Полезное</h3>

<ul>
	<li><a href="https://linuxize.com/post/create-a-file-in-linux/" rel="nofollow noopener noreferrer">Статья: создание файлов в linux</a></li>
	<li>Команда <code>touch</code></li>
	<li>Команда <code>echo</code></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>В корневой директории <code>/home/box</code> создать файл с названием <code>jusan</code> и с текстом внутри <code>singularity</code>.</li>
</ol>

<p>Пример для проверки:</p>

<pre><code class="language-bash">$ cat jusan
singularity</code></pre>

<h1>second-touch</h1>

<h3>Полезное</h3>

<ul>
	<li><a href="https://younglinux.info/bash/chmod" rel="nofollow noopener noreferrer">Изменение прав с помощью chmod</a></li>
	<li>Команда <code>chmod</code></li>
	<li>Команда <code>ls</code></li>
	<li><a href="https://linuxize.com/post/understanding-linux-file-permissions/" rel="nofollow noopener noreferrer">Understanding Linux File Permissions</a></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Cоздать файл с названием <code>second</code> и с текстом внутри <code>touch</code>.</li>
	<li>Установить созданному файлу права <code>rw--wx-w-</code>.</li>
</ol>

<p>Пример проверки прав:</p>

<pre><code class="language-bash">$ ls -l
-rw--wx-w-  1 root  staff    6 Mar  7 16:23 second
</code></pre>

<h1>touch-art</h1>

<h3>Полезное</h3>

<ul>
	<li>Команда для создания ссылок <code>ln</code></li>
	<li>Команда для создания папок <code>mkdir</code></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>В корневой директории создайте папку <code>touch-art</code> и создайте папки и файлы в <code>touch-art</code>, чтобы права, названия файлов, ссылок и папок был таким же как по примеру ниже.</li>
</ol>

<p>Пример проверки прав:</p>

<pre><code class="language-bash">$ cd touch-art
$ ls -lF
total 4
-rwxrwxrwx. 1 box box    0 Mar 28 08:22 a*
lrwxrwxrwx. 1 box box    1 Mar 28 08:22 b -&gt; a*
-rw-----wx. 1 box box    0 Mar 28 08:22 c*
drw--w--wx. 2 box box 4096 Mar 28 08:22 d/
-rw--w--wx. 1 box box    0 Mar 28 08:22 e*
-rw-----wx. 1 box box    0 Mar 28 08:22 f*
-rwx---rwx. 1 box box    0 Mar 28 08:22 g*
-rwxrwxrwx. 1 box box    0 Mar 28 08:22 h*</code></pre>

<h1>ultra-ls</h1>

<h3>Задание</h3>

<ol>
	<li>Написать скрипт, который использует команду <code>ls</code>:

	<ul>
		<li>Не показывать директории <code>.</code> и <code>..</code>;</li>
		<li>Вывести <code>/</code> символ <em>slash</em> после название папки;</li>
		<li>Отсортировать по <em>time modified</em> по убыванию;</li>
	</ul>
	</li>
</ol>

<h1>project-structure</h1>

<h3>Задание</h3>

<ol>
	<li>Cоздайте папку <code>project</code> в корневой директории. В ней создайте такую структуру файлов и папок как показано ниже:</li>
</ol>

<pre><code>.
├── README.md
├── usecase
│   └── registration
│       ├── registration.go
│       └── registration_test.go
└── pkg
    └── util
        ├── helper.go
        ├── util_test.go
        └── util.go

</code></pre>

<h1>missing-line</h1>

<h3>Задание</h3>

<ol>
	<li>В корневой директории <code>/home/box</code> создать папку <code>sandbox</code> и в ней создать файл <code>jusan</code>.</li>
	<li>В файл <code>jusan</code> записать слово <code>singularity</code> без новой линии в конце.</li>
</ol>

<p>Пример для проверки:</p>

<pre><code class="language-bash">box@dec74273716e: ~ $ cat jusan | wc -l
     0</code></pre>


<h1>where-is</h1>

<h3>Полезное</h3>

<ul>
	<li>Команда <code>find</code> для поиска файлов</li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать скрипт, который будет искать в текущей директории и в ее поддиректориях файлы по следующим условиям:
	<ul>
		<li>Начинается на символ <code>j</code>, или</li>
		<li>Заканчивается на символ <code>n</code>, или</li>
		<li>Начинается на <code>n</code> и заканчивается на <code>j]</code></li>
	</ul>
	</li>
</ol>

<p>Пример вывода:</p>

<pre><code>./ton
./jack
./nokoj]
</code></pre>


<h1>where-is-md</h1>

<h3>Задание</h3>

<p>1. Написать скрипт, который будет искать в текущей директории и в ее поддиректориях файлы по следующим условиям:</p>

<ul>
	<li>Заканчивается на <code>.md</code></li>
</ul>

<h1>count-files</h1>

<h3>Полезное</h3>

<ul>
	<li>Команда для подсчета <code>wc</code></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать команду, которая посчитает количество файлов в текущей директории и в ее поддиректориях.</li>
</ol>

<h1>count-dirs</h1>

<h3>Задание</h3>

<ol>
	<li>Написать команду, которая посчитает количество папок в текущей директории и в ее поддиректориях.</li>
</ol>   


<h1>who-is-author</h1>

<h3>Полезное</h3>

<ul>
	<li><code>ls</code></li>
	<li><code>awk</code></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать команду, которая покажет все содержимое в текущей директории в формате <code>user filename</code>. Не показывать в выводе директории <code>.</code> и <code>..</code>.</li>
</ol>

<p>Пример вывода:</p>

<pre>
<code>root avatar.png
amurat solution.txt
jchris song.mp3
</code></pre>


<h1>echo-cat</h1>

<h3>Полезные команды</h3>

<ul>
	<li><code>cat</code></li>
</ul>

<p>В директории текущей директории есть файл <code>dont-open.txt</code>.</p>

<h3>Задание</h3>

<ol>
	<li>Создайте в папку <code>/sandbox</code>  и в ней файл c dont-open.txt который содержит текст из  <code>dont-open.txt</code>.</li>
</ol>

<h1>rm-test</h1>

<h3>Полезное</h3>

<ul>
	<li>Команда <code>rm</code> для удаления</li>
</ul>

<h3>Задание</h3>

<ol>
	<li>В директории <code>/home/box/project</code> удалите все файлы, которые заканчиваются на <code>_test.py</code>.</li>
</ol>

<h1>last-5</h1>

<h3>Подсказка</h3>

<ul>
	<li>Команда <code>tail</code> для показа последних строк в файле</li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать скрипт, который покажет последние 5 линии из файла <code>./access.log</code>.</li>
</ol>

<p>Файл <code>access.log</code> для примера:</p>

<pre><code>80.91.33.133 - - [17/May/2015:08:05:50 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.22)"
173.203.139.108 - - [17/May/2015:08:05:03 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
80.91.33.133 - - [17/May/2015:08:05:35 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.16)"
5.83.131.103 - - [17/May/2015:08:05:51 +0000] "GET /downloads/product_1 HTTP/1.1" 200 490 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.22)"
80.91.33.133 - - [17/May/2015:08:05:59 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.17)"
200.6.73.40 - - [17/May/2015:08:05:42 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
80.91.33.133 - - [17/May/2015:08:05:48 +0000] "GET /downloads/product_1 HTTP/1.1" 404 324 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.17)"
</code></pre>

<h1>first-5</h1>

<h3>Подсказка</h3>

<ul>
	<li>Команда <code>head</code> для показа первых строк в файле</li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать скрипт, который покажет первые 5 линии из файла <code>./access.log</code>.</li>
</ol>

<p>Файл <code>access.log</code> для примера:</p>

<pre><code>80.91.33.133 - - [17/May/2015:08:05:50 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.22)"
173.203.139.108 - - [17/May/2015:08:05:03 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
80.91.33.133 - - [17/May/2015:08:05:35 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.16)"
5.83.131.103 - - [17/May/2015:08:05:51 +0000] "GET /downloads/product_1 HTTP/1.1" 200 490 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.22)"
80.91.33.133 - - [17/May/2015:08:05:59 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.17)"
200.6.73.40 - - [17/May/2015:08:05:42 +0000] "GET /downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
80.91.33.133 - - [17/May/2015:08:05:48 +0000] "GET /downloads/product_1 HTTP/1.1" 404 324 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.17)"
</code></pre>

<h1>replace-inplace</h1>

<h3>Полезное</h3>

<ul>
	<li><code>sed</code></li>
	<li><code>tr</code></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать скрипт, который заменит в файле <code>access.log</code> текст <code>jusan.kz</code> на <code>example.com</code> глобально.</li>
</ol>

<p>Файл <code>access.log</code> для примера:</p>

<pre><code>80.91.33.133 - - [17/May/2015:08:05:50 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.22)"
173.203.139.108 - - [17/May/2015:08:05:03 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
80.91.33.133 - - [17/May/2015:08:05:35 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.16)"
5.83.131.103 - - [17/May/2015:08:05:51 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 200 490 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.22)"
80.91.33.133 - - [17/May/2015:08:05:59 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.17)"
200.6.73.40 - - [17/May/2015:08:05:42 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
80.91.33.133 - - [17/May/2015:08:05:48 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 404 324 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.17)"
</code></pre>

<h1>grep</h1>

<h3>Полезное</h3>

<ul>
	<li>Команда <code>grep</code> для поиска в текста</li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать скрипт, который покажет в файле <code>./access.log</code> только линии содержащие <code>jusan.kz</code>.</li>
</ol>

<p>Файл <code>access.log</code> для примера:</p>

<pre><code>180.179.174.219 - - [17/May/2015:18:05:22 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 339 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
152.90.220.18 - - [17/May/2015:18:05:18 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 336 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
10.16.62.10 - - [17/May/2015:18:05:32 +0000] "GET http://example.com/downloads/product_1 HTTP/1.1" 404 318 "-" "Debian APT-HTTP/1.3 (1.0.1ubuntu2)"
180.179.174.219 - - [17/May/2015:18:05:52 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 336 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
62.210.152.199 - - [17/May/2015:18:05:38 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 200 2592 "-" "urlgrabber/3.9.1 yum/3.2.29"
204.77.169.137 - - [17/May/2015:18:05:23 +0000] "GET https://jusan.kz/downloads/product_2 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.2)"
94.23.21.169 - - [17/May/2015:18:05:07 +0000] "GET http://example.com/downloads/product_1 HTTP/1.1" 404 328 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
85.214.47.178 - - [17/May/2015:18:05:08 +0000] "GET http://example.com/downloads/product_1 HTTP/1.1" 404 331 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
176.58.26.49 - - [17/May/2015:18:05:37 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 200 2575 "-" "urlgrabber/3.9.1 yum/3.2.29"
54.194.93.59 - - [17/May/2015:18:05:33 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 333 "-" "Debian APT-HTTP/1.3 (1.0.1ubuntu2)"
204.77.169.137 - - [17/May/2015:18:05:09 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 319 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.2)"
54.183.135.30 - - [17/May/2015:18:05:50 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (1.0.1ubuntu2)"
204.77.169.137 - - [17/May/2015:18:05:46 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 319 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.2)"
202.78.200.137 - - [17/May/2015:18:05:12 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 333 "-" "Debian APT-HTTP/1.3 (1.0.1ubuntu2)"
194.76.107.17 - - [17/May/2015:18:05:53 +0000] "HEAD /downloads/product_2 HTTP/1.1" 200 0 "-" "Wget/1.13.4 (linux-gnu)"
212.83.167.232 - - [17/May/2015:18:05:38 +0000] "GET http://example.com/downloads/product_1 HTTP/1.1" 404 341 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
</code></pre>

<h1>grep-exclude</h1>

<h3>Полезное</h3>

<ul>
	<li><code>ls</code></li>
	<li><code>grep</code></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать скрипт, который:
	<ul>
		<li>перечислит содержимое в текущей директории, не включая <code>.</code> и <code>..</code>;</li>
		<li>откинет из перечисленного папку <code>.git</code>.</li>
	</ul>
	</li>
</ol>

<h1>count-grep</h1>

<h3>Полезное</h3>

<ul>
	<li>Команда <code>wc</code> для подсчета</li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать скрипт, который покажет в файле <code>./access.log</code> количество линий, содержащих <code>jusan.kz</code>.</li>
</ol>

<p>Файл <code>access.log</code> для примера:</p>

<pre><code>180.179.174.219 - - [17/May/2015:18:05:22 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 339 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
152.90.220.18 - - [17/May/2015:18:05:18 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 336 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
10.16.62.10 - - [17/May/2015:18:05:32 +0000] "GET http://example.com/downloads/product_1 HTTP/1.1" 404 318 "-" "Debian APT-HTTP/1.3 (1.0.1ubuntu2)"
180.179.174.219 - - [17/May/2015:18:05:52 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 336 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
62.210.152.199 - - [17/May/2015:18:05:38 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 200 2592 "-" "urlgrabber/3.9.1 yum/3.2.29"
204.77.169.137 - - [17/May/2015:18:05:23 +0000] "GET https://jusan.kz/downloads/product_2 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.2)"
94.23.21.169 - - [17/May/2015:18:05:07 +0000] "GET http://example.com/downloads/product_1 HTTP/1.1" 404 328 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
85.214.47.178 - - [17/May/2015:18:05:08 +0000] "GET http://example.com/downloads/product_1 HTTP/1.1" 404 331 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
176.58.26.49 - - [17/May/2015:18:05:37 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 200 2575 "-" "urlgrabber/3.9.1 yum/3.2.29"
54.194.93.59 - - [17/May/2015:18:05:33 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 333 "-" "Debian APT-HTTP/1.3 (1.0.1ubuntu2)"
204.77.169.137 - - [17/May/2015:18:05:09 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 319 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.2)"
54.183.135.30 - - [17/May/2015:18:05:50 +0000] "GET https://jusan.kz/downloads/product_1 HTTP/1.1" 304 0 "-" "Debian APT-HTTP/1.3 (1.0.1ubuntu2)"
204.77.169.137 - - [17/May/2015:18:05:46 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 319 "-" "Debian APT-HTTP/1.3 (0.8.16~exp12ubuntu10.2)"
202.78.200.137 - - [17/May/2015:18:05:12 +0000] "GET http://example.com/downloads/product_2 HTTP/1.1" 404 333 "-" "Debian APT-HTTP/1.3 (1.0.1ubuntu2)"
194.76.107.17 - - [17/May/2015:18:05:53 +0000] "HEAD /downloads/product_2 HTTP/1.1" 200 0 "-" "Wget/1.13.4 (linux-gnu)"
212.83.167.232 - - [17/May/2015:18:05:38 +0000] "GET http://example.com/downloads/product_1 HTTP/1.1" 404 341 "-" "Debian APT-HTTP/1.3 (0.9.7.9)"
</code></pre>

<h1>ultra-cat</h1>

<h3>Полезное</h3>

<ul>
	<li><code>cat EOF</code></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Написать скрипт, который запишет в файл <code>output.txt</code> следующие линии:</li>
</ol>

<pre><code>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec neque purus,
rutrum vel purus eget, mattis aliquam tortor. Morbi rhoncus metus faucibus
tortor blandit, in luctus leo ultrices. Donec finibus vulputate ex, vel
feugiat erat. Ut ultrices felis sit amet urna tincidunt tempor. Suspendisse
vel eleifend augue. Nam porta leo urna. Mauris augue mi, lacinia in consectetur
a, accumsan nec nibh. Mauris ornare pulvinar lorem, sit amet venenatis enim
feugiat non. Praesent aliquet nec lorem ac interdum. Mauris quis finibus orci,
at tempor mi.
</code></pre>

<h1>stepik-join-date</h1>

<h3>Полезные команды</h3>

<ul>
	<li>Команда для выполнения HTTP запросов <code>curl</code></li>
	<li>Команда для парсинга JSON <code>jq</code></li>
</ul>

<p>У <em>stepik.org</em> есть публичный API. Через него можно получать общедоступную информацию по платформе.</p>

<p>Например, такой запрос вернет пользователя под id <code>1</code>, т.е. самого первого пользователя на <em>stepik.org</em>.</p>

<pre>curl -s https://stepik.org:443/api/users/1</pre>

<pre><code>{"meta": {"page": 1, "has_next": false, "has_previous": false}, "users": [{"id": 1, "profile": 1, "is_private": false, "is_active": true, "is_guest": false, "is_organization": false, "short_bio": "", "details": "", "first_name": "Andrey", "last_name": "Balandin", "full_name": "Andrey Balandin", "alias": null, "avatar": "https://stepik.org/users/1/59109f498310fb45ff2ae4642cd06f96fa7382dc/avatar.svg", "cover": null, "city": 498817, "knowledge": 167, "knowledge_rank": 401819, "reputation": 2, "reputation_rank": 111316, "join_date": "2013-07-02T10:41:22Z", "social_profiles": [], "solved_steps_count": 164, "created_courses_count": 0, "created_lessons_count": 2, "issued_certificates_count": 0, "followers_count": 4}]}
</code></pre>

<h3>Задание</h3>

<ol>
	<li>В корневой директории <code>/home/box</code> создайте файл <code>stepik.sh</code></li>
	<li>Напишите скрипт в <code>stepik.sh</code>, который выведет <code>join_date</code> вашего профиля.</li>
	<li>Дайте права 755 на <code>stepik.sh</code>.</li>
</ol>

<p>Например, для пользователя под id <code>1</code> ответ:</p>

<pre><code>2013-07-02T10:41:22Z
</code></pre>



<h1>Настройка сервера</h1>

<h1>apt-nginx</h1>

<p>В этом уроке начнем знакомиться с <code>apt</code>.</p>

<h3>Полезное</h3>

<ul>
	<li><a href="https://itsfoss.com/apt-get-linux-guide/" rel="nofollow noopener noreferrer">apt для новичков</a></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Обновите (англ. "update") базу пакетов.</li>
	<li>Обновите (англ. "upgrade") установленные пакеты.</li>
	<li>Установите (англ. "install") пакет nginx.</li>
	<li>Напишите команды по порядку </li>
</ol>


<h1>apt-delete-nginx</h1>

<p>В этом уроке полностью удалим nginx из сервера.</p>

<p>На сервере заранее установлен nginx.</p>

<h3>Полезные ссылки</h3>

<ul>
	<li><a href="https://itsfoss.com/apt-get-linux-guide/" rel="nofollow noopener noreferrer">apt для новичков</a></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Удалить (англ. "delete") полностью nginx вместе с конфигурационными файлами.</li>
</ol>

<h1>apt-gcc</h1>

<p>В этом уроке разберем подкоманду <code>show</code>.</p>

<h3>Полезное</h3>

<ul>
	<li><code>apt show</code></li>
	<li><a href="https://itsfoss.com/apt-get-linux-guide/" rel="nofollow noopener noreferrer">apt для новичков</a></li>
</ul>

<h3>Задание</h3>

<ul>
	<li>Обновите (англ. "update") базу пакетов.</li>
	<li>Отправьте значение поля <code>Bugs</code> от информации по пакету <code>gcc</code>.</li>
</ul>




<h1>ssh-key</h1>

<p>В этом уроке разберем как работать с удаленным сервером по <code>ssh</code>.</p>

<p>Для выполнения задачи нам понадобится запустить локальный VPS сервер. На компьютере должен быть установлен <code>docker</code>.</p>

<p>В терминале выполним следующую команду для запуска VPS:</p>

<pre><code class="language-bash">PORT=22 &amp;&amp; docker run -d --rm --name local-vps-$PORT -p $PORT:$PORT atlekbai/local-vps $PORT</code></pre>

<p>Для подключения:</p>

<pre><code class="language-bash">ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no root@127.0.0.1 -p 22</code></pre>

<p>Пароль: <code>password</code></p>

<h3>Полезные ссылки</h3>

<ul>
	<li><a href="https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys-on-ubuntu-1804" rel="nofollow noopener noreferrer">Установка ssh ключей</a></li>
</ul>

<h3>Задание</h3>

<ol>
	<li>Сгенерируйте связку ключей, если нет.</li>
	<li>Установите ключи на VPS сервере, чтобы подключаться без пароля.</li>
	<li>Выполненные команды отправьте в поле ввода.</li>
</ol>

<h1>Пользователи и группы</h1>

useradd-junior

Каждый пользователь Linux должен иметь отдельную учетную запись. В учетной записи можно безопасно хранить файлы, настраивать окружение и конфигурации.

Группы — это способ назначения прав в системе, которые могут быть определены для нескольких пользователей одновременно.

Самый простой способ создания нового пользователя — команда useradd.

Единственным обязательным параметром является логин пользователя, но можно включить в него дополнительную информацию. Для данного урока понадобится следующий флаг.

-c "комментарий" — комментарий к новой учетной записи пользователя. Обычно это полное имя пользователя.
Полезное

Введите команду useradd в терминале для получения списка всех флагов
Используйте passwd для установки пароля
Задание

Создать учетную запись с именем пользователя sara и полным именем Sara Smith.
Установить пароль пользователю sara - smith95.
