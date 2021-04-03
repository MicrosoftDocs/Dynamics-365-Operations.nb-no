---
title: Komme i gang med tillegget Elektronisk fakturering for Brasil
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Brasil i Finance and Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: eaf9433ad2d9ccf3d3c5632d0f2d4fe772ff8bde
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592676"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Komme i gang med tillegget Elektronisk fakturering for Brasil 

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kommer i gang med tillegget Elektronisk fakturering for Brasil. Fremgangsmåten i dette emnet tar deg gjennom konfigurasjonstrinnene som er landavhengige i RCS (Regulatory Configuration Services), og utfyller trinnene som beskrives i emnet [Komme i gang med tillegget for elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for funksjon for elektronisk fakturering for brasiliansk NF-e (BR)

Hvis du konfigurerer funksjonen for elektronisk fakturering for brasiliansk NF-e (BR), kreves det at bestemte trinn må fullføres. Noen av parameterne fra konfigurasjonene publiseres med standardverdier, så de må gjennomgås og oppdateres slik at de passer bedre til forretningsoperasjonen.

### <a name="prerequisites"></a>Forutsetninger

Før du fullfører prosedyren i denne delen, oppretter du en funksjon for elektronisk fakturering for brasiliansk NF-e (BR) for organisasjonen, som beskrevet i delen **Opprette en funksjon for elektronisk fakturering under organisasjonsleverandøren** i emnet [Komme i gang med tillegget for elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS velger du flisen **Tillegg for elektronisk fakturering** i delen **Funksjoner** i arbeidsområdet **Globaliseringsfunksjon**.
2. På siden **Funksjoner for tillegg for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **brasiliansk NF-e (BR)** som du opprettet, er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
4. Velg **Send** i fanen **Oppsett** i rutenettet, og velg deretter **Rediger.**
5. Velg handlingen **(Forhåndsversjon) Signer XML-dokument** i feltgruppen **Handlinger** i fanen **Handlinger**.
6. Velg **Sertifikatnavn** i feltgruppen **Parametere**, og angir navnet på sertifikatet som er knyttet til Key Vault-parameteren, i feltet **Verdi**.
7. Velg handlingen **(Forhåndsversjon) Kalle opp brasiliansk SEFAZ-tjeneste** i feltgruppen **Handlinger** i fanen **Handlinger**.
8. Velg parameteren **URL-adresse** i feltgruppen **Parametere**.
9. I feltet **Verdi** kan du om nødvendig gå gjennom og oppdatere URL-adressen til webtjenestene som er publisert av SEFAZ-dokumentasjonen for din stat, og deretter velger du **Lagre.**
10. I feltgruppen **Oppsett av relevansregler** i fanen **Relevansregler** går du gjennom og oppdaterer kriteriene for feltet **Tilstand** som obligatoriske for den samme tilstanden som URL-adressen for webtjenestene refererer til.
11. Velg **Lagre** og lukk siden.
12. Hvis du vil konfigurere programoppsettet, kan du se [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for programoppsett for funksjon for elektronisk fakturering for brasiliansk NF-e (BR)

Hvis du konfigurerer programoppsettet for funksjonen for elektronisk fakturering for brasiliansk NF-e (BR), kreves det at bestemte trinn må fullføres. Fullfør disse trinnene før du distribuerer funksjonen for elektronisk fakturering til tilleggsmiljøet for elektronisk fakturering.

### <a name="prerequisites"></a>Forutsetninger

Før du fullfører prosedyren i denne delen, oppretter og starter du programkonfigurasjonen for funksjonen for elektronisk fakturering for brasiliansk NF-e (BR), som beskrevet i delen **Konfigurere programoppsettet** i emnet [Komme i gang med tillegget for elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS velger du flisen **Tillegg for elektronisk fakturering** i delen **Funksjoner** i arbeidsområdet **Globaliseringsfunksjon**.
2. På siden **Funksjoner for tillegg for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **brasiliansk NF-e (BR)** er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt.
4. I fanen **Oppsett** velger du **Programopsett**, og i feltet **Tilkoblet program** velger du programmet der du vil distribuere.
5. I feltet **Tabellnavn** kontrollerer du at **Regnskapsdokumenthode** er valgt.
6. Velg **Svartyper**, og velg deretter **Ny**.
7. I feltet **Svartype** angir du "Svar" som en fast verdi, og i feltet **Beskrivelse** skriver du inn "Beskrivelse".
8. I feltet for **innsendingsstatus** velger du **Venter**.
9. I feltet **Modelltilordning** velger du **Modelltilordning fra svarmelding** med **(Forhåndsversjon) Format for import av svarmelding**, og deretter velger du **Lagre**.
10. Velg **Ny**, i feltet **Svartype** angir du "Svardata" som en fast verdi, og i feltet **Beskrivelse** angir du "Beskrivelse".
11. I feltet for **innsendingsstatus** velger du **Venter**.
12. I feltet **Modelltilordning** velger du **Import av svardata** med **(Forhåndsversjon) Format for import av NF-e-svardata (BR)**, og deretter velger du **Lagre**.
13. Hvis du vil distribuere funksjonen for elektronisk fakturering, kan du se [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for funksjonen for elektronisk fakturering for brasiliansk NFS-e ABRASF Curitiba (BR)

Hvis du konfigurerer funksjonen for elektronisk fakturering for brasiliansk NFS-e ABRASF Curitiba, kreves det at bestemte trinn må fullføres. Noen av parameterne fra konfigurasjonene publiseres med standardverdier, så de må gjennomgås og oppdateres slik at de passer bedre til forretningsoperasjonen.

### <a name="prerequisites"></a>Forutsetninger

Før du fullfører prosedyren i denne delen, må du opprette en funksjon for elektronisk fakturering for brasiliansk NFS-e ABRASF Curitiba (BR) i organisasjonen. Dette beskrives i delen **Konfigurere funksjon for elektronisk fakturering** i emnet [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS velger du flisen **Tillegg for elektronisk fakturering** i delen **Funksjoner** i arbeidsområdet **Globaliseringsfunksjon**.
2. På siden **Funksjoner for tillegg for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **brasiliansk NFS-e ABRASF Curitiba (BR)** som du opprettet, er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt, og i fanen **Oppsett** i rutenettet velger du **Send**.
4. Velg **Rediger**, og i feltgruppen **Handlinger** i fanen **Handlinger** velger du den første forekomsten av **(Forhåndsversjon) Signer XML-dokument**.
5. Velg **Sertifikatnavn** i feltgruppen **Parametere**.
6. I feltet **Verdi** angir du navnet på sertifikatet som er knyttet til Key Vault-parameteren.
7. I feltgruppen **Handlinger** velger du den andre forekomsten av **(Forhåndsvis) Signer XML-dokument**.
8. Velg **Sertifikatnavn** i feltgruppen **Parametere**.
9. I feltet **Verdi** angir du navnet på sertifikatet som er knyttet til Key Vault-parameteren.
10. Velg handlingen **(Forhåndsversjon) Kalle opp brasiliansk SEFAZ-tjeneste** i feltgruppen **Handlinger** i fanen **Handlinger**.
11. Velg parameteren **URL-adresse** i feltgruppen **Parametere**.
12. I feltet **Verdi** kan du om nødvendig gå gjennom og oppdatere URL-adressen til webtjenestene som er publisert av skattemyndighetene i byen Curitiba, og deretter velger du **Lagre.**
13. Velg **Forespør** i fanen **Oppsett** i rutenettet, og velg deretter **Rediger.**
14. Velg handlingen **(Forhåndsversjon) Kalle opp brasiliansk SEFAZ-tjeneste** i feltgruppen **Handlinger** i fanen **Handlinger**.
15. Velg parameteren **URL-adresse** i feltgruppen **Parametere**.
16. I feltet **Verdi** kan du om nødvendig gå gjennom og oppdatere URL-adressen til webtjenestene som er publisert av skattemyndighetene i byen Curitiba.
17. Velg **Lagre** og lukk deretter siden.
18. Hvis du vil konfigurere programoppsettet, kan du se [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landspesifikk konfigurasjon for programoppsett for funksjonen for elektronisk fakturering for brasiliansk NFS-e ABRASF Curitiba (BR)

Hvis du konfigurerer programoppsettet for funksjonen for elektronisk fakturering for brasiliansk NFS-e ABRASF Curitiba (BR), kreves det at bestemte trinn må fullføres før du distribuerer funksjonen for elektronisk fakturering i tjenestemiljøet for elektronisk fakturering.

### <a name="prerequisites"></a>Forutsetninger

Før du fullfører prosedyren i denne delen, oppretter og starter du en funksjon for elektronisk fakturering for brasiliansk NFS-e ABRASF Curitiba (BR), som beskrevet i delen **Konfigurere programoppsettet** i emnet [Komme i gang med tillegget for elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS velger du flisen **Tillegg for elektronisk fakturering** i delen **Funksjoner** i arbeidsområdet **Globaliseringsfunksjon**.
2. På siden **Funksjoner for tillegg for elektronisk fakturering** kontrollerer du at funksjonen for elektronisk fakturering for **brasiliansk NFS-e ABRASF Curitiba (BR)**, er valgt.
3. I fanen **Versjoner** kontrollerer du at versjonen **Utkast** er valgt, og i fanen **Oppsett** i rutenettet velger du **Programoppsett**.
4. Velg programmet du vil distribuere til, i feltet **Tilkoblet program**.
5. I feltet **Tabellnavn** kontrollerer du at regnskapsdokumenthodet er valgt.
6. Velg **Svartyper** og deretter **Ny**.
7. I feltet **Svartype** angir du "ABRASFCuritibaSendSvar" som en fast verdi, og i feltet **Beskrivelse** skriver du inn "Beskrivelse".
8. I feltet for **innsendingsstatus** velger du **Venter**.
9. I feltet **Modelltilordning** velger du **Import av svarmelding** med **(Forhåndsversjon) Import av svarmelding for NFS-e-ABRASF Curitiba (BR)**, og deretter velger du **Lagre**.
10. Velg **Ny**, i feltet **Svartype** angir du "ABRASFCuritibaSendSvardata" som en fast verdi, og i feltet **Beskrivelse** angir du "Beskrivelse".
11. I feltet for **innsendingsstatus** velger du **Venter**.
12. I feltet **Modelltilordning** velger du **Import av svardata** med **(Forhåndsversjon) Format for import av svardata for NFS-e-ABRASF (BR)**, og deretter velger du **Lagre**.
13. Velg **Ny**, i feltet **Svartype** angir du "ABRASFCuritibaForespørSvar" som en fast verdi, og i feltet **Beskrivelse** angir du "Beskrivelse".
14. I feltet for **innsendingsstatus** velger du **Venter**.
15. I feltet **Modelltilordning** velger du **Import av svarmelding** med **(Forhåndsversjon) Import av svarmelding for NFS-e-ABRASF Curitiba (BR).**
16. Velg **Lagre**, og returner deretter til emnet [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md) for å distribuere funksjonen for elektronisk fakturering.

## <a name="privacy-notice"></a>Personvernerklæring
Aktivering av funksjonene **NF-e Føderal – Brasiliansk elektronisk fakura (BR)** og **NFS-e – Elektronisk faktura for brasiliansk tjeneste (poststed)** kan kreve at begrensede data sendes, inkludert skatteregistrerings-ID-en for organisasjonen. Disse dataene blir overført til tredjepartsleverandører autorisert av skattemyndigheten for å sende elektroniske fakturaer til skattemyndighetene i det forhåndsdefinerte formatet som kreves for integrering med myndighetenes webtjeneste. Som administrator kan du aktivere eller slå av funksjonene **NF-e Føderal – Brasiliansk elektronisk faktura (BR)** og **NFS-e – Elektronisk faktura for brasiliansk tjeneste (poststed)**. Følgende fremgangsmåte viser hvordan du gjør dette: 

1. Gå til **Organisasjonsstyring** > **Oppsett** > **Parametere for elektronisk dokument**. 
2. I fanen **Funksjoner** velger du raden som inneholder funksjonen **NF-e Føderal – Brasiliansk elektronisk faktura (BR)** eller **NFS-e – Elektronisk faktura for brasiliansk tjeneste (poststed)** og velger funksjonen. Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delene om personvernerklæring i dokumentasjon for landspesifikke funksjoner.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over tillegg for elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tjenesteadministrasjon for tillegget for elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Komme i gang med Elektronisk fakturering-tillegget](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
