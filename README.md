# tokenicer

Tinkering with tokenization and NLP for Icelandic.

Visualizations from https://www.kaggle.com/code/deeepsig/llm-tokenizer-visualizer

The project is based on the video by Andrej Karpathy on tokenization: https://www.youtube.com/watch?v=zduSFxRajkE

special tokens(not actrually special tokens, but tokens for text generation):
"<Afmæli> <Birthdays> <Afríka> <Africa> <Afþreying> <Entertainment> <Almannavarnir> <Civil protection> <Alþingiskosningar> <General elections> <Asía> <Asia> <Atvinnulíf> <Business> <Atvinnumál> <Employment Affairs> <Auðlesið efni> <Easy news> <Aðsent> <From readers> <Bandaríkin> <USA> <Barnaefni> <Children's section> <Bretland> <UK> <Bæjar- og sveitarfélög> <Municipalities> <Bílar> <Auto section> <Bíó og sjónvarp> <Film & TV> <Bókmenntir> <Books> <Covid> <Covid> <Covid-19> <Covid-19> <Dóms- og lögreglumál> <Crime> <Dýr> <Animals> <Esb> <EU> <Efnahagsmál> <Economy> <Erlendar fréttir> <World> <Eurovision> <Eurovision> <Evrópa> <Europe> <Eyjaálfa> <Oceania> <Fasteignir og húsæðsmál> <Real estate and housing> <Ferðalög> <Travel> <Ferðamál> <Tourism> <Fjölskyldan> <Family> <Flug> <Air Traffic> <Flóttafólk og innflytjendamál> <Refugees and immigration> <Fréttaskýringar> <Commentary> <Fréttir> <News> <Fólk> <People> <Fótbolti> <Football> <Fótbolti - ísland> <Domestic football> <Gagnrýni> <Review> <Garðrækt> <Garden> <Golf> <Gold> <Handbolti> <Handball> <Handbolti - ísland> <Domestic handball> <Hannyrðir> <Needlework> <Heilbrigðismál> <Public Health Authority> <Heilsa og útlit> <Health & Fitness> <Heimilið> <Home> <Hryðjuverk> <Terrorism> <Innlent> <Iceland> <Jafnréttismál> <Equality> <Jól> <Christmas> <Kjaramál> <Wage Affairs> <Klaustursmálið> <Klaustur scandal> <Kosningar> <Election> <Kvikmyndir> <Film> <Kynning> <Promotion> <Körfubolti> <Basketball> <Körfubolti - ísland> <Domestic basketball / Basketball - Iceland> <Landbúnaður> <Agriculture> <Landshlutar> <Local> <Leiklist> <Theater / Stage> <Leiðarar> <Editorials> <Lesbók morgunblaðsins> <Morgunblaðið weekend supplement> <Loftslagsmál> <Climate> <Lífsstíll> <Lifestyle> <Mannlíf> <People / Life> <Matur og drykkur> <Food & drink> <Menning> <Culture> <Menntamál> <Education> <Minningargreinar> <Obituaries> <Mið- og suður-ameríka> <Central- & South-America> <Mið-austurlönd> <Middle East> <Myndlist> <Art> <Neytendamál> <Consumer issues> <Norður-ameríka> <North-America> <Norðurlönd> <Nordic countries> <Náttúra og umhverfi> <Nature & Environment> <Samgöngumál> <Transportation Affairs> <Sjávarútvegsmál> <Fisheries> <Sjónvarp> <TV> <Skopmyndir> <Cartoons> <Slys og eldsvoðar> <Accidents and fire> <Smartland> <Smartland> <Stjórnmál> <Politics> <Stríð> <War> <Tilkynningar> <Announcements> <Trúarbrögð> <Religion> <Tækni og vísindi> <Tech & Science> <Tíska> <Fashion> <Tónlist> <Music> <Tölvuleikir> <Games> <Umfjöllun> <Discussion> <Umræða> <Debate> <Uppljóstrun> <Exposure> <Veiði> <Hunting & Fishing> <Veður> <Weather> <Veður og náttúruhamfarir> <Weather & Natural Disasters> <Viðhorf> <Opinion> <Viðskipti> <Commerce> <Viðtöl> <Interviews> <Í dag - mbl.is> <Today - mbl.is> <Íslensk stjórnmál> <Domestic politics> <Íslenskt mál> <Icelandic language> <Íþróttir> <Sports> <Óflokkað> <Uncategoriezed> <Ólympíuleikar> <Olympics>"

example output

<Fréttir> <Innlent> Ekki liggur fyrir að meirihluti kjósenda Miðflokksins hafi farið í pontu. Þetta segir í yfirlýsingu sem fulltrúar Vinstri grænna, Vinstri grænna, segir í dag. Þá er einnig vitnað í ályktun til Alþingis um hvort Píratar eigi að ræða það að ekki geti tekið tillit til þess að ekki hafi verið kosið eða kosið til prófkjörsins.<Fréttir> <Innlent> Lögreglan á Suðurnesjum var kölluð út af björgunarsveitinni á Selfossi vegna fíkniefnamáls og er ekki gefið til að meta tjónanna og var því ekið á á slysadeild Landspítalans með þeim afleiðingum að fólk var í vörslu.Í tilkynningu frá lögreglunni er m.a. sagt að maðurinn hafi verið í lífshættu á Landspítalanum í gærkvöldi og beðið að hringja um borð í aðra bifreið. „Þá var maður bara að koma til móts við bílinn. Ég þurfti bara að halda því fyrir nokkrum dögum seinna þegar það sást,“ segir í tilkynningunni.<Mannlíf> „Það er rosalega gaman að koma í heiminn. Ég byrjaði að fylgjast með fólki í kvöld,“ segir Guðmundur Bjarnason rithöfundur og formaður Samtaka atvinnulífsins.„Ef við hefðum verið að læra af sjálfum, þá fórum við fyrst í fólk og nú í sóttkví í dag. Það gekk kannski að gera þetta því þá. Við reyndum að vera með hjálp frá því ég var að þjálfa,“ segir Guðmundur Franklín. Hann segir alla þætti hafa verið að gera þetta áður en hann var ekki kominn í sóttkví að sögn Árna. „Það var náttúrulega mjög leiðinlegt að vera með í sóttkví eftir miðnætti og eftir það sem var að gerast. Það var auðvitað eitthvað sem hafði verið fyrir utan sóttkvíar. Ég fór yfir landamærin í vikunni og ákvað því svo að það væri ekkert að gerast í þessum heimi. En það eru allt fólk og við vorum að fá þetta og það er mikið af fólki. Þá ertu bara einhver að fara að fara að skoða þetta,“ segir Halldór.Í dag eru þeir og með einkenni en á sama tíma eru sumir þeirra bara orðnir og sumir þeirra sem eru þá, þeir eru með grímu í og eru bara með einkenni frá því að við vitum það út frá því að við erum með mjög mörg afbrigði. „Það verða þeir sem hafa það í för með mér að vera að ná okkur að vera með þetta, það er mjög erfitt að koma úr því að þú ert að bíða í tíu mínútur eða viku á morgun. En þetta var bara alveg magnað,“ segir Sigurður og brosir.<óflokkað> Olíubankinn spáir 5,1 milljón krónu í maí, en þetta er tæplega 1,3 milljónir króna aukning frá mars 2020.Icelandair Group spáir 3.400% hækkun...

How do we make great language models for smaller languages such as Icelandic?

I believe that to develop a good language model, the tokenizer must be great.

Currently, the architecture of language models such as GPT and BERT depends on tokenization. Before the training of language models all text must be given a numerical representation, or a respective token. The act of converting text into tokens is called tokenization, and the algorithm that performs tokenization is called a tokenizer.

If the training data is badly tokenized it becomes difficult for the language model to converge. Therefore, to develop a good language model, the tokenizer must be great.

The question is: how good are the tokenizers of state-of-the-art language models for Icelandic and what can we do to improve them?

I measured the performance of 3 different tokenizers, here are the results:

1. The GPT-2 tokenizer

   -

2. The GPT-4 tokenizer

3. Jón Friðrik Daðason's gpt-2-igc-is tokenizer
