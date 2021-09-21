---
title: Rediger personlige oplysninger
description: Denne artikel beskriver, hvordan du redigerer personlige oplysninger i selvbetjening for medarbejdere og ledelse.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bb827e17dcfc63031d0edcb5f447e70f03e8ac3c
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431456"
---
# <a name="edit-personal-information"></a>Rediger personlige oplysninger

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan redigere dine personlige oplysninger i Dynamics 365 Human Resources i arbejdsområdet **Medarbejderselvbetjening**.

De personlige oplysninger, du kan redigere, omfatter:

- Adresser
- Kontaktoplysninger
- Personlige kontakter
- Identifikationsnumre
- Betalingsmetode
- Billede, der bruges i Human Resources

>[!NOTE]
>Du vil muligvis ikke kunne redigere bestemte typer personlige oplysninger, f.eks. oplysninger om forretningskontakter. Du kan finde flere oplysninger i [Begrænse redigering af personlige oplysninger](hr-employee-self-service-restrict-editing.md).

Parametre, der angives i de **globale adressekartotekparametre**, bestemmer, hvilke roller der kan se dine personlige oplysninger.

1. Vælg **Medarbejderselvbetjening** i Human Resources.

2. Vælg **Rediger personlige oplysninger**.

3. Hvis du vil ændre din adresse, skal du vælge fanen **Adresser**. De ændringer, du foretager, vises i arbejdsområdet **Personalestyring** som en påmindelse for HR.

    - Vælg **Tilføj** for at tilføje en ny adresse.
    - Hvis du vil redigere en eksisterende adresse, skal du vælge adressen og derefter vælge **Rediger**.
    - Vælg **Kort** for at få vist et kort.
    - Hvis du vil tilføje eller fjerne en kontaktperson, skal du vælge **Flere indstillinger** og derefter vælge **Avanceret**. Under **Kontaktoplysninger** skal du vælge **Tilføj** eller **Fjern** og redigere felterne efter behov.
    - Hvis du vil angive tidszone og sted, skal du vælge **Flere indstillinger** og derefter vælge **Avanceret**. Rediger felterne under **Generelt**, hvis det er nødvendigt.

4. Hvis du vil ændre dine kontaktoplysninger, skal du vælge fanen **Kontaktoplysninger**. Du kan angive forskellige typer kontaktoplysninger, herunder telefon, e-mail, og links til sociale medier. Du kan angive kontaktoplysninger som primær, men du kan kun angive en af de enkelte typer som primær.

    - Vælg **Tilføj** for at tilføje en ny kontaktoplysning. Tilpas felterne efter behov.
    - Hvis du vil redigere eksisterende kontaktoplysninger, skal du vælge det pågældende element og derefter vælge **Rediger**. Tilpas felterne efter behov.
    - Hvis du vil indstille en kontaktoplysning som privat, skal du markere elementet, vælge **Avanceret** og derefter vælge **Ja** i indstillingen **Privat**. Vælg **OK**.
      >[!NOTE]
      >Knappen **Avanceret** kan ikke vælges, hvis administratoren har aktiveret funktionen **(Forhåndsversion) Begræns medarbejdere i at tilføje eller redigere adresse- og kontaktoplysninger til udvalgte formål** i dit miljø. Du kan finde flere oplysninger i [Begrænse redigering af personlige oplysninger](hr-employee-self-service-restrict-editing.md).
  
5. Hvis du vil ændre dine personlige kontaktpersoner, skal du vælge fanen **Personlige kontakter**. Du kan udpege kontakter til nødstilfælde, beneficianter og afhængige. En kontakt kan være en person eller organisation. Funktionen **Administration af frynsegoder** bruger personlige kontaktoplysninger. Du kan finde flere oplysninger under [Konfigurere indstillinger for personlig kontaktberettigelse](hr-benefits-setup-contact-eligibility-options.md).

6. Hvis du vil ændre id-numrene, f.eks. CPR-nummer, skal du vælge fanen **Identifikationsnumre**. Ændringerne gennemgår muligvis en godkendelsesproces, hvis organisationen opretter en arbejdsgang for godkendelse.

    - Vælg **Ny** for at tilføje et identifikationsnummer. Udfyld felterne efter behov, og vælg **Gem**.
    - Hvis du vil redigere et nummer, skal du vælge **Rediger**. Rediger felterne efter behov, og vælg **Gem**.

7. Hvis du vil ændre de metoder, som du bliver betalt efter, skal du vælge fanen **Mine betalingsoplysninger**. Denne fane er kun tilgængelig, hvis betalingsmetoderne er aktiveret i formularen **Human Resourcesparametre**. HR kan aktivere **Bankanvisning**, **Kontant**, **Check**, **Elektronisk betaling** eller **Anden**. HR kan også deaktivere validering af elektronisk betaling (bruges til amerikanske løn) og validering af bankkonto- og registreringsnummer.

8. Hvis du vil ændre det billede, der vises i Human Resources for din profil, skal du vælge fanen **Billede**. Afhængigt af organisationens indstillinger kan billeder sendes til godkendelse.

    - Hvis du vil overføre et billede, skal du vælge **Overfør nyt billede**.
    - Hvis du vil fjerne et billede, skal du markere billedet og derefter vælge **Fjern**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
