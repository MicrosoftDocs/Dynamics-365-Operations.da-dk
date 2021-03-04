---
title: Rediger personlige oplysninger
description: Denne artikel beskriver, hvordan du redigerer personlige oplysninger i selvbetjening for medarbejdere og ledelse.
author: andreabichsel
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0158bd4ee74e24006e338c0477ee0ac4210b1bf5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417732"
---
# <a name="edit-personal-information"></a>Rediger personlige oplysninger

Du kan redigere dine personlige oplysninger i Dynamics 365 Human Resources i arbejdsområdet **Medarbejderselvbetjening**.

De personlige oplysninger, du kan redigere, omfatter:

- Adresser
- Kontaktoplysninger
- Personlige kontakter
- Identifikationsnumre
- Betalingsmetode
- Billede, der bruges i Human Resources

Parametre, der angives i det globale adressekartotek, bestemmer, hvilke roller der kan se dine personlige oplysninger.

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
  
5. Hvis du vil ændre dine personlige kontaktpersoner, skal du vælge fanen **Personlige kontakter**. Du kan udpege kontakter til nødstilfælde, beneficianter og afhængige. En kontakt kan være en person eller organisation. Funktionen **Administration af frynsegoder** bruger personlige kontaktoplysninger. Du kan finde flere oplysninger under [Konfigurere indstillinger for personlig kontaktberettigelse](hr-benefits-setup-contact-eligibility-options.md).

6. Hvis du vil ændre id-numrene, f.eks. CPR-nummer, skal du vælge fanen **Identifikationsnumre**. Ændringerne gennemgår muligvis en godkendelsesproces, hvis organisationen opretter en arbejdsgang for godkendelse.

    - Vælg **Ny** for at tilføje et identifikationsnummer. Udfyld felterne efter behov, og vælg **Gem**.
    - Hvis du vil redigere et nummer, skal du vælge **Rediger**. Rediger felterne efter behov, og vælg **Gem**.

7. Hvis du vil ændre de metoder, som du bliver betalt efter, skal du vælge fanen **Mine betalingsoplysninger**. Denne fane er kun tilgængelig, hvis betalingsmetoderne er aktiveret i formularen **Personaleparametre**. HR kan aktivere **Bankanvisning**, **Kontant**, **Check**, **Elektronisk betaling** eller **Anden**. HR kan også deaktivere validering af elektronisk betaling (bruges til amerikanske løn) og validering af bankkonto- og registreringsnummer.

8. Hvis du vil ændre det billede, der vises i Personale for din profil, skal du vælge fanen **Billede**. Afhængigt af organisationens indstillinger kan billeder sendes til godkendelse.

    - Hvis du vil overføre et billede, skal du vælge **Overfør nyt billede**.
    - Hvis du vil fjerne et billede, skal du markere billedet og derefter vælge **Fjern**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]