# swiss_german_news_articles



## Data description

This dataset contains 2401 swiss german newspaper article from the tagesanzeiger.ch
which were scraped in June 2018

Each data record contains:
    - date -> date when scraped
    
    - id -> unique id
    
    - title -> the title of the article
    
    - teaser -> the teaser of the article
    
    - text -> the text of the article
    
    - url -> the actual url where the article can be displayed in the browser






## Data format and example


{

"357": {

    "date": "2018-06-27 20:09:09.793833",
    
    "id": 357,
    
    "teaser": "EU-B\u00fcrger, die in der Schweiz wohnen und arbeiten wollen, m\u00fcssen zwei Unterlagen vorlegen. Eine Liste der EU zeigt, dass sich einige Kantone nicht ans Personenfreiz\u00fcgigkeitsabkommen halten.",
    
    "text": "Gem\u00e4ss Personenfreiz\u00fcgigkeitsabkommen d\u00fcrfen Kantone von EU-B\u00fcrgern zwei Unterlagen verlangen, damit diese in der Schweiz wohnen und arbeiten d\u00fcrfen \u2013 einen g\u00fcltigen Ausweis und eine Arbeitsbest\u00e4tigung. Nun hat die Europ\u00e4ische Union alle Kantone auf deren Praxis \u00fcberpr\u00fcft. Herausgekommen ist ein 19-seitiges S\u00fcndenregister, auf dem die Beamten Verst\u00f6sse gegen das Abkommen Kanton f\u00fcr Kanton aufgelistet haben. Die EU h\u00e4lt fest, dass Kantone oft auch Miet- oder Arbeitsvertr\u00e4ge verlangen. Nach einer Intervention der EU-Kommission sah sich das Staatssekretariat f\u00fcr Migration (SEM) veranlasst, die Kantone anzuweisen, ihre Praxis anhand der EU-Liste anzupassen. Laut einem Bericht der \u00abRundschau\u00bb wollen diese aber trotzdem zus\u00e4tzliche Nachweise von EU-B\u00fcrgern einfordern. Spielraum beibehalten In einem Interview mit der \u00abRundschau\u00bb gesteht Marcel Suter, Pr\u00e4sident der Vereinigung der Kantonalen Migrations\u00e4mter, ein, dass gewisse Kantone formaljuristisch betrachtet gegen das Abkommen verstossen, man sehe aber einen gewissen Spielraum in der Auslegung des Abkommens, den man gerne beibehalten m\u00f6chte. Weil die EU die Einhaltung des Vertrages fordert, drohe laut FDP-St\u00e4nderat Philipp M\u00fcller neues Ungemach mit der Union. Bereits im Dezember habe man dies bei der B\u00f6rsen\u00e4quivalenz gesehen, so M\u00fcller. Die EU sei sehr wohl in der Lage und vor allem willens, \u00abuns zu piesacken\u00bb. Juristisch betrachtet meint M\u00fcller, dass man einen Vertrag ausgehandelt habe und wenn man diesen \u00e4ndern wolle, m\u00fcsse man verhandeln. Tessin besonders in der Kritik Der l\u00e4ngste Eintrag im S\u00fcndenregister befasst sich mit Norman Gobbi, dem Sicherheitsdirektor im Kanton Tessin. Es sei im Interesse des Kantons, diese Kontrollen sicherzustellen, weshalb das Tessin die Praxis sicher nicht anpasse, sagt Gobbi unbeeindruckt durch die Kritik aus Br\u00fcssel. Angestellte und Grenzg\u00e4nger aus der EU m\u00fcssen f\u00fcr eine Aufenthaltsbewilligung im Tessin deshalb weiterhin in jedem Fall Mietvertrag, Arbeitsvertrag und einen Strafregisterauszug einreichen. Drei weitere Kantone folgen nun der Tessiner Praxis: Neu verlangen auch Waadt, Basel-Landschaft und Basel-Stadt einen Strafregisterauszug. Dies sei so mit dem Freiz\u00fcgigkeitsabkommen vereinbart, lautet deren Standpunkt. Ein Punkt, der f\u00fcr die EU wohl nicht hinnehmbar sein wird. Mit dem Strafregisterauszug werde \u00abeine Grenze \u00fcberschritten\u00bb, stellte der Botschafter der EU in Bern, Michael Matthiessen, bereits letztes Jahr gegen\u00fcber der \u00abNZZ\u00bb klar. Damals vermochte der Bundesrat die EU zu bes\u00e4nftigen, indem er ihr versicherte, den Missstand zu beheben. Dem war offenbar nicht so. (nag) Erstellt: 31.01.2018, 19:26 Uhr",
    
    "title": "Droht ein neuer Streit mit der EU?",
    
    "url": "https://www.tagesanzeiger.ch/schweiz/standard/Droht-ein-neuer-Streit-mit-der-EU/story/27142182"
    
},

...

...

}





## Loading the data with Python 3


import json

### loading the news into the dict news_dict
with open('news.json', 'r') as fp:
    data = json.load(fp)


### printing some values
print(news_dict['33'])

{'date': '2018-06-26 23:16:40.157664',
 'id': 33,
 'teaser': '«Falsche Anschuldigungen»: Susanne Blank zieht nach der Postauto-Affäre die Konsequenzen.',
 'text': 'Post-Verwaltungsrätin Susanne Blank tritt zurück. Sie wolle mit ihrem freiwilligen Rücktritt an der Generalversammlung der Schweizerischen Post falsche Spekulationen stoppen und der Post einen Neuanfang ermöglichen, teilte die Gewerkschaft Transfair am Dienstag mit. Blank sitzt seit Juni 2008 als Vertreterin des Personals im Post-Verwaltungsrat, delegiert vom Personalverband Transfair. Die Ökonomin hatte von 2010 bis Mitte 2014 Einsitz im Ausschuss «Audit and Risk» und seither im Ausschuss «Organisation, Nomination and Remuneration». «Keinerlei Pflichtverletzungen begangen» Zu den Spekulationen in den Medien um ihre Person hält sie in der Mitteilung der Gewerkschaft Transfair fest: «Ich habe im Fall des Subventionsbetrugs bei Postauto keinerlei Pflichtverletzungen begangen und insbesondere die Aktennotiz vom 21. August 2013 zur Prüfung Ortsbus nie erhalten, weder per Briefpost noch per Mail.» Sie habe von der Existenz der Aktennotiz erstmals im Februar 2018 in der Tageszeitung «Blick» erfahren. In den vergangenen Wochen habe sie keinerlei Medienauskünfte gegeben, sei aber dennoch mit einer Falschaussage zitiert worden. Diese Art von Berichterstattung sei rufschädigend und rechtswidrig. Blank «wehrt sich vor dem Presserat gegen falsche Anschuldigungen», heisst es in der Pressemitteilung von Transfair. Die Gewerkschaft Transfair verurteilte in der Mitteilung auch «die politische Hetzjagd» gegen Blank. Ohne Kenntnis der Faktenlage sei insbesondere aus dem rechten Lager der Rücktritt der Personalvertreterin gefordert worden. Wegen des laufenden Strafverfahrens habe sie auf Geheiss des Bundesamtes für Polizei (fedpol) keine Auskunft geben dürfen. Damit hätten auch die falschen Annahmen im Untersuchungsbericht des Anwaltsbüros Kellerhals Carrard nicht richtiggestellt werden können. Es sei kein gutes Zeichen für den Service Public und die Post, dass ausgerechnet die Personalvertreterin im Verwaltungsrat ins Visier der Politik gerate. Köpferollen auf breiter Front Anfang Februar war bekannt geworden, dass die Postauto AG jahrelang im subventionierten Geschäftsbereich Regionaler Personenverkehr Gewinne erzielt und zu hohe Subventionen von Bund und Kantonen eingestrichen hatte. Im Zuge dieser Affäre musste zunächst Post-Chefin Susanne Ruoff zurücktreten. Bei der Postauto AG mussten nach den Abgängen von CEO und Finanzchef im Februar Anfang Juni auch die noch verbliebenen acht Mitglieder der Geschäftsleitung und die Leiterin der internen Revision ihren Hut nehmen. Mitte Juni kündigte auch der Vize-Verwaltungsratspräsident der Post, Adriano Vassalli, seinen Rücktritt auf die Generalversammlung vom Dienstag hin an. Politiker von links bis rechts forderten in der Folge, dass auch andere Verwaltungsräte die Konsequenz ziehen sollten - darunter Verwaltungsratspräsident Urs Schwaller. (mch/sda) Erstellt: 26.06.2018, 13:02 Uhr',
 'title': 'Post-Verwaltungsrätin weist Vorwürfe zurück – und tritt ab',
 'url': 'https://www.tagesanzeiger.ch/wirtschaft/unternehmen-und-konjunktur/postverwaltungsraetin-susanne-blank-tritt-zurueck/story/30260633'}


print(news_dict['33']['id'])
33

print(news_dict['33']['teaser'])
«Falsche Anschuldigungen»: Susanne Blank zieht nach der Postauto-Affäre die Konsequenzen.



### iter over all news and print the title
for i, (k, val) in enumerate(data.items()):
    print(k, val['title'])

### print all available keys
data.keys()
