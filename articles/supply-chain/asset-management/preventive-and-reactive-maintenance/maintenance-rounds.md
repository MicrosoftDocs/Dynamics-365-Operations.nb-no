---
title: Vedlikeholdsrunder
description: Dette emnet beskriver vedlikeholdsrunder i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 63cb2614b2037fac1129c7d2f82a26dac41a3490
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434442"
---
# <a name="maintenance-rounds"></a>Vedlikeholdsrunder

[!include [banner](../../includes/banner.md)]

 

I **Aktivastyring** kan du opprette vedlikeholdsrunder for ulike aktiva, der du må utføre en lignende oppgave med jevne mellomrom. For eksempel smørejobber eller sikkerhetsinspeksjonsjobber som må utføres på flere maskiner i samme intervall. Første trinn er å opprette en vedlikeholdsrunde, inkludert aktiva som krever samme form for vedlikeholdsjobb. Deretter planlegger du vedlikeholdsrundene. Når du har fullført vedlikeholdsrundeplanen, kan du se alle jobbpostene knyttet til runden i **Alle vedlikeholdsplaner** og **Åpne vedlikeholdsplanlinjer**.

>[!NOTE]
>Vedlikeholdsrunder kan også defineres på arbeidssteder, som skal fullføres for aktivaene på arbeidsstedet når den rundebaserte arbeidsordren opprettes. Se [Opprette arbeidssteder](../functional-locations/create-functional-locations.md) hvis du vil ha mer informasjon om oppsettet av vedlikeholdsrunder på arbeidssteder.

## <a name="set-up-a-maintenance-round"></a>Sette opp en vedlikeholdsrunde

1. Klikk på **Aktivastyring** > **Oppsett** > **Forebyggende vedlikehold** > **Vedlikeholdsrunder**.

2. Klikk på **Ny** for å opprette en ny vedlikeholdsrunde.

3. Sett inn en ID i **Vedlikeholdsrunde**-feltet og et navn på vedlikeholdsrunden i **Navn**-feltet.

4. Velg en startdato for runden i **Startdato**-feltet.

5. I feltene **Fullfør innen dager** og **Fullfør innen timer** kan du sette inn forventet sluttdato i dager eller timer. Den forventede sluttdatoen beregnes i forhold til startdatoen, som beregnes når vedlikeholdsplanlinjer opprettes. Du kan for eksempel sette inn 7 i feltet **Fullfør innen dager** for å angi at den tilknyttede jobben skal fullføres innen en uke fra startdatoen.

6. Velg Ja på **Opprett automatisk**-veksleknappen hvis arbeidsordrer skal opprettes automatisk fra vedlikeholdsplanlinjer som er opprettet fra vedlikeholdsrunden.

7. I **Arbeidsordretype**-feltet velger du arbeidsordretypen som skal brukes på arbeidsordrer som opprettes fra denne vedlikeholdsrunden.

8. I **Servicenivå**-feltet velger du arbeidsordreservicenivået som skal brukes på arbeidsordrer som opprettes fra denne vedlikeholdsrunden.

9. I hurtigfanen **Aktivalinjer** klikker du på **Legg til** for å legge til et aktivum i vedlikeholdsrunden.

10. Et linjenummer settes inn automatisk i **Linjenummer**-feltet for å angi rekkefølgen på aktivaene i vedlikeholdsrunden.

11. Velg aktivaet i **Aktivum**-feltet.

12. Velg vedlikeholdsjobbtypen for aktivaet i **Vedlikeholdsjobbtype**-feltet.

13. Velg om nødvendig **Variant av vedlikeholdsjobbtype** og **Handel** som er knyttet til vedlikeholdsjobbtypen.

14. Velg gjentakelse (dag, uke osv.) i **Periodetype**-feltet.

15. I **Periodefrekvens**-feltet setter du inn antall gjentakelser for vedlikeholdsrunden. Eksempel: Hvis du har valgt Dag i feltet **Periodetype**, og du setter inn tallet 7 i dette feltet, opprettes det nye vedlikeholdsrundelinjer under forebyggende vedlikeholdsplanlegging én gang i uken.

16. Velg en startdato for aktivaet som skal inkluderes i vedlikeholdsrunden, i **Startdato**-feltet. Denne datoen kan være forskjellig fra startdatoen som er angitt i vedlikeholdsrunden.

17. Gjenta trinn 9–16 for å legge til flere aktiva i vedlikeholdsrunden.

18. I hurtigfanen **Arbeidsstedslinjer** klikker du på **Legg til** for å legge til et arbeidssted i vedlikeholdsrunden. Se beskrivelsen for de relaterte feltene ovenfor. De samme feltene er tilgjengelige som for å opprette en aktivalinje, men du kan også velge **Produsent** og **Modell** for et arbeidssted, om nødvendig. Hvis du bare velger et arbeidssted på en linje, men ikke gjør noen valg i **Aktivatype**, **Produsent**, **Modell**, **Vedlikeholdsjobbtype**, **Variant av vedlikeholdsjobbtype** og **Handel**, vil alle aktiva som er knyttet til dette arbeidsstedet på tidspunktet for vedlikeholdsplanlegging, bli inkludert i vedlikeholdsrunden.

19. Klikk på **Legg til** i hurtigfanen **Puljer** for å velge en arbeidsordrepulje som skal tas med i vedlikeholdsrunden. Flere arbeidsordrepuljer kan kobles til én vedlikeholdsrunde.

20. Lagre oppsettet.

>[!NOTE]
>Feltene **Aktiva** og **Linjer** i **Detaljer**-gruppen i hurtigfanen **Hode** viser antall aktiva og linjer knyttet til den valgte vedlikeholdsrunden.

Illustrasjonen nedenfor viser et eksempel på en vedlikeholdsrunding som inneholder tre aktiva.

![Figur 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Planlegg vedlikeholdsrunder

Når du har definert en vedlikeholdsrunde, kjører du en planleggingsjobb for å planlegge alle jobbene som er knyttet til vedlikeholdsrunden.

1. Klikk på **Aktivastyring** > **Periodisk** > **Forebyggende vedlikehold** > **Planlegg vedlikeholdsrunder**, eller **Aktivastyring** > **Felles** > **Vedlikeholdsplan** > **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer** eller **Åpne vedlikeholdsplanpuljer** > velg vedlikeholdsplanlinje i listen > **Vedlikeholdsrunder**-knappen.

2. I feltet **Periode** velger du periodetypen som skal brukes for planleggingsjobben.

3. I **Periodefrekvens**-feltet setter du inn antall perioder som skal være med i planleggingsjobben. Starten på planleggingen er gjeldende dato.

4. Velg Ja på veksleknappen **Opprett automatisk** hvis det automatisk skal opprettes en arbeidsordre på grunnlag av en vedlikeholdsrunde.

>[!NOTE]
>Hvis denne veksleknappen er satt til Ja, og veksleknappen **Opprett automatisk** også er satt til Ja for vedlikeholdsrunden i **Vedlikeholdsrunder**-skjemaet, opprettes arbeidsordrer på grunnlag av vedlikeholdsrundelinjene, og vedlikeholdsplanlinjer med statusen "Arbeidsordre opprettet" opprettes også. Hvis bare en av **Opprett automatisk**-veksleknappene er satt til Ja, i denne rullegardinlisten eller i **Vedlikeholdsrunder**, blir bare vedlikeholdsplanlinjer opprettet med statusen "Opprettet". I dette tilfellet opprettes ingen arbeidsordrer.

5. Hvis nødvendig, kan du velge bestemte runder eller en annen startdato for planleggingsjobben. Klikk på **Filter**, og legg til rundene som skal tas med.

6. Klikk **OK**.

7. Du kan nå vise vedlikeholdsrundejobbene i **Aktivastyring** > **Felles** > **Vedlikeholdsplan** > **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer**. Hvis de planlagte runden er koblet til en arbeidsordrepulje, kan du også se vedlikeholdsplanlinjer i **Åpne vedlikeholdsplanpuljer**. Vedlikeholdsplanlinjer som er opprettet fra en runde, har referansetypen Vedlikeholdsrunder.

De to illustrasjonene nedenfor viser en planlagt jobb dialogboksen **Planlegg vedlikeholdsrunder** og linjer for vedlikeholdsplan som er opprettet i **Alle vedlikeholdsplaner**, som er basert på den planlagte jobben.

![Figur 2](media/14-preventive-maintenance.png)

![Figur 3](media/15-preventive-maintenance.png)

- Når arbeidsordrer opprettes manuelt for aktiva som dekkes av en leverandørgaranti, vises en dialogboks for å gjøre brukeren oppmerksom på garantien. Opprettingen av arbeidsordren kan deretter avbrytes. Kontrollen av en garantirelasjon utelates for arbeidsordrer som opprettes automatisk.  
- Du kan sette opp en satsvis jobb i hurtigfanen **Kjør i bakgrunnen** for å planlegge runder med jevne mellomrom.  
- Hvis en runde er inkludert i flere arbeidsordrepuljer (se [Arbeidsordrepuljer](../work-orders/work-order-pools.md)), vises én post for hver pulje i **Åpne vedlikeholdsplanpuljer**. Dette gjøres for å optimalisere filtreringsalternativene for arbeidsordrepuljer.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]