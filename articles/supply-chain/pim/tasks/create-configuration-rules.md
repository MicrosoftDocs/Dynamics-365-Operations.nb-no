---
title: Opprette konfigurasjonsregler
description: Denne prosedyren oppretter konfigurasjonsregler som kan brukes til dimensjonsbasert konfigurasjon for å fremtvinge eller nekte bestemte kombinasjoner av stykklistelinjer.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a315ddecd2e10f508b86ac8ea18a36df71616963
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568472"
---
# <a name="create-configuration-rules"></a>Opprette konfigurasjonsregler

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren oppretter konfigurasjonsregler som kan brukes til dimensjonsbasert konfigurasjon for å fremtvinge eller nekte bestemte kombinasjoner av stykklistelinjer. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den sjuende fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon.

1. Gå til Behandling av produktinformasjon > Stykklister og formler > Stykklister.
2. Finn og velg ønsket post i listen.
    * Søk etter og velg stykklisten for den dimensjonsbaserte konfigurasjonen.  
3. Klikk Alternativer i handlingsruten.
4. Klikk Bytt visning.
5. Klikk Hodevisning.
    * Åpne hodevisningen for å få tilgang til hurtigkategorien Konfigurasjonsrute.  
6. Vis eller skjul delen Konfigurasjonsrute.
    * Hurtigkategorien Konfigurasjonsrute må være i utvidet modus.  
7. Klikk Konfigurasjonsregler.
8. Klikk Ny.
9. Merk den valgte raden i listen.
10. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
    * Varene i den gjeldende konfigurasjonsgruppen vises. Velg den som representerer betingelsen i regelen.  
11. Klikk koblingen i den valgte raden i listen.
12. Velg et alternativ i Metode-feltet.
    * Det er mulig å fremtvinge et valg eller en opphevelse av valg av en vare fra en annen konfigurasjonsgruppe.  
13. Klikk rullegardinknappen i feltet Avledet gruppe for å åpne oppslaget.
14. Finn og velg ønsket post i listen.
15. Klikk koblingen i den valgte raden i listen.
    * Velg ønsket konfigurasjonsgruppe.  
16. Klikk rullegardinknappen i feltet Avledet varenummer for å åpne oppslaget.
17. Klikk koblingen i den valgte raden i listen.
    * Velg varenummeret som enten skal velges eller oppheves avhengig av den valgte metoden.  
18. Lukk siden.

