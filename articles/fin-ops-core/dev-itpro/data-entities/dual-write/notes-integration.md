---
title: Merknadsintegrering
description: Dette emnet beskriver integreringen av merknadsdata i dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ceb5b7c90cc7efa0049d0278e2c245228e5b52bd
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186792"
---
# <a name="note-integration"></a>Merknadsintegrering

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I forretningsprosesser samler Microsoft Dynamics 365-brukere ofte inn informasjon om kundene sine. Denne informasjonen registreres som aktiviteter og merknader. Dette emnet beskriver integreringen av merknadsdata i dobbel skriving.

Kundeopplysninger kan klassifiseres på følgende måter:

+ **Handlingsbar informasjon som en Dynamics 365-bruker håndterer på vegne av en kunde** –  Contoso (en Dynamics 365-bruker) arrangerer for eksempel en spørrekonkurranse. En av Contoso-kundene (en kunde) ønsker å delta i spørrekonkkurransen. Kunden ber en Contoso-ansatt om å reservere en plass i spørrekonkkurranse for dem. Reservasjonen skjer i Contoso sin hendelseskalender for deltakeren.
+ **Informasjon som kan behandles for en Dynamics 365-bruker** – En kunde som kjøper en Surface-enhet, legger for eksempel inn spesielle instruksjoner som indikerer at enheten skal pakkes inn i gave før levering. Disse instruksjonene er informasjon som kan behandles, og som bør behandles av Contoso-ansatte som er ansvarlig for emballasje.
+ **Informasjon som ikke kan behandles** – En kunde besøker for eksempel Contoso-butikken, og uttrykker interesse for *Halo*-spill og spilltilbehør i samtalen med butikkmedarbeideren. Butikkmedarbeideren noterer seg denne informasjonen. Produktanbefalingsmotoren bruker deretter informasjonen til å foreta anbefalinger til kunden.

Som regel registreres informasjon som kan behandles, som *aktiviteter* i Finance and Operations-apper og Customer Engagement-apper. Informasjon som ikke kan behandles, blir lagret som *merknader* i Finance and Operations-apper, og som *kommentarer* i Customer Engagement-apper.

> [!TIP]
> Selv om notater er beregnet på informasjon som ikke kan behandles, vil ikke appene hindre deg i å bruke dem til å lagre og håndtere informasjon som kan behandles, hvis du vil bruke dem på denne måten.

Microsoft frigir funksjonalitet for merknadsintegrering. (Funksjonalitet for aktivitetsintegrering blir frigitt senere.) Merknadsintegrasjon er tilgjengelig for kunder, leverandører, salgsordrer og bestillinger.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Opprette en merknad i en Customer Engagement-app

Følg denne fremgangsmåten for å opprette et notat i en Customer Engagement-app og deretter synkronisere den med en Finance and Operations-app.

1. Åpne kontoposten for en kunde i Customer Engagement-appen.
2. I ruten **Tidslinje** velger du plusstegnet (**+**), og deretter velger du **Merknad** for å opprette en merknad.

    ![Oppretting av en merknad i Customer Engagement-appen](media/notes-ce-1.png)

3. Skriv inn en tittel og en beskrivelse, og velg deretter **Legg til merknad**.

    ![Angivelse av en tittel og en beskrivelse](media/notes-ce-2.png)

    Den nye merknaden legges til på kundetidslinjen.

    ![Ny merknad på kundetidslinjen](media/notes-ce-3.png)

4. Logg på Finance and Operations-appen og åpne den samme kundeposten. Legg merke til knappen **Vedlegg** (binderssymbol) i øvre høyre hjørne viser at posten har en tilknytning.

    ![Varsling om en tilknytning](media/notes-ce-4.png)

5. Velg knappen **Vedlegg** for å åpne siden **Vedlegg**. Du bør finne merknaden du opprettet i Customer Engagement-appen.

    ![Merknad fra Customer Engagement-appen](media/notes-ce-5.png)

Alle oppdateringer av merknaden synkroniseres frem og tilbake mellom Finance and Operations-appen og Customer Engagement-appen.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Opprette en merknad i en Finance and Operations-app

Du kan også opprette en merknad i en Finance and Operations-app, og den blir synkronisert til en Customer Engagement-app.

Følg denne fremgangsmåten for å opprette et notat i en Finance and Operations-app og deretter synkronisere den med en Customer Engagement-app.

1. Velg **Ny** \> **merknad** på siden **Vedlegg** i Finance and Operations-appen.

    ![Oppretting av en merknad i Finance and Operations-appen](media/notes-fo-1.png)

2. Skriv inn en tittel og et kort sett med instruksjoner, og velg deretter **Lagre**.

    ![Angivelse av en tittel og instruksjoner](media/notes-fo-2.png)

3. Oppdater posten i Customer Engagement-appen. Du bør finne det nye notatet på tidslinjen.

    ![Ny merknad på tidslinjen i Customer Engagement-appen](media/notes-fo-3.png)

Du kan klassifisere en merknad som enten intern eller ekstern.

- Åpne merknaden på siden **Vedlegg** i Finance and Operations-appen, og velg deretter **Intern** eller **Ekstern** i feltet **Begrensning**.

    ![Restriksjonsfelt](media/notes-fo-4.png)

Du kan også opprette en URL.

1. Velg **Ny** \> **URL** på siden **Vedlegg** i Finance and Operations-appen.
2. Angi en tittel og URL-adressen.
3. Velg **Intern** eller **Ekstern** i feltet **Begrensning**.

    ![Oppretting av en URL-adresse i Finance and Operations-appen](media/notes-fo-5.png)

4. Velg **Lagre**.

    Ettersom Customer Engagement-apper ikke har en URL-type, er URL-adressen integrert med skrivetilgang som et notat.

    ![URL-adresse som vises som et notat i Customer Engagement-appen](media/notes-ce-6.png)

> [!NOTE]
> Filvedlegg støttes ikke.

## <a name="templates"></a>Maler

Merknadsintegrering inkluderer en samling tabelltilordninger som fungerer sammen under datasamhandling, som vist i følgende tabell.

| Finance and Operations-app | Kundeengasjementsapp | beskrivelse |
|----------------------------|-------------------------|-------------|
| [Kundevedlegg](mapping-reference.md#230) | Merknader | Virksomheter som bruker ren tekst og URL-adresser, til å registrere kundespesifikk informasjon (for både organisasjoner og personer). |
| [Vedlegg for leverandørdokument](mapping-reference.md#231) | Merknader | Virksomheter som bruker ren tekst og URL-adresser, til å registrere leverandørspesifikk informasjon (for både organisasjoner og personer). |
| [Dokumentvedlegg for topptekst i salgsordre](mapping-reference.md#229) | Merknader | Virksomheter som bruker ren tekst og URL-adresser, til å registrere salgsordrespesifikk informasjon. |
| [Dokumentvedlegg for topptekst i bestilling](mapping-reference.md#232) | Merknader | Virksomheter som bruker ren tekst og URL-adresser, til å registrere bestillingspesifikk informasjon. |

## <a name="limitations"></a>Begrensninger

Når du har installert merknadsløsningen, kan du ikke avinstallere den. 

Hvis du vil ha mer informasjon, kan du se [Referanse for lesetilgang til skrivetilgang](mapping-reference.md).
