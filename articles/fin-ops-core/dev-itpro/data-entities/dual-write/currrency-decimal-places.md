---
title: Migrering av valutadatatype for dobbelt skriving
description: Dette emnet beskriver hvordan du endrer antallet desimaler som dobbelt skriving støtter for valuta.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456820"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Migrering av valutadatatype for dobbelt skriving

[!include [banner](../../includes/banner.md)]

Du kan øke antallet desimaler som støttes for valutaverdier, til maksimalt 10. Standardgrensen er fire desimalplasser. Hvis du øker antallet desimaler, bidrar du til å hindre tap av data når du bruker toveisskriving for å synkronisere data. Økningen i antall desimalplasser er en endring som velges. Hvis du vil implementere den, må du be om hjelp fra Microsoft.

Prosessen med å endre antall desimaler har to trinn:

1. Be om migrering fra Microsoft.
2. Endre antall desimaler i Common Data Service.

Finance and Operations-appen og Common Data Service må støtte samme antall desimalplasser i valutaverdier. Ellers kan det oppstå tap av data når denne informasjonen synkroniseres mellom apper. Migreringsprosessen konfigurerer måten valuta og valutakursverdier lagres på, på nytt, men den endrer ikke data. Når migreringen er fullført, kan antall desimaler for valutakoder og prissetting økes, og dataene som brukere legger inn og viser, kan ha større desimalpresisjon.

Migreringen er valgfri. Hvis du kan dra nytte av støtte for flere desimaler, anbefaler vi at du vurderer migreringen. Organisasjoner som ikke krever verdier som har mer enn fire desimalplasser, trenger ikke å migrere.

## <a name="requesting-migration-from-microsoft"></a>Be om migrering fra Microsoft

Lagring for eksisterende valutafelt i Common Data Service kan ikke støtte mer enn fire desimalplasser. I løpet av migreringsprosessen kopieres derfor valutaverdier til nye interne felt i databasen. Denne prosessen skjer kontinuerlig til alle data er migrert. Internt, på slutten av migreringen, erstatter de nye lagringstypene de gamle lagringstypene, men dataverdiene er uendret. Valutafeltene kan da støtte opptil 10 desimalplasser. Under migreringsprosessen kan Common Data Service fortsatt brukes uten avbrudd.

Samtidig endres valutakursene, slik at de støtter opptil 12 desimalplasser i stedet for den gjeldende grensen på 10. Denne endringen er nødvendig, slik at antall desimaler er det samme i både Finance and Operations-appen og Common Data Service.

Migreringen endrer ikke data. Når feltene for valuta og valutakurs er konvertert, kan administratorer konfigurere systemet til å bruke opptil 10 desimaler for valutafelt ved å angi antall desimalplasser for hver transaksjonsvaluta og for prissetting.

### <a name="request-a-migration"></a>Be om en migrering

Hvis du vil gjøre denne funksjonen tilgjengelig, send en e-post til **CDSExpandDecimal@microsoft.com**, og inkluder følgende informasjon:

+ **Emne:** Forespørsel om å aktivere utvidet desimalstøtte for \<organizationID\>
+ **Tekst:** Jeg vil aktivere utvidet støtte for desimaler i organisasjonen min \<organizationID\>.

En Microsoft-representant vil kontakte deg innen to til tre arbeidsdager for de neste trinnene.

Når du ber om en migrering, bør du være oppmerksom på følgende detaljer og planlegge dem i henhold til følgende:

+ Tiden som kreves for å migrere dataene, avhenger av mengden data i systemet. Migrering av store databaser kan ta flere dager.
+ Størrelsen på databasen øker midlertidig mens migreringen kjøres, fordi det kreves ekstra plass til indekser. Det meste av den ekstra plassen frigjøres når migreringen er fullført.
+ Hvis det under migreringsprosessen oppstår feil som hindrer migreringen fra å bli fullført, sender systemet varsler til Microsoft kundestøtte, slik at støttepersonale kan settes inn. Selv om det oppstår feil under migreringen, forblir imidlertid Common Data Service fullstendig tilgjengelig for vanlig bruk.
+ Migreringsprosessen er ikke reversibel.

## <a name="changing-the-number-of-decimal-places"></a>Endre antall desimaler

Når migreringen er fullført, kan Common Data Service lagre numre som har flere desimaler. Administratorer kan velge hvor mange desimaler som brukes for bestemte valutakoder og for prissetting. Brukere av Microsoft Power Apps, Power BI og Power Automate kan deretter vise og bruke tall som har flere desimaler.

Hvis du vil utføre denne endringen, må du oppdatere følgende innstillinger i Power Apps:

+ **Systeminnstillinger: Valutapresisjon for prissetting** – Feltet for **Sett valutapresisjonen som brukes for prissetting i hele systemet** definerer hvordan valutaen vil fungere i organisasjonen når **Prissettingspresisjon** er valgt.
+ **Forretningsstyring: Valutaer** – Med feltet **Valutapresisjon** kan du angi et egendefinert antall desimalplasser for en bestemt valuta. Det er et tilbakefall til innstillingen for hele organisasjonen.

Det er noen av begrensninger:

+ Du kan ikke konfigurere valutafeltet i en enhet.
+ Du kan angi mer enn fire desimalplasser bare på nivåene **Prissetting** og **Transaksjonsvaluta**.

### <a name="system-settings-currency-precision-for-pricing"></a>Systeminnstillinger: Valutapresisjon for prissetting

Når migreringen er fullført, kan administratorer angi valutapresisjonen. Gå til **Innstillinger \> Administrasjon**, og velg **Systeminnstillinger**. I kategorien **Generelt** endrer du verdien for **Sett valutapresisjonen som brukes for prissetting i hele systemet**, som vist i illustrasjonen nedenfor.

![Systeminnstillinger for valuta](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Forretningsstyring: Valutaer

Hvis du krever at valutapresisjonen for en bestemt valuta er forskjellig fra valutapresisjonen som brukes til prissetting, kan du endre den. Gå til **Innstillinger \> Forretningsstyring**, velg **Valutaer**, og velg valutaen som skal endres. Deretter setter du **Valutapresisjon**-feltet til ønsket antall desimalplasser, som vist i følgende illustrasjon.

![Valutainnstillinger for en bestemt nasjonal innstilling](media/specific-currency.png)

### <a name="entities-currency-field"></a>Enheter: Valuta-felt

Antallet desimaler som kan konfigureres for bestemte valutafelt, er begrenset til fire.
