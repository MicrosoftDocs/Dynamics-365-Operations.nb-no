---
title: Kan ikke endre ikrafttredelsesdatoen for en godkjent leverandør
description: Listen over godkjente leverandører per produktenhet tillater ikke at ikrafttredelsesdatoen endres
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477156"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Kan ikke endre ikrafttredelsesdatoen for en godkjent leverandør


## <a name="symptoms"></a>Symptomer

Et produkt har en godkjent leverandør som for eksempel har gyldighetsdato 11. januar 2018 (*01/11/2018*) og utløpsdatoen *Aldri*. Hvis du prøver å endre ikrafttredelsesdatoen til 10. januar 2018 (*01/10/2018*) eller 12. januar 2018 (*01/12/2018*), får du følgende feilmelding:

> Kan ikke opprette en post i liste over godkjente leverandører (PdsApproveVendorList). Verdien for utløpsdato må være større enn eller lik verdien for gyldighetsdato.

## <a name="resolution"></a>Løsning

Du kan bare forlenge perioden leverandøren er godkjent for. Følgende regler gjelder:

- Hvis du vil endre ikrafttredelsesdatoen slik at den er tidligere enn noen av de eksisterende postene (perioder) for vareleverandøren, må utløpsdatoen for den nye perioden være før alle utløpsdatoene i de eksisterende postene.
- Hvis du vil endre utløpsdatoen slik at den er senere enn noen av de eksisterende periodene, må ikrafttredelsesdatoen være etter den seneste utløpsdatoen i alle eksisterende poster.
- Hvis du vil redusere den overordnede perioden som leverandøren er godkjent for, må du slette eller endre eksisterende poster. Du kan også bruke bryteren for **avkorting** under import. Denne bryteren sletter alle eksisterende poster i tabellen for godkjente leverandører etter vare.

For eksempel scenarioet som er beskrevet i problembeskrivelsen, der en post har en gyldighetsdato på *01/11/2018* og utløpsdatoen *Aldri*, kan du importere en ny post som har en gyldighetsdato på *01/10/2018* og utløpsdatoen *Aldri*. Du kan imidlertid ikke redusere perioden slik at ikrafttredelsesdatoen oppdateres til *01/12/2018* via databehandling. Du må gjøre denne endringen i brukergrensesnittet.
