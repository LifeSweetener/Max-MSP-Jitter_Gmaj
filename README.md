# Max-MSP-Jitter_Gmaj
 My first project written on Max programming language!

<h1>О проекте</h1>
<h2>Для дневника</h2>
<p align="justify"><i>23.02.2022</i> я решил заняться музыкой: поиграл на гитаре, опробовал новый её строй, пониженный на целый тон (с E на D) (недавно я впервые в жизни порвал струну и заменил её), а потом вечером занялся программированием музыки. Открыл видео-ролики одного клёвого пацана по имени <b>Тимофей</b>: https://www.youtube.com/watch?v=eL2HaA0S0JQ&list=PL32i_iv4dLiyoksnO-GVAEsFuGddR4RCT — который хорошо, понятно и доступно объясняет основы языка <b>Max</b>. И начал бабахать код на Максе.</p>

<p align="justify">Утром около пяти утра у меня получилось сделать свою первую небольшую мелодию (а равно — программу на Max!) из трёх звуков в соль мажоре. Ниже я подробно опишу, о чём вообще я тут говорю вам, дорогой читатель!)</p>

<h2>Содержание</h2>
<p align="justify">
<ul>
 <li><a href="#theory">Введение в курс дела</a>
  <ul>
   <li><a href="#max">О языке программирования Max</a></li>
  </ul>
 </li>
</ul>
</p>

<h2 name="theory">Введение в курс дела</h2>
<h3 name="max">О языке программирования Max</h3>
<p align="justify">Это визуальный объектно-ориентированный язык программирования для создания real-time приложений музыкальной направленности и не только (в нём можно обрабатывать видео, изображения и т.д.). Визуальный в том смысле, что объекты, такие как виртуальные осцилляторы, микшеры, разные фильтры звуковых волн, даже объекты обычных целых чисел, арифметических операций и многие другие — эти разнообразные объекты вы расставляете прямо курсором мыши в IDE, не прописывая никакого кода!</p>

<p align="justify">То есть Max позволяет нам написать свою музыку, сделать свой электронный музыкальный инструмент и обработать уже готовые аудиозаписи других музыкантов. Кроме этого, с его помощью также можно управлять различными электронными устройствами, построенным на платформе Arduino. То есть возможна связка Arduino и Max.</p>

<p align="justify">Говоря «Max», я имею в виду совокупность сразу нескольких разных технологий: <b>Max/MSP/Jitter</b>. <i>«Max – это среда визуального программирования, основа всего; MSP – расширение, делающее возможной работу с аудио, а Jitter – расширение для работы с видео. Отсюда и название – Max/MSP/Jitter»</i> [].</p>

<p align="justify">Язык придуман <b>Миллером Паккеттом</b> — американским профессором музыки, директором центра исследования IT и искусства (англ. Center for Research in Computing and the Arts; CRCA). Такие заведения, исследующие музыкальную информатику, появились в США в середине XX-го века и очень хорошо сейчас развиваются. Запад является, можно сказать, лидером в этой области, тогда как российским умам, по словам автора книги «МУЗЫКАЛЬНАЯ ИНФОРМАТИКА В СИСТЕМЕ ПРОФЕССИОНАЛЬНОГО МУЗЫКАЛЬНОГО ОБРАЗОВАНИЯ» Ю. Терентьева, будет ещё над чем поработать в этой отрасли.</p>

<p align="justify">Среда программирования Max существует уже более 30-ти лет, и её используют композиторы, исполнители, создатели программного обеспечения и художники для создания своих музыкальных произведений, оформления своих живых выступлений перед публикой и построения художественных инсталляций. Как написано в Вики, кроме того, Max — это модульный язык программирования, имеющий в себе множество отдельных библиотек и модулей программ и предоставляющий богатый API другим людям, заинтересованным в функциональности этой среды. Max написан, к сведению, на C/C++.</p>

<h3 name="">Об основных понятиях языка</h3>
<p align="justify">Проект этого репозитория будет, хотя бы в целом, ясен и новичкам в програмировании! Объясню вам основные понятия программирования, касающиеся и Макса.</p>
<p align="justify">Программисты пишут программы в <b>исходных файлах</b>, которые имеют свой формат в каждом языке программирования:
<ul>
 <li>в Java это файлы <code>.java</code>;</li>
 <li>в C++ это исходники формата <code>.cpp</code>, <code>.h</code> или <code>.c</code>;</li>
 <li>а Python-разработчики скрипты пишут в файлах <code>.py</code>;</li>
</ul>
в Max/MSP/Jitter программы пишутся в файлах, называемых патчами и имеющих расширение <code>.pd</code>.
</p>

<p align="justify">У Max есть как проприетарная версия, так и бесплатная, называемая <b>Pure Data</b>. И именно о ней я сейчас говорю, и она использована в рамках этого репозитория и этой статьи. Эти две разновидности, две стороны одной и той же монеты — вообще ничем не отличаются, кроме графического интерфейса: у оригинального Max, разрабатываемого и продвигаемого фирмой Cycling '74, он более красочный, детальный и насыщенный. У Pure Data, которую сделал и продвинул сам Miller Puckette, интерфейс выглядит намного проще, но, если приглядеться, он такой же понятный и так же чётко отрабатывающий. Если вы пользуетесь и будете пользоваться версией Макса от Cycling '74, то за помощью по конкретным нерешённым для вас вопросам обращайтесь, вы понимаете куда, на их официальный сайт: https://cycling74.com/get-started.</p>

<p align="justify">Помимо всего, у каждого языка есть своя документация — у Pure Data она тоже есть (https://puredata.info/docs), в том числе и встроенный обучающий, справочный модуль <i>"help-intro"</i> в IDE.</p>

<p align="justify"><table align="center"><tr><td><img align="center" title="Окно справки в Pure Data" src="help module.jpg" alt="Общий вид справочного Windows-модуля Pure Data"></img></td></tr></table><p align="center">Скриншот 1 — Справочное окно в Pure Data</p></p>
