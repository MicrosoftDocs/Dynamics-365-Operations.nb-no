---
title: Varekvalitetsgrupper
description: Dette emnet beskriver hvordan du kan bruke og opprette varekvalitetsgrupper for logisk å gruppere produkter slik at de kan tilordnes til kvalitetstilknytninger for automatisk generering av kvalitetsordrer.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f7a4932c561c052bec1eb0094a390e315b9b1bb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580918"
---
# <a name="item-quality-groups"></a>Varekvalitetsgrupper

[!include [banner](../includes/banner.md)]

En kvalitetsgruppe representerer felles testkrav for varer. Dette emnet beskriver hvordan du kan bruke og opprette varekvalitetsgrupper for logisk å gruppere produkter slik at de kan tilordnes til kvalitetstilknytninger for automatisk generering av kvalitetsordrer.

Gå til **Lagerstyring \> Oppsett \> Kvalitetsgrupper** for å definere, redigere og vise varene som er tilordnet til en kvalitetsgruppe, eller kvalitetsgruppene som er tilordnet til en vare. Når du har definert testkravene på siden **Testgrupper**, kan du definere reglene for automatisk generering av kvalitetsordrer. For å forenkle prosessen kan du ikke definere reglene for individuelle varer. I stedet definerer du regler for en kvalitetsgruppe på siden **Kvalitetstilknytninger**.

## <a name="example-of-an-item-quality-group"></a>Eksempel på en varekvalitetsgruppe

Et produksjonsfirma kjøper inn ulike råmaterialer som har samme testkrav for innkommende inspeksjon. Firmaet definerer derfor en kvalitetsgruppe og tilordner deretter varenumrene som er tilknyttet råvarene til denne gruppen. Senere kjøper selskapet en ny type råvarer som har samme testkrav. I stedet for å opprette nye testkrav for det nye materialet, legger firmaet til varenummeret for det nye materialet i den eksisterende kvalitetsgruppen.

Det samme firmaet produserer også varer med samme krav til produksjonstesting, og leverer varer med samme krav til utføring av tester før forsendelse. Firmaet definerer derfor to ekstra kvalitetsgrupper, og tilordner deretter de aktuelle varenumrene til hver gruppe.

## <a name="create-a-quality-group"></a>Opprette en kvalitetsgruppe

Hvis du vil opprette en kvalitetsgruppe, følger du disse trinnene.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetsgrupper**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Kvalitetsgruppe** – Angi en unik ID eller et unikt navn for kvalitetsgruppen.
    - **Beskrivelse** – Angi en detaljert beskrivelse av kvalitetsgruppen.

1. Lukk siden.

## <a name="manually-add-items-to-a-quality-group"></a>Legge til varer i en kvalitetsgruppe manuelt

Følg denne fremgangsmåten for å legge til varer manuelt i en kvalitetsgruppe.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetsgrupper**.
1. Velg kvalitetsgruppen som du vil legge til varer i.
1. Velg **Varer** i handlingsruten.
1. Velg **Ny** i handlingsruten på siden **Varer i kvalitetsgrupper** for å legge til en rad i rutenettet. Angi deretter **Varenummer**-feltet for den nye raden til varenummeret du vil legge til.
1. Gjenta det forrige trinnet for hver tilleggsvare du må legge til.
1. Lukk sidene.

## <a name="add-multiple-items-to-a-quality-group"></a>Legge til flere varer i en kvalitetsgruppe

Følg denne fremgangsmåten for å legge til flere varer i en kvalitetsgruppe.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetsgrupper**.
1. Opprett eller velg kvalitetsgruppen som du vil legge til varer i.
1. Velg **Legg til varer** i handlingsruten.
1. I dialogboksen **Forespørsel** angir du filterkriteriene for varene du vil legge til. Du kan for eksempel filtrere for alle varer i en bestemt varegruppe.
1. Velg **OK**.
1. I dialogboksen **Legg til varer** viser et rutenett alle varene som samsvarer med spørringen. Se gjennom resultatene.

    Hvis det kreves endringer, velger du **Velg** for å gå tilbake til dialogboksen **Forespørsel**, og justerer spørringen.

1. Når resultatene inkluderer alle varene du vil legge til, velger du **OK**.
1. Lukk siden.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Knytte en vare til en kvalitetsgruppe manuelt

Følg denne fremgangsmåten for å knytte til en vare manuelt i en kvalitetsgruppe.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Varekvalitetsgrupper**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Varenummer** – Velg varenummeret du vil legge til.
    - **Kvalitetsgruppe** – Velg kvalitetsgruppen som skal tilordnes varen.

1. Gjenta det forrige trinnet for hver ekstra kombinasjon av en vare og en kvalitetsgruppe som må legges til.
1. Lukk sidene.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Legge til en kvalitetsgruppe manuelt fra Frigitte produkter-siden

Følg denne fremgangsmåten for å legge til en kvalitetsgruppe manuelt fra **Frigitte produkter**-siden.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg produktet du vil tilordne en kvalitetsgruppe til.
1. I handlingsruten, i fanen **Administrer lager** i gruppen **Kvalitet**, velger du **Varekvalitetsgrupper**.
1. Velg **Ny** i handlingsruten på siden **Varer i kvalitetsgrupper** for å legge til en rad i rutenettet. Angi deretter **Kvalitetsgruppe**-feltet for den nye raden til kvalitetsgruppen du vil tilordne til produktet.
1. Gjenta det forrige trinnet for hver ekstra kvalitetsgruppe du vil tilordne til produktet.
1. Lukk sidene.

## <a name="additional-resources"></a>Tilleggsressurser

- [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md)
- [Kvalitetsstyringstester](quality-tests.md)
- [Testgrupper for kvalitetsstyring](quality-test-groups.md)
- [Testvariabler for kvalitetsstyring](quality-test-variables.md)
- [Kvalitetstilknytninger](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
