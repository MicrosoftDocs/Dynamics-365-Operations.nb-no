---
title: Fordelingsbetingelser
description: Dette emnet gir informasjon om hvordan du bruker tildelingsbetingelser på en hovedkonto.
author: rachel-profitt
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 637e12f0deaa53811093a8745bc74dbc19e34f6b
ms.sourcegitcommit: 4676ea9646fa1a182103ecab93e78a69001f0b8d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/21/2020
ms.locfileid: "3613157"
---
# <a name="allocation-terms"></a>Fordelingsbetingelser

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om hvordan du bruker tildelingsbetingelser på en hovedkonto. Tildelingsvilkår brukes til å distribuere beløp på tvers av flere kombinasjoner av finanskonti. De bidrar til å sikre at utgifter eller inntekter belastes til riktig objekt i regnskapet.

Hver tildelingsbetingelse du oppretter på en hovedkonto, definerer prosenten av et bilag som skal fordeles fra en hovedkonto med én kilde og en kombinasjon av finansdimensjoner. I tillegg definerer du den målhovedkontoen og finansdimensjonene der beløpet skal fordeles. 

Når du definerer finansdimensjonen for en kilde for tildelingen, kan du velge om hver dimensjon er spesifikk eller ikke-spesifikk. Spesifikk angir at finansdimensjonen for kildetransaksjonen må samsvare med den valgte dimensjonen. Når du velger ikke-spesifikk, angir det at alle verdier for finansdimensjonen kan bidra til en match.

Når du definerer målfinanskontoen for en fordelingsbetingelse, må du angi hovedkontoen du tildeler beløpet til. Du kan bruke samme hovedkonto som kildetransaksjonen posteres til, eller en annen hovedkonto. Hvis den samme hovedkontoen brukes, vises det en advarsel når du lagrer posten. I tillegg til å angi hovedkontoen må du også angi måldimensjonene. For hver dimensjon kan du angi om du vil beholde kildefinansdimensjonsverdien eller endre den. Hvis du velger Nei, må du velge en ny verdi for finansdimensjonen. Hvis du velger Ja, blir det ikke angitt mer informasjon, og systemet opprettholder de opprinnelige finansdimensjonene når du posterer.

Det er ingen grense for antall tildelingsbetingelser du kan legge til i en hovedkonto. Summen av prosenten som skal tildeles en fordelingsbetingelse, kan imidlertid ikke overskride 100. Du kan opprette tildelinger for mindre enn 100 prosent hvis en del av det opprinnelige bilagsbeløpet skal forbli i kildefinansdimensjonene. Tildelingsbetingelser kan legges til en hovedkonto som overstyring av en juridisk enhet. Hvis du bruker en delt kontoplan, må tildelingsbetingelsene defineres for hver juridiske enhet. Hvis du vil ha tilgang til **Tildelingsbetingelser**-knappen, må du først merke av for **Tildeling** i overstyringen av den juridiske enheten.

## <a name="allocation-term-example"></a>Eksempel på tildelingsbetingelse
Du har definert et kostsenter for organisasjonen som kalles FIRMA, som er nummerert 000. Når fakturaer posteres for administrative utgifter, er de kodet til dette FIRMA-kostsenteret. Firmaet har definert en regel om at alle administrative utgifter skal fordeles med en prosentandel til hvert enkelt kostsenter. De andre finansdimensjonene for avdeling og forretningsenhet vil forbli de samme.

I dette eksemplet opprettes det en ny fordelingsbetingelse for hovedkontoen for adminmistrative utgifter. Det vil bli opprettet en rad for hvert kostsenter med prosenten som skal fordeles. **Utvalgskriteriene** for kildefinansdimensjonene for hver rad vil være **Spesifikk** for **Kostsenter**, og verdien settes til 000: FIRMA. For avdeling og forretningsenhet vil **utvalgskriteriene** være **Ikke-spesifikk**.

På hurtigfanen **Målfinanskonto** vil hovedkontoen være den samme kontoen for administrative utgifter, og **Behold kildefinansdimensjoner** settes til **Ja** for **Forretningsenhet** og **Avdeling**. **Behold kildefinansdimensjoner** settes til **Nei** for **Kostsenter**, og den valgte verdien vil være hvert respektive kostsenter du tildeler til. Hvis det er tre kostsentre å tildele til, opprettes det tre poster med tildelingsbetingelser. Den eneste forskjellen mellom hver tildelingsbetingelse er kostsenteret som er angitt i målfinanskontoen.

## <a name="create-an-allocation-term-on-a-main-account"></a>Opprette en tildelingsbetingelse for en hovedkonto

1. I **navigasjonsruten** går du til **Moduler > Økonomimodul > Kontoplan > Kontoer > Hovedkontoer**.
2. Finn og velg ønsket post i listen.
3. På hurtigfanen **Overstyringer for juridisk enhet** velger du **Legg til**.
4. Velg **Firma**, og velg deretter **Legg til**.
5. Merk av for **Tildeling**.
6. Velg **Tildelingsbetingelser**.
7. Velg **Rediger** for å endre standardposten, eller velg **Ny** for å legge til en post.
8. I **Prosent**-feltet angir du prosenten for bilagstransaksjoner som du vil tildele.
9. På hurtigfanen **Kildefinansdimensjon** i **utvalgskriteriene** for hver finansdimensjon velger du et alternativ.
    - Hvis du velger **Spesifikk**, velger du finansdimensjonsverdien i rullegardinlisten til høyre.
    - Hvis du velger **Ikke-spesifikk**, kreves det ingen tilleggsinformasjon for finansdimensjonen.
10. På hurtigfanen **Målfinanskonto** i feltet **Til konto** velger du hovedkontoen der du ønsker å tildele prosenten for bilagstransaksjonen.
11. Velg et alternativ under **Behold kildefinansdimensjoner** for hver finansdimensjon.
    - Hvis du velger **Nei**, velger du finansdimensjonsverdien i rullegardinlisten til høyre der du vil at bilagstransaksjonen skal tildeles.
    - Hvis du velger **Ja**, er ingen tilleggsinformasjon nødvendig. Systemet vil beholde verdien på det opprinnelige bilaget ved postering av tildelingen.
12. Gjenta trinn 7 til 11 for hver ytterligere tildeling. Summen av alle tildelingene vises i **Total prosent**-feltet. Denne summen kan ikke overskride 100.
13. Lukk alle sidene.

>[!NOTE] 
> Du kan eventuelt bruke **Kopier**-knappen til å duplisere den valgte tildelingen.

Når en tildelingsbetingelse opprettes for en hovedkonto, vil systemet automatisk postere et nytt bilag når et bilag posteres som samsvarer med de kildefinansdimensjonene for tildelingsbetingelsene.
