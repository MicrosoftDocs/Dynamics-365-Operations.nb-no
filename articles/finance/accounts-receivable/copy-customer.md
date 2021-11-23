---
title: Kopiere kunder ved hjelp av delte nummerserier
description: Dette emnet forklarer hvordan du bruker delte nummerserier til å kopiere en kunde til en annen juridisk enhet og samtidig beholde samme kunde-ID.
author: abruer
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0a93f0519b292c12ea31a8faf3bff051fc111216
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753495"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Kopiere kunder ved hjelp av delte nummerserier

[!include [banner](../includes/banner.md)]

Du kan bruke delte nummerserier til å tilordne kunde-IDer. Delte nummerserier lar deg også kopiere kunder fra én juridisk enhet til en annen juridisk enhet, og bruke samme kunde-ID-er i begge juridiske enheter.

## <a name="setup"></a>Oppsett

Funksjonen er aktivert når du bruker en delt nummerserie til å tilordne kunde-ID-er. Du må bruke samme nummerserie i alle juridiske enheter som du vil kopiere en kunde til. Du kan endre kundenummerserien på siden **Kundeparametere** for hver juridiske enhet. Velg **Leverandører** \> **Parametere**, og velg deretter fanen **Nummerserier**.

Du kan også definere kundenummerserier for hver kundegruppe. Disse nummerseriene må også være delt. Nummerrekkefølgen for en kundegruppe brukes først. Hvis ingen nummerserie er angitt for en kundegruppe, brukes nummerserien som er angitt på siden **Kundeparametere**.

Du kan også kopiere kunder mellom juridiske enheter hvis du bruker manuelle kunde-ID-er. Hvis du imidlertid prøver å kopiere en kunde til en juridisk enhet der kunde-ID-en allerede finnes, starter ikke kopieringen.

## <a name="copy-a-customer"></a>Kopiere en kunde

Hvis du vil kopiere en kunde, velger du **Ny** på listesiden **Alle kunder** for å åpne dialogboksen **Opprett kunde**. Legg merke til at den nye kunde-ID-en ikke tilordnes umiddelbart. Denne virkemåten skiller seg fra virkemåten i tidligere versjoner. Systemet kan ikke fastslå riktig nummerserie å bruke fordi du ennå ikke har valgt kundegruppe. I tillegg kan det heller ikke fastslå om du prøver å opprette en ny kunde eller kopiere en kunde. Derfor tilordnes ikke kunde-ID-en før du velger **Lagre** nederst i dialogboksen.

Hvis du oppretter en ny kunde, kan du fortsette å fylle ut alle feltene på vanlig måte. Når du er ferdig og du velger **Lagre**, vil du se at kunde-ID-en ble tilordnet automatisk. For manuelle nummerserier ser du også at den manuelle kunde-ID-en ble brukt.

Hvis du vil kopiere en kunde, går du til feltet **Navn** og angir ett eller flere tegn som representerer kunden som du leter etter. En dialogboks for søk viser en liste over parter som kan representere kunden du leter etter. Når du velger en av partene, vises tilleggsinformasjon til høyre i dialogboksen:

- Fanen **Generelt** viser partens telefonnummer og adresse.
- Fanen **Roller** viser rollene som den valgte parten kan ha, og den juridiske enheten der den har hver rolle.
- Fanen **ID for mva-registrering** viser ID-er for mva-registrering som er tilordnet til parten.

Du kan kopiere en part bare hvis den har en kunderollen og hvis den har denne rollen i en juridisk enhet som ikke er gjeldende juridisk enhet. Følg denne fremgangsmåten når du finner en part som oppfyller disse kriteriene.

1. Alternativet **Kopier kunde** vises. Dette alternativet er satt til **Nei** som standard. Hvis du vil kopiere kunden til gjeldende juridisk enhet, setter du alternativet til **Ja**. 
2. Feltet **Juridisk enhet** vises. Velg den juridiske enheten du skal kopiere kunden fra. Hvis kunden finnes i bare én juridisk enhet, er feltet satt til den juridiske enheten som standard.
3. Velg **Velg**. Den nye kunden opprettes.

## <a name="validation"></a>Validering

Når du kopierer en kunde, prøver systemet å lagre den nye kundeinformasjonen. Valideringer kjøres for å bekrefte at dataene som ble kopiert er korrekte. Du får en feilmelding for hver validering som mislykkes. Feilmeldingene forklarer hvilken informasjon som må oppdateres. Kopien av kunden kan ikke lagres før du retter alle valideringsfeilene.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Kopiere en kunde ved hjelp av søkefunksjonen for mva-organisasjonsnummer

Du kan også kopiere kunder ved hjelp av søkefunksjonen for mva-organisasjonsnummer i **Registrering**-gruppen i fanen **Kunde** i handlingsruten på siden **Alle kunder**. Dialogboksen for **søk etter mva-organisasjonsnummer** som vises, viser mva-organisasjonsnumre, kunde-ID, kundenavn og den juridiske enheten der ID-en for mva-organisasjonsnummeret brukes. Du kan kopiere en kunde bare hvis den er i en juridisk enhet som ikke er gjeldende juridisk enhet. Følg fremgangsmåten nedenfor når du har valgt en kunde som oppfyller dette kriteriet.

1. Alternativet **Kopier kunde** vises. Dette alternativet er satt til **Nei** som standard. Hvis du vil kopiere kunden til gjeldende juridisk enhet, setter du alternativet til **Ja**. 
2. Velg **Velg**. Den nye kunden opprettes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
