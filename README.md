<details><summary>Лучший язык для промышленной разработки?</summary>
  
  ‎  
Этот абзац субъективен, однако опирается на [объективные бенчмарки](https://benchmarksgame-team.pages.debian.net/benchmarksgame/index.html). 
1. Прежде всего, язык должен быть достаточно мейнстримным, чтобы проект на нем был поддерживаемым. Сразу выбрасываем за борт всю экзотику и функциональщину вроде Haskell, Elixir, Nim, Erlang... Ruby туда же.
1. Общая практика показывает что слабая типизация однозначно вредит читаемости, поддерживаемости и порождает большое количество ошибок, поэтому выкидываем JavaScript и PHP. 
1. Идя далее, замечаем что динамическая типизация сильно ухудшает скорость работы, а варианты компиляции традиционно динамических языков, отличаются плохой поддерживаемостью, и выглядят скорее как извращение, поэтому за бортом остаётся и строго-типизированный, но динамический Python. 
1. В сухом остатке у нас есть мейнстримные строго-статически-типизированные C & C++, C#, Java, поднимающиеся к ним Kotlin, Go и Rust. 
1. Не каждый пожелает разбираться в абстракциях C++, поэтому, несмотря на лучшие пока показатели по скорости, отложим его вместе с более низкоуровневым Си для узких мест. 
1. C# и Java близнецы. Но C# более стройный синтаксически: в нем исправлены известные проблемы Java (слабые дженерики пропадающие на этапе компиляции, отсутствие пользовательских значимых типов на стеке, сочетаемость значимых и ссылочных типов как `List<Integer>`). 
1. Долгое время C# казался мне практически идеальным по кроссплатформености, высокоуровневости абстракций и скорости приближающейся местами к С++. Однако практика с Kotlin показала, что он превосходит C# и по концепциям, и по синтаксической стройности. Если C# идет по пути добавления в ядро языка все новых и новых абстракций и ключевых слов, то ядро Kotlin весьма лаконично, а весь синтаксический "сахар" базируется на встраиваемых лямбдах и вынесен в стандартную библиотеку. В чем здесь преимущество? Почти любую фичу, казалось бы языка, в Kotlin можно прочитать в стандартной библиотеке и понять как любой другой код. Kotlin, правда, немного уступает C# по скорости, но лишь потому что компилируется в байт-код Java. 
1. Перейдем к Go. Тут все так грустно и очевидно, что без лишних слов перейдем дальше к Rust. 
1. У Rust порог входа выше чем у C++, уже потому что на C++ сразу можно писать как на любом другом высокоуровневом ЯП, предоставив стандартной библиотеке разруливать работу с памятью. Rust же не даст спрятаться от решения вопросов безопасности и размещения в памяти и из-за этой необходимости, он (внезапно!) превращается в достаточно низкоуровневый язык, сравнимый скорее с Си, чем с C++.  

_Итак, по моему мнению на текущий момент, для написания большинства кроссплатформенных приложений удобнее всего использовать Kotlin, дополняя его C++ в тех случаях когда требуется скорость. Kotlin язык экосистемы Android по умолчанию, легко компилируется в JS и WebAssembly для браузеров, с небольшими приседаниями может быть использован для iOS, а с помощью jpackage легко можно подготовить исполняемый файл для Windows, macOS, Linux. _
</details>
