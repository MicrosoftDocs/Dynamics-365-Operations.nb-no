---
title: Rediger personlige opplysninger
description: Denne artikkelen beskriver hvordan du redigerer personlige opplysninger i selvbetjening for ansatte og ledere.
author: andreabichsel
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2170d3b8c476fb82786721512013eae45bb78ce5
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052151"
---
# <a name="edit-personal-information"></a>Rediger personlige opplysninger

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan redigere de personlige opplysningene i Dynamics 365 Human Resources i **arbeidsområdet Ansattselvbetjening**.

De personlige opplysningene du kan redigere, omfatter følgende:

- Adresser
- Kontaktdetaljer
- Personlige kontakter
- Identifikasjonsnumre
- Betalingsmetode
- Bilde som brukes i Human Resources

>[!NOTE]
>Det er ikke sikkert du kan redigere bestemte typer personlige opplysninger, for eksempel forretningskontaktdetaljer. Hvis du vil ha mer informasjon, kan du se [Begrense redigering av personlige opplysninger](hr-employee-self-service-restrict-editing.md).

Parametere angitt i den globale adresseboken bestemmer hvilke roller som kan se dine personlige opplysninger.

1. Velg **Ansattselvbetjening** i Human Resources.

2. Velg **Rediger personlig informasjon**.

3. Hvis du vil endre adressen din, velger du kategorien **Adresser**. Endringer du utfører, vises i arbeidsområdet **Personaladministrasjon** for varsling av HR.

    - Velg **Legg til** for å legge til en ny adresse.
    - Hvis du vil redigere en eksisterende adresse, merker du adressen og velger **Rediger**.
    - Hvis du vil vise et kart, velger du **Kart**.
    - Hvis du vil legge til eller fjerne en kontakt, velger du **Flere alternativer** og velger deretter **Avansert**. Under **Kontaktinformasjon** velger du **Legg til** eller **Fjern** og redigerer feltene etter behov.
    - Hvis du vil angi tidssone og sted, velger du **Flere alternativer** og velger deretter **Avansert**. Rediger feltene etter behov under **Generelt**.

4. Hvis du vil endre kontaktopplysninger, velger du **Kontaktdetaljer**. Du kan tilby ulike typer kontaktinformasjon, inkludert telefon, e-post og koblinger til sosiale medier. Du kan angi en kontaktdetalj som primær, men du kan bare angi én av hver type som primær.

    - Velg **Legg til** for å legge til en ny kontaktinformasjon. Rediger feltene etter behov.
    - Hvis du vil redigere eksisterende kontaktinformasjon, merker du elementet og velger **Rediger**. Rediger feltene etter behov.
    - Hvis du vil angi en kontaktdetalj som privat, velger du elementet, velger **Avansert**, og setter deretter **Privat**-veksleknappen til **Ja**. Velg **OK**.
      >[!NOTE]
      >Knappen **Avansert** er ikke tilgjengelig hvis administratoren har aktivert funksjonen **(Forhåndsversjon) Hindre ansatte i å legge til eller redigere adresse- og kontaktinformasjon for utvalgte formål** i miljøet ditt. Hvis du vil ha mer informasjon, kan du se [Begrense redigering av personlige opplysninger](hr-employee-self-service-restrict-editing.md).
  
5. Hvis du vil endre personlige kontakter, velger du kategorien **Personlige kontakter**. Du kan angi krisekontakter, mottakere og avhengige. En kontakt kan være en person eller en organisasjon. Funksjonen **Fordelsbehandling** bruker personlig kontaktinformasjon. Hvis du vil ha mer informasjon, kan du se [Konfigurere alternativer for personlige kontaktrettigheter](hr-benefits-setup-contact-eligibility-options.md).

6. Hvis du vil endre identifikasjonsnumrene, for eksempel personnummer, velger du kategorien **Identifikasjonsnumre**. Endringer kan gå gjennom en godkjenningsprosess hvis organisasjonen din har satt opp en godkjenningsarbeidsflyt.

    - Hvis du vil legge til et identifikasjonsnummer, velger du **Ny**. Fyll ut feltene etter behov, og velg **Lagre**.
    - Hvis du vil redigere et nummer, velger du **Rediger**. Rediger feltene etter behov, og velg **Lagre**.

7. Hvis du vil endre metodene du blir betalt med, velger du kategorien **Min betalingsinformasjon**. Denne kategorien er bare tilgjengelig hvis betalingsmåter er aktivert i skjemaet **Personalparametere**. Personale kan aktivere **Bankoverføring**, **Kasse**, **Sjekk**, **Elektronisk betaling** eller **Annet**. Personale kan også deaktivere validering av elektronisk betaling (brukt for amerikanske lønn), og validering av bankkonto- og registreringsnummer.

8. Hvis du vil endre bildet som vises i Human Resources for profilen din, velger du kategorien **Bilde**. Avhengig av organisasjonens innstillinger kan det hende at bilder rutes for godkjenning.

    - Hvis du vil laste opp et bilde, velger du **Last opp nytt bilde**.
    - Hvis du vil fjerne et bilde, merker du bildet og velger **Fjern**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]