---
title: Manuelt opprettede arbeidsordrer
description: Dette emnet forklarer hvordan du oppretter arbeidsordrer manuelt i Aktivastyring.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875818"
---
# <a name="manually-created-work-orders"></a>Manuelt opprettede arbeidsordrer

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Du kan opprette arbeidsordrer manuelt på to måter:

- i **Alle arbeidsordrer** eller **Aktive arbeidsordrer**  
- i **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler** eller **Mine vedlikeholdsforespørsler for arbeidssted**  

## <a name="create-work-order"></a>Opprett arbeidsordre

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Klikk på **Ny**-knappen.

3. I rullegardinlisten **Opprett arbeidsordre** velger du en arbeidsordretype.

4. Velg en beskrivelse om nødvendig.

5. Velg anleggsmiddelet for arbeidsordren og en vedlikeholdsjobbtype.

>[!NOTE]
>Når du velger et aktiva, kan tre kategorier være tilgjengelige: Kategorien **Mine aktiva** inneholder aktiva som er knyttet til arbeidsstedene der du (personen som er logget på systemet), kan være tilordnet (oppsett i [Vedlikeholdsarbeidere og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md)). Hvis ingen arbeidssteder er definert for en person i [Vedlikeholdsarbeidere og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md), er ikke kategorien **Mine aktiva** synlig. Kategorien **Aktive aktiva** inneholder en liste over alle aktiva med statusen "Aktiv" for livsløpstilstanden. Kategorien **Aktivavisning** viser en trevisning av arbeidssteder og aktiva som er installert på disse stedene.

6. Velg om nødvendig **Variant av vedlikeholdsjobbtype** og **Handel**.

7. Hvis det er nødvendig, kan du endre servicenivået for arbeidsordren i **Servicenivå**-feltet.

8. Velg forventet start- og sluttdato i de tilknyttede feltene.

9. Klikk på **OK** for å opprette en ny arbeidsordre.

10. Rediger arbeidsordren i **Alle arbeidsordrer** om nødvendig.

- I **Alle arbeidsordrer** kan du legge til flere aktiva i en arbeidsordre i detaljvisningen ved å legge til linjer i hurtigfanen **Vedlikeholdsjobber for arbeidsordre**. I et aktiva kan du bare velge vedlikeholdsjobbtypene som er definert for aktivatypen som er valgt for aktivaet.  
- Hvis du har endret et servicenivå for et anleggsmiddel eller en kritisk aktivitet for et anleggsmiddel etter at du har brukt dem i en arbeidsordre (se [Tjenestenivåer for aktiva](../setup-for-objects/object-priorities.md) og [Kritiske forhold omkring aktiva](../setup-for-objects/object-criticalities.md)), oppdateres ikke servicenivået eller kritikaliteten i arbeidsordren tilsvarende.
- Kritikaliteten i en arbeidsordre beregnes på nytt hver gang en arbeidsordrelinje legges til eller slettes i arbeidsordren.
- I **Alle arbeidsordrer**-detaljvisningen > **Hode**-visningen > **Plan**-hurtigfanen kan du velge en ansvarlig vedlikeholdspersongruppe eller en ansvarlig vedlikeholdsperson i feltene **Ansvarlig gruppe** eller **Ansvarlig**. Disse innstillingene kan endres så lenge arbeidsordren er aktiv, for eksempel når livssyklustilstanden for arbeidsordren endres. Det automatiske valget som gjøres under opprettingen av arbeidsordrer, er basert på oppsettet i **Ansvarlige vedlikeholdsarbeidere**. Hvis du legger til eller fjerner arbeidsordrejobber etter at du har opprettet en arbeidsordre, og **Ansvarlig gruppe**-feltet og **Ansvarlig**-feltet er tomme når du oppdaterer arbeidsordren, søker Aktivastyring etter et mulig treff i oppsettsskjemaet for en ansvarlig vedlikeholdspersongruppe eller ansvarlig vedlikeholdsperson. Hvis **Ansvarlig gruppe**-feltet eller **Ansvarlig**-feltet allerede er fylt ut når du oppdaterer arbeidsordren, gjøres det ingen endringer. 

- I **Vedlikeholdsstatus** kan du gjøre en beregning for å få en oversikt over arbeidsbelastningen for innkommende og fullførte arbeidsordrer.  

- I hurtigfanen **Linjedetaljer** bruker du feltene **Breddegrad** og **Lengdegrad** til å legge til geografiske koordinater for aktivaet som er valgt i arbeidsordrejobben.  

## <a name="create-related-work-order"></a>Opprett relatert arbeidsordre

Du kan opprette en relatert arbeidsordre til en eksisterende arbeidsordre hvis du for eksempel vil arbeide med primære og sekundære arbeidsordrer. En ny arbeidsordre er basert på en arbeidsordrejobb fra en eksisterende arbeidsordre.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren som du vil opprette en tilknyttet arbeidsordre for.

3. Klikk på **Relatert arbeidsordre**.

4. I rullegardinlisten **Opprett relatert arbeidsordre** velger du arbeidsordrejobben som du vil opprette en tilknyttet arbeidsordre for, i feltet **Arbeidsordrejobb**.

5. Velg en vedlikeholdsjobbtype i feltet **Vedlikeholdsjobbtype**, og, om nødvendig, en tilknyttet variant av vedlikeholdsjobbtype og handel i feltene **Variant av vedlikeholdsjobbtype** og **Handel**.

6. Hvis dette er den første tilknyttede arbeidsordren du oppretter, klikker du på alternativknappen **Ny arbeidsordre**.

7. Velg en **arbeidsordretype** og en **beskrivelse** i de tilknyttede feltene.

8. Hvis det er nødvendig, endrer du servicenivået for arbeidsordren i **Servicenivå**-feltet.

9. Sett inn forventet start- og sluttdato i de tilknyttede feltene.

10. Klikk **OK**. Den nye tilknyttede arbeidsordren vises i listen **Alle arbeidsordrer**.

11. Hvis du oppretter en relatert arbeidsordre i en arbeidsordre som allerede har tilknyttede arbeidsordrer, kan du legge til arbeidsordrejobben i en allerede tilknyttet arbeidsordre. Dette gjøres ved å klikke på alternativknappen **Legg til tilknyttet arbeidsordre** i trinn 6. Deretter velger du den tilknyttede arbeidsordren som du vil legge til en ny arbeidsordrejobb i. Rediger **Servicenivå**, **Forventet start**- og **Forventet slutt**-feltene etter behov, og klikk på **OK**. Arbeidsordrejobben legges til den eksisterende tilknyttede arbeidsordren.


![Figur 1](media/03-work-orders.png)

**Obs!** Hvis du har definert en relatert arbeidsordremaske i **Aktivabehandlingsparametere** > **Arbeidsordrer**-koblingen > **Relatert arbeidsordremaske**-feltet, blir det opprettet arbeidsordre-ID-er i samsvar med maskeoppsettet. Hvis det ikke er definert en tilknyttet arbeidsordremaske, vil den neste tilgjengelige arbeidsordre-ID-en brukes for tilknyttede arbeidsordrer.

## <a name="copy-work-order"></a>Kopier arbeidsordre

Det er mulig å opprette en ny arbeidsordre fra en eksisterende arbeidsordre raskt. Denne måten å arbeide med arbeidsordrer på er forskjellig fra å opprette arbeidsordrer basert på vedlikeholdsplaner. Det er nyttig hvis du for eksempel har en arbeidsordre med mange arbeidsordrejobber med ulike jobber for ulike anleggsmidler som skal fullføres med jevne mellomrom.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren du vil kopiere innhold fra.

3. Klikk på **Kopier arbeidsordre**. Arbeidsordreoppsettet fra den valgte arbeidsordren vises. Hvis det er nødvendig, kan du redigere noen av feltene.

4. Klikk på **OK** for å opprette den nye arbeidsordren.

5. Rediger arbeidsordren i **Alle arbeidsordrer** om nødvendig.

>[!NOTE]
>Når den nye arbeidsordren opprettes, kopieres noe informasjon direkte fra den eksisterende arbeidsordren. Informasjon om prognoser, verktøy, sjekklister for vedlikehold, arbeidssted, adresser og planlegging blir ikke kopiert, men initialisert fra gjeldende oppsett i Aktivastyring. Dette betyr at hvis det ble gjort endringer i disse dataene fra tidspunktet da den første arbeidsordren ble opprettet, til tidspunktet du opprettet en kopi av arbeidsordren, blir disse endringene tatt med i den nye arbeidsordren du har opprettet. Eksempler er endringer i prognoser eller oppdaterte kontrollister for vedlikehold.


![Figur 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Opprette arbeidsordre basert på en vedlikeholdsanmodning

1. Klikk på **Aktivastyring** > **Felles** > **Vedlikeholdsforespørsler** > **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler**.

2. Velg vedlikeholdsforespørselen du vil opprette en arbeidsordre for, og klikk på **Rediger**.

3. Klikk på **Arbeidsordre** i **Alle forespørsler**.

4. Fyll ut rullegardinlisten **Arbeidsordre**. Hvis en vedlikeholdsjobbtype er valgt i vedlikeholdsforespørselen, kan du velge en annen vedlikeholdsjobbtype, hvis det er nødvendig, når du oppretter arbeidsordren.

5. Klikk **OK**. Du vil se en melding som gir deg beskjed om at arbeidsordren er opprettet.

6. Hvis du vil se hvilke arbeidsordrer som er knyttet til en vedlikeholdsforespørsel, velger du vedlikeholdsforespørselen i listene **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler** og klikker på **Arbeidsordrer**-knappen.


![Figur 3](media/05-work-orders.png)


>[!NOTE]
>Arbeidsordrer kan også opprettes automatisk ved å planlegge vedlikeholdsplanjobber, eller ved å definere vedlikeholdsplaner for automatisk oppretting eller vedlikeholdsrunder for et anleggsmiddel. Arbeidsordrer opprettet fra vedlikeholdsforespørsler i **Vedlikeholdsplan** opprettes med vedlikeholdsjobbtypene som er valgt i vedlikeholdsforespørslene.

