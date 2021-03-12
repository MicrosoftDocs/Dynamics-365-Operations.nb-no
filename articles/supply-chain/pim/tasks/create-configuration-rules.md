---
title: Opprette konfigurasjonsregler
description: Denne prosedyren oppretter konfigurasjonsregler som kan brukes til dimensjonsbasert konfigurasjon for å fremtvinge eller nekte bestemte kombinasjoner av stykklistelinjer.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d75e9ecaa814085e8fce1836125553511cf4f48b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999737"
---
# <a name="create-configuration-rules"></a>Opprette konfigurasjonsregler

[!include [banner](../../includes/banner.md)]

Denne prosedyren oppretter konfigurasjonsregler som kan brukes til dimensjonsbasert konfigurasjon for å fremtvinge eller nekte bestemte kombinasjoner av stykklistelinjer. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den sjuende fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon.

1. Gå til Behandling av produktinformasjon > Stykklister og formler > Stykklister.
2. Finn og velg ønsket post i listen.
    * Søk etter og velg stykklisten for den dimensjonsbaserte konfigurasjonen.  
3. Klikk på Alternativer i handlingsruten.
4. Klikk på Bytt visning.
5. Klikk på Hodevisning.
    * Åpne hodevisningen for å få tilgang til hurtigfanen Konfigurasjonsrute.  
6. Vis eller skjul delen Konfigurasjonsrute.
    * Hurtigfanen Konfigurasjonsrute må være i utvidet modus.  
7. Klikk på Konfigurasjonsregler.
8. Klikk på Ny.
9. Merk den valgte raden i listen.
10. Klikk på rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
    * Varene i den gjeldende konfigurasjonsgruppen vises. Velg den som representerer betingelsen i regelen.  
11. Klikk på koblingen i den valgte raden i listen.
12. Velg et alternativ i Metode-feltet.
    * Det er mulig å fremtvinge et valg eller en opphevelse av valg av en vare fra en annen konfigurasjonsgruppe.  
13. Klikk på rullegardinknappen i feltet Avledet gruppe for å åpne oppslaget.
14. Finn og velg ønsket post i listen.
15. Klikk på koblingen i den valgte raden i listen.
    * Velg ønsket konfigurasjonsgruppe.  
16. Klikk på rullegardinknappen i feltet Avledet varenummer for å åpne oppslaget.
17. Klikk på koblingen i den valgte raden i listen.
    * Velg varenummeret som enten skal velges eller oppheves avhengig av den valgte metoden.  
18. Lukk siden.

