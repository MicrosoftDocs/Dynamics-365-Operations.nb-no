---
title: Bytte mellom leverandørutforminger
description: Dette emnet beskriver hvordan du bytter integreringen av leverandørdata mellom Finance and Operations-apper og Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 70904ee716aabd019210e92895a894810bde27fb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346526"
---
# <a name="switch-between-vendor-designs"></a>Bytte mellom leverandørutforminger

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Flyt for leverandørdata 

Hvis du velger å bruke **Konto**-tabellen til å lagre leverandører av **Organisasjon**-typen og **Kontakt**-tabellen til å lagre leverandører av **Person**-typen, konfigurerer du følgende arbeidsflyter. Hvis ikke kreves ikke denne konfigurasjonen.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Bruke den utvidede leverandørutformingen for leverandører av typen Organisasjon

**Dynamics365FinanceExtended**-løsningspakken inneholder følgende arbeidsflytprosess-maler: Du vil opprette en arbeidsflyt for hver mal.

+ Opprette leverandører i tabellen Kontoer
+ Opprette leverandører i tabellen Leverandører
+ Oppdatere leverandører i tabellen Kontoer
+ Oppdatere leverandører i tabellen Leverandører

Slik oppretter du nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:

1. Opprett en ny arbeidsflytprosess for **Leverandør**-tabellen, og velg arbeidsflytprosess-malen **Opprette leverandører i tabellen Kontoer**. Velg deretter **OK**. Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Konto**-tabellen.

    ![Arbeidsflytprosessen Opprette leverandører i tabellen Kontoer.](media/create_process.png)

2. Opprett en ny arbeidsflytprosess for **Leverandør**-tabellen, og velg arbeidsflytprosess-malen **Oppdatere leverandører i tabellen Kontoer**. Velg deretter **OK**. Denne arbeidsflyten håndterer oppdateringsscenarioet for **Konto**-tabellen.
3. Opprett en ny arbeidsflytprosess for **Konto**-tabellen, og velg arbeidsflytprosess-malen **Opprette leverandører i tabellen Leverandører**.
4. Opprett en ny arbeidsflytprosess for **Konto**-tabellen, og velg arbeidsflytprosess-malen **Oppdatere leverandører i tabellen Leverandører**.
5. Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov. Velg **Konverter til en bakgrunnsarbeidsflyt** for å konfigurere en arbeidsflyt som en bakgrunnsarbeidsflyt.

    ![Knappen Konverter til en bakgrunnsarbeidsflyt.](media/background_workflow.png)

6. Aktiver arbeidsflytene du opprettet for tabellene **Konto** og **Leverandør**, for å begynne å bruke **Konto**-tabellen til å lagre informasjon for leverandører av **Organisasjon**-typen.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Bruke den utvidede leverandørutformingen for leverandører av typen Person

**Dynamics365FinanceExtended**-løsningspakken inneholder følgende arbeidsflytprosess-maler: Du vil opprette en arbeidsflyt for hver mal.

+ Opprette leverandører av typen Person i tabellen Leverandører
+ Opprette leverandører av typen Person i tabellen Kontakter
+ Oppdatere leverandører av typen Person i tabellen Kontakter
+ Oppdatere leverandører av typen Person i tabellen Leverandører

Slik oppretter du nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:

1. Opprett en ny arbeidsflytprosess for **Leverandør**-tabellen, og velg arbeidsflytprosess-malen **Opprette leverandører av typen Person i tabellen Kontakter**. Velg deretter **OK**. Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Kontakt**-tabellen.
2. Opprett en ny arbeidsflytprosess for **Leverandør**-tabellen, og velg arbeidsflytprosess-malen **Oppdatere leverandører av typen Person i tabellen Kontakter**. Velg deretter **OK**. Denne arbeidsflyten håndterer oppdateringsscenarioet for **Kontakt**-tabellen.
3. Opprett en ny arbeidsflytprosess for **Kontakt**-tabellen, og velg arbeidsflytprosess-malen **Opprette leverandører av typen Person i tabellen Leverandører**.
4. Opprett en ny arbeidsflytprosess for **Kontakt**-tabellen, og velg arbeidsflytprosess-malen **Oppdatere leverandører av typen Person i tabellen Leverandører**.
5. Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov. Velg **Konverter til en bakgrunnsarbeidsflyt** for å konfigurere en arbeidsflyt som en bakgrunnsarbeidsflyt.
6. Aktiver arbeidsflytene du opprettet for tabellene **Kontakt** og **Leverandør**, for å begynne å bruke **Kontakt**-tabellen til å lagre informasjon for leverandører av **Person**-typen.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]