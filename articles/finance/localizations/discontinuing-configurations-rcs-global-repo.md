---
title: Avslutt konfigurasjoner i det globale RCS-repositoriet
description: Denne artikkelen beskriver hvordan du avslutter konfigurasjoner i det globale RCS-repositoriet.
author: gionoder
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: b0605f56058e3c93ea088ee8386ba26c4ce2b65a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272344"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Avslutt konfigurasjoner i det globale RCS-repositoriet

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du avslutter konfigurasjon i det globale RCS-repositoriet. Tidligere var det bare mulig å slette konfigurasjoner som ikke lenger var nødvendige. Men nå kan du merke en frigitt konfigurasjon som **Avsluttet** i det globale RCS-repositoriet. Med denne funksjonaliteten kan du også gjøre følgende: 
 
 - Varsle på forhånd når en konfigurasjon skal avsluttes.
 - Inkluder aktuelle detaljer om erstatningskonfigurasjonen.
 - Angi en dato for **Støttes til** for den spesifikke konfigurasjonen for å informere brukeren når den skal avsluttes.

Når du avslutter en konfigurasjonsversjon, kan du angi følgende valgfri informasjon:

  - **Erstatningskonfigurasjon**
  - **Versjon av erstatningskonfigurasjon**
  - **Fritekstnotat**: Bruk dette feltet til å angi dokumentasjonskoblinger eller -referanser
  - **Støttes til**: Dette feltet inneholder den foreslåtte datoen som gjeldende konfigurasjon/versjon vil bli støttet frem til. Denne datoen må oppdateres manuelt.
  
Fullfør trinnene nedenfor for å avslutte konfigurasjonen. 

1. Velg om du vil avslutte én versjon eller alle versjoner med samme innstillinger i én operasjon, ved å sette **Alle versjoner** til **Ja**. 
2. Sett parameteren **Avslutt** til **Ja**.
3. Velg **OK** for å avslutte konfigurasjonene. Feltet **Utgått dato** fylles ut når du lagrer endringene.

![Avslutte konfigurasjonsinformasjon.](media/Discontinue-details-2.png)
  
Du kan tilbakestille konfigurasjonen til **Delt** eller justere avsluttingsinformasjon når som helst. Hvis du deler en konfigurasjon, angir du datoen for **Støttet til** og all annen informasjon relatert til avsluttingen, for å angi planene for fremtidig avslutting.

Hvis du vil dele informasjon om en planlagt avslutting før konfigurasjonen faktisk avsluttes, kan brukeren forhåndsfylle alle felt som er knyttet til erstatning, men la parameteren **Avslutte** være satt til **Nei**.

> [!NOTE]
> Avslutting begrenser ikke operasjoner med konfigurasjoner. Du kan fortsette å importere, kjøre eller avlede konfigurasjonene, og disse feltene er veiledende.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finans støtter visning av denne informasjonen fra versjon 10.0.14

Fra og med versjon 10.0.14 støtter Dynamics 365 Finance visning av avsluttingsinformasjon. På siden **Globalt repositorium** kan du vise oppdatert informasjon om avslutting. Som standard blir konfigurasjoner som avsluttes, filtrert bort.
  
Siden **Importerte konfigurasjoner** (ERSolutionTable) viser konfigurasjoner som allerede ble avsluttet da de ble importert. For de konfigurasjonene som ble avsluttet etter import, kan avsluttingsinformasjonen synkroniseres ved å kjøre jobben **Importere konfigurasjonsoppdateringer**.


