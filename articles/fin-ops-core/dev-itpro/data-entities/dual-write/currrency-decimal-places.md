---
title: Migrering av valutadatatype for dobbelt skriving
description: Denne artikkelen beskriver hvordan du endrer antallet desimaler som dobbelt skriving støtter for valuta.
author: RamaKrishnamoorthy
ms.date: 12/08/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 327d6ced7fca4bdae1fd80928086dafed6b0f931
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289722"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Migrering av valutadatatype for dobbelt skriving

[!include [banner](../../includes/banner.md)]



Du kan øke antallet desimaler som støttes for valutaverdier, til maksimalt 10. Standardgrensen er fire desimalplasser. Hvis du øker antallet desimaler, bidrar du til å hindre tap av data når du bruker toveisskriving for å synkronisere data. Økningen i antall desimalplasser er en endring som velges. Hvis du vil implementere den, må du be om hjelp fra Microsoft.

Prosessen med å endre antall desimaler har to trinn:

1. Be om migrering fra Microsoft.
2. Endre antall desimaler i Dataverse.

Økonomi- og driftsappen og Dataverse må støtte samme antall desimalplasser i valutaverdier. Ellers kan det oppstå tap av data når denne informasjonen synkroniseres mellom apper. Migreringsprosessen konfigurerer måten valuta og valutakursverdier lagres på, på nytt, men den endrer ikke data. Når migreringen er fullført, kan antall desimaler for valutakoder og prissetting økes, og dataene som brukere legger inn og viser, kan ha større desimalpresisjon.

Migreringen er valgfri. Hvis du kan dra nytte av støtte for flere desimaler, anbefaler vi at du vurderer migreringen. Organisasjoner som ikke krever verdier som har mer enn fire desimalplasser, trenger ikke å migrere.

## <a name="requesting-migration-from-microsoft"></a>Be om migrering fra Microsoft

Lagring for eksisterende valutakolonner i Dataverse kan ikke støtte flere enn fire desimalplasser. I løpet av migreringsprosessen kopieres derfor valutaverdier til nye interne kolonner i databasen. Denne prosessen skjer kontinuerlig til alle data er migrert. Internt, på slutten av migreringen, erstatter de nye lagringstypene de gamle lagringstypene, men dataverdiene er uendret. Valutakolonnene kan da støtte opptil 10 desimalplasser. Under migreringsprosessen kan Dataverse fortsatt brukes uten avbrudd.

Samtidig endres valutakursene, slik at de støtter opptil 12 desimalplasser i stedet for den gjeldende grensen på 10. Denne endringen er obligatorisk, slik at antall desimaler er det samme i både økonomi- og driftsappen og Dataverse.

Migreringen endrer ikke data. Når kolonnene for valuta og valutakurs er konvertert, kan administratorer konfigurere systemet til å bruke opptil 10 desimaler for valutakolonner ved å angi antall desimalplasser for hver transaksjonsvaluta og for prissetting.

### <a name="request-a-migration"></a>Be om en migrering

Hvis du vil gjøre denne funksjonen tilgjengelig, send en e-post til **CDSExpandDecimal@microsoft.com**, og inkluder følgende informasjon:

+ **Emne:** Forespørsel om å aktivere utvidet desimalstøtte for \<organizationID\>
+ **Tekst:** Jeg vil aktivere utvidet støtte for desimaler i organisasjonen min \<organizationID\>.

En Microsoft-representant vil kontakte deg innen to til tre arbeidsdager for de neste trinnene.

Når du ber om en migrering, bør du være oppmerksom på følgende detaljer og planlegge dem i henhold til følgende:

+ Tiden som kreves for å migrere dataene, avhenger av mengden data i systemet. Migrering av store databaser kan ta flere dager.
+ Størrelsen på databasen øker midlertidig mens migreringen kjøres, fordi det kreves ekstra plass til indekser. Det meste av den ekstra plassen frigjøres når migreringen er fullført.
+ Hvis det under migreringsprosessen oppstår feil som hindrer migreringen fra å bli fullført, sender systemet varsler til Microsoft kundestøtte, slik at støttepersonale kan settes inn. Selv om det oppstår feil under migreringen, forblir imidlertid Dataverse fullstendig tilgjengelig for vanlig bruk.
+ Migreringsprosessen er ikke reversibel.

## <a name="changing-the-number-of-decimal-places"></a>Endre antall desimaler

Når migreringen er fullført, kan Dataverse lagre numre som har flere desimaler. Administratorer kan velge hvor mange desimaler som brukes for bestemte valutakoder og for prissetting. Brukere av Microsoft Power Apps, Power BI og Power Automate kan deretter vise og bruke tall som har flere desimaler.

Hvis du vil utføre denne endringen, må du oppdatere følgende innstillinger i Power Apps:

+ **Systeminnstillinger: Valutapresisjon for prissetting** – Kolonnen **Sett valutapresisjonen som brukes for prissetting i hele systemet** definerer hvordan valutaen vil fungere i organisasjonen når **Prissettingspresisjon** er valgt.
+ **Forretningsstyring: Valutaer** – Med kolonnen **Valutapresisjon** kan du angi et egendefinert antall desimalplasser for en bestemt valuta. Det er et tilbakefall til innstillingen for hele organisasjonen.

Det er noen av begrensninger:

+ Du kan ikke konfigurere valutakolonnen i en tabell.
+ Du kan angi mer enn fire desimalplasser bare på nivåene **Prissetting** og **Transaksjonsvaluta**.

### <a name="system-settings-currency-precision-for-pricing"></a>Systeminnstillinger: Valutapresisjon for prissetting

Når migreringen er fullført, kan administratorer angi valutapresisjonen. Gå til **Innstillinger \> Administrasjon**, og velg **Systeminnstillinger**. I **Generelt**-fanen endrer du verdien for kolonnen **Sett valutapresisjonen som brukes for prissetting i hele systemet**, som vist i illustrasjonen nedenfor.

![Systeminnstillinger for valuta.](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Forretningsstyring: Valutaer

Hvis du krever at valutapresisjonen for en bestemt valuta er forskjellig fra valutapresisjonen som brukes til prissetting, kan du endre den. Gå til **Innstillinger \> Forretningsstyring**, velg **Valutaer**, og velg valutaen som skal endres. Deretter setter du **Valutapresisjon**-kolonnen til ønsket antall desimalplasser, som vist i følgende illustrasjon.

![Valutainnstillinger for en bestemt nasjonal innstilling.](media/specific-currency.png)

### <a name="tables-currency-column"></a>Tabeller: Valuta-kolonne

Antallet desimaler som kan konfigureres for bestemte valutakolonner, er begrenset til fire.

### <a name="default-currency-decimal-precision"></a>Standard valutadesimalpresisjon
Hvis du vil ha forventet virkemåte for standard valutadesimalpresisjon under overførings- og ikke-overføringsscenarioer, kan du se følgende tabell. 

| Opprettingsdato  | Valutadesimalfelt    | Eksisterende organisasjon (Valuta-feltet ikke overført) | Eksisterende organisasjon (Valuta-feltet overført) | Ny organisasjonsopprettede poster build 9.2.21062.00134 |
|---------------------------------------------------------|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|------------------------------------------------|
| Valutafelt opprettet før build 9.2.21111.00146  |     |  |       |
|    | Maks presisjon synlig i grensesnitt   | 4 sifre    | 10 sifre    | I/T    |
| | Maks presisjon synlig i resultatgrensesnittet for database og DB-spørringer         | 4 sifre   | 10 sifre   | I/T    |
| Valutafelt opprettet etter build 9.2.21111.00146 |    |  |     |   |
|   | Maks desimalpresisjon synlig i grensesnitt     | 4 sifre   | 10 sifre   | 10 sifre     |
|          | Maks desimalpresisjon synlig i resultatgrensesnittet for database og DB-spørringer | 10 sifre. Bare 4 er imidlertid signifikante med alle nuller utover de 4 desimaltallene. Dette gjør det mulig med en enklere og raskere overføring av organisasjon om nødvendig. | 10 sifre      | 10 sifre     |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

