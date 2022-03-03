---
title: Administrere B2B-forretningspartnere ved hjelp av kundehierarkier
description: Dette emnet beskriver hvordan du bruker kundehierarkider til å administrere forretningspartnere for bedrift-til-bedrift-e-handelsnettsteder (B2B) for Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6e594cbb824a8b823912118e99b819585adc45e
ms.sourcegitcommit: 8bcb9c13eccb14e61c39ca6578d135b64090fad2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2022
ms.locfileid: "8313834"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>Administrere B2B-forretningspartnere ved hjelp av kundehierarkier

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du bruker kundehierarkider til å administrere forretningspartnere for bedrift-til-bedrift-e-handelsnettsteder (B2B) for Microsoft Dynamics 365 Commerce.

I Commerce Headquarters brukes enheten *kundehierarki* til å representere forretningspartnerorganisasjonene som bruker B2B-e-handelsnettstedet. Før du kan begynne å bruke kundehierarkier til å administrere forretningspartnere, må du aktivere funksjonene for B2B-e-handel i Commerce Headquarters og deretter definere en nummerserie for kundehierarkiet.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>Aktivere funksjonen for B2B-e-handel i Commerce Headquarters

For å kunne bruke funksjonene for B2B-e-handel må du først aktivere funksjonen **Aktiver bruk av B2B-funksjoner for e-handel** i Commerce Headquarters.

1. Gå til **Arbeidsområder \> Funksjonsbehandling**.
1. I **Alle**-fanen bruker du filterboksen til å søke etter **Modul: Detaljhandel og handel**.
1. Finn funksjonen **Aktiver bruk av B2B-funksjoner for e-handel**, velg den, og velg deretter **Aktiver nå** i nedre høyre hjørne.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Definere en nummerserie for kundehierarkiet

Nummerserier brukes for å generere lesbare, unike ID-er for hoveddataposter og transaksjonsposter som krever ID-er. Du må definere en nummerserie som skal brukes til å generere ID-en for kundehierarkiet. Hvis du vil ha mer informasjon om nummerserier, kan du se [Oversikt over nummerserier](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Du definerer en nummerserie for kundehierarkiet i Commerce Headquarters ved å følge denne fremgangsmåten.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Nummerserier \> Nummerserier**.
1. Opprett en ny nummerserie, eller velg en eksisterende nummerserie for å bruke den på nytt.
1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere**.
1. I **Nummerserier**-fanen legger du til nummerserien du opprettet eller valgte tidligere, i referansen **Kundehierarki-ID**.

![Nummerserien er lagt til i referansen Kundehierarki-ID.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Hvordan godkjenningsprosessen fungerer

Når en forretningspartner ber om å bli med på et B2B-e-handelsnettsted, lagrer systemet forespørselen som et *kundeemne*. En identitet i Commerce Headquarters, for eksempel en driftsleder for detaljhandel, kan godkjenne eller avvise partnerforespørsler. Hvis du vil ha mer informasjon om hvordan du administrerer forretningspartnerforespørsler og kundeemnegodkjenninger, kan du se [Administrere forretningspartnerbrukere på B2B-e-handelsnettsteder](manage-b2b-users.md).

Når et kundeemne godkjennes, oppretter systemet to nye kundeposter:

- Én kundepost av typen **Organisasjon** representerer organisasjonen som ber om å bli forretningspartner.
- Én kundepost av typen **Person** representerer personen som sendte inn forespørselen.

Det opprettes i tillegg en ny kundehierarkipost i **Detaljhandel og handel \> Kunder \> Kundehierarkier**. Denne kundehierarkiposten har følgende egenskaper:

- **Kundehierarki-ID** – Den unike ID-en for kundehierarkiet. Denne ID-en bruker nummerserien du definerte i Delte handelsparametere.
- **Navn** – Organisasjonsnavnet til forretningspartneren, som angitt i forespørselen om pålasting. Dette feltet kan redigeres.
- **Formål** – Denne egenskapen er satt til den forhåndsdefinerte verdien **B2B-organisasjon**.
- **Organisasjon** – Kunde-ID-en til forretningspartnerorganisasjonen.

Personen som sendte inn innføringsforespørselen, blir lagt til i hurtigfanen **Hierarki**, og vedkommende for tilordnet rollen **Administrator**. Etter hvert som administratoren legger til flere brukere i forretningspartnerorganisasjonen på et B2B-område, opprettes det en ny kundepost for hver bruker. Kundeposten legges også til i den relevante kundehierarkiposten for forretningspartneren, og rollen **Bruker** blir tilordnet til den.

### <a name="examples"></a>Eksempler

En person med navnet Sam J. sender inn en innføringsforespørsel på vegne av Microsoft-organisasjonen. Når forespørselen er godkjent, opprettes det to nye kundekontoer: en av typen **Person** for Sam J. og en av typen **Organisasjon** for Microsoft.

Eksemplet i illustrasjonen nedenfor viser at det også opprettes en ny kundehierarkipost. Denne posten har samme navn som organisasjonen (**Microsoft**), og rollen **Administrator** blir tilordnet til Sam J. Som administrator legger Sam J. til eventuelle andre Microsoft-brukere for B2B-området i dette hierarkiet og tilordner rollen **Bruker** til dem. I dette eksemplet er Sush R. lagt til som en bruker.

![Eksempel på en kundehierarkipost.](../media/CustomerHierarchy2.png)

Du kan fastsette om en kunde er knyttet til et kundehierarki, ved å åpne kundeposten. Eksemplet i illustrasjonen nedenfor viser at feltet **Kundehierarki-ID** i **B2B**-delen i hurtigfanen **Detaljhandel** viser om kunden er en del av et kundehierarki, og alternativet **B2B-administrator** angir om kunden er administrator for dette hierarkiet.

![Eksempel på B2B-delen i hurtigfanen Detaljhandel for en kundepost der kunden er knyttet til et hierarki og angitt som administrator.](../media/CustomerHierarchyMapping2.png)

I de fleste tilfeller skal egenskapsverdiene for alle kundeposter i et hierarki samsvare. Fordi alle forretningspartnerbrukere for eksempel skal få like priser for produkter, bør prisgruppen og tilknyttede konfigurasjoner samsvare. Systemet iverksetter imidlertid ikke denne konsistensen. Derfor er de relevante Commerce Headquarters-brukerne ansvarlige for å sikre at egenskapsverdiene og konfigurasjonene samsvarer for alle kunder i et gitt hierarki.

Commerce Headquarters-brukere kan undersøke egenskapsverdiene for alle kundeposter i et hierarki i side-ved-side-visning. Eksemplet i illustrasjonen nedenfor viser at du kan bruke alternativet **Generelt** i rullegardinlisten i hurtigfanen **Hierarki** og deretter velge enhver del i kundeposten for å vise de relaterte egenskapene. Brukere kan redigere egenskapsverdiene direkte i denne visningen. Hvis du vil kopiere alle verdiene fra en administratorkundepost til alle brukere, velger du **Overstyr** i hurtigfanen **Hierarki**.

![Eksempel på en kundehierarkipost som viser Overstyr-knappen og alternativet i rullegardinlisten.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
