---
title: Du finner ikke rullegardinboksen Arbeidsflyt for lagerjournaler
description: Du finner ikke rullegardinboksen "Arbeidsflyt" på journalsiden, eller relaterte arbeidsflytoperasjoner er ikke tilgjengelige
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477182"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Du finner ikke rullegardinboksen Arbeidsflyt for lagerjournaler

## <a name="symptoms"></a>Symptomer

Du finner ikke rullegardinboksen **Arbeidsflyt** på journalsiden, eller relaterte arbeidsflytoperasjoner er ikke tilgjengelige.

Dette problemet kan oppstå av tre årsaker, som beskrevet i delene nedenfor.

## <a name="resolution-1"></a>Løsning 1

Hvis problemet gjelder alle brukere, kan årsaken være at godkjenningsarbeidsflyten ikke er tilordnet til journalnavnet. Følg fremgangsmåten nedenfor for å løse problemet.

1. Gå til **Lagerstyring &gt; Oppsett &gt; Journalnavn &gt; Beholdning**.
1. I listeruten velger du et journalnavn for å åpne innstillingene for den.
1. I hurtigfanen **Generelt** angir du *Ja* for alternativet **Arbeidsflyt for godkjenning**. Hvis du blir bedt om å bekrefte endringen, velger du **Ja**.
1. Velg arbeidsflyten du vil bruke for det valgte journalnavnet, i **Arbeidsflyt**-feltet.

## <a name="resolution-2"></a>Løsning 2

Hvis arbeidsflyten bruker tilpasset kode, kan det oppstå problemer etter at du har oppgradert systemet. **Send inn**-knappen kan for eksempel være nedtonet i journalarbeidsflyten, slik at du ikke kan velge den for å godkjenne en innsending.

Hvis **Send inn**-knappen er nedtonet, kan arbeidsflyten ha blitt tilpasset, som betyr at metoden for arbeidsflyten, `canSubmitToWorkflow()` i `FormDataUtil`, har blitt utvidet. Du kan rette dette problemet ved å endre hvordan du utvider metoden for `canSubmitToWorkflow()`, slik at den bruker strukturen i følgende eksempel.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Løsning 3

Hvis problemet bare gjelder noen få bestemte brukere, kan det hende at disse brukerne ikke har sikkerhetsrettighetene som kreves for å kjøre arbeidsflytoperasjoner på lagerjournaler. Kontroller at hver berørte bruker har sikkerhetsrettigheten *Vedlikehold lagerjournalarbeidsflyt*. Denne rettigheten er som standard tilordnet til en plikt med samme navn, og denne plikten brukes på rollene *Lagerarbeider* og *Lagersjef*.
