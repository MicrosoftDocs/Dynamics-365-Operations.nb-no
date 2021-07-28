---
title: Sjekklister for vedlikehold
description: Dette emnet beskriver sjekklister for vedlikehold i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderChecklist, EntAssetMobileWorkOrderLineChecklistDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 135887e4ca8dfc6cae9aa73b316815ed3a7041a9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347098"
---
# <a name="maintenance-checklists"></a>Sjekklister for vedlikehold

[!include [banner](../../includes/banner.md)]



Kontrollister for vedlikehold defineres i vedlikeholdsjobbtyper. Du fyller ut en sjekkliste for vedlikehold som en del av prosessen med å fullføre en arbeidsordre. For mer informasjon om hvordan du konfigurer kontrollister for vedlikehold på vedlikeholdsjobbtyper på siden **Standarder for vedlikeholdsjobbtype**, se [Kategorier for vedlikeholdsjobbtype og vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtype, handel for vedlikeholdsjobb og sjekklister for vedlikehold](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Når du arbeider med sjekklister for vedlikehold i en arbeidsordre, kan du fylle ut de forhåndsdefinerte sjekklistene for vedlikehold som er knyttet til vedlikeholdsjobbtyper. Du kan også legge til flere kontrollister for vedlikehold.


## <a name="fill-in-a-maintenance-checklist"></a>Fylle ut en kontrolliste for vedlikehold

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren og deretter, i handlingsruten, går du til fanen **Arbeidsordre** i gruppen **Linjer** og velger **Sjekkliste for vedlikehold**.

3. **Sjekkliste for vedlikeholdsjobb for arbeidsordre** viser sjekklistene for alle arbeidsordrejobber. Hvis arbeidsordrejobbene har forskjellige vedlikeholdsjobbtyper, kan vedlikeholdssjekklistene være forskjellige på hver arbeidsordrejobb. Velg en arbeidsordrejobb for å arbeide med tilknyttet kontrolliste for vedlikehold. Detaljer for den valgte vedlikeholdssjekklistelinjen vises i hurtigfanen **Linjedetaljer**.

4. Fullfør alle sjekklistelinjene for vedlikehold, én om gangen, i den rekkefølgen de vises i. Du fullfører en vedlikeholdssjekklistelinje ved å fylle ut feltene i hurtigfanen **Linjedetaljer**. Informasjonen som kreves for å fullføre en linje, kan variere avhengig av linjetypen. På en linje av typen **Tekst** kan du legge til en merknad som forklarer resultatet av kontrollen. På en linje av typen **Måling** kan du legge til tellerverdien du leser på utstyret, og du kan også legge til en merknad hvis det er nødvendig. En vedlikeholdssjekklistelinje av typen **Hode** brukes som en overskrift for å gruppere vedlikeholdssjekklistelinjene som vises nedenfor. Du trenger ikke å fylle ut et hode. Som for alle andre typer vedlikeholdssjekklistelinjer kan du legge til en merknad på en linje av typen **Hode**.

5. Hvis instruksjoner er knyttet til en vedlikeholdssjekklistelinje, er avmerkingsboksen **Instruksjoner** merket. Les instruksjonene for den valgte vedlikeholdssjekklistelinjen på hurtigfanen **Linjedetaljer** i feltet **Instruksjoner**.

6. Når du har fullført en vedlikeholdssjekklistelinje, merker du av for **Kontrollert** på linjen for å merke den som fullført. Hvis du vil forkaste en vedlikeholdssjekklistelinje fordi den ikke er relevant for arbeidsordrejobben, merker du av for **I/T** på linjen. Hvis det er merket av for **Obligatorisk** på sjekklistelinjen for vedlikehold, må du merke av **Kontrollert** eller **I/T**.

>[!NOTE]
>Du kan bare oppdatere vedlikeholdssjekklisteregistreringer hvis arbeidsordren er i en [aktiv](../setup-for-work-orders/work-order-lifecycle-states.md) livssyklustilstand.  


## <a name="add-a-maintenance-checklist-line"></a>Legge til en linje i sjekkliste for vedlikehold

Sjekklister for vedlikehold opprettes fra definisjonen for standard vedlikeholdsjobbtype og overføres til en arbeidsordrejobb. Om nødvendig kan du legge til vedlikeholdssjekklistelinjer i en arbeidsordrejobb. Manuelt tilføyde sjekklistelinjer får referansen **Manuell**.

1. På siden **Sjekkliste for vedlikeholdsjobb for arbeidsordre** velger du arbeidsordrejobben som du vil legge til en vedlikeholdssjekkliste for.

2. På hurtigfanen **Vedlikeholdssjekklistelinjer** velger du en vedlikeholdssjekklistelinje. Hvis du vil sette inn en ny linje etter den valgte linjen, trykker du på **Pil ned**-tasten. Det neste nummeret i sekvensen settes automatisk inn fra **Linjenummer**-feltet. Hvis du vil sette inn en ny linje før den valgte linjen, velger du **Legg til linje**. 

3. Sett inn et navn for vedlikeholdssjekklistelinjen i **Navn**-feltet.

4. Velg en type for vedlikeholdssjekklistelinjen i **Type**-feltet. For hver type vedlikeholdssjekkliste viser hurtigfanen **Linjedetaljer** relaterte felt.
    - **Tekst** - Bruk denne typen til å legge til en sjekklistelinje for vedlikehold med tekst som beskriver hva som må gjøres. Bruk for eksempel denne hvis du vil at en arbeider skal sjekke eller inspisere noe, men du ikke forventer et bestemt (målbart) resultat. Når du har valgt denne typen, skriver du inn teksten som beskriver hva som må gjøres, i feltet **Instruksjoner** i hurtigfanen **Linjedetaljer**.
    - **Hode** – En vedlikeholdssjekklistelinje av denne typen brukes som en overskrift for å gruppere vedlikeholdssjekklistelinjene som vises nedenfor. Denne typen er nyttig hvis du har flere vedlikeholdssjekklistelinjer som kan deles inn i bestemte områder. Når du har valgt denne typen, skriver du inn et beskrivende navn i **Navn**-feltet.
    - **Mal** – Denne typen er ikke tilgjengelig når du legger til en vedlikeholdssjekklistelinje manuelt i en arbeidsordrejobb.  
    - **Variabel** – Bruk denne typen til å definere et mulig resultat i et område på en vedlikeholdssjekklistelinje. Hvis du vil ha mer informasjon om oppsett av vedlikeholdssjekklistevariabler, se [Kategorier for vedlikeholdsjobbtyper og vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtyper, vedlikeholdsjobbfag og sjekklister for vedlikehold](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Når du har valgt denne typen, skriver du inn et beskrivende navn på variabelen i **Navn**-feltet. Velg variabelen **Variabel**-feltet i hurtigfanen **Linjedetaljer**. I **Instruksjoner**-feltet angir du en tekst som beskriver hva som må gjøres.
    - **Mål** – Bruk denne typen til å registrere et bestemt mål på sjekklistelinje for vedlikehold. Når du har valgt denne typen, skriver du inn et navn på målet i **Navn**-feltet. Velg aktuelle verdier i feltene **Teller** og **Enhet** i hurtigfanen **Linjedetaljer**. I **Instruksjoner**-feltet angir du en tekst som beskriver hva som må gjøres.

5. Når du er ferdig med å legge til linjer for vedlikeholdssjekklister manuelt, fyller du ut linjene som beskrevet i delen **Fylle ut en kontrolliste for vedlikehold** ovenfor.

>[!NOTE]
>På siden **Sjekkliste for vedlikeholdsjobb for arbeidsordre** kan du ikke slette vedlikeholdssjekklistelinjer med referansen **Jobbtype**. Du kan bare slette vedlikeholdssjekklistelinjer som du eller andre vedlikeholdspersoner har opprettet manuelt, og som har referansen **Manuell**.

Illustrasjonen nedenfor viser et eksempel på en kontrolliste for vedlikehold.

![Figur 1.](media/14-work-orders.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]