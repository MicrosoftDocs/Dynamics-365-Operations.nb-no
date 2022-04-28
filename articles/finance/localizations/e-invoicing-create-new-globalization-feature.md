---
title: Opprette en globaliseringsfunksjon
description: Dette emnet forklarer hvordan du oppretter globaliseringsfunksjon.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 94038b0eb412632c348081bbf467f44310d9e955
ms.sourcegitcommit: 6109fc2fe5f407363bb6f240d64b7214657f5914
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/15/2022
ms.locfileid: "8603032"
---
# <a name="create-a-globalization-feature"></a>Opprette en globaliseringsfunksjon

[!include [banner](../includes/banner.md)]

Du kan opprette en funksjon for elektronisk fakturering fra grunnen av, eller du kan basere den på en eksisterende funksjon. Når du oppretter en funksjon fra grunnen av, må du legge til konfigurasjoner for elektronisk rapportering (ER) og andre komponenter manuelt, for eksempel detaljene for funksjonsoppsett og programoppsett. Når du oppretter en funksjon som er basert på en eksisterende funksjon, arver den nye funksjonen alle konfigurasjonene og parameterne for basisfunksjonen. Du kan gå gjennom det som kopieres fra basisfunksjonen til den nye funksjonen.

## <a name="create-a-feature-from-scratch"></a>Opprette en funksjon fra grunnen av

Denne delen forklarer hvordan du oppretter en funksjon for elektronisk fakturering når ingen globaliseringsfunksjon er bruksklart tilgjengelig i det globale repositoriet for forretningsscenarioene.

Følg disse trinnene for å opprette en funksjon for elektronisk fakturering.

1. Logg deg på kontoen for Regulatory Configuration Service (RCS).
2. I arbeidsområdet **Globaliseringsfunksjon**, i **Funksjoner**-delen velger du flisen **Elektronisk fakturering**.
3. Velg **Legg til**, og velg deretter alternativet **Ny funksjon** i rullegardinboksen.
4. Angi et navn og en beskrivelse for funksjonen for elektronisk fakturering.
5. Velg **Opprett funksjon**. Den første versjonen av den nye funksjonen vises til høyre på siden og har statusen **Utkast**.

    Du må deretter legge til ER-konfigurasjoner og funksjonsoppsett. Før du legger til nye eller eksisterende ER-formatkonfigurasjoner, må du kontrollere at de finnes i det lokale RCS-repositoriet.

6. Velg funksjonen for elektronisk fakturering som du arbeider med.
7. I **Konfigurasjoner**-fanen velger du **Legg til**.
8. I rutenettet **Konfigurasjoner** blar du til og velger formatkonfigurasjonene som kreves for datasamlebåndet for behandling (for eksempel for å generere elektroniske fakturafiler eller behandle svar fra eksterne nettjenester).
9. Velg **OK**. Du kan nå bruke konfigurasjonene i handlinger i datasamlebåndet for behandling. Hvis du vil ha mer informasjon, kan du se [Arbeide med konfigurasjoner](e-invoicing-work-configurations.md).
10. Du kan legge til et funksjonsoppsett for elektronisk fakturering ved å opprette det i **Oppsett**-fanen på siden **Ny funksjon**. Hvis du vil ha mer informasjon, kan du se [Arbeide med funksjonsoppsett](e-invoicing-feature-setup.md).
11. Fullfør oppsettet, og rull ut funksjonen for elektronisk fakturering til tjenestemiljøet. Hvis du vil ha mer informasjon, kan du se [Fullføre, publisere og rulle ut en globaliseringsfunksjon](e-invoicing-complete-publish-deploy-globalization-feature.md).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Opprette filformatkonfigurasjoner som er avledet fra den eksisterende fakturamodellen

Du kan hoppe over denne delen hvis du ikke trenger å opprette ER-konfigurasjoner, men kan bruke eksisterende versjoner som basis.

Denne fremgangsmåten viser hvordan du oppretter filformatkonfigurasjonene som kreves for den nye funksjonen for elektronisk fakturering du vil opprette. Opprett filformatkonfigurasjonen for elektronisk faktura og alle andre filformatkonfigurasjoner som den nye funksjonen for elektronisk fakturering krever.

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.
3. Velg **Fakturamodell** eller **Regnskapsmodell** for brasilianske scenarioer.
4. Velg **Opprett konfigurasjon**, og velg deretter **Format basert på datamodellen Faktura** i rullegardinboksen.
5. Angi et navn og en beskrivelse for formatkonfigurasjonen.
6. Velg filutvidelsestypen i **Formattype**-feltet.
7. Velg rotstrukturen du vil tilordne formatet til, i feltet **Definisjon av datamodell**. For kundefakturaformater brukes for eksempel **InvoiceCustomer**.
8. Velg **Opprett konfigurasjon**.
9. Velge den nye formatkonfigurasjonen.
10. Velg **Utforming**, og bruk verktøyet for formatdesigner til å konfigurere filoppsettet slik at det oppfyller filformatspesifikasjonene.
11. Lukk siden.
12. I fanen **Versjoner** velger du **Endre status** \> **Fullfør**.
13. Velg **Endre status** \> **Del** for å publisere formatkonfigurasjonen i det globale repositoriet.

De nye filformatkonfigurasjonene må deles med Microsoft-domenet før de kan brukes av tjenesten for elektronisk fakturering.

1. Velg formatkonfigurasjonen du arbeider på. Statusen til konfigurasjonen må være **Delt**.
2. Velg **Avansert deling** \> **Globalt repositorium** i fanen **Versjoner**.
3. I fanen **Delt med** velger du **Organisasjon**.
4. I **Parametere**-feltet angir du **microsoft.com** for å dele formatkonfigurasjonen med Microsoft-domenet.
5. Velg **OK**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Opprette en funksjon som er basert på en eksisterende funksjon

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Globaliseringsfunksjon**, i **Funksjoner**-delen velger du flisen **Elektronisk fakturering**.
3. Kontroller at den aktive konfigurasjonsleverandøren er valgt i feltet **Konfigurasjonsleverandør**. Dermed vises den nye funksjonen for elektronisk fakturering i listen etter at den er opprettet. Hvis du ikke har valgt den aktive konfigurasjonsleverandøren, filtreres den nye funksjonen ut av listen.
4. Velg **Legg til**, og merk deretter av for **Basert på eksisterende versjon** i rullegardinmenyen i dialogboksen.
5. Angi et navn og en beskrivelse for funksjonen.
6. Velg basisversjonen av funksjonen i feltet **Basisfunksjon**.
7. Velg **Opprett funksjon**. Funksjonen opprettes og har statusen **Utkast**.
8. Gå gjennom funksjonskomponentene for å finne ut om oppdateringer kreves:

    - Gå gjennom konfigurasjonene i tilfelle du må tilpasse ER-formatene og bindingen deres til formattilordninger for funksjonsversjonen.
    - Gå gjennom oppsettet i tilfelle du må tilpasse **Handlinger**-fanen, **Relevansregler**-fanen eller **Variabler**-fanen for funksjonsversjonen.

9. Fullfør oppsettet, og rull ut funksjonen for elektronisk fakturering til tjenestemiljøet. Hvis du vil ha mer informasjon, kan du se [Fullføre, publisere og rulle ut en globaliseringsfunksjon](e-invoicing-complete-publish-deploy-globalization-feature.md).
