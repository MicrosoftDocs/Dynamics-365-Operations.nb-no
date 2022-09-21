---
title: Asynkron kundeopprettingsmodus
description: Denne artikkelen beskriver den asynkrone kundeopprettingsmodusen i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 95102936871e15f8e525abca736fa75927569b34
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473713"
---
# <a name="asynchronous-customer-creation-mode"></a>Asynkron kundeopprettingsmodus

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver den asynkrone kundeopprettingsmodusen i Microsoft Dynamics 365 Commerce.

I Commerce finnes det to måter å opprette kunder på: synkron (sync) og asynkron (async). Som standard opprettes kunder synkront. De opprettes med andre ord i Commerce Headquarters i sanntid. Kundeopprettingsmodusen for synkron kan være nyttig fordi nye kunder umiddelbart kan søkes etter på tvers av kanaler. Den har imidlertid også en tilbaketrekking. Ettersom modusen genererer kall i [Commerce Data Exchange: Real-time Service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) til Commerce Headquarters, kan ytelsen påvirkes hvis det utføres mange samtidige kundeopprettingsanrop.

Hvis alternativet **Opprett kunde i asynkron modus** er satt til **Ja** i butikkens funksjonalitetsprofil (**Detaljhandel og handel \> Kanaloppsett \> Oppsett av nettbutikk \> Funksjonsprofiler**), brukes ikke kall i Real-time Service til å opprette kundeposter i kanaldatabasen. Asynkron modus for kundeoppretting påvirker ikke ytelsen til Commerce Headquarters. En midlertidig, globalt unik ID tilordnes hver nye Async-kundepost og brukes som kundekonto-ID. Denne GUID-en vises ikke for salgsstedsbrukere. I stedet vil disse brukerne se **Venter på synkronisering** som kundekonto-ID-en.

> [!IMPORTANT]
> Hvis POS kobles fra, oppretter systemet automatisk kundene asynkront, selv om asynkron modus for kundeoppretting er deaktivert. Derfor, uavhengig av valget mellom synkron og asynkron kundeoppretting, må Commerce headquarters-administratorer opprette og planlegge en gjentakende satsvis jobb for **P-jobben**, jobben **Synkroniser kunder og forretningspartnere fra Async-modus** og jobben **1010**, slik at alle asynkrone kunder konverteres til synkrone kunder i Commerce headquarters.

## <a name="async-customer-limitations"></a>Async-kundebegrensninger

Asynkron-kundefunksjonaliteten har følgende begrensninger:

- Fordelskort kan ikke utstedes til asynkron-kunder med mindre den nye kundekonto-IDen er synkronisert tilbake til kanalen.

## <a name="async-customer-enhancements"></a>Asynkron-kundeforbedringer

For å hjelpe organisasjoner med å bruke asynkron kundeopprettingsmodus for å administrere kunder, og til å redusere kommunikasjon i sanntid med Commerce headquarters, har følgende forbedringer rullet ut for å bringe paritet mellom synkrone og asynkrone moduser i kanaler. 

| Funksjonsforbedring | Commerce-versjon | Funksjonsdetaljer |
|---|---|---|
| Ytelsesforbedringer når kundeinformasjon hentes fra kanaldatabasen | 10.0.20 og nyere | Kundeenheten er delt inn i mindre enheter for å forbedre ytelsen. Systemet henter da bare den nødvendige informasjonen fra kanaldatabasen. |
| Mulighet til å opprette adresse asynkront under betaling | 10.0.22 og nyere | <p>Funksjonsbytte: **Aktiver asynkron oppretting for kundeadresser**</p><p>Funksjonsdetaljer:</p><ul><li>Mulighet til å legge til adresser uten å foreta serviceanrop i sanntid til Commerce headquarters</li><li>Mulighet til å identifisere adresser i kanaldatabasen entydig uten å bruke en post-ID (**RecId**-verdi)</li><li>Sporing av tidsstempler for adresseoppretting</li><li>Synkronisering av adresser i Commerce headquarters</li></ul><p>Denne funksjonen påvirker både synkroniserte kunder og asynkrone kunder. Hvis du vil redigere adresser asynkron i tillegg til å opprette dem asynkront, må du aktivere funksjonen **Redigering av kunder i asynkron modus**.</p> |
| Aktiver paritet mellom synkron og asynkron kundeopprettelse. | 10.0.24 og nyere | <p>Funksjonsbytte: **Aktiver forbedret asynkron kundeopprettelse**</p><p>Funksjonsdetaljer: Mulighet til å registrere tilleggsinformasjon, som tittel, ansettelsesforhold fra standardkunden og sekundær kontaktinformasjon (telefonnummer og e-postadresse), mens du oppretter kunder asynkront</p> |
| Brukervennlige feilmeldinger | 10.0.28 og nyere | Disse forbedringene hjelper deg med å forbedre brukervennlige feilmeldinger hvis en bruker ikke umiddelbart kan redigere informasjon mens synkroniseringen pågår. Du aktiverer disse forbedringene ved å bruke innstillingen **Tillat bestemte grensesnittelementer som ikke kan endres av en asynkron kunde** under **Områdeinnstillinger \> Utvidelser** i Commerce-områdebygger. |
| Mulighet til å redigere kundeinformasjon asynkron | 10.0.29 og nyere | <p>Funksjonsbytte: **Aktiver redigering av kunder i asynkron modus**</p><p>Funksjonsdetaljer: Mulighet til å redigere kundedata asynkron</p><p>Hvis du vil ha svar på vanlige spørsmål om problemer som er knyttet til å redigere kundeinformasjon asynkront, kan du se [Vanlige spørsmål om asynkron kundeopprettingsmodus](async-customer-mode-faq.md).</p> |

### <a name="feature-switch-hierarchy"></a>Funksjonsbyttehierarki

På grunn av hierarkiet av funksjonsbytter må følgende funksjoner aktiveres før du aktiverer funksjonen **Aktiver redigering av kunder i asynkron modus**: 

- **Ytelsesforbedringer for kundeordrer og kundetransaksjoner** – Denne funksjonen er obligatorisk siden Commerce-versjon 10.0.28. 
- **Aktiver forbedret asynkron kundeopprettelse**
- **Aktiver asynkron oppretting for kundeadresser**

Hvis du vil ha svar på vanlige feilsøkingsspørsmål, kan du se [Vanlige spørsmål om asynkron kundeopprettingsmodus](async-customer-mode-faq.md). 

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
