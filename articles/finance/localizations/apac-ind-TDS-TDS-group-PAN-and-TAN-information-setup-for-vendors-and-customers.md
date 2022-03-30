---
title: Konfigurere informasjon om TDS-gruppe, PAN og TAN for leverandører og kunder
description: Dette emnet forklarer hvordan du konfigurerer informasjon om TDS-gruppe (Tax Deducted at Source), permanent kontonummer (PAN) og TAN (Tax Account Number) for leverandører og kunder.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 808fa7b72651ab274415e48f5e0a356784ca6525
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407542"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Konfigurasjon av informasjon om TDS-gruppe, PAN og TAN for leverandører og kunder

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer informasjon om TDS-gruppe (Tax Deducted at Source), permanent kontonummer (PAN) og TAN (Tax Account Number) for leverandører og kunder.

1. Gå til **Leverandører \> Leverandører \> Alle leverandører** eller **Kunder \> Kunder \> Alle kunder**.

    [![Siden Alle leverandører.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Velg **Ny** i handlingsruten for å opprette en leverandør eller kunde, og angi de nødvendige detaljene. Du kan alternativt velge en eksisterende leverandør eller kunde.
3. Sett alternativet **Beregn kildeskatt** til **Ja** i **Kildeskatt**-delen i hurtigfanen **Faktura og levering** for å beregne kildeskatt, TDS eller TCS (Tax Collected at Source) for leverandøren eller kunden.
4. TDS for en innkjøpsfaktura beregnes basert på standard TDS-gruppe som er definert for leverandøren eller kunden. Velg standard TDS-gruppe i feltet **TDS-gruppe**.

    > [!NOTE]
    > Feltene **Kildeskattgruppe** og **TDS-gruppe** blir utilgjengelige når du velger en TDS-gruppe i feltet **TDS-gruppe**.

5. Velg statusen for det permanente kontonummeret for leverandøren eller kunden i **Status**-feltet i delen **PAN-informasjon** i hurtigfanen **Avgiftsinformasjon**:

    - **Ikke tilgjengelig** – Leverandøren eller kunden har ikke et PAN-nummer.
    - **Mottatt** – Leverandøren eller kunden har et PAN-nummer.
    - **Søkt** – Leverandøren eller kunden har søkt om et PAN-nummer.
    - **Ugyldig** – Leverandøren eller kunden har et PAN-nummer, men det er ikke gyldig.

6. Hvis du valgte **Mottatt** i **Status**-feltet for å angi at leverandøren eller kunden har et PAN-nummer, angir du PAN-nummeret i **Nummer**-feltet. PAN-nummeret må bestå av fem alfabetiske bokstaver, deretter fire numeriske tegn og deretter én alfabetisk bokstav. Her er et eksempel: **ABCDE1260A**.
7. Hvis du valgte **Søkt** i **Status**-feltet for å angi at leverandøren eller kunden har søkt om et PAN-nummer, angir du referansenummeret i feltet **Referansenummer**.
8. Velg kategorien for skattebetalertype som leverandøren eller kunden hører til i, i feltet **Skattebetalertype**.

    - Selskap
    - HUF
    - Firma
    - Enkeltvis
    - AOP
    - BOI
    - Lokale myndigheter
    - Annet

    [![Hurtigfanen Avgiftsinformasjon.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. Velg **Registrerings-ID-er** i **Registrering**-gruppen i **Leverandør**-fanen i handlingsruten for å åpne siden **Administrer adresser**.
10. Velg **Legg til** eller **Rediger** i hurtigfanen **Avgiftsinformasjon** på siden **Administrer adresser** for å åpne siden **Administrer avgiftsinformasjon**, der du kan vedlikeholde oppføringen for avgiftsregistrering.
11. Angi TAN-nummeret i feltet **TAN-nummer (Tax Account Number)** i hurtigfanen **Kildeskatt** på siden **Administrer avgiftsinformasjon**. TAN-nummeret må bestå av fire alfabetiske bokstaver, deretter fem numeriske tegn og deretter én alfabetisk bokstav. Her er et eksempel: **AFGH54821T**.
12. Lukk siden.
