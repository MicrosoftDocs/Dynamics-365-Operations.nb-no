---
title: Manuelt opprettede arbeidsordrer
description: Denne artikkelen forklarer hvordan du oppretter arbeidsordrer manuelt i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5d2cc1f5b8eccb51b6bea8655fdee243c1a2df55
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015034"
---
# <a name="manually-created-work-orders"></a>Manuelt opprettede arbeidsordrer

[!include [banner](../../includes/banner.md)]


Du kan opprette arbeidsordrer manuelt på to måter:

- På siden **Alle arbeidsordrer** eller **Aktive arbeidsordrer** 
- På siden **Alle meldinger** eller **Aktive meldinger** eller **Mine meldinger for funksjonslokasjon** 

## <a name="create-work-order"></a>Opprett arbeidsordre

1. Velg **Aktivastyring** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg **Ny**.

3. I dialogboksen **Opprett arbeidsordre** velger du en arbeidsordretype i feltet **Arbeidsordretype**.

4. Velg en **Beskrivelse** om nødvendig.

5. Velg feltet **Aktivum** velger du aktivumet.

>[!NOTE]
>Når du velger et aktivum, kan tre kategorier være tilgjengelige i rullegardinlisten **Aktivum**: 

- fanen **Aktive aktiva** – Denne fanen inneholder en liste over alle aktiva med en "Aktiv" livssyklustilstand. 
- **Aktivavisning** – Denne fanen viser en trevisning av funksjonslokasjoner og aktiva som er installert på dem.
- **Mine aktiva** – Denne fanen inneholder aktiva som er relatert til funksjonslokasjonene som du (arbeideren som er logget på systemet) kan tildeles. (Hvis du vil ha informasjon om oppsettet, kan du se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md).) Hvis ingen funksjonslokasjoner er definert for en arbeider i [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md), er ikke fanen **Mine aktiva** tilgjengelig. 

6. I feltet **Vedlikeholdsjobbtype** velger du en vedlikeholdsjobbtype for arbeidsordren.

7. Velg om nødvendig **Variant av vedlikeholdsjobbtype** og **Handel**.

8. Hvis det er nødvendig, kan du endre servicenivået for arbeidsordren i **Servicenivå**-feltet.

9. Velg **Forventet startdato** og **Forventet sluttdato** i de tilknyttede feltene.

10. Klikk på **OK** for å opprette arbeidsordren.

11. På listesiden **Alle arbeidsordrer** kan du redigere arbeidsordren etter behov.

Merk følgende punkt:

- I detaljvisningen på listesiden **Alle arbeidsordrer** kan du legge til flere aktiva i en arbeidsordre ved å legge til linjer i hurtigfanen **Vedlikeholdsjobber for arbeidsordre**. I et aktivum kan du bare velge vedlikeholdsjobbtypene som er definert for aktivatypen som er valgt for aktivumet.  

- Hvis du endrer servicenivået eller aktivakritikalitet for aktivumet etter at du har brukt det på en arbeidsordre, oppdateres ikke servicenivået eller kritikaliteten i arbeidsordren i henhold til dette. Hvis du vil ha mer informasjon om servicenivåer og kritikaliteter, se [Tjenestenivåer for aktiva](../setup-for-objects/object-priorities.md) og [Type kritisk aktivitet for aktiva](../setup-for-objects/object-criticalities.md).

- Kritikaliteten i en arbeidsordre beregnes på nytt hver gang en arbeidsordrejobb legges til eller slettes fra arbeidsordren.

- I detaljvisningen **Alle arbeidsordrer** > fanen **Hode** > **Plan**-hurtigfanen i feltet **Ansvarlig gruppe** eller **Ansvarlig** kan du velge en ansvarlig vedlikeholdspersongruppe eller en ansvarlig vedlikeholdsperson. Disse innstillingene kan endres mens arbeidsordren er aktiv. De kan for eksempel endres når tilstanden for arbeidsordrelivssyklusen endres. Det automatiske valget som gjøres under opprettingen av arbeidsordrer, er basert på oppsettet på siden **Ansvarlige vedlikeholdspersoner**. Hvis du legger til eller fjerner arbeidsordrejobber etter at du har opprettet en arbeidsordre, og hvis feltene **Ansvarlig gruppe** og **Ansvarlig** er tomme når du oppdaterer arbeidsordren, søker Aktivastyring etter en ansvarlig vedlikeholdspersongruppe eller en ansvarlig vedlikeholdsperson. Hvis **Ansvarlig gruppe**-feltet eller **Ansvarlig**-feltet allerede er angitt når du oppdaterer arbeidsordren, gjøres det ingen endringer. Hvis du vil ha informasjon om ansvarlige vedlikeholdspersoner og arbeidergrupper, kan du se [Ansvarlige vedlikeholdspersoner](../setup-for-maintenance-requests/responsible-workers.md).

- På siden [Vedlikeholdsstatus](../controlling-and-reporting/maintenance-status.md) kan du gjøre en beregning for å få en oversikt over arbeidsbelastningen for innkommende og fullførte arbeidsordrer.  

- I detaljvisningen på siden **Alle arbeidsordrer** i hurtigfanen **Linjedetaljer** kan du bruke feltene **Breddegrad** og **Lengdegrad** til å legge til geografiske koordinater for aktiva som er valgt i arbeidsordrejobben.  


## <a name="create-related-work-order"></a>Opprett relatert arbeidsordre

Du kan opprette en arbeidsordre som er knyttet til en eksisterende arbeidsordre. Denne funksjonen er nyttig hvis du for eksempel vil arbeide med primære og sekundære arbeidsordrer. En ny arbeidsordre er basert på en arbeidsordrejobb fra en eksisterende arbeidsordre.

1. Velg **Aktivastyring** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren du vil opprette en relatert arbeidsordre for.

3. Velg **Relatert arbeidsordre** i gruppen **Ny** i **Arbeidsordre**-fanen i handlingsruten.

4. I dialogboksen **Opprett relatert arbeidsordre** velger du arbeidsordrejobben som du vil opprette en tilknyttet arbeidsordre for, i feltet **Arbeidsordrejobb**.

5. Velg en vedlikeholdsjobbtype i feltet **Vedlikeholdsjobbtype**.

6. Velg en relatert vedlikeholdsjobbtypevariant og -handel i feltene **Variant av vedlikeholdsjobbtype** og **Handel** etter behov.

7. Hvis denne arbeidsordren er den første tilknyttede arbeidsordren som er opprettet for den valgte arbeidsordren, følger du denne fremgangsmåten:
    1. Velg alternativet **Ny arbeidsordre**.
    2. Velg en arbeidsordretype i feltet **Arbeidsordretype**.
    3. Angi en beskrivelse i **Beskrivelse**-feltet.
    4. Hvis det er nødvendig, endrer du servicenivået for arbeidsordren i **Servicenivå**-feltet.
    5. Velg start- og sluttdatoer i feltene **Forventet start** og **Forventet slutt**.
    6. Velg **OK**. Den nye tilknyttede arbeidsordren vises på listesiden **Alle arbeidsordrer**.  

8. Hvis arbeidsrekkefølgen du oppretter denne tilknyttede arbeidsordren for, allerede har tilknyttede arbeidsordrer, følger du denne fremgangsmåten for å legge til en ny arbeidsordrejobb i en eksisterende relatert arbeidsordre:
    1. Velg alternativet **Legg til tilknyttet arbeidsordre**.
    2. Velg den tilknyttede arbeidsordren som du vil legge til en ny arbeidsordrejobb i, i feltet **Arbeidsordre**.
    3. Hvis det er nødvendig, endrer du servicenivået for arbeidsordren i **Servicenivå**-feltet.
    4. Endre start- og sluttdatoer i feltene **Forventet start** og **Forventet slutt** etter behov.
    5. Velg **OK**. Arbeidsordrejobben legges til den eksisterende tilknyttede arbeidsordren.

Illustrasjonen nedenfor viser et eksempel på dialogboksen **Opprett relatert arbeidsordre**.

![Figur 1.](media/03-work-orders.png)

>[!NOTE]
>Hvis du har definert en relatert arbeidsordremaske i **Aktivabehandlingsparametere** > **Arbeidsordrer**-fanen > **Relatert arbeidsordremaske**-feltet, blir det opprettet arbeidsordre-ID-er i samsvar med maskeoppsettet. Hvis det ikke er definert en tilknyttet arbeidsordremaske, vil den neste tilgjengelige arbeidsordre-ID-en brukes for tilknyttede arbeidsordrer.

## <a name="copy-a-work-order"></a>Kopiere en arbeidsordre

Du kan opprette en ny arbeidsordre fra en eksisterende arbeidsordre raskt. Denne måten å arbeide med arbeidsordrer på er forskjellig fra å opprette arbeidsordrer basert på [vedlikeholdsplaner](../preventive-and-reactive-maintenance/maintenance-plans.md). Det er nyttig hvis du for eksempel har en arbeidsordre med mange arbeidsordrejobber, og de ulike jobbene skal fullføres på ulike aktiva med jevne mellomrom.

1. Velg **Aktivastyring** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren du vil kopiere innhold fra.

3. Velg **Kopier arbeidsordre** i gruppen **Ny** i fanen **Arbeidsordre** i handlingsruten.

4. Arbeidsordreoppsettet fra den valgte arbeidsordren vises. Du kan redigere noen av feltene etter behov.

5. Velg **OK** for å opprette den nye arbeidsordren.

6. På listesiden **Alle arbeidsordrer** kan du redigere arbeidsordren etter behov.

>[!NOTE]
>Når den nye arbeidsordren opprettes, kopieres noe informasjon direkte fra den eksisterende arbeidsordren. Informasjon om prognoser, verktøy, kontrollister for vedlikehold, funksjonsplassering, adresser og planlegging kopieres ikke. Den initialiseres i stedet fra det gjeldende oppsettet i aktivastyring. Hvis denne informasjonen ble endret fra tiden da den første arbeidsordren ble opprettet, og tidspunktet da du laget en kopi av arbeidsordren, blir imidlertid endringene tatt med i den nye arbeidsordren. Eksempler inneholder endringer for prognoser eller oppdateringer av kontrollister for vedlikehold.

Illustrasjonen nedenfor viser et eksempel på dialogboksen **Kopier arbeidsordre**.

![Figur 2.](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Opprette en arbeidsordre basert på en melding

1. Velg **Aktivastyring** > **Meldinger** > **Alle meldinger** eller **Aktive meldinger**.

2. Velg meldingen du vil opprette en arbeidsordre for, og klikk på **Rediger**.

3. Velg **Arbeidsordre** i gruppen **Ny** i fanen **Melding** i handlingsruten.

4. I dialogboksen **Arbeidsordre** angir du feltene. Hvis en vedlikeholdsjobbtype er valgt i meldingen, kan du velge en annen vedlikeholdsjobbtype når du oppretter arbeidsordren, etter behov.

5. Velg **OK**. En meldingen forteller deg at en arbeidsordre er blitt opprettet.

6. Hvis du vil se hvilke arbeidsordrer som er knyttet til en melding, velger du meldingen på listesiden **Alle meldinger** eller **Aktive meldinger**. Deretter velger du **Arbeidsordre** i gruppen **Vis** i fanen **Melding** i handlingsruten.


Illustrasjonen nedenfor viser et eksempel på dialogboksen **Opprett arbeidsordre**.

![Figur 3.](media/05-work-orders.png)


>[!NOTE]
>Hvis du vil at arbeidsordrer skal opprettes automatisk, kan du planlegge vedlikeholdsplanjobber, eller du kan konfigurere "Opprett automatisk" [vedlikeholdsplaner](../preventive-and-reactive-maintenance/maintenance-plans.md) eller [vedlikeholdsrunder](../preventive-and-reactive-maintenance/maintenance-rounds.md) på aktivumet. Arbeidsordrer som opprettes fra meldinger på listesiden **Alle vedlikeholdsplaner**, har vedlikeholdsjobbtypene som er valgt på meldingene.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]