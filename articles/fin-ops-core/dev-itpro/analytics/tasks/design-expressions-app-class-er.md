---
title: Utforme ER-uttrykk for å kalle programklassemetoder
description: Dette emnet beskriver hvordan du bruker den eksisterende programlogikken i konfigurasjoner for elektronisk rapportering på nytt ved å kalle opp nødvendige metoder for programklasser.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11b4d185703731d8491ad10bdeedea40ce811f5d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564100"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Utforme ER-uttrykk for å kalle programklassemetoder

[!include [banner](../../includes/banner.md)]

Denne veiledningen gir informasjon om hvordan du bruker den eksisterende programlogikken i elektronisk rapportering (ER)-konfigurasjoner på nytt ved å kalle nødvendige metoder for programklasser i ER-uttrykk. Verdier for argumenter for kallklasser kan defineres dynamisk under kjøring: for eksempel basert på informasjon i analysedokumentet for å sikre nøyaktighet. I denne veiledningen skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet, Litware, Inc. Denne fremgangsmåten er opprettet for brukere som har tilordnet rollen som Systemansvarlig eller Utvikler av elektronisk rapportering. 

Disse trinnene kan fullføres ved hjelp av hvilket som helst datasett. Du må også laste ned og lagre følgende fil lokalt: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "ER Opprette en konfigurasjonsleverandør og merke den som aktiv.

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Kontroller at konfigurasjonsleverandøren for eksempelfirma Litware, Inc. er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".   
    * Du utformer en prosess for å analysere innkommende bankkontoutdrag for en oppdatering av programdata. Du vil motta innkommende bankkontoutdrag som TXT-filer som inneholder IBAN-koder. Som en del av importprosessen for bankkontoutdrag må du validere riktigheten av disse IBAN-kodene ved hjelp av logikken som allerede finnes.   

## <a name="import-a-new-er-model-configuration"></a>Importere en ny ER-konfigurasjon
1. Finn og velg ønsket post i listen.
    * Velg flisen Microsoft-leverandør.  
2. Klikk på Repositorier.
3. Klikk på Vis filtre.
4. Legg til et "Typenavn"-filterfelt. I Navn-feltet angir du verdien "ressurser", velger "inneholder"-filteroperatoren og klikker på Bruk.
5. Klikk på Åpne.
6. Velg Betalingsmodell i treet.
    * Hvis Importer-knappen på hurtigfanen Versjoner ikke er aktivert, har du allerede importert versjon 1 av ER-konfigurasjonen "Betalingsmodell". Du kan hoppe over resten trinnene i denne underoppgaven.   
7. Klikk på Importer.
8. Klikk på Ja.
9. Lukk siden.
10. Lukk siden.

## <a name="add-a-new-er-format-configuration"></a>Legg til en ny ER-formatkonfigurasjon
1. Klikk på Rapporteringskonfigurasjoner.
    * Legg til et nytt ER-format for å analysere innkommende bankkontoutdrag i TXT-format.  
2. Velg Betalingsmodell i treet.
3. Klikk på Opprett konfigurasjon for å åpne dialogmenyen.
4. I feltet Ny angir du Format basert på datamodell PaymentModel.
5. Skriv inn 'Importformat for bankkontoutdrag (eksempel)' i Navn-feltet.
    * Importformat for bankkontoutdrag (eksempel)  
6. Velg Ja i feltet Støtter dataimport.
7. Klikk på Opprett konfigurasjon.

## <a name="design-the-er-format-configuration---format"></a>Utforme ER-formatkonfigurasjonen – format
1. Klikk på Utforming.
    * Det utformede formatet representerer den forventet strukturen for den eksterne filen i TXT-format.  
2. Klikk på Legg til rot for å åpne dialogmenyen.
3. Velg Tekst\Sekvens i treet.
4. Skriv inn Rot i Navn-feltet.
    * Rot  
5. Velg Ny linje - Windows (CR LF) i Spesialtegn-feltet.
    * Alternativet Ny linje - Windows (CR LF) er valgt i Spesialtegn-feltet. Basert på denne innstillingen, betraktes hver linje i analysefilen som en egen oppføring.  
6. Klikk på OK.
7. Klikk på Legg til for å åpne nedtrekksdialogen.
8. Velg Tekst\Sekvens i treet.
9. I Navn-feltet skriver du inn Rader.
    * Rader  
10. Velg "Én mange" i feltet Multiplisitet.
    * Alternativet Én mange er valgt i feltet Multiplisitet. Basert på denne innstillingen, forventes det at minst én linje vises i analysefilen.  
11. Klikk på OK.
12. Velg Rot\Rader i treet.
13. Klikk på Legg sekvens.
14. I Navn-feltet skriver du inn Felt.
    * Felt  
15. Velg "Nøyaktig én" i feltet Multiplisitet.
16. Klikk på OK.
17. I treet velger du Rot\Rader\Felt.
18. Klikk på Legg til for å åpne nedtrekksdialogen.
19. Velg Tekst\Streng i treet.
20. I Navn-feltet skriver du IBAN.
    * IBAN  
21. Klikk på OK.
    * Det er konfigurert at hver linje i analysefilen inneholder den eneste IBAN-koden.  
22. Klikk på Lagre.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>Utforme ER-formatkonfigurasjonen – tilordne til datamodell
1. Klikk på Tilordne format til modell.
2. Klikk på Ny.
3. I Definisjon-feltet skriver du inn BankToCustomerDebitCreditNotificationInitiation.
    * BankToCustomerDebitCreditNotificationInitiation  
4. ResolveChanges definisjonen.
5. Skriv inn Tilordning til datamodell i Navn-feltet.
    * Tilordning til datamodell  
6. Klikk på Lagre.
7. Klikk på Utforming.
8. Velg Dynamics 365 for Operations\Klasse i treet.
9. Klikk på Legg til rot.
    * Legg til en ny datakilde for å kalle den eksisterende programlogikken for validering av IBAN-koder.  
10. I Navn-feltet skriver du inn check_codes.
    * check_codes  
11. Skriv inn ISO7064 i feltet Klasse.
    * ISO7064  
12. Klikk på OK.
13. Utvid 'format' i treet.
14. Utvid 'format\Rot: Sequence(Root) i treet.
15. I treet velger du "format\Rot: Sequence(Root)\Rader: Sekvens 1..* (Rader)'.
16. Klikk på Bind.
17. I treet utvider du "format\Rot: Sequence(Root)\Rader: Sekvens 1..* (Rader)'.
18. Utvid format\Rot: Sequence(Root)\Rader: Sekvens 1..* (Rader)\Felt: Sekvens 1..1 (Felt)" i treet.
19. Velg format\Rot: Sequence(Root)\Rader: Sekvens 1..* (Rader)\Felt: Sekvens 1..1 (Felt)\IBAN: String(IBAN) i treet.
20. Utvid Betalinger = format.Root.Rows i treet.
21. Utvid Betalinger = format.Root.Rows\Creditor Account(CreditorAccount) i treet.
22. Utvid Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identification i treet.
23. Velg Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN i treet.
24. Klikk på Bind.
25. Klikk på fanen Valideringer.
26. Klikk på Ny.
    * Legg til en ny valideringsregel som viser en feil for alle linjer i analysefilen som inneholder ugyldig IBAN-kode.  
27. Klikk på Rediger betingelse.
28. Utvid check_codes i treet.
29. Velg check_codes\verifyMOD1271_36.
30. Klikk på Legg til datakilde.
31. I Formel-feltet skriver du inn 'check_codes.verifyMOD1271_36('.
    * check_codes.verifyMOD1271_36(  
32. Utvid 'format' i treet.
33. Utvid 'format\Rot: Sequence(Root) i treet.
34. I treet utvider du "format\Rot: Sequence(Root)\Rader: Sekvens 1..* (Rader)'.
35. Utvid format\Rot: Sequence(Root)\Rader: Sekvens 1..* (Rader)\Felt: Sekvens 1..1 (Felt)" i treet.
36. Velg format\Rot: Sequence(Root)\Rader: Sekvens 1..* (Rader)\Felt: Sekvens 1..1 (Felt)\IBAN: String(IBAN) i treet.
37. Klikk på Legg til datakilde.
38. I Formel-feltet skriver du inn 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Klikk på Lagre.
40. Lukk siden.
    * Valideringsbetingelsen er konfigurert til å returnere FALSE for en ugyldig IBAN-kode ved å kalle den eksisterende metoden "verifyMOD1271_36" i programklassen "ISO7064". Legg merke til at verdien til IBAN-koden defineres dynamisk under kjøring som argumentet for kallmetoden basert på innholdet i TXT-filen for analyse.   
41. Klikk på Rediger melding.
42. Angi 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)' i Formel-feltet.
    * CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)  
43. Klikk på Lagre.
44. Lukk siden.
45. Klikk på Lagre.
46. Lukk siden.

## <a name="run-the-format-mapping"></a>Kjøre formattilordningen
For testformål kan du utføre formattilordningen med filen SampleIncomingMessage.txt som du lastet ned. De genererte utdataene omfatter informasjon som importeres fra den valgte TXT-filen og fylles ut i den egendefinerte datamodellen under den reelle importen.   
1. Klikk på Kjør.
    * Klikk på Bla gjennom og gå til SampleIncomingMessage.txt-filen som du lastet ned tidligere.  
2. Klikk på OK.
    * Gå gjennom utdataene i XML-format, som representerer dataene som er importert fra den valgte filen og overført til datamodellen. Vær oppmerksom på at bare 3 linjer i den importerte TXT-filen ble behandlet. IBAN-koden på linje 4 som ikke er gyldig, ble hoppet over, og en feilmelding gis i infologgen.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]