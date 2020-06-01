---
title: Konfigurieren eines Identitätswechsels
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: efcef39f-e26d-4eed-95ac-36a5bf8c089f
description: Erfahren Sie, wie Sie einem Dienstkonto mithilfe der Exchange-Verwaltungsshell die Identitätswechselrolle gewähren können.
localization_priority: Priority
ms.openlocfilehash: f8fe95536213e347840af082d765a9cc2fbce819
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455898"
---
# <a name="configure-impersonation"></a><span data-ttu-id="9421d-103">Konfigurieren eines Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="9421d-103">Configure impersonation</span></span>

<span data-ttu-id="9421d-104">Erfahren Sie, wie Sie einem Dienstkonto mithilfe der Exchange-Verwaltungsshell die Identitätswechselrolle gewähren können.</span><span class="sxs-lookup"><span data-stu-id="9421d-104">Learn how to grant the impersonation role to a service account by using the Exchange Management Shell.</span></span> 
  
<span data-ttu-id="9421d-p101">Durch den Identitätswechsel kann ein Aufrufer wie eine Dienstanwendung ein Benutzerkonto imitieren. Der Aufrufer kann Vorgänge mithilfe der Berechtigungen durchführen, die dem imitierten Konto zugewiesen sind, statt die dem Aufruferkonto zugewiesenen Berechtigungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9421d-p101">Impersonation enables a caller, such as a service application, to impersonate a user account. The caller can perform operations by using the permissions that are associated with the impersonated account instead of the permissions associated with the caller's account.</span></span>
  
<span data-ttu-id="9421d-p102">Exchange Online, Exchange Online als Teil von Office 365 und Versionen von Exchange ab Exchange 2013 verwenden die rollenbasierte Zugriffssteuerung (RBAC), um Konten Berechtigungen zu gewähren. Ihr Exchange-Serveradministrator muss den Dienstkonten die **ApplicationImpersonation**-Rolle mithilfe des [New-ManagementRoleAssignment](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)-Cmdlets gewähren, die andere Benutzer imitieren.</span><span class="sxs-lookup"><span data-stu-id="9421d-p102">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013 use role-based access control (RBAC) to assign permissions to accounts. Your Exchange server administrator will need to grant any service account that will be impersonating other users the **ApplicationImpersonation** role by using the [New-ManagementRoleAssignment](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet.</span></span> 
  
## <a name="configuring-the-applicationimpersonation-role"></a><span data-ttu-id="9421d-109">Konfigurieren der ApplicationImpersonation-Rolle</span><span class="sxs-lookup"><span data-stu-id="9421d-109">Configuring the ApplicationImpersonation role</span></span>

<span data-ttu-id="9421d-110">Verwenden Sie oder Ihr Exchange-Serveradministrator beim Zuweisen der **ApplicationImpersonation**-Rolle folgende Parameter des **New-ManagementRoleAssignment**-Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="9421d-110">When you or your Exchanger server administrator assigns the **ApplicationImpersonation** role, use the following parameters of the **New-ManagementRoleAssignment** cmdlet:</span></span> 
  
-  <span data-ttu-id="9421d-111">_Name_ &ndash; Der Anzeigename der Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="9421d-111">_Name_ &ndash; The friendly name of the role assignment.</span></span> <span data-ttu-id="9421d-112">Jedes Mal, wenn eine Rolle zugewiesen wird, wird ein Eintrag in der Liste der RBAC-Rollen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="9421d-112">Each time that you assign a role, an entry is made in the RBAC roles list.</span></span> <span data-ttu-id="9421d-113">Verwenden Sie das Cmdlet [Get-ManagementRoleAssignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx), um Rollenzuweisungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9421d-113">You can verify role assignments by using the [Get-ManagementRoleAssignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
    
-  <span data-ttu-id="9421d-114">_Role_ &ndash; Die zuzuweisende RBAC-Rolle.</span><span class="sxs-lookup"><span data-stu-id="9421d-114">_Role_ &ndash; The RBAC role to assign.</span></span> <span data-ttu-id="9421d-115">Beim Einrichten des Identitätswechsels weisen Sie die **ApplicationImpersonation**-Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="9421d-115">When you set up impersonation, you assign the **ApplicationImpersonation** role.</span></span> 
    
-  <span data-ttu-id="9421d-116">_User_ &ndash; Das Dienstkonto.</span><span class="sxs-lookup"><span data-stu-id="9421d-116">_User_ &ndash; The service account.</span></span> 
    
-  <span data-ttu-id="9421d-117">_CustomRecipientScope_ &ndash; Der Benutzerumfang, den das Benutzerkonto imitieren kann.</span><span class="sxs-lookup"><span data-stu-id="9421d-117">_CustomRecipientScope_ &ndash; The scope of users that the service account can impersonate.</span></span> <span data-ttu-id="9421d-118">Das Dienstkonto darf den Identitätswechsel nur für andere Benutzer innerhalb des angegebenen Bereichs zulassen.</span><span class="sxs-lookup"><span data-stu-id="9421d-118">The service account will only be allowed to impersonate other users within the specified scope.</span></span> <span data-ttu-id="9421d-119">Wenn kein Umfang angegeben ist, wird dem Dienstkonto die **ApplicationImpersonation**-Rolle für alle Benutzer in einem Unternehmen gewährt.</span><span class="sxs-lookup"><span data-stu-id="9421d-119">If no scope is specified, the service account is granted the **ApplicationImpersonation** role over all users in an organization.</span></span> <span data-ttu-id="9421d-120">Sie können benutzerdefinierte Verwaltungsbereiche mithilfe des [New-ManagementScope](https://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx)-Cmdlets angeben.</span><span class="sxs-lookup"><span data-stu-id="9421d-120">You can create custom management scopes by using the [New-ManagementScope](https://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet.</span></span> 
    
<span data-ttu-id="9421d-121">Bevor Sie den Identitätswechsel konfigurieren, benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9421d-121">Before you can configure impersonation, you need:</span></span>
  
- <span data-ttu-id="9421d-122">Administratoranmeldeinformationen für den Exchange-Server</span><span class="sxs-lookup"><span data-stu-id="9421d-122">Administrative credentials for the Exchange server.</span></span>
    
- <span data-ttu-id="9421d-123">Domänenadministrator-Anmeldeinformationen oder andere Anmeldeinformationen mit der Berechtigung zum Erstellen und Zuweisen von Rollen und Bereichen</span><span class="sxs-lookup"><span data-stu-id="9421d-123">Domain Administrator credentials, or other credentials with the permission to create and assign roles and scopes.</span></span>
    
- <span data-ttu-id="9421d-p106">Exchange-Verwaltungstools. Sie werden auf dem Computer installiert, über den Sie die Befehle ausführen.</span><span class="sxs-lookup"><span data-stu-id="9421d-p106">Exchange management tools. These are installed on the computer from which you will run the commands.</span></span>
    
### <a name="to-configure-impersonation-for-all-users-in-an-organization"></a><span data-ttu-id="9421d-126">So konfigurieren Sie den Identitätswechsel für alle Benutzer in einem Unternehmen</span><span class="sxs-lookup"><span data-stu-id="9421d-126">To configure impersonation for all users in an organization</span></span>

1. <span data-ttu-id="9421d-127">Öffnen Sie die Exchange-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="9421d-127">Open the Exchange Management Shell.</span></span> <span data-ttu-id="9421d-128">Wählen Sie im Startmenü **Alle Programme** > **Microsoft Exchange Server 2013**.</span><span class="sxs-lookup"><span data-stu-id="9421d-128">From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="9421d-p108">Führen Sie das **New-ManagementRoleAssignment**-Cmdlet aus, um die Identitätswechselberechtigung für den angegebenen Benutzer hinzuzufügen. Im folgenden Beispiel wird veranschaulicht, wie man den Identitätswechsel konfigurieren muss, damit ein Dienstkonto alle anderen Benutzer in einem Unternehmen imitieren kann.</span><span class="sxs-lookup"><span data-stu-id="9421d-p108">Run the **New-ManagementRoleAssignment** cmdlet to add the impersonation permission to the specified user. The following example shows how to configure impersonation to enable a service account to impersonate all other users in an organization.</span></span> 
    
   ```powershell
   New-ManagementRoleAssignment -name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount 
   ```

### <a name="to-configure-impersonation-for-specific-users-or-groups-of-users"></a><span data-ttu-id="9421d-131">So konfigurieren Sie den Identitätswechsel für bestimmte Benutzer oder Benutzergruppen</span><span class="sxs-lookup"><span data-stu-id="9421d-131">To configure impersonation for specific users or groups of users</span></span>

1. <span data-ttu-id="9421d-p109">Öffnen Sie die Exchange-Verwaltungsshell. Wählen Sie im Startmenü **Alle Programme** > **Microsoft Exchange Server 2013**.</span><span class="sxs-lookup"><span data-stu-id="9421d-p109">Open the Exchange Management Shell. From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="9421d-p110">Führen Sie das **New-ManagementScope**-Cmdlet aus, um einen Bereich zu erstellen, dem die Identitätswechselrolle zugewiesen werden kann. Wenn ein vorhandener Bereich verfügbar ist, können Sie diesen Schritt überspringen. Im folgenden Beispiel wird veranschaulicht, wie ein Verwaltungsbereich für eine bestimmte Gruppe erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9421d-p110">Run the **New-ManagementScope** cmdlet to create a scope to which the impersonation role can be assigned. If an existing scope is available, you can skip this step. The following example shows how to create a management scope for a specific group.</span></span> 
    
   ```powershell
    New-ManagementScope -Name:scopeName -RecipientRestrictionFilter:recipientFilter
   ```

   <span data-ttu-id="9421d-137">Der _RecipientRestrictionFilter_-Parameter des **New-ManagementScope**-Cmdlets definiert die Elemente des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="9421d-137">The _RecipientRestrictionFilter_ parameter of the **New-ManagementScope** cmdlet defines the members of the scope.</span></span> <span data-ttu-id="9421d-138">Sie können die Eigenschaften des **Identity**-Objekt verwenden, um den Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9421d-138">You can use the properties of the **Identity** object to create the filter.</span></span> <span data-ttu-id="9421d-139">Das folgende Beispiel ist ein Filter, der das Ergebnis auf einen einzelnen Benutzer mit dem Benutzernamen „John" begrenzt.</span><span class="sxs-lookup"><span data-stu-id="9421d-139">The following example is a filter that restricts the result to a single user with the user name "john."</span></span> 
    
   ```powershell
   Name -eq "john"
   ```

3. <span data-ttu-id="9421d-p112">Führen Sie das **New-ManagementRoleAssignment**-Cmdlet aus, um die Berechtigung zum Imitieren der Elemente des angegebenen Bereichs hinzuzufügen. Im folgenden Beispiel wird veranschaulicht, wie ein Dienstkonto zum Imitieren aller Benutzer in einem Bereich konfiguriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="9421d-p112">Run the **New-ManagementRoleAssignment** cmdlet to add the permission to impersonate the members of the specified scope. The following example shows how to configure a service account to impersonate all users in a scope.</span></span> 
    
   ```powershell
    New-ManagementRoleAssignment -Name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount -CustomRecipientWriteScope:scopeName
    
   ```


<span data-ttu-id="9421d-p113">Nachdem der Administrator die Identitätswechsel-Berechtigungen gewährt hat, können Sie das Dienstkonto verwenden, um Aufrufe zu anderen Benutzerkonten auszuführen. Sie können die Rollenzuweisungen mithilfe des [Get-ManagementRoleAssignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)-Cmdlets verifizieren.</span><span class="sxs-lookup"><span data-stu-id="9421d-p113">After your administrator grants impersonation permissions, you can use the service account to make calls against other users' accounts. You can verify role assignments by using the [Get-ManagementRoleAssignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9421d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9421d-144">See also</span></span>

- [<span data-ttu-id="9421d-145">Identitätswechsel und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9421d-145">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
- [<span data-ttu-id="9421d-146">ApplicationImpersonation-Rolle</span><span class="sxs-lookup"><span data-stu-id="9421d-146">ApplicationImpersonation role</span></span>](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)   
- [<span data-ttu-id="9421d-147">New-ManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9421d-147">New-ManagementRoleAssignment</span></span>](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)    
- [<span data-ttu-id="9421d-148">Get-ManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9421d-148">Get-ManagementRoleAssignment</span></span>](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)
    

