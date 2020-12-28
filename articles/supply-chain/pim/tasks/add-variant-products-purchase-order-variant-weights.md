---
title: Legge til variantprodukter i bestillinger ved hjelp av variantvekt
description: Denne prosedyren hjelper deg gjennom trinnene med å bruke variantvekter for å fylle ut bestillingslinjer automatisk for hver variant av et produkt.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27ff3784074a36d073930ba68c8dec8b1121356e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434812"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a>Legge til variantprodukter i bestillinger ved hjelp av variantvekt

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper deg gjennom trinnene med å bruke variantvekter for å fylle ut bestillingslinjer automatisk for hver variant av et produkt. Når du velger antallet for produktet du vil kjøpe, opprettes bestillingslinjer for alle variantene av produktet med foreslåtte antall basert på vekten som er konfigurert for produktvariantene. Denne prosedyren inkluderer ikke trinn for å konfigurere vektverdier for produktdimensjoner og produktvarianter. Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.

1. Gå til Leverandører > Bestillinger > Alle bestillinger.
2. Klikk Ny.
3. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
4. Klikk koblingen i den valgte raden i listen.
5. Aktiver/deaktiver utvidelsen av delen Generelt.
6. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
10. Klikk koblingen i den valgte raden i listen.
11. Klikk OK.
12. Aktiver/deaktiver utvidelsen av delen Linjedetaljer.
13. Klikk kategorien Varianter.
14. Klikk Legg til linje.
15. Merk den valgte raden i listen.
16. Skriv inn 0140 i Varenummer-feltet.
17. Sett verdien for Antall til 1000.
18. Klikk Lagre.

