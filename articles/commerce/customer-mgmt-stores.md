---
title: Kundebehandling i butikker
description: Denne artikkelen beskriver hvordan forhandlere kan aktivere kundebehandlingsfunksjoner ved salgsstedet (POS) i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 805d0b5894b18e2fc34f481bdc32ada7a4b1aee0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863493"
---
# <a name="customer-management-in-stores"></a>Kundebehandling i butikker

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan forhandlere kan aktivere kundebehandlingsfunksjoner ved salgsstedet (POS) i Microsoft Dynamics 365 Commerce.

Det er viktig at butikkmedarbeidere kan opprette og redigere kundeposter i salgsstedet. På den måten kan de registrere alle oppdateringer til kundeopplysninger som e-postadresse, telefonnummer og adresse. Denne informasjonen er nyttig i systemene som brukes til nedbetaling, for systemenes effektivitet avhenger av nøyaktigheten til kundedataene.

Salgsmedarbeidere kan utløse arbeidsflyten for kundeopprettelse fra to POS-oppføringspunkter. De kan velge en knapp som er tilordnet til operasjonen **Legg til kunde**, eller de kan velge **Opprett kunde** på applinjen på søkeresultatsiden. I begge tilfeller vises dialogboksen **Ny kunde**, der salgsmedarbeidere kan angi nødvendige kundedetaljer, for eksempel kundens navn, e-postadresse, telefonnummer, adresse og eventuell tilleggsinformasjon som er relevant for virksomheten. Denne tilleggsinformasjonen kan registreres ved hjelp av kundeattributtene som er tilknyttet kunden. Hvis du vil ha mer informasjon om kundeattributter, kan du se [Kundeattributter](dev-itpro/customer-attributes.md).

Salgsmedarbeidere kan også registrere sekundære e-postadresser og telefonnumre. I tillegg kan de registrere kundens ønsker om å motta markedsføringsinformasjon via en hvilken som helst av disse sekundære e-postadressene eller telefonnumrene. For å aktivere denne funksjonaliteten må forhandlere aktivere funksjonen **Lagre flere e-poster og telefonnumre og samtykke for markedsføring i disse kontaktene** i arbeidsområdet **Funksjonsstyring** i Commerce Headquarters (**Systemadministrasjon \> Arbeidsområder \> Funksjonsstyring**).

## <a name="default-customer-properties"></a>Standard kundeegenskaper

Forhandlere kan bruke siden **Alle butikker** i Commerce Headquarters (**Detaljhandel og handel \> Kanaler \> Butikker**) til å knytte en standardkunde til hver butikk. Commerce kopierer deretter egenskapene som er definert for standardk kunde, til alle nye kundeposter som opprettes. Dialogboksen **Opprett kunde** viser for eksempel egenskaper som arves fra standardkunden som er knyttet til butikken. Disse egenskapene inkluderer **kundetype**, **kundegruppe**, **kvitteringsalternativ**, **kvitterings-e-post**, **valuta** og **språk**. Eventuelle **tilknytninger** (kundegrupper) arves også fra standardkunden. **Finansdimensjoner** arves imidlertid fra kundegruppen som er knyttet til standardkunden, ikke fra selve standardkunden.

> [!NOTE]
> Verdien av **e-postkvittering** blir bare kopiert fra standardkunden hvis e-post-IDen for kvittering ikke er angitt for de nyopprettede kundene. Dette betyr at hvis kvitterings-e-post-IDen finnes på standardkunden, vil alle kundene som er opprettet fra e-handelsområdet, få samme e-post-ID for kvittering, fordi det ikke finnes et brukergrensesnitt for å registrere kvitterings-e-post-IDen fra kunden. Vi anbefaler at du holder **kvitterings-e-post**-feltet tomt for butikkens standardkunde og bare bruker det hvis du har en forretningsprosess som er avhengig av at en kvitterings-e-postadresse vises. 

Salgsmedarbeidere kan registrere flere adresser for en kunde. Kundens navn og telefonnummer arves fra kontaktinformasjonen som er tilknyttet hver adresse. Hurtigfanen **Adresser** i en kundepost inneholder feltet **Formål** som salgsmedarbeidere kan redigere. Hvis kundetypen er **Person**, er standardverdien **Hjem**. Hvis kundetypen er **Organisasjon**, er standardverdien **Virksomhet**. Andre verdier som dette feltet støtter, omfatter **Hjem**, **Kontor** og **Postboks**. Verdien i feltet **Land** for en adresse blir arvet fra den primære adressen som er angitt på siden **Driftsenhet** i Commerce Headquarters under **Organisasjonsstyring \> Organisasjoner \> Driftsenheter**.



## <a name="additional-resources"></a>Tilleggsressurser

[Asynkron kundeopprettingsmodus](async-customer-mode.md)

[Konvertere asynkron-kunder til synkron-kunder](convert-async-to-sync.md)

[Kundeattributter](dev-itpro/customer-attributes.md)

[Utelatelse av frakoblede data](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
