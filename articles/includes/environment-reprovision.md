---
ms.openlocfilehash: f6bf4b6c946ebc63d3d84140f762cd4b789deb03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459622"
---
Når du kopierer en database mellom miljøer, må du kjøre verktøyet for ny klargjøring av miljøet før den kopierte databasen kan tas i bruk, slik at alle Commerce-komponenter er oppdatert.

> [!IMPORTANT]
> Vi anbefaler at du kjører denne prosedyren enten du bruker Commerce-komponenter eller ikke, fordi Commerce-funksjonalitet er inkludert i alle miljøer. 

Før du fortsetter, må du kontrollere at følgende forutsetninger er oppfylt:
1. Hvis du oppgraderer til juli 2017-utgivelsen 7.2.11792.56024 (også kalt 7.2), bruker du følgende X++-hurtigreparasjoner til programmet i målmiljøet før du kjører dataoppgraderingen i dette miljøet. Dette forhindrer at ulike feil oppstår under dataoppgraderingen:

    - KB 4036156 – Mindre versjonsoppgradering for Retail – Variantnummerserie er ikke angitt. Denne reparasjonspakken inneholder også KB 4035399 og KB 4035751. Vær oppmerksom på at du må ha minimum Platform Update 9 for å bruke denne pakken. Hvis du er usikker, installerer du de nyeste binærfilene.
    
2. Hvis du oppgraderer fra Microsoft Dynamics AX 2012, installerer du følgende X++-reparasjoner til programmet i målmiljøet før du kjører dataoppgraderingen:
    - KB 4033183 – Dynamics AX 2012 R2- eller Dynamics AX 2012 R3 Pre-CU8-oppgraderingen for ikke-detaljhandel mislykkes med feilen Finner ikke objekt for dbo.RETAILTILLLAYOUTZONE.
    - KB 4040692 – Oppgraderingen fra Dynamics AX 2012 R3 til Microsoft Dynamics 365 for Operations 7.2 mislykkes på grunn av duplisert indeks for RetailSalesLine på SalesLineIdx.
    - KB 4035490 – Ytelsesproblem med oppgraderingsskriptet til feltet GeneralJournalAccountEntry MainAccount.


Følg denne fremgangsmåten for å kjøre verktøyet for ny klargjøring av miljøet.

1. Velg **Distribuerbar programvarepakke** i Delt aktivabibliotek.
2. Last ned verktøyet for ny klargjøring av miljøet.
3. Velg **Distribuerbar programvarepakke** i aktivabiblioteket for prosjektet.
4. Velg **Ny** for å opprette en ny pakke.
5. Angi et navn og en beskrivelse for pakken. Du kan bruke **Verktøy for ny klargjøring av miljø** som pakkenavn.
6. Last opp pakken som du lastet ned tidligere.
7. Velg **Vedlikehold** > **Bruk oppdateringer** på siden **Miljødetaljer** for målmiljøet.
8. Velg verktøyet for ny klargjøring av miljø som du lastet opp tidligere, og velg deretter **Bruk** for å bruke pakken.
9. Overvåk fremdriften for pakkedistribusjonen. 

Hvis du vil ha mer informasjon om hvordan du bruker en distribuerbar pakke, kan du se [Bruke en distribuerbar pakke](../deployment/create-apply-deployable-package.md). Hvis du vil ha mer informasjon om hvordan du bruker en distribuerbar pakke manuelt, kan du se [Installere en distribuerbar pakke](../deployment/install-deployable-package.md).
