---
title: Planlegge laster og leveringer ved hjelp av arbeidsområdet for lastplanlegging
description: Dette emnet viser hvordan du bruker arbeidsområdet for lastplanlegging til å opprette en last for en salgsordre.
author: ShylaThompson
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ef95dfc3dba8ef162d0be145a52b7153912cb77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828257"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Planlegge laster og leveringer ved hjelp av arbeidsområdet for lastplanlegging

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du bruker arbeidsområdet for lastplanlegging til å opprette en last for en salgsordre. Som en forutsetning skal vi først opprette salgsordren. Denne prosedyren er en del av det daglige arbeidet for transportkoordinator. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-sales-order"></a>Opprette en salgsordre
1. Gå til **Navigasjonsrute > Moduler > Kunder > Ordrer > Alle salgsordrer**.
2. Velg **Ny**.
3. Klikk på rullegardinknappen i **Kundekonto**-feltet for å åpne oppslaget.
4. Velg konto **US-004**.
5. Velg **OK**.
6. Klikk på rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.
7. Velg vare **A0001**. **A0001** er aktivert for transportstyring.  
8. Klikk på rullegardinknappen i feltet **Område** for å velge et element.
9. Angi et tall i **Antall**-feltet.
10. I **Lager**-feltet skriver du inn 24 for dette eksemplet. Dette lageret er aktivert for transportstyring og avansert lagerstyring.  
11. Velg **Lagre**.
12. Lukk siden.

## <a name="create-a-new-load"></a>Opprette en ny last
1. Gå til **Navigasjonsrute > Moduler > Transportatstyring > Planlegging > Arbeidsområde for lastplanlegging**.
2. Velg fanen **Salgslinjer**. Nå vil du bygge belastningen for salgsordren som du nettopp opprettet. Belastninger kan bygges basert på tilbud og etterspørsel fra bestillinger, salgsordrer og overføringsordrer.  
3. Velg **Forsyning og behov** i handlingsruten.
4. Velg **Til ny belastning**.
5. Klikk på rullegardinknappen i feltet **Lastmal-ID** for å åpne oppslaget. Lastmalen angir maksimale mål for vekt og volum for hele belastningen. Lastmalen kan for eksempel representere størrelsen på en container eller lastebil. Velg en vare.
6. Velg **OK**.

## <a name="rate-and-route-the-load"></a>Vurdere og rute lasten
1. Velg **Vurdering og ruting**.
2. Velg **Arbeidsområde for vurderingsrute**.
3. Velg **Vurder butikk**.
4. Finn og velg ønsket post i listen.
5. Velg **Tilordne**.
6. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]