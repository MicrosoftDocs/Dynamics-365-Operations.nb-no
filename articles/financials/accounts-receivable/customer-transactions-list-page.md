---
title: Listeside for kundetransaksjoner
description: Dette emnet gir informasjon om listesiden for kundetransaksjoner for Microsoft Dynamics 365 for Finance and Operations.
author: mikefalkner
manager: aolson
ms.date: 08/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e828cb292ad48bb4690117b41589b25edcdf28bc
ms.contentlocale: nb-no
ms.lasthandoff: 08/31/2018

---

# <a name="customer-transaction-list-page"></a>Listeside for kundetransaksjoner

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Vis utligninger

Kategorien **Vis utligninger** i handlingsruten gir rask tilgang til utligningshistorikken og mer informasjon om hele utligningstransaksjonen. Du kan også vise flere transaksjoner som er knyttet til den valgte transaksjonen, fordi de var en del av samme utligningen, eller fordi de er betalinger som ble opprettet i samme betalingsjournalen.

1. Velg **Kunder \> Kunder**.
2. Velg en kunde som har transaksjoner, og velg deretter **Kunde \> Transaksjoner**.
3. Velg en transaksjonen du vil undersøke.
4. Velg kategorien **Vis utligninger** i handlingsruten.

    I dialogboksen **Vis utligninger** vises den valgte transaksjonen og alle dokumenter som er utlignet mot den. Denne dialogboksen ligner på utligningsloggvisningen, men den inneholder alle relaterte dokumenter. 

5. Du kan utføre forskjellige oppgaver i denne dialogboksen. Velg ett eller flere bilag, og velg deretter én av følgende menyer:

   - **Vis regnskap** – alle bilagene som er knyttet til de valgte dokumentene, vises. Velg **Lukk** for å lukke dialogboksen.
   - **Eksporter** – eksporter de valgte bilagene til Microsoft Excel.
   - **Vis relaterte betalinger** – alle journaltransaksjoner for betaling som ble opprettet i betalingsjournalen som er knyttet til det valgte dokumentet, vises. I tillegg vises alle utligninger som er knyttet til disse betalingene. Etiketten for denne menyen også endres til **Vis utligninger**. Velg **Vis utligninger** for å vise bare transaksjonene som ble vist da du åpnet dialogboksen **Vis utligninger** for første gang.
    - **Utlign transaksjoner** – denne menyen vises hvis det opprinnelige dokumentet som ble valgt, ikke ble helt utlignet. Når du velger dette, vises dialogboksen **Utlign transaksjoner**, der du kan velge transaksjoner for utligning.
    - **Angre utligninger** – denne menyen vises hvis det opprinnelige dokumentet som ble valgt, ble helt utlignet. Når du velger dette, vises dialogboksen **Angre utligninger**, der du kan angre utligningene som er utført for dette dokumentet.
    

