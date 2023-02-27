# Lab Report 3
Command chosen: grep\
grep is a command line tool to search for strings, input files, matching lines, patterns in files.\
This is how you use it: `grep 'word' filename`

## 1. `-r`
`r` is used to search for a string recursively in all directories.\
For example, if you want to search for a student's name, you can use this command. \
Here are two examples:\
All the matching strings are highlighted in red in the attached images.

```
[cs15lwi23aho@ieng6-202]:skill-demo1-data: 106$ grep-r
"Centuries" written 2
written_2/travel_guides/berlitz1/HistoryIbiza.txt:
the island and quickly imposed their culture. Centuries of almost
written_2/travel_guides/berlitz1/WhereToMadrid.txt:
soon recovered. Centuries of investigation have failed to uncover the<img width="574" alt="image" src="https://user-images.githubusercontent.com/92295739/221454849-98a7d4eb-c7d4-4496-b3d1-602611957a29.png">

written_2/travel _guides/berlitz2/Bahamas-History.txt: Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the L
uccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modes
† crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the
Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called th
ese people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not fi
nding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
```
```
[cs15lwi23aho@ieng6-202] :skill-demo1-data: 104$ grep
".txt" results.txt > grep-results. txt<img width="1094" alt="image" src="https://user-images.githubusercontent.com/92295739/221451690-947b994e-bfc6-4252-880f-8eda934371fb.png">

[cs15lwi23aho@ieng6-202]: skill-demo1-data: 105$ grep
-r
"Lucayans" written 2
written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the L
uccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modes
t crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the
Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called th
ese people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not fi
nding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt: The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that th
eir galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the exp
lorers dug a fresh-water well - at a spot now known as
"Spanish Wells"
- which was used to replenish the supplies of water on their ships before they
egan the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 p
eople, were removed from the Bahamas to work - and die
- in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewh
ere in the Caribbean.
```

![Image](r1.png)
![Image](r2.png)

It is important to note that `-r` looks at uppercase and lower case. Searching for "Centuries" will give results for Centuries with 'C' capatalized. 

## 2. `-i`
`i` is basically `r` but ignoring case sensitivity. It searches for the relevant string no matter if it's uppercase or lowercase.\
This has a similar application as `-r`. For example, if you want to search for a student's name, but there are instances where you have mentioned the name in lower case as well as upper case, you can use this command. There are cases where we accidentally use uppercase in between words. `-i` would help us in such cases. \

Here are two examples:
```
[cs15lwi23aho@ieng6-2021 :berlitz1:131$ grep -i "india" IntroIndia.txt
INDIA AND ITS PEOPLE
India is exhilarating, exhausting, and infuriating - a land where,
that popular myth attaches to India. In place of the much-publicized,
and much-misunderstood, mysticism of its ancient religions, India in
India comprises a diamond-shaped subcontinent that stretches
right down to Kanyakumari, or Cape Comorin, on the Indian Ocean. From
east to west India also covers about 3,000 km, from Arunachal Pradesh
cultural affinity with India - feuding brothers rather than unrelated
to be a perpetual but necessary dynamic of Indian civilization.
banknotes are sinteami: Wit', * b° fcial cangtages: Hindt, Urdu,
of the languages spoken all over India, leaving out the dialects, comes
from southern India, you soon realize there's no such thing as a
"typical" Indian.
India's prehistoric settlers were probably what
ruddy granite that dominates the peninsula of southern India.
```
```
[cs15lwi23aho@ieng6-202]:berlitz1:135$ grep -i "japan" WhatToJapan.txt
Modern Japan has embraced the consumer society to such an
extent that shopping can be a full-time pursuit. The Japanese
Japan is notoriously expensive, so don't expect fabulous
inefficient distribution systems. Japanese tourists visiting other
countries are still shocked to find Japanese consumer goods available
at Japan's highest prices.
```
Note: we searched in lowercase but results are also in uppercase.

![Image](i1.png)
![Image](i2.png)

## 3. `-c`
`c` counts the total number of lines where the string pattern appears\
Eg: If you want to look for how many times a student has gotten an academic dishonesty violation, you can simply use this command followed by the student's name and all the lines where the student's name appears will show up. This will give you an idea of how many times a student has been academically dishonest.

Here are two examples:
```
[cs15lwi23aho@ieng6-202] :berlitz1:140$ grep -c "Vegas" IntroLasVegas.txt
25
[cs15lwi23aho@ieng6-202] :berlitz1:141$ grep-c "Italian" HistoryFrance.txt
2
[cs15lwi23aho@ieng6-202l :berlitz1:142$
```
![Image](c.png)

## 4. `-v`
`v` is used to invert the grep output. It lists all the lines that do not contain the mentioned string\
For example, if you want to search for all the students that passed the class, you can search for 'F' and all the other letter grades will show up.

Here are two examples:

```
[cs15lwi23aho@ieng6-202] :berlitz1:137$ grep -v "japan" WhatToJapan. txt
What to Do
Shopping
Modern Japan has embraced the consumer society to such an
extent that shopping can be a full-time pursuit. The Japanese
themselves (in the big cities at least) can be seen more often than not
with some kind of shopping bag - they make very large, sturdy
ones - just on the off chance that they might want to buy something.
You cannot get to know this country properly, even if you don't want to
buy anything, without exploring the rich and varied range of
traditional arts and crafts, the famous cornucopia of electronic
gadgets and precision instruments, or the impressively awful selection
of kitsch souvenirs in the major tourist centers.
```

```
[cs15lwi23aho@ieng6-202] :berlitz1:139$ grep -v "History" HistoryIbiza.txt
A handful of Bronze Age relics has fostered an assumption
that prehistoric settlers inhabited Ibiza thousands of years ago.
Greater evidence of such a people is found on Mallorca and Menorca than
on Ibiza, but one of the Balearics'
most important sites is actually on
the island of Formentera, where the megalithic monument/tomb of Ca Na
Costa has been dated to 2000 b.c.
•Ibiza's key location between Africa and ancient Iberia made
it a convenient stopover for Mediterranean seafarers, such as the
Phoenician traders, who called the island Ibosim. The Greeks dubbed it
Ebysos, the Romans called it Ebusus, and the Moors, Yebisah.
```

![Image](v1.png)
![Image](v2.png)

## 5. `-w`
`w` searches for the line containing the exact matching word\
You can use this to find the name of the student. For example, if you are looking for a student called 'Bella', using `-i` would provide results saying 'Isabella' too. Using `w` would give us precise results. \
Here are two examples:

In the first example, since there are no words that say exactly "ind", there are no results. In the sceond example, we see all "India" results. 

```
[cs15lwi23aho@ieng6-202] :berlitz1:142$ grep-w "ind" HistoryIndia.txt
[cs15lwi23aho@ieng6-202] :berlitz1:143$ grep -w "India" HistoryIndia.txt
India has always been a melange of peoples. Apart from some
pre-Ice Age hominids, the first settlers to arrive in India were
then on to Iran before entering India. These fair-skinned
took to the asceticism which has characterized spiritual life in India.
invaders appeared at India's frontiers; Cyrus, Emperor of Persia,
lasting impact on India during the two-year campaign.
Maurya (321-297 b.c. ), was also to become the founder of India's first
elephants, chariots, and infantry. Southern India remained independent,
the northern half of India and into Central Asia. His reign was one of
prosperity, making India a trade center between east and west.
arts also flourished in India during these early times. Madurai was the
many bounties, such as silk, musk, and amber, in exchange for India's
reigned for 40 years over northern India, and encouraged Buddhist monks
In southern India, power was shared by the Pallavas in
Islam Comes to India
```

![Image](w.png)

Click here for the [sources](https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix)
