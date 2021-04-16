---
title: Malstykklister
description: En malstykkliste gir en standardisert liste over komponentene for serviceobjekter som blir vedlikeholdt regelmessig.
author: ShylaThompson
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70b514aeed48180bb1b14be8b3d95d55d44d2ca8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824337"
---
# <a name="template-boms"></a>Malstykklister    

[!include [banner](../includes/banner.md)]


En malstykkliste gir deg en standardisert liste over komponentene for serviceobjekter som blir vedlikeholdt regelmessig. Komponentene som er oppført i malstykklisten, representerer de individuelle delkomponentene til serviceobjektet. Ved å bruke en malstykkliste på et serviceobjekt, kan du holde oversikt over delkomponentene som er erstattet på serviceobjektet.

Du kan bruke en malstykkliste på en serviceavtale eller en serviceordre ved å knytte den til en serviceobjektforbindelse.


> [!NOTE]
> <P>Du kan bare bruke én malstykkliste på et serviceobjekt.</P>

## <a name="create-a-template-bom"></a>Opprette en malstykkliste

Tabellen nedenfor inneholder informasjon om de forskjellige metodene du kan bruke til å opprette en malstykkliste.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Metode</p></th>
<th><p>beskrivelse</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Produksjon</p></td>
<td><p>Malstykklisten er basert på en produksjonsordre. Dette alternativet er bare tilgjengelig hvis du jobber i et produksjonsmiljø. Fordelen er at du har en aktuell, detaljert oppføring av komponentene som utgjør en vare.</p></td>
</tr>
<tr class="even">
<td><p>Vare BOM</p></td>
<td><p>Malstykklisten er basert på en varestykkliste. Varestykklisten, i motsetning til produksjonsstykklisten, er en statisk liste over komponentene som utgjør en vare.</p></td>
</tr>
<tr class="odd">
<td><p>Eksisterende mal</p></td>
<td><p>Malen er basert på en eksisterende malstykkliste.</p></td>
</tr>
<tr class="even">
<td><p>Manuell</p></td>
<td><p>Hvis du vet hvilke reservedeler som vanligvis erstattes på et serviceobjekt, kan du opprette malstykklisten manuelt. Denne metoden bidrar til å sikre at komponentene som er inkludert i malen, gjenspeiler de faktiske kravene til arbeidsplassen.</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Bruk malstykklisten på en serviceavtale eller en serviceordre

Du kan bruke en malstykkliste kan brukes for en serviceavtale og en serviceordre, eller begge deler. Serviceavtalen dekker vanligvis et langsiktig forhold med en kunde. Loggen for erstatninger som er registrert i servicestykkmalen, er nyttige data å ha for serviceavtalen.

Du kan også bruke en malstykkliste på en serviceordre for å registrere historikken for servicen som er utført på et serviceobjekt.

## <a name="copy-the-history-of-a-service-bom"></a>Kopiere loggen til en servicestykkliste

Du kan kopiere loggen til en servicestykklistelinje fra en serviceavtale til en annen serviceavtale. Når du kopierer serviceloggen mellom serviceavtaler, kan du beholde erstatningsoppføringen for en vare.

**Eksempel**

Du har angitt en serviceavtale på tre år for bilen til en kunde. I den perioden blir kunden vant til firmaets gode service som firmaet tilbyr. Derfor når avtalen utløper, ønsker kunden å sette opp en ny. Du kan nå forhandle bedre betingelser for firmaet. Ettersom oppføringen av erstattede komponenter kan være nyttig i fremtiden, kopierer du loggen for servicestykklisten til den nye avtalen.

## <a name="modify-the-template-bom"></a>Endre malstykklisten

Hvis en malstykkliste ikke er knyttet til et serviceobjekt, kan du endre eller slette linjer i den. Når malstykklisten er knyttet til et serviceobjekt, kan du bare endre den lokale versjonen av stykklisten. Hvis du vil duplisere oppsettet av en lokal versjon av malstykklisten, kan du opprette en ny malstykkliste basert på den lokale versjonen. Hvis du vil ha mer informasjon, se [Endre en servicestykkliste](modify-service-bom.md).

Hvis du erstatter en vare i stykklisten, kan du registrere erstatningen på stykklistelinjen i stykklisteutformeren. Du kan også opprette en serviceordrelinje for erstatningsobjektet. Hvis du oppretter en serviceordrelinje, kan du fakturere erstatningsvaren. Hvis du ikke oppretter en serviceordrelinje for en erstatning, beholdes erstatningsregistreringen slik at du kan spore loggen til serviceobjektet.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Endre hvordan informasjon på stykklistelinjen vises

Du kan endre hvordan informasjonen på stykklistelinjen vises for alle maler og servicestykklister. Endringene brukes på alle malstykklister og servicestykklister. Dette inkluderer de som er knyttet til serviceobjekter.

## <a name="set-up-number-sequences-for-template-boms"></a>Angi nummerserier for malstykklister

Hvis du vil bruke malstykklister, må du angi to nummerserier. Definer en nummerserie for malstykklisten og en for linjenummeret for stykklistelogg.


> [!NOTE]
> <P>Nummerserier brukes til å tildele identifikatorer oppføringer som krever det. Før du kan tilordne en nummerserie for en malstykkliste eller et linjenummer for stykklistelogg, må du definere nummerseriekoder.</P>


## <a name="set-up-number-sequences"></a>Definer nummerserier

1.  På listesiden **Nummerserier** oppretter du nummerserier for malstykklister og linjenummeret for stykklisteloggen. 

2.  Klikk på **Servicestyring** \> **Oppsett** \> **Servicestyringsparametere**.

3.  Klikk på **Nummerserier**, og velg en nummerseriekode for nummerseriereferansene du har opprettet i skjemaet **Nummerserier**.

4.  Lukk skjemaet for å lagre endringene.


> [!NOTE]
> <P>Linjenummeret for stykklisteloggen brukes av systemet til å knytte transaksjonene i stykklisteloggen til en serviceavtale eller serviceordre. Nummeret vises ikke i brukergrensesnittet.</P>



## <a name="see-also"></a>Se også

[Opprette en malstykkliste](create-template-bom.md)

[Behandle malstykklister på objektrelasjoner](manage-template-boms-on-object-relations.md)

[Endre en servicestykkliste](modify-service-bom.md)

 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]