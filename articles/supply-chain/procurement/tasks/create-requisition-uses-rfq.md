---
title: Opprett en rekvisisjon som bruker en tilbudsforespørsel
description: Denne artikkelen viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecde250e3517464611b68fe3c960bfbfdf06319
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846018"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Opprett en rekvisisjon som bruker en tilbudsforespørsel

[!include [banner](../../includes/banner.md)]

Denne artikkelen viser hvordan du legger til pris- og leverandørinformasjon i en innkjøpsrekvisisjon fra en prosess for tilbudsforespørsel. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF, og du må være logget på som administrator for å fullføre alle trinnene. Oppgavene i denne veiledningen utføres vanligvis av innkjøpsansvarlige.


## <a name="create-a-requisition"></a>Opprette en rekvisisjon
1. I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Innkjøpsrekvisisjoner > Innkjøpsrekvisisjoner klargjort av meg**.
2. Velg **Ny**.
3. Skriv inn en verdi i **Navn**-feltet.
4. Angi en dato i feltet **Ønsket dato**.
5. Angi en dato i feltet **Regnskapsdato**.
6. Velg **OK**.
7. Angi eller velg en verdi i **Årsak**-feltet.
8. Velg **Legg til linje**.
9. Velg en kategori i treet i **Innkjøpskategori**-feltet, og klikk deretter **OK**.
10. Skriv inn en verdi i feltet **Produktnavn**.
11. Angi et tall i **Antall**-feltet.
12. Angi eller velg en verdi i **Enhet**-feltet.
13. Velg **Lagre**.
14. Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.
15. Velg **Send**.
16. Lukk siden.
17. Velg **Send**.

## <a name="reassign-a-workflow-task"></a>Tilordne en arbeidsflytoppgave på nytt
Den neste oppgaven er å opprette en tilbudsforespørsel for å få bud fra leverandører for produktet. I demonstrasjonsdataene for USMF er rekvisisjonsarbeidsflyten definert med en regel slik at hvis en leverandør ikke er valgt, eller enhetsprisen er 0 for en linje, tilordnes en oppgave til en bestemt arbeider for å opprette en tilbudsforespørsel. Du må tilordne oppgaven på nytt til en annen bruker (deg selv) for å fortsette med denne veiledningen. Du kan bare gjøre dette hvis du er logget på som administrator.  

1. Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.
2. Velg **Vis logg**.
3. Oppdater siden.
4. Vis delen **Sporingsdetaljer**.
5. I treet velger du linjen som begynner med Linjeelementarbeidsflyt aktivert på.
6. Velg **Vis arbeidsflytdetaljer**.
7. Vis delen **Arbeidselementer**.
8. Velg **Tilordne på nytt**.
9. Velg **Administrator** i **Bruker**-feltet.
10. Velg **Tilordne på nytt**.
11. Lukk de to sidene.

## <a name="create-an-rfq"></a>Opprette en tilbudsforespørsel

1. Oppdater siden.
2. Velg **Tilbudsforespørsel**.
3. Velg **USMF** i feltet **Kjøpende juridisk enhet**. Du må velge den samme juridiske enheten som er på rekvisisjonslinjen.  
4. Merk den valgte raden i listen. Hvis du har flere linjer på innkjøpsrekvisisjonen din, velger du alle linjene som du vil legge til i tilbudsforespørselen.  
5. Velg **OK**.
6. Oppdater siden.
7. Kontroller at faktaboksen er åpen, og vis deretter delen **Relaterte dokumenter**.
8. Klikk på koblingen i **Tilbudsforespørsel**-feltet for å åpne tilbudsforespørselen som nettopp ble opprettet.
9. Velg **Topptekst**.
10. Velg **Legg til**.
11. Angi eller velg en verdi i **Leverandørkonto**-feltet.
12. Velg **Legg til**.
13. Angi eller velg en verdi i **Leverandørkonto**-feltet.
14. Velg **Send**.
15. Velg **OK**.
16. Velg **Angi svar**.
17. Velg **Svar** i handlingsruten.
18. Velg **Kopier data til svar**. Dette kopierer data, for eksempel antall og datoer, fra tilbudsforespørselen til svaret.  
19. Angi et tall i **Enhetspris**-feltet. Dette er prisen du har mottatt fra leverandøren. Du kan også angi tilleggsinformasjon fra leverandøren.  
20. Velg **Godta**.
21. Velg **OK**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Kontrollere at leverandøren prisen er overfør til rekvisisjonen
1. Lukk siden.
2. Velg **Linjer**.
3. Velg **Relatert informasjon**.
4. Velg **Innkjøpsrekvisisjon**.
5. Velg linjen som ble overført til tilbudsforespørselen. Kontroller at prisen og leverandøren er kopiert til rekvisisjonen.  
6. Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.
7. Velg Fullført.
8. Velg siden.
9. Velg Fullført.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]