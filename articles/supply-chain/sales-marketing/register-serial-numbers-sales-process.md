---
title: Registrere serienumre i salgsprosessen
description: Dette emnet forklarer hvordan du kan registrere serienumre på følgesedler eller fakturaer i løpet av salgsprosessen. Denne funksjonaliteten er nyttig hvis et firma ønsker å ha serienumre for service- og garantiformål, men ikke trenger å vedlikeholde serienumrene på lageret fra mottak til avgang.
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d655015a2048bb8e7d85d8ea3679b8b2506caf10
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572112"
---
# <a name="register-serial-numbers-in-the-sales-process"></a>Registrere serienumre i salgsprosessen

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du kan registrere serienumre på følgesedler eller fakturaer i løpet av salgsprosessen. Denne funksjonaliteten er nyttig hvis et firma ønsker å ha serienumre for service- og garantiformål, men ikke trenger å vedlikeholde serienumrene på lageret fra mottak til avgang.

Mange firmaer vil bare ha serienumre for service- og garantiformål, og trenger ikke vedlikeholde serienumrene på lageret fra mottak til avgang. I slike tilfeller kan du registrere serienumre på følgesedler eller fakturaer når varer selges. Hvis en vare returneres til deg senere, kan du spore den til en faktura for å finne ut om du solgte produktet, og om tjenesten eller garantiforpliktelsene er gyldige.

Du må aktivere serienumre for salgsprosessen ved å merke av for **Aktiv i salgsprosess** på siden **Sporingsdimensjonsgrupper**. Følgende hendelser forekommer deretter i Supply Chain Management:
-   På hurtigfanen **Serienumre** er **Serienummerkontroll** avmerket. Når det er merket av for dette alternativet, må du registrere ett serienummer for hver vare på følgeseddelen eller fakturaen.
-   Alle valg i sporingsdimensjonsgruppen for serienumre fjernes, bortsett fra alternativet **Tom avgang tillatt**. Du kan merke av for **Tom avgang tillatt** for å overstyre serienummerkontrollen og tillate at produkter pakkes og faktureres uten at serienumre registreres.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Når registrerer jeg serienumre i salgsprosessen?
Du kan registrere serienumre på følgeseddelen for en salgsordre eller på fakturaen. Når du forbereder en faktura for en serialisert vare som ble sendt med en følgeseddel, kan du velge hvilke av serienumrene som skal faktureres, på følgeseddelen. Antallet registrerte serienumre, må ikke overskride antallet varer som ble sendt. Hvis du oppretter en delvis faktura, kan du velge færre serialiserte varer enn det som er registrert på følgeseddelen. Når du skriver ut en følgeseddel eller faktura, inkluderes serienumrene som ble registrert.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Kan jeg angi serienumre ved å skanne dem, eller må jeg skrive dem inn?
Du kan skanne eller skrive inn serienumre. Når du bruker en skanner, avgjør søkemodusen om serienumrene legges til eller fjernes fra listen over serienumre på fakturaen eller følgeseddelen. Hvis du vil skanne serienumre ved for eksempel å bruke en håndholdt strekkodeskanner, konfigurerer du skanneren slik at den sender en Angi- eller TAB-kommando etter serienummeret. Denne kommandoen indikerer slutten av dataflyten. Hvis ikke, må du trykke Enter eller TAB på tastaturet etter du har skannet hvert serienummer.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Hvis jeg aktiverer serienumre for salgsprosessen, må jeg registrere alle serienumre for alle varer?
Oppsettet for sporingsdimensjonsgruppen som er tilordnet til produktet, avgjør om serienumre for alle varer på en følgeseddel eller faktura må registreres. Når du aktiverer serienumre for salgsprosessen, blir det automatisk merket av for **Serienummerkontroll**. Du må deretter registrere ett serienummer eller registrere en tom registrering for et uleselig nummer, for hvert element på følgeseddelen eller fakturaen. Hvis du ikke vil kreve et serienummer for hver vare, merker du av for **Tom avgang tillatt** i sporingsdimensjonsgruppen som er tilordnet varen. Deretter kan du registrere færre serienumre enn antallet varer som leveres. Hvis du registrerer flere serienumre enn vareantallet som skal sendes, kan du ikke postere følgeseddelen eller fakturaen.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Kan jeg registrere serienumre for delvise fakturaer og delvise forsendelser?
Du kan opprette delvise fakturaer og følgesedler for salgsordrer og registrere bare serienumrene for varene disse fakturaene og følgesedlene inneholder. Hvis du vil opprette en delvis faktura og har flere følgesedler for salgsordren, kan du ta med serienumre fra flere følgesedler. Det kan imidlertid bare være én følgeseddel som ikke inkluderer alle serienumrene. Hvis du har tre pakksedler og alle inneholder to serialiserte varer, kan du for eksempel ikke opprette en delfaktura for én vare fra hver følgeseddel.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Hva gjør jeg når et serienummer ikke er lesbart?
Hvis et serienummer ikke kan leses eller skannes, kan du opprette en tom linje for varen ved å klikke **Ikke lesbart** på **Serienumre**-siden. Hvis serienummeret blir tilgjengelig senere, kan du oppdatere fakturaen eller følgeseddelen. Hvis du vil ha mer informasjon, kan du se neste del Kan jeg rette eller endre serienumrene jeg har registrert for en salgsordre?

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Kan jeg rette eller endre serienumrene jeg har registrert for en salgsordre?
Ja, du kan korrigere serienumre hvis følgende betingelser er oppfylt:
-   **Fakturaer**  – Du kan endre serienumre for varer du ikke har fakturert enda. Følgeseddelen oppdateres også. Hvis du korrigerte en salgsordrelinje ved å registrere et negativt antall, kan du imidlertid ikke endre serienumre for salgsordrelinjen.
-   **Følgesedler**  – Du kan ikke delvis korrigere en følgeseddellinje som inneholder serialiserte varer. Du må tilbakeføre hele antallet for linjen. Hvis en følgeseddel er avbrutt eller rettet, trenger du ikke å registrere de tilbakeførte serienumrene på nytt når du oppretter en ny følgeseddel for de samme serialiserte varene. Numrene som var registrert, vil bli brukt.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Kan jeg vise serienumrene som ble sendt sammen med en bestemt følgeseddel eller som ble inkludert på en faktura?
Ja, kan du kjøre en spørring på følgeseddeljournallinjen eller fakturajournallinjen for å vise en liste over alle serienumre som ble inkludert i dokumentet.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Kan jeg vise de serialiserte varene jeg har på lager?
Nei, du kan ikke vise de serialiserte varene du har på lager fordi serienumre ikke registreres for varer før varene er solgt.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Kan jeg registrere serienumre for faktisk vekt-varer?
Nei, du kan ikke registrere serienumre for faktisk vekt-varer under salgsprosessen. Hvis et produkt er definert som en faktisk vekt-vare, kan du ikke tilordne produktet til en sporingsdimensjonsgruppe som er konfigurert til å bruke serienumre bare i løpet av salgsprosessen.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Kan jeg registrere serienumre på salgsstedet?

Ja, salgsstedet ber brukeren om å angi et serienummer når brukeren selger en vare som er tilordnet en sporingsdimensjonsgruppe som er konfigurert til å bruke serienumre bare i løpet av salgsprosessen.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Hvilke sikkerhetsroller er nødvendige for å registrere serienumre i løpet av salgsprosessen?
Denne funksjonaliteten er tilgjengelig for alle roller som kan vedlikeholde salgsfølgesedler og salgsfakturaer. Oppgavene nedenfor gir brukerne mulighet til å korrigere serienumre og registrere tomme oppføringer for serienumre som ikke kan leses eller skannes:
-   Vedlikeholde rettelser av serienumre
-   Vedlikeholde registrering av ikke-lesbare serienumre





