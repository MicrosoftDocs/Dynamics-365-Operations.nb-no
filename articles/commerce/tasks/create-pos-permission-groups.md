---
title: " Opprette tillatelsesgrupper for salgssted"
description: Denne artikkelen forklarer hvordan du oppretter en salgsstedstillatelsesgruppe.
author: josaw1
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailPosPermissionGroup, HcmJob
ms.openlocfilehash: 0aa394e5dc6685954c31cdddae7cdc042b80af29
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277967"
---
# <a name="create-pos-permission-groups"></a> Opprette tillatelsesgrupper for salgssted

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du oppretter en salgsstedstillatelsesgruppe. Demonstrasjonsdatafirmaet USRT brukes til å opprette denne oppgaven. Denne oppgaven er ment for rollen Driftsleder for handel.

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
