---
title: Lagerblokkering
description: Dette emnet inneholder en oversikt over lagerblokkering, som er en del av kvalitetsinspeksjonsprosessen i Supply Chain Management. Du kan bruke lagerblokkering til å forhindre at varer behandles eller forbrukes.
author: yufeihuang
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b6169362c9e8cb3a9ace2f300dd9d80aa9cd085
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568885"
---
# <a name="inventory-blocking"></a>Lagerblokkering

[!include [banner](../includes/banner.md)]

Dette emnet inneholder en oversikt over lagerblokkering, som er en del av kvalitetsinspeksjonsprosessen i Supply Chain Management. Du kan bruke lagerblokkering til å forhindre at varer behandles eller forbrukes.

Du kan blokkere lagervarer på følgende måter:

- Manuelt
- Ved å opprette en kvalitetsordre
- Ved å bruke en prosess som genererer en kvalitetsordre
- Ved å bruke blokkering av beholdningsstatus

## <a name="blocking-items-manually"></a>Blokkere varer manuelt

Du kan blokkere et antall av en vare ved å opprette en transaksjon på **Lagerblokkering**-siden. Bare varer som er tilgjengelige i lagerbeholdningen kan blokkeres manuelt. Når det gjelder manuelt blokkerte antall, må du bestemme om planleggingsaktiviteter skal inkludere forventede mottak som et forventet antall på lager. Forventede mottak er blokkerte varer som du forventer skal være tilgjengelige som lagerbeholdning etter inspeksjon er foretatt. Du kan vedlikeholde den forventede datoen. Som standard er alternativet **Forventede mottak** valgt for varer som er blokkert via en kvalitetsordre. Du kan oppheve en manuell blokkering av et antall ved å slette transaksjonen på **Lagerblokkering**-siden.

## <a name="blocking-items-by-creating-a-quality-order"></a>Blokkere varer ved å opprette en kvalitetsordre

Du kan angi varer som må kontrolleres, ved å opprette en kvalitetsordre på **Kvalitetsordrer**-siden. Når du oppretter en kvalitetsordre, blokkeres antallet som du angir for en vare. Prøveplanen som er knyttet til en kvalitetsordre, styrer bare antallet varer som må kontrolleres, ikke antallet som er blokkert. Antallet som er angitt på kvalitetsordren, er antallet som er blokkert, uavhengig av hvilket antall som skal sendes til inspeksjon i henhold til prøveplanen.

> [!NOTE]
> Bruk av både utløpsdato for parti og blokkering av beholdningsstatus støttes ikke ved hovedplanlegging. Dette kan føre til dobbel utelatelse av lagerbeholdningen, som kan forekomme under hovedplanlegging. Det anbefales at du bruker partidisposisjonskoder i stedet for lagerstatus for å blokkere utløpte partier.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Blokkere varer ved hjelp av en prosess som genererer en kvalitetsordre

Hvis en kvalitetsprosess angir at en vare skal kontrolleres, blokkeres et antall av varen automatisk. Så når en kvalitetsordre genereres automatisk, kontrollerer vareprøveplanen som er knyttet til kvalitetsordren, både hvor mange varer som er sperret og hvor mange varer som skal kontrolleres. Hvis det er merket av for **Full blokkering** på **Vareprøve**-siden, blokkeres for eksempel hele antallet på en bestillingslinje under inspeksjon, uavhengig av vareprøveantallet.

### <a name="example"></a>Eksempel

I eksemplet nedenfor genereres en kvalitetsordre når en følgeseddel for bestilling blir postert. På **Kvalitetstilknytninger**-siden angav du at postering av en bestillingsfølgeseddel er prosessen som aktiverer en kvalitetsordre.

|Konfigurasjon |Brukerhandling |Resultat |
|----|---|---|
| En kvalitetstilknytning angir at det må genereres en kvalitetsordre når en bestillingsfølgeseddel posteres. Vareprøveoppsettet for kvalitetsordren angir at 10 % av antallet på bestillingslinjen må kontrolleres. Og ettersom det er merket av for **Full blokkering** i vareprøveoppsettet, må hele antallet for bestillingslinjen blokkeres under inspeksjon, uavhengig av antallet som sendes til inspeksjon. | Følgeseddelen posteres. | En kvalitetsordre genereres. Ti prosent av bestillingsantallet for varen sendes til inspeksjon. Hele antallet på bestillingslinjen er blokkert. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Blokkere varer ved å bruke blokkering av beholdningsstatus

Du kan angi hvilke beholdningsstatuser som er blokkeringsstatuser ved hjelp av parameteren **Lagerblokkering** på **Beholdningsstatuser**-siden.  Du kan ikke bruke lagerstatuser som blokkeringsstatuser for produksjonsordrer, salgsordrer, overføringsordrer, utgående transaksjoner og prosjektintegrering. Når det gjelder utgående arbeid, bruker du varer som har en tilgjengelig lagerstatus. Hvis varer har statusen **Brutt** og hovedplanlegging kjøres på disse varene, blir varene ansett som manglende, og beholdningen etterfylles automatisk.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Vær forsiktig når du blokkerer varer som bruker både lagerstatusblokkering og blokkering av kvalitetsordre

Du kan opprette en kvalitetsordre som er knyttet til lageret, og der lagerstatusens parameter **Lagerblokkering** er aktivert. I dette tilfellet vil kvalitetsordren generere en ekstra lagerblokkeringspost i tillegg til den som opprettes av lagerstatusen. Ettersom lagerblokkeringen for kvalitetsordren vil ha parameteren **Forventede mottak** aktivert, genererer dette en ekstra transaksjon for *Bestilt beholdning* som også er blokkert av beholdningsstatusen. Denne kombinasjonen kan føre til vanskeligheter med å skjønne meningen med genererte lagertransaksjoner, fordi det vil se ut som om totalt blokkert antall er høyere enn totalbeholdningen. La oss undersøke transaksjonene på et eksempel på et mottak av 10 stykker av vare A0001 med en kvalitetsordre som er generert til et eksempel på 1 stykk. Virkemåten vil også være avhengig av om alternativet **Reserver bestilte varer** er aktivert på siden **Parametere for beholdnings- og lagerstyring**.

>[!NOTE]
>Hvis du bruker lagerstatusblokkering og kvalitetsordrer sammen, anbefales det på det sterkeste at alternativet **Reserver bestilte varer** er aktivert.

### <a name="example-with-reserve-ordered-items-enabled"></a>Eksempel med Reserver bestilte varer aktivert

Når **Reserver bestilte varer** er aktivert, får alle lagerblokkeringstransaksjoner statusen *Fysisk reservert* eller *Reservert av bestilt*.

| Lagertransaksjonsreferanse | Tilgang | Problem | Antall | Site | Lager | Beholdningsstatus | Lokasjon | Nummerskilt | Kommentar |
|---|---|---|---|---|---|---|---|---|---|
| Bestilling | Kjøpt | | 10 stk | 2 | 24 | Blokkering | RECV | receiptLp1 | | 
| Lagerblokkering | | Fysisk reservert | -9 stk | 2 | 24 | Blokkering | | | Transaksjon som genereres av lagerstatusblokkeringen |
| Lagerblokkering | | Fysisk reservert | -1 stk | 2 | 24 | Blokkering | RECV | receiptLp1 | Transaksjon som genereres av prøveblokkering for kvalitetsordre |
| Lagerblokkering | Bestilt | | 1 stk | 2 | 24 | Blokkering | RECV | receiptLp1 | Forventede mottak fra prøveblokkering for kvalitetsordren |
| Lagerblokkering | | Reservert av bestilt | 1 stk | 2 | 24 | Blokkering | | | Transaksjon som genereres av lagerstatusblokkeringen

### <a name="example-with-reserve-ordered-items-disabled"></a>Eksempel med Reserver bestilte varer deaktivert

Når **Reserver bestilte varer** er deaktivert, kan ikke de forventede mottakene reserveres fordi de har statusen *Bestilt*, slik at delvis blokkering fortsatt vil eksistere i statusen *I ordre*.

| Lagertransaksjonsreferanse | Tilgang | Problem | Antall | Site | Lager | Lagerstatus | Lokasjon | Nummerskilt | Kommentar |
|---|---|---|---|---|---|---|---|---|---|
| Bestilling | Kjøpt | | 10 stk | 2 | 24 | Blokkering | RECV | receiptLp1 | |
| Lagerblokkering | | Fysisk reservert | -9 stk | 2 | 24 | Blokkering | | | Transaksjon som genereres av lagerstatusblokkeringen |
| Lagerblokkering | | Fysisk reservert | -1 stk | 2 | 24 | Blokkering | RECV | receiptLp1 | Transaksjon som genereres av prøveblokkering for kvalitetsordre |
| Lagerblokkering | Bestilt | | 1 stk | 2 | 24 | Blokkering | RECV | receiptLp1 | Forventede mottak fra prøveblokkering for kvalitetsordren |
| Lagerblokkering | | I ordre/bestilling | 1 stk | 2 | 24 | Blokkering | RECV | receiptLp1 | Transaksjon som genereres av lagerstatusblokkeringen

Legg merke til forskjellen i transaksjonsstatus og dimensjoner mellom de to tilfellene. Av denne grunnen anbefales det at du aktiverer alternativet **Reserver bestilte varer**.

<!-- KFM: (Enable this section when the feature leaves private preview)

### Disable expected receipts from quality orders that sample blocked inventory feature

To simplify the inventory transactions in the case of quality orders that sample inventory blocked as a consequence of inventory status, the system provides a feature that disables expected receipts from such quality orders. As the expected receipt is in any case immediately blocked by inventory status blocking, there is no reduction of on-hand inventory because of this change.

-->

## <a name="additional-resources"></a>Tilleggsressurser

[Opprette og vedlikeholde en lagerblokkering](tasks/create-maintain-inventory-blocking.md)

[Kvalitetsstyringsprosesser](quality-management-processes.md)

[Kontrollere varekvaliteten](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]