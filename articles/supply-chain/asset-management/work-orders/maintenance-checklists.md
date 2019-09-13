---
title: Sjekklister for vedlikehold
description: Dette emnet beskriver sjekklister for vedlikehold i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875825"
---
# <a name="maintenance-checklists"></a>Sjekklister for vedlikehold


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Sjekklister for vedlikehold defineres i vedlikeholdsjobbtyper og brukes når du jobber med en arbeidsordre. Det å fylle ut en sjekkliste for vedlikehold er en del av å fullføre en arbeidsordre. Se delen [Kategorier for vedlikeholdsjobbtyper og vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtyper, vedlikeholdsjobbfag og sjekklister for vedlikehold](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) hvis du vil ha mer informasjon om hvordan du definerer vedlikeholdssjekklister for vedlikeholdsjobbtyper i skjemaet **Standarder for vedlikeholdsjobbtype**.

Når du arbeider med sjekklister for vedlikehold i en arbeidsordre, kan du fylle ut de forhåndsdefinerte sjekklistene for vedlikehold som er knyttet til vedlikeholdsjobbtyper. Det er også mulig å legge til flere sjekklister for vedlikehold.

## <a name="fill-out-a-maintenance-checklist"></a>Fylle ut en sjekkliste for vedlikehold

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren, og klikk på **Sjekkliste for vedlikehold**.

3. I **Sjekkliste for vedlikeholdsjobb for arbeidsordre** ser du sjekklistene for vedlikehold for alle arbeidsordrejobber. Hvis arbeidsordrejobbene har forskjellige vedlikeholdsjobbtyper, kan vedlikeholdssjekklistene være forskjellige på hver arbeidsordrejobb. Velg en arbeidsordrejobb for å arbeide med tilknyttet kontrolliste for vedlikehold. Detaljer for en valgt vedlikeholdssjekklistelinje vises i hurtigfanen **Linjedetaljer**.

4. Fullfør alle sjekklistelinjene for vedlikehold, én om gangen, i den sekvensielle rekkefølgen de vises. En vedlikeholdssjekklistelinje av typen Hode brukes som en overskrift for å gruppere vedlikeholdssjekklistelinjene nedenfor. Det er ikke nødvendig å fylle ut et hode, men som for alle typer vedlikeholdssjekklistelinjer er det mulig å legge til en **merknad** i toppteksten.

5. Hvis instruksjoner er knyttet til en vedlikeholdssjekklistelinje, er avmerkingsboksen **Instruksjoner** merket. Les instruksjonene for den valgte vedlikeholdssjekklistelinjen i hurtigfanen **Linjedetaljer** > **Instruksjoner**.

6. Informasjonen som kreves for å fullføre en vedlikeholdssjekklistelinje, kan variere, avhengig av den tilknyttede vedlikeholdssjekklistetypen. Du fullfører en vedlikeholdssjekklistelinje ved å fylle ut feltene i hurtigfanen **Linjedetaljer**. På en linje av typen Tekst kan du for eksempel legge til en **merknad** som forklarer hva som var resultatet av denne sjekklistelinjen. På en linje av typen Måling kan du legge til **tellerverdien** du leser på utstyret, og du kan også legge til en **merknad** hvis det er nødvendig.

- Når du har fullført en vedlikeholdssjekklistelinje, merker du av for **Kontrollert** på linjen for å merke den som fullført. Hvis du vil forkaste en vedlikeholdssjekklistelinje fordi den ikke er relevant for arbeidsordrejobben, merker du av for **I/T** på linjen. Hvis en vedlikeholdssjekklistelinje er merket som **Obligatorisk**, må du merke den som enten Kontrollert eller I/T.  
- Du kan bare oppdatere vedlikeholdssjekklisteregistreringer hvis arbeidsordren er i en [aktiv](../setup-for-work-orders/work-order-lifecycle-states.md) livssyklustilstand.  


## <a name="add-a-maintenance-checklist-line"></a>Legge til en linje i sjekkliste for vedlikehold

Sjekklister for vedlikehold opprettes fra definisjonen for standard vedlikeholdsjobbtype og overføres til en arbeidsordrejobb. Om nødvendig kan du legge til vedlikeholdssjekklistelinjer i en arbeidsordrejobb. Manuelt tilføyde sjekklistelinjer får referansen Manuell.

1. I **Sjekkliste for vedlikeholdsjobb for arbeidsordre** velger du arbeidsordrejobben som du vil legge til en vedlikeholdssjekkliste for.

2. Velg en linje for vedlikeholdssjekkliste på hurtigfanen **Vedlikeholdssjekklistelinjer**, og trykk deretter på pil ned-knappen på tastaturet hvis du vil sette inn en ny linje etter den valgte linjen for vedlikeholdssjekkliste. Det neste nummeret i sekvensen settes automatisk inn fra **Linjenummer**-feltet. Du kan også velge en vedlikeholdssjekklistelinje og klikke på knappen **Legg til linje** hvis du vil sette inn en ny linje over den valgte sjekklistelinjen.

3. Sett inn et navn på vedlikeholdssjekklistelinjen i **Navn**-feltet.

4. Velg en type for vedlikeholdssjekklistelinjen i **Type**-feltet. For hver type vedlikeholdssjekkliste vises de relaterte feltene i hurtigfanen **Linjedetaljer**.  
  a. "Tekst" brukes for å legge til en vedlikeholdssjekklistelinje med en tekstbeskrivelse av hva som skal gjøres. Denne vedlikeholdssjekklistetypen kan brukes hvis du vil at en arbeider skal sjekke eller inspisere noe, uten å forvente et bestemt (målbart) resultat. Sett inn en beskrivelse av hva som skal gjøres, i **Instruksjoner**-delen på hurtigfanen **Linjedetaljer**. b. "Hode" brukes som en overskrift for å gruppere vedlikeholdssjekklistelinjene som vises under hodet. Dette er nyttig hvis du har flere vedlikeholdssjekklistelinjer som kan deles inn i bestemte områder. Sett inn et beskrivende navn i **Navn**-feltet.  
  c. "Mal" er ikke tilgjengelig når du legger til en vedlikeholdssjekklistelinje manuelt i en arbeidsordrejobb.  
  d. "Variabel" brukes til å definere et mulig resultat i et område på en vedlikeholdssjekklistelinje. Oppsettet av variabler for vedlikeholdssjekkliste er beskrevet i [Kategorier for vedlikeholdsjobbtyper og vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtyper, vedlikeholdsjobbfag og sjekklister for vedlikehold](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Sett inn et navn for å beskrive variabelen i **Navn**-feltet. I **Variabel**-feltet velger du variabelen. Sett inn en beskrivelse av hva som skal gjøres, i **Instruksjoner**-delen på hurtigfanen **Linjedetaljer**.  
  e. "Måling" brukes til å registrere en bestemt måling. Sett inn et navn på målingen i **Navn**-feltet. Velg **Teller** og **Enhet**på hurtigfanen **Linjedetaljer**. Sett inn en beskrivelse av hva som skal gjøres, i **Instruksjoner**-delen.  

5. Når du er ferdig med å legge til vedlikeholdssjekklistelinjer manuelt, fyller du ut linjene som beskrevet i delen ovenfor.

>[!NOTE]
>I **Sjekkliste for vedlikeholdsjobb for arbeidsordre** kan du ikke slette vedlikeholdssjekklistelinjer med referansen Jobbtype. Du kan bare slette vedlikeholdssjekklistelinjer med referansen "Manuell", som du eller andre vedlikeholdspersoner har opprettet manuelt.


![Figur 1](media/14-work-orders.png)

