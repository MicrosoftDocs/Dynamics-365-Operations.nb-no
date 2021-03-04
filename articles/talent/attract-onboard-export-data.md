---
title: Eksportere data fra Attract og Onboard
description: Eksportere data fra Dynamics 365 Talent – Attract og Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462059"
---
# <a name="export-data-from-attract-and-onboard"></a>Eksportere data fra Attract og Onboard

[!include [banner](includes/banner.md)]

Som annonsert i [Trekke tilbake Dynamics 365 Talent: Attract- og Dynamics 365 Talent: Onboard-apper](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), trekker vi tilbake Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard 1. februar 2022. For å hjelpe med migreringen til et annet produkt, tilbyr begge appene nå dataeksportmuligheter.

## <a name="export-data-from-attract"></a>Eksportere data fra Attract

Du kan eksportere dataene uten å begrense tilgangen til miljøet. Det kan være lurt å gjøre dette for testformål eller for å forstå datastrukturen vår. Når du er klar til å overføre, kan du begrense tilgangen til Attract-miljøet ditt ved hjelp av instruksjonene etter denne prosedyren. Sørg for at du eksporterer dataene dine igjen. 

1. Gå til [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Under **Dataeksport** velg **Be om en dataeksport**.

   ![[Be om en dataeksport fra Attract](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Når meldingsboksen **Forespørselen din er under behandling** vises, velger du **OK**. Dataeksporten kan ta opptil 20 minutter, avhengig av størrelsen på eksporten.

4. Når eksporten er fullført, velger du **Last ned**-knappen ved siden av den. 

   >[!NOTE]
   >Alle dataeksporter er tilgjengelige i sju dager, hvoretter **Last ned**-koblingen utløper.</br>
   
Nedlastingen inneholder en ZIP-fil med Attract-dataene dine, inkludert følgende mapper:

| Mappenavn | Beskrivelse |
| --- | --- |
| Administrasjonsinnstillinger | Konfigurasjoner for Attract-administrasjonssenteret. |
| Kandidater | Alle kandidater som er lagt til jobber eller talentsamlinger. |
| E-postmaler | Alle e-postmaler som er konfigurert for miljøet. |
| Jobbtilbudspakkemaler | Alle jobbtilbudspakkemalene som er opprettet, pluss de tilknyttede konfigurasjonene. |
| Regelsett for jobbtilbud |  Alle regelsettfiler som er lastet opp for tilbudsbehandling. |
| Jobbtilbudsmaler | Alle dokumentmaler for jobbtilbud som er opprettet for miljøet. |
| Ledige stillinger | Alle opprettede jobber. Slettede jobber eksporteres ikke. Undermappene inneholder kandidatsøknader, med undermapper for vedlegg til kandidatsøknader og tilbudspakker der det er aktuelt. |
| Maler for ledige stillinger | Jobbprosessmaler som er konfigurert i miljøet. |
| Talentsamlinger | Alle opprettede talentsamlinger, deres bidragsyterlister og kandidatlistene for talentsamlingene. |
| Arbeidere | Liste over alle arbeiderne som finnes i miljøet, pluss deres roller. |
| (rotmappe) | En JSON-skjemafil som beskriver datastrukturfeltene. |

### <a name="restrict-access-to-attract"></a>Begrense tilgang til Attract

Når du er klar til å overføre, kan du begrense tilgangen for ikke-administratorer til Attract-miljøet ditt og eksportere dataene.

>[!IMPORTANT]
>Begrensning av tilgang til Attract-miljøet ditt er permanent og kan ikke angres. Hvis du vil at ikke-administrative brukere skal kunne fortsette å få tilgang til miljøet ditt, hopper du over dette trinnet.

1. Gå til [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Hvis du vil begrense tilgangen for ikke-administratorer til Attract-miljøet ditt, velger du **Begrens tilgang nå** under **Begrens tilgang til denne appen**. Når du begrenser tilgangen, oppheves også posteringen av eventuelle aktive jobber som er postert.

   ![[Begrense tilgang for ikke-administratorer til Attract](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Når du ser advarselen **Dette er en permanent endring**, velger du **Begrens tilgang** for å begrense ikke-administrative brukere permanent fra dette miljøet. Hvis du ikke er klar til å fullføre dette trinnet, velger du **Avbryt**.

   ![[Advarsel om at begrensning av tilgang er en permanent endring](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Administratorer kan fortsatt få tilgang til dataeksport- og personrapportsider etter at du har begrenset tilgang til Attract-miljøet.

## <a name="export-data-from-onboard"></a>Eksportere data fra Onboard

Når du er klar, kan du laste ned maler, veiledninger og kandidatdata fra Onboard.

1. Gå til [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. Under **Dataeksport** velg **Be om en dataeksport**. 

   ![[Be om en dataeksport fra Onboard](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Når meldingsboksen **Forespørselen din er under behandling** vises, velger du **OK**. Dataeksporten kan ta opptil 20 minutter, avhengig av størrelsen på eksporten.

4. Når eksporten er fullført, velger du **Last ned**-knappen ved siden av den. 

   ![[Laste ned dataeksport fra Onboard](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Dataeksporten er tilgjengelig i sju dager. Etter sju dager utløper **Last ned**-koblingen, og du må be om en ny eksport hvis du må laste ned dataene på nytt. Når du starter en ny dataeksport, utløper eksisterende nedlastinger etter at den nye eksporten er fullført.

Nedlastingen er en ZIP-fil som inneholder:

- Mappen **Maler** som inneholder Onboard-malene i Word-dokumentformat.

- Mappen **Veiledninger** som inneholder Onboard-veiledningene i Word-dokumentformat.

## <a name="see-also"></a>Se også

[Trekke tilbake Dynamics 365 Talent: Attract- og Dynamics 365 Talent: Onboard-apper](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)

[!INCLUDE[footer-include](../includes/footer-banner.md)]