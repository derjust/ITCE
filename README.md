IT Consulting Essentials (ITCE)
====

# License
This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

# Introduction
## What it's not
## Dilbert

# IT Essentials
## Technology doesn't matter
[Programmers are obsessed with ease rather than simplicity (thank you Rich Hickey for making this point); or, what the experience of programming is instead of what the resulting program is like. This leads to useless conversations about semicolons and whether we need a preprocessor that eliminates curly braces. We still talk about programming as if typing in the code was the hard part. It's not - the hard part is maintaining the code.](http://singlepageappbook.com/goal.html)
## Issue tracking
Excel can be a solution
## SCM
Tags, Lost work of a day
## Patterns
Design by Bug - I guess it’s obvious how it works 
Design by feature - als schicksal so mancher älterer software. Vorzugsweise nach weggang der ursprünglichen entwickler
design by constriction - irgend eine zentrale komponente hat ne beschränkung. drumherum wird zuerst eine kleine lösung gefummelt, damit zu leben. Dann metastasiert das...

## Writing Code
You are not the first solving your current problem. Period.

* Abhaengigkeiten. Server wird auf ein Mal zu schnell
Oh, ja, da haben wieder zu viele Leute geglaubt, eine neue Technik sei ein "free lunch". Früher musste man alles optimieren, damit der Server es ausgeliefert bekam. Jetzt denken sie "ach, ist ja alles lokal am client, der ist schon schnell genug…". Wobei Ladereihenfolge bei JS, Packer-oder-nicht, Caching, da auch zwischenfummeln können und dem Client das Leben schwer machen.
Was die Freunde irgendwelcher fancy Animationen nicht raffen - es geht den Usern irgendwann am Arsch vorbei oder womöglich auf den Sack. War neulich auf einer Seite, die als Scrollpage aufgebaut war und die nachrückenden Elemente mit ausgewiesener(!) Verzögerung nachlud und dann mit einem gaaaaanz tollen zoom-move platzierte. Nein, zeigt es einfach an und gut ist. Form folgt der Funktion. Visual candy is no valuable functionality.


Aber in solchen Forenbeiträgen läuft es dann ja nicht anders - da sollte doch mal jemand mit "Welterfahrung" dabei sein! Stattdessen stehen die mit der Nase vor dem Problem und haben nie gelernt, einen Schritt zurück zu machen.

## Fixing Code
"It works. Don't know why" ist nicht gerade das Mindset mit dem Web-Applications entwickeln sollte die per normalem Internet zugaenglich sind.
Das Mindset hat nirgends Platz! Weil man dann nämlich weiß, dass man beim nächsten schwerwiegenden Problem "back to square one" ist, weil man es eben nicht verstanden hat und demnach nicht sinnvoll analysieren kann. Selber auch schon schön erlebt: Der Fehler tritt nicht mehr auf - Was habt ihr gemacht? - Nur XYZ an Stelle ABC. - Aber ABC hat mit dem eigentlichen Problem doch gar nix zu tun, warum soll das geholfen haben? - Weiß auch nicht, aber jetzt läuft es ja.
### Understand your framework/library/third party API

### Strings
http://www.joelonsoftware.com/articles/Unicode.html

### Dates
A date/time without a timezone is just a number - alles andere ist Glaskugel - Siehe Strings

### Databases
Wen muss ich bei MS und Oracle bezahlen, dass keien Inline-Parameter in SQL mehr funktionieren?!

"You know ACID for data bases – I can’t remember itself what those letters stand for - but it is about reliability”
BRAIN - I can't remember what that stands for. But it is about not forgetting to exhale.

### File handling
Warum GUIDs als Export-Datei-Namen eine schlechte Idee sind
Closing handles
OS-Limitations!

### Physical or logical units
Use complex types if available. A java.io.File should be used instead of re-inventing half the code with a plain String (Javascript: path)

## Rewriting Code
Don't - think about it - Still don't
http://www.joelonsoftware.com/articles/fog0000000069.html
http://onstartups.com/tabid/3339/bid/97052/How-To-Survive-a-Ground-Up-Rewrite-Without-Losing-Your-Sanity.aspx

## Performance improvements
Don't - measure first

## Documentation
So schreiben, als wenn keiner da waere zum Fragen. 
Ueberblick geben. Nicht das WIE ist entscheident, dass was und warum (vgl 5W, Abstraktion)
Wenn die Fehlermeldung vom Kunden ein 2. Mal nicht verstanden wird: Known-Errors Section anlegen (und den Meldungstext verbessern)
Irgendetwas WIki-Artiges oder nur ein Dokument auf einer Ablage haben reicht - man muss den Boss kein ECM budgetieren lassen.


## DevOps
Aus dem 'real life' würde ich wohl immer sagen „there ain’t no such thing as a free lunch“ - http://de.wikipedia.org/wiki/TANSTAAFL - irgendwer muss immer seine Arbeitsweise ändern, es geht nicht "umsonst". Wenn Ops schneller deplyoen soll, muss business vorher besser spec'en und Dev vorher besser testen… (mal ganz simpel).
Sowas hätte man aber auch ohne buzzword "Devops" vorher auch schon gut haben können… Und wenn ich dann noch an Echtweltszenarien denke, wo man keine Testsysteme oder Mocks hat, uiuiui. Das schreit dann nach mehr "red tape"

### Umgebungen
DEV, Test, UAT, Production, Post-Production
Nicht mischen - wissen wofuer was gut ist - Integration!

# Consulting
## Excel
"The excel" - encodings! Formatting! Macros! Popups!
## Abstraktion
Abstraktion erfordert, dass man selber den Kontext verstanden hat. Und vielleicht auch mal in Mustern denken kann.
Und fragmentierte Specs (die Bäume) ohne ein umgreifendes Konzept (der Wald) sind halt auch nur formell geil 

"Abstraktion für Dummies": Enthält 5 große und 5 kleine Kärtchen, 30 Verbindungspfeile, alles beschriftbar (und abwischbar). Die Advances Version hat dann nur 3, 3, 15 oder so.

* Vererbung wurde mal erfunden um gleiches Verhalten ueber Objekte hin zu erreichen - Copy&Paste macht das auch - Nur leider ausschliesslich einmalig. (Sprach's und erschuf 2 abstrakte Klassen und loeschte 5000 Zeilen Code)

Beware of the next toxic pattern: In der Diskussion so weit verallgemeinern, dass sich beliebige Problemfälle bis zur Frage nach der Weltformel erfassen lassen - das "natürlich" nicht lösbar ist und man dann eine prima Begründung für Untätigkeit hat.

## Mails
https://twitter.com/GSElevator/status/501844818654265344

## Meetings 

[David Grady: How to save the world (or at least yourself) from bad meetings](http://www.ted.com/talks/david_grady_how_to_save_the_world_or_at_least_yourself_from_bad_meetings)

### Kidnapping a meeting
### Agenda-less (aka Random) Meetign
## 5W
5W-Auditability (who what when where why).

http://en.wikipedia.org/wiki/Five_Ws

http://creatingminds.org/tools/kipling.htm

http://www.google.de/imgres?imgurl=http://coe.jmu.edu/learningtoolbox/images/5w1h01_c.gif&imgrefurl=http://coe.jmu.edu/learningtoolbox/5w1h.html&h=191&w=254&tbnid=709komaJ_L8Q2M:&zoom=1&tbnh=90&tbnw=120&usg=__VIp8aZcJq1KRbqEOaeCZcbJPxFQ=&docid=t1o671qYEJ7GsM&client=firefox-a&sa=X&ei=Zw-gU7bBMbSB7Qb0u4HgBA&ved=0CDMQ9QEwBA&dur=6749

http://www.google.de/imgres?imgurl=http://execpowerup.files.wordpress.com/2008/03/who-what-where-when-why-how.jpg&imgrefurl=http://execpowerup.wordpress.com/human-capital/5w1h-questions/&h=820&w=1075&tbnid=28oLBS1bd4mLHM:&zoom=1&tbnh=90&tbnw=118&usg=__QvNoTaDLVGWT46RzeXaTci_YH-A=&docid=YadrhkZpVW8YJM&client=firefox-a&sa=X&ei=Zw-gU7bBMbSB7Qb0u4HgBA&ved=0CCoQ9QEwAQ&dur=1618

## Security
["But when it comes time to deploy and enable modules, I need to have administrator permission", responded Jim.
"You can get the super-admin user to do that. No need for you to have those privileges."
"Well, yes. But that will delay things. And doesn't really do much for security, as I have full access to the source code, server and database." 

As an aside, it's rarely good to argue that you should be given a security exemption by suggesting that if you wanted to screw the company, it was already within your power to do so. Just keep that in the back of your mind as you move through your career.](http://thedailywtf.com/articles/Limited-Options)

## Career
http://www.javaworld.com/article/2597522/learn-java/what-i-wish-id-known-starting-out-as-a-programmer.html

## Abstrakte Kommunikation (Rundmails etc.)
Aus Fixpunkt bastelt man sich seine Realitaet wenn niemand gewillt ist die Fixpunkte zu erklaeren - ist doch das selbe mit mystischen Halbsaetzen in Konzernrundmails wenn sie nicht erklaert werden.
Mit der Publikation solcher Realitaetsannaehrungen sollte man dann wiederrum aber nicht jeden belaestigen der nicht bei 3 verschwunden ist 


# Appendix 
## Follow up material
http://www.tickld.com/x/6-management-lessons-that-everyone-should-know

http://www.faqs.org/docs/artu/ch01s06.html

https://github.com/substack/stream-handbook