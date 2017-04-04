---
title: "Administrere brukere av leverandørsamarbeid"
description: "Dette emnet beskriver hvordan du kan be om klargjøring av nye brukere for leverandørsamarbeid og hvordan du legger til nye kontakter for leverandørsamarbeid."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 380f1bcdf7109dc12fd898199033eac7710d863c
ms.lasthandoff: 03/31/2017


---

# <a name="manage-vendor-collaboration-users"></a>Administrere brukere av leverandørsamarbeid

Dette emnet beskriver hvordan du kan be om klargjøring av nye brukere for leverandørsamarbeid og hvordan du legger til nye kontakter for leverandørsamarbeid. 

Grensesnittet for leverandørsamarbeid i Microsoft Dynamics 365 for Operations viser informasjon om bestillinger, fakturaer og forsendelseslager til eksterne leverandører. Du kan opprette nye kontakter for leverandørsamarbeid og be om at nye brukere skal klargjøres hvis du arbeider med som en ekstern leverandør med sikkerhetsrollen **Leverandøradministrasjon (ekstern)** eller lignende tillatelser. Du kan også utføre disse oppgavene, hvis du arbeider som innkjøpsansvarlig. I dette emnet refererer denne rollen til en innkjøpsansvarlig som arbeider i firmaet som eier forekomsten av Dynamics 365 for Operations. Hvis du vil ha mer informasjon om hvordan du bruker samarbeid med leverandøren hvis du er en ekstern leverandør, kan du se [leverandør med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Hvis du vil ha mer informasjon om hvordan du bruker samarbeid med leverandøren hvis du er en profesjonell innkjøp, se [leverandøren samarbeid til med eksterne leverandører,](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Legge til nye kontakter for leverandørsamarbeid
Hvis du vil at noen skal ha tilgang til leverandørsamarbeid, må de først legges til som en kontakt for leverandørsamarbeid. Du kan også legge til kontakter for ansatte i firmaet som ikke bruker leverandørsamarbeid. De kan for eksempel være kontakten for andre typer innkjøpsinformasjon. Nye kontakter blir lagt til på den **alle kontakter** side, som er tilgjengelig fra den **leverandøren samarbeid**&gt;**kontakter** menyen. Slik legger du til en ny kontakt:

1.  Klikk **Ny**.
2.  Angi informasjon om kontaktpersonen.
3.  Velg hvilken juridisk enhet de representerer i firmaet, og hvilken juridisk enhet de skal jobbe med i firmaet som de skal samarbeide med. Dette gjør du ved å velge en **juridisk enhet i firmaet**/**juridisk enhet i kundeselskapet** par.
4.  Klikk **Opprett**.

Hvis du vil slette en kontakt, er det bare mulig å slette de du har opprettet.

## <a name="vendor-collaboration-user-requests"></a>Brukerforespørsler for leverandørsamarbeid
Brukerforespørsler for leverandørsamarbeid opprettes av innkjøpsansvarlig eller en ekstern leverandøradministrator.

-   Hvis du er en ekstern leverandør, kan du sende forespørsler fra den **alle kontakter** side i den **leverandøren samarbeid** modul.
-   Hvis du er innkjøpsansvarlig, kan du sende forespørsler fra siden **Vis kontakter**. Du gjør dette, på leverandørposten, i den **oppsett** -delen i handlingsruten, velger **kontakter**&gt;**vise kontakter**.

Du kan opprette en forespørsel om å klargjøre en bruker, deaktivere en bruker eller endre sikkerhetsroller. Hvis du er ekstern leverandøradministrator, må du være registrert som kontaktperson for leverandørkontoer som du vil opprette brukerforespørsler for, og du må ha tilgang til grensesnittet for leverandørsamarbeid for disse leverandørkontoene.  

Når en forespørsel sendes inn, legges den til i listen **Brukerforespørsler for leverandørsamarbeid** i modulen **Leverandørsamarbeid** og i listen**Brukerforespørsel for leverandørsamarbeid** i modulen **Innkjøp og leverandører** (modulen Innkjøp og leverandører er ikke er tilgjengelig for eksterne brukere).

### <a name="provision-a-user"></a>Klargjøre en bruker

Før du kan be om at en ny bruker klargjøres, må vedkommende defineres som en kontakt for én eller flere leverandørkontoer. Slik oppretter du en forespørsel for en ny bruker for leverandørsamarbeid:

1.  På den **alle kontakter** klikker du **Klargjør leverandørbruker**.
2.  Angi en e-postadresse for brukeren. Denne adressen brukes av brukeren for å logge på Dynamics 365 for Operations. Hvis e-postadressen tilhører et domene som er registrert som en leier i Microsoft Azure, må e-postadressen være en eksisterende Azure Active Directory-konto (ADD) for at klargjøringsprosessen skal fullføres. Hvis e-postadressen ikke tilhører et domene som er registrert i Microsoft Azure, opprettes en ADD-konto som en del av klargjøringsprosessen, og den nye brukeren mottar en e-postinvitasjon. Forbruker e-post adresser med domener som @hotmail.com, @gmail.com, eller @comcast.netkan ikke brukes til å registrere en Dynamics 365 for operasjoner bruker.
3.  Sett alternativet **Tilgang til leverandørsamarbeid tillatt** til **Ja** for alle de juridiske enhetene som brukeren må ha tilgang til.
4.  I delen **Tilordne brukerroller** merker du av for **Tilordne** for sikkerhetsrollene som den nye brukeren skal ha.
5.  Klikk **Send**.

Når leverandøren brukerforespørselen er sendt, den **leverandøren samarbeidstilgang tillatt** -feltet er satt til **Ja** for den valgte leverandørkontoen og en bruker ber om arbeidsflyten er startet. Som en del av arbeidsflyten opprettes en ny bruker i Dynamics 365 for Operations, og sikkerhetsroller tilordnes. I tillegg aktiveres en Azure B2B-tjeneste som starter samhandling med Azure-portalen og knytter en ny eller eksisterende AAD-konto til brukerkontoen for Dynamics 365 for Operations.

### <a name="inactivate-a-user"></a>Deaktivere en bruker

Det finnes to metoder for å fjerne tilgangen til leverandørsamarbeid for en bruker:

-   På **Kontakter**-siden for leverandøren setter du alternativet **Tilgang til leverandørsamarbeid tillatt** til **Nei** for kontakten. Dette kan gjøres individuelt per juridisk enhet som personen er kontakt for. Dette alternativet kan bare brukes av innkjøpsansvarlige.
-   Deaktiver hele brukerkontoen ved å sende inn en forespørsel om **deaktivering av leverandørbruker**.

Be om at en bruker er deaktivert:

1.  På den **alle kontakter** klikker du **Deaktiver****leverandørbruker**.
2.  Skriv inn en kommentar i feltet **Bestillingsårsak**.
3.  Klikk **Send**.

### <a name="modify-security-roles"></a>Endre sikkerhetsroller

Den **Vedlikehold leverandør brukerroller** siden er den samme som den **Klargjør leverandørbruker** siden bortsett fra at du kan redigere listen over sikkerhetsroller.  

Be om at sikkerhetsrollene endres for en bruker:

1.  På den **alle kontakter** klikker du **Behold****leverandøren brukerroller**.
2.  Skriv inn en kommentar i feltet **Bestillingsårsak**.
3.  I delen **Vedlikehold brukerroller** velger du sikkerhetsrollene som du vil tilordne, eller fjerner dem du vil fjerne.
4.  Klikk **Send**.



