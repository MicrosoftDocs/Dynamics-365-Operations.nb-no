---
title: Produktidentifikatorer
description: Dette emnet gir informasjon om de ulike typene av produktidentifikatorer og forklarer hvordan du kan legge til produktidentifikatorer i produktdataene.
author: cvocph
manager: AnnBe
ms.date: 03/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode, EcoResProductListPage, EcoResProductDetailsExtended, EcoResProductVariantsPerCompany
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 0aa8baf5802ccdd9a502e2a7d291a76fc4afe932
ms.sourcegitcommit: d91d96c98b31ae59bc82ec91efbb7da86ffb25fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172031"
---
# <a name="product-identifiers"></a>Produktidentifikatorer

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om de ulike typene av produktidentifikatorer og forklarer hvordan du kan legge til produktidentifikatorer i produktdataene.

Når du arbeider med produkter på shop floor eller i et lager i Microsoft Dynamics ERP eller Microsoft Dynamics CRM, må du ha en god strategi for å identifisere disse produktene og produktvariantene.

## <a name="unique-product-numberproduct-id"></a>Unikt produktnummer/produkt-ID

I Dynamics 365 Supply Chain Management er den primære ID-en for et produkt produktnummeret (det vil si den unike produkt-ID-en) Dette nummeret kan genereres automatisk av en nummerserie, eller det kan knyttes manuelt til et produkt. For produktvarianter kan numrene defineres gjennom produktterminologimalen .

I mange tilfeller er ikke produktnummeret opprinnelig opprettet i Dynamics 365 Supply Chain Management. Det er derimot tilknyttet et produkt i et system for administrasjon av produktlivssyklus (PLM) eller administrasjon av produktdata (PDM). Du bruker i dette tilfellet dataenheter for å importere produkter og produktvarianter. Supply Chain Management bruker deretter tallene i alle operasjoner.

Når du implementerer Supply Chain Management, bør du gi særlige hensyn til din strategi for produktnumre. Et godt nummereringssystem forbedrer logistikkflyter og bidrar til å forhindre feil. En god produkt-ID har opptil 15 tegn. Ideelt sett har den færre enn 10 tegn og inneholder ikke mer enn fem klassifiseringstegn. Du kan også bruke søkenavn for å aktivere hurtigsøk. Et søkenavn er et ekstra navn som representerer klassifiseringene av et produkt.

Når du bruker Common Data Service, er produktnummeret i Supply Chain Management også produktnummeret i Common Data Service. Produktvarianter synkroniseres til Common Data Service som forskjellige produkter.

## <a name="item-number-and-product-dimensions"></a>Varenummer og produktdimensjoner

Varenummeret er den produkt-IDen som brukes av en bestemt juridisk enhet. Ideelt sett bør varenummeret være lik produktnummeret. Hvis terminologien er forskjellig per juridisk enhet, blir det vanskelig å følge et produkt gjennom hele forsyningskjeden, og det nødvendiggjør tidkrevende nymerking og referanseprosesser. Vi har beholdt denne modellen for kompatibilitet med eldre versjoner (det vil si med Microsoft Dynamics AX 2009 og tidligere). Vi anbefaler imidlertid at du eliminerer identifikatorer som er spesifikke for juridiske enheter når det er mulig, og at du bruker de unike produktnumrene som den primære IDen i stedet.

I tillegg kan ikke en produktvariant identifiseres unikt av et varenummer. Det kreves alltid kombinasjonen av et varenummer og alle produktdimensjonene som er definert for produktstandarden. Dette kravet kan bli problematisk, og kan redusere hastigheten på identifikasjonsprosessen. Også derfor anbefaler vi at du bruker det unike produktnummeret i stedet varenummeret når det er mulig.

Mange sider har fremdeles varenummeret og produktdimensjonene som de primære IDer. Produktnumrene kan imidlertid brukes for søk. Under **Salg og markedsføring** &gt; **Oppsett** &gt; **Søk** &gt; **Søkeparametere** kan du endre søkeoppslaget slik at det bruker produktnumre i stedet for varenumre som den primære søkestrategien. Hvis du setter **Aktiver oppslag for produktsøk** til **Ja**, vil oppslaget ikke bare vise produktstandarder, men produktvarianter. Hvis du vil ha mer informasjon, kan du se [Søke etter produkter og produktvarianter under ordreregistrering](search-products-product-variants.md).

I tillegg skal du kunne søke og filtrere på produktnummeret, varenavnet og beskrivelsen av og produktdimensjonens ID-er for produktvarianten. Når du velger en variant, velges alle produktdimensjonens ID-er samt det tilknyttede varenummeret. Det er derfor enklere å finne og velge riktig variant. Denne innstillingen anbefales på det sterkeste hvis du bruker produktvarianter og det unike produktnummeret som de primære ID-ene for produkter. Det eneste unntaket er kanskje motebransjen, der organisasjonens forretningsprosesser ofte krever at du velger malen før du velger en variant. Du bør vurdere dette alternativet nøye før du implementerer nummereringssystemet.

> [!NOTE]
> Varenummeret for et produkt kan ikke endres når det finnes én eller flere transaksjoner for produktet.

## <a name="product-name-and-description"></a>Produktnavn og beskrivelse

Produktnavnet og beskrivelsen er de lesbare identifikatorene til et produkt, og de kan brukes på mange språk. Supply Chain Management-klienten vises som standard all produktinformasjon på standardspråket for firmaet, og ikke på brukerens foretrukne språk. Oversatte produktnavn og beskrivelser brukes imidlertid i all kommunikasjon med kunder og leverandører. Oversettelsene er basert på språkkoden for kunde- og leverandørkontiene.

For produktvarianter kan produktnavnet genereres via en produktterminologimal. Det ikke nødvendig at produktnavnet er unikt, og derfor kan det hende flere varer har samme navn.

## <a name="product-and-item-search-names"></a>Produkt- og varesøknavn

Supply Chain Management har et sekundært søkenavn for produkter og også for varer (frigitte produkter). Dette søkenavnet trenger ikke være unikt, og det kan endres etter at et produkt eller produktvarianten opprettes. Det anbefales at du bruker et søkenavn til å søke etter produkter etter kategorier. Søkenavnene aktiverer hurtigsøk, spesielt i salgs- og innkjøpsprosesser.

Søkenavnet kan også inneholde en ID for kunde- eller leverandørprodukt eller en ID for et annet eksternt produkt, hvis denne ID-en er det primære søkekriteriet for et produkt.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>ID-er for eksternt produkt (ID-er for kunde og leverandør)

For frigitte produkter kan du opprettholde varenumrene, varenavnene og varebeskrivelsene som kunden eller leverandøren bruker. Referansene vises på eksterne dokumenter, for eksempel salgsordrer, bestillinger, følgesedler og fakturaer. I den gjeldende versjonen av Supply Chain Management blir ikke eksterne referanser vist på kjernedriftssidene. Det eneste unntaket er leverandørens varenummer. Dette nummeret vises i dialogboksen **Produktinformasjon** hvis det er definert en standardleverandør for det frigitte produktet.

Du kan vedlikeholde ID-ene for eksternt produkt basert på frigitt produkt, frigitt produktvariant, kunde eller kundegruppe eller leverandør eller leverandørgruppe.

På siden **Frigitte produkter** gjør du ett av følgende.

- For kunder velger du **Ekstern varebeskrivelse** i gruppen **Beslektet informasjon** i fanen **Salg**.
- For leverandører velger du **Ekstern varebeskrivelse** i gruppen **Beslektet informasjon** i fanen **Kjøp**.

På siden **Eksterne varebeskrivelser** kan du knytte kundens eller leverandørens varenummer til et frigitt produkt. Denne tilknytningen må gjøres for hver juridiske enhet. Informasjonen nedenfor kan lagres. Etikettene er dessverre litt villedende i den gjeldende versjonen av Supply Chain Management. Disse etikettene kan imidlertid endres i en fremtidig versjon.

| Felt | Tilsvarende kundeinformasjon | Tilsvarende leverandørinformasjon |
|-------|------------------------------------|----------------------------------|
| Eksternt varenummer | Kundens varenummer | Leverandørens varenummer |
| beskrivelse | Navnet som kunden knytter til varen | Navnet som leverandøren knytter til varen |
| Ekstern varetekst | Kundens varebeskrivelse | Leverandørens varebeskrivelse |

Hvis mange kunder eller leverandører bruker de samme varenumrene (som for eksempel i forbindelse med en kjøpstilknytning eller en handelsgruppe), kan du opprette grupper med kunder eller leverandører som forenkler vedlikehold av ekstern produktinformasjon.

- For kundegrupper kan du gå til **Salg** &gt; **Oppsett** &gt; **Varer** &gt; **Ekstern varebeskrivelse** for å opprette og vedlikeholde gruppene og de tilknyttede varenumrene. Hvis du vil knytte kunder til en gruppe, kan du gå til **Kunder** &gt; **Kunder** &gt; **Alle kunder**, og deretter angir du en verdi i feltet **Vare – kundegruppe** i hurtigfanen **Standarder for salgsordre**.
- For leverandørgrupper går du til **Innkjøp og leverandører** &gt; **Oppsett** &gt; **Ekstern varebeskrivelsesgruppe** for å opprette og vedlikeholde gruppene og de tilknyttede varenumrene. Hvis du vil knytte leverandører til en gruppe, kan du gå til **Leverandører** &gt; **Leverandører** &gt; **Alle leverandører**, og deretter angir du en verdi i feltet **Vare – leverandørgruppe** i hurtigfanen **Bestillingsstandarder**.
 
## <a name="bar-codes"></a>Strekkoder

Hvis du vil bruke en strekkodeskanner til å identifisere produkter, må produkt-ID-en oppfylle kravene til strekkodestandarden som brukes. Strekkoder inneholder derfor ikke vanligvis råproduktnummeret, men et nummer som genereres for den valgte strekkodeteknologien. Du kan vedlikeholde flere strekkoder etter strekkodetype. Du kan også knytte samme strekkoden til flere produkter og deretter velge den faktiske aktive tilknytningen når du skanner en strekkode.

Før du definerer strekkoder, kan du definere ett eller flere strekkodeoppsett. Strekkodeoppsett kan hjelpe deg med å validere at strekkoder følger retningslinjene som er nødvendig, og at de kan derfor effektivt skrives ut og skannes. Du kan også vedlikeholde spesielle strekkoder for bestemte produkter.

Det anbefales at du bruker strekkodeoppsettet til vedlikehold av GTIN-koder (Global Trade Item Number) og IAN-koder (International Article Number).

Hvis du vil vedlikeholde strekkoder, velger du **Strekkoder** i gruppen **Lager** i fanen **Administrer lager** på siden **Frigitte produkter**.

## <a name="gtin-codes"></a>GTIN-koder

I e-handel er det viktig at alle parter snakker felles språk og refererer til produkter ved hjelp av et felles sett med identifikatorer. Derfor er noen bransjer avhengige av [GTIN](https://www.gs1.org/id-keys/gtin), som er et globalt varenummersystem som styres av GS1.

Vi anbefaler at du vedlikeholder GTIN som en strekkode. Du kan imidlertid også vedlikeholde den på siden **Vare – GTIN**. Hvis du vil åpne denne siden, velger du **GTIN-koder** i gruppen **Lager** i fanen **Administrer lager** på siden **Frigitte produkter**. Legg merke til at GTIN ikke vedlikeholdes som et globalt nummer. I stedet vedlikeholdes det basert på juridisk enhet.

I Supply Chain Management kan du definere varianter av emballasjen i lageroperasjonene ved å definere bestemte måleenheter. En vare kan for eksempel lagres i deler, i pakker på seks, i brett på 18 eller i hele paller. En bestemt måleenhet defineres for hver av disse emballasjevariantene. GTIN er vanligvis relatert til emballasjeenheten for et produkt, og derfor kan du vedlikeholde flere GTIN-koder per produkt og enhet på siden **Vare – GTIN**. Du kan imidlertid bruke den samme GTIN-koden mer enn én gang for ulike varer eller produktvarianter for en juridisk enhet.

Hvis du vil vedlikeholde **GTIN-koder**, velger du **GTIN** i gruppen **Lager** i fanen **Administrer lager** på siden **Frigitte produkter**.

## <a name="external-codes"></a>Eksterne koder

Eksterne koder kan defineres for mange enheter. Du kan for eksempel definere eksterne koder som identifiserer produkter og frigitte produkter. Disse eksterne kodene kan brukes til å knytte statistiske koder eller mva-koder til frigitte produkter og varianter av frigitte produkter. Eksterne koder defineres av juridisk enhet og kodetype. De må være unike basert på juridisk enhet, kodetype og tabellreferanse.

Det finnes dessverre ingen standardfunksjonalitet som lar deg søke etter produkter etter eksterne koder.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Dataenheter som brukes til å importere og eksportere produkt-ID-er

| Entitynavn | Import-ID-er | Eksport-ID-er | Kommentarer |
|-------------|--------------------|--------------------|----------|
| Produkter V2 | Produktnummer, produktsøkenavn, produktnavn, produktbeskrivelse | Produktnummer, produktsøkenavn, produktnavn, produktbeskrivelse | Avhengig av innstillingene for enheten og nummerserien for produktnummeret, kan produktnummeret opprettes automatisk under import. |
| Produktvarianter | Produktnummer, produktsøkenavn, produktnavn, produktbeskrivelse | Produktnummer, produktsøkenavn, produktnavn, produktbeskrivelse | Avhengig av produktterminologimalen, kan produktnummeret opprettes automatisk under import. Du kan imidlertid importere et hvilket som helst unikt produktnummer, og det produktnummeret trenger ikke følger samme struktur som produktterminologimalene. |
| Produktoversettelser | Produktnavn, produktbeskrivelse | Produktnavn, produktbeskrivelse | Denne enheten overskriver alle språk. Legg merke til at når navnet på eller beskrivelsen av en juridisk enhets primærspråk overskrives, endres navnet og beskrivelsen av selve produktet. |
| Frigitt produktoppretting V2 | Varenummer, produktnummer, varesøknavn| Varenummer, produktnummer, varesøknavn, produktsøknavn, produktnavn | Denne enheten kan være utfordrende når nummerserier brukes ved oppretting av nye frigitte produkter. Både nummerserien **Varenummer** og **Produktnummer** har en påvirkning. Nummerserien **Varenummer** er imidlertid per juridiske enhet, mens nummerserien **Produktnummer** er global. Derfor anbefales det ikke at du bruker nummerserien **Varenummer** når du distribuerer nye frigitte produkter. Når enheten brukes til å frigi et eksisterende produkt, må produktnummeret selvsagt angis i enheten. Hvis du vil ha mer informasjon, kan du se delen Produkt- og varenummerserier i dette emnet. |
| Frigitte produktvarianter | Varenummer, produktdimensjoner, produktnummer | Produktnummer, produktsøkenavn, produktnavn, produktbeskrivelse, produktdimensjoner | På samme måte som enheten **Produktvarianter** kan denne enheten brukes til å opprette nye produkter som følger produktterminologimalen eller bruker egne produktnumrene for varianten. |
| Ekstern varebeskrivelse for kunder | Kundens varenummer, varenavn for kunde, kundebeskrivelse, kundekonto | Kundens varenummer, varenavn for kunde, kundebeskrivelse, kundekonto | En gruppe av kunder (for eksempel en kjøpertilknytning) kan samles i én gruppe ved hjelp av enheten **Eksterne kundegrupper for beskrivelse av vare**. |
| Ekstern varebeskrivelse for leverandører | Leverandørens varenummer, varenavn for leverandør, leverandørbeskrivelse, leverandørkonto | Leverandørens varenummer, varenavn for leverandør, leverandørbeskrivelse, leverandørkonto | En gruppe av leverandører (for eksempel en salgstilknytning eller bransjeorganisasjon) kan samles i én gruppe ved hjelp av enheten **Eksterne leverandørgrupper for beskrivelse av vare**. |
| Varestrekkode | Strekkode | Strekkode | Legg merke til at under import må du henvise til et strekkodeoppsett som er definert i systemet. De importerte strekkodereferansene valideres mot dette strekkodeoppsettet, og de avvises hvis strekkodene ikke oppfyller kravene som er definert i dette strekkodeoppsettet. |
| Eksterne koder for frigitte produkter | Ekstern kode | Ekstern kode, eksterne kodeklasser, varenummer | Eksterne koder vises etter juridisk enhet. For import må du referere til en definerte kodeklasse. Importer kodeklassene ved hjelp av enheten **Eksterne kodeklasser for frigitte produkter**. |
| Eksterne koder for frigitte produktvarianter | Ekstern kode | Ekstern kode, eksterne kodeklasser, varenummer, produktdimensjoner | Eksterne koder vises etter juridisk enhet. For import må du referere til en definerte kodeklasse. Importer kodeklassene ved hjelp av enheten **Eksterne kodeklasser for frigitte produkter**. Denne enheten refererer til produktvarianter basert på varenummeret og produktdimensjonene. |
| Eksterne koder for utgitte produktvarianter etter produktnummer-ID | Ekstern kode | Ekstern kode, eksterne kodeklasser, produktnummer | Eksterne koder vises etter juridisk enhet. For import må du referere til en definerte kodeklasse. Importer kodeklassene ved hjelp av enheten **Eksterne kodeklasser for frigitte produkter**. Denne enheten refererer til produktvarianter basert på produktnummeret for varianten. (Fra den neste hovedversjonen) |
| GTIN | Gjelder ikke her | Gjelder ikke her | Det er for øyeblikket ingen bestemt enhet som brukes til å importere og eksportere GTIN-koder. Det anbefales at du i stedet bruker enheten **Varestrekkode**. |
| Enhet for ID for Common Data Service for produktenhet | Gjelder ikke her | Varenummer, varesøknavn, produktsøknavn, leverandørens varenummer, kundens varenummer, eksterne koder, GTIN-koder, strekkoder | Denne enheten konsoliderer alle identifikatorer til én datamodell, slik at et grensesnitt kan brukes til å eksportere alle identifikatorer og deres tilknyttede typer. Bruk enheten **Kode for produktenhets-ID** til å eksportere ID-kodene og beskrivelsene. Bruk enheten **Omfang for produktenhets-ID** til å eksportere mer områdeinformasjon til en identifikator, for eksempel parten, den juridiske enheten, antallet eller enheten. |

### <a name="product-and-item-number-sequences"></a>Nummerserier for produkt og vare

Du kan definere to ulike nummerserier:

- Nummerseriene for **Produktnummer** for det globale produktnummeret
- Nummerserien **Varenummer** for varenummeret per juridiske enhet

> [!NOTE]
> Du må bruke varenummeret som en egen identifikator bare når du overfører andre juridiske enheter fra forskjellige kilder med ulike tallsystemer. Du bør alltid bruke en produkt-ID som er unik på tvers av alle juridiske enheter. Derfor bør du sette alternativet **Manuell** til **Ja** for nummerserien **Varenummer**. På denne måten følger varenummeret produktnummeret ved oppretting. Hvis Supply Chain Management ikke er det ledende systemet for nye produktnumre, bør du sette alternativet **Manuell** til **Ja** for både nummerserien **Varenummer** og **Produktnummer**.

Når du bruker enheten **Frigitt produktoppretting V2** til å opprette produkter, kan flere innstillinger påvirke hvordan nummerseriene brukes til å opprette produktnummeret og varenummeretet:

- Innstillinger for nummerserien **Produktnummer**
- Innstillinger for nummerserien **Varenummer**
- Tilordningen for varenummeret 
- Tilordningen for produktnummeret

Tabellen nedenfor gir en oversikt over resultatene av import og manuell oppretting når bestemte kombinasjoner av nummerserien og feltinnstillingene for tilordning ble brukt.

| Nummerserie for produktnummer | Nummerserie for varenummer | Tilordning av varenummeret | Tilordning av produktnummeret | Resultat av enhetsimport | Resultat av manuell oppretting | Konklusjon |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Manuell = Nei | Manuell = Nei | Ingen tilordning | Ingen tilordning | Produktnumre bruker nummerserien **Produktnummer**. Varenumre bruker nummerserien **Varenummer**. | Produktnumre bruker nummerserien **Produktnummer**. Varenumre bruker nummerserien **Varenummer**. | Med denne konfigurasjonen vil produktnumre følge produktnummerserien, og varenumre vil følge varenummerserien. Denne konfigurasjonen vil imidlertid ikke fungere hvis det er mer enn en vare (rad) som skal importeres. |
| Manuell = Nei | Manuell = Ja | Autogenerer | Ingen tilordning | Både produktnumre og varenumre bruker nummerserien **Varenummer**. | Både produktnumre og varenumre bruker nummerserien **Produktnummer**. | Både produktnumre og varenumre følger produktnummerserien. Dette er den anbefalte fremgangsmåten for å importere bulkprodukter med dataenheten Frigitt produktoppretting V2. |
| Manuell = Nei | Manuell = Ja | Ingen tilordning | Ingen tilordning | Både produktnumre og varenumre bruker nummerserien **Produktnummer**. | Både produktnumre og varenumre bruker nummerserien **Produktnummer**. | Både produktnumre og varenumre bruker produktnummerserien. Denne konfigurasjonen vil imidlertid ikke fungere hvis det er mer enn en vare (rad) som skal importeres. |
| Manuell = Ja | Gjelder ikke | Gjelder ikke | Autogenerer | Du får følgende feilmelding: "Finner ikke nummerserien." | I henhold til nummerserien **Varenummer** | Denne innstillingen støttes ikke for import. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Produktenhets-ID (Eksporter alle produkt-ID-er)

Modellen for produktenhets-ID ble opprettet for å aktivere versjon 1.0 av CDS til å bli klargjort med alle identifikatorer som brukes til å referere til et produkt. For å forenkle denne oppgaven, kan alle identifikatorer samles i én tabell for globale identifikatorer, slik at de kan eksporteres som én modell. Vær oppmerksom på at denne versjonen av CDS ikke bruker modellen for produkt-ID-er. Derfor har enheten **Enhet for ID for Common Data Service for produktenhet** og denne prosessen begrenset praktisk bruk og vil sannsynligvis bli endret i fremtiden.

Tabellen for produkt-ID er en global tabell som fylles ut fra alle referansetabeller for den juridiske hovedenheten via en gjentakende satsvis jobb. Du må velge en juridisk enhet og et hierarki for produktkategori som definisjonen av hovedomfanget for globalt produkt. Generering av tabellen for global produkt-ID er begrenset til produkter som er frigitt til den valgte juridiske enheten, og produkter som er medlemmer av produkthierarkiet som velges for rollen **Common Data Service** i produktets kategorihierarki.

Denne prosessen forutsetter at produktets hoveddata først og fremst opprettholdes i én sentral juridisk enhet. (Denne juridiske enheten kan imidlertid være en virtuell juridisk enhet som brukes bare til å vedlikeholde globale hoveddata.)

Gjør følgende for å konfigurere miljøet.

1. Velg kategorihierarkiet for CDS. Opprett en ny tilknytning på siden **Rolletilknytninger for kategorihierarki** hvis ingen hierarkier er knyttet til rollen **Common Data Service**. Velg rollen **Common Data Service**, og knytt deretter til kategorihierarkiet som representerer produktporteføljen som skal synkroniseres til CDS.
2. Velg den juridiske enheten for globale produkthoveddata. Velg hovedfirmaet der produkt- og vare-ID-ene hovedsakelig vedlikeholdes, på siden **Parametere for produktinformasjonsbehandling** i fanen **Produktattributter**.
3. Definer ID-kodetypene og koder som skal eksporteres. Gå til **Produktinformasjonsbehandling** &gt; **Oppsett** &gt; **Produkt-ID-koder**. Hvis du vil generere ID-kodetypene, velger du **Generer koder**. En kodetypeoppføring genereres for hver type for ID-en som finnes i den valgte juridiske enheten.

    Vær oppmerksom på at det genereres en kodetype for hvert strekkodeoppsett for strekkoder. For eksterne koder genereres det en kodetype for hver eksterne kodeklasse.

    Nå kan du vedlikeholde listen over kodetypene. Du kan endre koden, navnet og beskrivelsen. Du kan også slette kodetyper. Kodetypene du sletter, blir ikke brukt til å fylle ut tabellen for global produktenhets-ID.

4. Når du er ferdig med å definere kodetypene for produkt-ID, kan du opprette identifikatorene i den globale tabellen ved å starte jobben **Opprett produktenhets-ID-er** på siden **Koder for produktenhets-ID**. Du bør kjøre denne jobben som en satsvis jobb. Denne jobben må defineres som en periodisk satsvis jobb slik at tabellen fylles ut i henhold til nye oppføringer.

Nå kan du bruke dataenhetene **Enhet for ID for Common Data Service for produktenhet**, **Kode for produktenhets-ID** og **Omfang for produktenhets-ID** til å eksportere identifikatorene for alle målsystemer.

## <a name="related-topic"></a>Relaterte emne

[Søke etter produkter og produktvarianter under ordreregistrering](search-products-product-variants.md)
