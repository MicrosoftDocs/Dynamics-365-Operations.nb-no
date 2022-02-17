---
title: Sammenslåing av Dynamics 365 Human Resources-infrastruktur – oppdatering av versjon 10.0.25
description: Dette emnet inneholder informasjon om Microsoft Dynamics 365 Human Resources, versjon 10.0.25, som inneholder den første bølgen av funksjoner i sammenslåingen av infrastrukturen.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a80bedd0224f1e31dfec4e9f4c39ad1ed75d7f2f
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024573"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Sammenslåing av Dynamics 365 Human Resources-infrastruktur – oppdatering av versjon 10.0.25

10.0.25-versjonen inneholder den første bølgen av funksjoner i sammenslåingen av infrastrukturen. I løpet av sammenslåingen av infrastrukturen blir Microsoft Dynamics 365 Human Resources slått sammen med Finance and Operations-infrastrukturen. Det vil imidlertid fortsatt være lisensiert som en uavhengig app, for eksempel Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Hvis du vil ha mer informasjon om sammenslåingen av infrastrukturen, kan du se [Vanlige spørsmål om sammenslåingen av Dynamics 365 Human Resources-infrastrukturen](../human-resources/hr-infrastructure-merge-faq.md).

Sammenslåingen vil gi konsistens for Human Resources-brukere på følgende måter:

- [Miljøstyring og integreringer er konsekvent mellom Human Resources- og Finance and Operations-apper.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Administrer miljøer i Microsoft Dynamics Lifecycle Services, problemsøk og Regression Suite Automation Tool.
    - Det finnes en enkelt kodebase der ny funksjonalitet for Human Resources lanseres som en del av den vanlige oppdateringsprosessen for én versjon.
    - Måten oppgraderinger, oppdateringer og hurtigreparasjoner brukes i miljøer på, er konsekvent.

- [Alternativer for utvidbarhet er forbedret.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Du kan fortsette å bruke Microsoft Power Platform-verktøy til å utvide etter behov.
    - Du kan utvide funksjonalitet via skjemaer, tabeller, metoder og API-er.
    - Du kan opprette og utvide enheter.

    Hvis du vil ha mer informasjon om tilgjengelige utvidelsesalternativer, kan du se [Oversikt over utvidelse i Dynamics 365](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Opprett ett sett med personalfunksjoner i Dynamics 365.](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    I 10.0.25-versjonen er funksjonelle egenskaper som bare fantes i Human Resources, blitt gjort tilgjengelige i Finance and Operations-infrastrukturen. For at kundene skal kunne dra nytte av disse funksjonene i et Finance and Operations-miljø, må følgende Human Resources-funksjoner være aktivert i Funksjonsbehandling:

    | Funksjonsnavn | Oversikt | Frigivelsesstatus | 
    |--------------|----------|----------------| 
    | Beregning av arbeidserfaring | Ved hjelp av et oppsettalternativ kan du velge datoen som skal brukes for beregningen av **Arbeidserfaring**. | Generelt tilgjengelig | 
    | Forbedringer for arbeidsflytopplevelse | Denne funksjonen gir en utvidet brukeropplevelse for arbeidsflytinnsendinger og -godkjenninger. | Generelt tilgjengelig | 
    | Skriv ut ytelsesvurderinger | Du kan skrive ut prestasjonsvurderinger i PDF-format. | Generelt tilgjengelig | 
    | Egendefinerte koblinger i **Lederselvbetjening** | Du kan opprette egendefinerte koblinger som vises i delen **Beslektede koblinger** i **Lederselvbetjening**. | Generelt tilgjengelig | 
    | Visning av kompensasjon på tvers av firmaer | Brukere kan vise kompensasjonsplaner i **Lederselvbetjening** på tvers av alle juridiske enheter, uten å måtte bytte firmaer. | Generelt tilgjengelig | 
    | Konfigurer flere kompensasjonsnivåer etter jobb\*&dagger; | Jobber støtter nå flere kompensasjonsnivåer. | Forhåndsversjon | 
    | Oppgavebehandling\* | Du kan opprette sjekklister og oppgaver for pålasting, avlasting og overgangsprosessen. | Forhåndsversjon | 
    | Strømlinjeformet ansattpost | Denne funksjonen gir en oppdatert brukeropplevelse på den eksisterende **Arbeider**-siden. | Forhåndsversjon | 
    | Forbedringer av brukeropplevelsen for personale | Se tabellen i neste del.  | Forhåndsversjon | 

\* Denne funksjonen må være aktivert før funksjonen **Forbedringer av brukeropplevelsen i Human Resources**.

&dagger; Denne funksjonen kan ikke deaktiveres etter at den er aktivert.

## <a name="human-resource-user-experience-enhancements"></a>Forbedringer av brukeropplevelsen i Human Resouces

| Funksjonsnavn | Oversikt | 
|--------------|----------| 
| Slett ansettelse | Du kan slette en ansettelse for en ansatt. | 
| Jobbserier | Du kan spore en gruppe jobber som omfatter lignende arbeid, og som krever lignende opplæring, kunnskap, kompetanse og ekspertise. | 
| Flere ansettelsesfelt | Følgende felter ble lagt til: **Ansettelseskategori**, **Ansettelsestype** og **Ansettelsesstatus**. | 
| Siden **Arbeidere uten ansettelse** | En side viser en liste over arbeidere som ikke har en ansettelsespost. | 
| Oppdater brukeropplevelse for stillingsdimensjon | Det er en utvidet brukeropplevelse for tilordning av stillingsdimensjoner per juridisk enhet. | 
| Adresseendringer i arbeidsområdet **Personaladministrasjon** | Denne funksjonen gir en telling av alle adresseendringene som skjedde i løpet av et angitt antall dager, som definert på siden **Human Resources-parametere**. | 
| Utløpende poster i arbeidsområdet **Personaladministrasjon** | Denne funksjonen gir en liste over varer som er utløpt eller utløper for sertifikater, identifikasjoner, prøveperioder, screeninger eller tester. | 
| Siden **Validering av stillingshierarki** | Det utføres en kontroll av sirkelreferanser i stillingslinjehierarkiet. | 
| Landspesifikk lønnsinformasjon | Flere lønnsfelter er tilgjengelige på siden **Ansettelse**, avhengig av landet eller regionen for den juridiske enheten der arbeideren er ansatt. | 
| Utvidelser i samsvarsrapportering | Flere rapporteringsalternativer er tilgjengelige for EEO-1, Vets 4212 og OSHA300a. | 
| Oppdateringer i arbeidsområdet **Personaladministrasjon** | Oppdateringer er utført for å spore adresseendringer og utløpende poster. I tillegg viser nye faner arbeider- og stillingshandlinger. | 
