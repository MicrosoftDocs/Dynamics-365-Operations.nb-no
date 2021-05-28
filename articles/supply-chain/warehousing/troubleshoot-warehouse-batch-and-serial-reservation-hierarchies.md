---
title: Feilsøke lagerparti- og seriereserveringshierarkier
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med reservasjonshierarkier som bruker parti- eller seriedimensjoner.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022552"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Feilsøke lagerparti- og seriereserveringshierarkier

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med reservasjonshierarkier som bruker parti- eller seriedimensjoner.

Hvis du vil ha mer informasjon, kan du se [Fleksibel dimensjonsreservasjonspolicy for lagernivå](flexible-warehouse-level-dimension-reservation.md).

Reservasjonshierarkiet til en vare angir behovet for lagringsdimensjoner som må oppfylles, for å tilordne en lokasjon til en behovsordre. Disse dimensjonene kan beskrives som *dimensjoner over lokasjonen* for alle dimensjonene som må oppfylles før en lokasjon tilordnes, og *dimensjoner under lokasjonen* for dimensjoner som kan tilordnes etter at en lokasjon er tilordnet behovsordren. Disse reservasjonshierarkiene kalles også *parti-over* og *parti-under* eller *serie-over* og *serie-under*.

Beholdningen kan bare tilordnes hvis det ikke er noen huller i dimensjonene over lokasjonen. I et reservasjonshierarki av typen *parti-over* forventer du for eksempel at dimensjonene **Sted**, **Lager** og **Partinummer** er angitt i behovsordren. Hvis noen av disse dimensjonene mangler, mislykkes tildelingsprosessen. I kontrast til dette kan reservasjonshierarki av typen *parti-under* eller *serie-under* ha et parti- eller serienummer angitt i behovsordren, men tildelingsprosessen krever ikke dette.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Jeg får følgende feilmelding: For å tilordne bølge må lastlinjer angi dimensjonene over lokasjonen. Hvis du vil tilordne disse dimensjonene, må du reservere og opprette lastlinjen på nytt.

### <a name="issue-description"></a>Problembeskrivelse

Når du bruker en vare som har et *parti-over*-reservasjonshierarki, fungerer ikke kommandoen **Frigi til lager** på siden **Arbeidsområde for lastplanlegging** hvis du prøver å frigi en last for en delvis mengde. Du får denne feilmeldingen, og det opprettes ikke noe arbeid for det delvise antallet.

Når du imidlertid bruker en vare som har et *parti-under*-reservasjonshierarki, kan du frigi en last for en delvis mengde fra siden **Arbeidsområde for lastplanlegging**.

### <a name="issue-cause"></a>Feilårsak

Når en dimensjon er over **Lokasjon**-dimensjonen i reservasjonshierarkiet, må den angis før frigivelse til lageret. Delvise antall kan ikke frigis hvis én eller flere dimensjoner over **Lokasjon** ikke er angitt.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Ledeteksten for automatisk reservering av et partinummer utløses selv om det er tilgjengelig lager.

### <a name="issue-description"></a>Problembeskrivelse

Når du bruker en vare som har et *parti-over*-reservasjonshierarki i et lager som ikke har aktivert lagerprosesser, og automatisk reservering er aktivert, vises ledeteksten for automatisk reservering for et partinummer, selv om bare ett parti er tilgjengelig for plukking.

Når du imidlertid bruker den samme varen i et lager der lagerprosessene er aktivert, vises ikke ledeteksten for automatisk reservering.

### <a name="issue-cause"></a>Feilårsak

Hvis et reserveringshierarki er definert som *parti-over* eller *serie-over*, må den refererte dimensjonen (**Partinummer** eller **Serienummer**) alltid være angitt i behovsordrer. Lagerprosesser kan kanskje fylle ut informasjonen hvis ett enkelt parti- eller serienummer er tilgjengelig. Siden lageret ikke er aktivert for lagerprosesser, må imidlertid brukeren alltid angi alle dimensjonene over **Lokasjon**.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Sporingsmaler som har kriteriet Vurder sporbeholdning, tar ikke hensyn til gjeldende lagerbeholdning for partiaktiverte varer.

Hvis du vil ha mer informasjon, kan du se [Lagersporing](warehouse-slotting.md).

### <a name="issue-description"></a>Problembeskrivelse

Sporingsmaler som har kriteriet *Vurder sporbeholdning*, tar ikke hensyn til gjeldende lagerbeholdning for *parti-over*-varer. De vurderer det bare hvis partinummeret er angitt på salgsordrelinjen.

Når du bruker *parti-under*-varer, vurderes imidlertid den gjeldende lagerbeholdningen som forventet.

### <a name="issue-cause"></a>Feilårsak

Sporingsmalhodet kan defineres for behovsstrategien *Bestilt*, *Reservert* eller *Frigitt*. Når det gjelder strategien for *bestilt* etterspørsel, gjelder de samme reservasjonshierarkikravene som gjelder for reservering eller frigivelse for lagerprosesser. For varer som har *parti-over*- og *serie-under*-reservasjonshierarkier, må derfor parti- eller serienummeret angis på behovsordren (salg eller overføring). Du kan også bruke strategien for *reservert* etterspørsel til å velge parti- eller serienummeret før lagerets sporbehov genereres.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
