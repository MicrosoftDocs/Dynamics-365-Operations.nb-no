---
title: Opprette plantyper
description: En plantype i Microsoft Dynamics 365 Human Resources er en gruppering på høyt nivå av bestemte typer fordeler. Hver plantype har en plantypekode som bestemmer regler for plantypen.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 88a6d89bf98ea145bbb6a4eb8f4e052e5f4088e5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419917"
---
# <a name="create-plan-types"></a>Opprette plantyper

En plantype i Microsoft Dynamics 365 Human Resources er en gruppering på høyt nivå av bestemte typer fordeler. Hver plantype har en plantypekode som bestemmer regler for plantypen. Plantypen Enkelt liv ville for eksempel ha plantypekoden Liv fordi den er en type livsforsikringsplan og må følge reglene som er angitt for livsplantypekoden. En annen plantype kan være Ekstra liv, også med plantypekoden Liv.

Hver plantype angir om en ansatt kan registrere seg i én plan av typen eller flere. En ansatt kan for eksempel sannsynligvis registrere seg både for polisene Enkelt liv og Ekstra liv av plantypen Liv. En ansatt kan sannsynligvis registrere seg for bare én polise av typen Medisinsk.

Hvis en plantype omfatter kontakter, angir plantypen om kontakter er mottakere eller avhengige. En Enkelt liv-plantype vil for eksempel ha mottakere, mens en Enkel medisin-plantype vil ha avhengige. I noen tilfeller kan det hende at en plan ikke har noen personlige kontakter. For eksempel en fleksibel forbrukskonto eller et parkeringsfradrag.

En plantype kan definere dekningsalternativer. Dekningsalternativene er definert i skjemaet Dekningsalternativ. Et dekningsalternativ kan angi fordelsbeløpet eller hvilke kontakter som er berettiget til plantypen. Hvis kontakttypen for eksempel er Mottaker, bør dekningsalternativet definere vilkårene for hva mottakeren kan motta når fordelen utnyttes. Hvis kontakt typen er Avhengig, bør dekningsalternativet definere forholdet mellom den avhengige og den ansatte. 

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
   | **Tillat avbrudd** | Angir om en ansatt kan annullere en fordelsplan i løpet av livshendelsen. |
   | **Endre dekningsalternativ** | Angir om en ansatt kan endre dekningsalternativer i løpet av livshendelsen. |
   | **Bytt til en ny plan** | Angir om en ansatt kan endre planer i løpet av livshendelsen. |
   | **Avbryt plan automatisk** | Angir om planen skal avbrytes automatisk i løpet av livshendelsen. |
   | **Åpne rettighetskontroll på nytt automatisk** | Angir om rettighetskontrollen for fordelsregistrering skal åpnes på nytt automatisk under levetidshendelsen. |
   | **Rapporteringsvindu** | Angir rapporteringsvinduet (i dager) for levetidshendelsen. **Obs**! Hvis du ikke angir et beløp, antar systemet at rapporteringsvinduet er null, og livshendelsen behandles ikke. |

5. Velg **Lagre**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]