---
title: Opprette en erstatningsordre for vare
description: Erstatningsordrer for varer opprettes vanligvis etter at et produkt er returnert og kontrollert.
author: josaw1
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14751fb0e0632ca986d6eddf55c93d44fbd68276
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015471"
---
# <a name="create-an-item-replacement-order"></a>Opprette en erstatningsordre for vare 

[!include [banner](../includes/banner.md)]


Erstatningsordrer for varer opprettes vanligvis etter at et produkt er returnert og kontrollert. Når en vare må erstattes før den er returnert, eller når originalvaren ikke vil bli returnert, kan du opprette en erstatningsordre for en vare rett etter at du har opprettet en returordre.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Opprette en erstatningsordre når du mottar en returnert vare

1.  Klikk på **Salg og markedsføring** \> **Salgsreturer** \> **Alle returordrer**.

2.  Opprett en ny returordre eller velg en returordre fra listen, for å åpne skjemaet **Returordre – autorisasjonsreturnr.: %1, %2**.

3.  Klikk på **Returlinje**, og velg deretter **Erstatningsvare**.

4.  Velg varen du vil erstatte den returnerte varen med. Angi spesifikasjonene for varen, og klikk deretter **Bruk**.

5.  Klikk på **Følgeseddel** for å generere følgeseddelen for returordren. En salgsordre genereres for erstatningsvaren som du har valgt.
    
    Når salgsordren er opprettet for erstatningsvaren, søkes det automatisk i salgsavtalene, og hvis det finnes en gjeldende salgsavtale, gjøres den gjeldende for slagsordren.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Opprette en erstatningsordre før du mottar en vare som vil bli returnert

1.  Klikk på **Salg og markedsføring** \> **Salgsreturer** \> **Alle returordrer**.

2.  Opprett en ny returordre eller velg en returordre fra listen, for å åpne skjemaet **Returordre – autorisasjonsreturnr.: %1, %2**.

3.  Klikk på **Søk etter salgsordre** hvis du vil finne salgsordren for den returnerte varen. Fyll ut skjemaet **Søk etter salgsordre**, og klikk deretter **OK** for å lukke skjemaet og gå tilbake til skjemaet **Returordre – autorisasjonsreturnr.: %1, %2**. Salgsordrelinjen for den returnerte varen kopieres til returordren.

4.  Klikk på **Erstatningsordre** for å åpne skjemaet **Opprett salgsordre**.

5.  Merk av for **Kopier returordrelinjer** for å overføre detaljer fra returordren du valgte i skjemaet **Returordre – autorisasjonsreturnr.: %1, %2**, til denne salgsordren.

6.  Angi eller endre detaljer etter behov.
    
    Hvis du identifiserte salgsordren i trinn 3 og salgsordrelinjen for den returnerte varen er koblet til salgsavtalen, vil ID-en for gjeldende salgsavtale for erstatningsordren for varen automatisk vises i feltet **Salgsavtale-ID**.

7.  Klikk på **OK** for å lukke skjemaet **Opprett salgsordre** og åpne skjemaet **Salgsordre**, der du kan fortsette å angi informasjon for den nye salgsordren. Eventuelle gjeldende returordrelinjer kopieres til den nye salgsordren. 
    
    Hvis ID-en for salgsavtalen automatisk vises i feltet **Salgsavtale-ID**, er salgsavtalen koblet til salgsordrehodet for erstatningsordren for varen. Hvis det finnes en gjeldende forpliktelse i salgsavtalen som ikke er oppfylt ennå, og salgsordren opprettes før salgsavtalen utløper, blir det opprettet en kobling mellom salgsavtalelinjen og salgsordrelinjen. Informasjon fra salgsavtalen, for eksempel varepris, kopieres derfor til den nye salgsordrelinjen. 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]