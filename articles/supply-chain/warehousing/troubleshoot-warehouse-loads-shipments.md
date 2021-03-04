---
title: Feilsøke lastplanlegging og forsendelser
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lastplanlegging og forsendelser i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2933bcfd2cc526e39a4e1343cd472334a5b95607
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645338"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Feilsøke lastplanlegging og forsendelser

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lastplanlegging og forsendelser i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Jeg får følgende feilmelding: Du kan ikke opprette en lastlinje for denne ordrelinjen fordi den inneholder lagerdimensjoner som er ugyldige ...

### <a name="issue-description"></a>Problembeskrivelse

Du får følgende feilmelding når du prøver å frigi en retursalgsordre til lageret:

> Du kan ikke opprette en lastlinje for denne ordrelinjen fordi den inneholder lagerdimensjoner som er ugyldige. Du kan ikke referere til lagerdimensjoner som finnes under lokasjonsdimensjonen i reservasjonshierarkiet. Fjern de ugyldige dimensjonene fra ordrelinjen.

### <a name="issue-resolution"></a>Problemløsning

Dessverre støtter ikke produktet lastbehandling for en salgsreturprosess. Derfor kan du ikke frigi retursalgsordren til lageret.

På salgsordretransaksjoner kan du ikke referere til lagerdimensjoner som finnes under **Lokasjon**-dimensjonen i reservasjonshierarkiet. Løsningen er å fjerne de ugyldige dimensjonene fra ordrelinjen.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Jeg får følgende feilmelding: En av linjene er allerede på en last. Kan ikke frigi til lager.

### <a name="issue-description"></a>Problembeskrivelse

Hvis du oppretter laster manuelt, eller hvis du definerer prosessen slik at laster allerede er opprettet før salgsordrelinjeposten inntreffer, antas det at den påfølgende frigivelsen utføres manuelt, og at ruten og vurderingen fra lasten skal brukes.

I et annet scenario vil du prøve å utføre en automatisk frigivelse av lageret, men bølgeprosessen kan ikke opprette arbeid. Derfor blir det fremdeles opprettet en åpen forsendelse eller last. Denne åpne forsendelsen eller lasten blokkerer deretter etterfølgende forsøk på å frigi ordren automatisk til du sletter den åpne forsendelsen eller lasten, eller manuelt behandler bølgen på nytt.

### <a name="issue-resolution"></a>Problemløsning

Du kan frigi fra salgsordresiden eller automatisk frigivelse fra siden frigivelse av salgsordre, bare hvis det ikke finnes en last før frigivelsen til lageret. Lasten vil automatisk bli opprettet etter at bølgen er behandlet.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Jeg får følgende feilmelding: Korrigeringen av følgeseddelen kan ikke behandles. Følgeseddelen inneholder bare varer som er underlagt lagerstyringsprosesser, siden disse ikke støttes av følgeseddelkorrigering.

### <a name="issue-description"></a>Problembeskrivelse

Når du har postert en følgeseddel, kan du ikke avbryte den fordi **Avbryt**-knappen ikke er tilgjengelig. Du kan heller ikke korrigere følgeseddelen. Hvis du prøver, får du denne feilmeldingen.

### <a name="issue-resolution"></a>Problemløsning

Hvis du vil korrigere posterte følgesedler for varer som er aktivert for avansert lagerstyring (WMS), må du utføre posteringen fra lasten, ikke direkte fra ordren.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Hvordan kan jeg opprette arbeid fra utgående laster i stedet for bølger?

### <a name="issue-description"></a>Problembeskrivelse

Her er en måte å gjenskape dette problemet på.

1. Opprette en utgående last ved hjelp av en salgsordre eller overføringsordre.
2. Frigi belastningen til lageret.
3. Legg merke til at det ennå ikke er generert noe plukkarbeid.

### <a name="issue-resolution"></a>Problemløsning

Hvis arbeid må genereres umiddelbart når lasten frigis, må du konfigurere bølgemalen i henhold til dette. I bølgemalen angir du følgende alternativer til *Ja*:

- Automatisk oppretting av bølge
- Behandle bølge ved frigivelse til lager
- Frigi bølge automatisk

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Jeg kan ikke frigi en delvis levert last på nytt.

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke frigi en delvis levert last til lageret. Når du gjør frigivelsen til lageret, vises meldingen Operasjon fullført, men ingenting skjer ikke, og det opprettes ikke noe arbeid for restantallet. Dette problemet oppstår når du bruker funksjonalitet for transportlast, og det er en ufullstendig reservasjon.

### <a name="issue-resolution"></a>Problemløsning

[KB-problem 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) (Delvis leverte laster kan bølges og behandles på nytt) er løst i [frigivelses 10.0.15](../get-started/whats-new-scm-10-0-15.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]