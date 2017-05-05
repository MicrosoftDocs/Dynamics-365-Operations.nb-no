---
title: Lagerblokkering
description: "Denne artikkelen inneholder en oversikt over lagerblokkering, som er en del av kvalitetsinspeksjonsprosessen i Microsoft Dynamics AX. Du kan bruke lagerblokkering til å forhindre at varer behandles eller forbrukes."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 0d7e37de63e6c63b5d7942a84de60ef8f3984cde
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-blocking"></a>Lagerblokkering

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder en oversikt over lagerblokkering, som er en del av kvalitetsinspeksjonsprosessen i Microsoft Dynamics AX. Du kan bruke lagerblokkering til å forhindre at varer behandles eller forbrukes.

Du kan blokkere lagervarer på følgende måter:
-   Manuelt
-   Ved å opprette en kvalitetsordre
-   Ved å bruke en prosess som genererer en kvalitetsordre
-   Ved å bruke blokkering av beholdningsstatus

## <a name="blocking-items-manually"></a>Blokkere varer manuelt
Du kan blokkere et antall av en vare ved å opprette en transaksjon på **Lagerblokkering**-siden. Bare varer som er tilgjengelige i lagerbeholdningen kan blokkeres manuelt. Når det gjelder manuelt blokkerte antall, må du bestemme om planleggingsaktiviteter skal inkludere forventede mottak som et forventet antall på lager. Forventede mottak er blokkerte varer som du forventer skal være tilgjengelige som lagerbeholdning etter inspeksjon er foretatt. Du kan vedlikeholde den forventede datoen. Som standard er alternativet **Forventede mottak** valgt for varer som er blokkert via en kvalitetsordre. Du kan oppheve en manuell blokkering av et antall ved å slette transaksjonen på **Lagerblokkering**-siden.

## <a name="blocking-items-by-creating-a-quality-order"></a>Blokkere varer ved å opprette en kvalitetsordre
Du kan angi varer som må kontrolleres, ved å opprette en kvalitetsordre på **Kvalitetsordrer**-siden. Når du oppretter en kvalitetsordre, blokkeres antallet som du angir for en vare. Prøveplanen som er knyttet til en kvalitetsordre, styrer bare antallet varer som må kontrolleres, ikke antallet som er blokkert. Antallet som er angitt på kvalitetsordren, er antallet som er blokkert, uavhengig av hvilket antall som skal sendes til inspeksjon i henhold til prøveplanen.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Blokkere varer ved hjelp av en prosess som genererer en kvalitetsordre
Hvis en kvalitetsprosess angir at en vare skal kontrolleres, blokkeres et antall av varen automatisk. Så når en kvalitetsordre genereres automatisk, kontrollerer vareprøveplanen som er knyttet til kvalitetsordren, både hvor mange varer som er sperret og hvor mange varer som skal kontrolleres. Hvis det er merket av for **Full blokkering** på **Vareprøve**-siden, blokkeres for eksempel hele antallet på en bestillingslinje under inspeksjon, uavhengig av vareprøveantallet.
### <a name="example"></a>Eksempel

I eksemplet nedenfor genereres en kvalitetsordre når en følgeseddel for bestilling blir postert. På **Kvalitetstilknytninger**-siden angav du at postering av en bestillingsfølgeseddel er prosessen som aktiverer en kvalitetsordre.

|Konfigurasjon                                                                     |Brukerhandling                 |Resultat             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| En kvalitetstilknytning angir at det må genereres en kvalitetsordre når en bestillingsfølgeseddel posteres. Vareprøveoppsettet for kvalitetsordren angir at 10 % av antallet på bestillingslinjen må kontrolleres. Og ettersom det er merket av for **Full blokkering** i vareprøveoppsettet, må hele antallet for bestillingslinjen blokkeres under inspeksjon, uavhengig av antallet som sendes til inspeksjon. | Følgeseddelen posteres. | En kvalitetsordre genereres. Ti prosent av bestillingsantallet for varen sendes til inspeksjon. Hele antallet på bestillingslinjen er blokkert. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Blokkere varer ved å bruke blokkering av beholdningsstatus
Du kan angi hvilke beholdningsstatuser som er blokkeringsstatuser ved hjelp av parameteren **Lagerblokkering** på **Beholdningsstatuser**-siden.  Du kan ikke bruke lagerstatuser som blokkeringsstatuser for produksjonsordrer, salgsordrer, overføringsordrer, utgående transaksjoner og prosjektintegrering. Når det gjelder utgående arbeid, bruker du varer som har en tilgjengelig lagerstatus. Hvis varer har statusen **Brutt** og hovedplanlegging kjøres på disse varene, blir varene ansett som manglende, og beholdningen etterfylles automatisk.



<a name="see-also"></a>Se også
--------

[Opprette og vedlikeholde en lagerblokkering (oppgaveveiledning)](https://ax.help.dynamics.com/en/wiki/create-and-maintain-an-inventory-blocking/)

[Kvalitetsstyringsprosesser](quality-management-processes.md)

[Kontrollere varekvaliteten (oppgaveveiledning)](https://ax.help.dynamics.com/en/wiki/inspect-the-quality-of-goods/)



