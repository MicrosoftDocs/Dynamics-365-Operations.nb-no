---
title: Konfigurer stillinger
description: Dette emnet beskriver hvordan stillinger er et viktig element i det nederste nivået i et organisasjonshierarki.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9121df9571b037478fb901cb6ac9f3298177548a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694802"
---
# <a name="set-up-positions"></a>Konfigurer stillinger


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Stillinger er et viktig element i det nederste nivået i et organisasjonshierarki. En stilling er én enkeltforekomst av en jobb. Stillingen "Salgssjef (øst)" er for eksempel én av stillingene som er knyttet til jobben "Salgssjef". Det finnes en stilling i en avdeling, og bare én arbeider kan tilordnes den. I denne oppgaven vil vi veilede deg gjennom fremgangsmåten som kreves for å opprette en stilling. Denne fremgangsmåten er ment for en personalespesialister.

1. Velg **Administrasjon av arbeidsstyrke**.
2. Velg **Åpne stillinger**.
3. Velg **Ny** for å åpne dialogboksen med rullegardinliste.
4. Angi eller velg en verdi i **Jobb**-feltet.

    Feltene **Jobbeskrivelsen**, **Tittel** og **Omregningsfaktor for fulltidsekvivalent** kopieres automatisk fra den valgte jobben til stillingen.

5. Velg **Opprett stilling**.
6. Angi eller velg en verdi i feltet **Avdeling**.
7. Angi eller velg en verdi i feltet **Stillingstype**.
8. Angi eller velg en verdi i feltet **Kompensasjonsområde**.

    Feltet **Kompensasjonsområde** bestemmer rettighetsreglene for kompensasjonen og budsjetter med fast økning som gjelder for en ansatt i denne stillingen.

9. Angi en dato og et klokkeslett i feltet **Tilgjengelig for tilordning**.
10. Vis delen **Stillingsvarighet**.

    Stillingsvarigheten angis som standard basert på datoene for aktivering og avgang ved pensjon, som ble angitt tidligere.

11. Utvid delen **Rapporterer til stilling**.

    Når du tilordner en arbeider til en stilling som rapporterer til en annen stilling, oppretter du en direkterapporteringsrelasjon mellom arbeidere som er tilordnet de to stillingene.

12. Velg **Ny** for å åpne dialogboksen med rullegardinliste.
13. Angi eller velg en verdi i feltet **Rapporter til**.
14. Velg **Opprett**.
15. Vis delen **Arbeidertilordning**.
16. Vis delen **Relasjoner**.

    Hvis organisasjonen bruker et matrisehierarki eller et annet egendefinert hierarki, kan du konfigurere stillingshierarkityper og deretter legge til rapporteringsrelasjoner i stillinger for hver hierarkitype som du definerer.

17. Velg **Legg til**.
18. Merk den valgte raden i listen.
19. Angi eller velg en verdi i feltet **Navn på hierarki**.
20. Angi eller velg en verdi i feltet **Rapporterer til stilling**.
21. Vis delen **Lønn**.
22. Angi eller velg en verdi i feltet **Lønnssyklus**.
23. Angi eller velg en verdi i feltet **Betalt av**.
24. Angi et tall i feltet **Årlige vanlige timer**.

    Verdien du angir, er antallet regelmessig betalte timer som arbeideren i denne stillingen er forventet å arbeide hvert år.

25. Vis delen **Fagforening**.
26. Skjul delen **Fagforening**.
27. Vis delen **Finansdimensjoner**.
28. Angi eller velg en verdi i feltet **Distribusjonsmal**.
29. Angi eller velg en verdi i feltet **Avdeling**.
30. Velg **Lagre**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
