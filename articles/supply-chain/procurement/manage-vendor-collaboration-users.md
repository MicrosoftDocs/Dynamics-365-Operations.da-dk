---
title: Administrere brugere af kreditorsamarbejde
description: Denne artikel beskriver, hvordan du kan anmode om klargøring af nye brugere af kreditorsamarbejde, og hvordan du tilføjer nye kontakter for kreditorsamarbejde.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 823e92cadc36659264a70132ed1390c7bcf8bc5d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852296"
---
# <a name="manage-vendor-collaboration-users"></a>Administrere brugere af kreditorsamarbejde

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kan anmode om klargøring af nye brugere af kreditorsamarbejde, og hvordan du tilføjer nye kontakter for kreditorsamarbejde. 

Grænsefladen for kreditorsamarbejde i Dynamics 365 Supply Chain Management viser oplysninger om indkøbsordrer, fakturaer og konsignationslager til eksterne leverandører. Du kan oprette nye kontakter for kreditorsamarbejde og anmode om, at nye brugere forsynes, hvis du arbejder som en ekstern leverandør med de **Kreditoradministrator (ekstern)** som sikkerhedsrolle eller tilsvarende tilladelser. Du kan også udføre disse opgaver, hvis du arbejder som en professionel indkøber. Denne artikel vedrører denne rolle en professionel indkøber, der arbejder i virksomheden, som ejer forekomsten af Supply Chain Management. Du kan finde flere oplysninger om, hvordan du bruger leverandørsamarbejde, hvis du er ekstern leverandør, under [Leverandørsamarbejde med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Du kan finde flere oplysninger om, hvordan du bruger leverandørsamarbejde, hvis du er professionel indkøber, under [Leverandørsamarbejde med eksterne leverandører](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Tilføje nye kontakter for kreditorsamarbejde
Hvis du ønsker, at andre skal have adgang til kreditorsamarbejde, skal de først tilføjes som en kontakt for kreditorsamarbejde. Du kan også tilføje kontakter for medarbejdere i din virksomhed, som ikke skal bruge kreditorsamarbejde. De kunne for eksempel være kontaktpunkt for andre typer indkøbsoplysninger. Nye kontakter tilføjes på siden **Alle kontaktpersoner**, som åbnes fra menuen **Kreditorsamarbejde** &gt; **Kontaktpersoner**. Sådan tilføjer du en ny kontakt:

1.  Klik på **Ny.**
2.  Indtast oplysninger om kontaktpersonen.
3.  Vælg, hvilken juridisk enhed personen repræsenterer i din virksomhed, og hvilken juridisk enhed personen skal arbejde med i det firma, der skal samarbejdes med. Det gør du ved at vælge et **Juridisk enhed i mit firma**/**Juridisk enhed i kundefirma**-par.
4.  Klik på **Opret.**

Hvis du vil slette en kontaktperson, er det kun muligt at slette dem, du har oprettet.

## <a name="vendor-collaboration-user-requests"></a>Brugeranmodninger om kreditorsamarbejde
Kreditorsamarbejdets brugeranmodninger kan forhøjes af en professionel indkøber eller en ekstern leverandøradministrator.

-   Hvis du er en ekstern leverandør, skal du sende anmodninger fra siden **Alle kontaktpersoner** i modulet **Kreditorsamarbejde**.
-   Hvis du er professionel indkøber, sender du anmodninger fra siden **Vis kontakter**. Du kan gøre dette på kreditorposten i sektionen **Konfiguration** i handlingsruden ved at vælge **Kontaktpersoner** &gt; **Vis kontakter**.

Du kan oprette en anmodning om at klargøre en bruger, deaktivere en bruger eller redigere sikkerhedsroller. Hvis du er administrator for ekstern leverandør, skal du være registreret som kontaktperson for kreditorkonti, du vil oprette brugeranmodninger om, og du skal have adgang til grænsefladen for kreditorsamarbejde for de pågældende kreditorkonti.  

Når en anmodning sendes, føjes den til listen **Brugeranmodninger om kreditorsamarbejde** i modulet **Kreditorsamarbejde** og listen **Brugeranmodning om kreditorsamarbejde** i modulet **Indkøb og forsyning** (Indkøb og forsyning-modulet er ikke tilgængeligt for eksterne brugere).

### <a name="provision-a-user"></a>Klargøre en bruger

Før du kan anmode om, at der er klargjort en ny bruger, skal vedkommende sættes op som kontaktperson for en eller flere kreditorkonti. Sådan opretter du en anmodning om en ny bruger af kreditorsamarbejde:

1. På siden **Alle kontaktpersoner** skal du klikke på **Klargør kreditorbruger**.
2. Angiv en mailadresse på brugeren. Denne adresse bruges af brugeren til at logge på Supply Chain Management. Hvis mailadressen hører til et domæne, der er registreret som lejer hos Microsoft Azure, skal mailadressen være en eksisterende Azure Active Directory-konto (AAD), for at klargøringsprocessen kan fuldføres. Hvis mailadressen ikke tilhører et domæne, der er registreret hos Microsoft Azure, vil en AAD-konto blive oprettet som en del af klargøringsprocessen, og den nye bruger modtager en invitationsmail. Forbrugeres mailadresser med domæner som @hotmail.com, @gmail.com eller @comcast.net kan ikke bruges til at registrere en bruger.
3. Angiv indstillingen **Adgang til kreditorsamarbejde tilladt** til **Ja** for alle de juridiske enheder, som brugeren skal have adgang til.
4. I sektionen **Tildel brugerroller** skal du markere **Tildel**-afkrydsningsfeltet for de sikkerhedsroller, som den nye bruger skal have.
5. Klik på **Send**.

Når kreditorbrugeranmodning sendes, bliver feltet **Adgang til kreditorsamarbejde tilladt** indstillet til **Ja** for den valgte kreditorkonto, og en arbejdsgang for brugeranmodning startes. Der oprettes en ny bruger som en del af arbejdsgangen, og der tildeles sikkerhedsroller. Desuden bliver en Azure B2B-tjeneste aktiveret, som starter interaktion med Azure-portal og knytter en ny eller eksisterende AAD-konto til Supply Chain Management-brugerkontoen. Du kan finde flere oplysninger i [Hvad er Azure AD B2B-samarbejde?](/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

### <a name="inactivate-a-user"></a>Deaktivere en bruger

Der er to måder at fjerne adgangen til leverandørsamarbejde for en bruger:

-   På siden **Kontakter** for kreditoren skal du angive indstillingen **Adgang til kreditorsamarbejde tilladt** til **Nej** for kontakten. Dette kan gøres individuelt pr. juridisk enhed, som personen er kontakt for. Denne indstilling kan kun bruges af indkøbsmedarbejderen.
-   Deaktiver hele brugerkontoen ved at indsende en **Deaktiver kreditorbruger**-anmodning.

Sådan anmoder du om, at en bruger deaktiveres:

1.  På siden **Alle kontaktpersoner** skal du klikke på **Deaktiver** **kreditorbruger**.
2.  Skriv en kommentar i feltet **Forretningsberettigelse**.
3.  Klik på **Send**.

### <a name="modify-security-roles"></a>Ændre sikkerhedsroller

Siden **Vedligehold kreditorbrugerroller** er den samme som siden **Klargør kreditorbruger** bortset fra, at listen over sikkerhedsroller kan redigeres.  

Sådan anmoder du om, at sikkerhedsrollerne ændres for en bruger:

1.  På siden **Alle kontaktpersoner** skal du klikke på **Vedligehold** **kreditorbrugerroller**.
2.  Skriv en kommentar i feltet **Forretningsberettigelse**.
3.  I sektionen **Vedligehold brugerroller** skal du vælge de sikkerhedsroller, som du vil tildele, eller fjerne markeringen af dem, som du vil fjerne.
4.  Klik på **Send**.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]