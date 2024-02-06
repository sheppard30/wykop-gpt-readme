
# Spis treści
1. [Wstęp](#wstep)
2. [Jak pozyskać tokeny?](#jak-pozyskać-tokeny?)
3. [FAQ](#faq)
4. [Uwagi techniczne](#uwagi-techniczne)
5. [Plany rozwoju](#plany-rozwoju)


## Wstęp
Wykop-gpt został stworzony aby służyć użytkownikom Wykopu i pozwolić im na korzystanie z narzędzia ChatGPT bez konieczności rejestracji na OpenAI i opłacania miesięcznej subskrypcji OpenAI Plus (za wersję gpt-4), która w momencie pisania tego tekstu wynosi aż **20 USD**. Każdy użytkownik ma do dyspozycji **1500** darmowych tokenów do wykorzystania w ramach zapytań do ChatGPT w wersji 3.5. 

## Jak pozyskać tokeny? 
Na samym początku chciałbym zaznaczyć, że jako autor tego narzędzia ponoszę szereg kosztów wynikających z udostępnienia tej funkcjonalności, m.in. koszty zapytań do OpenAI czy serwera, nie wspominając już o poświęconym prywatnym czasie na jej tworzeniu. Moim pomysłem jest finansowanie działania narzędzia jedynie z dobrowolnych wpłat użytkowników Wykopu i innych darczyńców, dlatego przyszłość bota i dalszy jego rozwój są uzależnione od tego czy/ile do tego projektu będę musiał dokładać z własnej kieszeni :)  

**Aby uzyskać kolejne tokeny**, wspomóż projekt, [kliknij i postaw mi wirtualną kawę w serwisie BuyCoffee](https://buycoffee.to/sheppard30) . W ramach wdzięczności, jeśli sobie zażyczysz, otrzymasz dodatkowe tokeny, dostęp do najnowszych feature'ów oraz **ChataGPT w wersji 4 Turbo**.  ( ͡° ͜ʖ ͡°) Pamiętaj, jeżeli chcesz otrzymać tokeny, **w formularzu na stronie BuyCoffee zaznacz opcję *Chcę pozostawić wiadomość dla Twórcy* i w polu, które się pojawi wpisz swój nick z Wykopu**, tak abym wiedział komu odblokować dostęp do najnowszych funkcjonalności i doładować konto.

**Pamiętaj!** Twoje wsparcie nie jest płatnością za usługę a dobrowolną darowizną. Nie ma żadnego oficjalnego przelicznika co do ilości tokenów / PLN natomiast chcę abyś pamiętał(a), że celem projektu **nie** jest zarabianie na nim a to aby, dzięki pieniądzom z darowizn móc **sfinansować działanie bota** oraz dać Wam możliwość wygodnego **korzystania z GPT-4 Turbo (ulepszona wersja GPT4, niedostępna w OpenAI Plus) zintegrowanego z Wykopem** na korzystnych dla Was warunkach.

## FAQ
**1.  Jak użyć WykopGPT?**

Wystarczy zawołać konto bota, np: "@wykop-gpt kto jest najpotężniejszym programistą i dlaczego Sheppard?". Możesz również wcześniej zacytować komentarz innego użytkownika aby nadać kontekst.

**2.  Ile wynosi limit tokenów w darmowej "próbce"?**

Limit wstępnie ustawiłem na 1500 tokenów. Możliwe, że zostanie skorygowany po pierwszych testach.

**3.  Ile wynosi doładowanie tokenów po wpłacie darowizny?**

To zależy od kwoty ale wstępnie, biorąc pod uwagę koszty, można bezpiecznie założyć że będzie to około 20-30gr za 1000 tokenów. Wielce prawdopodobne, że kwota ta będzie ruchoma, natomiast chciałbym aby stali darczyńcy mieli korzystniejsze warunki.

**4.  Ile to jest 1500 tokenów? Dużo, Mao?**

Możesz wejść na stronę https://platform.openai.com/tokenizer i sprawdzić sam wpisując jakieś zdanie w polu tekstowym. Pamiętaj, że ilość tokenów pobranych z Twojego konta to tokeny składające się na sumę pytania oraz odpowiedzi bota. 

**5.  Ile będę czekał(a) na doładowanie?**

Na początku nie będzie to proces zautomatyzowany, więc będę robił to w swoim wolnym czasie, możliwie szybko. W zależności od tego oraz zainteresowania, może to być do max kilku dni od czasu pojawienia się darowizny w systemie BuyCoffee. Po doładowaniu konta dostaniesz PW na Wykopie z informacją o ilości przyznanych dodatkowych tokenów. 

**6. Co jeżeli z jakiegoś powodu bot nie odpowie na moje pytanie? Czy tokeny znikną?**

Tokeny są odejmowane dopiero po wysłaniu odpowiedzi na Wykop. Jeżeli nie otrzymałeś odpowiedzi, nie zostały pobrane dla Twojego konta.

 **7. Dostałem informację, że moje pytanie zawiera potencjalnie niedozwolone treści. Co to oznacza?**
 
 Twoje pytanie zostało zakwalifikowane przez AI jako potencjalnie naruszające regulamin Wykopu oraz OpenAI i nie zostało przesłane do ChataGPT. W takim przypadku Twoje tokeny zostaną pobrane a powtarzanie się takich sytuacji, może skończyć się zablokowaniem dostępu do usługi dla Twojego konta. 

 **8. Wysłałem raptem kilka pytań i już nie mam darmowych tokenów?**
 
Liczba darmowych tokenów jest bardzo ograniczona ponieważ za "darmowe" tokeny na Wykopie autor musi mimo wszystko płacić OpenAI. Pamiętaj, że na całkowity "koszt" Twojego pytania składa się suma tokenów z pytania oraz odpowiedzi bota dlatego warto go poinstruować aby odpowiedział w możliwie zwięzły sposób.

 **9. Czy bot ogarnia pastę o serwerowni?**

 Nie, tej pasty o której myślicie nie ogarnia, więc szkoda marnować tokeny na zadawanie tego typu pytań. :)

**10. Jaka jest różnica między modelami?**

Darmowa wersja GPT-3.5 to "najprostszy" model, znacznie słabszy niż jego ulepszone wersje GPT-4 oraz najlepszy - GPT-4 Turbo. Zwykły GPT-4 jest dostępny w płatnej subskrypcji OpenAI Plus za 20$ miesięcznie natomiast GPT-4 Turbo (który udostępniam wspierającym) jest dostępny tylko dla użytku deweloperskiego.

## Uwagi techniczne

### Limity API

Każde z API, z których korzysta bot posiada swoje limity przyjmowanych requestów w jednostce czasu, np. wykopie zależy to od [rodzaju konta](https://wykop.pl/faq/konto#limity-na-koncie). Z tego powodu może się zdarzyć, że poprawne zapytanie nie zostanie przetworzone. W miarę możliwości, bot będzie zwracał informacje o problemie bądź próbował ponowić operację, jednak w przypadku odbicia się od wyżej wspomnianego limitu komentarzy na Wykopie, może się zdarzyć, że bot nie odpowie na pytanie użytkownika. Tokeny w takim wypadku nie zostaną pobrane z konta a odpowiedź pojawi się z opóźnieniem lub w ogóle.


## Plany rozwoju

- dodanie obsługi generowania grafiki przez chata bezpośrednio na Wykop
- wysłanie rozmowy z całego wpisu do bota, dzięki czemu pozna kontekst i lepiej dopasuje odpowiedź
- automatyzacja systemu doładowania tokenów i alternatywne metody ich pozyskania
- no i  się jeszcze zobaczy, jestem otwarty na pomysły od Was :)

Aktualizacja: 05.02.2024, 23:00






