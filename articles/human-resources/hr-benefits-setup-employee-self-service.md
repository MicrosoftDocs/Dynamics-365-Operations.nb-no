---
title: Konfigurere selvbetjening for ansatte
description: I Microsoft Dynamics 365 Human Resources kan du konfigurere fliser for navigasjon på øverste nivå i Ansattselvbetjening.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
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
ms.openlocfilehash: d7ddb1f1ea74a16265dac701151b2c25a4f9d4dc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687170"
---
# <a name="configure-employee-self-service"></a>Konfigurere selvbetjening for ansatte


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I Microsoft Dynamics 365 Human Resources kan du konfigurere fliser for navigasjon på øverste nivå i **Ansattselvbetjening**. Fordelsplanfliser dirigerer brukere til fordelsplaner de er berettiget for.

## <a name="set-up-a-benefit-plans-tile"></a>Definere en fordelsplanflis

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.

2. Velg kategorien **Oppsett av fordelsplanflis**, og velg deretter **Ny**.

3. Angi verdier for de følgende feltene.

   | Felt | Beskrivelse |
   | --- | --- |
   | **Kode for plantype** | Plantypen som vises når denne flisen er valgt i **Selvbetjeningsfordeler**. |
   | **Flis-ID** | Den unike ID-en for flisen. |
   | **Etikettekst for flis** | Teksten som vises for flisen i **Selvbetjeningsfordeler**. |
   | **Beskrivelse** | En beskrivelse av flisen. |
   | **Bilde for flisbakgrunn** | URL-adressen for bildet som skal brukes for flisen (valgfritt). |
   | **Spor åpen registrering** | Velg dette alternativet for å spore den åpne registreringsfremdriften for denne plantypen. Du kan for eksempel ha planer opprettet der **Plantype = Annet**. Disse planene kan være valgfrie planer som du ikke vil spore fremdriften for registrering for. Hvis du ikke velger denne plantypen, blir denne plantypen ignorert ved sporing av fremdrift for registrering eller fullføring av avregistrering i kategorien **Åpne registrering**. Denne innstillingen gjelder for plantypen som er valgt for alle perioder og juridiske enheter. |

4. Velg **Lagre**.

## <a name="set-up-a-flex-credit-plan-tile"></a>Definere en flis for fleksibel kredittplan

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.

2. Velg kategorien **Oppsett av flis for fleksibel kredittplan**, og velg deretter **Ny**.

3. Angi verdier for de følgende feltene.

   | Felt | Beskrivelse |
   | --- | --- |
   | **ID for fordelskreditt** | Planene for fleksibelt kredittprogram vises når denne flisen er valgt i **Selvbetjeningsfordeler**. |
   | **Flis-ID** | Den unike ID-en for flisen. |
   | **Etikettekst for flis** | Teksten som vises for flisen i **Selvbetjeningsfordeler**. |
   | **Beskrivelse** | En beskrivelse av flisen. |
   | **Bilde for flisbakgrunn** | URL-adressen for bildet som skal brukes for flisen (valgfritt). |
   | **Spor åpen registrering** | Velg dette alternativet for å spore den åpne registreringsfremdriften for denne plantypen. Du kan for eksempel ha planer opprettet der **Plantype = Annet**. Disse planene kan være valgfrie planer som du ikke vil spore fremdriften for registrering for. Hvis du ikke velger denne plantypen, blir denne plantypen ignorert ved sporing av fremdrift for registrering eller fullføring av avregistrering i kategorien **Åpne registrering**. Denne innstillingen gjelder for plantypen som er valgt for alle perioder og juridiske enheter. |

4. Velg **Lagre**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
