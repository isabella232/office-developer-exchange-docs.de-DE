---
title: Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: Hier erfahren Sie, wie Sie Berechtigungsstufen für einen Ordner mithilfe der verwaltete EWS-API oder EWS in Exchange festlegen.
ms.openlocfilehash: e25f1a49a430e8c95829d404fa53451b76cab167
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455870"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a><span data-ttu-id="1dbff-103">Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1dbff-103">Set folder permissions for another user by using EWS in Exchange</span></span>

<span data-ttu-id="1dbff-104">Hier erfahren Sie, wie Sie Berechtigungsstufen für einen Ordner mithilfe der verwaltete EWS-API oder EWS in Exchange festlegen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-104">Learn how to set permission levels on a folder by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="1dbff-105">Berechtigungen auf Ordnerebene ermöglichen Benutzern den Zugriff auf einen oder mehrere Ordner im Postfach eines anderen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1dbff-105">Folder-level permissions enable users to access one or more folders in another user's mailbox.</span></span> <span data-ttu-id="1dbff-106">Ordnerberechtigungen ähneln dem Stellvertretungszugriff, Sie unterscheiden sich jedoch folgendermaßen:</span><span class="sxs-lookup"><span data-stu-id="1dbff-106">Folder permissions are similar to delegate access, but they differ in the following ways:</span></span> 
  
- <span data-ttu-id="1dbff-107">Ordnerberechtigungen ermöglichen einem Benutzer nicht, "im Auftrag von" oder "Senden als" einen anderen Benutzer zu senden.</span><span class="sxs-lookup"><span data-stu-id="1dbff-107">Folder permissions do not enable a user to "send on behalf of" or "send as" another user.</span></span> <span data-ttu-id="1dbff-108">Sie ermöglichen nur den Zugriff auf Ordner.</span><span class="sxs-lookup"><span data-stu-id="1dbff-108">They only enable access to folders.</span></span> <span data-ttu-id="1dbff-109">Benutzer können Elemente in diesen Ordnern erstellen, aber nicht senden.</span><span class="sxs-lookup"><span data-stu-id="1dbff-109">Users can create items in those folders, but they can't send them.</span></span>
    
- <span data-ttu-id="1dbff-110">Sie können Ordnerberechtigungen für einen beliebigen Ordner im Postfach festlegen, aber Sie können nur einen Stellvertreter zu den Ordnern Kalender, Kontakte, Posteingang, Journal, Notizen und Aufgaben hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-110">You can set folder permissions on any folder in the mailbox, but you can only add a delegate to the Calendar, Contacts, Inbox, Journal, Notes, and Tasks folders.</span></span>
    
- <span data-ttu-id="1dbff-111">Sie können eine Reihe von [Berechtigungen für einen bestimmten Ordner](#bk_folderperms)festlegen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-111">You can set a number of [permissions on a specific folder](#bk_folderperms).</span></span> <span data-ttu-id="1dbff-112">Wenn Sie eine Stellvertretung hinzufügen, können Sie eine von nur [fünf Berechtigungsstufen](delegate-access-and-ews-in-exchange.md#bk_delegateperms)zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-112">When you add a delegate, you can assign one of only [five permission levels](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span>
    
- <span data-ttu-id="1dbff-113">Sie können Ordnerberechtigungen für anonyme und Standardbenutzer festlegen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-113">You can set folder permissions for anonymous and default users.</span></span> <span data-ttu-id="1dbff-114">Sie können nur einem e-Mail-aktivierten Konto Stellvertretungszugriff gewähren.</span><span class="sxs-lookup"><span data-stu-id="1dbff-114">You can only grant delegate access to a mail-enabled account.</span></span>
    
<span data-ttu-id="1dbff-115">Wenn Sie mit Zugriffssteuerungseinträgen (ACEs) und Discretionary Access Control Lists (DACLs) vertraut sind, wissen Sie, dass ein Benutzer nur über einen Berechtigungssatz für jeden Ordner verfügen kann.</span><span class="sxs-lookup"><span data-stu-id="1dbff-115">If you're familiar with Access Control Entries (ACEs) and Discretionary Access Control Lists (DACLs), you know that a user can only have one set of permissions for each folder.</span></span> <span data-ttu-id="1dbff-116">Wenn Sie versuchen, eine Gruppe von Berechtigungen für einen Benutzer hinzuzufügen und bereits über eine Reihe von Berechtigungen verfügen, erhalten Sie eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="1dbff-116">If you try to add a set of permissions for a user and they already have a set of permissions, you'll get an error.</span></span> <span data-ttu-id="1dbff-117">Wenn Sie Berechtigungen für einen Ordner hinzufügen, entfernen oder aktualisieren, erhalten Sie die aktuelle DACL, fügen ACEs hinzu oder entfernen Sie und senden dann die aktualisierte DACL.</span><span class="sxs-lookup"><span data-stu-id="1dbff-117">When you add, remove, or update permissions on a folder, you get the current DACL, add or remove any ACEs, and then send the updated DACL.</span></span> <span data-ttu-id="1dbff-118">Sie können nicht mehrere ACEs für denselben Benutzer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-118">You cannot add multiple ACEs for the same user.</span></span> <span data-ttu-id="1dbff-119">Wenn Sie Berechtigungen mithilfe des verwaltete EWS-API aktualisieren, müssen Sie den aktuellen ACE des Benutzers entfernen und dann den neuen ACE zur Auflistung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-119">When you update permissions by using the EWS Managed API, you need to remove the user's current ACE and then add their new ACE to the collection.</span></span> <span data-ttu-id="1dbff-120">Wenn Sie EWS verwenden, ersetzen Sie einfach den vorherigen ACEs-Datensatz durch die neuen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-120">If you're using EWS, you just replace the previous set of ACEs with the new ones.</span></span>
  
<span data-ttu-id="1dbff-121">Wenn Sie mehrere Berechtigungsänderungen an einem einzelnen Ordner vornehmen, können Sie den Batch hinzufügen, entfernen oder aktualisieren – beachten Sie, dass Sie keine Benutzer Updates in mehreren Ordnern stapeln können.</span><span class="sxs-lookup"><span data-stu-id="1dbff-121">If you're making multiple permission changes to a single folder, you can batch additions, removals, or updates —just note that you cannot batch user updates on multiple folders.</span></span> <span data-ttu-id="1dbff-122">Ein Aufruf ist erforderlich, um die Berechtigungen für einen einzelnen Ordner abzurufen, und ein zweiter Aufruf ist erforderlich, um die Berechtigungen für diesen Ordner zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1dbff-122">One call is required to get the permissions on a single folder, and a second call is required to update the permissions on that folder.</span></span> <span data-ttu-id="1dbff-123">Wenn Sie Benutzerberechtigungen hinzufügen, entfernen oder aktualisieren, verwenden Sie für jede Aufgabe dieselben zwei Methodenaufrufe oder-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="1dbff-123">When you add, remove, or update user permissions, you use the same two method calls or operations for each task.</span></span>
  
<span data-ttu-id="1dbff-124">**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge zum Festlegen von Ordnerberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="1dbff-124">**Table 1. EWS Managed API methods and EWS operations for setting folder permissions**</span></span>

|<span data-ttu-id="1dbff-125">Aktion</span><span class="sxs-lookup"><span data-stu-id="1dbff-125">If you want to…</span></span>|<span data-ttu-id="1dbff-126">Verwenden Sie diese verwaltete EWS-API-Methode...</span><span class="sxs-lookup"><span data-stu-id="1dbff-126">Use this EWS Managed API method…</span></span>|<span data-ttu-id="1dbff-127">Verwenden Sie diesen EWS-Vorgang...</span><span class="sxs-lookup"><span data-stu-id="1dbff-127">Use this EWS operation…</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1dbff-128">Aktivieren, entfernen oder Aktualisieren von Ordnerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="1dbff-128">Enable, remove, or update folder permissions</span></span>  <br/> |<span data-ttu-id="1dbff-129">[Folder. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) gefolgt von [Folder. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dbff-129">[Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) followed by [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="1dbff-130">[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) gefolgt von [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dbff-130">[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) followed by [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="1dbff-131">Erstellen eines Ordners und Definieren von Ordnerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="1dbff-131">Create a folder and define folder permissions</span></span>  <br/> |[<span data-ttu-id="1dbff-132">Folder.Save</span><span class="sxs-lookup"><span data-stu-id="1dbff-132">Folder.Save</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="1dbff-133">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="1dbff-133">CreateFolder</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a><span data-ttu-id="1dbff-134">Ordnerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="1dbff-134">Folder permissions</span></span>
<span data-ttu-id="1dbff-135"><a name="bk_folderperms"> </a></span><span class="sxs-lookup"><span data-stu-id="1dbff-135"><a name="bk_folderperms"> </a></span></span>

<span data-ttu-id="1dbff-136">Sie haben etliche Optionen, wenn es darum geht, Ordnerberechtigungen für einen bestimmten Ordner festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-136">You have quite a few options when it comes to setting folder permissions on a specific folder.</span></span> <span data-ttu-id="1dbff-137">Sie können eine Berechtigungsstufe für einen Ordner für jeden Benutzer festlegen, wodurch eine Reihe vordefinierter einzelner Berechtigungen zur DACL hinzugefügt wird, oder Sie können einzelne Berechtigungen für einen Ordner festlegen, jedoch keine Kombination aus-und abgleichen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-137">You can set a permission level on a folder for each user, which adds a set of predefined individual permissions to the DACL, or you can set individual permissions on a folder — but you can't mix and match.</span></span>
  
<span data-ttu-id="1dbff-138">Die folgenden einzelnen Berechtigungen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="1dbff-138">The following individual permissions are available:</span></span>
  
- <span data-ttu-id="1dbff-139">Erstellen kann</span><span class="sxs-lookup"><span data-stu-id="1dbff-139">Can create</span></span>
- <span data-ttu-id="1dbff-140">Unterordner können erstellt werden</span><span class="sxs-lookup"><span data-stu-id="1dbff-140">Can create subfolders</span></span>    
- <span data-ttu-id="1dbff-141">Ist Ordnerbesitzer</span><span class="sxs-lookup"><span data-stu-id="1dbff-141">Is folder owner</span></span>    
- <span data-ttu-id="1dbff-142">Ordner ist sichtbar</span><span class="sxs-lookup"><span data-stu-id="1dbff-142">Is folder visible</span></span>    
- <span data-ttu-id="1dbff-143">Ist Ordner Kontakt</span><span class="sxs-lookup"><span data-stu-id="1dbff-143">Is folder contact</span></span>    
- <span data-ttu-id="1dbff-144">Bearbeiten von Elementen</span><span class="sxs-lookup"><span data-stu-id="1dbff-144">Edit items</span></span>    
- <span data-ttu-id="1dbff-145">Löschen von Elementen</span><span class="sxs-lookup"><span data-stu-id="1dbff-145">Delete items</span></span>    
- <span data-ttu-id="1dbff-146">Elemente lesen</span><span class="sxs-lookup"><span data-stu-id="1dbff-146">Read items</span></span>
    
<span data-ttu-id="1dbff-147">Darüber hinaus stehen die folgenden Berechtigungsstufen zur Verfügung, die eine Teilmenge der einzelnen Berechtigungen und Werte definieren, wie in Tabelle 2 dargestellt:</span><span class="sxs-lookup"><span data-stu-id="1dbff-147">In addition, the following permission levels are available, which define a subset of individual permissions and values, as shown in Table 2:</span></span>
  
- <span data-ttu-id="1dbff-148">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-148">None</span></span>    
- <span data-ttu-id="1dbff-149">Besitzer</span><span class="sxs-lookup"><span data-stu-id="1dbff-149">Owner</span></span>    
- <span data-ttu-id="1dbff-150">Publishing Editor</span><span class="sxs-lookup"><span data-stu-id="1dbff-150">PublishingEditor</span></span>    
- <span data-ttu-id="1dbff-151">Editor</span><span class="sxs-lookup"><span data-stu-id="1dbff-151">Editor</span></span>    
- <span data-ttu-id="1dbff-152">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="1dbff-152">PublishingAuthor</span></span>    
- <span data-ttu-id="1dbff-153">Ursprung</span><span class="sxs-lookup"><span data-stu-id="1dbff-153">Author</span></span>    
- <span data-ttu-id="1dbff-154">Noneditingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="1dbff-154">NoneditingAuthor</span></span>    
- <span data-ttu-id="1dbff-155">Reviewer</span><span class="sxs-lookup"><span data-stu-id="1dbff-155">Reviewer</span></span>    
- <span data-ttu-id="1dbff-156">Contributor</span><span class="sxs-lookup"><span data-stu-id="1dbff-156">Contributor</span></span>   
- <span data-ttu-id="1dbff-157">Custom-dieser Wert kann nicht von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1dbff-157">Custom - This value cannot be set by the application.</span></span> <span data-ttu-id="1dbff-158">Der Server legt diesen Wert fest, wenn die Anwendung eine benutzerdefinierte Auflistung einzelner Berechtigungen enthält.</span><span class="sxs-lookup"><span data-stu-id="1dbff-158">The server sets this value if the application includes a custom collection of individual permissions.</span></span>    
- <span data-ttu-id="1dbff-159">FreeBusyTimeOnly-Dies kann nur für Kalenderordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1dbff-159">FreeBusyTimeOnly - This can only be set on Calendar folders.</span></span>   
- <span data-ttu-id="1dbff-160">FreeBusyTimeAndSubjectAndLocation-Dies kann nur für Kalenderordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1dbff-160">FreeBusyTimeAndSubjectAndLocation - This can only be set on Calendar folders.</span></span>
    
<span data-ttu-id="1dbff-161">In der folgenden Tabelle wird gezeigt, welche einzelnen Berechtigungen standardmäßig basierend auf der Berechtigungsstufe angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dbff-161">The following table shows which individual permissions are applied by default based on permission level.</span></span>
  
<span data-ttu-id="1dbff-162">**Tabelle 2. Einzelne Berechtigungen nach Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="1dbff-162">**Table 2. Individual permissions by permission level**</span></span>

|<span data-ttu-id="1dbff-163">Berechtigungsstufe</span><span class="sxs-lookup"><span data-stu-id="1dbff-163">Permission level</span></span>|<span data-ttu-id="1dbff-164">Kann Elemente erstellen</span><span class="sxs-lookup"><span data-stu-id="1dbff-164">Can create items</span></span>|<span data-ttu-id="1dbff-165">Unterordner können erstellt werden</span><span class="sxs-lookup"><span data-stu-id="1dbff-165">Can create sub folders</span></span>|<span data-ttu-id="1dbff-166">Ist Ordnerbesitzer</span><span class="sxs-lookup"><span data-stu-id="1dbff-166">Is folder owner</span></span>|<span data-ttu-id="1dbff-167">Ordner ist sichtbar</span><span class="sxs-lookup"><span data-stu-id="1dbff-167">Is folder visible</span></span>|<span data-ttu-id="1dbff-168">Ist Ordner Kontakt</span><span class="sxs-lookup"><span data-stu-id="1dbff-168">Is folder contact</span></span>|<span data-ttu-id="1dbff-169">Bearbeiten von Elementen</span><span class="sxs-lookup"><span data-stu-id="1dbff-169">Edit items</span></span>|<span data-ttu-id="1dbff-170">Löschen von Elementen</span><span class="sxs-lookup"><span data-stu-id="1dbff-170">Delete items</span></span>|<span data-ttu-id="1dbff-171">Elemente können gelesen werden</span><span class="sxs-lookup"><span data-stu-id="1dbff-171">Can read items</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1dbff-172">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-172">None</span></span>  <br/> |<span data-ttu-id="1dbff-173">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-173">False</span></span>  <br/> |<span data-ttu-id="1dbff-174">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-174">False</span></span>  <br/> |<span data-ttu-id="1dbff-175">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-175">False</span></span>  <br/> |<span data-ttu-id="1dbff-176">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-176">False</span></span>  <br/> |<span data-ttu-id="1dbff-177">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-177">False</span></span>  <br/> |<span data-ttu-id="1dbff-178">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-178">None</span></span>  <br/> |<span data-ttu-id="1dbff-179">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-179">None</span></span>  <br/> |<span data-ttu-id="1dbff-180">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-180">None</span></span>  <br/> |
|<span data-ttu-id="1dbff-181">Besitzer</span><span class="sxs-lookup"><span data-stu-id="1dbff-181">Owner</span></span>  <br/> |<span data-ttu-id="1dbff-182">True</span><span class="sxs-lookup"><span data-stu-id="1dbff-182">True</span></span>  <br/> |<span data-ttu-id="1dbff-183">True</span><span class="sxs-lookup"><span data-stu-id="1dbff-183">True</span></span>  <br/> |<span data-ttu-id="1dbff-184">True</span><span class="sxs-lookup"><span data-stu-id="1dbff-184">True</span></span>  <br/> |<span data-ttu-id="1dbff-185">True</span><span class="sxs-lookup"><span data-stu-id="1dbff-185">True</span></span>  <br/> |<span data-ttu-id="1dbff-186">True</span><span class="sxs-lookup"><span data-stu-id="1dbff-186">True</span></span>  <br/> |<span data-ttu-id="1dbff-187">Alle</span><span class="sxs-lookup"><span data-stu-id="1dbff-187">All</span></span>  <br/> |<span data-ttu-id="1dbff-188">Alle</span><span class="sxs-lookup"><span data-stu-id="1dbff-188">All</span></span>  <br/> |<span data-ttu-id="1dbff-189">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1dbff-189">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1dbff-190">Publishing Editor</span><span class="sxs-lookup"><span data-stu-id="1dbff-190">PublishingEditor</span></span>  <br/> |<span data-ttu-id="1dbff-191">True</span><span class="sxs-lookup"><span data-stu-id="1dbff-191">True</span></span>  <br/> |<span data-ttu-id="1dbff-192">True</span><span class="sxs-lookup"><span data-stu-id="1dbff-192">True</span></span>  <br/> |<span data-ttu-id="1dbff-193">False</span><span class="sxs-lookup"><span data-stu-id="1dbff-193">False</span></span>  <br/> |<span data-ttu-id="1dbff-194">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-194">True</span></span>  <br/> |<span data-ttu-id="1dbff-195">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-195">False</span></span>  <br/> |<span data-ttu-id="1dbff-196">Alle</span><span class="sxs-lookup"><span data-stu-id="1dbff-196">All</span></span>  <br/> |<span data-ttu-id="1dbff-197">Alle</span><span class="sxs-lookup"><span data-stu-id="1dbff-197">All</span></span>  <br/> |<span data-ttu-id="1dbff-198">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1dbff-198">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1dbff-199">Editor</span><span class="sxs-lookup"><span data-stu-id="1dbff-199">Editor</span></span>  <br/> |<span data-ttu-id="1dbff-200">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-200">True</span></span>  <br/> |<span data-ttu-id="1dbff-201">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-201">False</span></span>  <br/> |<span data-ttu-id="1dbff-202">False</span><span class="sxs-lookup"><span data-stu-id="1dbff-202">False</span></span>  <br/> |<span data-ttu-id="1dbff-203">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-203">True</span></span>  <br/> |<span data-ttu-id="1dbff-204">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-204">False</span></span>  <br/> |<span data-ttu-id="1dbff-205">Alle</span><span class="sxs-lookup"><span data-stu-id="1dbff-205">All</span></span>  <br/> |<span data-ttu-id="1dbff-206">Alle</span><span class="sxs-lookup"><span data-stu-id="1dbff-206">All</span></span>  <br/> |<span data-ttu-id="1dbff-207">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1dbff-207">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1dbff-208">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="1dbff-208">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="1dbff-209">True</span><span class="sxs-lookup"><span data-stu-id="1dbff-209">True</span></span>  <br/> |<span data-ttu-id="1dbff-210">True</span><span class="sxs-lookup"><span data-stu-id="1dbff-210">True</span></span>  <br/> |<span data-ttu-id="1dbff-211">False</span><span class="sxs-lookup"><span data-stu-id="1dbff-211">False</span></span>  <br/> |<span data-ttu-id="1dbff-212">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-212">True</span></span>  <br/> |<span data-ttu-id="1dbff-213">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-213">False</span></span>  <br/> |<span data-ttu-id="1dbff-214">Im Besitz</span><span class="sxs-lookup"><span data-stu-id="1dbff-214">Owned</span></span>  <br/> |<span data-ttu-id="1dbff-215">Im Besitz</span><span class="sxs-lookup"><span data-stu-id="1dbff-215">Owned</span></span>  <br/> |<span data-ttu-id="1dbff-216">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1dbff-216">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1dbff-217">Ursprung</span><span class="sxs-lookup"><span data-stu-id="1dbff-217">Author</span></span>  <br/> |<span data-ttu-id="1dbff-218">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-218">True</span></span>  <br/> |<span data-ttu-id="1dbff-219">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-219">False</span></span>  <br/> |<span data-ttu-id="1dbff-220">False</span><span class="sxs-lookup"><span data-stu-id="1dbff-220">False</span></span>  <br/> |<span data-ttu-id="1dbff-221">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-221">True</span></span>  <br/> |<span data-ttu-id="1dbff-222">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-222">False</span></span>  <br/> |<span data-ttu-id="1dbff-223">Im Besitz</span><span class="sxs-lookup"><span data-stu-id="1dbff-223">Owned</span></span>  <br/> |<span data-ttu-id="1dbff-224">Im Besitz</span><span class="sxs-lookup"><span data-stu-id="1dbff-224">Owned</span></span>  <br/> |<span data-ttu-id="1dbff-225">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1dbff-225">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1dbff-226">Noneditingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="1dbff-226">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="1dbff-227">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-227">True</span></span>  <br/> |<span data-ttu-id="1dbff-228">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-228">False</span></span>  <br/> |<span data-ttu-id="1dbff-229">False</span><span class="sxs-lookup"><span data-stu-id="1dbff-229">False</span></span>  <br/> |<span data-ttu-id="1dbff-230">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-230">True</span></span>  <br/> |<span data-ttu-id="1dbff-231">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-231">False</span></span>  <br/> |<span data-ttu-id="1dbff-232">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-232">None</span></span>  <br/> |<span data-ttu-id="1dbff-233">Im Besitz</span><span class="sxs-lookup"><span data-stu-id="1dbff-233">Owned</span></span>  <br/> |<span data-ttu-id="1dbff-234">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1dbff-234">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1dbff-235">Reviewer</span><span class="sxs-lookup"><span data-stu-id="1dbff-235">Reviewer</span></span>  <br/> |<span data-ttu-id="1dbff-236">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-236">False</span></span>  <br/> |<span data-ttu-id="1dbff-237">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-237">False</span></span>  <br/> |<span data-ttu-id="1dbff-238">False</span><span class="sxs-lookup"><span data-stu-id="1dbff-238">False</span></span>  <br/> |<span data-ttu-id="1dbff-239">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-239">True</span></span>  <br/> |<span data-ttu-id="1dbff-240">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-240">False</span></span>  <br/> |<span data-ttu-id="1dbff-241">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-241">None</span></span>  <br/> |<span data-ttu-id="1dbff-242">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-242">None</span></span>  <br/> |<span data-ttu-id="1dbff-243">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1dbff-243">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1dbff-244">Contributor</span><span class="sxs-lookup"><span data-stu-id="1dbff-244">Contributor</span></span>  <br/> |<span data-ttu-id="1dbff-245">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-245">True</span></span>  <br/> |<span data-ttu-id="1dbff-246">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-246">False</span></span>  <br/> |<span data-ttu-id="1dbff-247">False</span><span class="sxs-lookup"><span data-stu-id="1dbff-247">False</span></span>  <br/> |<span data-ttu-id="1dbff-248">Wahr</span><span class="sxs-lookup"><span data-stu-id="1dbff-248">True</span></span>  <br/> |<span data-ttu-id="1dbff-249">Falsch</span><span class="sxs-lookup"><span data-stu-id="1dbff-249">False</span></span>  <br/> |<span data-ttu-id="1dbff-250">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-250">None</span></span>  <br/> |<span data-ttu-id="1dbff-251">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-251">None</span></span>  <br/> |<span data-ttu-id="1dbff-252">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbff-252">None</span></span>  <br/> |
   
<span data-ttu-id="1dbff-253">Wenn Sie eine nicht benutzerdefinierte Berechtigungsstufe in der Berechtigungsanforderung auf Ordnerebene angeben, müssen Sie die einzelnen Berechtigungseinstellungen nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="1dbff-253">If you specify a non-custom permission level in the folder-level permissions request, you don't need to specify the individual permission settings.</span></span> <span data-ttu-id="1dbff-254">Wenn Sie beim Festlegen einer Berechtigungsstufe eine einzelne Berechtigung angeben, wird in der Antwort ein **ErrorInvalidPermissionSettings** -Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1dbff-254">If you do specify an individual permission when you set a permission level, an **ErrorInvalidPermissionSettings** error will be returned in the response.</span></span> 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="1dbff-255">Hinzufügen von Ordnerberechtigungen mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="1dbff-255">Adding folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="1dbff-256"><a name="bk_enableewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1dbff-256"><a name="bk_enableewsma"> </a></span></span>

<span data-ttu-id="1dbff-257">Im folgenden Codebeispiel wird die Verwendung der verwaltete EWS-API für Folgendes veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="1dbff-257">The following code example shows how to use the EWS Managed API to:</span></span> 
  
- <span data-ttu-id="1dbff-258">Erstellen Sie ein neues [FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) -Objekt für den neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="1dbff-258">Create a new [FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) object for the new user.</span></span> 
    
- <span data-ttu-id="1dbff-259">Abrufen der aktuellen Berechtigungen für einen Ordner mithilfe der [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1dbff-259">Get the current permissions for a folder by using the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method.</span></span> 
    
- <span data-ttu-id="1dbff-260">Fügen Sie die neue **FolderPermissions** der Eigenschaft [Folder. Permissions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) hinzu.</span><span class="sxs-lookup"><span data-stu-id="1dbff-260">Add the new **FolderPermissions** to the [Folder.Permissions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) property.</span></span> 
    
- <span data-ttu-id="1dbff-261">Rufen Sie die [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) -Methode auf, um die neuen Berechtigungen auf dem Server zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1dbff-261">Call the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the new permissions to the server.</span></span> 
    
<span data-ttu-id="1dbff-262">In diesem Beispiel wird davon ausgegangen, dass **Service** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Postfachbesitzer ist und dass der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="1dbff-262">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="1dbff-263">In der folgenden Codezeile wird die Berechtigungsstufe angegeben.</span><span class="sxs-lookup"><span data-stu-id="1dbff-263">The following line of code specifies the permission level.</span></span>
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

<span data-ttu-id="1dbff-264">Wenn Sie die benutzerdefinierte Berechtigungsstufe verwenden möchten, verwenden Sie stattdessen diesen Code.</span><span class="sxs-lookup"><span data-stu-id="1dbff-264">If you want to use the custom permission level, use this code instead.</span></span>
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

<span data-ttu-id="1dbff-265">Sie können eine beliebige oder alle schreibbaren [FolderPermission-Eigenschaften](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) festlegen, wenn Sie ein **FolderPermission** -Objekt mit einer benutzerdefinierten Berechtigungsstufe erstellen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-265">You can set any or all of the writable [FolderPermission properties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) when you create a **FolderPermission** object with a custom permission level.</span></span> <span data-ttu-id="1dbff-266">Beachten Sie jedoch, dass die [FolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) niemals explizit von der Anwendung auf **Custom** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1dbff-266">Note, however, that the [FolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) is never explicitly set to **Custom** by the application.</span></span> <span data-ttu-id="1dbff-267">**FolderPermissionLevel** wird nur dann auf Custom festgelegt, wenn Sie ein **FolderPermission** -Objekt erstellen und einzelne Berechtigungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-267">The **FolderPermissionLevel** is set to Custom only when you create a **FolderPermission** object and set individual permissions.</span></span> 
  
## <a name="adding-folder-permissions-by-using-ews"></a><span data-ttu-id="1dbff-268">Hinzufügen von Ordnerberechtigungen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="1dbff-268">Adding folder permissions by using EWS</span></span>
<span data-ttu-id="1dbff-269"><a name="bk_enableews"> </a></span><span class="sxs-lookup"><span data-stu-id="1dbff-269"><a name="bk_enableews"> </a></span></span>

<span data-ttu-id="1dbff-270">Die folgenden EWS-Codebeispiele zeigen, wie Sie Berechtigungen zu einem bestimmten Ordner hinzufügen, indem Sie die aktuellen Berechtigungen abrufen und dann eine Liste mit neuen Berechtigungen übermitteln.</span><span class="sxs-lookup"><span data-stu-id="1dbff-270">The following EWS code examples show how to add permissions to a specific folder by retrieving the current permissions and then submitting a list of new permissions.</span></span>
  
<span data-ttu-id="1dbff-271">Der erste Schritt besteht darin, eine [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Anforderung zu senden, wobei der [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) -Wert den Ordner angibt, in dem Berechtigungen hinzugefügt werden sollen (der Ordner "Gesendete Elemente" in diesem Beispiel), und der [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) -Wert enthält Folder: PermissionSet.</span><span class="sxs-lookup"><span data-stu-id="1dbff-271">The first step is to send a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request, where the [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to add permissions (the Sent Items folder in this example) and the [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="1dbff-272">Diese Anforderung Ruft die Berechtigungseinstellungen für den angegebenen Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="1dbff-272">This request will retrieve the permission settings for the folder specified.</span></span> 
  
<span data-ttu-id="1dbff-273">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn Sie die **Bind** -Methode aufrufen, um [Ordnerberechtigungen hinzuzufügen](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="1dbff-273">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [add folder permissions](#bk_enableewsma).</span></span>
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="1dbff-274">Der Server antwortet auf die **GetFolder** -Anforderung mit einer [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass der Ordner erfolgreich abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="1dbff-274">The server responds to the **GetFolder** request with a [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="1dbff-275">Die [Ordner](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) -und [parentfolderid](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) -Werte wurden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="1dbff-275">The [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) and [ParentFolderId](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) values have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="1dbff-276">Verwenden Sie als nächstes den **UpdateFolder** -Vorgang, um das aktualisierte [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)zu senden, das die [Berechtigung](https://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) für den neuen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="1dbff-276">Next, use the **UpdateFolder** operation to send the updated [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx), which includes the [Permission](https://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) for the new user.</span></span> <span data-ttu-id="1dbff-277">Beachten Sie, dass durch das Einschließen des [setfolderfield](https://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) -Elements für den entsprechenden Ordner im [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) -Vorgang alle Berechtigungseinstellungen für den Ordner überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1dbff-277">Note that including the [SetFolderField](https://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) element for the respective folder in the [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation will overwrite all the permission settings on the folder.</span></span> <span data-ttu-id="1dbff-278">Ebenso werden mit der [DeleteFolderField](https://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) -Option des **UpdateFolder** -Vorgangs auch alle Berechtigungseinstellungen für den Ordner gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1dbff-278">Likewise, including the [DeleteFolderField](https://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) option of the **UpdateFolder** operation will also delete all the permission settings on the folder.</span></span> 
  
<span data-ttu-id="1dbff-279">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn Sie die **Update** -Methode aufrufen, um [Ordnerberechtigungen hinzuzufügen](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="1dbff-279">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [add folder permissions](#bk_enableewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="1dbff-280">In der folgenden Codezeile wird die Berechtigungsstufe angegeben.</span><span class="sxs-lookup"><span data-stu-id="1dbff-280">The following line of code specifies the permission level.</span></span>
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

<span data-ttu-id="1dbff-281">Wenn Sie die benutzerdefinierte Berechtigungsstufe verwenden möchten, verwenden Sie stattdessen diesen Code.</span><span class="sxs-lookup"><span data-stu-id="1dbff-281">If you want to use the custom permission level, use this code instead.</span></span>
  
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

<span data-ttu-id="1dbff-282">Der Server antwortet auf die **UpdateFolder** -Anforderung mit einer [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass der Ordner erfolgreich aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1dbff-282">The server responds to the **UpdateFolder** request with an [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was updated successfully.</span></span>
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="1dbff-283">Entfernen von Ordnerberechtigungen mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="1dbff-283">Removing folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="1dbff-284"><a name="bk_removeewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1dbff-284"><a name="bk_removeewsma"> </a></span></span>

<span data-ttu-id="1dbff-285">Im folgenden Codebeispiel wird gezeigt, wie Sie mithilfe der verwaltete EWS-API alle Benutzerberechtigungen für einen bestimmten Ordner mit Ausnahme der standardmäßigen und anonymen Berechtigungen entfernen:</span><span class="sxs-lookup"><span data-stu-id="1dbff-285">The following code example shows how to use the EWS Managed API to remove all user permissions on a specific folder, except for the default and anonymous permissions, by:</span></span>
  
1. <span data-ttu-id="1dbff-286">Aufrufen der aktuellen Berechtigungen für einen Ordner mithilfe der **Bind** -Methode.</span><span class="sxs-lookup"><span data-stu-id="1dbff-286">Getting the current permissions for a folder by using the **Bind** method.</span></span> 
    
2. <span data-ttu-id="1dbff-287">Durchlaufen der **Permissions** -Auflistung und Entfernen von Berechtigungen für einzelne Benutzer.</span><span class="sxs-lookup"><span data-stu-id="1dbff-287">Iterating through the **Permissions** collection and removing permissions for individual users.</span></span> 
    
3. <span data-ttu-id="1dbff-288">Aufrufen der **Update** -Methode, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1dbff-288">Calling the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="1dbff-289">In diesem Beispiel werden alle Benutzerberechtigungen für einen Ordner entfernt.</span><span class="sxs-lookup"><span data-stu-id="1dbff-289">This example removes all user permissions on a folder.</span></span> <span data-ttu-id="1dbff-290">Wenn Sie dieses Beispiel ändern möchten, um Berechtigungen nur für einen bestimmten Benutzer zu entfernen, ändern Sie die folgende Codezeile, um entweder den Anzeigenamen oder die SMTP-Adresse des Benutzers zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1dbff-290">If you want to modify this example to remove permissions only for a specific user, change the following line of code to identify either the display name or SMTP address of the user.</span></span>
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

<span data-ttu-id="1dbff-291">In diesem Beispiel wird davon ausgegangen, dass **Service** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Postfachbesitzer ist und dass der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="1dbff-291">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="removing-folder-permissions-by-using-ews"></a><span data-ttu-id="1dbff-292">Entfernen von Ordnerberechtigungen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="1dbff-292">Removing folder permissions by using EWS</span></span>
<span data-ttu-id="1dbff-293"><a name="bk_removeews"> </a></span><span class="sxs-lookup"><span data-stu-id="1dbff-293"><a name="bk_removeews"> </a></span></span>

<span data-ttu-id="1dbff-294">Die folgenden EWS-Codebeispiele zeigen, wie Sie alle Benutzerberechtigungen für einen bestimmten Ordner mit Ausnahme der Standard-und anonymen Berechtigungen entfernen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-294">The following EWS code examples show how to remove all user permissions on a specific folder, except for the default and anonymous permissions.</span></span>
  
<span data-ttu-id="1dbff-295">Senden Sie zunächst eine [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Anforderung, wobei der [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) -Wert den Ordner angibt, in dem Berechtigungen entfernt werden sollen (der Ordner "Gesendete Elemente" in diesem Beispiel), und der [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) -Wert enthält Folder: PermissionSet.</span><span class="sxs-lookup"><span data-stu-id="1dbff-295">First, send a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request where the [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to remove permissions (the Sent Items folder in this example) and the [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="1dbff-296">Diese Anforderung Ruft das [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) für den angegebenen Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="1dbff-296">This request will retrieve the [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) for the folder specified.</span></span> 
  
<span data-ttu-id="1dbff-297">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn Sie die **Bind** -Methode aufrufen, um [Ordnerberechtigungen zu entfernen](#bk_removeewsma).</span><span class="sxs-lookup"><span data-stu-id="1dbff-297">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="1dbff-298">Der Server antwortet auf die **GetFolder** -Anforderung mit einer [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass der Ordner erfolgreich abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="1dbff-298">The server responds to the **GetFolder** request with a [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="1dbff-299">Die Werte der Elemente **Folder** -und **parentfolderid** wurden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="1dbff-299">The values of the **FolderId** and **ParentFolderId** elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="1dbff-300">Verwenden Sie als nächstes den **UpdateFolder** -Vorgang, um das aktualisierte **PermissionSet**zu senden, das nicht die **Berechtigung** für den entfernten Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="1dbff-300">Next, use the **UpdateFolder** operation to send the updated **PermissionSet**, which does not include the **Permission** for the removed user.</span></span> 
  
<span data-ttu-id="1dbff-301">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn Sie die **Update** -Methode aufrufen, um [Ordnerberechtigungen zu entfernen](#bk_removeewsma).</span><span class="sxs-lookup"><span data-stu-id="1dbff-301">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="1dbff-302">Der Server antwortet auf die **UpdateFolder** -Anforderung mit einer **UpdateFolderResponse** -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass das Update erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1dbff-302">The server responds to the **UpdateFolder** request with an **UpdateFolderResponse** message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the update was successful.</span></span>
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="1dbff-303">Aktualisieren von Ordnerberechtigungen mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="1dbff-303">Updating folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="1dbff-304"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1dbff-304"><a name="bk_updateewsma"> </a></span></span>

<span data-ttu-id="1dbff-305">Sie können die Ordnerberechtigungen für einen bestimmten Ordner auch mithilfe der verwaltete EWS-API aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1dbff-305">You can also update folder permissions for a specific folder by using the EWS Managed API.</span></span> <span data-ttu-id="1dbff-306">So aktualisieren Sie die Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="1dbff-306">To update the permissions:</span></span> 
  
1. <span data-ttu-id="1dbff-307">[Entfernen Sie die Ordnerberechtigungen](#bk_removeewsma) für die veralteten Berechtigungen, rufen Sie jedoch nicht die **Update** -Methode (noch) auf.</span><span class="sxs-lookup"><span data-stu-id="1dbff-307">[Remove the folder permissions](#bk_removeewsma) for the outdated permissions, but do not call the **Update** method (yet).</span></span> 
    
2. <span data-ttu-id="1dbff-308">[Fügen Sie Ordnerberechtigungen für die neuen oder geänderten Benutzer hinzu](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="1dbff-308">[Add folder permissions for the new or changed users](#bk_enableewsma).</span></span>
    
3. <span data-ttu-id="1dbff-309">Rufen Sie die **Update** -Methode auf, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1dbff-309">Call the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="1dbff-310">Wenn Sie versuchen, zwei Berechtigungssätze für denselben Benutzer hinzuzufügen, wird ein **ServiceResponseException** -Fehler mit der folgenden Beschreibung angezeigt: "der angegebene Berechtigungssatz enthält doppelte userids".</span><span class="sxs-lookup"><span data-stu-id="1dbff-310">If you try to add two sets of permissions for the same user, you will receive a **ServiceResponseException** error with the following description: "The specified permission set contains duplicate UserIds".</span></span> <span data-ttu-id="1dbff-311">Entfernen Sie in diesem Fall die aktuellen Berechtigungen aus der **Permission** -Auflistung, und fügen Sie dann der **Permission** -Auflistung die neuen Berechtigungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="1dbff-311">In that case, remove the current permissions from the **Permission** collection, then add the new permissions to the **Permission** collection.</span></span> 
  
## <a name="updating-folder-permissions-by-using-ews"></a><span data-ttu-id="1dbff-312">Aktualisieren von Ordnerberechtigungen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="1dbff-312">Updating folder permissions by using EWS</span></span>
<span data-ttu-id="1dbff-313"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="1dbff-313"><a name="bk_updateews"> </a></span></span>

<span data-ttu-id="1dbff-314">Sie können die Ordnerberechtigungen für bestimmte Ordner auch mithilfe von EWS aktualisieren, indem Sie den Vorgang zum Entfernen und hinzufügen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="1dbff-314">You can also update folder permissions for specific folders by using EWS by combining the removal and addition process.</span></span> <span data-ttu-id="1dbff-315">So aktualisieren Sie die Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="1dbff-315">To update the permissions:</span></span> 
  
1. <span data-ttu-id="1dbff-316">Dient zum Abrufen der aktuellen Berechtigungen des Ordners mithilfe des **GetFolder** -Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1dbff-316">Retrieve the folder's current permissions by using the **GetFolder** operation.</span></span> 
    
2. <span data-ttu-id="1dbff-317">Senden Sie eine aktualisierte Liste mit Berechtigungen mithilfe des **UpdateFolder** -Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1dbff-317">Send an updated list of permissions by using the **UpdateFolder** operation.</span></span> 
    
<span data-ttu-id="1dbff-318">Dabei handelt es sich um dieselben beiden Vorgänge, die Sie zum [aktivieren](#bk_enableews) oder [Entfernen des Zugriffs](#bk_removeews) mithilfe von EWS verwenden.</span><span class="sxs-lookup"><span data-stu-id="1dbff-318">These are the same two operations you use to [enable](#bk_enableews) or [remove access](#bk_removeews) by using EWS.</span></span> <span data-ttu-id="1dbff-319">Der einzige Unterschied besteht darin, dass, wenn Sie die **GetFolder** -Antwort erhalten, eine **Berechtigungs** Gruppe für den Benutzer enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1dbff-319">The only difference is that when you receive the **GetFolder** response, it will contain a **Permission** set for user.</span></span> <span data-ttu-id="1dbff-320">Ersetzen Sie einfach das vorhandene **Permission** -Element durch das neue **Permission** -Element, und senden Sie dann den **UpdateFolder** -Vorgang mit dem neuen **Berechtigungs** Wert oder den neuen Werten.</span><span class="sxs-lookup"><span data-stu-id="1dbff-320">Simply replace that existing **Permission** element with the new **Permission** element, and then send the **UpdateFolder** operation with the new **Permission** value or values.</span></span> 
  
<span data-ttu-id="1dbff-321">Wenn Sie versuchen, zwei Berechtigungssätze für denselben Benutzer hinzuzufügen, erhalten Sie den **Response Code** -Wert **ErrorDuplicateUserIdsSpecified**.</span><span class="sxs-lookup"><span data-stu-id="1dbff-321">If you try to add two sets of permissions for the same user, you will receive a **ResponseCode** value of **ErrorDuplicateUserIdsSpecified**.</span></span> <span data-ttu-id="1dbff-322">Entfernen Sie in diesem Fall den Wert veralteter Berechtigungen für den Benutzer aus der Anforderung, und wiederholen Sie die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1dbff-322">In that case, remove the outdated Permission value for the user from the request and then retry the request.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1dbff-323">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="1dbff-323">Next steps</span></span>

<span data-ttu-id="1dbff-324">Nachdem Sie einem bestimmten Ordner eine Benutzerberechtigung erteilt haben, kann der Benutzer auf den Ordner als Stellvertreter zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1dbff-324">After you give a user permission to a specific folder, the user can access the folder as a delegate.</span></span> <span data-ttu-id="1dbff-325">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="1dbff-325">For more information, see:</span></span>
  
- [<span data-ttu-id="1dbff-326">Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1dbff-326">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="1dbff-327">Zugriff auf einen Kalender als Delegat mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1dbff-327">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="1dbff-328">Zugriff auf Kontakte als Delegat mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1dbff-328">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="1dbff-329">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dbff-329">See also</span></span>

- [<span data-ttu-id="1dbff-330">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1dbff-330">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="1dbff-331">Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1dbff-331">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="1dbff-332">Ordner und Elemente in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1dbff-332">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    

