---
title: Bytte mellom leverandørutforminger
description: Dette emnet beskriver hvordan du bytter integreringen av leverandørdata mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173045"
---
# <a name="switch-between-vendor-designs"></a>Bytte mellom leverandørutforminger

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Flyt for leverandørdata 

Hvis du velger å bruke **Konto**-enheten til å lagre leverandører av **Organisasjon**-typen og **Kontakt**-enheten til å lagre leverandører av **Person**-typen, konfigurerer du følgende arbeidsflyter. Hvis ikke kreves ikke denne konfigurasjonen.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Bruke den utvidede leverandørutformingen for leverandører av typen Organisasjon

**Dynamics365FinanceExtended**-løsningspakken inneholder følgende arbeidsflytprosess-maler: Du vil opprette en arbeidsflyt for hver mal.

+ Opprette leverandører i kontoenhet
+ Opprette leverandører i leverandørenhet
+ Oppdatere leverandører i kontoenhet
+ Oppdatere leverandører i leverandørenhet

Slik oppretter du nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:

1. Opprett en ny arbeidsflytprosess for **Leverandør**-enheten, og velg arbeidsflytprosess-malen **Opprette leverandører i kontoenhet**. Velg deretter **OK**. Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Konto**-enheten.

    ![Arbeidsflytprosessen Opprette leverandører i kontoenhet](media/create_process.png)

2. Opprett en ny arbeidsflytprosess for **Leverandør**-enheten, og velg arbeidsflytprosess-malen **Oppdatere leverandører i kontoenhet**. Velg deretter **OK**. Denne arbeidsflyten håndterer oppdateringsscenarioet for **Konto**-enheten.
3. Opprett en ny arbeidsflytprosess for **Konto**-enheten, og velg arbeidsflytprosess-malen **Opprette leverandører i leverandørenhet**.
4. Opprett en ny arbeidsflytprosess for **Konto**-enheten, og velg arbeidsflytprosess-malen **Oppdatere leverandører i leverandørenhet**.
5. Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov. Velg **Konverter til en bakgrunnsarbeidsflyt** for å konfigurere en arbeidsflyt som en bakgrunnsarbeidsflyt.

    ![Knappen Konverter til en bakgrunnsarbeidsflyt](media/background_workflow.png)

6. Aktiver arbeidsflytene du opprettet for **konto**- og **leverandør**-enhetene for å begynne å bruke **Konto** -enheten til å lagre informasjon for leverandører av **Organisasjon**-typen.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Bruke den utvidede leverandørutformingen for leverandører av typen Person

**Dynamics365FinanceExtended**-løsningspakken inneholder følgende arbeidsflytprosess-maler: Du vil opprette en arbeidsflyt for hver mal.

+ Opprette leverandører av typen Person i leverandørenheten
+ Opprette leverandører av typen Person i kontaktenheten
+ Oppdatere leverandører av typen Person i kontaktenheten
+ Oppdatere leverandører av typen Person i leverandørenheten

Slik oppretter du nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:

1. Opprett en ny arbeidsflytprosess for **Leverandør**-enheten, og velg arbeidsflytprosess-malen **Opprette leverandører av typen Person i kontaktenheten**. Velg deretter **OK**. Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Kontakt**-enheten.
2. Opprett en ny arbeidsflytprosess for **Leverandør**-enheten, og velg arbeidsflytprosess-malen **Oppdatere leverandører av typen Person i kontaktenheten**. Velg deretter **OK**. Denne arbeidsflyten håndterer oppdateringsscenarioet for **Kontakt**-enheten.
3. Opprett en ny arbeidsflytprosess for **Kontakt**-enheten, og velg arbeidsflytprosess-malen **Opprette leverandører av typen Person i leverandørenhet**.
4. Opprett en ny arbeidsflytprosess for **Kontakt**-enheten, og velg arbeidsflytprosess-malen **Oppdatere leverandører av typen Person i leverandørenhet**.
5. Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov. Velg **Konverter til en bakgrunnsarbeidsflyt** for å konfigurere en arbeidsflyt som en bakgrunnsarbeidsflyt.
6. Aktiver arbeidsflytene du opprettet for **kontakt**- og **leverandør**-enhetene for å begynne å bruke **Kontakt** -enheten til å lagre informasjon for leverandører av **Person**-typen.
