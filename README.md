#### Немного мыслей.
<details><summary>Программирование: искусство или инженерия?</summary>  
  
  ‎  
Программирование вполне можно назвать ремеслом, искусством, но не как искусство художника, а как, например, дизайн обуви или изготовление предметов быта, где инженерные требования сочетаются с пресловутой красотой.  
Поясню мысль подробнее. Благодаря синтаксической гибкости, любого, чуть более сложного чем двоичный код ~~(или Go)~~ языка, одно и то же действие на любом уровне абстракции в большинстве случаев можно описать десятками, если не сотнями способов, а порой, как при именовании сущностей, количество вариантов вообще ничем не ограничено.  
_Многообразие требует от программиста постоянного выбора, который невозможно уложить в строгий регламент._ 
Поэтому, инженерные требования надежности и поддерживаемости естественным образом порождают, казалось бы на первый взгляд, оторванные от суровой прагматики, практики писать "красивый код", "чистый код" (термины широко вошли в индустрию).
</details>
<details><summary>Язык порождает мышление или наоборот?</summary>
  
  ‎  
Иногда говорят что "настоящий программист" прежде всего должен думать над алгоритмом, а писать можно на любом языке. Согласимся и рассмотрим процесс с другой стороны: получается что программист переводит мысль, последовательность действий, с человеческого языка, на используемый им язык программирования. Конечно талантливый переводчик может переводить и на пять и на десять языков. Но погружаясь в язык, человек начинает и думать на нем, и языки программирования здесь отнюдь не исключение (особенно это заметно по программисту в состоянии потокового мышления). И наиболее часто используемый язык, оставляет отпечаток на самом мышлении. Если используешь язык не часто, то и твой код на нем будет не так ясен.  
Один ЯП для проекта лучше чем пять.
</details>
<details><summary>Лучший язык для промышленной разработки?</summary>
  
  ‎  
Этот абзац субъективен, однако опирается на объективные бенчмарки: https://benchmarksgame-team.pages.debian.net/benchmarksgame/index.html  
1. Прежде всего, язык должен быть достаточно мейнстримным, чтобы проект на нем был поддерживаемым. Сразу выбрасываем за борт всю экзотику и функциональщину вроде Haskell, Elixir, Nim, Erlang... Ruby туда же.
1. Общая практика показывает что слабая типизация однозначно вредит читаемости, поддерживаемости и порождает большое количество ошибок, поэтому выкидываем JavaScript и PHP. 
1. Идя далее, замечаем что динамическая типизация сильно ухудшает скорость работы, а варианты компиляции традиционно динамических языков, отличаются плохой поддерживаемостью, и выглядят скорее как извращение, поэтому за бортом остаются и строго-типизированный, но динамический Python. 
1. В сухом остатке у нас есть мейнстримные строго-статически-типизированные C & C++, C#, Java, поднимающиеся к ним Kotlin, Go и Rust. 
1. Не каждый пожелает каждый день быть близким к низкоуровневым абстракциям C++ (порождающим синтаксические казусы), поэтому, несмотря на лучшие пока показатели по скорости, отложим его вместе с Си для узких мест. 
1. C# и Java близнецы. Но C# более стройный синтаксически: в нем исправлены известные проблемы Java (слабые дженерики пропадающие на этапе компиляции, отсутствие пользовательских значимых типов на стеке, сочетаемость значимых и ссылочных типов (`List<Integer>`)). 
1. Долгое время из всех ЯП, я считал C# практически идеальным по кроссплатформености, высокоуровневости абстракций и скоростью приближающейся местами к С++. Однако практика с Kotlin показала, что он превосходит C# и по концепциям, и по синтаксической стройности. Если C# идет по пути добавления в ядро языка все новых и новых абстракций и ключевых слов, то ядро Kotlin весьма лаконично, а весь "сахар" базируется на встраиваемых лямбдах и внесен в стандартную библиотеку. В чем здесь преимущество? Почти любую фичу, казалось бы языка, в Kotlin можно прочитать в стандартной библиотеке и понять как любой другой код. Kotlin, правда, немного уступает C# по скорости, но лишь потому что компилируется в байт-код Java. 
1. Перейдем к Go. Тут все так грустно и очевидно, что без лишних слов перейдем дальше к Rust. 
1. Rust базируется на прекрасных идеях, однако возносит безопасность в абсолют, поэтому программист становится заложником этой безопасности -- нельзя просто сконкатенировать строки, нельзя просто написать HelloWorld. Надо постоянно думать о памяти и использовать "правильные" абстракции (привет unwrap). По моим ощущениям, у Rust порог входа выше чем у C++, потому что в C++ можно писать как на высокоуровневом ЯП, предоставив стандартной библиотеке разруливать работу с памятью за тебя. Rust же не даст спрятаться от решения вопросов безопасности и размещения в памяти и из-за этой необходимости, он (внезапно!) превращается в достаточно низкоуровневый язык, сравнимый скорее с Си, чем с C++.  

_Итак, в сухом остатке, по моему мнению на текущий момент, для написания кроссплатформенных и не сильно требовательных по скорости (Windows, macOS, Linix, Android) приложений, проще и удобнее всего исползовать Kotlin, а для всех остальных (достаточно редких) случаев -- C++.
Kotlin "родной" язык для экосистемы Android, он компилируется как в JS так и WebAssembly для браузеров, а обычный jar файл можно упаковать для любой десктопной ОС._
</details>
