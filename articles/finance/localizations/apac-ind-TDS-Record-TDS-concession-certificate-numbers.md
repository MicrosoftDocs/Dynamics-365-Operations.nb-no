---
title: Registrere TDS-konsesjonssertifikatnumre
description: Denne artikkelen forklarer hvordan du registrerer TDS-konsesjonssertifikatnumre (Tax Deducted at Source) som utstedes til leverandører.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 116bc5c4b4f5f0b95d05dc73f2a012fbbc065bf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846620"
---
# <a name="record-tds-concession-certificate-numbers"></a>Registrere TDS-konsesjonssertifikatnumre

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du registrerer TDS-konsesjonssertifikatnumre (Tax Deducted at Source) som utstedes til leverandører.

1. Gå til **Avgift \> Indirekte avgifter \> Kildeskatt \> Kildeskattkonsesjoner**.
2. Velg **TDS** i **Avgiftstype**-feltet for å registrere konsesjonssertifikater for TDS-avgiftstypen.
3. Trykk på **ALT+N** i **Oversikt**-fanen for å opprette en linje.

    [![Topptekst for den nye linjen.](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. I feltet **Kildeskattkode** velger du TDS-avgiftskoden som konsesjonssertifikatene for leverandør er utstedt for. Feltet **Navn på kildeskattkode** viser navnet på TDS-avgiftskoden.
5. Definer gyldighetsperioden for konsesjonssertifikatet som bruker TDS-avgiftskoden til å beregne TDS for leverandøren på en konsesjonsmessig basis, i feltene **Fra-dato** og **Til-dato**.
6. Skriv inn eventuelle kommentarer i **Kommentarer**-feltet.
7. I **Paragraf**-feltet angir du den rettslige paragrafkoden som TDS-konsesjonssertifikatet brukes under.

    Hvis paragrafkoden er 197, vises verdien «A» i både kolonnen «Reason for non-deduction/lower deduction» i Form 26Q og kolonnen «Reason for non-deduction/lower deduction/grossing up (if any)» i Form 27Q. Hvis paragrafkoden er 197A, vises verdien «B» begge disse stedene.

8. Velg hurtigfanen **Sertifikat** for å registrere TDS-konsesjonssertifikatnumre for leverandører.
9. I **Leverandørkonto**-feltet velger du leverandørkontoen som TDS-konsesjonssertifikatet er utstedt for.
10. Definer gyldighetsperioden for TDS-konsesjonssertifikatet i feltene **Fra-dato** og **Til-dato**.

    Beregningen av TDS på konsesjonsmessig basis er basert på perioden når sertifikatet opprettes for leverandøren.

11. Angi TDS-konsesjonssertifikatnummeret i **Sertifikat**-feltet.

    [![Hurtigfanen Sertifikat.](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Lukk siden.
