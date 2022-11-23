---
title: Oprette eller sammenkæde med en eksisterende Azure AD B2C-lejer i Azure-portalen
description: Denne artikel beskriver, hvordan du opretter eller linker til en eksisterende Azure Active Directory (Azure AD) business-to-consumer (B2C)-lejer i Microsoft Azure-portalen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785251"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Oprette eller sammenkæde med en eksisterende Azure AD B2C-lejer i Azure-portalen

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du opretter eller linker til en Azure Active Directory (Azure AD) business-to-consumer (B2C)-lejer i Microsoft Azure-portalen. Du kan finde flere oplysninger i [Selvstudium: Oprette en Azure Active Directory B2C-lejer](/azure/active-directory-b2c/tutorial-create-tenant).

Hvis du vil oprette eller linke til en eksisterende Azure AD B2C-lejer på Azure-portalen, skal du følge disse trin.

1. Log på [Azure-portalen](https://portal.azure.com/).
1. Vælg **Opret en ressource** i Azure-portalmenuen. Sørg for at bruge det abonnement og den mappe, der er forbundet med dit Commerce-miljø.

    ![Oprette en ressource i Azure-portalen.](./media/B2CImage_1.png)

1. Gå til **Identitet \> Azure Active Directory B2C**.
1. Når du er på siden **Opret ny B2C lejer eller Opret et link til en eksisterende lejer**, skal du bruge en af de muligheder nedenfor, der bedst passer til firmaets behov:

    - **Opret en ny Azure AD B2C-lejer**: Brug denne indstilling til at oprette en ny Azure AD B2C-lejer.
        1. Vælg **Opret en ny Azure AD B2C-lejer**.
        1. Angiv organisationsnavnet under **Organisationsnavn**.
        1. Angiv det oprindelige domænenavn under **Oprindeligt domænenavn**.
        1. Vælg land eller område for **Land eller område**.
        1. Vælg **Opret** for at oprette lejeren.

     ![Opret en ny Azure AD-lejer.](./media/B2CImage_2.png)

     - **Sammenkæd en eksisterende Azure AD B2C lejer med mit Azure-abonnement**: Brug denne indstilling, hvis du allerede har en Azure AD B2C lejer, du vil oprette et link til.
        1. Vælg **Sammenkæd en eksisterende Azure AD B2C lejer til mit Azure-abonnement**.
        1. Vælg den relevante B2C-lejer for **Azure AD B2C-lejer**. Hvis meddelelsen "Der ikke blev fundet nogen berettiget B2C-lejer" vises i valgfeltet, har du ikke en eksisterende berettiget B2C-lejer og skal oprette en ny.
        1. Vælg **Opret ny** for **Ressourcegruppe**. Angiv et **Navn** på den ressourcegruppe, der skal indeholde lejeren, Vælg **Ressourcegruppens lokalitet**, og vælg derefter **Opret**.

    ![Sammenkæd en eksisterende Azure AD B2C-lejer med mit Azure-abonnement.](./media/B2CImage_3.png)

1. Når den nye Azure AD B2C-mappe er oprettet (det kan tage et øjeblik), vises der et link til den nye mappe på dashboardet. Dette link vil føre dig til siden "Velkommen til Azure Active Directory B2C".

    ![Sammenkæde med ny Azure AD-mappe](./media/B2CImage_4.png)

> [!NOTE]
> Hvis du har flere abonnementer til din Azure-konto eller har konfigureret B2C-lejeren uden at oprette forbindelse til et aktivt abonnement, kan du bruge banneret **Fejlfinding** til at knytte lejeren til et abonnement. Vælg fejlfindingsmeddelelsen, og følg instruktionerne for at løse abonnementsproblemet.

I følgende billede vises et eksempel på et Azure AD B2C-banner til **Fejlfinding**.

![Advarsel viser, at mappen ikke har noget aktivt abonnement.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Næste trin

Hvis du vil fortsætte med at konfigurere en B2C-lejer i Commerce, skal du fortsætte til [Opret B2C-ansøgning](create-b2c-app.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en B2C-lejer i Commerce](set-up-b2c-tenant.md)

[Opret B2C-programmet](create-b2c-app.md)

[Oprette politikker for brugerstrøm](create-user-flow-policies.md)

[Tilføj sociale identitetsudbydere (valgfrit)](add-social-identity-providers.md)

[Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger](update-hq-aad-b2c-info.md)

[Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren](config-b2c-tenant-site-builder.md)

[Flere B2C-oplysninger](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
