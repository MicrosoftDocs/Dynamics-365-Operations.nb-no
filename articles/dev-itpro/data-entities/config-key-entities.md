---
title: "Konfigurasjonsnøkler og dataenheter"
description: "Dette emnet beskriver forholdet mellom konfigurasjonsnøkler og dataenheter i Microsoft Dynamics 365 for Finance and Operations."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: f5b6ab35f65dbe325f2202ab2dda71152993359d
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="configuration-keys-and-data-entities"></a>Konfigurasjonsnøkler og dataenheter

[!include [banner](../includes/banner.md)]

Før du bruker dataenheter til å importere eller eksportere data, anbefaler vi at du først bestemmer virkningen av konfigurasjonsnøklene i dataenheter som du har tenkt å bruke. 

Du kan lære mer om konfigurasjonsnøkler i Finance and Operations i [Rapport for lisenskoder og konfigurasjonsnøkler](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Konfigurasjonsnøkkeltilordninger
Konfigurasjonsnøkler kan tilordnes til én eller alle følgende artefakter.
-   Dataenheter
-   Tabeller som brukes som datakilder
-   Tabellfelt
-   Dataenhetsfelt

Tabellen nedenfor viser hvordan konfigurasjonsnøkkelverdier i de forskjellige artefaktene som ligger under et objekt, endrer den forventede virkemåten for objektet.

| Konfigurasjonsnøkkelinnstilling i dataenhet | Konfigurasjonsnøkkelinnstilling i tabell | Konfigurasjonsnøkkelinnstilling i tabellfelt | Konfigurasjonsnøkkelinnstilling i dataenhetsfelt | Forventet virkemåte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------|-----------------------------|-----------------------------------|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Deaktivert                          | Ikke evaluert               | Ikke evaluert                     | Ikke evaluert                   | Hvis konfigurasjonsnøkkelen for dataenheten er deaktivert, vil ikke dataenheten fungere. Det spiller ingen rolle om konfigurasjonsnøklene i de underliggende tabellene og feltene er aktivert eller deaktivert.                                                                                                                                                                                                                                                                                                                                          |
| Aktivert                           | Deaktivert                    | Ikke evaluert                     | Ikke evaluert                   | Hvis konfigurasjonsnøkkelen for en dataenhet er aktivert, kontrollerer rammeverket for databehandling konfigurasjonsnøkkelen i hver av de underliggende tabellene. Hvis konfigurasjonsnøkkelen for en tabell er deaktivert, blir ikke denne tabellen tilgjengelig i dataenheten for funksjonell bruk. Hvis konfigurasjonsnøkkelen for en tabell er deaktivert, evalueres ikke konfigurasjonsnøkkelinnstillingene for tabellen og dataenheten. Hvis den primære tabellen i enheten har konfigurasjonsnøkkelen deaktivert, vil systemet fungere som om enhetens konfigurasjonsnøkkel ble deaktivert. |
| Aktivert                           | Aktivert                     | Deaktivert                          | Ikke evaluert                   | Hvis konfigurasjonsnøkkelen for en dataenhet er aktivert, og de underliggende konfigurasjonsnøklene for tabellene er aktivert, vil rammeverket for databehandling kontrollere konfigurasjonsnøkkelen for feltene i tabellene. Hvis konfigurasjonsnøkkelen for et felt er deaktivert, blir ikke dette feltet tilgjengelig i dataenheten for funksjonell bruk selv om det tilsvarende dataenhetsfeltet har konfigurasjonsnøkkelen aktivert.                                                                                                                                   |
| Aktivert                           | Aktivert                     | Aktivert                           | Deaktivert                        | Hvis konfigurasjonsnøkkelen er aktivert på alle andre nivåer, men konfigurasjonsnøkkelen for enhetsfeltet ikke er aktivert, blir ikke feltet tilgjengelig for bruk i dataenheten.                                                                                                                                                                                                                                                                                                                                                                          |

> [!NOTE]
> Hvis en enhet har en annen enhet som datakilde, brukes semantikken ovenfor på en rekursiv måte.

### <a name="entity-list-refresh"></a>Oppdatering av enhetsliste
Når enhetslisten oppdateres, bygger rammeverket for databehandling metadata for konfigurasjonsnøkkelen for kjøretidsbruk. Disse metadataene bygges ved hjelp av logikken som er beskrevet ovenfor. Vi anbefaler sterkt at du venter til enhetslisten er ferdig oppdatert før du bruker jobber og enheter i rammeverket for databehandling. Hvis du ikke venter, kan det være at metadataene for konfigurasjonsnøkkelen ikke er oppdatert, noe som kan føre til uventede resultater. Når enhetslisten oppdateres, vises følgende melding på enhetslistesiden.

![Oppdatering av enhetsliste](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Listesiden for dataenhet
Listesiden for dataenhet i arbeidsområdet for databehandling viser konfigurasjonsnøkkelinnstillingene for enhetene. Start fra denne siden for å forstå effekten konfigurasjonsnøklene har på dataenheten.
Denne informasjonen vises ved hjelp av metadataene som bygges under enhetsoppdateringen. Konfigurasjonsnøkkelkolonnen viser navnet på konfigurasjonsnøkkelen som er knyttet til dataenheten. Hvis denne kolonnen er tom, betyr det at det ikke er noen konfigurasjonsnøkkel knyttet til dataenheten. Kolonnen med status for konfigurasjonsnøkkel viser tilstanden for konfigurasjonsnøkkelen. Hvis den er merket av her, betyr det at nøkkelen er aktivert. Hvis den er tom, betyr det enten at nøkkelen er deaktivert eller at det ikke er noen nøkkel som er tilknyttet.

![Enhetslistesiden](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Målfelt
Det neste trinnet er å drille ned i dataenheten for å vise virkningen av konfigurasjonsnøkler på tabeller og felt. Målfeltskjemaet for en dataenhet viser konfigurasjonsnøkkel og nøkkelstatusinformasjonen for relaterte tabeller og felt i dataenheten.  Hvis selve dataenheten har konfigurasjonsnøkkelen deaktivert, vises en advarsel om at tabellene og feltene i målfeltskjemaet for denne enheten ikke blir tilgjengelig i det hele tatt, uavhengig av status for konfigurasjonsnøkkelen.

![Målfelt](./media/Target_fields_1.png)

### <a name="child-entities"></a>Underordnede enheter 
Enkelte enheter har andre enheter som datakilder eller er sammensatte dataenheter: konfigurasjonsnøkkelinformasjon for disse enhetene vises i skjemaet for underordnede enheter. Bruk dette skjemaet på lignende måte på enhetslistesiden som er beskrevet ovenfor. Målfeltskjemaet for den underordnede enheten fungerer også som det er beskrevet ovenfor.

![Målfelt](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Bruke dataenheter
Når du har forstått hele virkningen, om noen, av konfigurasjonsnøkler på dataenhetene som du vil bruke, kan du nå fortsette og bruke dataenhetene ved å legge dem til dataprosjekter. 

### <a name="run-time-validations-for-configuration-keys"></a>Kjøretidsvalideringer for konfigurasjonsnøkler
Ved hjelp av konfigurasjonsnøkkelmetadataene som er bygd under enhetslisteoppdateringen, utføres kjøretidsvalideringer i følgende brukstilfeller.

-   Når en dataenhet legges til en jobb

-   Når brukeren klikker valider på enhetslisten

-   Når brukeren laster inn en datapakke til et dataprosjekt

-   Når brukeren laster inn en mal til et dataprosjekt

-   Når et eksisterende dataprosjekt lastes inn

-   Når en mal lastes inn til et dataprosjekt

-   Før eksport-/importjobben utføres (parti, ikke-parti, regelmessig, Odata)

-   Når brukeren genererer tilordning

-   Når brukeren tilordner felt i tilordningsgrensesnittet

-   Når brukeren legger til bare importerbare felt


### <a name="managing-configuration-key-changes"></a>Administrasjon av konfigurasjonsnøkkelendringer
Når du oppdaterer konfigurasjonsnøkler på enhets-, tabell- og feltnivået, må enhetslisten i rammeverket for databehandling oppdateres. Denne prosessen sikrer at rammeverket henter de nyeste konfigurasjonsnøkkelinnstillingene. Inntil enhetslisten oppdateres, vises følgende advarsel på enhetslistesiden. De oppdaterte konfigurasjonsnøkkelendringene trer i kraft umiddelbart etter at enhetslisten oppdateres. Vi anbefaler at du validerer eksisterende dataprosjekter og jobber for å forsikre deg om at de fungerer som forventet når konfigurasjonsnøkkelendringene trer i kraft.

![Målfelt](./media/Target_fields_3.png)


