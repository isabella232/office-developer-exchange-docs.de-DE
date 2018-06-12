---
title: Konfigurieren des Identitätswechsels
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: efcef39f-e26d-4eed-95ac-36a5bf8c089f
description: Erfahren Sie, wie Sie einem Dienstkonto mithilfe der Exchange-Verwaltungsshell die Identitätswechselrolle gewähren können.
ms.openlocfilehash: 57ccef48a7553bcc06e3b3ae940b376b8555ef84
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756875"
---
# <a name="configure-impersonation"></a><span data-ttu-id="5c788-103">Konfigurieren des Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="5c788-103">Configure impersonation</span></span>

<span data-ttu-id="5c788-104">Erfahren Sie, wie Sie einem Dienstkonto mithilfe der Exchange-Verwaltungsshell die Identitätswechselrolle gewähren können.</span><span class="sxs-lookup"><span data-stu-id="5c788-104">Learn how to grant the impersonation role to a service account by using the Exchange Management Shell.</span></span> 
  
<span data-ttu-id="5c788-p101">Durch den Identitätswechsel kann ein Aufrufer wie eine Dienstanwendung ein Benutzerkonto imitieren. Der Aufrufer kann Vorgänge mithilfe der Berechtigungen durchführen, die dem imitierten Konto zugewiesen sind, statt die dem Aufruferkonto zugewiesenen Berechtigungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c788-p101">Impersonation enables a caller, such as a service application, to impersonate a user account. The caller can perform operations by using the permissions that are associated with the impersonated account instead of the permissions associated with the caller's account.</span></span>
  
<span data-ttu-id="5c788-p102">Exchange Online, Exchange Online als Teil von Office 365 und Versionen von Exchange ab Exchange 2013 verwenden die rollenbasierte Zugriffssteuerung (RBAC), um Konten Berechtigungen zu gewähren. Ihr Exchange-Serveradministrator muss den Dienstkonten die **ApplicationImpersonation**-Rolle mithilfe des [New-ManagementRoleAssignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)-Cmdlets gewähren, die andere Benutzer imitieren.</span><span class="sxs-lookup"><span data-stu-id="5c788-p102">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013 use role-based access control (RBAC) to assign permissions to accounts. Your Exchange server administrator will need to grant any service account that will be impersonating other users the **ApplicationImpersonation** role by using the [New-ManagementRoleAssignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet.</span></span> 
  
## <a name="configuring-the-applicationimpersonation-role"></a><span data-ttu-id="5c788-109">Konfigurieren der ApplicationImpersonation-Rolle</span><span class="sxs-lookup"><span data-stu-id="5c788-109">Configuring the ApplicationImpersonation role</span></span>

<span data-ttu-id="5c788-110">Verwenden Sie oder Ihr Exchange-Serveradministrator beim Zuweisen der **ApplicationImpersonation**-Rolle folgende Parameter des **New-ManagementRoleAssignment**-Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="5c788-110">When you or your Exchanger server administrator assigns the **ApplicationImpersonation** role, use the following parameters of the **New-ManagementRoleAssignment** cmdlet:</span></span> 
  
-  <span data-ttu-id="5c788-111">_Name_ &ndash; Den Anzeigenamen der rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="5c788-111">_Name_ &ndash; The friendly name of the role assignment.</span></span> <span data-ttu-id="5c788-112">Beim Zuweisen einer Rolle erfolgt ein Eintrag in der RBAC-Rollenliste.</span><span class="sxs-lookup"><span data-stu-id="5c788-112">Each time that you assign a role, an entry is made in the RBAC roles list.</span></span> <span data-ttu-id="5c788-113">Sie können Rollenzuweisungen mithilfe des [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)-Cmdlets verifizieren.</span><span class="sxs-lookup"><span data-stu-id="5c788-113">You can verify role assignments by using the [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
    
-  <span data-ttu-id="5c788-114">_Rolle_ &ndash; Der RBAC-Rolle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="5c788-114">_Role_ &ndash; The RBAC role to assign.</span></span> <span data-ttu-id="5c788-115">Beim Einrichten des Identitätswechsels weisen Sie die **ApplicationImpersonation**-Rolle zu.</span><span class="sxs-lookup"><span data-stu-id="5c788-115">When you set up impersonation, you assign the **ApplicationImpersonation** role.</span></span> 
    
-  <span data-ttu-id="5c788-116">_Benutzer_ &ndash; Das Dienstkonto.</span><span class="sxs-lookup"><span data-stu-id="5c788-116">_User_ &ndash; The service account.</span></span> 
    
-  <span data-ttu-id="5c788-117">_CustomRecipientScope_ &ndash; Des Umfangs der Benutzer, die das Dienstkonto imitieren kann.</span><span class="sxs-lookup"><span data-stu-id="5c788-117">_CustomRecipientScope_ &ndash; The scope of users that the service account can impersonate.</span></span> <span data-ttu-id="5c788-118">Das Dienstkonto kann nur Benutzer innerhalb des angegebenen Umfangs imitieren.</span><span class="sxs-lookup"><span data-stu-id="5c788-118">The service account will only be allowed to impersonate other users within the specified scope.</span></span> <span data-ttu-id="5c788-119">Wenn kein Umfang angegeben ist, wird dem Dienstkonto die **ApplicationImpersonation**-Rolle für alle Benutzer in einem Unternehmen gewährt.</span><span class="sxs-lookup"><span data-stu-id="5c788-119">If no scope is specified, the service account is granted the **ApplicationImpersonation** role over all users in an organization.</span></span> <span data-ttu-id="5c788-120">Sie können benutzerdefinierte Verwaltungsbereiche mithilfe des [New-ManagementScope](http://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx)-Cmdlets angeben.</span><span class="sxs-lookup"><span data-stu-id="5c788-120">You can create custom management scopes by using the [New-ManagementScope](http://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet.</span></span> 
    
<span data-ttu-id="5c788-121">Bevor Sie den Identitätswechsel konfigurieren, benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5c788-121">Before you can configure impersonation, you need:</span></span>
  
- <span data-ttu-id="5c788-122">Administratoranmeldeinformationen für den Exchange-Server</span><span class="sxs-lookup"><span data-stu-id="5c788-122">Administrative credentials for the Exchange server.</span></span>
    
- <span data-ttu-id="5c788-123">Domänenadministrator-Anmeldeinformationen oder andere Anmeldeinformationen mit der Berechtigung zum Erstellen und Zuweisen von Rollen und Bereichen</span><span class="sxs-lookup"><span data-stu-id="5c788-123">Domain Administrator credentials, or other credentials with the permission to create and assign roles and scopes.</span></span>
    
- <span data-ttu-id="5c788-p106">Exchange-Verwaltungstools. Sie werden auf dem Computer installiert, über den Sie die Befehle ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c788-p106">Exchange management tools. These are installed on the computer from which you will run the commands.</span></span>
    
### <a name="to-configure-impersonation-for-all-users-in-an-organization"></a><span data-ttu-id="5c788-126">So konfigurieren Sie den Identitätswechsel für alle Benutzer in einem Unternehmen</span><span class="sxs-lookup"><span data-stu-id="5c788-126">To configure impersonation for all users in an organization</span></span>

1. <span data-ttu-id="5c788-p107">Öffnen Sie die Exchange-Verwaltungsshell. Wählen Sie im Startmenü **Alle Programme** > **Microsoft Exchange Server 2013**.</span><span class="sxs-lookup"><span data-stu-id="5c788-p107">Open the Exchange Management Shell. From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="5c788-p108">Führen Sie das **New-ManagementRoleAssignment**-Cmdlet aus, um die Identitätswechselberechtigung für den angegebenen Benutzer hinzuzufügen. Im folgenden Beispiel wird veranschaulicht, wie man den Identitätswechsel konfigurieren muss, damit ein Dienstkonto alle anderen Benutzer in einem Unternehmen imitieren kann.</span><span class="sxs-lookup"><span data-stu-id="5c788-p108">Run the **New-ManagementRoleAssignment** cmdlet to add the impersonation permission to the specified user. The following example shows how to configure impersonation to enable a service account to impersonate all other users in an organization.</span></span> 
    
   ```powershell
   New-ManagementRoleAssignment -name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount 
   ```

### <a name="to-configure-impersonation-for-specific-users-or-groups-of-users"></a><span data-ttu-id="5c788-131">So konfigurieren Sie den Identitätswechsel für bestimmte Benutzer oder Benutzergruppen</span><span class="sxs-lookup"><span data-stu-id="5c788-131">To configure impersonation for specific users or groups of users</span></span>

1. <span data-ttu-id="5c788-p109">Öffnen Sie die Exchange-Verwaltungsshell. Wählen Sie im Startmenü **Alle Programme** > **Microsoft Exchange Server 2013**.</span><span class="sxs-lookup"><span data-stu-id="5c788-p109">Open the Exchange Management Shell. From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="5c788-p110">Führen Sie das **New-ManagementScope**-Cmdlet aus, um einen Bereich zu erstellen, dem die Identitätswechselrolle zugewiesen werden kann. Wenn ein vorhandener Bereich verfügbar ist, können Sie diesen Schritt überspringen. Im folgenden Beispiel wird veranschaulicht, wie ein Verwaltungsbereich für eine bestimmte Gruppe erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5c788-p110">Run the **New-ManagementScope** cmdlet to create a scope to which the impersonation role can be assigned. If an existing scope is available, you can skip this step. The following example shows how to create a management scope for a specific group.</span></span> 
    
   ```powershell
    New-ManagementScope -Name:scopeName -RecipientRestrictionFilter:recipientFilter
   ```

   <span data-ttu-id="5c788-137">Der Parameter _RecipientRestrictionFilter_ des Cmdlets **New-ManagementScope** definiert die Member des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="5c788-137">The _RecipientRestrictionFilter_ parameter of the **New-ManagementScope** cmdlet defines the members of the scope.</span></span> <span data-ttu-id="5c788-138">Sie können die Eigenschaften des **Identity**-Objekts verwenden, um den Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c788-138">You can use the properties of the **Identity** object to create the filter.</span></span> <span data-ttu-id="5c788-139">Das folgende Beispiel ist ein Filter, der das Ergebnis auf einen einzelnen Benutzer mit dem Benutzernamen „John" begrenzt.</span><span class="sxs-lookup"><span data-stu-id="5c788-139">The following example is a filter that restricts the result to a single user with the user name "john."</span></span> 
    
   ```powershell
   Name -eq "john"
   ```

3. <span data-ttu-id="5c788-p112">Führen Sie das **New-ManagementRoleAssignment**-Cmdlet aus, um die Berechtigung zum Imitieren der Elemente des angegebenen Bereichs hinzuzufügen. Im folgenden Beispiel wird veranschaulicht, wie ein Dienstkonto zum Imitieren aller Benutzer in einem Bereich konfiguriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="5c788-p112">Run the **New-ManagementRoleAssignment** cmdlet to add the permission to impersonate the members of the specified scope. The following example shows how to configure a service account to impersonate all users in a scope.</span></span> 
    
   ```powershell
    New-ManagementRoleAssignment -Name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount -CustomRecipientWriteScope:scopeName
    
   ```


<span data-ttu-id="5c788-p113">Nachdem der Administrator die Identitätswechsel-Berechtigungen gewährt hat, können Sie das Dienstkonto verwenden, um Aufrufe zu anderen Benutzerkonten auszuführen. Sie können die Rollenzuweisungen mithilfe des [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)-Cmdlets verifizieren.</span><span class="sxs-lookup"><span data-stu-id="5c788-p113">After your administrator grants impersonation permissions, you can use the service account to make calls against other users' accounts. You can verify role assignments by using the [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c788-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c788-144">See also</span></span>

- [<span data-ttu-id="5c788-145">Identitätswechsel und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="5c788-145">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
- [<span data-ttu-id="5c788-146">ApplicationImpersonation-Rolle</span><span class="sxs-lookup"><span data-stu-id="5c788-146">ApplicationImpersonation role</span></span>](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)   
- [<span data-ttu-id="5c788-147">New-ManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5c788-147">New-ManagementRoleAssignment</span></span>](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)    
- [<span data-ttu-id="5c788-148">Get-ManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5c788-148">Get-ManagementRoleAssignment</span></span>](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)
    
