---
title: Vedlikeholdspersoner og arbeidsgrupper
description: Denne artikkelen forklarer vedlikeholdspersoner og arbeidergrupper i Aktivastyring.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a24c880ee76af1490824aef07976b998d9225d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860906"
---
# <a name="maintenance-workers-and-worker-groups"></a>Vedlikeholdspersoner og arbeidsgrupper

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen forklarer vedlikeholdspersoner og arbeidergrupper i Aktivastyring. I Aktivastyring kan du koble vedlikeholdspersoner arbeidere til arbeidssteder. (Hvis du vil ha mer informasjon om arbeidssteder, se [Opprette arbeidssteder](../functional-locations/create-functional-locations.md).) Denne funksjonaliteten kan være nyttig hvis du for eksempel planlegger en vedlikeholdsjobb på en maskin som er plassert på arbeidssted 01, og du vil tilordne vedlikeholdspersoner fra samme sted til å utføre jobben.

Du kan også opprette vedlikeholdspersongrupper og knytte vedlikeholdspersoner til dem. Denne funksjonaliteten er nyttig når du utfører enkel ordreplanlegging, og du vil planlegge en gruppe med vedlikeholdspersoner i en arbeidsordre. Du kan bruke vedlikeholdspersoner og vedlikeholdspersongrupper til å definere foretrukne vedlikeholdspersoner og ansvarlige for vedlikeholdspersoner. 


## <a name="create-workers"></a>Opprett arbeidere

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidere** \> **Arbeidere**.
2. Velg **Ny** for å legge til en ny arbeider i listen.
3. Velg arbeideren i **Arbeider**-feltet.
4. Sett **Aktiv**-alternativet til **Ja** for å planlegge arbeideren på arbeidsordrer.

    I hurtigfanen **Generelt** fylles feltene **Ressurs** og **Beskrivelse** ut automatisk hvis en ressurs er valgt for arbeideren. **Kalender**-feltet fylles også automatisk ut, forutsatt at du har definert arbeideren som en ressurs og tildelt en kalender til ressursen på **Ressurser**-siden (**Organisasjonsadministrasjon** \> **Ressurser** \> **Ressurser**).

5. På hurtigfanen **Grupper** velger du **Legg til**, og velg deretter en vedlikeholdspersongruppe for arbeideren. En arbeider kan knyttes til flere enn én gruppe.
6. I standardoppsettet er en arbeiders tilknytning til en gruppe gyldig fra datoen når du legger til gruppen, og den utløper aldri. Denne datoen vises i **Gyldighet**-feltet. Hvis du vil se **Gyldighet**-feltet, velger du **Vis** \> **Alle**. Hvis arbeiderens tilknytning til en gruppe, skal være begrenset til en bestemt periode, bruker du feltene **Gyldighet** og **Utløp** felt til å definere perioden.
7. På hurtigfanen **Arbeidssteder** velger du **Legg til**, og velg deretter et arbeidssted for vedlikeholdspersonen. Angi også hvilket sted som er det primære arbeidsstedet for arbeideren.

    > [!NOTE]
    > Når du legger til arbeidssteder for en arbeider, vises alle aktive aktiva som er relatert til arbeidsstedene, på ulike menyelementer, for eksempel **Mine aktiva aktiva** og **Mine aktive arbeidssteder**. De vises også i aktivaoppslagene som vises når du oppretter et nytt aktivum, en melding eller en arbeidsordre.

    Feltene på hurtigfanen **Detaljer** viser antall vedlikeholdspersongrupper og arbeidssteder som den valgte vedlikeholdspersonen er relatert til.

## <a name="create-worker-groups"></a>Opprett arbeidergrupper

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidere** \> **Vedlikeholdspersongrupper**.
2. Velg **Ny** for å legge til en ny arbeidergruppe i listen.
3. Angi en gruppe-ID i feltet **Vedlikeholdspersongruppe**.
4. Angi et navn i **Navn**-feltet.
5. På hurtigfanen **Arbeidere** velger du **Legg til**, og velg deretter en vedlikeholdsperson for arbeidergruppen. Hvis du vil ha informasjon om feltene **Gyldighet** og **Utløp**, kan du se trinn 6 i forrige fremgangsmåte.
6. Hvis en ressursgruppe skal knyttes til den valgte vedlikeholdspersongruppen, velger du **Kopier fra ressursgruppe**. I **Gruppe**-feltet velger du ressursgruppen du vil kopiere kalenderinnstillinger fra. I feltet **Arbeidsgruppe** velger du arbeidergruppen du vil kopiere kalenderinnstillingene for ressursgruppen til. Dette trinnet er bare relevant hvis du vil at vedlikeholdspersoner skal bruke kalenderen som er relatert til en ressurs (arbeidssenter) under arbeidsordreplanlegging.

    Feltet på hurtigfanen **Detaljer** viser antall vedlikeholdspersoner som er definert for den valgte vedlikeholdspersongruppen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]