---
title: Opprett en ny transportstyringsmotor
description: Dette emnet beskriver hvordan du oppretter en ny transportstyringsmotor i Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88661b6a974e2bd60f78e38d49a08d3290008b8b
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652058"
---
# <a name="create-a-new-transportation-management-engine"></a>Opprett en ny transportstyringsmotor

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en ny transportstyringsmotor i Dynamics 365 Supply Chain Management. 

Transportbehandlingsmotorer (TMS) definerer logikken som brukes til å generere og behandle transportsatser i Transportstyring. Supply Chain Management gir flere forskjellige motortyper som beregner ulike parametere, for eksempel satser, transittider og antall soner som krysses under transport. Denne artikkelen beskriver hvordan du bruker Microsoft Visual Studio-utviklingsmiljøet sammen med utviklingsverktøy for Supply Chain Management til å opprette og distribuere en ny TMS-motor, og deretter hvordan du konfigurerer motoren i Operations. Hvis du vil ha mer informasjon om disse motorene, kan du se [Transportstyringsmotorer](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Opprette en ny TMS-motor

Denne delen beskriver hvordan du oppretter et klassebibliotek som har en TMS-motorimplementering, og hvordan du refererer til det fra en Supply Chain Management-modell.

1. For å kunne distribuere nye funksjoner må du ha en modell som vil inneholde motorene. Klikk **Opprett modell** for å opprette en ny modell, på menyen **Dynamics 365** &gt; **Modelladministrasjon**. På første side i veiviseren **Opprett modell** gir du modellen navnet **TMSEngines**. 

   [![Opprette en modell.](./media/012.png)](./media/012.png)

2. På den neste siden velger du **Opprett ny pakke**. 

   [![Opprett en ny pakke.](./media/021.png)](./media/021.png)

3. På den neste siden velger du **ApplicationSuite**-modellen som det skal refereres til. (**ApplicationPlatform**-modellen er forhåndsvalgt.) 

   [![Velge modellen som skal refereres til.](./media/032.png)](./media/032.png)

4. På den neste siden klikker du **Fullfør** for å bekrefte opprettelsen av en ny modell. 

   [![Fullfører modelloppretting.](./media/042.png)](./media/042.png)

5. I en ny løsning oppretter du et nytt Supply Chain Management-prosjekt og gir det navnet **TMSThirdParty**. I prosjektegenskapene angir du prosjektets modell til **TMSEngines**.
6. Legg til et nytt C\#-klassebibliotek i løsningen, og gi den navnet **ThirdPartyTMSEngines**.
7. I ThirdPartyTMSEngines-prosjektet legger du til referanser til Supply Chain Management-spesifikke samlinger:
   -   Programsamlinger som gjør det mulig å referere til X++-typer. Disse samlingene finnes på følgende steder. \[Pakkerot\] er banen til stedet der alle de distribuerte samlingene er plassert, for eksempel C:\\Pakker.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Rammeverksamlinger som gir tilgang til data-, LINQ- og tilleggsfunksjoner. Alle disse samlingene finnes i \[Pakkerot\]\\-boksen.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   Kjerne-TMS-samlingen (som inneholder motorer) og TMS-basissamlingen (som inneholder hjelpere, konstanter, dataoverføringsklassedefinisjoner og så videre). Disse samlingene finnes på følgende steder.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Gi C\#-klassen nytt navn som automatisk blir generert i ThirdPartyTMSEngines-prosjektet til **SampleRatingEngine**.
9. Implementer motoren. Fordi vi oppretter en ratemotor i dette eksemplet, arver vi fra basisklassen for ratemotorer. Basisklassen implementerer det meste av ratemotorgrensesnittet (**TMSFwkIRateEngine**). Vi må bare implementere ratemetoden. For at dette eksemplet skal være enkelt, gjør vi slik at denne metoden registrerer en hardkodet rate på 100. Du kan opprette motorer som implementerer hvilke som helst av motorgrensesnittene, for eksempel **TMSFwkIAccessorialEngine**. Alle motorgrensesnittene er definert i X++.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Bygg løsningen.
11. Legg til en ny referanse til TMSThirdParty-prosjektet. Referansen bør peke til prosjektet ThirdPartyTMSEngines. Når du er ferdig, skal løsningen se slik ut. 

    [![Løsningen, som inneholder en referanse til TMSThirdParty-prosjektet.](./media/052.png)](./media/052.png)

12. Bygg løsningen. Kontroller at det nye biblioteket vises i **Referanser**-noden i Programutforsker. 

    [![Det nye biblioteket i Programutforskererens referansenode.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>Distribuere TMS-motoren som en pakke

En metode som kan brukes til å distribuere tredjeparts-TMS-motorer, er gjennom en distribusjonspakke. Denne fremgangsmåten anbefales i et produksjonsmiljø. I et utviklingsmiljø kan du manuelt kopiere samlingene, som beskrevet i neste del, Definere en TMS-motor i Supply Chain Management. Hvis du vil distribuere motoren som en pakke, følger du disse trinnene.

1. Klikk <strong>Opprett distribusjonspakke</strong> på **Dynamics 365** &gt; **Distribuer**.
2. I dialogboksen **Opprett distribusjonspakke** velger du TMSEngines-modellen og angir banen til der du vil lagre pakkefilene. 

   [![Velge TMSEngines-modellen.](./media/071.png)](./media/071.png)

3. Du kan nå distribuere pakken til målmiljøet. Hvis du vil ha en opplæring, kan du se [Installere en distribuerbar pakke](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Definere TMS-motoren i Supply Chain Management

Denne delen beskriver hvordan du konfigurerer Supply Chain Management for å bruke en TMS-motor, og viser hvordan den nye motoren vi har opprettet, brukes til i innhenting av rater. Eksemplet i denne delen bruker USMF-demodatafirmaet.

1. Opprett en ny motor som beskrevet i delen Opprett en ny TMS-motor.
2. Bygg løsningen din.
3. Kopier den resulterende samlingen til den binære lokasjonen til Supply Chain Management-serveren, \[AOSWebRoot-posisjon\]-boksen. **Merk:** Dette trinnet er bare relevant i et utviklingsmiljø. I et produksjonsmiljø bør du distribuere gjennom en distribusjonspakke. Hvis du vil ha instruksjoner, kan du se den forrige delen, "Distribuere TMS-motoren som en pakke."
4. På siden **Ratemotorer** i Supply Chain Management oppretter du en ratemotor. Motoren bør peke på motorsamlingen som produseres ved å bygge motorklassebiblioteket og motorklassen du implementerte. 

   [![Opprette en ny ratemotor på siden Rate-motorer.](./media/081.png)](./media/081.png)

5. Opprett en transportør som bruker eksempelratemotoren. Fordi maskinen ikke bruker data, behøver du ikke å tilordne en vurderingsmal. 

   [![Opprette en ny transportør.](./media/092.png)](./media/092.png)

6. Klikk **Vurder butikk** på siden **Arbeidsområde for vurderingsrute**. Du skal se en sats på 100,00 fra SampleCarrier, som vist i skjermbildet nedenfor. I dette eksemplet innhenter vi rater for en rute fra lager 24 til kunde i US-004. Men fordi satsen er hardkodet, vil du alltid se en sats på 100,00.

   [![Arbeidsområde for vurderingsrute.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Tips og råd

- Hvis du bruker utviklingsverktøy for Supply Chain Management, er det nyttig å legge til et nytt prosjekt i løsningen. Hvis du angir dette prosjektet som oppstartsprosjektet og starter en feilsøkingsøkt, kan du feilsøke både X++- og C\#-kode i samme feilsøkingsøkt.
- Hver gang du endrer og rekompilerer ThirdPartyTMSEngines-prosjektet, må du manuelt kopiere den resulterende samlingen til den binære lokasjonen eller distribuere via en distribusjonspakke. Ellers kan du kjøre ved å bruke en foreldet samling.
- Når du har utført TMS-spesifikke operasjoner i Supply Chain Management, kan arbeidsprosessen for Internet Information Services (IIS) låse samlingen ThirdPartyTMSEngines slik at samlingen ikke kan oppdateres. I dette tilfellet starter du w3svc-prosessen på nytt.

### <a name="whitepaper"></a>Hvitbok

Hvis du vil ha mer informasjon, kan du laste ned følgende hvitbok (skrevet for å støtte AX2012, men gjelder fortsatt for Dynamics 365 Supply Chain Management)

- [Implementere og distribuere Transportstyringsmotorer](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]