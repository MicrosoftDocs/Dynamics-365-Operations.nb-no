---
title: Oversikt over plantype
description: En plantype i Microsoft Dynamics 365 Human Resources er en gruppering på høyt nivå av bestemte typer fordeler.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87be947c829641ba809e6850ccf41ea6d142161d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228968"
---
# <a name="plan-type-overview"></a>Oversikt over plantype


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/preview-banner.md)]

En plantype er en gruppering på høyt nivå av bestemte typer fordeler. Hver plantype har en plantypekode som bestemmer regler for plantypen. Plantypen **Enkelt liv** ville for eksempel ha plantypekoden **Liv** fordi den er en type livsforsikringsplan og må følge reglene som er angitt for plantypekoden **Liv**. En annen plantype kan være **Ekstra liv**. Denne plantypen vil også ha plantypkoden **Liv**.

Hver plantype angir om en ansatt kan registrere seg i én plan av typen eller flere. En ansatt kan for eksempel sannsynligvis registrere seg både for polisene **Enkelt liv** og **Ekstra liv** av plantypen Liv. En ansatt kan sannsynligvis registrere seg for bare én polise av typen Medisinsk.

Hvis en plantype omfatter kontakter, angir plantypen om kontakter er mottakere eller avhengige. En **Enkelt liv**-plantype vil for eksempel ha mottakere, mens en Enkel medisin-plantype vil ha avhengige. I noen tilfeller kan det hende at en plan ikke har noen personlige kontakter. For eksempel en fleksibel forbrukskonto eller et parkeringsfradrag.


En plantype kan definere dekningsalternativer. Dekningsalternativene er definert på siden **Dekningsalternativer**. Et dekningsalternativ kan angi fordelsbeløpet eller hvilke kontakter som er berettiget til plantypen. Hvis kontakttypen for eksempel er **Mottaker**, bør dekningsalternativet definere vilkårene for hva mottakeren kan motta når fordelen utnyttes. Hvis kontakt typen er **Avhengig**, bør dekningsalternativet definere forholdet mellom den avhengige og den ansatte. 

> [!IMPORTANT]
> Siden **Plantyper** inneholder nøkkeldata som påvirker alternativene som er tilgjengelige når en ny fordelsplan opprettes:
>
> - **Plantypekode** – Dette feltet påvirker hva som vises i kategorien **Konfigurasjon** når den faktiske fordelen er definert.  
> - **Samtidig registrering** – Dette feltet avgjør om flere registreringer er tillatt. (For en medisinsk plan er dette feltet vanligvis satt til **Én registrering**.)
> - **Kontakttype** – Dette feltet gjør det mulig å legge til avhengige eller mottakere i en plan. Hvis den er satt til **Ingen**, har ikke ansatte som har registrert seg i fordeler, muligheten til å velge enten en mottaker eller en avhengig.
> - **Dekningsalternativer** – Bruk dette feltet til å koble dekningsalternativene til plantypene. Den definerer enten personene som skal dekkes av denne plantypen, eller dekningsbeløpene som er tilgjengelige for denne plantypen. Du kan for eksempel angi at dekningen for en medisinsk plantype bare skal være tilgjengelig for den ansatte, den ansatte og en annen person, eller den ansatte og deres familie.

## <a name="create-plan-types"></a>Opprette plantyper

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Plantyper**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Plantype** | Et unikt navn som identifiserer plantypen. |
   | **Beskrivelse** | En beskrivelse av plantypen. |
   | **Kode for plantype** | Velg en plantypekode fra rullegardinlisten. Listen over plantypekoder viser alle plantypene som støttes i gjeldende versjon. |
   | **Samtidig registrering** | Angir om en ansatt kan registrere seg i flere fordelsplaner av samme plantype eller bare én fordelsplan per plantype. |
   | **Kontakttype** | Spesifiserer rollen til den personlige kontakten. Verdiene er tom, Avhengig og Mottaker. Du kan la **Kontakttype** stå tomt hvis plantypen ikke krever en avhengig eller mottaker basert på dekningsalternativet. |

4. Hvis du vil konfigurere alternativer for livshendelser, velger du **Handlinger** og deretter **Alternativer for livshendelser**. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Plantype** | Plantypen som det skal konfigureres alternativer for livshendelser for. |
   | **ID for levetidshendelsestype** | ID-en til livshendelsestypen. |
   | **Endre dekningsalternativ** | Angir om en ansatt kan endre dekningsalternativer i løpet av livshendelsen. |
   | **Bytt til en ny plan** | Angir om en ansatt kan endre planer i løpet av livshendelsen. |
   | **Åpne rettighetskontroll på nytt automatisk** | Angir om rettighetskontrollen for fordelsregistrering skal åpnes på nytt automatisk under levetidshendelsen. |
   | **Levetidshendelsesregistreringsperiode** | Angir rapporteringsvinduet (i dager) for levetidshendelsen. **Obs**! Hvis du ikke angir et beløp, antar systemet at rapporteringsvinduet er null, og livshendelsen behandles ikke. |
   | **Bare redigerbar av administrator** | Angir om administratorer kan avbryte eller redigere en plan i løpet av en levetidshendelse. Den ansatte kan ikke foreta noen endringer i arbeidsområdet **Ansattselvbetjening**. |
   | **Avbryt plan automatisk** | Angir om planen skal avbrytes automatisk i løpet av en livshendelse. Når endringene for levetidshendelsen er behandlet, beholdes alternativet **Automatisk annullering av plan** med det valgte planalternativet. Bare statusen **Bekreftet** eller **Utsjekket** blir fjernet. Planen forblir valgt. Ansatte som ikke foretar planleggingsvalg i løpet av registreringsperioden for livshendelsen, vil derfor ikke miste planvalget. 

5. Velg **Lagre**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
