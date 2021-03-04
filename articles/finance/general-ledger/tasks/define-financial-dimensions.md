---
title: Definere finansdimensjoner
description: Denne oppgaveveiledningen beskriver hvordan du legger til en enhetsstøttet finansdimensjon og en egendefinert finansdimensjon.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fbe739eec0cfa1e7b0276872640bd4f82be3ef7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446226"
---
# <a name="define-financial-dimensions"></a>Definere finansdimensjoner

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen beskriver hvordan du legger til en enhetsstøttet finansdimensjon og en egendefinert finansdimensjon.  Veiledningen bruker USMF demo firmaet.


## <a name="create-an-entity-backed-financial-dimension"></a>Opprette en enhetsstøttet finansdimensjon
1. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner**.
2. Klikk på **Ny**.
3. Velg en systemdefinert enhet som finansdimensjonen baseres på, i feltet **Brukerverdier fra**. 
4. Skriv inn en verdi for å beskrive finansdimensjonen i feltet **Dimensjonsnavn**. Navnet kan være forskjellig fra den systemdefinerte enheten, men kan ikke inneholde mellomrom eller spesialtegn.
5. Klikk **Aktiver**. Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner. Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes før den er aktivert.  
6. Klikk på **Lukk** på aktiveringsmeldingen.
7. Klikk **Aktiver**. Aktivering av dimensjonen kan planlegges til å kjøre som parti på en bestemt dato og klokkeslett.  
8. I **handlingsruten** klikker du på **Dimensjonsverdier**. Noen dimensjonsverdier er firmaspesifikke. Du kan kontrollere om de er firmaspesifikke ved om firmanavnet vises i dimensjonsverdilisten.  

## <a name="create-a-custom-financial-dimension"></a>Opprette en egendefinert finansdimensjon
1. Lukk siden.
2. Klikk på **Ny**.
3. I feltet **Bruk verdier fra** velger du **Egendefinert dimensjon**.
4. Skriv inn en verdi for å beskrive finansdimensjonen i feltet **Dimensjonsnavn**.
    - Navnet kan ikke inneholde mellomrom eller spesialtegn.  
    - Du kan også angi en kontomaske for å begrense mengden og typen informasjon som du kan angi for dimensjonsverdier.   
    - Du kan angi tegn som forblir de samme for hver dimensjonsverdi, for eksempel bokstaver eller en bindestrek. Du kan også angi nummertegn (#) og &-tegn som plassholdere for bokstaver og tall som vil endres hver gang en dimensjonsverdi opprettes. Bruk et nummertegn (#) som plassholder for et tall og et &-tegn som plassholder for en bokstav.  Eksempel: Hvis du vil begrense dimensjonsverdien til bokstavene CC og tre tall, kan du angi CC-### som formatmaske.  
5. Klikk **Aktiver**. Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner. Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes før den er aktivert.     
6. Klikk **Aktiver**. Aktivering av dimensjonen kan planlegges til å kjøre som parti på en bestemt dato og klokkeslett.      
7. I **handlingsruten** klikker du på **Dimensjonsverdier**.
8. Klikk på **Ny**.
9. Skriv inn et navn for å beskrive finansdimensjonsverdien i feltet **Dimensjonsverdi**.
10. Skriv inn en beskrivelse som beskriver finansdimensjonsverdien i **Beskrivelse**-feltet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]