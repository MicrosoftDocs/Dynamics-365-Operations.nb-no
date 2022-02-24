---
title: Opprette tillatelsesgrupper for salgssted
description: Dette emnet forklarer hvordan du oppretter en salgsstedstillatelsesgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac03e1bfb7a2463b31feca0a4303c182a00ad259
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964826"
---
# <a name="create-pos-permission-groups"></a>Opprette tillatelsesgrupper for salgssted

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter en salgsstedstillatelsesgruppe. Demonstrasjonsdatafirmaet USRT brukes til å opprette denne oppgaven. Denne oppgaven er ment for rollen Driftsleder for handel.

1. I navigasjonsruten går du til **Moduler > Detaljhandel og handel > Ansatte > Tillatelsesgrupper**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **ID for salgsstedstillatelsesgruppe**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Velg **Ja** i feltet **Vis tidsklokkeoppføringer**. Nå kan du aktivere eller deaktivere ulike tillatelser for salgsstedstillatelsesgruppen. For enkelte tillatelser kan du angi en verdi som skal brukes til å vurdere om salgsstedsbrukeren kan utføre handlingen. Denne oppgaveveiledningen angir noen tillatelser som kan gis til en kasserer.  
6. Velg **Ja** i feltet **Tillat oppretting av ordre**.
7. Velg **Ja** i feltet **Tillat redigering av ordre**.
8. Velg **Ja** i feltet **Tillat oppretting av ordre**.
9. Velg **Ja** i feltet **Tillat passordendring**.
10. Velg **Ja** i feltet **Tillat usporet lukking**.
11. Velg **Lagre**. Når endringene er lagret, må du kjøre stabsdistribusjonsplanen for å overføre endringene til handelskanalene. 
12. I navigasjonsruten går du til **Moduler > Personale > Jobber > Jobber**.
13. Vi vil nå tilordne salgsstedstillatelsesgruppen til en jobb. Finn og velg ønsket post i listen.
14. Velg **Rediger**.
15. Vis delen **Jobbklassifisering**.
16. Angi eller velg en verdi i feltet Gruppe for salgsstedstillatelse. Alle arbeidere i stillinger for denne jobben bruker salgsstedstillatelsesgruppens innstillinger med mindre arbeidernes salgsstedstillatelser har blitt overstyrt på stillingsnivået.  
17. Velg **Lagre**. Når endringene er lagret, må du kjøre stabsdistribusjonsplanen for å overføre endringene til handelskanalene.  

