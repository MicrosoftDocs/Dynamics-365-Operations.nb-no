---
title: " Opprette produktpakker for bestillinger"
description: Denne prosedyren hjelper med å opprette en produktpakke og bruke den i en bestilling.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b0084c6b4acbf14e3afec552575d5be26114237
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414692"
---
# <a name="create-product-packages-for-purchase-orders"></a> Opprette produktpakker for bestillinger

[!include [banner](../includes/banner.md)]

Denne prosedyren hjelper med å opprette en produktpakke og bruke den i en bestilling. Bestillingen skal brukes til å opprette en ordre for et forhåndsdefinert sett med produkter. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.


## <a name="create-a-product-package"></a>Opprette en produktpakke
1. Gå til Detaljhandel og handel > Lagerstyring > Etterfylling > Produktpakker.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Pakkenummer.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
6. Klikk koblingen i den valgte raden i listen.
7. Klikk Legg til.
8. Skriv inn 0160 i Varenummer-feltet.
9. Klikk rullegardinknappen i Størrelse-feltet for å åpne oppslaget.
10. Klikk koblingen i den valgte raden i listen.
11. Angi et tall i feltet Antall.
12. Klikk Legg til.
13. Skriv inn 0160 i Varenummer-feltet.
14. Klikk rullegardinknappen i feltet Variantnummer for å åpne oppslaget.
15. Klikk koblingen i den valgte raden i listen.
16. Angi et tall i feltet Antall.
17. Klikk Legg til.
18. Skriv inn 0175 i Varenummer-feltet.
19. Angi et tall i feltet Antall.
20. Klikk Lagre.
21. Lukk siden.

## <a name="add-package-to-purchase-order"></a>Legge til pakken i bestillingen
1. Gå til Leverandører > Bestillinger > Alle bestillinger.
2. Klikk Ny.
3. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
4. Velg den samme leverandøren som produktpakken ble opprettet for tidligere, i listen, hvis du valgte en leverandør.
5. Aktiver/deaktiver utvidelsen av delen Generelt.
6. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
9. Klikk koblingen i den valgte raden i listen.
10. Klikk OK.
11. Aktiver/deaktiver utvidelsen av delen Linjedetaljer.
12. Klikk kategorien Produktpakker.
13. Klikk Bestillingslinje.
14. Klikk Opprett linjer fra pakke.
15. Finn og velg produktpakken som ble opprettet i forrige trinn, i listen.
16. Angi et tall i Antall-feltet.
17. Klikk Opprett.
18. Klikk Lagre.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]