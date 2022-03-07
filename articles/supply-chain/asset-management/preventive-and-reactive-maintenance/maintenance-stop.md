---
title: Vedlikeholdsnedetid
description: Dette emnet forklarer hvordan nedetid ved vedlikehold brukes til å få en oversikt over kapasiteten som kreves for å utføre vedlikeholdsjobber på bestemte aktiva i en bestemt periode.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e9d024a5096b499b986ec2d5c38c0d6a2b7794d3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356494"
---
# <a name="maintenance-downtime-activities"></a>Vedlikeholdsnedetid

[!include [banner](../../includes/banner.md)]

Nedetid ved vedlikehold brukes til å få en oversikt over kapasiteten som kreves for å utføre vedlikeholdsjobber på bestemte aktiva i en bestemt periode. Du kan for eksempel opprette en registrering av vedlikeholdsnedetid for produksjonslinje 10 i produksjonshall 29-A på produksjonsområde 02. Vedlikeholdsnedetidregistreringen har et start- og sluttidspunkt som angir perioden som aktivaene knyttet til vedlikeholdsstoppen ikke er tilgjengelige for produksjon.

**Aktiviteter for vedlikeholdsnedetid** er en oversikt over vedlikeholdsplanlinjer og vedlikeholdsjobber for arbeidsordre på aktuelle aktiva i en bestemt periode. Linjene knyttet til vedlikeholdsjobber for arbeidsordre har alle en forventet startdato innenfor vedlikeholdsstopperioden. Du kan trekke ut nyttig informasjon og foreta justeringer i planlagte vedlikeholdsjobber:

- Få en oversikt over nødvendige driftsstansperioder for produksjonsutstyr (aktiva).  
- Få en oversikt over planlagt vedlikehold (timer) gruppert etter kompetanse (ansvarlige vedlikeholdspersongrupper eller vedlikeholdspersoner), for eksempel kapasitetsbelastning på elektrikere, smeder eller andre vedlikeholdsarbeidsgrupper som kreves for å gjøre de planlagte vedlikeholdsjobbene.  
- Foreta justeringer i vedlikeholdsplanlinjer eller arbeidsordrevedlikeholdsjobber knyttet til aktivaene, for eksempel endre forventet start- og sluttidspunkt på en linje eller velge andre vedlikeholdspersoner for å optimalisere arbeidsflyten for vedlikeholdspersoner og vedlikeholdspersongrupper.

Når det er valgt aktiva i en registrering av vedlikeholdsnedetid, inkluderes alle åpne vedlikeholdsplanlinjer og vedlikeholdsjobber i arbeidsordrer knyttet til aktive arbeidsordrer, i registreringen.

## <a name="maintenance-downtime-activities"></a>Aktiviteter for nedetid ved vedlikehold

Klikk på **Aktivastyring** > **Felles** > **Aktiviteter for vedlikeholdsnedetid** > **Alle aktiviteter for vedlikeholdsnedetid** for å åpne en liste over alle aktivitetene for vedlikeholdsnedetid og se informasjon om aktivitetene. Klikk på en kobling i kolonnen **Aktiviteter for vedlikeholdsnedetid** for å åpne detaljvisningen. Illustrasjonen nedenfor viser et eksempel på listen **Aktiviteter for vedlikeholdsnedetid**.

![Figur 1.](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Opprette en aktivitet for vedlikeholdsnedetid

1. Klikk på **Aktivastyring** > **Felles** > **Aktiviteter for vedlikeholdsnedetid** > **Alle aktiviteter for vedlikeholdsnedetid** eller **Aktive aktiviteter for vedlikeholdsnedetid**.

2. Klikk på **Ny**.

3. Sett inn en ID i **Aktiviteter for vedlikeholdsnedetid**-feltet og et navn i **Navn**-feltet.

4. Sett inn perioden for vedlikeholdsstoppen i feltene **Startdato/-klokkeslett** og **Sluttdato/-klokkeslett**.

5. I hurtigfanen **Aktiva for aktiviteter for vedlikeholdsnedetid** klikker du på **Legg til linje** for å legge til aktiva, ett om gangen, i vedlikeholdsnedetidsaktiviteten.

6. Klikk på **Lagre** når alle aktivaene er lagt til. Illustrasjonen nedenfor viser et eksempel på en aktivitet for vedlikeholdsnedetid med tilknyttede aktiva og vedlikeholdsjobber.

7. Vedlikeholdsjobbene for arbeidsordrer og åpne vedlikeholdsplanlinjer for de valgte aktivaene vises i hurtigfanene **Resulterende vedlikeholdsjobber for arbeidsordrer** og **Vedlikeholdsplanlinjer**. I hurtigfanen **Generelt** > **Arbeidsordrer**-gruppen > **Vedlikeholdsprognosetimer**-feltet og hurtigfanen **Generelt** > **Vedlikeholdsplan**-gruppen > **Vedlikeholdsprognosetimer**-feltet , ser du totalt antall timer anslått for vedlikeholdsjobber for arbeidsordrer og vedlikeholdsplanlinjer.

Illustrasjonen nedenfor viser et eksempel på detaljvisningen **Aktiviteter for vedlikeholdsnedetid**.

![Figur 2.](media/20-preventive-maintenance.png)

>[!NOTE]
>Vedlikeholdsjobbene for arbeidsordrer og vedlikeholdsplanlinjene som er relatert til de valgte aktivaene, oppdateres automatisk hvis nye arbeidsordrer eller vedlikeholdsplanlinjer opprettes etter at du har opprettet aktiviteten for vedlikeholdsnedetid. Hvis du for eksempel planlegger vedlikeholdsplaner eller vedlikeholdsrunder for de tilknyttede aktivaene to dager etter at aktiviteten for vedlikeholdsnedetid ble opprettet, legges nye vedlikeholdsplanlinjer automatisk til i vedlikeholdsnedetidsaktiviteten.

8. I **Alle aktiviteter for vedlikeholdsnedetid** > **Aktiviteter for vedlikeholdsnedetid** > velger du en aktivitet for vedlikeholdsnedetid i listen og klikker på **Kapasitetsbelastning** for å åpne dialogboksen **Beregn kapasitetsbelastning**. Bruk denne dialogboksen til å få en oversikt over kapasitetsbelastning på for eksempel datoer, aktiva, aktivatyper og vedlikeholdsjobbtyper. Legg merke til at datoene som vises i dialogboksen, er start- og sluttdatoene som er valgt i **Aktiviteter for vedlikeholdsnedetid**. Denne beregningen omfatter aktivaene knyttet til aktiviteten for vedlikeholdsnedetid.

9. I dialogboksen **Beregn kapasitetsbelastning** redigerer du start- og sluttidspunktene om nødvendig, og velger om du vil ta med arbeidsordrer og vedlikeholdsplaner i beregningen. Du kan bruke **Nivå**-feltet til å angi hvor detaljert beregningen av kapasitetsbelastning skal være når det gjelder arbeidssted. Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle aktivaene for et arbeidssted som er valgt i aktiviteten for vedlikeholdsnedetid, på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle kapasitetsbelastningslinjene på alle arbeidsstedsnivåene de er relatert til.

10. Klikk på **OK** for å starte beregningen. Totalt antall timer vises i oversikten **Kapasitetsbelastning**. I fanen **Kapasitetsbelastning** > **Grupper etter...**-handlingsrutegruppene klikker du på de relevante knappene for å få en mer detaljert oversikt over fordelingen av prognosetimer. Illustrasjonen nedenfor viser resultatet av en **Kapasitetsbelastning**-beregning.

![Figur 3.](media/21-preventive-maintenance.png)

11. Når du har fått en oversikt over kapasitetsbelastningen, hvis du vil foreta justeringer på vedlikeholdsjobber for arbeidsordrer eller vedlikeholdsplanlinjer, går du tilbake til detaljvisningen **Aktiviteter for vedlikeholdsnedetid** og velger linjene du vil justere i hurtigfanene **Resulterende vedlikeholdsjobber for arbeidsordrer** og **Vedlikeholdsplanlinjer**.

12. Klikk på **Juster**-knappen og oppdater forventede start- og sluttdatoer, servicenivå eller ansvarlige vedlikeholdspersoner for de valgte vedlikeholdsjobbene for arbeidsordrer eller vedlikeholdsplanlinjene.

13. Klikk på **OK** når du har gjort de nødvendige justeringene. 

>[!NOTE]
>Vedlikeholdsjobber for arbeidsordrer og vedlikeholdsplanlinjer som ikke er inkludert i vedlikeholdsnedetidsperioden etter at du har gjort justeringene, fjernes automatisk fra **Aktiviteter for vedlikeholdsnedetid**.

14. I **Alle aktiviteter for vedlikeholdsnedetid** > **Aktiviteter for vedlikeholdsnedetid** > velger du en aktivitet for vedlikeholdsnedetid i listen og klikker på **Vareprognose** for å åpne dialogboksen **Beregn vareprognose**. Bruk denne dialogboksen til å beregne prognoser for varer (reservedeler og andre nødvendige varer), og grupper dem for å få en oversikt, for eksempel etter dato, aktiva, aktivatype og vedlikeholdsjobbtype. Legg merke til at datoene som vises i dialogboksen, er start- og sluttdatoene som er valgt i **Aktiviteter for vedlikeholdsnedetid**. Denne beregningen omfatter reservedeler og varer knyttet til aktivaene som er valgt i aktiviteten for vedlikeholdsnedetid.

15. I dialogboksen **Beregn vareprognose** redigerer du start- og sluttidspunktene om nødvendig, og velger om du vil ta med arbeidsordrer og vedlikeholdsplaner i beregningen. Du kan bruke **Nivå**-feltet til å angi hvor detaljert beregningen av kapasitetsbelastning skal være når det gjelder arbeidssted. Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle aktivaene for et arbeidssted som er valgt i aktiviteten for vedlikeholdsnedetid, på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle kapasitetsbelastningslinjene på alle arbeidsstedsnivåene de er relatert til.

16. Klikk på **OK** for å starte beregningen. Totalt antall vareprognoser vises i oversikten **Vareprognose**. I fanen **Vareprognose** > **Grupper etter...**-handlingsrutegruppene klikker du på de relevante knappene for å få en mer detaljert oversikt over fordelingen av prognosevarer. Illustrasjonen nedenfor viser resultatet av en **Vareprognose**-beregning.

![Figur 4.](media/22-preventive-maintenance.png)

- Du kan kopiere aktiva fra én aktivitet for vedlikeholdsnedetid til en annen. I **Alle aktiviteter for vedlikeholdsnedetid** velger du **Kopier aktiviteter for vedlikeholdsnedetid**-knappen, gjør valgene i feltene **Fra aktiviteter for vedlikeholdsnedetid** og **Til aktiviteter for vedlikeholdsnedetid**, og klikker på **OK**.
- I **Alle aktiviteter for vedlikeholdsnedetid** klikker du på knappen **Vedlikeholdsplanlinjer** eller **Aktive arbeidsordrer** for å åpne de tilknyttede listene og vise linjene som er knyttet til den valgte aktiviteten for vedlikeholdsnedetid.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]