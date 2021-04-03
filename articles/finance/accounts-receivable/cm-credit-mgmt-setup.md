---
title: Oppsett av parametere for kredittbehandling
description: Dette emnet beskriver alternativene du kan bruke til å konfigurere kredittbehandling for å dekke bedriftens behov.
author: mikefalkner
manager: AnnBe
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 126cae03228b1fb49ded877af69643ec8676c1ec
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242889"
---
# <a name="credit-management-parameters-setup"></a>Oppsett av parametere for kredittbehandling

[!include [banner](../includes/banner.md)]

Dette emnet beskriver alternativene du kan bruke til å konfigurere kredittbehandling for å dekke bedriftens behov. Når du skal bruke funksjonene for kredittbehandling, definerer du parameterne på siden **Parametere for kreditt og innkreving** (**Kreditt og innkreving \> Oppsett \> Parametere for kreditt og innkreving**).

## <a name="credit-parameters"></a>Kredittparametere

Det finnes fire hurtigfaner i **Kreditt**-delen der du kan endre parameterne som styrer kredittstyring: **Kredittsperrer**, **Kontrollpunkt for kredittbehandling**, **Statistikk for kredittbehandling** og **Kredittgrenser**. Følgende deler beskriver innstillingene som er tilgjengelige i hver hurtigfane.

### <a name="credit-holds"></a>Kredittsperrer

- Sett alternativet **Tillat redigering av salgsordreverdi etter at ordresperre er frigitt** til **Nei** for å kreve at posteringsreglene sjekkes på nytt hvis salgsordreverdien (utvidet pris) er økt etter at salgsordren ble frigitt fra på vent-listen. .
- I feltet **Årsaker til kansellerte ordrer** velger du frigivelsesårsaken som skal brukes som standard når en salgsordre som var på vent i kredittbehandling, avbrytes.
- Sett alternativet **Kontroller kredittgrense for kundekredittgrupper** til **Ja** for å kontrollere kredittgrensen til en kundekredittgruppe når kunden på en salgsordre tilhører en kundekredittgruppe. Kredittgrensen for gruppen vil bli kontrollert, og deretter, hvis den er tilstrekkelig, blir kredittgrensen for kunden kontrollert.
- Sett alternativet **Kontroller kredittgrense når betalingsbetingelser økes** til **Ja** for å kontrollere rangeringene for betalingsbetingelser for å avgjøre om betalingsbetingelsene i salgsordren er forskjellige fra standard betalingsbetingelser for kunden. Hvis de nye betalingsbetingelsene har en høyere rangering enn de opprinnelige betalingsbetingelsene, settes ordren på vent for kredittbehandling.
- Sett alternativet **Kontroller kredittgrense når en utligningsrabatt økes** til **Ja** for å kontrollere rangeringene for utligningsrabatter for å avgjøre om kontantrabatten i salgsordren er forskjellig fra standard kontantrabatt for kunden. Hvis den nye kontantrabatten har en høyere rangering enn den opprinnelige kontantrabatten, settes ordren på vent for kredittbehandling.
- I feltet **Årsak til frigivelse av endrede order** velger du frigivelsesårsaken som skal brukes som standard når endrede ordrer frigis automatisk fra kredittbehandlingssperre.
- Sett alternativet **Ignorer blokkeringsregel for kredittgrense utløpt når utløpsdato er tom** til **Ja** for å kontrollere virkemåten til regelen **Kredittgrense utløpt**. Sett alternativet til **Nei** for å blokkere en ordre når utløpsdatoen er tom.
- I lagerstyring kan laster opprettes på tidspunktet for salgsordreregistrering. Sett alternativet **Fjern blokkerte lastelinjer** til **Nei** for å beholde salgsordrelinjer for lasten når en salgsordre er i kredittsperre. Lasten kan ikke behandles når salgsordren er på vent. Sett alternativet til **Ja** for å fjerne salgsordrelinjer fra lasten når en salgsordre er i kredittsperre. Lasten kan deretter behandles.
- Salgsordrer kan frigis automatisk fra kredittbehandlingskontroll. I feltet **Årsak til å frigi automatisk** kan du velge en frigivelsesårsak som skal brukes som standard når salgsordrer frigis automatisk.
- Salgsordrer kan frigis automatisk fra kredittbehandlingskontroll. Velg **Uten postering** i **Automatisk frigivelse**-feltet for å frigi sperren i en ordre. Du må kjøre prosessen som satte ordren på vent, manuelt. Velg **Med postering** for å postere ordren ved å bruke den samme posteringsprosessen som ble kjørt da salgsordren ble satt på vent.

### <a name="credit-management-checkpoint"></a>Kontrollpunkt for kredittbehandling

Du kan angi tidspunkt som skal brukes til å kontrollere salgsordrer for kredittproblemer. Hurtigfanen **Kontrollpunkt for kredittbehandling** identifiserer dokumentposteringsprosessene som omfatter behandling av kredittstyringsregler. Du kan også kontrollere kredittreglene mens du enten gjør en proformapostering eller en fullstendig postering av salgsordren. Merk av i avmerkingsboksene for å definere posteringsprosessene som skal sette en ordre på vent hvis det blir funnet et problem etter at blokkeringsreglene for kredittbehandling er behandlet.

Du kan også definere antall løpedager før kredittreglene kontrolleres på nytt. Selv om du kan angi at kredittbehandlingsreglene skal kontrolleres ved postering, blir ikke reglene kontrollert for det angitte antallet løpedager. Du bekrefter for eksempel en salgsordre på dag 1, og du angir to løpedager for bekreftelsestrinnet. I dette tilfellet blir ikke kredittreglene kontrollert ved neste posteringstrinn (for eksempel opprettelse av en følgeseddel eller fakturering av ordren) frem til dag 4. På eller etter dag 4 vil reglene bli kontrollert på nytt når posteringer skjer, og antall løpedager vil bli endret til verdien som er angitt for neste posteringskontrollpunkt.

Hvis du ikke angir antall løpedager, blir kredittreglene kontrollert på hvert posteringstrinn som er definert for å kjøre kredittbehandlingsregler. Hvis du frigir salgsordren uten å postere og deretter kjører samme ordrebehandlingstrinn på nytt, blir kredittreglene kontrollert på nytt. En ordre settes for eksempel på vent etter en bekreftelse, og du frigir den enten med eller uten postering. I dette tilfellet vil ordren settes på vent igjen hvis du bekrefter den på nytt. Bruk løpedager hvis ordren skal gå videre til neste behandlingstrinn uten å settes på vent igjen.

Du kan ikke angi løpedager for noen posteringskontrollpunkt, men ikke for andre. Du må definere alle posteringskontrollpunkt slik at de har løpedager, eller du må definere dem alle slik at de ikke har løpedager.

- Merk av for **Postering** for å kjøre kredittbehandlingsreglene når posteringskontrollpunktet som vises på linjen, kjøres. Hvis du ikke merker av i avmerkingsboksen, kontrolleres reglene bare én gang under hele posteringsprosessen.
- Hvis du merker av for **Postering**, angir du antall løpedager som skal gå før blokkeringsreglene kontrolleres på nytt. Du kan ikke legge til løpedager hvis avmerkingsboksen **Postering** ikke er merket.
- Merk av for **Proforma** for å kjøre kredittbehandlingsreglene når posteringskontrollpunktet for proforma som vises på linjen, kjøres. I de fleste tilfeller settes **Postering**-feltet til **Nei** i dialogboksen som vises når en salgsordre posteres.
- Hvis du merker av for **Postering**, angir du antall løpedager som skal gå før blokkeringsreglene kontrolleres på nytt. Du kan ikke legge til løpedager hvis avmerkingsboksen **Postering** ikke er merket.

### <a name="credit-management-statistics"></a>Statistikk for kredittbehandling

Flere kredittbehandlingsstatistikker er inkludert i faktaboksen **Statistikk for kundekredittbehandling** på **Kunde**-siden. Du må angi flere verdier som kreves for å beregne disse statistikkene. Angi antall måneder som skal brukes til å beregne følgende verdier i faktaboksen **Statistikk for kundekredittbehandling**:

1. Dager utestående salg 1
2. Dager utestående salg 2
3. Gjennomsnittlig saldo 1
4. Gjennomsnittlig saldo 2
5. Gjennomsnittlig kredittgrense %
6. Gjennomsnittlig eksponering %

### <a name="credit-limits"></a>Kredittgrenser

- I kredittbehandling vises kundekredittgrensen i kundens valuta. Du må definere valutakurstypen for kredittgrensen i kundens valuta. I feltet **Valutakurstype for kredittgrense** velger du valutakurstypen som skal brukes til å konvertere den primære kredittgrensen til kundens kredittgrense.
- Sett alternativet **Tillat manuell redigering av kredittgrenser** til **Nei** for å hindre brukere i å redigere kredittgrenser på **Kunde**-siden. Hvis dette alternativet settes til **Nei**, kan endringer i kundens kredittgrense bare gjøres ved å postere justeringstransaksjoner for kredittgrense.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Nummerserier og parametere for delt nummerserie

Det kreves en journal-ID for å behandle justeringer av kredittgrense. Du må legge til kredittgrensejusteringsnummeret som skal brukes til å generere journal-ID-en.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]