---
title: ER Konfigurere mål
description: Denne fremgangsmåten beskriver hvordan du definerer og bruker forskjellige mål for utdatakomponenter for elektronisk rapportering (ER), for eksempel en mappe eller fil.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0fabf5c9475b5acd7cbd77a51c2912c96681894
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142645"
---
# <a name="er-configure-destinations"></a>ER Konfigurere mål

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du definerer og bruker forskjellige mål for utdatakomponenter for elektronisk rapportering (ER), for eksempel en mappe eller fil. Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren. Tyskland er landet\området for den juridiske enhetens primæradresse, men du kan bruke alle juridiske enheter for denne fremgangsmåten. 

Formatet som brukes i dette eksemplet er ISO20022 Kredittoverføring, men du kan bruke alle formater som du allerede har importert. Legg merke til at denne fremgangsmåten er et eksempel på en enkelt fil og et enkelt måloppsett. Du finner mer informasjon om administrasjon av mål for elektroniske rapportering i Hjelp for Dynamics 365 Finance.

1. Gå til Organisasjonsstyring > Elektronisk rapportering > Mål for elektroniske rapportering.
2. Klikk Ny for å opprette et nytt sett med mål for et format.
3. I feltet Referanse velger du et format som du vil konfigurere mål for.
    * Hvis du ikke har en verdi å velge, betyr det at du ikke har importert formatkonfigurasjoner for elektronisk rapportering. Du må importere en formatkonfigurasjonen før du definerer mål.  
4. Klikk Ny for å opprette et nytt filmål.
    * Vær oppmerksom på at du kan opprette ett filmål for hver utdatakomponent med samme format, for eksempel en mappe eller en fil. Du kan aktivere og deaktivere mål separat under innstillingene.  
5. I Navn-feltet angir du det brukervennlige navnet på komponenten for utdata.
    * Vi anbefaler at du bruker beskrivende navn, for eksempel "Betalingsfil" eller "Kontrollrapport". Disse navnene vil vises for brukeren under konfigurasjonen sammen med innstillingene for målet.  
6. I Filnavn velger du fil eller mappe som er spesifikk for formatet.
7. Klikk Innstillinger.
8. Velg Ja i feltet Aktivert.
    * Merket for Aktivert i hver kategori aktiverer og deaktiverer hvert mål separat. I dette eksemplet skal du aktivere sending av en utdatafil til en e-postmottaker når filen genereres.  
9. Klikk Rediger for å konfigurere e-postmottakere.
10. Klikk Legg til.
11. Klikk E-post for utskriftsbehandling.
12. Velg et alternativ i E-postkilde-feltet.
    * Du kan velge forskjellige e-postkildetyper, for eksempel en kunde eller en leverandør. Dette angir type argument som skal returneres av formelen for kildekonto for e-post. Formelen for kildekonto for e-post, som er beskrevet i fremgangsmåten nedenfor, er stedet der du binder en e-postkilde. Velg Leverandør hvis formelen skal returnere en leverandørkonto. Bruk Leverandør hvis du bruker konfigurasjonseksemplet ISO 20022 Kredittoverføring.  
13. Klikk Bind e-postkilde-knappen.
14. Angi en dokumentspesifikk referanse til en parttype du valgte tidligere, i formelen.
    * I stedet for å skrive inn kan du finne en datakildenode som representerer partskontoen, og klikke knappen Legg til datakilde for å oppdatere formelen. Hvis du for eksempel bruker konfigurasjonen ISO 20022 Kredittoverføring, er noden som representerer en leverandørkonto '$PaymentsForCoveringLetter'. Creditor.Identification.SourceID. Du kan eventuelt angi en hvilken som helst strengverdi, for eksempel "DE-001", for å lagre en formel.  
15. Klikk Lagre.
16. Lukk siden.
17. Velg Rediger for å konfigurere kontaktdetaljer for parten.
18. Velg Ja i feltet Hovedkontakt.
    * Du kan bruke forskjellige alternativer for å angi hvilken kontakttype for parten som skal brukes som e-postadresse for dette målet. Vi bruker en primærkontakt i dette eksemplet.  
19. Klikk OK.
20. Klikk OK.
21. Skriv inn en verdi i Emne-feltet.
22. Klikk OK.

