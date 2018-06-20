---
title: Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: Erfahren Sie, wie Berechtigungsstufen für einen Ordner festlegen, indem verwenden die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 5bf570612d6349628e7f3abf858daa33daa13745
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757004"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a><span data-ttu-id="e0ef8-103">Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0ef8-103">Set folder permissions for another user by using EWS in Exchange</span></span>

<span data-ttu-id="e0ef8-104">Erfahren Sie, wie Berechtigungsstufen für einen Ordner festlegen, indem verwenden die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-104">Learn how to set permission levels on a folder by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="e0ef8-105">Berechtigungen auf Ordnerebene können Benutzer einen oder mehrere Ordner im Postfach eines anderen Benutzers zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-105">Folder-level permissions enable users to access one or more folders in another user's mailbox.</span></span> <span data-ttu-id="e0ef8-106">Ordnerberechtigungen ähneln Zugriff delegieren, jedoch unterscheiden sich wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e0ef8-106">Folder permissions are similar to delegate access, but they differ in the following ways:</span></span> 
  
- <span data-ttu-id="e0ef8-107">Berechtigungen für Ordner aktivieren ein Benutzers zum "Senden im Auftrag von" und "Senden als" eines anderen Benutzers nicht.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-107">Folder permissions do not enable a user to "send on behalf of" or "send as" another user.</span></span> <span data-ttu-id="e0ef8-108">Sie ermöglichen nur Zugriff auf Ordner.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-108">They only enable access to folders.</span></span> <span data-ttu-id="e0ef8-109">Benutzer können Elemente in diesen Ordnern erstellen, aber er können nicht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-109">Users can create items in those folders, but they can't send them.</span></span>
    
- <span data-ttu-id="e0ef8-110">Sie können Ordnerberechtigungen für alle Ordner im Postfach festlegen, aber Sie können nur eine Stellvertretung den Ordner Kalender, Kontakte, Posteingang, Journal, Notizen und Aufgaben hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-110">You can set folder permissions on any folder in the mailbox, but you can only add a delegate to the Calendar, Contacts, Inbox, Journal, Notes, and Tasks folders.</span></span>
    
- <span data-ttu-id="e0ef8-111">Sie können eine Reihe von [Berechtigungen für einen bestimmten Ordner](#bk_folderperms)festlegen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-111">You can set a number of [permissions on a specific folder](#bk_folderperms).</span></span> <span data-ttu-id="e0ef8-112">Wenn Sie eine Stellvertretung hinzugefügt haben, können Sie nur [fünf Berechtigungsstufen](delegate-access-and-ews-in-exchange.md#bk_delegateperms)zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-112">When you add a delegate, you can assign one of only [five permission levels](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span>
    
- <span data-ttu-id="e0ef8-113">Sie können legen Sie Berechtigungen für anonyme und Standard-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-113">You can set folder permissions for anonymous and default users.</span></span> <span data-ttu-id="e0ef8-114">Sie können nur Delegieren des Zugriffs auf ein e-Mail-aktiviertes Konto erteilen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-114">You can only grant delegate access to a mail-enabled account.</span></span>
    
<span data-ttu-id="e0ef8-115">Wenn Sie mit Access Control Entries, (Zugriffssteuerungseinträge ACEs) und Discretionary Access Control Lists () vertraut sind, wissen Sie, dass ein Benutzer nur ein Satz von Berechtigungen für jeden Ordner ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-115">If you're familiar with Access Control Entries (ACEs) and Discretionary Access Control Lists (DACLs), you know that a user can only have one set of permissions for each folder.</span></span> <span data-ttu-id="e0ef8-116">Wenn Sie versuchen, eine Reihe von Berechtigungen für einen Benutzer hinzuzufügen, und sie bereits eine Reihe von Berechtigungen besitzen, erhalten Sie einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-116">If you try to add a set of permissions for a user and they already have a set of permissions, you'll get an error.</span></span> <span data-ttu-id="e0ef8-117">Wenn Sie hinzufügen, entfernen oder aktualisieren Sie die Berechtigungen für einen Ordner, Sie erhalten die aktuelle DACL, hinzufügen oder Entfernen von ACEs, und senden Sie die aktualisierte DACL.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-117">When you add, remove, or update permissions on a folder, you get the current DACL, add or remove any ACEs, and then send the updated DACL.</span></span> <span data-ttu-id="e0ef8-118">Sie können nicht mehrere ACEs für denselben Benutzer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-118">You cannot add multiple ACEs for the same user.</span></span> <span data-ttu-id="e0ef8-119">Wenn Sie Berechtigungen mithilfe der EWS Managed API aktualisieren, müssen Sie aktuelle ACE des Benutzers zu entfernen, und fügen Sie ihrer neuen ACE der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-119">When you update permissions by using the EWS Managed API, you need to remove the user's current ACE and then add their new ACE to the collection.</span></span> <span data-ttu-id="e0ef8-120">Wenn Sie Exchange-Webdienste verwenden, ersetzen Sie den vorherigen Satz von ACEs, die nur durch die neue.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-120">If you're using EWS, you just replace the previous set of ACEs with the new ones.</span></span>
  
<span data-ttu-id="e0ef8-121">Wenn Sie mehrere Berechtigung Änderungen in einem einzelnen Ordner durchführen, können Sie batch hinzugefügt, entfernt oder Updates – Beachten Sie, dass Sie benutzeraktualisierungen in mehreren Ordnern batch ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-121">If you're making multiple permission changes to a single folder, you can batch additions, removals, or updates —just note that you cannot batch user updates on multiple folders.</span></span> <span data-ttu-id="e0ef8-122">Ein Anruf ist erforderlich, um die Berechtigungen für einen einzelnen Ordner erhalten möchten, und ein zweiter Aufruf ist erforderlich, um die Berechtigungen für diesen Ordner zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-122">One call is required to get the permissions on a single folder, and a second call is required to update the permissions on that folder.</span></span> <span data-ttu-id="e0ef8-123">Wenn Sie hinzufügen, entfernen oder von Benutzerberechtigungen aktualisieren, verwenden Sie die gleichen zwei-Methodenaufrufen oder Vorgänge für jeden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-123">When you add, remove, or update user permissions, you use the same two method calls or operations for each task.</span></span>
  
<span data-ttu-id="e0ef8-124">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Festlegen von Berechtigungen für Ordner**</span><span class="sxs-lookup"><span data-stu-id="e0ef8-124">**Table 1. EWS Managed API methods and EWS operations for setting folder permissions**</span></span>

|<span data-ttu-id="e0ef8-125">Aktion</span><span class="sxs-lookup"><span data-stu-id="e0ef8-125">If you want to…</span></span>|<span data-ttu-id="e0ef8-126">Verwenden Sie diese Methode EWS Managed API...</span><span class="sxs-lookup"><span data-stu-id="e0ef8-126">Use this EWS Managed API method…</span></span>|<span data-ttu-id="e0ef8-127">Verwenden Sie diese Operation EWS...</span><span class="sxs-lookup"><span data-stu-id="e0ef8-127">Use this EWS operation…</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0ef8-128">Aktivieren, entfernen oder Aktualisieren von Berechtigungen für Ordner</span><span class="sxs-lookup"><span data-stu-id="e0ef8-128">Enable, remove, or update folder permissions</span></span>  <br/> |<span data-ttu-id="e0ef8-129">[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) gefolgt von [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0ef8-129">[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) followed by [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="e0ef8-130">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) gefolgt von [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0ef8-130">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) followed by [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="e0ef8-131">Erstellen Sie einen Ordner, und definieren Sie Berechtigungen für Ordner</span><span class="sxs-lookup"><span data-stu-id="e0ef8-131">Create a folder and define folder permissions</span></span>  <br/> |[<span data-ttu-id="e0ef8-132">Folder.Save</span><span class="sxs-lookup"><span data-stu-id="e0ef8-132">Folder.Save</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e0ef8-133">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="e0ef8-133">CreateFolder</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a><span data-ttu-id="e0ef8-134">Berechtigungen für Ordner</span><span class="sxs-lookup"><span data-stu-id="e0ef8-134">Folder permissions</span></span>
<span data-ttu-id="e0ef8-135"><a name="bk_folderperms"> </a></span><span class="sxs-lookup"><span data-stu-id="e0ef8-135"></span></span>

<span data-ttu-id="e0ef8-136">Sie haben eine Anzahl von Optionen, wenn es darum geht, Festlegen von Berechtigungen für einen bestimmten Ordner.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-136">You have quite a few options when it comes to setting folder permissions on a specific folder.</span></span> <span data-ttu-id="e0ef8-137">Setzen Sie eine Berechtigungsstufe für einen Ordner, für jeden Benutzer, die eine Reihe von vordefinierten einzelne Berechtigungen der DACL hinzufügt, oder Sie können einzelne Berechtigungen für einen Ordner festlegen – jedoch nicht möglich, mischen und übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-137">You can set a permission level on a folder for each user, which adds a set of predefined individual permissions to the DACL, or you can set individual permissions on a folder — but you can't mix and match.</span></span>
  
<span data-ttu-id="e0ef8-138">Die folgenden einzelnen Berechtigungen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="e0ef8-138">The following individual permissions are available:</span></span>
  
- <span data-ttu-id="e0ef8-139">Erstellen können</span><span class="sxs-lookup"><span data-stu-id="e0ef8-139">Can create</span></span>
- <span data-ttu-id="e0ef8-140">Unterordner können erstellen werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-140">Can create subfolders</span></span>    
- <span data-ttu-id="e0ef8-141">Ist der Besitzer des Ordners</span><span class="sxs-lookup"><span data-stu-id="e0ef8-141">Is folder owner</span></span>    
- <span data-ttu-id="e0ef8-142">Ordner ist sichtbar</span><span class="sxs-lookup"><span data-stu-id="e0ef8-142">Is folder visible</span></span>    
- <span data-ttu-id="e0ef8-143">Ordner Kontakt</span><span class="sxs-lookup"><span data-stu-id="e0ef8-143">Is folder contact</span></span>    
- <span data-ttu-id="e0ef8-144">Elemente bearbeiten</span><span class="sxs-lookup"><span data-stu-id="e0ef8-144">Edit items</span></span>    
- <span data-ttu-id="e0ef8-145">Löschen von Elementen</span><span class="sxs-lookup"><span data-stu-id="e0ef8-145">Delete items</span></span>    
- <span data-ttu-id="e0ef8-146">Elemente lesen</span><span class="sxs-lookup"><span data-stu-id="e0ef8-146">Read items</span></span>
    
<span data-ttu-id="e0ef8-147">Darüber hinaus stehen die folgenden Berechtigungsstufen, die definieren eine Teilmenge von einzelnen Berechtigungen und Werten, wie in Tabelle 2 gezeigt:</span><span class="sxs-lookup"><span data-stu-id="e0ef8-147">In addition, the following permission levels are available, which define a subset of individual permissions and values, as shown in Table 2:</span></span>
  
- <span data-ttu-id="e0ef8-148">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-148">None</span></span>    
- <span data-ttu-id="e0ef8-149">Besitzer</span><span class="sxs-lookup"><span data-stu-id="e0ef8-149">Owner</span></span>    
- <span data-ttu-id="e0ef8-150">Vom Typ PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="e0ef8-150">PublishingEditor</span></span>    
- <span data-ttu-id="e0ef8-151">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="e0ef8-151">Editor</span></span>    
- <span data-ttu-id="e0ef8-152">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="e0ef8-152">PublishingAuthor</span></span>    
- <span data-ttu-id="e0ef8-153">Autor</span><span class="sxs-lookup"><span data-stu-id="e0ef8-153">Author</span></span>    
- <span data-ttu-id="e0ef8-154">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="e0ef8-154">NoneditingAuthor</span></span>    
- <span data-ttu-id="e0ef8-155">Prüfer</span><span class="sxs-lookup"><span data-stu-id="e0ef8-155">Reviewer</span></span>    
- <span data-ttu-id="e0ef8-156">Mitwirkender</span><span class="sxs-lookup"><span data-stu-id="e0ef8-156">Contributor</span></span>   
- <span data-ttu-id="e0ef8-157">Benutzerdefinierte - dieser Wert kann nicht von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-157">Custom - This value cannot be set by the application.</span></span> <span data-ttu-id="e0ef8-158">Der Server legt diesen Wert, wenn die Anwendung benutzerdefinierte Zusammenstellung von einzelnen Berechtigungen enthält.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-158">The server sets this value if the application includes a custom collection of individual permissions.</span></span>    
- <span data-ttu-id="e0ef8-159">FreeBusyTimeOnly - kann dies nur für Kalenderordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-159">FreeBusyTimeOnly - This can only be set on Calendar folders.</span></span>   
- <span data-ttu-id="e0ef8-160">FreeBusyTimeAndSubjectAndLocation - kann dies nur für Kalenderordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-160">FreeBusyTimeAndSubjectAndLocation - This can only be set on Calendar folders.</span></span>
    
<span data-ttu-id="e0ef8-161">Die folgende Tabelle enthält die einzelnen Berechtigungen basierend auf Berechtigungsstufe standardmäßig angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-161">The following table shows which individual permissions are applied by default based on permission level.</span></span>
  
<span data-ttu-id="e0ef8-162">**In Tabelle 2. Einzelne Berechtigungen von Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="e0ef8-162">**Table 2. Individual permissions by permission level**</span></span>

|<span data-ttu-id="e0ef8-163">Berechtigungsstufe</span><span class="sxs-lookup"><span data-stu-id="e0ef8-163">Permission level</span></span>|<span data-ttu-id="e0ef8-164">Elemente können erstellen werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-164">Can create items</span></span>|<span data-ttu-id="e0ef8-165">Unterordner können erstellen werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-165">Can create sub folders</span></span>|<span data-ttu-id="e0ef8-166">Ist der Besitzer des Ordners</span><span class="sxs-lookup"><span data-stu-id="e0ef8-166">Is folder owner</span></span>|<span data-ttu-id="e0ef8-167">Ordner ist sichtbar</span><span class="sxs-lookup"><span data-stu-id="e0ef8-167">Is folder visible</span></span>|<span data-ttu-id="e0ef8-168">Ordner Kontakt</span><span class="sxs-lookup"><span data-stu-id="e0ef8-168">Is folder contact</span></span>|<span data-ttu-id="e0ef8-169">Elemente bearbeiten</span><span class="sxs-lookup"><span data-stu-id="e0ef8-169">Edit items</span></span>|<span data-ttu-id="e0ef8-170">Löschen von Elementen</span><span class="sxs-lookup"><span data-stu-id="e0ef8-170">Delete items</span></span>|<span data-ttu-id="e0ef8-171">Lesen von Elementen</span><span class="sxs-lookup"><span data-stu-id="e0ef8-171">Can read items</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e0ef8-172">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-172">None</span></span>  <br/> |<span data-ttu-id="e0ef8-173">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-173">False</span></span>  <br/> |<span data-ttu-id="e0ef8-174">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-174">False</span></span>  <br/> |<span data-ttu-id="e0ef8-175">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-175">False</span></span>  <br/> |<span data-ttu-id="e0ef8-176">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-176">False</span></span>  <br/> |<span data-ttu-id="e0ef8-177">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-177">False</span></span>  <br/> |<span data-ttu-id="e0ef8-178">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-178">None</span></span>  <br/> |<span data-ttu-id="e0ef8-179">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-179">None</span></span>  <br/> |<span data-ttu-id="e0ef8-180">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-180">None</span></span>  <br/> |
|<span data-ttu-id="e0ef8-181">Besitzer</span><span class="sxs-lookup"><span data-stu-id="e0ef8-181">Owner</span></span>  <br/> |<span data-ttu-id="e0ef8-182">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-182">True</span></span>  <br/> |<span data-ttu-id="e0ef8-183">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-183">True</span></span>  <br/> |<span data-ttu-id="e0ef8-184">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-184">True</span></span>  <br/> |<span data-ttu-id="e0ef8-185">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-185">True</span></span>  <br/> |<span data-ttu-id="e0ef8-186">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-186">True</span></span>  <br/> |<span data-ttu-id="e0ef8-187">Alle</span><span class="sxs-lookup"><span data-stu-id="e0ef8-187">All</span></span>  <br/> |<span data-ttu-id="e0ef8-188">Alle</span><span class="sxs-lookup"><span data-stu-id="e0ef8-188">All</span></span>  <br/> |<span data-ttu-id="e0ef8-189">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e0ef8-189">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e0ef8-190">Vom Typ PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="e0ef8-190">PublishingEditor</span></span>  <br/> |<span data-ttu-id="e0ef8-191">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-191">True</span></span>  <br/> |<span data-ttu-id="e0ef8-192">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-192">True</span></span>  <br/> |<span data-ttu-id="e0ef8-193">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-193">False</span></span>  <br/> |<span data-ttu-id="e0ef8-194">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-194">True</span></span>  <br/> |<span data-ttu-id="e0ef8-195">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-195">False</span></span>  <br/> |<span data-ttu-id="e0ef8-196">Alle</span><span class="sxs-lookup"><span data-stu-id="e0ef8-196">All</span></span>  <br/> |<span data-ttu-id="e0ef8-197">Alle</span><span class="sxs-lookup"><span data-stu-id="e0ef8-197">All</span></span>  <br/> |<span data-ttu-id="e0ef8-198">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e0ef8-198">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e0ef8-199">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="e0ef8-199">Editor</span></span>  <br/> |<span data-ttu-id="e0ef8-200">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-200">True</span></span>  <br/> |<span data-ttu-id="e0ef8-201">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-201">False</span></span>  <br/> |<span data-ttu-id="e0ef8-202">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-202">False</span></span>  <br/> |<span data-ttu-id="e0ef8-203">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-203">True</span></span>  <br/> |<span data-ttu-id="e0ef8-204">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-204">False</span></span>  <br/> |<span data-ttu-id="e0ef8-205">Alle</span><span class="sxs-lookup"><span data-stu-id="e0ef8-205">All</span></span>  <br/> |<span data-ttu-id="e0ef8-206">Alle</span><span class="sxs-lookup"><span data-stu-id="e0ef8-206">All</span></span>  <br/> |<span data-ttu-id="e0ef8-207">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e0ef8-207">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e0ef8-208">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="e0ef8-208">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="e0ef8-209">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-209">True</span></span>  <br/> |<span data-ttu-id="e0ef8-210">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-210">True</span></span>  <br/> |<span data-ttu-id="e0ef8-211">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-211">False</span></span>  <br/> |<span data-ttu-id="e0ef8-212">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-212">True</span></span>  <br/> |<span data-ttu-id="e0ef8-213">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-213">False</span></span>  <br/> |<span data-ttu-id="e0ef8-214">Gehören</span><span class="sxs-lookup"><span data-stu-id="e0ef8-214">Owned</span></span>  <br/> |<span data-ttu-id="e0ef8-215">Gehören</span><span class="sxs-lookup"><span data-stu-id="e0ef8-215">Owned</span></span>  <br/> |<span data-ttu-id="e0ef8-216">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e0ef8-216">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e0ef8-217">Autor</span><span class="sxs-lookup"><span data-stu-id="e0ef8-217">Author</span></span>  <br/> |<span data-ttu-id="e0ef8-218">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-218">True</span></span>  <br/> |<span data-ttu-id="e0ef8-219">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-219">False</span></span>  <br/> |<span data-ttu-id="e0ef8-220">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-220">False</span></span>  <br/> |<span data-ttu-id="e0ef8-221">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-221">True</span></span>  <br/> |<span data-ttu-id="e0ef8-222">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-222">False</span></span>  <br/> |<span data-ttu-id="e0ef8-223">Gehören</span><span class="sxs-lookup"><span data-stu-id="e0ef8-223">Owned</span></span>  <br/> |<span data-ttu-id="e0ef8-224">Gehören</span><span class="sxs-lookup"><span data-stu-id="e0ef8-224">Owned</span></span>  <br/> |<span data-ttu-id="e0ef8-225">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e0ef8-225">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e0ef8-226">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="e0ef8-226">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="e0ef8-227">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-227">True</span></span>  <br/> |<span data-ttu-id="e0ef8-228">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-228">False</span></span>  <br/> |<span data-ttu-id="e0ef8-229">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-229">False</span></span>  <br/> |<span data-ttu-id="e0ef8-230">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-230">True</span></span>  <br/> |<span data-ttu-id="e0ef8-231">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-231">False</span></span>  <br/> |<span data-ttu-id="e0ef8-232">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-232">None</span></span>  <br/> |<span data-ttu-id="e0ef8-233">Gehören</span><span class="sxs-lookup"><span data-stu-id="e0ef8-233">Owned</span></span>  <br/> |<span data-ttu-id="e0ef8-234">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e0ef8-234">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e0ef8-235">Prüfer</span><span class="sxs-lookup"><span data-stu-id="e0ef8-235">Reviewer</span></span>  <br/> |<span data-ttu-id="e0ef8-236">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-236">False</span></span>  <br/> |<span data-ttu-id="e0ef8-237">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-237">False</span></span>  <br/> |<span data-ttu-id="e0ef8-238">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-238">False</span></span>  <br/> |<span data-ttu-id="e0ef8-239">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-239">True</span></span>  <br/> |<span data-ttu-id="e0ef8-240">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-240">False</span></span>  <br/> |<span data-ttu-id="e0ef8-241">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-241">None</span></span>  <br/> |<span data-ttu-id="e0ef8-242">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-242">None</span></span>  <br/> |<span data-ttu-id="e0ef8-243">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e0ef8-243">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e0ef8-244">Mitwirkender</span><span class="sxs-lookup"><span data-stu-id="e0ef8-244">Contributor</span></span>  <br/> |<span data-ttu-id="e0ef8-245">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-245">True</span></span>  <br/> |<span data-ttu-id="e0ef8-246">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-246">False</span></span>  <br/> |<span data-ttu-id="e0ef8-247">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-247">False</span></span>  <br/> |<span data-ttu-id="e0ef8-248">True</span><span class="sxs-lookup"><span data-stu-id="e0ef8-248">True</span></span>  <br/> |<span data-ttu-id="e0ef8-249">False</span><span class="sxs-lookup"><span data-stu-id="e0ef8-249">False</span></span>  <br/> |<span data-ttu-id="e0ef8-250">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-250">None</span></span>  <br/> |<span data-ttu-id="e0ef8-251">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-251">None</span></span>  <br/> |<span data-ttu-id="e0ef8-252">Keine</span><span class="sxs-lookup"><span data-stu-id="e0ef8-252">None</span></span>  <br/> |
   
<span data-ttu-id="e0ef8-253">Wenn Sie in der Berechtigungen auf Ordnerebene Anforderung eine nicht benutzerdefinierte Berechtigungsstufe angeben, müssen Sie nicht die einzelnen Berechtigungen angeben.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-253">If you specify a non-custom permission level in the folder-level permissions request, you don't need to specify the individual permission settings.</span></span> <span data-ttu-id="e0ef8-254">Wenn Sie eine einzelne Berechtigung angeben, wenn Sie eine Berechtigungsstufe festgelegt, wird ein Fehler **ErrorInvalidPermissionSettings** in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-254">If you do specify an individual permission when you set a permission level, an **ErrorInvalidPermissionSettings** error will be returned in the response.</span></span> 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="e0ef8-255">Hinzufügen von Berechtigungen für Ordner mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="e0ef8-255">Adding folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="e0ef8-256"><a name="bk_enableewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e0ef8-256"></span></span>

<span data-ttu-id="e0ef8-257">Im folgenden Codebeispiel wird veranschaulicht, wie die EWS Managed API zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="e0ef8-257">The following code example shows how to use the EWS Managed API to:</span></span> 
  
- <span data-ttu-id="e0ef8-258">Erstellen Sie ein neues [FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) -Objekt für den neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-258">Create a new [FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) object for the new user.</span></span> 
    
- <span data-ttu-id="e0ef8-259">Rufen Sie die aktuellen Berechtigungen für einen Ordner mit der Methode [zu binden](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e0ef8-259">Get the current permissions for a folder by using the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method.</span></span> 
    
- <span data-ttu-id="e0ef8-260">Fügen Sie der neuen **FolderPermissions** der [Folder.Permissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-260">Add the new **FolderPermissions** to the [Folder.Permissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) property.</span></span> 
    
- <span data-ttu-id="e0ef8-261">Rufen Sie die [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) -Methode, um die neuen Berechtigungen auf dem Server zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-261">Call the [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the new permissions to the server.</span></span> 
    
<span data-ttu-id="e0ef8-262">In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und, die der Benutzer wurde an einen Exchange-Server authentifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-262">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void EnableFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.Permissions);
    // Specify the SMTP address of the new user and the folder permissions level.
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
    
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, WellKnownFolderName.SentItems, propSet);
 
    // Add the permissions for the new user to the Sent Items DACL.
    sentItemsFolder.Permissions.Add(fldperm);
    // This call results in a UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

<span data-ttu-id="e0ef8-263">Die folgende Codezeile gibt die Berechtigungsstufe.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-263">The following line of code specifies the permission level.</span></span>
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

<span data-ttu-id="e0ef8-264">Wenn Sie die benutzerdefinierte Berechtigungsstufe verwenden möchten, verwenden Sie stattdessen diesen Code.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-264">If you want to use the custom permission level, use this code instead.</span></span>
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

<span data-ttu-id="e0ef8-265">Sie können einige oder alle schreibbaren [Eigenschaften FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) festlegen, wenn Sie ein **FolderPermission** -Objekt mit der eine benutzerdefinierte Berechtigungsstufe erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-265">You can set any or all of the writable [FolderPermission properties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) when you create a **FolderPermission** object with a custom permission level.</span></span> <span data-ttu-id="e0ef8-266">Beachten Sie jedoch, dass die [FolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) von der Anwendung nicht explizit auf **Custom** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-266">Note, however, that the [FolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) is never explicitly set to **Custom** by the application.</span></span> <span data-ttu-id="e0ef8-267">Die **FolderPermissionLevel** wird nur, wenn ein **FolderPermission** -Objekt erstellen und Festlegen von einzelnen Berechtigungen zu benutzerdefinierten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-267">The **FolderPermissionLevel** is set to Custom only when you create a **FolderPermission** object and set individual permissions.</span></span> 
  
## <a name="adding-folder-permissions-by-using-ews"></a><span data-ttu-id="e0ef8-268">Hinzufügen von Berechtigungen für Ordner mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="e0ef8-268">Adding folder permissions by using EWS</span></span>
<span data-ttu-id="e0ef8-269"><a name="bk_enableews"> </a></span><span class="sxs-lookup"><span data-stu-id="e0ef8-269"></span></span>

<span data-ttu-id="e0ef8-270">Die folgenden EWS-Codebeispiele zeigen, wie zum Hinzufügen von Berechtigungen zu einem bestimmten Ordner durch Abrufen der aktuellen Berechtigungen und senden Sie dann eine Liste der neuen Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-270">The following EWS code examples show how to add permissions to a specific folder by retrieving the current permissions and then submitting a list of new permissions.</span></span>
  
<span data-ttu-id="e0ef8-271">Der erste Schritt besteht, senden Sie eine [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Anforderung, wobei der Wert [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) gibt den Ordner in dem zum Hinzufügen von Berechtigungen (in diesem Beispiel wird der Ordner "Gesendete Objekte") und der [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) Wert enthält Ordner: PermissionSet.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-271">The first step is to send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request, where the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to add permissions (the Sent Items folder in this example) and the [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="e0ef8-272">Diese Anforderung wird, werden die berechtigungseinstellungen für den angegebenen Ordner abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-272">This request will retrieve the permission settings for the folder specified.</span></span> 
  
<span data-ttu-id="e0ef8-273">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Bind** -Methode zum [Hinzufügen von Berechtigungen für Ordner](#bk_enableewsma)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-273">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [add folder permissions](#bk_enableewsma).</span></span>
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:GetFolder>
        <m:FolderShape>
          <t:BaseShape>IdOnly</t:BaseShape>
          <t:AdditionalProperties>
            <t:FieldURI FieldURI="folder:PermissionSet" />
          </t:AdditionalProperties>
        </m:FolderShape>
        <m:FolderIds>
          <t:DistinguishedFolderId Id="sentitems" />
        </m:FolderIds>
      </m:GetFolder>
    </soap:Body>
  </soap:Envelope>
```

<span data-ttu-id="e0ef8-274">Der Server antwortet auf die Anforderung **GetFolder** mit einer [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-274">The server responds to the **GetFolder** request with a [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="e0ef8-275">Die Werte [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) und [ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-275">The [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) and [ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) values have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="CgAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="e0ef8-276">Verwenden Sie die **UpdateFolder** -Operation im nächsten Schritt die aktualisierte [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)senden die die [Berechtigung](http://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) für den neuen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-276">Next, use the **UpdateFolder** operation to send the updated [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx), which includes the [Permission](http://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) for the new user.</span></span> <span data-ttu-id="e0ef8-277">Beachten Sie, dass das [SetFolderField](http://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) -Element für den jeweiligen Ordner in den Vorgang [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) einschließlich die berechtigungseinstellungen für den Ordner überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-277">Note that including the [SetFolderField](http://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) element for the respective folder in the [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation will overwrite all the permission settings on the folder.</span></span> <span data-ttu-id="e0ef8-278">Entsprechend wird die Option [DeleteFolderField](http://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) des Vorgangs **UpdateFolder** einschließlich auch die berechtigungseinstellungen für den Ordner gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-278">Likewise, including the [DeleteFolderField](http://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) option of the **UpdateFolder** operation will also delete all the permission settings on the folder.</span></span> 
  
<span data-ttu-id="e0ef8-279">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Update** -Methode zum [Hinzufügen von Berechtigungen für Ordner](#bk_enableewsma)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-279">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [add folder permissions](#bk_enableewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="CgAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
                      </t:UserId>
                      <t:PermissionLevel>Editor</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e0ef8-280">Die folgende Codezeile gibt die Berechtigungsstufe.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-280">The following line of code specifies the permission level.</span></span>
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

<span data-ttu-id="e0ef8-281">Wenn Sie die benutzerdefinierte Berechtigungsstufe verwenden möchten, verwenden Sie stattdessen diesen Code.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-281">If you want to use the custom permission level, use this code instead.</span></span>
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress> sadie@contoso.com </t:PrimarySmtpAddress>
    </t:UserId>
    <t:CanCreateItems>true</t:CanCreateItems>
    <t:CanCreateSubFolders>true</t:CanCreateSubFolders>
    <t:IsFolderOwner>false</t:IsFolderOwner>
    <t:IsFolderVisible>false</t:IsFolderVisible>
    <t:IsFolderContact>false</t:IsFolderContact>
    <t:EditItems>None</t:EditItems>
    <t:DeleteItems>None</t:DeleteItems>
    <t:ReadItems>None</t:ReadItems>
    <t:PermissionLevel>Custom</t:PermissionLevel>
</t:Permission>
```

<span data-ttu-id="e0ef8-282">Der Server antwortet auf die Anforderung **UpdateFolder** mit einer [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-282">The server responds to the **UpdateFolder** request with an [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was updated successfully.</span></span>
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="e0ef8-283">Entfernen von Berechtigungen für Ordner mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="e0ef8-283">Removing folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="e0ef8-284"><a name="bk_removeewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e0ef8-284"></span></span>

<span data-ttu-id="e0ef8-285">Im folgenden Codebeispiel wird veranschaulicht, wie die EWS Managed API verwenden, um alle Benutzerberechtigungen für einen bestimmten Ordner, mit Ausnahme der standardmäßigen und anonyme Berechtigungen durch entfernen:</span><span class="sxs-lookup"><span data-stu-id="e0ef8-285">The following code example shows how to use the EWS Managed API to remove all user permissions on a specific folder, except for the default and anonymous permissions, by:</span></span>
  
1. <span data-ttu-id="e0ef8-286">Abrufen der aktuellen Berechtigungen für einen Ordner mit der Methode **zu binden** .</span><span class="sxs-lookup"><span data-stu-id="e0ef8-286">Getting the current permissions for a folder by using the **Bind** method.</span></span> 
    
2. <span data-ttu-id="e0ef8-287">Die **Berechtigungen** -Auflistung durchlaufen, und Entfernen von Berechtigungen für einzelne Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-287">Iterating through the **Permissions** collection and removing permissions for individual users.</span></span> 
    
3. <span data-ttu-id="e0ef8-288">Aufrufen der **Update** -Methode, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-288">Calling the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="e0ef8-289">Dieses Beispiel entfernt alle Benutzerberechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-289">This example removes all user permissions on a folder.</span></span> <span data-ttu-id="e0ef8-290">Wenn Sie in diesem Beispiel wird zum Entfernen von Berechtigungen für einen bestimmten Benutzer nur ändern möchten, ändern Sie die folgende Codezeile zum Identifizieren entweder des Anzeigenamen oder die SMTP-Adresse des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-290">If you want to modify this example to remove permissions only for a specific user, change the following line of code to identify either the display name or SMTP address of the user.</span></span>
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

<span data-ttu-id="e0ef8-291">In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und, die der Benutzer wurde an einen Exchange-Server authentifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-291">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void RemoveFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.FirstClassProperties, FolderSchema.Permissions);
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, new FolderId(WellKnownFolderName.SentItems, "primary@contoso.com"), propSet);
    // Iterate through the collection of permissions and remove permissions for any 
    // user with a display name or SMTP address. This leaves the anonymous and 
    // default user permissions unchanged. 
    if (sentItemsFolder.Permissions.Count != 0)
    {
        for (int t = 0; t < sentItemsFolder.Permissions.Count; t++)
        {
            // Find any permissions associated with the specified user and remove them from the DACL
            if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
            {
                sentItemsFolder.Permissions.Remove(sentItemsFolder.Permissions[t]);
            }
        }
    }
    // This call results in an UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

## <a name="removing-folder-permissions-by-using-ews"></a><span data-ttu-id="e0ef8-292">Entfernen von Berechtigungen für Ordner mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="e0ef8-292">Removing folder permissions by using EWS</span></span>
<span data-ttu-id="e0ef8-293"><a name="bk_removeews"> </a></span><span class="sxs-lookup"><span data-stu-id="e0ef8-293"></span></span>

<span data-ttu-id="e0ef8-294">Die folgenden EWS-Codebeispiele zeigen, wie alle Benutzerberechtigungen für einen bestimmten Ordner, mit Ausnahme der Standard- und anonymen Berechtigungen entfernen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-294">The following EWS code examples show how to remove all user permissions on a specific folder, except for the default and anonymous permissions.</span></span>
  
<span data-ttu-id="e0ef8-295">Senden Sie zunächst eine [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Anforderung, in dem Ordner, in dem Entfernen von Berechtigungen (in diesem Beispiel wird der Ordner "Gesendete Objekte") gibt den [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) -Wert und der Wert [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) Ordner: PermissionSet enthält.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-295">First, send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request where the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to remove permissions (the Sent Items folder in this example) and the [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="e0ef8-296">Diese Anforderung wird die [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) für den angegebenen Ordner abrufen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-296">This request will retrieve the [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) for the folder specified.</span></span> 
  
<span data-ttu-id="e0ef8-297">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Bind** -Methode zum [Entfernen von Ordnerberechtigungen für](#bk_removeewsma)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-297">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:PermissionSet" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e0ef8-298">Der Server antwortet auf die Anforderung **GetFolder** mit einer [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-298">The server responds to the **GetFolder** request with a [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="e0ef8-299">Die Werte der Elemente **FolderId** und **ParentFolderId** wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-299">The values of the **FolderId** and **ParentFolderId** elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="EAAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
              <t:ParentFolderId Id="CQAAAA=="
                                ChangeKey="AQAAAA==" />
              <t:FolderClass>IPF.Note</t:FolderClass>
              <t:DisplayName>Drafts</t:DisplayName>
              <t:TotalCount>0</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:EffectiveRights>
                <t:CreateAssociated>true</t:CreateAssociated>
                <t:CreateContents>true</t:CreateContents>
                <t:CreateHierarchy>true</t:CreateHierarchy>
                <t:Delete>true</t:Delete>
                <t:Modify>true</t:Modify>
                <t:Read>true</t:Read>
                <t:ViewPrivateItems>true</t:ViewPrivateItems>
              </t:EffectiveRights>
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:SID>S-1-5-21-1337771579-694202782-848329751-1535223</t:SID>
                      <t:PrimarySmtpAddress>sadie@Contoso.com</t:PrimarySmtpAddress>
                      <t:DisplayName>Sadie Daniels</t:DisplayName>
                    </t:UserId>
                    <t:CanCreateItems>true</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>true</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>All</t:EditItems>
                    <t:DeleteItems>All</t:DeleteItems>
                    <t:ReadItems>FullDetails</t:ReadItems>
                    <t:PermissionLevel>Editor</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
              <t:UnreadCount>0</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="e0ef8-300">Im nächsten Schritt verwenden Sie die **UpdateFolder** -Operation, um die aktualisierte **PermissionSet**Versand nicht die **Berechtigung** für den entfernten Benutzer enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-300">Next, use the **UpdateFolder** operation to send the updated **PermissionSet**, which does not include the **Permission** for the removed user.</span></span> 
  
<span data-ttu-id="e0ef8-301">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Update** -Methode zum [Entfernen von Ordnerberechtigungen für](#bk_removeewsma)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-301">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="EAAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e0ef8-302">Der Server antwortet auf die Anforderung **UpdateFolder** mit einer **UpdateFolderResponse** -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Aktualisierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-302">The server responds to the **UpdateFolder** request with an **UpdateFolderResponse** message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the update was successful.</span></span>
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="e0ef8-303">Aktualisieren von Berechtigungen für Ordner mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="e0ef8-303">Updating folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="e0ef8-304"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e0ef8-304"></span></span>

<span data-ttu-id="e0ef8-305">Sie können auch die EWS Managed API Ordnerberechtigungen für einen bestimmten Ordner aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-305">You can also update folder permissions for a specific folder by using the EWS Managed API.</span></span> <span data-ttu-id="e0ef8-306">So aktualisieren Sie die Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="e0ef8-306">To update the permissions:</span></span> 
  
1. <span data-ttu-id="e0ef8-307">[Entfernen von Berechtigungen für den Ordner](#bk_removeewsma) für die veralteten Berechtigungen, aber rufen Sie nicht die **Update** -Methode (noch).</span><span class="sxs-lookup"><span data-stu-id="e0ef8-307">[Remove the folder permissions](#bk_removeewsma) for the outdated permissions, but do not call the **Update** method (yet).</span></span> 
    
2. <span data-ttu-id="e0ef8-308">[Berechtigungen für die neue oder geänderte Benutzer hinzufügen](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="e0ef8-308">[Add folder permissions for the new or changed users](#bk_enableewsma).</span></span>
    
3. <span data-ttu-id="e0ef8-309">Rufen Sie die **Update** -Methode, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-309">Call the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="e0ef8-310">Wenn Sie versuchen, zwei Sätze von Berechtigungen für den gleichen Benutzer hinzufügen, erhalten Sie eine Fehlermeldung **ServiceResponseException** mit der folgenden Beschreibung: "der angegebenen Berechtigungssatz enthält doppelte Benutzer-IDs".</span><span class="sxs-lookup"><span data-stu-id="e0ef8-310">If you try to add two sets of permissions for the same user, you will receive a **ServiceResponseException** error with the following description: "The specified permission set contains duplicate UserIds".</span></span> <span data-ttu-id="e0ef8-311">In diesem Fall die aktuellen Berechtigungen aus der **Permission** -Auflistung entfernen und dann die neuen Berechtigungen auf der **Permission** -Auflistung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-311">In that case, remove the current permissions from the **Permission** collection, then add the new permissions to the **Permission** collection.</span></span> 
  
## <a name="updating-folder-permissions-by-using-ews"></a><span data-ttu-id="e0ef8-312">Aktualisieren von Berechtigungen für Ordner mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="e0ef8-312">Updating folder permissions by using EWS</span></span>
<span data-ttu-id="e0ef8-313"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="e0ef8-313"></span></span>

<span data-ttu-id="e0ef8-314">Sie können auch Berechtigungen für bestimmte Ordner aktualisieren, mithilfe der EWS durch die Kombination des Prozesses zum Entfernen sowie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-314">You can also update folder permissions for specific folders by using EWS by combining the removal and addition process.</span></span> <span data-ttu-id="e0ef8-315">So aktualisieren Sie die Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="e0ef8-315">To update the permissions:</span></span> 
  
1. <span data-ttu-id="e0ef8-316">Abrufen von aktuellen Berechtigungen für den Ordner mithilfe des **GetFolder** -Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-316">Retrieve the folder's current permissions by using the **GetFolder** operation.</span></span> 
    
2. <span data-ttu-id="e0ef8-317">Senden Sie eine aktualisierte Liste von Berechtigungen mithilfe des **UpdateFolder** -Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-317">Send an updated list of permissions by using the **UpdateFolder** operation.</span></span> 
    
<span data-ttu-id="e0ef8-318">Dies sind die gleichen zwei Vorgänge, die Sie mithilfe von EWS zum [Aktivieren](#bk_enableews) oder [Entfernen Sie den Zugriff](#bk_removeews) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-318">These are the same two operations you use to [enable](#bk_enableews) or [remove access](#bk_removeews) by using EWS.</span></span> <span data-ttu-id="e0ef8-319">Der einzige Unterschied ist, wenn Sie die **GetFolder** -Antwort erhalten, eine **Berechtigung** für Benutzer enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-319">The only difference is that when you receive the **GetFolder** response, it will contain a **Permission** set for user.</span></span> <span data-ttu-id="e0ef8-320">Ersetzen Sie einfach, vorhandene **Permission** -Element mit dem neuen **Berechtigung** Element, und senden Sie den Vorgang **UpdateFolder** mit den neuen **Berechtigung** oder Werte.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-320">Simply replace that existing **Permission** element with the new **Permission** element, and then send the **UpdateFolder** operation with the new **Permission** value or values.</span></span> 
  
<span data-ttu-id="e0ef8-321">Wenn Sie versuchen, zwei Sätze von Berechtigungen für den gleichen Benutzer hinzufügen, erhalten Sie **ResponseCode** Wert **ErrorDuplicateUserIdsSpecified**.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-321">If you try to add two sets of permissions for the same user, you will receive a **ResponseCode** value of **ErrorDuplicateUserIdsSpecified**.</span></span> <span data-ttu-id="e0ef8-322">In diesem Fall entfernen Sie den Wert für veralteten Berechtigung für den Benutzer aus der Anforderung, und wiederholen Sie die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-322">In that case, remove the outdated Permission value for the user from the request and then retry the request.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e0ef8-323">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e0ef8-323">Next steps</span></span>

<span data-ttu-id="e0ef8-324">Nachdem Sie eine Benutzer die Berechtigung in einen bestimmten Ordner erteilen, kann der Benutzer eine Stellvertretung den Ordner zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e0ef8-324">After you give a user permission to a specific folder, the user can access the folder as a delegate.</span></span> <span data-ttu-id="e0ef8-325">Weitere Informationen finden Sie unter folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e0ef8-325">For more information, see:</span></span>
  
- [<span data-ttu-id="e0ef8-326">Access-e-Mail eine Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0ef8-326">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="e0ef8-327">Zugriff auf einen Kalender als Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0ef8-327">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="e0ef8-328">Access-Kontakte als Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0ef8-328">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="e0ef8-329">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0ef8-329">See also</span></span>

- [<span data-ttu-id="e0ef8-330">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0ef8-330">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="e0ef8-331">Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0ef8-331">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="e0ef8-332">Ordner und Elemente in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0ef8-332">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    

