
Abstract	2
Section 1 (Gruppe 1)	2
1. What is Energy?	2
2. Which 3 variables are analyzed?	2
3. What are Execution Types?	2
4. What is a Programming Paradigm?	3
Section 2.1 (Gruppe 2)	3
Warum ist RQ1 nicht offensichtlich?	3
Was sind Benchmark-Probleme?	5
Können Sie im Detail auf die vier Paradigmen eingehen?	5
Section 2.2 (Gruppe 3)	6
Can you explain 1-3 of the (benchmark) problems (research)?	6
n-body Benchmark	6
How was the experiment set up to ensure compatibility of results?	6
What does listing 1 do exactly?	6
Section 2.3 (Gruppe 4)	7
1. Can we replicate the experiment in a small way?	7
2. Can we make a general statement regarding (c ), (i), (v)?	7
3. Can you make an additional statement looking at table 3?	7
Section 3.1 (Gruppe 5)	8
What is the difference between the results and analysis section?	8
Restate the research questions in your Own words	8
Draw a Graphic for The results in 3.1	9
Section 3.2 (Gruppe 6)	10
1. List the averaged groupings and define the terms	10
What is the answer to RQ2?	10
Time is not correlated with Energie ?	10
What can you say about the results shown in Table 4?	11
Section 3.3 (Gruppe 7)	11
RQ3:	11
RQ4:	11
Summary / Conclusion (Gruppe 8)	12
Explain in your own words how you can use Table 5.	12
Do you care about this ?/Why is this relevant ?	12
What language are you interested in and why ?	12
Abstract
In this study, we assess the performance of 27 programming languages across ten standardized problems from the Computer Language Benchmark Game. Employing identical algorithms, we execute programs using top-tier compilers, virtual machines, interpreters, and libraries for each language. Our analysis focuses on three variables: execution time, memory consumption, and energy usage. We categorize results based on execution type (compiled, virtual machine, interpreted) and programming paradigm (imperative, functional, object-oriented, scripting), presenting rankings for each combination. Noteworthy findings include the correlation between slower/faster languages and energy consumption, as well as the impact of memory usage on energy efficiency. The discussion explores how these insights can aid software engineers in selecting languages with an emphasis on energy efficiency.
Section 1 (Gruppe 1)
1. What is Energy?
Energy = Time x Power (vgl. Seite 256, rechts unten)
[a shorter execution Time doesn't mean better energy efficiency]

In our context, energy mainly refers to the consumption of energy by software applications and systems and the goal which is to be as energy efficient as possible
2. Which 3 variables are analyzed?
Execution time, memory consumption, energy consumption
3. What are Execution Types? 
Execution types refer to different methods by which a programming language is translated or processed to execute the instructions written in the code. There are three main methods:
Compiled Execution: Source code is translated into machine code or an intermediate code by a compiler before the execution. The compilation process is done ahead of time and after that the resulting code is executed.
Virtual Machine (VM) Execution: The source code is not directly translated into machine code. Instead, it is translated into an intermediate code that is executed by a virtual machine. The virtual machine acts like a translator between the program (compiled code) and the computer, making is easier for the program to run on different types of computers (windows, mac, Linux)
Intérpreted Execution: In this method, there is no separate compilation step. The source code is interpreted and executed line by line by an interpreter at runtime. This method is often platform-independent, as the interpreter reads and executes the code directly, adapting to the specifics of the underlying system.
4. What is a Programming Paradigm [paradaim]?
A programming paradigm is a way or style of organizing and structuring computer programs. Different programming paradigms provide distinct principles, concepts, and techniques for creating programs.

Impérative: Focuses on describing the step-by-step procedure for achieving a specific goal. Instructions are given to the computer to perform operations in a specific order.

Functional: Emphasizes the use of functions and the evaluation of expressions rather than the execution of statements.

Object oriented (OO): Organizes code into objects, which are instances of classes. Encapsulation, inheritance, and polymorphism (reusability) are key concepts in OO, allowing the modeling of real-world entities and their interactions.

Procédural: Focuses on specifying what the program should accomplish without specifying how to achieve it. It describes the desired outcome, and the interpreter or compiler figures out the implementation of details.

5. What is a Benchmark?
Benchmarks sind in diesem Kontext eine Reihe von Programmen, die in verschiedenen Programmiersprachen geschrieben sind und dazu dienen, vergleichbare, repräsentative und umfassende Lösungen für eine Reihe von gut bekannten und vielfältigen Programmieraufgaben bereitzustellen (vgl. The Computer Language Benchmarks Game).

Beispiel für Benchmarks im Alltag: CPU/GPU Benchmark, zum Testen der Leistung, Temperatur etc. von Prozessoren und Grafikkarten. Bei diesen wird unter Volllast bzw. in verschiedenen Spielen getestet, wie sich das Verhalten der zu testenden Geräte sich ändert.
Section 2.1 (Gruppe 2)

Warum ist RQ1 nicht offensichtlich?
RQ1: Können wir die Energieeffizienz von Programmiersprachen vergleichen?

Antworten:
1. Unterschiedliche Problemräume:
Programmiersprachen sind oft für verschiedene Arten von Aufgaben oder Problemfelder optimiert. Einige Sprachen eignen sich möglicherweise hervorragend für numerische Berechnungen, während andere besser für die Verarbeitung von Text oder die Webentwicklung geeignet sind. Daher hilft der Vergleich ihrer Energieeffizienz über eine vielfältige Auswahl von Benchmark-Problemen, eine umfassendere Perspektive zu bieten.
(Verschieden Sprachen sind für verschiedene Aufgaben optimiert)
2. Implementierungsunterschiede:
Auch für dasselbe Problem können verschiedene Sprachen unterschiedliche Implementierungen, Algorithmen oder Codierungsstile haben. Ein Vergleich der Energieeffizienz erfordert nicht nur den Vergleich von Sprachen, sondern auch die Sicherstellung, dass die Implementierungen für jede Sprache vergleichbar und gut optimiert sind.
(Verschiedene Sprachen haben verschiedenen Code für die gleiche Aufgabe)
3. Ausführungsumgebung:
Die Effizienz einer Programmiersprache kann von der zugrunde liegenden Hardware- und Softwareumgebung beeinflusst werden. Faktoren wie die Compiler-Version, die Laufzeitumgebung und die Systemarchitektur können die Leistung beeinflussen. Daher muss ein fairer Vergleich diese Variablen kontrollieren.
(Verschiedene Programmiersprachen sind für verschiedene Hard- und Software optimiert -> möglichst neutrale Umgebung schaffen)
4. Messherausforderungen:
Die genaue Messung des Energieverbrauchs ist eine komplexe Aufgabe. Im Paper wird die Verwendung von Intels RAPL-Tool erwähnt, das feinkörnige Energieabschätzungen bietet. Jedoch können Unsicherheiten in den Messmethoden und -werkzeugen Abweichungen in den Vergleich einführen.
(Es können Messfehler vorkommen)
5. Wechselspiel von Faktoren:
Energieeffizienz geht nicht nur um Ausführungszeit oder Speicherplatz; es ist eine Kombination dieser Faktoren. Das Verständnis der Beziehungen zwischen Energieverbrauch, Ausführungszeit und Speicherverbrauch ist entscheidend für einen umfassenden Vergleich.
(Es gibt mehrere Faktoren, die relevant sind und ineinander greifen)
 6. Objektive Metriken:
Die Definition objektiver Metriken für Energieeffizienz und die Sicherstellung fairer Vergleiche zwischen Sprachen stellt Herausforderungen dar. Faktoren wie die Effizienz von Compilern, Laufzeitbibliotheken und die Fähigkeit zur Nutzung von Hardwaremerkmalen können die Ergebnisse beeinflussen.
 
Angesichts dieser Komplexitäten zielen die Forscher darauf ab, RQ1 durch die Etablierung einer robusten Methodik zu adressieren, die verschiedene vergleichbare Implementierungen von Lösungen für verschiedene Probleme in mehreren Programmiersprachen umfasst. Dieser Ansatz gewährleistet ein umfassenderes Verständnis der Energieeffizienz und ihrer Beziehung zu Ausführungszeit und Speicherverwendung in unterschiedlichen Szenarien. Die Nicht-Offensichtlichkeit liegt in der Notwendigkeit einer systematischen und gründlichen Untersuchung, um sinnvolle und gültige Vergleiche zwischen Programmiersprachen zu ziehen.

Was sind Benchmark-Probleme?
Benchmark-Probleme sind spezifische Rechenaufgabe oder Programmierherausforderungen, die verwendet werden, um die Leistung und Energieeffizienz verschiedener Programmiersprachen zu bewerten und zu vergleichen. Jedes Benchmark-Problem ist darauf ausgelegt, einen bestimmten Typ von Berechnung oder Problemlösungsszenario zu repräsentieren.

Können Sie im Detail auf die vier Paradigmen eingehen?
1. Funktionales Paradigma:
Beispiele: Erlang, Ruby, Rust
Charakteristika:
- Fokussiert auf das Konzept mathematischer Funktionen.
- Vermeidung von veränderbaren Daten und Zustandsänderungen.
- Betonung von Ausdrücken und Deklarationen anstelle von Anweisungen.
- Starke Unterstützung für Funktionen höherer Ordnung und Rekursion.
2. Imperatives Paradigma:
Beispiele: Ada, C, C++
Charakteristika:
 - Ausführung basiert auf Anweisungen, die den Zustand eines Programms ändern
 - Verwendung von Variablen und Zuweisungen zur Speicherung und Manipulation von Daten
 - Betonung von Kontrollstrukturen wie Schleifen und Bedingungen
 - Ermöglicht die explizite Manipulation des Speichers und unterstützt mutierbare Daten.
3. Objektorientiertes Paradigma:
Beispiele: Ada, C++, C#
Charakteristika:
 - Organisiert Code in Objekte, die Daten und Verhalten kapseln.
 - Unterstützt Konzepte wie Vererbung, Polymorphismus und Kapselung.
 - Objekte kommunizieren miteinander über definierte Schnittstellen.
 - Fördert die Wiederverwendung von Code und Modularität durch die Erstellung von Klassen und Objekten.
4. Skript-Paradigma:
Beispiele: Dart, TypeScript, JavaScript, Python
Charakteristika:
 - Interpretierte Sprachen, die oft für die Automatisierung von Aufgaben verwendet werden.
 - Haben typischerweise dynamische Typisierung und Abstraktionen auf hohem Niveau.
 - Betonung von Benutzerfreundlichkeit und schneller Entwicklung.

 - Gut geeignet für Aufgaben wie Webentwicklung, Automatisierung und Systemskripting.

Section 2.2 (Gruppe 3)
Can you explain 1-3 of the (benchmark) problems (research)?
n-body Benchmark
https://benchmarksgame-team.pages.debian.net/benchmarksgame/description/nbody.html#nbody
The program simulates the orbits of Jovian planets (Jupiter, Saturn, Uranus, and Neptune) using a specific method called a symplectic integrator. A symplectic integrator is a numerical method used to approximate solutions to differential equations.	
fannkuch-redux
fannkuch-redux description (Benchmarks Game) (pages.debian.net)
Fannkuch-redux is a benchmark problem used to evaluate the performance and energy efficiency of programming languages, involving the generation of permutations of a sequence and the computation of the maximum reversal distance for those permutations.
spectral-norm
Spectral-norm is a benchmark problem that assesses the performance and energy efficiency of programming languages by computing the highest singular value of a matrix.
How was the experiment set up to ensure compatibility of results?
Languages which didn’t at least cover 80% of the benchmark problems were discarded.
The study followed the CLBG (Computer Language Benchmark games) documentation for compiler and execution options.
Each solution was tested individually to ensure it could be executed without errors.
Each benchmark solution was executed ten times to reduce the impact of cold starts and cache effects. 
Consistent hardware was used across all tests.
What does listing 1 do exactly?
The listing records the current time before the execution of a benchmark solution.
The listing then performs an initial energy measurement using the RAPL (Running Average Power Limit) tool
The program for the benchmark solution is being executed
The listing then performs the RAPL calculation again to determine the difference between the initial energy measurement and the measurement after the program execution.
Finally, the solution calculates the time elapsed during the benchmark solution.
Section 2.3 (Gruppe 4)
Can we replicate the experiment in a small way?
Yes, you could replicate the experiment in a small way, but the results would be less precise
Can we make a general statement regarding (c ), (i), (v)?
Compiled languages best energy consumptions, low run time and low memory usage, followed by virtual machine and then interpreted
Can vary
Depends on the Application

Can you make an additional statement looking at table 3?
Still good options other than compiler based languages, like virtual machine based languages
Java is best virtual machine based language, comparable performance to the compiler based in some benchmarks
The ratio plot allows us to understand if the relationship between energy and time is consistent across languages
A variation in the ratio indicates that energy consumed is not directly proportional to time, but dependent on the language and/or benchmark solution









Section 3.1 (Gruppe 5)


What is the difference between the results and analysis section? 
 
The results section focuses on showing the result of the previous Test and answers RQ1, while in the Analysis section, new questions are being asked on the foundation of the results section. 
 
Restate the research questions (RQ) in your Own words
 RQ1: Is there a numerical factor to compare programming Languages in terms of energy efficiency?
RQ2: Is using a faster Programming language always more Energy Efficent? 
 
RQ3: 	Is there a programming Language that uses less memory and is more energy           Efficient? 
RQ4: Are Memory, Time and Energy the only factors relevant for judging what is the best Programming Language?

Draw a Graphic for The results in 3.1 





Section 3.2 (Gruppe 6)

 List the averaged groupings and define the terms
The least amount of memory space to execute the solutions:
 
Programming languages:
Compiled Languages: Needed 125Mb on average.
Virtual Machine Languages: Needed 285Mb on average.
Interpreted Languages: Needed 426Mb on average.
 
Programming Languages by Paradigm:
Imperative Languages: Needed 116Mb on average.
Object-Oriented Languages: Needed 249Mb on average.
Functional Languages: Needed 251Mb on average.
Scripting Languages: Needed 421Mb on average.
 
Ein Programmierparadigma ist ein grundlegender Stil, in dem ein Programm entworfen wird.
Programming Paradigms: Programming Paradigms (lmu.edu)
What is the answer to RQ2?
RQ2: Is the fastest language always the most energy efficient?
Antwort kann in Tabelle 4 gefunden werden. Wenn man sich nur die ersten drei Sprachen anschaut, könnte man vermuten, dass die Antwort ja lautet, allerdings gibt es viele Sprachen, die das Gegenteil beweisen. Die einzigen Sprachen, die abseits von den Top sprachen bei energy und time auf dem gleichen Platz bleiben sind nämlich OCaml, Haskel, Racket und Python der rest Shuffled durch und beweist, dass die schnellere Sprache nicht immer die Energieeffizienteste ist.

Time is not correlated with Energie ? 

Ein allgemeines Missverständnis ist, dass wenn man die Ausführungszeit reduziert, sich der Energieverbrauch gleichermaßen reduziert. Die Formel für Energie ist Power X Time. Allerdings kann man die variable Power nicht als konstant ansehen. So gibt es Sprachen, die zwar sehr schnell sind, aber auch sehr viel Energie verbrauchen.
Das sieht man auch in Tabelle vier bei der allgemeinen Auswertung: Nur die Top-Sprachen haben ähnliche Ränke bei Zeit und Energieverbrauch, bei den restlichen Unterscheiden sich die Ränke stark. 

What can you say about the results shown in Table 4?
Tabelle 4 fasst die Ergebnisse aller Durchführungen zusammen und bewertet anhand von Energie, Zeit und Memory.
Die genutzte Memory hat nichts mit Zeit oder Energie zu tun. Kompilierte Sprachen sind bei allen drei Punkten am weitesten oben. 


Section 3.3 (Gruppe 7)
RQ3:
How does memory usage relate to energy consumption? -> Wie ist der Zusammenhang zwischen dem Energieverbrauch und dem Speicherverbrauch?
Es gibt keinen klaren Zusammenhang zwischen dem Energieverbrauch des DRAM und dem Spitzen-Speicherverbrauch (peak memory usage). Die Korrelation ist zu schwach, um einen Zusammenhang zu erkennen.
Schlussfolgerung: Der Energieverbrauch hat nicht mit der Menge des Speichers zu einem bestimmten Zeitpunkt zu tun, sondern wie der Speicher arbeitet/verwendet wird. Es sollte also in Zukunft der kontinuierliche Speicherverbrauch (continuous memory usage) untersucht werden, welcher einen stärkeren Einfluss auf den Energieverbrauch haben sollte. Vor allem Faktoren wie Garbage Collection, Cache-Nutzung, Registerplatzierung und Datenmanagementeffizienz werden hierbei berücksichtigt*. 


*pov:


 relationship between memory usage and energy consumption in computer programming languages.
 Two scenarios are considered: 
-  continuous memory usage 
- peak memory usage.


When examining DRAM energy consumption, the top five languages with the lowest energy consumption are C, Rust, C++, Ada, and Java, with only Java not being compiled. The bottom five, with higher energy consumption, are Lua, JRuby, Python, Perl, and Ruby, all interpreted languages.


******
 On average, compiled languages consume less energy than virtual machine or interpreted languages.
*****





Need md plug-in














RQ4:
Können wir automatisch entscheiden, welche Programmiersprache unter Berücksichtigung von Energie, Zeit und Speichernutzung am besten ist? 
Oftmals sind Entwickler besorgt um mehr als eine (möglicherweise begrenzte) Ressource. Zum Beispiel sowohl um Energie und Zeit, Zeit und Speicherplatz, Energie und Speicherplatz oder alle drei.
=>Wenn der Entwickler nur an Ausführungszeit und Energieverbrauch interessiert ist, dann ist es fast immer möglich, die beste Programmiersprache auszuwählen. Bei Berücksichtigung von Speicher wird es schon schwieriger.
=>Aber meistens muss der Entwickler eine Entscheidung treffen und dabei berücksichtigen, welche anderen Merkmale in jedem speziellen Szenario am wichtigsten sind. Dabei sollten auch funktionale und nicht-funktionale Anforderungen für die Entwicklung der Anwendung beachtet werden.









Summary / Conclusion (Gruppe 8)

Explain in your own words how you can use Table 5.
->Table 5 Compares programming Languages based on an algorithm called Pareto optimization.
It compares the languages based on (execution) time, Energy (consumption) and memory (usage).
We can use this table to decide what programming languages to use for our project based on our requirements.
 
Do you care about this ?/Why is this relevant ?
->  This becomes increasingly important for greater tasks and cost. Example: Companies need programs that run efficiently. It is required that their programs are written in languages that consume less energy and require less memory and thus require less ram and hardware to execute. (lower cost)
Also considering Ai research this becomes important. AI models need to read a lot of data quickly in order to create responses and provide solutions. Writing these AI models in programming languages that run the fastest and are the most resource-efficient seems logical.
 
What language are you interested in and why ?
->The programming languages C, Pascal and Rust seem to be the most effective languages to write code when considering the factors Memory, time and Energy.
