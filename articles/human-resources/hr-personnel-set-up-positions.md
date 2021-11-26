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
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4b9f09db8465cc55c9b0c4dc403c2c7a3647d7e
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728724"
---
# <a name="set-up-positions"></a>Konfigurer stillinger

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Stillinger er et viktig element i det nederste nivået i et organisasjonshierarki. En stilling er én enkeltforekomst av en jobb. Stillingen "Salgssjef (øst)" er for eksempel én av stillingene som er knyttet til jobben "Salgssjef". Det finnes en stilling i en avdeling, og bare én arbeider kan tilordnes den. I denne oppgaven vil vi veilede deg gjennom fremgangsmåten som kreves for å opprette en stilling. Denne fremgangsmåten er ment for en personalespesialister.

1. Velg **Administrasjon av arbeidsstyrke**.
2. Velg **Åpne stillinger**.
3. Velg **Ny** for å åpne dialogboksen med rullegardinliste.
4. Angi eller velg en verdi i **Jobb**-feltet.

    Feltene **Jobbeskrivelsen**, **Tittel** og **Omregningsfaktor for fulltidsekvivalent** kopieres automatisk fra den valgte jobben til stillingen.

5. ResolveChanges jobben.
6. Velg **Opprett stilling**.
7. Angi eller velg en verdi i feltet **Avdeling**.
8. Angi eller velg en verdi i feltet **Stillingstype**.
9. Angi eller velg en verdi i feltet **Kompensasjonsområde**.

    Feltet **Kompensasjonsområde** bestemmer rettighetsreglene for kompensasjonen og budsjetter med fast økning som gjelder for en ansatt i denne stillingen.

10. Angi en dato og et klokkeslett i feltet **Tilgjengelig for tilordning**.
11. Vis delen **Stillingsvarighet**.

    Stillingsvarigheten angis som standard basert på datoene for aktivering og avgang ved pensjon, som ble angitt tidligere.

12. Utvid delen **Rapporterer til stilling**.

    Når du tilordner en arbeider til en stilling som rapporterer til en annen stilling, oppretter du en direkterapporteringsrelasjon mellom arbeidere som er tilordnet de to stillingene.

13. Velg **Ny** for å åpne dialogboksen med rullegardinliste.
14. Angi eller velg en verdi i feltet **Rapporter til**.
15. Velg **Opprett**.
16. Vis delen **Arbeidertilordning**.
17. Vis delen **Relasjoner**.

    Hvis organisasjonen bruker et matrisehierarki eller et annet egendefinert hierarki, kan du konfigurere stillingshierarkityper og deretter legge til rapporteringsrelasjoner i stillinger for hver hierarkitype som du definerer.

18. Velg **Legg til**.
19. Merk den valgte raden i listen.
20. Angi eller velg en verdi i feltet **Navn på hierarki**.
21. Angi eller velg en verdi i feltet **Rapporterer til stilling**.
22. Vis delen **Lønn**.
23. Angi eller velg en verdi i feltet **Lønnssyklus**.
24. Angi eller velg en verdi i feltet **Betalt av**.
25. Angi et tall i feltet **Årlige vanlige timer**.

    Verdien du angir, er antallet regelmessig betalte timer som arbeideren i denne stillingen er forventet å arbeide hvert år.

26. Vis delen **Fagforening**.
27. Skjul delen **Fagforening**.
28. Vis delen **Finansdimensjoner**.
29. Angi eller velg en verdi i feltet **Distribusjonsmal**.
30. Angi eller velg en verdi i feltet **Avdeling**.
31. Velg **Lagre**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
