## **Webshoppen del 1**

Det här ett spännande och praktiskt uppdrag där vi ska skapa en enkel men funktionell webbshop! I detta projekt kommer ni att bygga en webbplats för en fiktiv butik som säljer ett urval av produkter. Målet är att ge er praktisk erfarenhet av webbutveckling och att använda JavaScript för att manipulera data och skapa en interaktiv användarupplevelse.

![](https://github.com/chasacademy-sandra-larsson/boilerroom-webshoppen/blob/main/inspo.png)

## **Instruktioner** 👋

*Teamet:*
* Alla i teamet ska vara med och implementera och diskutera. Föredra mobbprogrammering, men använd gärna Git :-)

*Vad ni ska göra:*
- Utveckla en enkel webbshop där besökarna kan se och interagera med ett urval av produkter. Den behöver bara innehålla en HTML-sida men får innehålla fler.
- Använd arraymetoder som **`map`**, **`filter`**, **`sort`** och **`reduce`** för att hantera produktdatan.
- Ni ska visa produkter baserat på produktdata, det ska gå att filtrera mellan kategorier, sortera efter pris, det ska gå att lägga till produkter i en varukorg och även beräkna totalpriset av produkterna som lagts till i varukorgen. Ni får addera mer funktionalitet om ni hinner.
    - **`map`:** för att rendera ut produkterna från början och i kundvagnen.
    - **`filter`:** för att filtrera kategorierna.
    - **`reduce`:** för att slå ihop totalpriset.
- Byt ut varukorgen till en separat sida och använd **`localStorage`** för att spara innehållet i varukorgen över sessioner.
- Om behov finns, dela upp js i moduler
- Använd regelbunden versionshantering och tydliga commitmeddelanden. 
- Prioritera funktionalitet, men glöm inte att webbplatsen ska vara responsiv och användarvänlig.
- Ni får utgå från exemplen nedan eller koda allt från scratch!

*Exempel på HTML och JS*
```
/* 
Ni väljer om ni använder produktdatan i js eller json och om ni vill lägga till 
fler properties som bilder etc.

Ni fetchar från ett api  som t.ex. https://fakestoreapi.com/ för att generara
ut fiktiva produkter därifrån istället för från en lokal js/json.
*/

const products = [
    { id: 1, name: 'T-shirt', category: 'kläder', price: 100 },
    { id: 2, name: 'Hörlurar', category: 'elektronik', price: 250 },
    { id: 3, name: 'Keps', category: 'kläder', price: 50 },
    { id: 4, name: 'Mobiltelefon', category: 'elektronik', price: 500 }
];

const cart = [];
```
```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Enkel Webbshop</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>
  <h1>Välkommen till vår Webbshop!</h1>
	  
  <h2>Våra produkter</h2>
  <!-- filter knappar för produkt kategorier här -->
  <!-- Visa era produkter innuti product-container -->
  <div id="product-container"></div>

  <h2>Din Varukorg</h2>
  <!-- visa produkter som lagts till i kundvagnen och totalsumman innuti cart -->
  <div id="cart"></div>
	
  <!-- alert, eller sida som säger produkterna är på väg -->
  <button id="checkout">Gå till kassan</button>
	
  <script src="script.js" type="module"></script>
</body>

</html>
```
## **Design**

Ni har full kreativ frihet att designa webbshoppen. Ta en titt på några befintliga e-handelsplattformar eller använd en enkel design som nedan.

![](https://github.com/chasacademy-sandra-larsson/boilerroom-webshoppen/blob/main/inspo2.png)
![](https://github.com/chasacademy-sandra-larsson/boilerroom-webshoppen/blob/main/inspo3.png)

## **Webbshoppen del 2**

I denna del ska du implementera händelsespårning av taggen gtag.js som monitoreras i Google Analytics.

1. Skapa ett Google Analytics konto
2. Skapa ny egendom som baserar sig på live-versionen av denna sida.
3. I slutet av steg 2) får du denna kodsnutt. Lägg in den i index.html

```
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID">
</script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```
4. Vänta 2-3 dagar på att gtagg:en synkar mot er sida. Kolla i Google Analytics kontot att du får besökare som registreras.


###Workshop  19:e november

Nu ska ni ha en gtag som registrear händelsepårning i Google Analytics.

1. Börja med att diskutera i teamet vad de olika default events:en innebär: 

* 	page-view
* 	user_engagement
* 	scroll
* 	session_start
* 	first_visit

2. Nu ska ni implementera minst 3 st custom events. För gtag ser det ut så här: 

    ```
    gtag('event', 'button_click', {
        'event_category': 'interactions on products',
        'event_label': 'adding products to cart',
        'value': 1,
        'debug_mode': true
      });
    ```

    Som ni sedan lägger in under önskad händelse någonstans i er JS.
   
  3. Börja att kolla i "Debug view" att händelsen registreras. 
  4. Se sedan över monitoreringen i "Realtime overview".
  5. För dokumentation och inlämning tar ni screenshots över era custom events och en beskrivning vad de spårar.
  6. Reflektera i teamet och sammanfatta på 300-500 ord i Readme.md. Vilka möjligheter finns det med händelsespårning? Finns det begränsningar?
     

## **Inlämning**

Ni lämnar in slutgiltigt repo under u04 i Canvas. 
 💫🚀
