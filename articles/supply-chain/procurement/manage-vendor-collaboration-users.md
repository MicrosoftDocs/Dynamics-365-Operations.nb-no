---
title: Administrere brukere av leverandørsamarbeid
description: Dette emnet beskriver hvordan du kan be om klargjøring av nye brukere for leverandørsamarbeid og hvordan du legger til nye kontakter for leverandørsamarbeid.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 520dcaa1eec3c0fb8aa72fc7f75a56622069881f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555067"
---
# <a name="manage-vendor-collaboration-users"></a>Administrere brukere av leverandørsamarbeid

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kan be om klargjøring av nye brukere for leverandørsamarbeid og hvordan du legger til nye kontakter for leverandørsamarbeid. 

Grensesnittet for leverandørsamarbeid i Microsoft Dynamics 365 for Finance and Operations viser informasjon om bestillinger, fakturaer og forsendelseslager til eksterne leverandører. Du kan opprette nye kontakter for leverandørsamarbeid og be om at nye brukere skal klargjøres hvis du arbeider med som en ekstern leverandør med sikkerhetsrollen **Leverandøradministrasjon (ekstern)** eller lignende tillatelser. Du kan også utføre disse oppgavene, hvis du arbeider som innkjøpsansvarlig. I dette emnet refererer denne rollen til en innkjøpsansvarlig som arbeider i firmaet som eier forekomsten av Finance and Operations. Hvis du vil ha mer informasjon om hvordan du bruker samarbeid med leverandøren hvis du er en ekstern leverandør, kan du se [leverandør med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Hvis du vil ha mer informasjon om hvordan du bruker samarbeid med leverandøren hvis du er en innkjøpsansvarlig, kan du se [Leverandørsamarbeid med eksterne leverandører](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Legge til nye kontakter for leverandørsamarbeid
Hvis du vil at noen skal ha tilgang til leverandørsamarbeid, må de først legges til som en kontakt for leverandørsamarbeid. Du kan også legge til kontakter for ansatte i firmaet som ikke bruker leverandørsamarbeid. De kan for eksempel være kontakten for andre typer innkjøpsinformasjon. Nye kontakter legges til på siden **Alle kontakter**, som åpnes fra menyen **Leverandørsamarbeid** &gt; **Kontakter**. Slik legger du til en ny kontakt:

1.  Klikk **Ny**.
2.  Angi informasjon om kontaktpersonen.
3.  Velg hvilken juridisk enhet de representerer i firmaet, og hvilken juridisk enhet de skal jobbe med i firmaet som de skal samarbeide med. Dette gjør du ved å velge et par av **Juridisk enhet i mitt firma** / **Juridisk enhet i kundefirma**.
4.  Klikk **Opprett**.

Hvis du vil slette en kontakt, er det bare mulig å slette de du har opprettet.

## <a name="vendor-collaboration-user-requests"></a>Brukerforespørsler for leverandørsamarbeid
Brukerforespørsler for leverandørsamarbeid opprettes av innkjøpsansvarlig eller en ekstern leverandøradministrator.

-   Hvis du er en ekstern leverandør, kan du sende forespørsler fra siden **Alle kontakter** i modulen **Leverandørsamarbeid**.
-   Hvis du er innkjøpsansvarlig, kan du sende forespørsler fra siden **Vis kontakter**. Hvis du vil gjøre dette, går du til **Oppsett**-delen i handlingsruten i en leverandørpost, velger **Kontakter** &gt; **Vis kontakter**.

Du kan opprette en forespørsel om å klargjøre en bruker, deaktivere en bruker eller endre sikkerhetsroller. Hvis du er ekstern leverandøradministrator, må du være registrert som kontaktperson for leverandørkontoer som du vil opprette brukerforespørsler for, og du må ha tilgang til grensesnittet for leverandørsamarbeid for disse leverandørkontoene.  

Når en forespørsel sendes inn, legges den til i listen **Brukerforespørsler for leverandørsamarbeid** i modulen **Leverandørsamarbeid** og i listen **Brukerforespørsel for leverandørsamarbeid** i modulen **Innkjøp og leverandører** (modulen Innkjøp og leverandører er ikke er tilgjengelig for eksterne brukere).

### <a name="provision-a-user"></a>Klargjøre en bruker

Før du kan be om at en ny bruker klargjøres, må vedkommende defineres som en kontakt for én eller flere leverandørkontoer. Slik oppretter du en forespørsel for en ny bruker for leverandørsamarbeid:

1. På siden **Alle kontakter** klikker du **Klargjør leverandørbruker**.
2. Angi en e-postadresse for brukeren. Denne adressen brukes av brukeren for å logge på Finance and Operations. Hvis e-postadressen tilhører et domene som er registrert som en leier i Microsoft Azure, må e-postadressen være en eksisterende Azure Active Directory-konto (AAD) for at klargjøringsprosessen skal fullføres. Hvis e-postadressen ikke tilhører et domene som er registrert i Microsoft Azure, opprettes en AAD-konto som en del av klargjøringsprosessen, og den nye brukeren mottar en e-postinvitasjon. E-postadresser for forbrukere med domener som @hotmail.com, @gmail.com eller @comcast.net, kan brukes for å registrere en bruker for Finance and Operations.
3. Sett alternativet **Tilgang til leverandørsamarbeid tillatt** til **Ja** for alle de juridiske enhetene som brukeren må ha tilgang til.
4. I delen **Tilordne brukerroller** merker du av for **Tilordne** for sikkerhetsrollene som den nye brukeren skal ha.
5. Klikk **Send**.

Når brukerforespørselen for leverandør sendes inn, settes feltet **Tilgang til leverandørsamarbeid tillatt** til **Ja** for den valgte leverandørkontoen, og en arbeidsflyt for brukerforespørsel startes. Som en del av arbeidsflyten opprettes en ny bruker i Finance and Operations, og sikkerhetsroller tilordnes. I tillegg aktiveres en Azure B2B-tjeneste som starter samhandling med Azure-portalen og knytter en ny eller eksisterende AAD-konto til brukerkontoen for Finance and Operations. Hvis du vil ha mer informasjon, se [Hva er Azure AD B2B samarbeid?](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

### <a name="inactivate-a-user"></a>Deaktivere en bruker

Det finnes to metoder for å fjerne tilgangen til leverandørsamarbeid for en bruker:

-   På **Kontakter**-siden for leverandøren setter du alternativet **Tilgang til leverandørsamarbeid tillatt** til **Nei** for kontakten. Dette kan gjøres individuelt per juridisk enhet som personen er kontakt for. Dette alternativet kan bare brukes av innkjøpsansvarlige.
-   Deaktiver hele brukerkontoen ved å sende inn en forespørsel om **deaktivering av leverandørbruker**.

Slik ber du om at en bruker deaktiveres:

1.  På siden **Alle kontakter** klikker du **Deaktiver** **leverandørbruker**.
2.  Skriv inn en kommentar i feltet **Bestillingsårsak**.
3.  Klikk **Send**.

### <a name="modify-security-roles"></a>Endre sikkerhetsroller

Siden **Vedlikehold roller for leverandørbruker** er den samme som siden **Klargjør leverandørbruker** bortsett fra at du kan redigere listen over sikkerhetsroller.  

Slik ber du om at sikkerhetsrollene endres for en bruker:

1.  På siden **Alle kontakter** klikker du **Vedlikehold** **roller for leverandørbruker**.
2.  Skriv inn en kommentar i feltet **Bestillingsårsak**.
3.  I delen **Vedlikehold brukerroller** velger du sikkerhetsrollene som du vil tilordne, eller fjerner dem du vil fjerne.
4.  Klikk **Send**.




