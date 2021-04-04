---
title: Begrænse redigering af personlige oplysninger
description: Begrænse medarbejdere i at redigere kontaktoplysninger i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4785232dbb21c5f8a800497fb0cfd3c64dea2d8
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/05/2021
ms.locfileid: "5503030"
---
# <a name="restrict-editing-of-personal-information"></a>Begrænse redigering af personlige oplysninger

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Dette emne beskriver, hvordan du begrænser medarbejdernes mulighed for at redigere kontaktoplysninger i Dynamics 365 Human Resources. Du kan f.eks. forhindre medarbejdere i at redigere bestemte kontaktoplysninger, f.eks. deres firmaadresse eller mailadresse.

> [!NOTE]
> Hvis du vil bruge denne funktion, skal du først aktivere **(Forhåndsversion) Begrænse medarbejdere i at tilføje eller redigere adresse- og kontaktoplysninger til udvalgte formål** i Funktionsstyring. Du kan finde flere oplysninger om aktivering af prøveversionsfunktioner i [Administrere funktioner](hr-admin-manage-features.md).<br><br>![Aktivér visningsfunktion](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Vælge de oplysninger, som en medarbejder kan tilføje eller redigere

1. I Human Resources skal du vælge **Personalestyring**, vælge **Links** og derefter vælge **Human Resources-parametre**.

   ![Gå til Personaleparametre](./media/hr-employee-self-service-human-resources-parameters.png)

2. Vælg fanen **Medarbejderselvbetjening** på siden **Personaleparametre**.

   ![Medarbejderselvbetjening](./media/hr-employee-self-service-tab.png)

3. Under fanen **Medarbejderselvbetjening** skal du fjerne markeringen af alle oplysninger i afsnittet **Adresse- og kontaktoplysninger**, som du ikke ønsker, at medarbejdere skal tilføje eller redigere. I dette eksempel har vi ikke markeret **Forretningskontaktoplysninger**.

   ![Begrænse redigeringen af forretningskontaktoplysninger](./media/hr-employee-self-service-restrict-business.png)

4. Vælg **Gem**.

   ![Gem ændringer](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Medarbejdererfaring

Når du har begrænset medarbejdernes adgang til at tilføje eller redigere kontaktoplysninger, kan de se oplysningerne, men de kan ikke ændre dem.

I dette eksempel, hvor medarbejdere ikke kan redigere **forretningskontaktoplysninger**, kan de stadig se oplysningerne i Medarbejderselvbetjening:

![Se forretningskontaktoplysninger](./media/hr-employee-self-service-restrict-view.png)

Men når de vælger forretningskontaktoplysninger, vises ruden **Rediger adresse** som skrivebeskyttet, og de kan ikke ændre nogen af felterne.

![Forretningskontaktoplysninger vises som skrivebeskyttede](./media/hr-employee-self-service-restrict-read-only.png)

Hvis de vælger **Tilføj** for at tilføje en ny adresse, kan de heller ikke vælge **Forretning** på rullelisten **Formål**.

![Medarbejderen kan ikke tilføje en forretningsadresse](./media/hr-employee-self-service-restrict-add.png)

Medarbejdere får samme erfaring, når de vælger **Kontaktoplysninger** på siden **Personlige oplysninger** og tilføjer en ny adresse. På rullelisten **Formål** vises kun de typer oplysninger, de kan tilføje. 

![Medarbejderen kan ikke vælge Forretning på rullelisten Formål](./media/hr-employee-self-service-restrict-purpose.png)

**Kontaktoplysninger** viser nu **Formål** i gitteret.

![Formål vises i gitteret Kontaktoplysninger](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Se også

[Oversigt over medarbejder- og lederselvbetjening](hr-employee-manager-self-service-overview.md)<br>
[Konfigurere Human Resources-parametre](hr-setup-parameters.md)<br>
[Rediger personlige oplysninger](hr-employee-manager-self-service-edit-personal-information.md)