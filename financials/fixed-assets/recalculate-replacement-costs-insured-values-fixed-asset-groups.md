---
title: Omberegne erstatningskostnader og forsikrede verdier for anleggsmiddelgrupper
description: "Denne artikkelen beskriver prosessen for å oppdatere erstatningskostnader og forsikrede verdier for anleggsmidler."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 38f779274da370d436509e021cabf5b90ab08475
ms.lasthandoff: 03/31/2017


---

# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Omberegne erstatningskostnader og forsikrede verdier for anleggsmiddelgrupper

Denne artikkelen beskriver prosessen for å oppdatere erstatningskostnader og forsikrede verdier for anleggsmidler.

Du kan få beskjed regelmessig om at kostnadene ved erstatning eller forsikring av bestemte anleggsmidler er endret. Lederen kan for eksempel informere deg om at inflasjonene var 3 prosent i fjor, slik at du må øke erstatningskostnaden for alle anleggsmidler med 3 prosent. 

Selv om du kan redigere erstatningskostnaden og den forsikrede verdien for enkle anleggsmidler i Anleggsmidler-skjemaet, kan du bruke skjemaet Oppdater erstatningskostnader og forsikrede verdier til å oppdatere disse verdiene for en gruppe anleggsmidler samtidig. Denne informasjonen beskriver hvordan du oppdaterer verdier for anleggsmiddelgrupper, eller for bestemte anleggsmidler i gruppene.

## <a name="how-values-are-updated"></a> Hvordan verdier oppdateres
Hvis du vil beregne erstatningskostnader og forsikrede verdier på nytt for anleggsmiddelgrupper, må du først angi prosenten som de eksisterende erstatningskostnadene og de forsikrede verdiene skal endres med, og deretter utføre den periodiske oppdateringen for faktisk å beregne verdiene på nytt. Du angir prosenten i feltene Faktor for erstatningskostnad og Faktor for forsikret verdi i Anleggsmiddelgrupper-skjemaet. Selv om du angir disse faktorene for anleggsmiddelgruppen når du bruker skjemaet Oppdater erstatningskostnader og forsikrede verdier, kan du velge å beregne erstatningskostnaden og den forsikrede verdien på nytt for bare bestemte anleggsmidler i en gruppe. 

Når du bruker skjemaet Oppdater erstatningskostnader og forsikrede verdier for å omberegne erstatningskostnaden og den forsikrede verdien for anleggsmidlene, brukes følgende formler:

-   \[(Asset gruppe erstatning kostnad faktor / 100) + 1\]\* Anleggsmidlets eksisterende erstatningskostnad
-   \[(Gruppe anleggsmidler faktor for forsikret verdi / 100) + 1\]\* Anleggsmidlets eksisterende forsikrede verdien

> [!NOTE] 
> Når du bruker skjemaet Oppdater erstatningskostnader og forsikrede verdier, oppdateres både erstatningskostnaden og den forsikrede verdien for de valgte anleggsmidlene. Du kan ikke angi at bare én verdi skal oppdateres. Hvis du vil la den ene verdien være den samme og oppdatere den andre verdien, kan du angi 0 (null) som faktor i Anleggsmiddelgrupper-skjemaet. En nullverdi eller tom faktorverdi fører til at beregningen utelates i oppdateringen. Den bokførte verdien og netto bokført verdi for anleggsmidler berøres ikke av den periodiske oppdateringen. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Hvordan du bruker en dato til å velge hvilke varer som skal oppdateres
Som standard oppdaterer den periodiske prosessen de valgte anleggsmidlene som ikke ble oppdatert på den gjeldende dagen, men som kan ha blitt oppdatert på tidligere dager. For eksempel &lt;gjeldende dato betyr "før i dag." Du kan endre datoen i oppdateringen erstatning og forsikrede verdier-skjemaet ved å klikke Velg-knappen. Datokriteriene du angir, sammenlignes med datoen for den siste periodiske oppdateringen for anleggsmidlet (feltet Siste periodiske verdi-/kostnadsoppdatering i skjemaet Anleggsmidler). Hver gang du oppdaterer erstatningskostnaden eller den forsikrede verdien for et anleggsmiddel, oppdateres feltet Siste periodiske verdi-/kostnadsoppdatering automatisk med gjeldende dato. 

Eksempel 

Du oppdaterte erstatningskostnaden for kjøretøy, kontormøbler og bygningsgrupper med 5 prosent i går, og nå anser du disse anleggsmidlene som nøyaktig oppdatert. Hvis du vil utelate disse anleggsmidlene når du oppdaterer alle andre anleggsmidler i dag, angir du en dato i sist periodiske verdi/update kostnadsfelt som er før i går (&lt; gårsdagens dato) fordi den siste oppdateringen for kjøretøy, kontormøbler og bygninger grupper oppstod utenfor Datokriteriene du angav.

## <a name="cumulative-effect-of-each-update"></a> Akkumulert effekt for hver oppdatering
Hver oppdatering har en akkumulert effekt. Du må derfor planlegge oppdateringen nøye. Hvis du for eksempel øker alle anleggsmidler med 3 prosent på tirsdag, og deretter øker kontormøbler med 4 prosent på fredag, vil kontormøbler øke med totalt 7,12 prosent.

## <a name="scenario"></a>Scenario
Sjefen din gir deg beskjed om følgende endringer i anleggsmidler:
-   Øk erstatningskostnaden for alle anleggsmidler, bortsett fra datamaskiner, med 3,25 prosent.
-   Øk erstatningskostnaden for alle kontormøbler med 1 prosent ekstra.
-   Reduser erstatningskostnaden og den forsikrede verdien for alle datamaskiner med 10 prosent.

Du gjør følgende endringer:
1.  I Anleggsmidldelgrupper-skjemaet, for alle anleggsmiddelgrupper, bortsett fra kontormøblergruppen og gruppen for datamaskiner, skriver du inn 3,25 i feltet Faktor for erstatningskostnad og 0 i feltet Faktor for forsikret verdi.
2.  For kontormøblergruppen, skriver du inn 4,25 i feltet Faktor for erstatningskostnad og 0 i feltet Faktor for forsikret verdi.
3.  For gruppen for datamaskiner skriver du inn -10 i feltet Faktor for erstatningskostnad og -10 i feltet Faktor for forsikret verdi.
4.  I skjemaet Oppdater erstatningskostnader og forsikrede verdier klikker du OK for å utføre omberegningen for alle anleggsmidler.

Neste dag gir sjefen deg beskjed om at datamaskiner ble redusert med 8 prosent, i stedet for 10 prosent, slik at du må rette opp erstatningskostnadene og de forsikrede verdiene. Hvis du vil rette opp feilen, kan du bruke disse to metodene:
-   Endre feltene Forsikret verdi og Erstatningskostnad i Anleggsmidler-skjemaet for hvert anleggsmiddel i anleggsmiddelgruppen for datamaskiner manuelt. Beregn og angi manuelt verdiene som om du reduserte det opprinnelige beløpet med 8 prosent. Med denne metoden bruker du ikke skjemaet Oppdater erstatningskostnader og forsikrede verdier.
-   Angi faktorer for erstatningskostnad og forsikret verdi for datamaskingruppen i feltene Erstatningskostnad og Forsikret verdi i Anleggsmiddelgrupper-skjemaet. Dette vil både tilbakestille anleggsmidlene tilbake til den opprinnelige verdien (før reduksjonen på 10 prosent) og bruke reduksjonen på 8 prosent på den opprinnelige verdien. Bruk deretter skjemaet Oppdater erstatningskostnader og forsikrede verdier til å omberegne verdiene, avhengig av faktorene du angav.

> [!NOTE]  
> Du kan ikke tilbakeføre faktoren –10 ved å angi en faktor med positiv 10 (eller en faktor på 2, forskjellen mellom –10 og –8), fordi beløpene ikke vil beregnes slik du har til hensikt å gjøre. 




