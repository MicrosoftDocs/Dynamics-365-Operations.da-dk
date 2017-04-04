---
title: Administrere brugere af kreditorsamarbejde
description: "Dette emne beskriver, hvordan du kan anmode om klargøring af nye brugere af kreditorsamarbejde, og hvordan du tilføjer nye kontakter for kreditorsamarbejde."
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

# <a name="manage-vendor-collaboration-users"></a>Administrere brugere af kreditorsamarbejde

Dette emne beskriver, hvordan du kan anmode om klargøring af nye brugere af kreditorsamarbejde, og hvordan du tilføjer nye kontakter for kreditorsamarbejde. 

Grænsefladen for kreditorsamarbejde i Microsoft Dynamics 365 for Operations viser oplysninger om indkøbsordrer, fakturaer og konsignationslager til eksterne leverandører. Du kan oprette nye kontakter for kreditorsamarbejde og anmode om, at nye brugere forsynes, hvis du arbejder som en ekstern leverandør med de **Kreditoradministrator (ekstern)** som sikkerhedsrolle eller tilsvarende tilladelser. Du kan også udføre disse opgaver, hvis du arbejder som en professionel indkøber. I dette emne vedrører denne rolle en professionel indkøber, der arbejder i virksomheden, som ejer forekomsten af Dynamics 365 for Operations. Yderligere oplysninger om, hvordan du bruger leverandør samarbejde, hvis du er en ekstern leverandør, du [kreditor med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Finde flere oplysninger om, hvordan du bruger leverandør samarbejde, hvis du er en professionel indkøb, [leverandør samarbejde til med eksterne leverandører](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Tilføje nye kontakter for kreditorsamarbejde
Hvis du ønsker, at andre skal have adgang til kreditorsamarbejde, skal de først tilføjes som en kontakt for kreditorsamarbejde. Du kan også tilføje kontakter for medarbejdere i din virksomhed, som ikke skal bruge kreditorsamarbejde. De kunne for eksempel være kontaktpunkt for andre typer indkøbsoplysninger. Føjes nye kontaktpersoner på den **alle kontaktpersoner** side, som åbnes fra den **leverandør samarbejde**&gt;**kontakter** i menuen. Sådan tilføjer du en ny kontakt:

1.  Klik på **Ny.**
2.  Indtast oplysninger om kontaktpersonen.
3.  Vælg, hvilken juridisk enhed personen repræsenterer i din virksomhed, og hvilken juridisk enhed personen skal arbejde med i det firma, der skal samarbejdes med. Det gør du ved at vælge en **juridisk enhed i mit firma**/**juridisk enhed i kundens virksomhed** par.
4.  Klik på **Opret.**

Hvis du vil slette en kontaktperson, er det kun muligt at slette dem, du har oprettet.

## <a name="vendor-collaboration-user-requests"></a>Brugeranmodninger om kreditorsamarbejde
Kreditorsamarbejdets brugeranmodninger kan forhøjes af en professionel indkøber eller en ekstern leverandøradministrator.

-   Hvis du er en ekstern leverandør, skal du sende anmodninger fra den **alle kontaktpersoner** side inden for den **leverandør samarbejde** modul.
-   Hvis du er professionel indkøber, sender du anmodninger fra siden **Vis kontakter**. At gøre dette, på kreditorpost, i den **Setup** afsnit i handlingsruden, Vælg **kontakter**&gt;**se kontaktpersoner**.

Du kan oprette en anmodning om at klargøre en bruger, deaktivere en bruger eller redigere sikkerhedsroller. Hvis du er administrator for ekstern leverandør, skal du være registreret som kontaktperson for kreditorkonti, du vil oprette brugeranmodninger om, og du skal have adgang til grænsefladen for kreditorsamarbejde for de pågældende kreditorkonti.  

Når en anmodning sendes, føjes den til listen **Brugeranmodninger om kreditorsamarbejde** i modulet **Kreditorsamarbejde** og listen **Brugeranmodning om kreditorsamarbejde** i modulet **Indkøb og forsyning** (Indkøb og forsyning-modulet er ikke tilgængeligt for eksterne brugere).

### <a name="provision-a-user"></a>Klargøre en bruger

Før du kan anmode om, at der er klargjort en ny bruger, skal vedkommende sættes op som kontaktperson for en eller flere kreditorkonti. Sådan opretter du en anmodning om en ny bruger af kreditorsamarbejde:

1.  På den **alle kontaktpersoner** skal du klikke på **bestemmelse kreditorbruger**.
2.  Angiv en mailadresse på brugeren. Denne adresse bruges til at logge på Dynamics 365 for Operations af brugeren. Hvis mailadressen hører til et domæne, der er registreret som lejer hos Microsoft Azure, skal mailadressen være en eksisterende Azure Active Directory-konto (ADD), for at klargøringsprocessen kan fuldføres. Hvis mailadressen ikke tilhører et domæne, der er registreret hos Microsoft Azure, vil en ADD-konto blive oprettet som en del af klargøringsprocessen, og den nye bruger modtager en invitationsmail. Forbruger email adresser med domæner som @hotmail.com, @gmail.com, eller @comcast.netkan ikke bruges til at registrere en Dynamics 365 for operationer bruger.
3.  Angiv indstillingen **Adgang til kreditorsamarbejde tilladt** til **Ja** for alle de juridiske enheder, som brugeren skal have adgang til.
4.  I sektionen **Tildel brugerroller** skal du markere **Tildel**-afkrydsningsfeltet for de sikkerhedsroller, som den nye bruger skal have.
5.  Klik på **Send**.

Når brugeren kreditoranmodningen sendes, den **leverandør samarbejde adgang tilladt** er angivet til **Ja** for den valgte kreditorkonto og en bruger anmoder om arbejdsgangen er startet. Der oprettes en ny bruger i Dynamics 365 for Operations som en del af arbejdsgangen, og der tildeles sikkerhedsroller. Desuden bliver en Azure B2B-tjeneste aktiveret, som starter interaktion med Azure-portal og knytter en ny eller eksisterende AAD-konto til Dynamics-365 for Operations-brugerkonto.

### <a name="inactivate-a-user"></a>Deaktivere en bruger

Der er to måder at fjerne adgangen til leverandørsamarbejde for en bruger:

-   På siden **Kontakter** for kreditoren skal du angive indstillingen **Adgang til kreditorsamarbejde tilladt** til **Nej** for kontakten. Dette kan gøres individuelt pr. juridisk enhed, som personen er kontakt for. Denne indstilling kan kun bruges af indkøbsmedarbejderen.
-   Deaktiver hele brugerkontoen ved at indsende en **Deaktiver kreditorbruger**-anmodning.

Til at anmode om, at en bruger er deaktiveret:

1.  På den **alle kontaktpersoner** skal du klikke på **Deaktiver****kreditorbrugeren**.
2.  Skriv en kommentar i feltet **Forretningsberettigelse**.
3.  Klik på **Send**.

### <a name="modify-security-roles"></a>Ændre sikkerhedsroller

Den **Vedligehold kreditor brugerroller** side er den samme som den **bestemmelse kreditorbruger** side, bortset fra at listen over sikkerhedsroller kan redigeres.  

Til at anmode om, at sikkerhedsrollerne er ændret for en bruger:

1.  På den **alle kontaktpersoner** skal du klikke på **Vedligehold****leverandør brugerroller**.
2.  Skriv en kommentar i feltet **Forretningsberettigelse**.
3.  I sektionen **Vedligehold brugerroller** skal du vælge de sikkerhedsroller, som du vil tildele, eller fjerne markeringen af dem, som du vil fjerne.
4.  Click **Submit**.



