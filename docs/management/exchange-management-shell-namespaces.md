---
title: Exchange-Verwaltungsshell Namespaces
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff849238-06b7-4891-884b-c51ce0f1ebbc
description: Hier finden Sie Informationen zu den Namespaces für die Exchange-Verwaltungsshell in Exchange.
ms.openlocfilehash: 370c3e6cde48662eba8c62ad20e42fb716e66f2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44435814"
---
# <a name="exchange-management-shell-namespaces"></a><span data-ttu-id="d407d-103">Exchange-Verwaltungsshell Namespaces</span><span class="sxs-lookup"><span data-stu-id="d407d-103">Exchange Management Shell namespaces</span></span>

<span data-ttu-id="d407d-104">Hier finden Sie Informationen zu den Namespaces für die Exchange-Verwaltungsshell in Exchange.</span><span class="sxs-lookup"><span data-stu-id="d407d-104">Find information about the namespaces for the Exchange Management Shell in Exchange.</span></span>
  
<span data-ttu-id="d407d-105">**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="d407d-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="d407d-106">Exchange-Verwaltungsshell Anwendungen für Exchange Online, Exchange Online als Teil Office 365 oder eine Version von Exchange, die mit Exchange 2013 beginnt, interagieren mit der Windows PowerShell Umgebung über die Typen, die vom **System. Management. Automation-** Namespace verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="d407d-106">Exchange Management Shell applications for Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013 interact with the Windows PowerShell environment through the types that are exposed by the **System.Management.Automation** namespace.</span></span> <span data-ttu-id="d407d-107">Die Exchange-Verwaltungsshell-Cmdlets verwenden Typen aus einer Reihe von Exchange-Bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="d407d-107">The Exchange Management Shell cmdlets use types from a number of Exchange libraries.</span></span> <span data-ttu-id="d407d-108">Dieser Abschnitt enthält Referenzinformationen zu den Typen und Schnittstellen aus den Exchange-Bibliotheken, die von Exchange-Verwaltungsshell-Cmdlets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d407d-108">This section provides reference information about the types and interfaces from the Exchange libraries that are used by Exchange Management Shell cmdlets.</span></span> 
  
<span data-ttu-id="d407d-109">Die Exchange-Verwaltungsshell enthält die folgenden Namespaces:</span><span class="sxs-lookup"><span data-stu-id="d407d-109">The Exchange Management Shell contains the following namespaces:</span></span>
  
- [<span data-ttu-id="d407d-110">Microsoft. Exchange. Configuration. Tasks</span><span class="sxs-lookup"><span data-stu-id="d407d-110">Microsoft.Exchange.Configuration.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Configuration.Tasks.aspx)
    
- [<span data-ttu-id="d407d-111">Microsoft. Exchange. Data</span><span class="sxs-lookup"><span data-stu-id="d407d-111">Microsoft.Exchange.Data</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx)
    
- [<span data-ttu-id="d407d-112">Microsoft. Exchange. Data. Directory</span><span class="sxs-lookup"><span data-stu-id="d407d-112">Microsoft.Exchange.Data.Directory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.aspx)
    
- [<span data-ttu-id="d407d-113">Microsoft. Exchange. Data. Directory. Management</span><span class="sxs-lookup"><span data-stu-id="d407d-113">Microsoft.Exchange.Data.Directory.Management</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.Management.aspx)
    
- [<span data-ttu-id="d407d-114">Microsoft. Exchange. Data. Directory. Permission</span><span class="sxs-lookup"><span data-stu-id="d407d-114">Microsoft.Exchange.Data.Directory.Permission</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.Permission.aspx)
    
- [<span data-ttu-id="d407d-115">Microsoft. Exchange. Data. Directory. Recipient</span><span class="sxs-lookup"><span data-stu-id="d407d-115">Microsoft.Exchange.Data.Directory.Recipient</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.Recipient.aspx)
    
- [<span data-ttu-id="d407d-116">Microsoft. Exchange. Data. Directory. "SystemConfiguration</span><span class="sxs-lookup"><span data-stu-id="d407d-116">Microsoft.Exchange.Data.Directory.SystemConfiguration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.aspx)
    
- [<span data-ttu-id="d407d-117">Microsoft. Exchange. Data. MAPI</span><span class="sxs-lookup"><span data-stu-id="d407d-117">Microsoft.Exchange.Data.Mapi</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mapi.aspx)
    
- [<span data-ttu-id="d407d-118">Microsoft. Exchange. Data. Queue Digest</span><span class="sxs-lookup"><span data-stu-id="d407d-118">Microsoft.Exchange.Data.QueueDigest</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.QueueDigest.aspx)
    
- [<span data-ttu-id="d407d-119">Microsoft. Exchange. Data. QueueViewer</span><span class="sxs-lookup"><span data-stu-id="d407d-119">Microsoft.Exchange.Data.QueueViewer</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.QueueViewer.aspx)
    
- [<span data-ttu-id="d407d-120">Microsoft. Exchange. Data. RightsManagement</span><span class="sxs-lookup"><span data-stu-id="d407d-120">Microsoft.Exchange.Data.RightsManagement</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.RightsManagement.aspx)
    
- [<span data-ttu-id="d407d-121">Microsoft. Exchange. Data. Storage</span><span class="sxs-lookup"><span data-stu-id="d407d-121">Microsoft.Exchange.Data.Storage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.aspx)
    
- [<span data-ttu-id="d407d-122">Microsoft. Exchange. Data. Storage. ActiveMonitoring</span><span class="sxs-lookup"><span data-stu-id="d407d-122">Microsoft.Exchange.Data.Storage.ActiveMonitoring</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.ActiveMonitoring.aspx)
    
- [<span data-ttu-id="d407d-123">Microsoft. Exchange. Data. Storage. Management</span><span class="sxs-lookup"><span data-stu-id="d407d-123">Microsoft.Exchange.Data.Storage.Management</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.Management.aspx)
    
- [<span data-ttu-id="d407d-124">Microsoft. Exchange. Data. Storage. Management. Migration</span><span class="sxs-lookup"><span data-stu-id="d407d-124">Microsoft.Exchange.Data.Storage.Management.Migration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.Management.Migration.aspx)
    
- [<span data-ttu-id="d407d-125">Microsoft. Exchange. Data. Storage. StoreConfigurableType</span><span class="sxs-lookup"><span data-stu-id="d407d-125">Microsoft.Exchange.Data.Storage.StoreConfigurableType</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.StoreConfigurableType.aspx)
    
- [<span data-ttu-id="d407d-126">Microsoft. Exchange. EdgeSync. Validation</span><span class="sxs-lookup"><span data-stu-id="d407d-126">Microsoft.Exchange.EdgeSync.Validation</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.EdgeSync.Validation.aspx)
    
- [<span data-ttu-id="d407d-127">Microsoft. Exchange. MailboxReplicationService</span><span class="sxs-lookup"><span data-stu-id="d407d-127">Microsoft.Exchange.MailboxReplicationService</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MailboxReplicationService.aspx)
    
- [<span data-ttu-id="d407d-128">Microsoft. Exchange. Management. AgentTasks</span><span class="sxs-lookup"><span data-stu-id="d407d-128">Microsoft.Exchange.Management.AgentTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.AgentTasks.aspx)
    
- [<span data-ttu-id="d407d-129">Microsoft. Exchange. Management. ClassificationDefinitions</span><span class="sxs-lookup"><span data-stu-id="d407d-129">Microsoft.Exchange.Management.ClassificationDefinitions</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ClassificationDefinitions.aspx)
    
- [<span data-ttu-id="d407d-130">Microsoft. Exchange. Management. Extension</span><span class="sxs-lookup"><span data-stu-id="d407d-130">Microsoft.Exchange.Management.Extension</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Extension.aspx)
    
- [<span data-ttu-id="d407d-131">Microsoft. Exchange. Management. FfoReporting</span><span class="sxs-lookup"><span data-stu-id="d407d-131">Microsoft.Exchange.Management.FfoReporting</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.FfoReporting.aspx)
    
- [<span data-ttu-id="d407d-132">Microsoft. Exchange. Management. FfoReporting. Common</span><span class="sxs-lookup"><span data-stu-id="d407d-132">Microsoft.Exchange.Management.FfoReporting.Common</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.FfoReporting.Common.aspx)
    
- [<span data-ttu-id="d407d-133">Microsoft. Exchange. Management. ' MessagingPolicies '. AddressRewrite</span><span class="sxs-lookup"><span data-stu-id="d407d-133">Microsoft.Exchange.Management.MessagingPolicies.AddressRewrite</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.MessagingPolicies.AddressRewrite.aspx)
    
- [<span data-ttu-id="d407d-134">Microsoft. Exchange. Management. Migration</span><span class="sxs-lookup"><span data-stu-id="d407d-134">Microsoft.Exchange.Management.Migration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Migration.aspx)
    
- [<span data-ttu-id="d407d-135">Microsoft. Exchange. Management. OutlookProtectionRules</span><span class="sxs-lookup"><span data-stu-id="d407d-135">Microsoft.Exchange.Management.OutlookProtectionRules</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.OutlookProtectionRules.aspx)
    
- [<span data-ttu-id="d407d-136">Microsoft. Exchange. Management. PolicyNudges</span><span class="sxs-lookup"><span data-stu-id="d407d-136">Microsoft.Exchange.Management.PolicyNudges</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.PolicyNudges.aspx)
    
- [<span data-ttu-id="d407d-137">Microsoft. Exchange. Management. ProvisioningTasks</span><span class="sxs-lookup"><span data-stu-id="d407d-137">Microsoft.Exchange.Management.ProvisioningTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ProvisioningTasks.aspx)
    
- [<span data-ttu-id="d407d-138">Microsoft. Exchange. Management. RecipientTasks</span><span class="sxs-lookup"><span data-stu-id="d407d-138">Microsoft.Exchange.Management.RecipientTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.RecipientTasks.aspx)
    
- [<span data-ttu-id="d407d-139">Microsoft. Exchange. Management. ReportingTask. Common</span><span class="sxs-lookup"><span data-stu-id="d407d-139">Microsoft.Exchange.Management.ReportingTask.Common</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ReportingTask.Common.aspx)
    
- [<span data-ttu-id="d407d-140">Microsoft. Exchange. Management. ReportingTask. Query</span><span class="sxs-lookup"><span data-stu-id="d407d-140">Microsoft.Exchange.Management.ReportingTask.Query</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ReportingTask.Query.aspx)
    
- [<span data-ttu-id="d407d-141">Microsoft. Exchange. Management. ReportingTask. TenantReport</span><span class="sxs-lookup"><span data-stu-id="d407d-141">Microsoft.Exchange.Management.ReportingTask.TenantReport</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ReportingTask.TenantReport.aspx)
    
- [<span data-ttu-id="d407d-142">Microsoft. Exchange. Management. RightsManagement</span><span class="sxs-lookup"><span data-stu-id="d407d-142">Microsoft.Exchange.Management.RightsManagement</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.RightsManagement.aspx)
    
- [<span data-ttu-id="d407d-143">Microsoft. Exchange. Management. Sharing</span><span class="sxs-lookup"><span data-stu-id="d407d-143">Microsoft.Exchange.Management.Sharing</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Sharing.aspx)
    
- [<span data-ttu-id="d407d-144">Microsoft. Exchange. Management. StoreTasks</span><span class="sxs-lookup"><span data-stu-id="d407d-144">Microsoft.Exchange.Management.StoreTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.StoreTasks.aspx)
    
- [<span data-ttu-id="d407d-145">Microsoft. Exchange. Management. Supervision</span><span class="sxs-lookup"><span data-stu-id="d407d-145">Microsoft.Exchange.Management.Supervision</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Supervision.aspx)
    
- [<span data-ttu-id="d407d-146">Microsoft. Exchange. Management. SystemConfigurationTasks</span><span class="sxs-lookup"><span data-stu-id="d407d-146">Microsoft.Exchange.Management.SystemConfigurationTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.SystemConfigurationTasks.aspx)
    
- [<span data-ttu-id="d407d-147">Microsoft. Exchange. Management. Tasks</span><span class="sxs-lookup"><span data-stu-id="d407d-147">Microsoft.Exchange.Management.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Tasks.aspx)
    
- [<span data-ttu-id="d407d-148">Microsoft. Exchange. Management. Tools</span><span class="sxs-lookup"><span data-stu-id="d407d-148">Microsoft.Exchange.Management.Tools</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Tools.aspx)
    
- [<span data-ttu-id="d407d-149">Microsoft. Exchange. Management. Tracking</span><span class="sxs-lookup"><span data-stu-id="d407d-149">Microsoft.Exchange.Management.Tracking</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Tracking.aspx)
    
- [<span data-ttu-id="d407d-150">Microsoft. Exchange. Management. TransportLogSearchTasks</span><span class="sxs-lookup"><span data-stu-id="d407d-150">Microsoft.Exchange.Management.TransportLogSearchTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.TransportLogSearchTasks.aspx)
    
- [<span data-ttu-id="d407d-151">Microsoft. Exchange. ' MessagingPolicies '. CompliancePrograms. Tasks</span><span class="sxs-lookup"><span data-stu-id="d407d-151">Microsoft.Exchange.MessagingPolicies.CompliancePrograms.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MessagingPolicies.CompliancePrograms.Tasks.aspx)
    
- [<span data-ttu-id="d407d-152">Microsoft. Exchange. ' MessagingPolicies '. Journaling</span><span class="sxs-lookup"><span data-stu-id="d407d-152">Microsoft.Exchange.MessagingPolicies.Journaling</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MessagingPolicies.Journaling.aspx)
    
- [<span data-ttu-id="d407d-153">Microsoft. Exchange. ' MessagingPolicies '. Rules. Tasks</span><span class="sxs-lookup"><span data-stu-id="d407d-153">Microsoft.Exchange.MessagingPolicies.Rules.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MessagingPolicies.Rules.Tasks.aspx)
    
- [<span data-ttu-id="d407d-154">Microsoft. Exchange. Migration</span><span class="sxs-lookup"><span data-stu-id="d407d-154">Microsoft.Exchange.Migration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Migration.aspx)
    
- [<span data-ttu-id="d407d-155">Microsoft. Exchange. Monitoring</span><span class="sxs-lookup"><span data-stu-id="d407d-155">Microsoft.Exchange.Monitoring</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Monitoring.aspx)
    
- [<span data-ttu-id="d407d-156">Microsoft. Exchange. Monitoring. ActiveMonitoring</span><span class="sxs-lookup"><span data-stu-id="d407d-156">Microsoft.Exchange.Monitoring.ActiveMonitoring</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Monitoring.ActiveMonitoring.aspx)
    
- [<span data-ttu-id="d407d-157">Microsoft. Exchange. Transport. Sync. Common. Subscription</span><span class="sxs-lookup"><span data-stu-id="d407d-157">Microsoft.Exchange.Transport.Sync.Common.Subscription</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.aspx)
    
- [<span data-ttu-id="d407d-158">Microsoft. Exchange. Transport. Sync. Common. Subscription. Connect</span><span class="sxs-lookup"><span data-stu-id="d407d-158">Microsoft.Exchange.Transport.Sync.Common.Subscription.Connect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Connect.aspx)
    
- [<span data-ttu-id="d407d-159">Microsoft. Exchange. Transport. Sync. Common. Subscription. DeltaSync</span><span class="sxs-lookup"><span data-stu-id="d407d-159">Microsoft.Exchange.Transport.Sync.Common.Subscription.DeltaSync</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.DeltaSync.aspx)
    
- [<span data-ttu-id="d407d-160">Microsoft. Exchange. Transport. Sync. Common. Subscription. IMAP</span><span class="sxs-lookup"><span data-stu-id="d407d-160">Microsoft.Exchange.Transport.Sync.Common.Subscription.Imap</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Imap.aspx)
    
- [<span data-ttu-id="d407d-161">Microsoft. Exchange. Transport. Sync. Common. Subscription. PIM</span><span class="sxs-lookup"><span data-stu-id="d407d-161">Microsoft.Exchange.Transport.Sync.Common.Subscription.Pim</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Pim.aspx)
    
- [<span data-ttu-id="d407d-162">Microsoft. Exchange. Transport. Sync. Common. Subscription. Pop</span><span class="sxs-lookup"><span data-stu-id="d407d-162">Microsoft.Exchange.Transport.Sync.Common.Subscription.Pop</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Pop.aspx)
    
- [<span data-ttu-id="d407d-163">Microsoft. Exchange. um. RPC</span><span class="sxs-lookup"><span data-stu-id="d407d-163">Microsoft.Exchange.UM.Rpc</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.UM.Rpc.aspx)
    
- [<span data-ttu-id="d407d-164">Microsoft. Exchange. um. UMCommon</span><span class="sxs-lookup"><span data-stu-id="d407d-164">Microsoft.Exchange.UM.UMCommon</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.UM.UMCommon.aspx)
    
- [<span data-ttu-id="d407d-165">Microsoft. Exchange. Rolle workloadmanagement</span><span class="sxs-lookup"><span data-stu-id="d407d-165">Microsoft.Exchange.WorkloadManagement</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.WorkloadManagement.aspx)
    
## <a name="see-also"></a><span data-ttu-id="d407d-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d407d-166">See also</span></span>

- [<span data-ttu-id="d407d-167">Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="d407d-167">Exchange Management Shell</span></span>](exchange-management-shell.md)  
- [<span data-ttu-id="d407d-168">Erstellen von Exchange-Verwaltungsshell Tools</span><span class="sxs-lookup"><span data-stu-id="d407d-168">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md) 
- [<span data-ttu-id="d407d-169">Eingabe- und Ausgabetypen für Cmdlets der Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="d407d-169">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)
    

