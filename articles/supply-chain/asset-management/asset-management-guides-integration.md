---
title: Integrere Dynamics 365 Supply Chain Management (Aktivabehandling) med Dynamics 365 Guides
description: Dette emnet forklarer hvordan du integrerer Aktivabehandling-modulen i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides for å dra nytte av veiledninger for to virkelighet i de daglige tjeneste- og vedlikeholdsarbeidsflytene.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: e3e9e74397faec12f6eecff1f562fd9d731ac5e2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230158"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Integrere Dynamics 365 Supply Chain Management (Aktivabehandling) med Dynamics 365 Guides

Du kan integrere **Aktivabehandling**-modulen i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides for å dra nytte av veiledninger for to virkelighet i de daglige tjeneste- og vedlikeholdsarbeidsflytene. Hvis en veiledning er knyttet til en arbeidsordre for aktivastyring, vil en arbeider som åpner kontrolliste for vedlikehold for arbeidsordren i mobilappen for Supply Chain Management (Dynamics 365), se at en veiledning er tilgjengelig. Arbeideren kan deretter finne og åpne veiledningen i Dynamics 365 Guides HoloLens-appen.

## <a name="prerequisites"></a>Forutsetninger

Før du kan dra nytte av veiledninger for arbeidsordrer for aktivabehandling, må du fullføre disse forutsetningene:

- [Konfigurer Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) versjon 10.0.9 eller senere.
- [Aktivere toveis skriving for Supply Chain Management-apper](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Aktiver testversjon](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for **MRGuidesFeature**-funksjonen. (For produksjonsmiljøer må du først sende en støtteforespørsel for å få leieren din lagt til i kontrollgruppen.)
- [Slå på følgende konfigurasjonsnøkler](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) på **Lisenskonfigurasjon**-siden:

    - Aktivabehandling \> Aktivabehandling, blandet virkelighet
    - Blandet virkelighet \> Blandet virkelighet-veiledning

- [Konfigurer Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versjon 200.0.0.96 eller senere.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Bruke Dynamics 365 Guides med aktivastyring

Hvis du vil knytte til en veiledning, bruker du en kontrollistelinje for vedlikehold i Aktivabehandling. Du kan opprette tilknytningen gjennom en mal for kontrolliste for vedlikehold, en vedlikeholdsjobbtype eller en arbeidsordre, fordi alle tre inneholder vedlikeholdssjekklistelinjer. Du kan spare tid ved hjelp av en mal, fordi en mal kan knyttes til alle vedlikeholdsjobbtypene som bruker den. En veiledning som for eksempel er tilknyttet en vedlikeholdsjobbtype, knyttes automatisk til alle arbeidsordrer som angir denne jobbtypen. På den andre siden vil en veiledning som er knyttet direkte til en arbeidsordre, bare finnes for den aktuelle arbeidsordren.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Knytte en veiledning til en mal for kontrolliste for vedlikehold

Følg disse trinnene for å knytte en veiledning til en mal for kontrolliste for vedlikehold.

1. Opprett en veiledning ved å bruke Dynamics 365 Guides-PC og HoloLens-apper. Hvis du vil ha informasjon om hvordan du oppretter en veiledning, kan du se emnene nedenfor:

    - [Bruke PC-appen til å opprette en veiledning](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Bruke HoloLens-appen til å plassere hologrammene](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. I Supply Chain Management [oppretter du en mal for vedlikeholdssjekkliste](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Knytt til veiledningen du opprettet ved hjelp av kontrollistelinjen for vedlikehold i den nye malen for vedlikeholdssjekkliste:

    1. I hurtigfanen **Vedlikeholdssjekklistelinjer** velger du linjen du vil knytte veiledningen til.
    1. På hurtigfanen **Tilknyttede veiledninger** velger du **Legg til veiledning**.

        ![Knytte en veiledning til en kontrollistelinje for vedlikehold](media/am-guides-integration-add-guide.png "Knytte en veiledning til en kontrollistelinje for vedlikehold")

    1. I **Navn**-feltet velger du veiledningen og deretter **Lagre**.

        ![Velg en veiledning i Navn-feltet](media/am-guides-integration-select-guide.png "Velg en veiledning i Navn-feltet")

1. Knytt kontrollistemalen for vedlikehold til en jobbtype:

    1. [Opprett en vedlikeholdsjobbtype](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), eller velg en eksisterende vedlikeholdsjobbtype.
    1. Velg **Standarder for vedlikeholdsjobbtype** i handlingsruten.

        ![Knappen Standarder for vedlikeholdsjobbtype](media/am-guides-integration-job-defaults.png "Knappen Standarder for vedlikeholdsjobbtype")

    1. Opprett en linje, og velg deretter **Lagre**.

        ![Opprett en linje](media/am-guides-integration-add-line.png "Opprett en linje")

    1. Velg **Sjekkliste for vedlikehold** på handlingsruten.

        ![Knappen Sjekkliste for vedlikehold](media/am-guides-integration-maintenance-checklist.png "Knappen Sjekkliste for vedlikehold")

    1. På hurtigfanen **Vedlikeholdssjekklistelinjer** legger du til en linje, og deretter endrer du verdien i feltet **Type** til **Mal**.

        ![Endre Type-verdien](media/am-guides-integration-checklist-lines.png "Endre Type-verdien")

    1. I hurtigfanen **Linjedetaljer** i feltet **Mal** velger du malen du vil knytte veiledningen til, og deretter valger du **Lagre**.

        ![Velg malen](media/am-guides-integration-checklist-line-details.png "Velg malen")

1. [Opprett en arbeidsordre](work-orders/manually-created-workorders.md#create-work-order), og velg deretter vedlikeholdsjobbtypen som bruker sjekklistemalen for vedlikehold som du knyttet veiledningen til. Veiledning knyttes automatisk til arbeidsordren.

    ![Velg en vedlikeholdsjobbtype](media/am-guides-integration-create-work-order.png "Velg en vedlikeholdsjobbtype")

1. Vis veiledningen som er knyttet til arbeidsordren og arbeiderne:

    1. Åpne [Mobilt arbeidsområde for aktivabehandling](asset-management-mobile-workspace.md) for å få tilgang til arbeidsordren.
    1. [Åpne kontrollisten for vedlikehold](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for arbeidsordren.
    1. Velg en sjekklistelinje for å vise den tilknyttede veiledningen.

        ![Veiledning tilknyttet en sjekklistelinje](media/am-guides-integration-show-guide.png "Veiledning tilknyttet en sjekklistelinje")

    1. Åpne veiledningen på HoloLens.

        ![Åpne veiledningen på HoloLens](media/am-guides-integration-hololens-select.png "Åpne veiledningen på HoloLens")

> [!NOTE]
> Du kan også tilknytte en veiledning direkte i kontrolliste for vedlikehold for en arbeidsordre eller en jobbtype.

> [!IMPORTANT]
> Det finnes et kjent problem: Når du knytter en sjekklistemal for vedlikehold til en standard vedlikeholdsjobbtype, vises ikke veiledningen som er koblet til malen, på hurtigfanen **Tilknyttede veiledninger** på siden **Standarder for vedlikeholdsjobbtype**. Veiledningen vises imidlertid etter at denne jobbtypen er brukt på en arbeidsordre på hurtigfanen **Tilknyttede veiledninger**.

## <a name="see-also"></a>Se også

- [Oversikt over dobbel skriving](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Oversikt over anleggsmiddelbehandling](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]