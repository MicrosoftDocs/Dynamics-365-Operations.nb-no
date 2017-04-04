---
title: Opprette bestillinger
description: "Denne artikkelen beskriver prosessen og alternativene når du oppretter en bestilling manuelt."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: de8fa93bfc0119d6f9433fb4215c326abdda2899
ms.lasthandoff: 03/31/2017


---

# <a name="create-purchase-orders"></a>Opprette bestillinger

Denne artikkelen beskriver prosessen og alternativene når du oppretter en bestilling manuelt.

Når du oppretter en bestilling, angis generell informasjon om hele ordren i bestillingshodet, og deretter legger du til én eller flere bestillingslinjer. Denne artikkelen beskriver noen av de mest brukte alternativene som er tilgjengelige.  

Du kan også opprette bestillinger ved å kopiere linjer fra et annet bestillingsdokument eller en salgsordre. I slike tilfeller kan du snu fortegnet på beholdningen, slik du vil snu fortegnet på en faktura for å angi kreditnota.  

Selv om du kan opprette bestillinger manuelt, genereres de vanligvis fra andre prosesser. Ordre kan opprettes automatisk basert på andre dokumenter, for eksempel rekvisisjoner. De kan også opprettes som en del av prosessen gjennom planlagte POs for hovedplanlegging. Hvis du bruker kjøpsavtaler, POs kan opprettes av den **frigivelsesordre** handling. Det er også mer avanserte metoder for å automatisk opprette en bestilling. Bestillinger kan for eksempel opprettes når du bruker direktelevering eller konserninterne bestillingskjeder.

## <a name="creating-a-purchase-order-header"></a>Opprette et bestillingshode
Når du oppretter en ny bestilling, vises en dialogboks der du kan angi den vanligste informasjonen for bestillingshodet. Når du klikker **OK** for å lukke dialogboksen, opprettes bestillingen, og du kan deretter angi tilleggsinformasjon i hodet.  

Den første informasjonen du må tenke på når du oppretter en bestilling, er bestillingstypen. Typen **Bestilling** brukes oftest. Hvis en kreditnota er nødvendig, kan du imidlertid bruke typen **Returordre**.  

Du må angi leverandør i feltet **Leverandørkonto**. Du kan søke etter kontoen eller leverandørnavnet for dette feltet. Hvis en leverandør leverer fra flere lokasjoner, men bruker én enkelt fakturakonto, kan du velge denne fakturakontoen i feltet **Fakturakonto** og deretter bruke denne med forskjellige leverandørkontoer. Hvis du må opprette en bestilling for produkter som ikke skal bestilles gjentatte ganger, kan du bruke alternativet **Engangsleverandør**. Dette alternativet oppretter automatisk en ny leverandørkonto som er merket som en engangskonto for å støtte en senere oppryddingsprosess for engangskontoer i modulen **Leverandører**. Når du velger en leverandørkonto, arver mange felt i bestillingshodet standardverdier fra informasjonen som er knyttet til leverandørkontoen. Standard leveringssted og lager kopieres for eksempel fra leverandørinformasjon. Du kan imidlertid overstyre disse standardverdiene hvis kjøpet er ment for en annen lokasjon.  

Hvis leverandøren har gitt et referansenummer for bestillingen, kan du registrere denne informasjonen i feltet **Leverandørreferanse**. For returnerte ordrer må du angi en verdi i feltet **ARM** for å referere til leverandørens autorisasjon for behandling av returen.  

Hvis en kjøpsavtale er tilknyttet ordren, må du angi denne informasjonen i feltet **Kjøpsavtale**.  

Bestillingshodet inneholder også informasjon om gebyrer som gjelder hele ordren i stedet for enkeltlinjer. Tillegg kan legges automatisk til ordren hvis automatiske tillegg er definert for leverandøren eller leverandørens kostnadsgruppe. Du kan også legge til tillegg manuelt i ordrehodet ved å klikke **Vedlikehold tillegg** i handlingsruten.

## <a name="adding-purchase-order-lines"></a>Legge til bestillingslinjer
Bestillinger kan være for fysiske produkter eller tjenester. En innstilling på lagermodellgruppen avgjør om et bestemt varenummer gjelder for et produkt eller en tjeneste. Varen som kjøpes angis vanligvis av et varenummer. Hvis ordren er for produktene eller tjenestene som forbrukes direkte, kan du imidlertid også angi varen ved hjelp av en innkjøpskategori.  

Bestillingslinjene inneholder mange felt, men mange av disse feltene har en standardverdi eller en verdi som er arvet fra ordrehodet. Flere felt angis når du velger et produkt eller tjeneste. Feltene som oftest angis manuelt inkluderer feltene for varenummer, antall og ønsket leveringsdato. Informasjon om enhetspris og rabatter er også svært viktig, men verdiene i disse feltene bestemmes ofte av forretningsavtaler eller kjøpsavtaler.  

Når du velger et produkt, kan du søke på hele eller deler av produktnavnet i stedet for å bruke varenummeret. Hvis produktet har flere varianter, for eksempel forskjellige størrelser, kan du vise en oversikt over tilgjengelige varianter ved hjelp av funksjonen **Legg til linjer** eller ved å bruke oppslag som er tilgjengelige i feltet **Variantnummer**.  

Du må ofte angi flere dimensjoner for varen som er valgt på hver bestillingslinje. Dimensjonene som må angis, avhenger av dimensjonsgruppene som er knyttet til den overordnede definisjonen for produktstandard. Du må for eksempel ofte angi et sted og lager for å angi lokasjonen som produktet skal leveres til. Du kan identifisere produktvarianter ved å angi et variantnummer, eller ved å angi verdier for én eller flere produktdimensjoner, for eksempel farge, størrelse, konfigurasjon eller stil. Sporingsdimensjoner, for eksempel parti- og serienummer, lar deg identifiserer hver lagerpartiet. Når du har opprettet en ordre, du kan registrere dimensjonsverdier på bestillingen ved hjelp av handlingen **Registrering**. Du har for eksempel bestilt fem stykk av en vare. Senere registrerer du at tre av delene skal være svart og to av blå. Denne tilnærmingen er et alternativ til å registrere dimensjonsinformasjon under ankomstregistreringen.  

Du kan kontrollere detaljene for lagertransaksjonsstatus for lagerførte produkter. Du kan for eksempel kontrollere lagerbeholdningen for å hjelpe deg med å avgjøre hvor mye du skal bestille. Du kan også se gjennom beholdningsstatusen for et bestilt antall for å se om innkommende ankomstregistrering er utført.  

En bestillingslinjen som brukes til å returnere et produkt til leverandøren har et negativt antall. Du kan velge et bestemt parti å returnere ved hjelp av handlingen **Reservering**.  

Noen ganger vil du kanskje dele antallet du har bestilt, slik at ulike deler av det leveres på forskjellige datoer. Du kan definere disse leveringene ved hjelp av handlingen **Leveringsplan**, som er tilgjengelig på **Bestillingslinje**-menyen i visningen **Linjer**.  

Tillegg kan legges automatisk til bestillingslinjer hvis automatiske tillegg er definert for leverandøren eller leverandørtilleggsgruppen, og for varen eller varens kostnadsgruppe. Imidlertid legges vanligvis tillegg til manuelt på ordrelinjenivå. Hvis du vil legge til et tillegg, åpner du siden **Vedlikehold tillegg** ved hjelp av handlingen **Vedlikehold tillegg** på siden **Finans** -menyen i visningen **Linjer**. Fordelen med å legge til tillegg direkte på ordrelinjenivå er at tillegget kan tildeles som en lagerkost. Hvis du vil definere tilleggskoder for kontoproduktkostnader, bruker du debetalternativet **Vare**. Disse tilleggstypene må tildeles fra bestillingshodet til linjene før ordren kan bekreftes. Du kan for eksempel tilordne tillegg basert på antallet på hver linje. Kategorien for tillegg påvirker også hvordan tillegg etterberegnes. Faste tillegg angir for eksempel et fast beløp, og prosenttillegg beregnes som en prosent av nettobeløpet for ordrelinjen. Bestillinger kan tilordnes til en last, og lasten kan inneholde et estimat over den forventede kostnaden for transportkostnadene. Du kan tildele denne utgiften fra lasten tilbake til bestillingslinjene.

## <a name="purchase-order-actions"></a>Bestillingshandlinger
Når du har lagt til hodet og linjene i bestillingen, må du ofte fullføre flere trinn før bestillingen er klar til å bli bekreftet. Fordi så mange alternativer er tilgjengelige, kan det være nyttig å bruke [Handlingsøk](/dynamics365/operations/action-search) for å finne det relevante menyelementet.  

Du kan konfigurere produkter i ordren, slik at de har tilleggsvarer. Tilleggsvarer er varer som må eller kan kjøpes sammen med andre produkter. Tilleggsprodukter kan legges til kostnadsfritt som medfølgende produkter, eller du kan avgjøre om du vil legge dem til i ordren eller ikke. Du kan se gjennom tilleggsvarene etter hver ordrelinje som legges til. Du vil imidlertid sannsynligvis finne det enklere å se gjennom og legge til relevante tilleggsvarer for alle ordrelinjene ved hjelp av siden **Tilleggsvarer**, som du kan åpne i handlingsruten.  

Rabatter legges vanligvis til linjer når de opprettes. Noen få rabatter gjelder imidlertid hele ordren:

-   Handlingen **Sluttrabatt** beregner en sluttrabattprosent som gjelder for hele ordren. Du må ikke forveksle denne rabatten med kontantrabattprosenten. Kontantrabatter brukes når fakturaen betales, og de er avhengige av betalingsutligning innen en bestemt dato.
-   Hvis en samkjøpsrabatt gjelder, må du bruke handlingen **Samkjøpsrabatt** til å beregne og tilordne den til ordren. Samkjøpsrabatter er rabatter som kan tilbys hvis en blanding av produkter i ordren, overskrider en fellesterskel. Bare noen få selskaper bruker denne typen rabatt.

Tillegg som har en tilleggskode som bruker debettypen **Vare**, må tilordnes til linjenivå før ordren kan bekreftes. Det kan være nyttig å tilordne disse tilleggene på ordrehodenivå, slik at du kan angi det totale beløpet for tillegget. I dette tilfellet må imidlertid tillegget deretter tildeles ned til hver linje før ordren kan bekreftes. Du kan bruke handlingen **Tilordne tillegg** for å skille beløp fra tillegg som er tilordnet på hodenivå og ned til ordrelinjene. Tillegg kan skilles i henhold til nettobeløpet for hver linje, i henhold til antallet som er bestilt eller jevnt fordelt over ordrelinjene. Når du har tildelt tilleggene til linjene, fjernes tillegget fra ordrehodet.  

Bestillinger kan konfigureres til å kreve at budsjettmidler fordeles til ordren før den kan behandles. I slike tilfeller kan du bruke handlingen **Budsjettkontroll** for å fordele budsjettet.  

Det kan hende du må forsinke fullføringen av en bestilling. Du vil for eksempel ha mer informasjon om produkter eller tjenester, eller det kan hende du må få godkjenning av forbruket. Det er flere måter å holde tilbake en ordre. Du kan for eksempel vente med å bekrefte ordren. Hvis en arbeidsflyt for endringsadministrasjon brukes, sender du ikke ordren til godkjenning. Hvis du må blokkere alle ordrer for en bestemt leverandør, kan du også merke leverandør som **På vent** for behandling på leverandørstandarden. Det finnes også situasjoner som kan hindre at ordren blir behandlet. Behandling kan for eksempel hindres hvis kredittgrenser er overskredet, eller hvis nødvendige budsjettmidler er ikke tilgjengelige.

<a name="see-also"></a>Se også
--------

[Purchase order overview](purchase-order-overview.md)

[Bestillingsgodkjenning og -bekreftelse](purchase-order-approval-confirmation.md)

[Produktkvittering mot kjøpsordrer](product-receipt-against-purchase-orders.md)

[Oversikt over leverandørfakturaer](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)


