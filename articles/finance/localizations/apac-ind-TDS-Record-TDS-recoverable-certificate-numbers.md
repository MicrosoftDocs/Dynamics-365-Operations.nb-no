---
title: Registrer numre på fradragsberettigede TDS-sertifikater
description: Dette emnet forklarer hvordan du bruker siden Fradragsberettigede sertifikater til å registrere sertifikatnumrene og -datoene for TDS-sertifikater (Tax Deducted at Source) for en bestemt leverandør, kunde eller finans.
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
ms.openlocfilehash: 8fa4d1200818b4657b044a376ebb292426250ae1
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407746"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Registrer numre på fradragsberettigede TDS-sertifikater

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du bruker siden **Fradragsberettigede sertifikater** til å registrere sertifikatnumrene og -datoene for TDS-sertifikater (Tax Deducted at Source) for en bestemt leverandør, kunde eller finans. Hvis du vil oppdatere TDS-sertifikatnumrene og -datoene som er registrert for TDS-transaksjoner på denne siden, bruker du siden **Oppdater sertifikat** (**Økonomimodul \> Periodisk \> Kildeskatt \> Oppdater sertifikat**). Når du er ferdig å oppdatere TDS-sertifikatnumre, lukker du dem.

Følg denne fremgangsmåten for å registrere TDS-sertifikatnumrene og -datoene.

1. Gå til **Avgift \> Indirekte avgift \> Kildeskatt \> Fradragsberettigede sertifikater**.

    [![Siden Fradragsberettigede sertifikater.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Velg **TDS** i **Avgiftstype**-feltet på siden **Fradragsberettigede sertifikater**.
3. Velg **Ny** for å opprette en oppføring.
4. Angi TDS-sertifikatnummeret i **Sertifikatnummer**-feltet.
5. I **Kontotype**-feltet velger du kontotypen som TDS-sertifikatet mottas for: **Leverandør**, **Kunde** eller **Finans**.
6. I **Konto**-feltet velger du nummeret på leverandør-, kunde- eller finanskontoen, avhengig av kontotypen du har valgt. **Navn**-feltet viser navnet på leverandør-, kunde- eller finanskontoen.
7. I **Sertifikatbeløp**-feltet angir du beløpet på TDS-sertifikatet.
8. Angi sertifikatdatoen for sertifikatnummeret i **Dato**-feltet.
9. Velg **Forespørsler** for å åpne siden **Sertifikattransaksjoner**, der du kan vise TDS-transaksjonene som TDS-sertifikatnummeret og -datoen er oppdatert for. Denne informasjonen kan oppdateres på siden **Oppdater sertifikat** (**Avgift \> Deklareringer \> Kildeskatt \> Oppdater sertifikat**).

    Siden **Oppdater sertifikat** viser følgende informasjon for hver TDS-transaksjon:

    - **Dato** – Posteringsdatoen for TDS-transaksjonen.
    - **Bilag** – Bilagsnummeret for TDS-transaksjonen.
    - **Kilde** – Modulen som TDS-transaksjonen ble opprettet i.
    - **Konto** – Nummeret på leverandør-, kunde- eller finanskontoen som TDS-transaksjonen ble opprettet for.
    - **Navn** – Navnet på leverandør-, kunde- eller finanskontoen som TDS-transaksjonen ble opprettet for.
    - **Beløp** – Fakturabeløpet som TDS ble beregnet for.
    - **Avgiftsbeløp** – TDS-avgiftsbeløpet som ble beregnet for transaksjonen.
    - **Sertifikatdato** – TDS-sertifikatdatoen som ble oppdatert for TDS-transaksjonen.
    - **Sertifikatnummer** – TDS-sertifikatnummeret som ble oppdatert for TDS-transaksjonen.

10. Merk av for **Lukket** på siden **Fradragsberettigede sertifikater** for å lukke TDS-sertifikatnummeret etter at du er ferdig å oppdatere det for TDS-transaksjoner på siden **Oppdater sertifikat**.

    Hvis du vil merke av for **Lukket** for alle poster på siden, velger du **Merk alle**.

    > [!NOTE]
    > TDS-sertifikatnumre som alternativet **Lukket** er merket av for, er ikke tilgjengelige på siden **Oppdater sertifikat**.
