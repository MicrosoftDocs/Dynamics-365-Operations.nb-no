---
title: Komme i gang med leasing av aktiva
description: Dette emnet beskriver funksjonen for leasing av aktiva og går gjennom fremgangsmåten for å opprette leasing av aktiva og vise informasjon for leasingavtalene.
author: moaamer
manager: Ann Beebe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b4f1bdf74dc5319f0b3ba145969b064ad33d5010
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229604"
---
# <a name="asset-leasing-get-started"></a>Komme i gang med leasing av aktiva

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjonen for leasing av aktiva og går gjennom fremgangsmåten for å opprette leasing av aktiva og vise informasjon for leasingavtalene. Emnet definerer også terminologien som brukes i brukergrensesnittet og i dokumentasjonen. Leasing av aktiva er en avansert funksjon for behandling, sporing og automatisering av mindre, økonomiske transaksjoner for leasede aktiva i Microsoft Dynamics 365 Finance. Leasing av aktiva overholder internasjonale regnskapsstandarder (IFRS 16) og amerikanske GAAP-standarder (ASC 842). Leasing av aktiva registrerer og behandler informasjon om leasing og beregner journaloppføringer gjennom livssyklusen til leasingen fra innledende gjenkjenning, månedlige journaloppføringer, til skader og avslutning av leasingen. Leasing av aktiva integreres sømløst med andre komponenter i Dynamics 365 Finance, inkludert anleggsmidler, leverandører og økonomimodulen.

Hvis du vil ha mer informasjon om regnskapsstandarder, se standard dokumentasjonen for IFRS 16 og US GAAP ASC 842.

## <a name="asset-leasing-elements"></a>Elementer i leasing av aktiva
Diagrammet nedenfor viser hovedelementene i forretningsprosessen for leasingavtaler.

[![Elementer i leasing av aktiva](./media/overview-01.png)](./media/overview-01.png)

Leasing av aktiva inneholder følgende hovedkomponenter:

- **Leieavtale** – Utleieren eier aktivaet og blir enig med leier om utleie av et anleggsmiddel for en bestemt periode i bytte for periodisk leiebetaling. I tillegg til den juridiske kontrakten mellom utleier og leier, inneholder leieavtalen administrasjonsbeslutninger, for eksempel sannsynligheten for å gjennomføre et fornyelsesalternativ og overføring av eierskap.

- **Beregning og klassifisering av leieavtale i henhold til regnskapsstandard** – Beregningen og klassifiseringen av leieavtalen identifiserer regnskapsstandarden som skal brukes i den første og den etterfølgende målingen, i tillegg til klassifiseringstesten som avgjør hva leietypen skal være. En leieavtale kan være en finansiell leie, en gjeldende leie, en kortsiktig leie eller en lavverdileie. Systemet beregner også nåverdien av fremtidige, minste leiebetalinger for vurdering og klassifisering.

- **Leietransaksjoner** – Leie av anleggsmidler støtter den opprinnelige anerkjennelsen av anleggsmiddelets leie i balansen, i tillegg til etterfølgende målinger for leieavtaler i balanse eller leie utenfor balanse. Den opprinnelige anerkjennelsestransaksjonen måler nåverdien av fremtidig minste leiebetaling. Disse dataene brukes til å fastslå verdien for første bruksrettseiendel og leieforpliktelse, som påvirker organisasjonens balanse. De etterfølgende målingene av månedlige leietransaksjoner innebærer akkumulering av rente for leieforpliktelsen, noe som øker leieforpliktelsen. Den måler også avsetningen av leiebetalinger som reduserer leieforpliktelsen, og som deretter vil bli betalt til utleier. Målingen omfatter også amortisering av bruksrettseiendelen.

  For leieavtaler utenfor balanse vil systemet beregne den lineære leieutgiften med hensyn til hva som er minst: den økonomiske levetiden til eiendelen eller leieavtalen. Leiejusteringer måler kontraktsendringer, for eksempel en leieutvidelse eller forlengelse, og transaksjonen for verdiforringelsen som bruker bruksrettseiendelen for kostnader som er fradragsberettiget.

  Leie av anleggsmidler integreres med økonomimodulen for å sikre at alle posterte leietransaksjoner oppdaterer kontoplanen din. Leie av anleggsmidler integreres med leverandører for å spore utleierfakturaer i leverandør og ta fremtidige betalinger derfra. Ved hjelp av integrering med anleggsmidler, kan du spore leieavtaler i journalen for anleggsmidler og postere transaksjoner for bruksrettseiendeler, inkludert innledende gjenkjenning, avskrivning og verdiforringelse av anleggsmiddelet, i anleggsmidler.   

## <a name="asset-leasing-components"></a>Komponenter for leie av anleggsmiddel 
Leie av anleggsmidler tilordner leieinformasjon, betalingsplaner, start- og sluttdatoer og betalingsfrekvensen. Den vil også automatisere beregninger for nåverdi, månedlige leiebetalinger, rente og leieamortisering. Systemet utfører klassifiseringstester for leie, avhengig av konfigurasjonen. Systemet oppretter og posterer også de tilsvarende leietransaksjonene, som er basert på rammeverket som er definert av regnskapsstandarden du følger.

Diagrammet nedenfor viser leietablået, leieavtalen, beregnet betalingsplan, klassifiseringstestene for leieavtaler og leietablåer, og de tilsvarende regnskapstransaksjonene.

[![Leie, leietablå og betalingsplan](./media/overview-02.png)](./media/overview-02.png)

- **Leietablå** – Leieavtaler omfatter all informasjon om leiekontrakt, for eksempel leievilkår, virkelig verdi og leiebetalinger. Det inneholder også regnskapsstandarden du følger, leietype og terskler som vurderes i klassifiseringstester for leie. Leietablået inneholder også leietransaksjonene som er postert til økonomimodulen. 
  
- **Leie** – Leieavtalen inneholder informasjon om leieavtaler for anleggsmidler som representerer grunnlaget for leien av anleggsmidler, kilde for leieinformasjon er leiekontrakt og administrasjonsbeslutninger som begge gjøres utenfor Dynamics 365 Finance. Anleggsmiddelets virkelige verdi er prisen som ville bli betalt for et anleggsmiddel i en transaksjon på målingsdatoen. Denne verdien kan avhenge av type anleggsmiddel, markedsforhold og andre kriterier som kan tas i med i vurderingen. Virkelig verdien for anleggsmiddelet vil bli tatt hensyn til i oppsettet for klassifiseringstesten.

- **Levetid for anleggsmiddel** – Dette representerer de gjenstående periodene for levetiden til et anleggsmiddel, fra startdatoen for leieavtalen. Levetiden til et anleggsmiddel vil bli tatt hensyn til i oppsettet for klassifiseringstesten. Den er forskjellig fra levetiden som er definert i anleggsmidler.

- **Trinnvis lånerente** – Dette er rentesatsen som vil bli brukt til å beregne nåverdi. Systemet vil bruke den implisitte satsen hvis den er definert i leiedataene, til å beregne nåverdien av leiebetalingene. Hvis den implisitte satsen ikke er definert, vil systemet bruke den trinnvise lånerenten.

- **Annuitetstype** – Dette er leiebetalingen som forfaller enten i begynnelsen av betalingsperioden eller på slutten av perioden. Dette kan være forskuddsbetaling eller annuitetsforfall (i begynnelsen av perioden for leiebetaling), eller vanlig annuitet (på slutten av perioden for leiebetaling).

  Den første måneden vil bli ansett som periode null for forskuddsbetaling. Den første måneden blir ansett som periode én for etterskuddsbetaling.

- **Sammensetningsintervall** – Dette representerer antall perioder som renten har i løpet av året. Dette kan være månedlig (12 perioder per år), kvartalsvis (4 perioder per år), halvårs (2 perioder per år) eller årlig (1 periode per år). Antallet perioder vil bli vurdert i beregning av nåverdien.

- **Startdato** – Dette er datoen som utleier gjør anleggsmiddelet tilgjengelig for bruk av leier. Alle beregninger og transaksjoner for leieavtaler baseres på startdatoen. Startdatoen må være i begynnelsen av en periode (den første i måneden) for å sikre nøyaktigheten til etterfølgende beregninger. Du kan bruke feltet **Kontraktsdato for signering** til å angi den faktiske datoen da kontrakten ble signert.

- **Leieperiode** – Dette er lengden på leieperioden i måneder.

> [!NOTE] 
> Definisjonen av leieavtalen er basert på antall perioder, eller intervaller, i betalingsplanlinjene. Det definerte antallet intervaller vil bli konvertert til måneder.

- **Betalingsplanlinje** – Dette registrerer leiebetalinger per periode. Det angir også om en fornyelsesperiode vil bli gjennomført og inkludert i den opprinnelige målingen for bruksrettseiendelen og leieforpliktelsen. Du kan definere startdatoen for forfallsbetalinger for leie, og periodeintervallene som representerer lengden på leieavtalen, som kan være dager, måneder eller år.

- **Betalingsfrekvens** – Dette angir om betalingen er månedlig, kvartalsvis, halvårlig eller årlig. Sluttdatoen beregnes automatisk basert på startdatoen og angitt antall perioder.

- **Betalingsplan** – Dette er den beregnede nåverdien, basert på hvor lang tid som dekkes av de leiebetalingene, beløpet for betalingene, sammensetningsperiodene og annuitetstypen.

- **Perioder** – Dette er leieperiodene som gjenspeiler den sammensetningen internt og annuitetstypen. Sammensetningsintervallet bestemmer hvordan perioder skal deles. Du kan angi følgende sammensetningsintervaller:

  - Månedlig, 12 perioder per år
  - Kvartalsvis, 4 perioder per år
  - Hvert halvår, 2 perioder per år
  - Årlig, 1 perioder per år

Den første perioden starter med perioden null, hvis annuitetstypen er annuitetsforfall. Hvis ikke starter den første perioden med perioden en, hvis annuitetstypen er etterskuddsbetaling.

- **Måneder** – Dette angir antall kalendermåneder i forhold til leieavtalen. Betalingsbeløpet er det forfalte beløpet som er definert i betalingsfrekvensen. Den beregnede nåverdien er den nåværende verdibaserte leiebetalingen per periode, sammensetningsintervallene og den trinnvise lånerenten.

> [!NOTE] 
> Nåverdien beregnes basert på kontantstrømligningen for rabatten.

- **Bøker** – Dette er det forhåndskonfigurerte oppsettet som vil bli knyttet til hver leieavtale. Tablået definerer den brukte regnskapsstandarden, leietypene og terskelen som brukes som grunnlag for klassifiseringstestene. Klassifiseringstester brukes til å angi leasing leietypen automatisk.

- **Regnskapsrammeverk** – Dette viser den valgte regnskapsstandarden, enten IFRS 16 og ASC 842, som du støtter. Regnskapsstandarden defineres for tablået som er knyttet til leieavtalen. Regnskapsstandarden bestemmer hvilke finanskontoer som er angitt i posteringsprofilen.

- **Leietyper** Dette angir hvilke av de to typene leieavtaler som skal brukes, enten en finansiell leie eller en gjeldende leie. Under en finansiell leie blir risikoer og belønninger som er knyttet til det leide anleggsmiddelet, overført til leier. Under en gjeldende leie blir risikoer og belønninger som er knyttet til det leide anleggsmiddelet, forbli hos utleier. Et tredje alternativ er en automatisk identifikasjon av leietypen, enten finansiell eller gjeldende, basert på de definerte tersklene i tablået. Denne automatiske identifikasjonen blir utført under testen for omklassifisering av leien.

- **Terskler** – Dette brukes i testene for leieklassifisering for å finne ut om anleggsmiddelet er klassifisert som ett av følgende:

  - **Leieavtale** – Dette er prosentdelen av levetiden som skal brukes i klassifiseringstesten. Systemet klassifiserer leieavtalen som finansiell hvis leietypen er satt til automatisk, og hvis leieperioden for anleggsmiddelets levetid er større enn eller lik prosentdelen som er definert her.

  - **Nåverdi** – Dette er prosentdelen av anleggsmiddelets virkelige verdi som skal brukes i klassifiseringstesten. Systemet klassifiserer leieavtalen som finansiell hvis leietypen er satt til automatisk, og hvis nåverdien for fremtidige leiebetalinger for anleggsmiddelets virkelige verdi er større enn eller lik prosentdelen som er definert her.

  - **Korttidsleie** – Hvis leieavtalen er mindre enn eller lik den definerte verdien, klassifiseres leieavtalen som korttidsleie.

  - **Lavverdi** – Hvis den virkelige verdien for anleggsmiddelet er mindre enn eller lik den definerte verdien, klassifiseres leieavtalen som lavverdileie.

  - **Leieklassifisering og transaksjoner** Leieklassifiseringen er en automatisert prosess for å klassifisere leieavtaler basert på definerte terskler i andre tablåer enn klassifiseringstestkriterier for å identifisere om leieavtalen er en finansiell leie, gjeldende leie, korttidsleie eller lavverdileie. Dette brukes også til å identifisere om prosessen for utsatte leie etterfølges.

Klassifiseringstestene omfatter overføring av eierskap, kjøpsalternativ, leieperiode, nåverdi og unikt anleggsmiddel. Diagrammet nedenfor illustrerer klassifiseringtesten for leien.

[![Klassifiseringstest for leie](./media/overview-03.png)](./media/overview-03.png)

Hver leietype håndterer regnskap forskjellig for ulike leietransaksjoner. Transaksjonene omfatter innledende gjenkjenning, renteutgift, forfallsbetaling for leie og leieavskrivning, og de er basert på regnskapsstandardene du følger (IFRS 16 eller ASC 842). Finanskontoer defineres under leieposteringsprofilen for hver transaksjonstype og regnskapsrammeverk.

## <a name="asset-leasing-transactions"></a>Transaksjoner for leie av anleggsmiddel

#### <a name="initial-recognition"></a>Opprinnelig føring 
Den opprinnelige gjenkjenningen av et leid anleggsmiddel bruker den beregnede nåverdien, slik at den kan rapporteres i balansen. Regnskapsoppføringen for denne genereres automatisk. Denne transaksjonen debiterer kontoen for bruksrettseiendelen, og krediterer kontoen for gjeldende leieforpliktelse. Hvis et anleggsmiddel er knyttet til leieavtalen, vil den innledende gjenkjenningsoppføringen gjenspeiles som anleggsmiddelanskaffelse. I dette scenariet må du definere en posteringsprofil for anleggsmiddel som skal posteres til kontoen for bruksrettseiendelen. 

> [!NOTE]
> Gjeldende leier støttes bare av amerikansk GAAP ASC 842.

|     Type                                          |     Debet                     |     Kreditt                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Gjeldende   leie i henhold til  amerikansk GAAP              |     Bruksrettseiendel      |     Gjeldende   leieforpliktelse       |
|     Finansiell leie   i henhold til IFRS og amerikansk GAAP        |     Bruksrettseiendel      |     Gjeldende   leieforpliktelse       |

#### <a name="lease-liability-amortization-interest-expense"></a>Nedbetaling av leieforpliktelse (renteutgift) 
Renten for en leieavtale gjenkjennes ved å beregne renter for leieavtalens startsaldo, leiebetaling for periode, lånerente og perioder for sammensetningsintervall per år. Rentebeløpet øker kontoen for gjeldende leieforpliktelse ved å kreditere den, noe som vil bli gjenspeilet i organisasjonens balanse. Transaksjonen inkluderer også en debetoppføring til kontoen for renteutgifter, som gjenspeiles på resultatregnskapet for finansielle leier, og til kontoen for leieutgifter for gjeldende leier.

|     Type                                          |     Debet                     |     Kreditt                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Oppføring for gjeldende leieforpliktelse i henhold til amerikansk GAAP ASC 842    |     Renteutgift          |     Driftsleiegjeld         |
|     Oppføring for finansiell leieforpliktelse i henhold til IFRS og amerikansk GAAP      |     Renteutgift          |     Leiegjeld for finans           |

#### <a name="accrued-lease-payment"></a>Påløpt leiebetaling
En påløpt leiebetaling gjenkjennes som en fremtidige leiebetaling som forfaller til behandling som en betalingstransaksjon fra bank- eller kassakontoen. Forfalt leiebetaling reduserer leieforpliktelsen ved å debitere kontoen for leieforpliktelse mot en underfinans for leverandør i tilfelle det er definert en leverandør, eller postering av kreditsiden til en gjeldsfinanskonto. Betalingen utføres da mot leverandør eller gjeld.

|     Type                                          |     Debet                     |     Kreditt                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Gjeldende   leie i henhold til  amerikansk GAAP              |  Driftsleiegjeld    |   Leverandørgjeld (underfinans) / gjeld  |
|     Finansiell leie   i henhold til IFRS og amerikansk GAAP        |  Leiegjeld for finans      |   Leverandørgjeld (underfinans) / gjeld  |

#### <a name="asset-depreciation"></a>Avskrivning av anleggsmiddel
Bruksrettseiendelen avskrives over med hensyn til det som er minst – anleggsmiddelets levetid eller leieperioden. Metoden for beregning av avskrivning for amerikansk GAAP (ASC 842) er basert på forskjellen mellom leieavtalen for den lineære leieutgiften og rentebeløpet. Rente på finansielle leier beregnes ved å bruke en standard lineær metode. Leieavskrivningen påvirker resultatregnskapet ved å debitere renteutgifter. Balansen påvirkes av den akkumulerte kontoen for bruksrettseiendelen for finansielle leier. For gjeldende leier krediterer avskrivningen kontoen for leieutgifter. Hvis leieavtalen er koblet til et anleggsmiddel, blir avskrivningstransaksjonene bare utført fra anleggsmiddelmodulen. 

|     Type                                          |     Debet                     |     Kreditt                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Gjeldende   leie i henhold til  amerikansk GAAP              |  Leieutgift                |   Akkumulert avskrivning for bruksrettseiendel     |
|     Finansiell leie   i henhold til IFRS og amerikansk GAAP        |   Utgift for avskrivning av bruksrettseiendel   |   Akkumulert avskrivning for bruksrettseiendel    |

#### <a name="short-term-lease"></a>Kortsiktig leie
En korttidsleie gjenkjennes som en utgift, noe som vil påvirke en organisasjons resultatregnskap. Den genererte leiebetalingen som forfaller, vil debitere kontoen for leieutgifter og kreditere kontoen for gjeld eller underfinanskontoen for leverandør.

|     Type                                          |     Debet                     |     Kreditt                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Oppføring for korttidsleie i henhold til IFRS og amerikansk GAAP     |  Leieutgift                |   Leverandørgjeld (underfinans) / gjeld  |

#### <a name="low-value-lease"></a>Lavverdileie
En lavverdileie gjenkjennes som en utgift som vil påvirke organisasjonens resultatregnskap. Den genererte leiebetalingen som forfaller, vil debitere kontoen for leieutgifter og kreditere kontoen for gjeld eller underfinanskontoen for leverandør.

|     Type                                          |     Debet                     |     Kreditt                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Oppføring for lavverdileie i henhold til IFRS og amerikansk GAAP      |  Leieutgift                |   Leverandørgjeld (underfinans) / gjeld  |


#### <a name="index-revaluation"></a>Revaluering av indeks
Dette er kontoen for leie av anleggsmidler for variable leiebetalinger målt av en indeksrente. Endringer i leiebetalinger som forårsakes av svingninger i indeksrenten, utgjør en leiejustering i henhold til IFRS 16. Leieforpliktelsen og bruksrettseiendelene vil bli justert for til kontoen for de nye betalingene. 

|     Type                                          |     Debet                             |     Kreditt                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Revalueringen av indeksoppføring i henhold til IFRS i tilfelle økning  |  Bruksrettseiendel       |   Driftsleiegjeld |
|   Revalueringen av indeksoppføring i henhold til IFRS i tilfelle reduksjon  |  Driftsleiegjeld  |   Bruksrettseiendel      |

Når betalinger endres på grunn av en endring i indeksrenten, vil bare de variable betalingene endres med mindre det er flere endringer i kontantstrømmene, for eksempel en endring i leievilkårene som er knyttet til rentesatser i henhold til amerikansk GAAP ASC 842.

#### <a name="lease-adjustment"></a>Leiejustering
Leie av anleggsmiddel gjør det mulig for å justere leieavtaler hvis leievilkårene endres, leieavtalen utvides, eller hvis det er andre omstendigheter der en leieavtale krever justering. Leiejusteringer posteres for å øke eller redusere bruksrettseiendel eller leieforpliktelse. Justeringsprosessen tar overførte sluttsaldoer med nedbetaling av gjeld og anleggsmiddelsaldo på justeringsdatoen. Når en leieavtale er koblet til et anleggsmiddel, posteres justering for bruksrett med ID-en som er tilordnet i anleggsmidler. 

|     Type                                          |     Debet                             |     Kreditt                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Oppføring for leiejustering for IFRS og US GAAP i tilfelle økning     |  Bruksrettseiendel       |   Driftsleiegjeld |
|   Oppføring for leiejustering for IFRS og US GAAP i tilfelle reduksjon     |  Driftsleiegjeld  |   Bruksrettseiendel      |


#### <a name="lease-impairment"></a>Verdiforringelse for leieavtale
Dette representerer overføring av saldoreduksjon for bruksrettseiendelen. Identifiser beløp for verdiforringelse, transaksjonsdato og perioder som gjenstår. Det gjenstående bruksrettseiendelen vil bli nedbetalt lineært. Logikken for verdiforringelse for leieavtale vurderer overføringsverdi for anleggsmiddelet, som finnes i tidsplanen for avskrivning av anleggsmiddelet.  

|     Type                                          |     Debet                             |     Kreditt                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Oppføring for verdiforringelse for IFRS og amerikansk GAAP           |  Verdiforringelsesutgift                   |    Bruksrettseiendel     |

>[!NOTE]
> Hvis leieavtalen er koblet til et anleggsmiddel, skal verdiforringelsen for anleggsmiddelet posteres fra anleggsmidler fordi avskrivning for anleggsmiddel kjøres fra anleggsmiddelmodulen.

**Dobbel valuta** Leietransaksjoner kan posteres i en annen valuta enn regnskaps- og rapporteringsvalutaen. Valutakursen defineres i økonomimodulen på startdatoen. Du kan endre valutakursene ved å sette **Fast kurs**-feltet til **Ja** når du oppretter leieavtalen. Når du angir leietransaksjoner, vil den innledende gjenkjenningen og de etterfølgende avskrivningstransaksjonene bruke valutakursen fra og med startdatoen. De etterfølgende betalingene og rentetransaksjonene vil bruke gjeldende aktive valutakurs. 

## <a name="create-an-asset-lease"></a>Opprette en leieavtale for anleggsmiddel
Fullfør fremgangsmåten nedenfor for å opprette en ny leieavtale. 

1. Hvis du vil **Leie av anleggsmiddel**, må du aktivere den i arbeidsområdet **Funksjonsbehandling**. Fra arbeidsområder **Funksjonsbehandling** velger du **Alle**, slik at alle funksjonene vises på siden. Velg **Leie av anleggsmiddel**, og velg deretter **Aktiver nå**.
2. Gå til **Leie av anleggsmiddel > Felles > Leiesammendrag**. Angi feltene nedenfor i hurtigfanen **Generelt**. 
   - **Leiedetaljer**
   - **Aktivalevetid (måneder)**
   - **Leiegruppe**
   - **Trinnvis lånesats (%)**
   - **Sammensetningsintervall**
   - **Annuitetstype**
   - **Valuta.**
   - **Iverksettelsesdato**

3. Gå til hurtigfanen **Betalingsplanlinjer** og angi en betalingslinje, og velg deretter **Opprett tidsplaner**.

4. Velg **Bøker**. 

5. Bytt til hurtigfanen **Generelt**. **Første bruksrettseiendel** og **Leieforpliktelse** beregnes. 

6. Gå til hurtigfanen **Klassifiseringstest for leie** for å kontrollere verdien i feltet **Leietype**. 

   Den automatiske **leietypen** klassifiseres basert på kriteriene som er definert på siden **Tablåer**.

7.  Gå til **Betalingsplan** under **Funksjon**-delen.  

   Siden **Betalingsplan** viser en liste over fremtidige betalingsplaner for en leie-ID. Velg **Bekreft plan** for å postere transaksjonene for **opprinnelige gjenkjenning**. 

[![Funksjon for opprinnelig gjenkjenning](./media/overview-13.png)](./media/overview-13.png)

8. Velg **Opprinnelig gjenkjenning** for å opprette en opprinnelig føringsjournal. 

9. Velg **Journaler for leie av anleggsmidler** for å postere den opprinnelig gjenkjente transaksjonen. 

   Fra betalingsplanen kan du åpne en detaljert side med en oversikt over transaksjonene for bruksrettseiendelen. 
 
   **Nedbetalingsplan for leieforpliktelse** viser rentebeløpet som beregnes for hver periode.
   
10. Opprett journalen, og gå deretter til **Journaler for leie av anleggsmidler**. **Nedbetalingsplan for leieforpliktelse** vises også i rentetransaksjonene.

   Siden **Tidsplan for avskrivning av anleggsmidler** viser avskrivningstransaksjonene for den valgte leie-ID-en. 

   [![Transaksjonsside for bruksrettseiendel](./media/overview-20.png)](./media/overview-20.png)

   Siden **Transaksjoner for bruksrettseiendel** viser opprinnelig gjenkjenning, akkumulert avskrivning og anleggsmiddelsaldo. 

   Siden **Transaksjoner for leieforpliktelse** viser den opprinnelige gjenkjenningen, rentebetalingen for leie, leiebetaling og saldo for leieforpliktelse. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]