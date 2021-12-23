---
title: Asynkron kundeopprettingsmodus
description: Dette emnet beskriver den asynkrone kundeopprettingsmodusen i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 22bb4eaf3d4897904412120fa5580c42637b56e0
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913805"
---
# <a name="asynchronous-customer-creation-mode"></a>Asynkron kundeopprettingsmodus

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet beskriver den asynkrone kundeopprettingsmodusen i Microsoft Dynamics 365 Commerce.

I Commerce finnes det to måter å opprette kunder på: synkron (sync) og asynkron (async). Som standard opprettes kunder synkront. De opprettes med andre ord i Commerce Headquarters i sanntid. Kundeopprettingsmodusen for synkron kan være nyttig fordi nye kunder umiddelbart kan søkes etter på tvers av kanaler. Den har imidlertid også en tilbaketrekking. Ettersom modusen genererer kall i [Commerce Data Exchange: Real-time Service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) til Commerce Headquarters, kan ytelsen påvirkes hvis det utføres mange samtidige kundeopprettingsanrop.

Hvis alternativet **Opprett kunde i asynkron modus** er satt til **Ja** i butikkens funksjonalitetsprofil (**Detaljhandel og handel \> Kanaloppsett \> Oppsett av nettbutikk \> Funksjonsprofiler**), brukes ikke kall i Real-time Service til å opprette kundeposter i kanaldatabasen. Asynkron modus for kundeoppretting påvirker ikke ytelsen til Commerce Headquarters. En midlertidig, globalt unik ID tilordnes hver nye Async-kundepost og brukes som kundekonto-ID. Denne GUID-en vises ikke for salgsstedsbrukere. I stedet vil disse brukerne se **Venter på synkronisering** som kundekonto-ID-en.

> [!IMPORTANT]
> Hvis POS kobles fra, oppretter systemet automatisk kundene asynkront, selv om asynkron modus for kundeoppretting er deaktivert. Uansett hva du velger mellom synkron og asynkron kundeoppretting, må derfor Commerce Headquarters-administratorer opprette og planlegge en gjentakende satsvis jobb for **P-jobben**, jobben **Synkroniser kunder og forretningspartnere fra asynkron modus** (tidligere kalt jobben **Synkronisere kunder og forretningspartnere fra asynkron modus**), og **1010**-jobben, slik at alle asynkron-kunder blir konvertert til synkron-kunder i Commerce Headquarters.

## <a name="async-customer-limitations"></a>Async-kundebegrensninger

Asynkron-kundefunksjonaliteten har følgende begrensninger:

- Async-kundeposter kan ikke redigeres med mindre kunden er opprettet i Commerce Headquarters, og den nye kundekonto-IDen er synkronisert tilbake til kanalen.
- Fordelskort kan ikke utstedes til asynkron-kunder med mindre den nye kundekonto-IDen er synkronisert tilbake til kanalen.

## <a name="async-customer-enhancements"></a>Asynkron-kundeforbedringer

I Commerce versjon 10.0.24-versjonen kan du aktivere funksjonen for **aktivering av forbedret asynkron-kundeopprettelse** i arbeidsområdet for **Funksjonsbehandling**. Denne funksjonen bygger bro mellom asynkrone og synkrone kundeopprettingsmoduser på salgsstedet og e-handel på følgende måter:

- Ansettelsesforhold kan ikke knyttes til asynkron-kunder.
- Titler kan legges til i asynkron-kunder.
- Sekundære e-postadresser og telefonnumre kan ikke registreres for asynkron-kunder.

I Commerce versjon 10.0.22-versjonen kan du aktivere funksjonen for **Aktiver asynkron oppretting for kundeadresser** i arbeidsområdet for **Funksjonsbehandling**. Ved hjelp av denne funksjonen kan nyopprettede kundeadresser lagres asynkront for både synkron-kunder og asynkron-kunder.

Når du har aktivert tidligere nevnte funksjoner, må du planlegge en gjentakende satsvis jobb for **P-jobb**, jobben **Synkroniser kunder og forretningspartnere fra asynkron modus** og **1010**-jobben, slik at alle asynkron-kunder konverteres til synkron-kunder i Commerce Headquarters.

### <a name="customer-creation-in-pos-offline-mode"></a>Kundeoppretting i frakoblet modus i POS

Som nevnt tidligere, hvis POS kobles fra, oppretter systemet automatisk kundene asynkront, selv om opprettingsmodus for asynkron-kunde er deaktivert. Derfor må Commerce Headquarters-administratorer opprette og planlegge en gjentakende satsvis jobb for **P-jobb**, jobben **Synkroniser kunder og forretningspartnere fra asynkron modus** og jobben **1010**, slik at alle asynkron-kunder konverteres til synkron-kunder i Commerce Headquarters.

> [!NOTE]
> Hvis alternativet **Filtrer delte kundedatatabeller** er satt til **Ja** på siden **Handelskanalskjema** (**Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabasegruppe**), blir ikke kundeposter opprettet i frakoblet modus i POS. Hvis du vil ha mer informasjon, kan du se [Utelatelse av frakoblede data](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Tilleggsressurser

[Kundebehandling i butikker](customer-mgmt-stores.md)

[Konvertere asynkron-kunder til synkron-kunder](convert-async-to-sync.md)

[Kundeattributter](dev-itpro/customer-attributes.md)

[Utelatelse av frakoblede data](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
