---
title: Skrive ut avgiftsinformasjon på overføringsordredokumenter
description: Dette emnet beskriver hvordan skatteinformasjonen som bestemmes av skatteberegningstjenesten, kan skrives ut på overføringsordredokumenter.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: d55767ef47e01edd11099f644134cfa48ea70e18
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675740"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Skrive ut avgiftsinformasjon på overføringsordredokumenter

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Dette emnet forklarer hvordan du skriver ut avgiftsinformasjon på overføringsordredokumenter. Du kan skrive ut proforma-fakturadokumentet for en overføringsordre for lageroverføringer som betraktes som fellesskapsforsyning og fellesskapsanskaffelse under EU-bestemmelser om merverdiavgift. 

Følgende avgiftsrelevante data legges til i overføringsordredokumentene:

- Navnene og forsendelses- og forsendelsesadressene for lageroverføringen
- Skatteidentifikasjonsnumrene til leverandøren og mottakeren
- Enhetsprisen og det avgiftspliktige beløpet for de leverte varene
- Mva-koden, mva-satsen, mva-beløpet og avgiftsdirektivene

Hvis du vil konfigurere disse dataene, må du gå gjennom følgende hovedtrinn.

1. [Aktiver og definer avgiftsfunksjonen for overføringsordrer](tasks/Tax-feature-support-for-transfer-order.md).
2. [Opprett og definer flere avgiftsregistreringsnumre for en juridisk enhet](emea-multiple-vat-registration-numbers.md).
3. Definer fritakskoden, beskrivelsen, mva-direktivene og skriv ut koden i avgiftskoder. For dette eksemplet opprettes og synkroniseres det tre avgiftskoder i Microsoft Dynamics 365 Finance: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.

    1. I Finance går du til **Avgift** \> **Oppsett** \> **Merverdiavgift** \> **Mva-fritakskoder**.
    2. Velg **Rediger**, og angi en beskrivelse for **EC**-fritakskoden. Du kan for eksempel angi **Avgiftsfrie EU-forsendelser med avgiftsregistreringsnummer**.
    3. Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.
    4. Velg **BE-RC-21**-avgiftskoden, og velg deretter **Avgiftsdirektiver**.
    5. Velg **Ny**.
    6. I **Språk**-feltet velger du **EN-US**. I **Tekst**-feltet angir du deretter **Dokument som angir overføringen av varer i henhold til artikkel 138. 2. c) i EU VAT Directive 2006/112/EC**.
    7. Lukk siden.
    8. I hurtigfanen **Generelt** i **Skriv ut**-feltet velger du **Mva-sats**.
    8. Velg **NL-Exempt**-avgiftskoden. I hurtigfanen **Generelt** i **Skriv ut**-feltet, velger du deretter **Mva-sats**.

    > [!NOTE] 
    > Mva-koden, mva-satsen og beskrivelse av avgiftsfritak skrives ikke ut på overføringsordredokumenter hvis det ikke vedlikeholdes noen beskrivelse av avgiftskoden eller avgiftsdirektivene.

## <a name="print-the-transfer-order---shipment-document"></a>Skrive ut overføringsordren – forsendelsesdokument

Når en overføring er sendt, følger du fremgangsmåten nedenfor for å skrive ut overføringsordren – forsendelsesdokumentet.

1. Gå til **Lagerstyring** \> **Forespørsler og rapporter** \> **Overføringsordrer** \> **Forsendelse**.
2. i fanen **Parametere** i **Skriv ut**-gruppen aktiverer du **Avgiftsinformasjon**.
3. I fanen **Poster som skal inkluderes** velger du **Filter**, velg overføringsordrenummeret, og velg **OK**.
4. Velg **OK** for å skrive ut overføringsordren – forsendelsesdokument.

## <a name="print-the-transfer-order---receipt-document"></a>Skrive ut overføringsordren – kvitteringsdokument

Når en overføring er mottatt, følger du fremgangsmåten nedenfor for å skrive ut overføringsordren – kvitteringsdokumentet.

1. Gå til **Lagerstyring** \> **Forespørsler og rapporter** \> **Overføringsordrer** \> **Motta**.
2. i fanen **Parametere** i **Skriv ut**-gruppen aktiverer du **Avgiftsinformasjon**.
3. I fanen **Poster som skal inkluderes** velger du **Filter**, velg overføringsordrenummeret, og velg **OK**.
4. Velg **OK** for å skrive ut overføringsordren – kvitteringsdokumentet.

## <a name="print-the-transfer-overview-document"></a>Skrive ut dokumentet for overføringsoversikt

Følg denne fremgangsmåten for å skrive ut dokumentet for overføringsoversikt.

> [!NOTE]
> Skatteinformasjon er bare tilgjengelig når overføringsordren er sendt eller mottatt.

1. Gå til **Lagerstyring** \> **Forespørsler og rapporter** \> **Overføringsordrer** \> **Overføringsoversikt**.
2. i fanen **Parametere** i **Skriv ut**-gruppen aktiverer du **Avgiftsinformasjon**.
3. I fanen **Poster som skal inkluderes** velger du **Filter**, velg overføringsordrenummeret, og velg **OK**.
4. Velg **OK** for å skrive ut overføringsordren – overføringsdokumentet.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
