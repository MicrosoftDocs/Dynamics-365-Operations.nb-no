---
title: Kontrollere varekvaliteten
description: Denne prosedyren viser hvordan du behandler en kvalitetsordre.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "315435"
---
# <a name="inspect-the-quality-of-goods"></a>Kontrollere varekvaliteten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du behandler en kvalitetsordre. Du kan bruke denne veiledningen i USMF-demodatafirmaet. Før du starter denne eksempelprosedyren, må du bekrefte bestillingen "000016" og postere en produktkvittering. Dermed opprettes automatisk en kvalitetsordre. Kvalitetsinspeksjoner utføres vanligvis av en kvalitetsassistent.


## <a name="select-a-quality-order"></a>Velge en kvalitetsordre
1. Gå til Lagerstyring > Periodiske oppgaver > Kvalitetsstyring > Kvalitetsordrer.
2. Merk den valgte raden i listen.
    * Velg kvalitetsordren som ble opprettet før du startet denne prosedyren.  

## <a name="record-test-results"></a>Registere testresultater
1. Klikk Resultater.
2. Klikk Rediger.
3. Angi et tall i Resultatantall-feltet.
4. Merk den valgte raden i listen.
5. Klikk rullegardinknappen i Resultat-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
    * I dette eksemplet er resultatet basert på et forhåndsdefinert resultat. Vanligvis vil du registrere et mer spesifikt testresultat, for eksempel en størrelse eller annen dimensjon.  
7. Klikk koblingen i den valgte raden i listen.
8. Klikk Lagre.
9. Lukk siden.

## <a name="validate-the-quality-order"></a>Valider kvalitetsordren
1. Klikk Valider.
2. Klikk rullegardinknappen i feltet Valider av for å åpne oppslaget.
    * Velg brukeren som utfører inspeksjonen.  
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Velg.
5. Klikk OK.
6. Lukk siden.

