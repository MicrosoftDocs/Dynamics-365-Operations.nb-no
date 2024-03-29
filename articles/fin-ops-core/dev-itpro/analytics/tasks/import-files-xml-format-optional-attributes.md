---
title: (RCS) Importere filer i XML-format med valgfrie attributter
description: Denne artikkelen inneholder informasjon om hvordan en bruker kan utforme ER-formatkonfigurasjon for å importere filer i XML-format som inneholder valgfrie attributter.
author: kfend
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 5254a3d631129d0e41fcd37a341b54f97cfe6a9e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290012"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Importere filer i XML-format med valgfrie attributter

[!include [banner](../../includes/banner.md)]

Fremgangsmåten nedenfor forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ER-formatkonfigurasjon for å importere filer i XML-format som inneholder valgfrie attributter. For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv". Før du begynner, laster du ned filen IncomingDocumentToLearnHowToHandleOptionalAttributes.xml fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) og lagrer den lokalt.

1.    Gå til **Alle arbeidsområder** > **Elektronisk rapportering**.
2.    Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).
3.    Klikk på **Rapporteringskonfigurasjoner**.

## <a name="create-a-new-data-model-configuration"></a>Opprett en ny datamodellkonfigurasjon
1.    Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.
2.    Skriv inn «Modell for å importere XML-fil» i **Navn**-feltet.
3.    Klikk **Opprett konfigurasjon**.
4.    Klikk **Utforming**.
5.    Klikk på **Ny** for å åpne nedtrekksdialogen.
6.    Skriv inn «Rot» i **Navn**-feltet.
7.    Klikk **Legg til**.
8.    Klikk på **Ny** for å åpne nedtrekksdialogen.
9.    Skriv inn «Liste» i **Navn**-feltet.
10.    Velg **Postliste** i **Varetype**-feltet.
11.    Klikk **Legg til**.
12.    Klikk på **Ny** for å åpne nedtrekksdialogen.
13.    I **Navn**-feltet skriver du inn «Kode».
14.    Velg **Streng** i **Varetype**-feltet.
15.    Klikk **Legg til**.
16.    Klikk **Lagre**.
17.    Lukk siden.
18.    Klikk på **Endre status**.
19.    Klikk på **Fullført**.
20.    Klikk **OK**.

## <a name="create-a-format-for-data-import"></a>Opprette et format for dataimport
1.    Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.
2.    I **Ny**-feltet angir du «Format basert på datamodellen Modell for å importere XML-fil».
3.    Skriv inn «Format for å importere XML-fil» i **Navn**-feltet.
4.    Velg **Ja** i feltet **Støtter dataimport**.
5.    Klikk **Opprett konfigurasjon**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Utforme et format for å analysere innkommende fil i XML-format
1.    Klikk **Utforming**.
2.    Klikk på **Legg til rot** for å åpne nedtrekksdialogen.
3.    Velg **XML\Element** i treet.
4.    Skriv inn «rot» i **Navn**-feltet.
5.    Klikk **OK**.
6.    Klikk på **Legg til** for å åpne nedtrekksdialogen.
7.    Velg **XML\Element** i treet.
8.    I **Navn**-feltet skriver du inn «dokument».
9.    Velg **Én mange** i feltet **Multiplisitet**.
10.    Klikk **OK**.
11.    Velg **rot\dokument** i treet.
12.    Klikk på **Legg til** for å åpne nedtrekksdialogen.
13.    Velg **XML\Attributt** i treet.
14.    I **Navn**-feltet skriver du inn «ID».
15.    Klikk **OK**.
16.    Klikk **Lagre**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Utforme en formattilordning for å lagre analysert informasjon i datamodell
1. Klikk på **Tilordne format til modell**.
2. Klikk på **Ny**.
3. Angi eller velg en verdi i feltet **Definisjon**.
4. Klikk koblingen i den valgte raden i listen.
5. I **Navn**-feltet skriver du inn «Tilordning».
6. Klikk **Lagre**.
7. Klikk **Utforming**.
8. Utvid **format** i treet.
9. I treet utvider du **format\rot: XML-element(rot)**.
10.    I treet velger du **format\root: XML-element(rot)\dokument: XML-element 1..* (dokument)**.
11.    Klikk på **Bind**.
12.    I treet utvider du **format\rot: XML-element(rot)\dokument: XML-element 1..* (dokument)**.
13.    I treet velger du **format\root: XML-element(rot)\dokument: XML-element 1..* (dokument)\id**.
14.    I treet utvider du **Liste = format.rot.dokument**.
15.    I treet velger du **Liste = format.rot.dokument\Kode**.
16.    Klikk på **Bind**.
17.    Klikk **Lagre**.
18.    Lukk siden.
 
## <a name="run-format-mapping"></a>Kjøre formattilordning
1. Klikk på **Kjør**.
2. Klikk på **Bla gjennom**, og velg **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Klikk **OK**.

> [!NOTE]
> Den valgte filen er ikke importert, siden formatutformingen forutsetter at et «id»-attributt finnes for «dokument»-elementet, men den importerte filen inneholder ikke noe slikt attributt.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Endre formatstrukturen for å håndtere XML-attributter som valgfrie
1. Lukk siden.
2. Utvid **rot\dokument** i treet.
3. Velg **rot\dokument\id** i treet.
4. Velg **Ja** i feltet **Tom streng for manglende attributt**.
5. Klikk **Lagre**.
 
## <a name="run-format-mapping-to-test-changes"></a>Kjøre formattilordning for å teste endringer
1. Klikk på **Tilordne format til modell**.
2. Klikk på **Kjør**.
3. Klikk på **Bla gjennom**, og velg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Klikk **OK**.
5. Se gjennom den genererte filen. 

> [!NOTE]
> Den samme filen har blitt importert siden formatutformingen nå regner «id»-attributtet for «dokument»-elementet for å være valgfritt.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
