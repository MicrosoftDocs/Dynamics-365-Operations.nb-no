---
title: Lagerblokkering
description: "Denne artikkelen inneholder en oversikt over lagerblokkering, som er en del av kvalitetsinspeksjonsprosessen i Enterprise-utgaven av Microsoft Dynamics 365 for Finance and Operations. Du kan bruke lagerblokkering til å forhindre at varer behandles eller forbrukes."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 4c5ebea58630188615fb4c22cc9da5215461e513
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Lagerblokkering
<a id="inventory-blocking" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder en oversikt over lagerblokkering, som er en del av kvalitetsinspeksjonsprosessen i Enterprise-utgaven av Microsoft Dynamics 365 for Finance and Operations. Du kan bruke lagerblokkering til å forhindre at varer behandles eller forbrukes.

Du kan blokkere lagervarer på følgende måter:
-   Manuelt
-   Ved å opprette en kvalitetsordre
-   Ved å bruke en prosess som genererer en kvalitetsordre
-   Ved å bruke blokkering av beholdningsstatus

## Blokkere varer manuelt
<a id="blocking-items-manually" class="xliff"></a>
Du kan blokkere et antall av en vare ved å opprette en transaksjon på **Lagerblokkering**-siden. Bare varer som er tilgjengelige i lagerbeholdningen kan blokkeres manuelt. Når det gjelder manuelt blokkerte antall, må du bestemme om planleggingsaktiviteter skal inkludere forventede mottak som et forventet antall på lager. Forventede mottak er blokkerte varer som du forventer skal være tilgjengelige som lagerbeholdning etter inspeksjon er foretatt. Du kan vedlikeholde den forventede datoen. Som standard er alternativet **Forventede mottak** valgt for varer som er blokkert via en kvalitetsordre. Du kan oppheve en manuell blokkering av et antall ved å slette transaksjonen på **Lagerblokkering**-siden.

## Blokkere varer ved å opprette en kvalitetsordre
<a id="blocking-items-by-creating-a-quality-order" class="xliff"></a>
Du kan angi varer som må kontrolleres, ved å opprette en kvalitetsordre på **Kvalitetsordrer**-siden. Når du oppretter en kvalitetsordre, blokkeres antallet som du angir for en vare. Prøveplanen som er knyttet til en kvalitetsordre, styrer bare antallet varer som må kontrolleres, ikke antallet som er blokkert. Antallet som er angitt på kvalitetsordren, er antallet som er blokkert, uavhengig av hvilket antall som skal sendes til inspeksjon i henhold til prøveplanen.

## Blokkere varer ved hjelp av en prosess som genererer en kvalitetsordre
<a id="blocking-items-by-using-a-process-that-generates-a-quality-order" class="xliff"></a>
Hvis en kvalitetsprosess angir at en vare skal kontrolleres, blokkeres et antall av varen automatisk. Så når en kvalitetsordre genereres automatisk, kontrollerer vareprøveplanen som er knyttet til kvalitetsordren, både hvor mange varer som er sperret og hvor mange varer som skal kontrolleres. Hvis det er merket av for **Full blokkering** på **Vareprøve**-siden, blokkeres for eksempel hele antallet på en bestillingslinje under inspeksjon, uavhengig av vareprøveantallet.
### Eksempel
<a id="example" class="xliff"></a>

I eksemplet nedenfor genereres en kvalitetsordre når en følgeseddel for bestilling blir postert. På **Kvalitetstilknytninger**-siden angav du at postering av en bestillingsfølgeseddel er prosessen som aktiverer en kvalitetsordre.

|Konfigurasjon                                                                     |Brukerhandling                 |Resultat             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| En kvalitetstilknytning angir at det må genereres en kvalitetsordre når en bestillingsfølgeseddel posteres. Vareprøveoppsettet for kvalitetsordren angir at 10 % av antallet på bestillingslinjen må kontrolleres. Og ettersom det er merket av for **Full blokkering** i vareprøveoppsettet, må hele antallet for bestillingslinjen blokkeres under inspeksjon, uavhengig av antallet som sendes til inspeksjon. | Følgeseddelen posteres. | En kvalitetsordre genereres. Ti prosent av bestillingsantallet for varen sendes til inspeksjon. Hele antallet på bestillingslinjen er blokkert. |

## Blokkere varer ved å bruke blokkering av beholdningsstatus
<a id="blocking-items-by-using-inventory-status-blocking" class="xliff"></a>
Du kan angi hvilke beholdningsstatuser som er blokkeringsstatuser ved hjelp av parameteren **Lagerblokkering** på **Beholdningsstatuser**-siden.  Du kan ikke bruke lagerstatuser som blokkeringsstatuser for produksjonsordrer, salgsordrer, overføringsordrer, utgående transaksjoner og prosjektintegrering. Når det gjelder utgående arbeid, bruker du varer som har en tilgjengelig lagerstatus. Hvis varer har statusen **Brutt** og hovedplanlegging kjøres på disse varene, blir varene ansett som manglende, og beholdningen etterfylles automatisk.



Se også
<a id="see-also" class="xliff"></a>
--------

[Opprette og vedlikeholde en lagerblokkering (oppgaveveiledning)](https://ax.help.dynamics.com/en/wiki/create-and-maintain-an-inventory-blocking/)

[Kvalitetsstyringsprosesser](quality-management-processes.md)

[Kontrollere varekvaliteten (oppgaveveiledning)](https://ax.help.dynamics.com/en/wiki/inspect-the-quality-of-goods/)




