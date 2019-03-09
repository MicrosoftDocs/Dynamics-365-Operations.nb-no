---
title: Planlegge laster og leveringer ved hjelp av arbeidsområdet for lastplanlegging
description: Denne fremgangsmåten viser hvordan du bruker arbeidsområdet for lastplanlegging til å opprette en last for en salgsordre.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "343909"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Planlegge laster og leveringer ved hjelp av arbeidsområdet for lastplanlegging

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du bruker arbeidsområdet for lastplanlegging til å opprette en last for en salgsordre. Som en forutsetning skal vi først opprette salgsordren. Denne prosedyren er en del av det daglige arbeidet for transportkoordinator. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-sales-order"></a>Opprette en salgsordre
1. Gå til Kunder > Ordrer > Alle salgsordrer.
2. Klikk Ny.
3. Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.
4. Velg konto US-004.
5. Klikk OK.
6. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
7. Velg vare A0001.
    * A0001 er aktivert for transportstyring.  
8. Klikk koblingen i den valgte raden i listen.
9. Angi et tall i feltet Antall.
10. Skriv inn 24 i Lager-feltet.
    * I dette eksemplet velger du lager 24. Dette lageret er aktivert for transportstyring og avansert lagerstyring.  
11. Klikk Lagre.
12. Lukk siden.

## <a name="create-a-new-load"></a>Opprette en ny last
1. Gå til Transportstyring > Planlegging > Arbeidsområde for lastplanlegging.
2. Klikk kategorien Salgslinjer.
    * Nå vil du bygge belastningen for salgsordren som du nettopp opprettet. Belastninger kan bygges basert på tilbud og etterspørsel fra bestillinger, salgsordrer og overføringsordrer.  
3. Klikk Forsyning og behov i handlingsruten.
4. Klikk Til ny belastning.
5. Klikk rullegardinknappen i feltet Lastmal-ID for å åpne oppslaget.
    * Lastmalen angir maksimale mål for vekt og volum for hele belastningen. Lastmalen kan for eksempel representere størrelsen på en container eller lastebil.  
6. Klikk koblingen i den valgte raden i listen.
7. Klikk OK.

## <a name="rate-and-route-the-load"></a>Vurdere og rute lasten
1. Klikk Vurdering og ruting.
2. Klikk Arbeidsområde for vurderingsrute.
3. Klikk Vurder butikk.
4. Finn og velg ønsket post i listen.
5. Velg Tilordne.
6. Lukk siden.
7. Lukk siden.

