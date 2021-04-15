---
title: Kundebehandling i butikker
description: Dette emnet beskriver hvordan forhandlere kan aktivere kundebehandlingsfunksjoner ved salgsstedet (POS) i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46a18d36a389e8a52253c2c3a153e0eae95c0e57
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799427"
---
# <a name="customer-management-in-stores"></a>Kundebehandling i butikker

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan forhandlere kan aktivere kundebehandlingsfunksjoner ved salgsstedet (POS) i Microsoft Dynamics 365 Commerce.

Det er viktig at butikkmedarbeidere kan opprette og redigere kundeposter i salgsstedet. På den måten kan de registrere alle oppdateringer til kundeopplysninger som e-postadresse, telefonnummer og adresse. Denne informasjonen er nyttig i systemene som brukes til nedbetaling, for systemenes effektivitet avhenger av nøyaktigheten til kundedataene.

Salgsmedarbeidere kan utløse arbeidsflyten for kundeopprettelse fra to POS-oppføringspunkter. De kan velge en knapp som er tilordnet til operasjonen **Legg til kunde**, eller de kan velge **Opprett kunde** på applinjen på søkeresultatsiden. I begge tilfeller vises dialogboksen **Ny kunde**, der salgsmedarbeidere kan angi nødvendige kundedetaljer, for eksempel kundens navn, e-postadresse, telefonnummer, adresse og eventuell tilleggsinformasjon som er relevant for virksomheten. Denne tilleggsinformasjonen kan registreres ved hjelp av kundeattributtene som er tilknyttet kunden. Hvis du vil ha mer informasjon om kundeattributter, kan du se [Kundeattributter](dev-itpro/customer-attributes.md).

Salgsmedarbeidere kan også registrere sekundære e-postadresser og telefonnumre. I tillegg kan de registrere kundens ønsker om å motta markedsføringsinformasjon via en hvilken som helst av disse sekundære e-postadressene eller telefonnumrene. For å aktivere denne funksjonaliteten må forhandlere aktivere funksjonen **Lagre flere e-poster og telefonnumre og samtykke for markedsføring i disse kontaktene** i arbeidsområdet **Funksjonsstyring** i Commerce Headquarters (**Systemadministrasjon \> Arbeidsområder \> Funksjonsstyring**).

## <a name="default-customer-properties"></a>Standard kundeegenskaper

Forhandlere kan bruke siden **Alle butikker** i Commerce Headquarters (**Detaljhandel og handel \> Kanaler \> Butikker**) til å knytte en standardkunde til hver butikk. Commerce kopierer deretter egenskapene som er definert for standardk kunde, til alle nye kundeposter som opprettes. Dialogboksen **Opprett kunde** viser for eksempel egenskaper som arves fra standardkunden som er knyttet til butikken. Disse egenskapene inkluderer kundetypen, kundegruppen, kvitteringsinnstillinger, valuta og språk. Eventuelle ansettelsesforhold (kundegrupper) arves også fra standardkunden. Finansdimensjoner arves imidlertid fra kundegruppen som er knyttet til standardk kunden, ikke fra selve standardkanten.

Salgsmedarbeidere kan registrere flere adresser for en kunde. Kundens navn og telefonnummer arves fra kontaktinformasjonen som er tilknyttet hver adresse. Hurtigfanen **Adresser** i en kundepost inneholder feltet **Formål** som salgsmedarbeidere kan redigere. Hvis kundetypen er **Person**, er standardverdien **Hjem**. Hvis kundetypen er **Organisasjon**, er standardverdien **Virksomhet**. Andre verdier som dette feltet støtter, omfatter **Hjem**, **Kontor** og **Postboks**. Verdien i feltet **Land** for en adresse blir arvet fra den primære adressen som er angitt på siden **Driftsenhet** i Commerce Headquarters under **Organisasjonsstyring \> Organisasjoner \> Driftsenheter**.

## <a name="sync-customers-and-async-customers"></a>Synkronisere kunder og Async-kunder

I Commerce finnes det to måter å opprette kunder på: Synkron (eller Synkron) og Asynkron (eller Asynkron). Som standard opprettes kunder synkront. De opprettes med andre ord i Commerce Headquarters i sanntid. Det kan være nyttig å synkronisere kundeopprettingsmodus, fordi nye kunder umiddelbart kan søke på tvers av kanaler. Den har imidlertid også en tilbaketrekking. Ettersom modusen genererer kall i [Commerce Data Exchange: Real-time Service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) til Commerce Headquarters, kan ytelsen påvirkes hvis det utføres mange samtidige kundeopprettingsanrop.

Hvis alternativet **Opprett kunde i asynkron modus** er satt til **Ja** i butikkens funksjonalitetsprofil (**Detaljhandel og handel \> Kanaloppsett \> Oppsett av nettbutikk \> Funksjonsprofiler**), brukes ikke kall i Real-time Service til å opprette kundeposter i kanaldatabasen. Opprettingsmodus for asynkron kunde påvirker ikke ytelsen til Commerce Headquarters. En midlertidig, globalt unik ID tilordnes hver nye Async-kundepost og brukes som kundekonto-ID. Denne GUID-en vises ikke for POS-brukere. I stedet vil disse brukerne se **Venter på synkronisering** som kundekonto-ID-en. Selv om denne konfigurasjonen tvinger kunder til å opprettes asynkront, gjøres det alltid synkront å redigere kundeposter.

### <a name="convert-async-customers-to-sync-customers"></a>Konvertere Async-kunder til Sync-kunder

Hvis du vil konvertere Async-kunder til Sync-kunder, må du først kjøre P-jobben for å sende Async-kundene til Commerce Headquarters. Deretter kjører du jobben **Synkroniser kunder og forretningspartnere fra asynkron modus** for å opprette kundekonto-ID-er. Til slutt kjører du jobben **1010** for å synkronisere de nye kundekonto-ID-ene til kanalene.

### <a name="async-customer-limitations"></a>Async-kundebegrensninger

Async-kundefunksjonaliteten har følgende begrensninger:

- Async-kundeposter kan ikke redigeres med mindre kunden er opprettet i Commerce Headquarters, og den nye kundekonto-IDen er synkronisert tilbake til kanalen.
- Ansettelsesforhold kan ikke knyttes til Async-kunder. Derfor arver ikke nye Async-kunder ansettelsesforhold fra standardkunden.
- Fordelskort kan ikke utstedes til Async-kunder med mindre den nye kundekonto-IDen er synkronisert tilbake til kanalen.
- Sekundære e-postadresser og telefonnumre kan ikke registreres for Async-kunder.

### <a name="customer-creation-in-pos-offline-mode"></a>Kundeoppretting i frakoblet modus i POS

Hvis POS kobles fra mens opprettingsmodus for Async-kunde er aktivert, opprettes det nye kundeposter asynkront. Hvis POS kobles fra mens opprettingsmodus for Async-kunde er deaktivert, bytter systemet automatisk til opprettingsmodus for asynkron kunde. Med andre ord kan det hende kundeposter blir opprettet asynkront selv om opprettingsmodus for Async-kunde er deaktivert. Derfor må Commerce Headquarters-administratorer opprette og planlegge en gjentakende satsvis jobb for P-jobben, jobben **Synkroniser kunder og forretningspartnere fra Async-modus** og jobben **1010**, slik at alle Async-kunder konverteres til Sync-kunder i Commerce Headquarters.

> [!NOTE]
> Hvis alternativet **Filtrer delte kundedatatabeller** er satt til **Ja** på siden **Handelskanalskjema** (**Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabasegruppe**), blir ikke kundeposter opprettet i frakoblet modus i POS. Hvis du vil ha mer informasjon, kan du se [Utelatelse av frakoblede data](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Tilleggsressurser

[Kundeattributter](dev-itpro/customer-attributes.md)

[Utelatelse av frakoblede data](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
