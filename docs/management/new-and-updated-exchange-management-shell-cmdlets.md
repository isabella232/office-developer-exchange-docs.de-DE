---
title: Neue und aktualisierte Exchange-Verwaltungsshell-Cmdlets
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5941a439-94d2-4133-81fc-7240863a13df
description: Hier finden Sie Informationen zu Neuerungen in der Exchange-Verwaltungsshell in Exchange.
ms.openlocfilehash: bda6607be20f2a21bc22d472d63615d46634d8ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457144"
---
# <a name="new-and-updated-exchange-management-shell-cmdlets"></a><span data-ttu-id="8cf24-103">Neue und aktualisierte Exchange-Verwaltungsshell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cf24-103">New and updated Exchange Management Shell cmdlets</span></span>

<span data-ttu-id="8cf24-104">Hier finden Sie Informationen zu Neuerungen in der Exchange-Verwaltungsshell in Exchange.</span><span class="sxs-lookup"><span data-stu-id="8cf24-104">Find information about what's new in the Exchange Management Shell in Exchange.</span></span>
  
<span data-ttu-id="8cf24-105">**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="8cf24-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="8cf24-106">Dieser Artikel enthält Informationen zu neuen Cmdlets in der Exchange-Verwaltungsshell, Cmdlets, die in geändert wurden, und Cmdlets, die aus Exchange Online entfernt wurden, Exchange Online im Rahmen von Office 365 oder einer lokalen Exchange-Version.</span><span class="sxs-lookup"><span data-stu-id="8cf24-106">This article provides information about new Exchange Management shell cmdlets, cmdlets that were modified in, and cmdlets that were removed from Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange.</span></span>
  
## <a name="new-and-updated-cmdlets-in-exchange-2013-sp1"></a><span data-ttu-id="8cf24-107">Neue und aktualisierte Cmdlets in Exchange 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="8cf24-107">New and updated cmdlets in Exchange 2013 SP1</span></span>

### <a name="new-cmdlets"></a><span data-ttu-id="8cf24-108">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cf24-108">New cmdlets</span></span>

<span data-ttu-id="8cf24-109">Die folgenden Cmdlets wurden in Build 15.00.0847.032 (Exchange Server 2013 SP1) eingeführt:</span><span class="sxs-lookup"><span data-stu-id="8cf24-109">The following cmdlets were introduced in build 15.00.0847.032 (Exchange Server 2013 SP1):</span></span>
  
- <span data-ttu-id="8cf24-110">**Get-AuthRedirect**</span><span class="sxs-lookup"><span data-stu-id="8cf24-110">**Get-AuthRedirect**</span></span>
    
- <span data-ttu-id="8cf24-111">**New-AuthRedirect**</span><span class="sxs-lookup"><span data-stu-id="8cf24-111">**New-AuthRedirect**</span></span>
    
- <span data-ttu-id="8cf24-112">**Remove-AuthRedirect**</span><span class="sxs-lookup"><span data-stu-id="8cf24-112">**Remove-AuthRedirect**</span></span>
    
- <span data-ttu-id="8cf24-113">**Gruppe-AuthRedirect**</span><span class="sxs-lookup"><span data-stu-id="8cf24-113">**Set-AuthRedirect**</span></span>
    
- <span data-ttu-id="8cf24-114">**New-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="8cf24-114">**New-DataClassification**</span></span>
    
- <span data-ttu-id="8cf24-115">**Remove-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="8cf24-115">**Remove-DataClassification**</span></span>
    
- <span data-ttu-id="8cf24-116">**Gruppe-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="8cf24-116">**Set-DataClassification**</span></span>
    
- <span data-ttu-id="8cf24-117">**Neu – Fingerabdruck**</span><span class="sxs-lookup"><span data-stu-id="8cf24-117">**New-FingerPrint**</span></span>
    
- <span data-ttu-id="8cf24-118">**Get-MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="8cf24-118">**Get-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="8cf24-119">**New-MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="8cf24-119">**New-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="8cf24-120">**Remove-MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="8cf24-120">**Remove-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="8cf24-121">**Gruppe-MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="8cf24-121">**Set-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="8cf24-122">**Get-OMEConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8cf24-122">**Get-OMEConfiguration**</span></span>
    
- <span data-ttu-id="8cf24-123">**Set-OMEConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8cf24-123">**Set-OMEConfiguration**</span></span>
    
- <span data-ttu-id="8cf24-124">**Get-SmimeConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-124">**Get-SmimeConfig**</span></span>
    
- <span data-ttu-id="8cf24-125">**Gruppe-SmimeConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-125">**Set-SmimeConfig**</span></span>
    
- <span data-ttu-id="8cf24-126">**Get-IntraOrganizationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8cf24-126">**Get-IntraOrganizationConfiguration**</span></span>
    
- <span data-ttu-id="8cf24-127">**Get-IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-127">**Get-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="8cf24-128">**New-IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-128">**New-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="8cf24-129">**Remove-IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-129">**Remove-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="8cf24-130">**Gruppe-IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-130">**Set-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="8cf24-131">**Get-HistoricalSearch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-131">**Get-HistoricalSearch**</span></span>
    
- <span data-ttu-id="8cf24-132">**Start-HistoricalSearch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-132">**Start-HistoricalSearch**</span></span>
    
- <span data-ttu-id="8cf24-133">**Stop-HistoricalSearch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-133">**Stop-HistoricalSearch**</span></span>
    
- <span data-ttu-id="8cf24-134">**New-SearchDocumentFormat**</span><span class="sxs-lookup"><span data-stu-id="8cf24-134">**New-SearchDocumentFormat**</span></span>
    
- <span data-ttu-id="8cf24-135">**Remove-SearchDocumentFormat**</span><span class="sxs-lookup"><span data-stu-id="8cf24-135">**Remove-SearchDocumentFormat**</span></span>
    
### <a name="updated-cmdlets"></a><span data-ttu-id="8cf24-136">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cf24-136">Updated cmdlets</span></span>

<span data-ttu-id="8cf24-137">Die folgenden Cmdlets wurden in Build 15.00.0847.032 (Exchange 2013 SP1) aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="8cf24-137">The following cmdlets were updated in build 15.00.0847.032 (Exchange 2013 SP1):</span></span>
  
- <span data-ttu-id="8cf24-138">**Get-AuditLogSearch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-138">**Get-AuditLogSearch**</span></span>
    
- <span data-ttu-id="8cf24-139">**Get-QuarantineMessage**</span><span class="sxs-lookup"><span data-stu-id="8cf24-139">**Get-QuarantineMessage**</span></span>
    
- <span data-ttu-id="8cf24-140">**New-InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-140">**New-InboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-141">**New-MailboxDatabase**</span><span class="sxs-lookup"><span data-stu-id="8cf24-141">**New-MailboxDatabase**</span></span>
    
- <span data-ttu-id="8cf24-142">**New-PublicFolderMoveRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-142">**New-PublicFolderMoveRequest**</span></span>
    
- <span data-ttu-id="8cf24-143">**New-TransportRule**</span><span class="sxs-lookup"><span data-stu-id="8cf24-143">**New-TransportRule**</span></span>
    
- <span data-ttu-id="8cf24-144">**Gruppe-Frontend Transportservice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-144">**Set-FrontendTransportService**</span></span>
    
- <span data-ttu-id="8cf24-145">**Gruppe-InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-145">**Set-InboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-146">**Set-Mailbox**</span><span class="sxs-lookup"><span data-stu-id="8cf24-146">**Set-Mailbox**</span></span>
    
- <span data-ttu-id="8cf24-147">**Gruppe-Mailbox Transportservice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-147">**Set-MailboxTransportService**</span></span>
    
- <span data-ttu-id="8cf24-148">**Gruppe-MoveRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-148">**Set-MoveRequest**</span></span>
    
- <span data-ttu-id="8cf24-149">**Set-OrganizationConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-149">**Set-OrganizationConfig**</span></span>
    
- <span data-ttu-id="8cf24-150">**Gruppe-OwaMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-150">**Set-OwaMailboxPolicy**</span></span>
    
- <span data-ttu-id="8cf24-151">**Gruppe-OwaVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="8cf24-151">**Set-OwaVirtualDirectory**</span></span>
    
- <span data-ttu-id="8cf24-152">**Festlegen von TransportConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-152">**Set-TransportConfig**</span></span>
    
- <span data-ttu-id="8cf24-153">**Festlegen-TransportRule**</span><span class="sxs-lookup"><span data-stu-id="8cf24-153">**Set-TransportRule**</span></span>
    
- <span data-ttu-id="8cf24-154">**Festlegen-Transport Server**</span><span class="sxs-lookup"><span data-stu-id="8cf24-154">**Set-TransportServer**</span></span>
    
- <span data-ttu-id="8cf24-155">**Gruppe-Transportservice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-155">**Set-TransportService**</span></span>
    
- <span data-ttu-id="8cf24-156">**Test-MRSHealth**</span><span class="sxs-lookup"><span data-stu-id="8cf24-156">**Test-MRSHealth**</span></span>
    
- <span data-ttu-id="8cf24-157">**Test-OAuthConnectivity**</span><span class="sxs-lookup"><span data-stu-id="8cf24-157">**Test-OAuthConnectivity**</span></span>
    
### <a name="removed-cmdlets"></a><span data-ttu-id="8cf24-158">Entfernte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cf24-158">Removed cmdlets</span></span>

<span data-ttu-id="8cf24-159">Die folgenden Cmdlets wurden aus Build 15.00.0847.032 (Exchange 2013 SP1) entfernt:</span><span class="sxs-lookup"><span data-stu-id="8cf24-159">The following cmdlets were removed from build 15.00.0847.032 (Exchange 2013 SP1):</span></span>
  
- <span data-ttu-id="8cf24-160">**Get-AvailabilityReportOutage**</span><span class="sxs-lookup"><span data-stu-id="8cf24-160">**Get-AvailabilityReportOutage**</span></span>
    
- <span data-ttu-id="8cf24-161">**New-AvailabilityReportOutage**</span><span class="sxs-lookup"><span data-stu-id="8cf24-161">**New-AvailabilityReportOutage**</span></span>
    
- <span data-ttu-id="8cf24-162">**Remove-AvailabilityReportOutage**</span><span class="sxs-lookup"><span data-stu-id="8cf24-162">**Remove-AvailabilityReportOutage**</span></span>
    
- <span data-ttu-id="8cf24-163">**Gruppe-AvailabilityReportOutage**</span><span class="sxs-lookup"><span data-stu-id="8cf24-163">**Set-AvailabilityReportOutage**</span></span>
    
## <a name="new-and-updated-cmdlets-in-exchange-2013"></a><span data-ttu-id="8cf24-164">Neue und aktualisierte Cmdlets in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8cf24-164">New and updated cmdlets in Exchange 2013</span></span>

### <a name="new-cmdlets"></a><span data-ttu-id="8cf24-165">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cf24-165">New cmdlets</span></span>
<span data-ttu-id="8cf24-166"><a name="bk_new"> </a></span><span class="sxs-lookup"><span data-stu-id="8cf24-166"><a name="bk_new"> </a></span></span>

<span data-ttu-id="8cf24-167">Die folgenden Cmdlets wurden in Exchange 2013 eingeführt:</span><span class="sxs-lookup"><span data-stu-id="8cf24-167">The following cmdlets were introduced in Exchange 2013:</span></span>
  
- <span data-ttu-id="8cf24-168">**Get-ActiveSyncDeviceAutoblockThreshold**</span><span class="sxs-lookup"><span data-stu-id="8cf24-168">**Get-ActiveSyncDeviceAutoblockThreshold**</span></span>
    
- <span data-ttu-id="8cf24-169">**Gruppe-ActiveSyncDeviceAutoblockThreshold**</span><span class="sxs-lookup"><span data-stu-id="8cf24-169">**Set-ActiveSyncDeviceAutoblockThreshold**</span></span>
    
- <span data-ttu-id="8cf24-170">**Disable-App**</span><span class="sxs-lookup"><span data-stu-id="8cf24-170">**Disable-App**</span></span>
    
- <span data-ttu-id="8cf24-171">**Enable-App**</span><span class="sxs-lookup"><span data-stu-id="8cf24-171">**Enable-App**</span></span>
    
- <span data-ttu-id="8cf24-172">**Get-App**</span><span class="sxs-lookup"><span data-stu-id="8cf24-172">**Get-App**</span></span>
    
- <span data-ttu-id="8cf24-173">**New-App**</span><span class="sxs-lookup"><span data-stu-id="8cf24-173">**New-App**</span></span>
    
- <span data-ttu-id="8cf24-174">**Remove-App**</span><span class="sxs-lookup"><span data-stu-id="8cf24-174">**Remove-App**</span></span>
    
- <span data-ttu-id="8cf24-175">**Gruppe-App**</span><span class="sxs-lookup"><span data-stu-id="8cf24-175">**Set-App**</span></span>
    
- <span data-ttu-id="8cf24-176">**Get-AuthConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-176">**Get-AuthConfig**</span></span>
    
- <span data-ttu-id="8cf24-177">**Gruppe-AuthConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-177">**Set-AuthConfig**</span></span>
    
- <span data-ttu-id="8cf24-178">**Get-AuthServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-178">**Get-AuthServer**</span></span>
    
- <span data-ttu-id="8cf24-179">**New-AuthServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-179">**New-AuthServer**</span></span>
    
- <span data-ttu-id="8cf24-180">**Remove-AuthServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-180">**Remove-AuthServer**</span></span>
    
- <span data-ttu-id="8cf24-181">**Gruppe-AuthServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-181">**Set-AuthServer**</span></span>
    
- <span data-ttu-id="8cf24-182">**New-AvailabilityConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-182">**New-AvailabilityConfig**</span></span>
    
- <span data-ttu-id="8cf24-183">**Remove-AvailabilityConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-183">**Remove-AvailabilityConfig**</span></span>
    
- <span data-ttu-id="8cf24-184">**Get-CalendarDiagnosticAnalysis**</span><span class="sxs-lookup"><span data-stu-id="8cf24-184">**Get-CalendarDiagnosticAnalysis**</span></span>
    
- <span data-ttu-id="8cf24-185">**Get-ClassificationRuleCollection**</span><span class="sxs-lookup"><span data-stu-id="8cf24-185">**Get-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="8cf24-186">**New-ClassificationRuleCollection**</span><span class="sxs-lookup"><span data-stu-id="8cf24-186">**New-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="8cf24-187">**Remove-ClassificationRuleCollection**</span><span class="sxs-lookup"><span data-stu-id="8cf24-187">**Remove-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="8cf24-188">**Gruppe-ClassificationRuleCollection**</span><span class="sxs-lookup"><span data-stu-id="8cf24-188">**Set-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="8cf24-189">**Get-ConnectSubscription**</span><span class="sxs-lookup"><span data-stu-id="8cf24-189">**Get-ConnectSubscription**</span></span>
    
- <span data-ttu-id="8cf24-190">**New-ConnectSubscription**</span><span class="sxs-lookup"><span data-stu-id="8cf24-190">**New-ConnectSubscription**</span></span>
    
- <span data-ttu-id="8cf24-191">**Remove-ConnectSubscription**</span><span class="sxs-lookup"><span data-stu-id="8cf24-191">**Remove-ConnectSubscription**</span></span>
    
- <span data-ttu-id="8cf24-192">**Gruppe-ConnectSubscription**</span><span class="sxs-lookup"><span data-stu-id="8cf24-192">**Set-ConnectSubscription**</span></span>
    
- <span data-ttu-id="8cf24-193">**Get-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="8cf24-193">**Get-DataClassification**</span></span>
    
- <span data-ttu-id="8cf24-194">**Get-DataClassificationConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-194">**Get-DataClassificationConfig**</span></span>
    
- <span data-ttu-id="8cf24-195">**Get-DlpPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-195">**Get-DlpPolicy**</span></span>
    
- <span data-ttu-id="8cf24-196">**New-DlpPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-196">**New-DlpPolicy**</span></span>
    
- <span data-ttu-id="8cf24-197">**Remove-DlpPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-197">**Remove-DlpPolicy**</span></span>
    
- <span data-ttu-id="8cf24-198">**Gruppe-DlpPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-198">**Set-DlpPolicy**</span></span>
    
- <span data-ttu-id="8cf24-199">**Export-DlpPolicyCollection**</span><span class="sxs-lookup"><span data-stu-id="8cf24-199">**Export-DlpPolicyCollection**</span></span>
    
- <span data-ttu-id="8cf24-200">**Import-DlpPolicyCollection**</span><span class="sxs-lookup"><span data-stu-id="8cf24-200">**Import-DlpPolicyCollection**</span></span>
    
- <span data-ttu-id="8cf24-201">**Get-DlpPolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="8cf24-201">**Get-DlpPolicyTemplate**</span></span>
    
- <span data-ttu-id="8cf24-202">**Import-DlpPolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="8cf24-202">**Import-DlpPolicyTemplate**</span></span>
    
- <span data-ttu-id="8cf24-203">**Remove-DlpPolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="8cf24-203">**Remove-DlpPolicyTemplate**</span></span>
    
- <span data-ttu-id="8cf24-204">**Get-ExchangeServerAccessLicense**</span><span class="sxs-lookup"><span data-stu-id="8cf24-204">**Get-ExchangeServerAccessLicense**</span></span>
    
- <span data-ttu-id="8cf24-205">**Get-ExchangeServerAccessLicenseUser**</span><span class="sxs-lookup"><span data-stu-id="8cf24-205">**Get-ExchangeServerAccessLicenseUser**</span></span>
    
- <span data-ttu-id="8cf24-206">**Get-FfoMigrationReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-206">**Get-FfoMigrationReport**</span></span>
    
- <span data-ttu-id="8cf24-207">**Get-Frontend Transportservice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-207">**Get-FrontendTransportService**</span></span>
    
- <span data-ttu-id="8cf24-208">**Gruppe-Frontend Transportservice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-208">**Set-FrontendTransportService**</span></span>
    
- <span data-ttu-id="8cf24-209">**Add-GlobalMonitoringOverride**</span><span class="sxs-lookup"><span data-stu-id="8cf24-209">**Add-GlobalMonitoringOverride**</span></span>
    
- <span data-ttu-id="8cf24-210">**Get-GlobalMonitoringOverride**</span><span class="sxs-lookup"><span data-stu-id="8cf24-210">**Get-GlobalMonitoringOverride**</span></span>
    
- <span data-ttu-id="8cf24-211">**Remove-GlobalMonitoringOverride**</span><span class="sxs-lookup"><span data-stu-id="8cf24-211">**Remove-GlobalMonitoringOverride**</span></span>
    
- <span data-ttu-id="8cf24-212">**Get-GroupActivityReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-212">**Get-GroupActivityReport**</span></span>
    
- <span data-ttu-id="8cf24-213">**Get-HealthReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-213">**Get-HealthReport**</span></span>
    
- <span data-ttu-id="8cf24-214">**Get-HostedConnectionFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-214">**Get-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-215">**New-HostedConnectionFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-215">**New-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-216">**Remove-HostedConnectionFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-216">**Remove-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-217">**Gruppe-HostedConnectionFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-217">**Set-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-218">**Get-hostedcontentfilterpolicy dient zum**</span><span class="sxs-lookup"><span data-stu-id="8cf24-218">**Get-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-219">**New-hostedcontentfilterpolicy dient zum**</span><span class="sxs-lookup"><span data-stu-id="8cf24-219">**New-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-220">**Remove-hostedcontentfilterpolicy dient zum**</span><span class="sxs-lookup"><span data-stu-id="8cf24-220">**Remove-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-221">**Gruppe-hostedcontentfilterpolicy dient zum**</span><span class="sxs-lookup"><span data-stu-id="8cf24-221">**Set-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-222">**Get-HostedOutboundSpamFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-222">**Get-HostedOutboundSpamFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-223">**Gruppe-HostedOutboundSpamFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-223">**Set-HostedOutboundSpamFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-224">**Remove-HybridConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8cf24-224">**Remove-HybridConfiguration**</span></span>
    
- <span data-ttu-id="8cf24-225">**Get-HybridMailflow**</span><span class="sxs-lookup"><span data-stu-id="8cf24-225">**Get-HybridMailflow**</span></span>
    
- <span data-ttu-id="8cf24-226">**Gruppe-HybridMailflow**</span><span class="sxs-lookup"><span data-stu-id="8cf24-226">**Set-HybridMailflow**</span></span>
    
- <span data-ttu-id="8cf24-227">**Get-HybridMailflowDatacenterIPs**</span><span class="sxs-lookup"><span data-stu-id="8cf24-227">**Get-HybridMailflowDatacenterIPs**</span></span>
    
- <span data-ttu-id="8cf24-228">**Get-InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-228">**Get-InboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-229">**New-InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-229">**New-InboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-230">**Remove-InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-230">**Remove-InboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-231">**Gruppe-InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-231">**Set-InboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-232">**Get-MailboxActivityReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-232">**Get-MailboxActivityReport**</span></span>
    
- <span data-ttu-id="8cf24-233">**Disable-mailboxquarantine können**</span><span class="sxs-lookup"><span data-stu-id="8cf24-233">**Disable-MailboxQuarantine**</span></span>
    
- <span data-ttu-id="8cf24-234">**Enable-mailboxquarantine können**</span><span class="sxs-lookup"><span data-stu-id="8cf24-234">**Enable-MailboxQuarantine**</span></span>
    
- <span data-ttu-id="8cf24-235">**Get-Mailbox Transportservice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-235">**Get-MailboxTransportService**</span></span>
    
- <span data-ttu-id="8cf24-236">**Gruppe-Mailbox Transportservice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-236">**Set-MailboxTransportService**</span></span>
    
- <span data-ttu-id="8cf24-237">**Get-MailDetailDlpPolicyReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-237">**Get-MailDetailDlpPolicyReport**</span></span>
    
- <span data-ttu-id="8cf24-238">**Get-MailDetailMalwareReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-238">**Get-MailDetailMalwareReport**</span></span>
    
- <span data-ttu-id="8cf24-239">**Get-MailDetailReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-239">**Get-MailDetailReport**</span></span>
    
- <span data-ttu-id="8cf24-240">**Get-MailDetailSpamReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-240">**Get-MailDetailSpamReport**</span></span>
    
- <span data-ttu-id="8cf24-241">**Get-MailDetailTransportRuleReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-241">**Get-MailDetailTransportRuleReport**</span></span>
    
- <span data-ttu-id="8cf24-242">**Get-MailFilterListReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-242">**Get-MailFilterListReport**</span></span>
    
- <span data-ttu-id="8cf24-243">**Get-MailTrafficPolicyReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-243">**Get-MailTrafficPolicyReport**</span></span>
    
- <span data-ttu-id="8cf24-244">**Get-MailTrafficReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-244">**Get-MailTrafficReport**</span></span>
    
- <span data-ttu-id="8cf24-245">**Get-MailTrafficSummaryReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-245">**Get-MailTrafficSummaryReport**</span></span>
    
- <span data-ttu-id="8cf24-246">**Get-MailTrafficTopReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-246">**Get-MailTrafficTopReport**</span></span>
    
- <span data-ttu-id="8cf24-247">**Get-MalwareFilteringServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-247">**Get-MalwareFilteringServer**</span></span>
    
- <span data-ttu-id="8cf24-248">**Gruppe-MalwareFilteringServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-248">**Set-MalwareFilteringServer**</span></span>
    
- <span data-ttu-id="8cf24-249">**Get-MalwareFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-249">**Get-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-250">**New-MalwareFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-250">**New-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-251">**Remove-MalwareFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-251">**Remove-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-252">**Gruppe-MalwareFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-252">**Set-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="8cf24-253">**Get-MalwareFilterRecoveryItem**</span><span class="sxs-lookup"><span data-stu-id="8cf24-253">**Get-MalwareFilterRecoveryItem**</span></span>
    
- <span data-ttu-id="8cf24-254">**Remove-MalwareFilterRecoveryItem**</span><span class="sxs-lookup"><span data-stu-id="8cf24-254">**Remove-MalwareFilterRecoveryItem**</span></span>
    
- <span data-ttu-id="8cf24-255">**Resume-MalwareFilterRecoveryItem**</span><span class="sxs-lookup"><span data-stu-id="8cf24-255">**Resume-MalwareFilterRecoveryItem**</span></span>
    
- <span data-ttu-id="8cf24-256">**Send-MapiSubmitSystemProbe**</span><span class="sxs-lookup"><span data-stu-id="8cf24-256">**Send-MapiSubmitSystemProbe**</span></span>
    
- <span data-ttu-id="8cf24-257">**Redirect-Message**</span><span class="sxs-lookup"><span data-stu-id="8cf24-257">**Redirect-Message**</span></span>
    
- <span data-ttu-id="8cf24-258">**Get-MessageTrace**</span><span class="sxs-lookup"><span data-stu-id="8cf24-258">**Get-MessageTrace**</span></span>
    
- <span data-ttu-id="8cf24-259">**Get-MessageTraceDetail**</span><span class="sxs-lookup"><span data-stu-id="8cf24-259">**Get-MessageTraceDetail**</span></span>
    
- <span data-ttu-id="8cf24-260">**Complete-MigrationBatch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-260">**Complete-MigrationBatch**</span></span>
    
- <span data-ttu-id="8cf24-261">**Remove-MigrationBatch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-261">**Remove-MigrationBatch**</span></span>
    
- <span data-ttu-id="8cf24-262">**Get-MigrationConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-262">**Get-MigrationConfig**</span></span>
    
- <span data-ttu-id="8cf24-263">**Gruppe-MigrationConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-263">**Set-MigrationConfig**</span></span>
    
- <span data-ttu-id="8cf24-264">**Get-MigrationEndpoint**</span><span class="sxs-lookup"><span data-stu-id="8cf24-264">**Get-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="8cf24-265">**New-MigrationEndpoint**</span><span class="sxs-lookup"><span data-stu-id="8cf24-265">**New-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="8cf24-266">**Remove-MigrationEndpoint**</span><span class="sxs-lookup"><span data-stu-id="8cf24-266">**Remove-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="8cf24-267">**Gruppe-MigrationEndpoint**</span><span class="sxs-lookup"><span data-stu-id="8cf24-267">**Set-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="8cf24-268">**Get-MigrationStatistics**</span><span class="sxs-lookup"><span data-stu-id="8cf24-268">**Get-MigrationStatistics**</span></span>
    
- <span data-ttu-id="8cf24-269">**Get-MigrationUser**</span><span class="sxs-lookup"><span data-stu-id="8cf24-269">**Get-MigrationUser**</span></span>
    
- <span data-ttu-id="8cf24-270">**Remove-MigrationUser**</span><span class="sxs-lookup"><span data-stu-id="8cf24-270">**Remove-MigrationUser**</span></span>
    
- <span data-ttu-id="8cf24-271">**Get-MigrationUserStatistics**</span><span class="sxs-lookup"><span data-stu-id="8cf24-271">**Get-MigrationUserStatistics**</span></span>
    
- <span data-ttu-id="8cf24-272">**Clear-MobileDevice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-272">**Clear-MobileDevice**</span></span>
    
- <span data-ttu-id="8cf24-273">**Get-MobileDevice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-273">**Get-MobileDevice**</span></span>
    
- <span data-ttu-id="8cf24-274">**Remove-MobileDevice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-274">**Remove-MobileDevice**</span></span>
    
- <span data-ttu-id="8cf24-275">**Get-MobileDeviceMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-275">**Get-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="8cf24-276">**New-MobileDeviceMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-276">**New-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="8cf24-277">**Remove-MobileDeviceMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-277">**Remove-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="8cf24-278">**Gruppe-MobileDeviceMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-278">**Set-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="8cf24-279">**Get-MobileDeviceStatistics**</span><span class="sxs-lookup"><span data-stu-id="8cf24-279">**Get-MobileDeviceStatistics**</span></span>
    
- <span data-ttu-id="8cf24-280">**Get-MonitoringItemHelp**</span><span class="sxs-lookup"><span data-stu-id="8cf24-280">**Get-MonitoringItemHelp**</span></span>
    
- <span data-ttu-id="8cf24-281">**Get-MonitoringItemIdentity**</span><span class="sxs-lookup"><span data-stu-id="8cf24-281">**Get-MonitoringItemIdentity**</span></span>
    
- <span data-ttu-id="8cf24-282">**Invoke-MonitoringProbe**</span><span class="sxs-lookup"><span data-stu-id="8cf24-282">**Invoke-MonitoringProbe**</span></span>
    
- <span data-ttu-id="8cf24-283">**Get-Notification**</span><span class="sxs-lookup"><span data-stu-id="8cf24-283">**Get-Notification**</span></span>
    
- <span data-ttu-id="8cf24-284">**Festlegen-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="8cf24-284">**Set-Notification**</span></span>
    
- <span data-ttu-id="8cf24-285">**Test-OAuthConnectivity**</span><span class="sxs-lookup"><span data-stu-id="8cf24-285">**Test-OAuthConnectivity**</span></span>
    
- <span data-ttu-id="8cf24-286">**Get-OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="8cf24-286">**Get-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="8cf24-287">**New-OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="8cf24-287">**New-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="8cf24-288">**Remove-OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="8cf24-288">**Remove-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="8cf24-289">**Gruppe-OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="8cf24-289">**Set-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="8cf24-290">**Enable-OrganizationCustomization**</span><span class="sxs-lookup"><span data-stu-id="8cf24-290">**Enable-OrganizationCustomization**</span></span>
    
- <span data-ttu-id="8cf24-291">**Get-OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-291">**Get-OutboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-292">**New-OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-292">**New-OutboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-293">**Remove-OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-293">**Remove-OutboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-294">**Gruppe-OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="8cf24-294">**Set-OutboundConnector**</span></span>
    
- <span data-ttu-id="8cf24-295">**Get-PartnerApplication**</span><span class="sxs-lookup"><span data-stu-id="8cf24-295">**Get-PartnerApplication**</span></span>
    
- <span data-ttu-id="8cf24-296">**New-PartnerApplication**</span><span class="sxs-lookup"><span data-stu-id="8cf24-296">**New-PartnerApplication**</span></span>
    
- <span data-ttu-id="8cf24-297">**Remove-PartnerApplication**</span><span class="sxs-lookup"><span data-stu-id="8cf24-297">**Remove-PartnerApplication**</span></span>
    
- <span data-ttu-id="8cf24-298">**Gruppe-PartnerApplication**</span><span class="sxs-lookup"><span data-stu-id="8cf24-298">**Set-PartnerApplication**</span></span>
    
- <span data-ttu-id="8cf24-299">**Get-PendingFederatedDomain**</span><span class="sxs-lookup"><span data-stu-id="8cf24-299">**Get-PendingFederatedDomain**</span></span>
    
- <span data-ttu-id="8cf24-300">**Gruppe-PendingFederatedDomain**</span><span class="sxs-lookup"><span data-stu-id="8cf24-300">**Set-PendingFederatedDomain**</span></span>
    
- <span data-ttu-id="8cf24-301">**Get-PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-301">**Get-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="8cf24-302">**New-PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-302">**New-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="8cf24-303">**Remove-PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-303">**Remove-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="8cf24-304">**Gruppe-PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-304">**Set-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="8cf24-305">**Dump-ProvisioningCache**</span><span class="sxs-lookup"><span data-stu-id="8cf24-305">**Dump-ProvisioningCache**</span></span>
    
- <span data-ttu-id="8cf24-306">**Reset-ProvisioningCache**</span><span class="sxs-lookup"><span data-stu-id="8cf24-306">**Reset-ProvisioningCache**</span></span>
    
- <span data-ttu-id="8cf24-307">**Update-PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="8cf24-307">**Update-PublicFolderMailbox**</span></span>
    
- <span data-ttu-id="8cf24-308">**Get-PublicFolderMailboxDiagnostics**</span><span class="sxs-lookup"><span data-stu-id="8cf24-308">**Get-PublicFolderMailboxDiagnostics**</span></span>
    
- <span data-ttu-id="8cf24-309">**Get-PublicFolderMigrationRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-309">**Get-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="8cf24-310">**New-PublicFolderMigrationRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-310">**New-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="8cf24-311">**Remove-PublicFolderMigrationRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-311">**Remove-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="8cf24-312">**Resume-PublicFolderMigrationRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-312">**Resume-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="8cf24-313">**Gruppe-PublicFolderMigrationRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-313">**Set-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="8cf24-314">**Suspend-PublicFolderMigrationRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-314">**Suspend-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="8cf24-315">**Get-PublicFolderMigrationRequestStatistics**</span><span class="sxs-lookup"><span data-stu-id="8cf24-315">**Get-PublicFolderMigrationRequestStatistics**</span></span>
    
- <span data-ttu-id="8cf24-316">**Get-QuarantineMessage**</span><span class="sxs-lookup"><span data-stu-id="8cf24-316">**Get-QuarantineMessage**</span></span>
    
- <span data-ttu-id="8cf24-317">**Release-QuarantineMessage**</span><span class="sxs-lookup"><span data-stu-id="8cf24-317">**Release-QuarantineMessage**</span></span>
    
- <span data-ttu-id="8cf24-318">**Get-Queue Digest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-318">**Get-QueueDigest**</span></span>
    
- <span data-ttu-id="8cf24-319">**Get-ResourcePolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-319">**Get-ResourcePolicy**</span></span>
    
- <span data-ttu-id="8cf24-320">**New-ResourcePolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-320">**New-ResourcePolicy**</span></span>
    
- <span data-ttu-id="8cf24-321">**Remove-ResourcePolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-321">**Remove-ResourcePolicy**</span></span>
    
- <span data-ttu-id="8cf24-322">**Gruppe-ResourcePolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-322">**Set-ResourcePolicy**</span></span>
    
- <span data-ttu-id="8cf24-323">**Add-ResubmitRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-323">**Add-ResubmitRequest**</span></span>
    
- <span data-ttu-id="8cf24-324">**Get-ResubmitRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-324">**Get-ResubmitRequest**</span></span>
    
- <span data-ttu-id="8cf24-325">**Remove-ResubmitRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-325">**Remove-ResubmitRequest**</span></span>
    
- <span data-ttu-id="8cf24-326">**Gruppe-ResubmitRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-326">**Set-ResubmitRequest**</span></span>
    
- <span data-ttu-id="8cf24-327">**Get-ServerComponentState**</span><span class="sxs-lookup"><span data-stu-id="8cf24-327">**Get-ServerComponentState**</span></span>
    
- <span data-ttu-id="8cf24-328">**Gruppe-ServerComponentState**</span><span class="sxs-lookup"><span data-stu-id="8cf24-328">**Set-ServerComponentState**</span></span>
    
- <span data-ttu-id="8cf24-329">**Get-ServerHealth**</span><span class="sxs-lookup"><span data-stu-id="8cf24-329">**Get-ServerHealth**</span></span>
    
- <span data-ttu-id="8cf24-330">**Gruppe-Server Monitor**</span><span class="sxs-lookup"><span data-stu-id="8cf24-330">**Set-ServerMonitor**</span></span>
    
- <span data-ttu-id="8cf24-331">**Add-ServerMonitoringOverride**</span><span class="sxs-lookup"><span data-stu-id="8cf24-331">**Add-ServerMonitoringOverride**</span></span>
    
- <span data-ttu-id="8cf24-332">**Get-ServerMonitoringOverride**</span><span class="sxs-lookup"><span data-stu-id="8cf24-332">**Get-ServerMonitoringOverride**</span></span>
    
- <span data-ttu-id="8cf24-333">**Get-Site Mailbox**</span><span class="sxs-lookup"><span data-stu-id="8cf24-333">**Get-SiteMailbox**</span></span>
    
- <span data-ttu-id="8cf24-334">**New-Site Mailbox**</span><span class="sxs-lookup"><span data-stu-id="8cf24-334">**New-SiteMailbox**</span></span>
    
- <span data-ttu-id="8cf24-335">**Gruppe-Site Mailbox**</span><span class="sxs-lookup"><span data-stu-id="8cf24-335">**Set-SiteMailbox**</span></span>
    
- <span data-ttu-id="8cf24-336">**Test-Site Mailbox**</span><span class="sxs-lookup"><span data-stu-id="8cf24-336">**Test-SiteMailbox**</span></span>
    
- <span data-ttu-id="8cf24-337">**Update-Site Mailbox**</span><span class="sxs-lookup"><span data-stu-id="8cf24-337">**Update-SiteMailbox**</span></span>
    
- <span data-ttu-id="8cf24-338">**Get-SiteMailboxDiagnostics**</span><span class="sxs-lookup"><span data-stu-id="8cf24-338">**Get-SiteMailboxDiagnostics**</span></span>
    
- <span data-ttu-id="8cf24-339">**Get-SiteMailboxProvisioningPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-339">**Get-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="8cf24-340">**New-SiteMailboxProvisioningPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-340">**New-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="8cf24-341">**Remove-SiteMailboxProvisioningPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-341">**Remove-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="8cf24-342">**Set-SiteMailboxProvisioningPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-342">**Set-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="8cf24-343">**Undo-SoftDeletedMailbox**</span><span class="sxs-lookup"><span data-stu-id="8cf24-343">**Undo-SoftDeletedMailbox**</span></span>
    
- <span data-ttu-id="8cf24-344">**Get-StaleMailboxDetailReport**</span><span class="sxs-lookup"><span data-stu-id="8cf24-344">**Get-StaleMailboxDetailReport**</span></span>
    
- <span data-ttu-id="8cf24-345">**Get-Stal Emailbox Report**</span><span class="sxs-lookup"><span data-stu-id="8cf24-345">**Get-StaleMailboxReport**</span></span>
    
- <span data-ttu-id="8cf24-346">**Update-StoreMailboxState**</span><span class="sxs-lookup"><span data-stu-id="8cf24-346">**Update-StoreMailboxState**</span></span>
    
- <span data-ttu-id="8cf24-347">**New-SyncMailPublicFolder**</span><span class="sxs-lookup"><span data-stu-id="8cf24-347">**New-SyncMailPublicFolder**</span></span>
    
- <span data-ttu-id="8cf24-348">**Get-Transportservice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-348">**Get-TransportService**</span></span>
    
- <span data-ttu-id="8cf24-349">**Gruppe-Transportservice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-349">**Set-TransportService**</span></span>
    
- <span data-ttu-id="8cf24-350">**Disable-UMCallAnsweringRule**</span><span class="sxs-lookup"><span data-stu-id="8cf24-350">**Disable-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="8cf24-351">**Enable-UMCallAnsweringRule**</span><span class="sxs-lookup"><span data-stu-id="8cf24-351">**Enable-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="8cf24-352">**Get-UMCallAnsweringRule**</span><span class="sxs-lookup"><span data-stu-id="8cf24-352">**Get-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="8cf24-353">**New-UMCallAnsweringRule**</span><span class="sxs-lookup"><span data-stu-id="8cf24-353">**New-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="8cf24-354">**Remove-UMCallAnsweringRule**</span><span class="sxs-lookup"><span data-stu-id="8cf24-354">**Remove-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="8cf24-355">**Gruppe-UMCallAnsweringRule**</span><span class="sxs-lookup"><span data-stu-id="8cf24-355">**Set-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="8cf24-356">**Get-UMCallRouterSettings**</span><span class="sxs-lookup"><span data-stu-id="8cf24-356">**Get-UMCallRouterSettings**</span></span>
    
- <span data-ttu-id="8cf24-357">**Gruppe-UMCallRouterSettings**</span><span class="sxs-lookup"><span data-stu-id="8cf24-357">**Set-UMCallRouterSettings**</span></span>
    
- <span data-ttu-id="8cf24-358">**Disable-UMService**</span><span class="sxs-lookup"><span data-stu-id="8cf24-358">**Disable-UMService**</span></span>
    
- <span data-ttu-id="8cf24-359">**Enable-UMService**</span><span class="sxs-lookup"><span data-stu-id="8cf24-359">**Enable-UMService**</span></span>
    
- <span data-ttu-id="8cf24-360">**Get-UMService**</span><span class="sxs-lookup"><span data-stu-id="8cf24-360">**Get-UMService**</span></span>
    
- <span data-ttu-id="8cf24-361">**Set-UMService**</span><span class="sxs-lookup"><span data-stu-id="8cf24-361">**Set-UMService**</span></span>
    
- <span data-ttu-id="8cf24-362">**Get-UserPhoto**</span><span class="sxs-lookup"><span data-stu-id="8cf24-362">**Get-UserPhoto**</span></span>
    
- <span data-ttu-id="8cf24-363">**Remove-UserPhoto**</span><span class="sxs-lookup"><span data-stu-id="8cf24-363">**Remove-UserPhoto**</span></span>
    
- <span data-ttu-id="8cf24-364">**Set-UserPhoto**</span><span class="sxs-lookup"><span data-stu-id="8cf24-364">**Set-UserPhoto**</span></span>
    
- <span data-ttu-id="8cf24-365">**Get-WorkloadManagementPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-365">**Get-WorkloadManagementPolicy**</span></span>
    
- <span data-ttu-id="8cf24-366">**New-WorkloadManagementPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-366">**New-WorkloadManagementPolicy**</span></span>
    
- <span data-ttu-id="8cf24-367">**Remove-WorkloadManagementPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-367">**Remove-WorkloadManagementPolicy**</span></span>
    
- <span data-ttu-id="8cf24-368">**Get-WorkloadPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-368">**Get-WorkloadPolicy**</span></span>
    
- <span data-ttu-id="8cf24-369">**New-WorkloadPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-369">**New-WorkloadPolicy**</span></span>
    
- <span data-ttu-id="8cf24-370">**Remove-WorkloadPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-370">**Remove-WorkloadPolicy**</span></span>
    
- <span data-ttu-id="8cf24-371">**Gruppe-WorkloadPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-371">**Set-WorkloadPolicy**</span></span>
    
### <a name="modified-cmdlets"></a><span data-ttu-id="8cf24-372">Geänderte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cf24-372">Modified cmdlets</span></span>
<span data-ttu-id="8cf24-373"><a name="bk_update"> </a></span><span class="sxs-lookup"><span data-stu-id="8cf24-373"><a name="bk_update"> </a></span></span>

<span data-ttu-id="8cf24-374">Die Eingabe-oder Ausgabetypen für die folgenden Cmdlets wurden in Exchange 2013 geändert:</span><span class="sxs-lookup"><span data-stu-id="8cf24-374">The input or output types for following cmdlets were modified in Exchange 2013:</span></span>
  
- <span data-ttu-id="8cf24-375">**Clear-ActiveSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-375">**Clear-ActiveSyncDevice**</span></span>
    
- <span data-ttu-id="8cf24-376">**Remove-ActiveSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="8cf24-376">**Remove-ActiveSyncDevice**</span></span>
    
- <span data-ttu-id="8cf24-377">**Get-ActiveSyncMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-377">**Get-ActiveSyncMailboxPolicy**</span></span>
    
- <span data-ttu-id="8cf24-378">**New-ActiveSyncMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-378">**New-ActiveSyncMailboxPolicy**</span></span>
    
- <span data-ttu-id="8cf24-379">**New-ActiveSyncVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="8cf24-379">**New-ActiveSyncVirtualDirectory**</span></span>
    
- <span data-ttu-id="8cf24-380">**New-AutodiscoverVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="8cf24-380">**New-AutodiscoverVirtualDirectory**</span></span>
    
- <span data-ttu-id="8cf24-381">**Gruppe-AvailabilityConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-381">**Set-AvailabilityConfig**</span></span>
    
- <span data-ttu-id="8cf24-382">**Enable-ExchangeCertificate**</span><span class="sxs-lookup"><span data-stu-id="8cf24-382">**Enable-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="8cf24-383">**Export-ExchangeCertificate**</span><span class="sxs-lookup"><span data-stu-id="8cf24-383">**Export-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="8cf24-384">**Import-ExchangeCertificate**</span><span class="sxs-lookup"><span data-stu-id="8cf24-384">**Import-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="8cf24-385">**Remove-ExchangeCertificate**</span><span class="sxs-lookup"><span data-stu-id="8cf24-385">**Remove-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="8cf24-386">**Get-FailedContentIndexDocuments**</span><span class="sxs-lookup"><span data-stu-id="8cf24-386">**Get-FailedContentIndexDocuments**</span></span>
    
- <span data-ttu-id="8cf24-387">**Get-FederationInformation**</span><span class="sxs-lookup"><span data-stu-id="8cf24-387">**Get-FederationInformation**</span></span>
    
- <span data-ttu-id="8cf24-388">**New-HybridConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8cf24-388">**New-HybridConfiguration**</span></span>
    
- <span data-ttu-id="8cf24-389">**Gruppe-HybridConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8cf24-389">**Set-HybridConfiguration**</span></span>
    
- <span data-ttu-id="8cf24-390">**New-Mailbox**</span><span class="sxs-lookup"><span data-stu-id="8cf24-390">**New-Mailbox**</span></span>
    
- <span data-ttu-id="8cf24-391">**Resume-MailboxDatabaseCopy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-391">**Resume-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="8cf24-392">**Gruppe-MailboxDatabaseCopy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-392">**Set-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="8cf24-393">**Suspend-MailboxDatabaseCopy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-393">**Suspend-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="8cf24-394">**Update-MailboxDatabaseCopy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-394">**Update-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="8cf24-395">**Get-MailboxExportRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-395">**Get-MailboxExportRequest**</span></span>
    
- <span data-ttu-id="8cf24-396">**Gruppe-MailboxExportRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-396">**Set-MailboxExportRequest**</span></span>
    
- <span data-ttu-id="8cf24-397">**Add-MailboxFolderPermission**</span><span class="sxs-lookup"><span data-stu-id="8cf24-397">**Add-MailboxFolderPermission**</span></span>
    
- <span data-ttu-id="8cf24-398">**Remove-MailboxFolderPermission**</span><span class="sxs-lookup"><span data-stu-id="8cf24-398">**Remove-MailboxFolderPermission**</span></span>
    
- <span data-ttu-id="8cf24-399">**Gruppe-MailboxFolderPermission**</span><span class="sxs-lookup"><span data-stu-id="8cf24-399">**Set-MailboxFolderPermission**</span></span>
    
- <span data-ttu-id="8cf24-400">**Get-MailboxImportRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-400">**Get-MailboxImportRequest**</span></span>
    
- <span data-ttu-id="8cf24-401">**Gruppe-MailboxImportRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-401">**Set-MailboxImportRequest**</span></span>
    
- <span data-ttu-id="8cf24-402">**Get-MailboxRestoreRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-402">**Get-MailboxRestoreRequest**</span></span>
    
- <span data-ttu-id="8cf24-403">**Gruppe-MailboxRestoreRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-403">**Set-MailboxRestoreRequest**</span></span>
    
- <span data-ttu-id="8cf24-404">**Get-MailboxSearch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-404">**Get-MailboxSearch**</span></span>
    
- <span data-ttu-id="8cf24-405">**Remove-MailboxSearch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-405">**Remove-MailboxSearch**</span></span>
    
- <span data-ttu-id="8cf24-406">**Gruppe-MailboxSearch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-406">**Set-MailboxSearch**</span></span>
    
- <span data-ttu-id="8cf24-407">**Start-MailboxSearch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-407">**Start-MailboxSearch**</span></span>
    
- <span data-ttu-id="8cf24-408">**Stop-MailboxSearch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-408">**Stop-MailboxSearch**</span></span>
    
- <span data-ttu-id="8cf24-409">**Deaktivieren-MailPublicFolder**</span><span class="sxs-lookup"><span data-stu-id="8cf24-409">**Disable-MailPublicFolder**</span></span>
    
- <span data-ttu-id="8cf24-410">**Get-MailPublicFolder**</span><span class="sxs-lookup"><span data-stu-id="8cf24-410">**Get-MailPublicFolder**</span></span>
    
- <span data-ttu-id="8cf24-411">**Set-MailPublicFolder**</span><span class="sxs-lookup"><span data-stu-id="8cf24-411">**Set-MailPublicFolder**</span></span>
    
- <span data-ttu-id="8cf24-412">**Get-MigrationBatch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-412">**Get-MigrationBatch**</span></span>
    
- <span data-ttu-id="8cf24-413">**New-MigrationBatch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-413">**New-MigrationBatch**</span></span>
    
- <span data-ttu-id="8cf24-414">**Gruppe-MigrationBatch**</span><span class="sxs-lookup"><span data-stu-id="8cf24-414">**Set-MigrationBatch**</span></span>
    
- <span data-ttu-id="8cf24-415">**Test-MigrationServerAvailability**</span><span class="sxs-lookup"><span data-stu-id="8cf24-415">**Test-MigrationServerAvailability**</span></span>
    
- <span data-ttu-id="8cf24-416">**Get-MoveRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-416">**Get-MoveRequest**</span></span>
    
- <span data-ttu-id="8cf24-417">**New-OfflineAddressBook**</span><span class="sxs-lookup"><span data-stu-id="8cf24-417">**New-OfflineAddressBook**</span></span>
    
- <span data-ttu-id="8cf24-418">**Get-OrganizationConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-418">**Get-OrganizationConfig**</span></span>
    
- <span data-ttu-id="8cf24-419">**Set-OrganizationConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-419">**Set-OrganizationConfig**</span></span>
    
- <span data-ttu-id="8cf24-420">**Test-OutlookConnectivity**</span><span class="sxs-lookup"><span data-stu-id="8cf24-420">**Test-OutlookConnectivity**</span></span>
    
- <span data-ttu-id="8cf24-421">**Test-OutlookWeb Services**</span><span class="sxs-lookup"><span data-stu-id="8cf24-421">**Test-OutlookWebServices**</span></span>
    
- <span data-ttu-id="8cf24-422">**Get-OwaMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-422">**Get-OwaMailboxPolicy**</span></span>
    
- <span data-ttu-id="8cf24-423">**New-OwaVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="8cf24-423">**New-OwaVirtualDirectory**</span></span>
    
- <span data-ttu-id="8cf24-424">**New-PowerShellVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="8cf24-424">**New-PowerShellVirtualDirectory**</span></span>
    
- <span data-ttu-id="8cf24-425">**Get-PublicFolder**</span><span class="sxs-lookup"><span data-stu-id="8cf24-425">**Get-PublicFolder**</span></span>
    
- <span data-ttu-id="8cf24-426">**New-PublicFolder**</span><span class="sxs-lookup"><span data-stu-id="8cf24-426">**New-PublicFolder**</span></span>
    
- <span data-ttu-id="8cf24-427">**Gruppe-PublicFolder**</span><span class="sxs-lookup"><span data-stu-id="8cf24-427">**Set-PublicFolder**</span></span>
    
- <span data-ttu-id="8cf24-428">**Add-PublicFolderClientPermission**</span><span class="sxs-lookup"><span data-stu-id="8cf24-428">**Add-PublicFolderClientPermission**</span></span>
    
- <span data-ttu-id="8cf24-429">**Get-PublicFolderClientPermission**</span><span class="sxs-lookup"><span data-stu-id="8cf24-429">**Get-PublicFolderClientPermission**</span></span>
    
- <span data-ttu-id="8cf24-430">**Remove-PublicFolderClientPermission**</span><span class="sxs-lookup"><span data-stu-id="8cf24-430">**Remove-PublicFolderClientPermission**</span></span>
    
- <span data-ttu-id="8cf24-431">**Get-PublicFolderItemStatistics**</span><span class="sxs-lookup"><span data-stu-id="8cf24-431">**Get-PublicFolderItemStatistics**</span></span>
    
- <span data-ttu-id="8cf24-432">**Get-PublicFolderStatistics**</span><span class="sxs-lookup"><span data-stu-id="8cf24-432">**Get-PublicFolderStatistics**</span></span>
    
- <span data-ttu-id="8cf24-433">**Get-Recipient**</span><span class="sxs-lookup"><span data-stu-id="8cf24-433">**Get-Recipient**</span></span>
    
- <span data-ttu-id="8cf24-434">**Gruppe-ResourceConfig**</span><span class="sxs-lookup"><span data-stu-id="8cf24-434">**Set-ResourceConfig**</span></span>
    
- <span data-ttu-id="8cf24-435">**Test-WebServicesConnectivity**</span><span class="sxs-lookup"><span data-stu-id="8cf24-435">**Test-WebServicesConnectivity**</span></span>
    
- <span data-ttu-id="8cf24-436">**New-WebServicesVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="8cf24-436">**New-WebServicesVirtualDirectory**</span></span>
    
### <a name="removed-cmdlets"></a><span data-ttu-id="8cf24-437">Entfernte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cf24-437">Removed cmdlets</span></span>
<span data-ttu-id="8cf24-438"><a name="bk_removed"> </a></span><span class="sxs-lookup"><span data-stu-id="8cf24-438"><a name="bk_removed"> </a></span></span>

<span data-ttu-id="8cf24-439">Die folgenden Cmdlets wurden aus Exchange 2013 entfernt:</span><span class="sxs-lookup"><span data-stu-id="8cf24-439">The following cmdlets were removed from Exchange 2013:</span></span>
  
- <span data-ttu-id="8cf24-440">**Update-FileDistributionService**</span><span class="sxs-lookup"><span data-stu-id="8cf24-440">**Update-FileDistributionService**</span></span>
    
- <span data-ttu-id="8cf24-441">**Restore – Postfach**</span><span class="sxs-lookup"><span data-stu-id="8cf24-441">**Restore-Mailbox**</span></span>
    
- <span data-ttu-id="8cf24-442">**Clean-MailboxDatabase**</span><span class="sxs-lookup"><span data-stu-id="8cf24-442">**Clean-MailboxDatabase**</span></span>
    
- <span data-ttu-id="8cf24-443">**Vollständige Migration**</span><span class="sxs-lookup"><span data-stu-id="8cf24-443">**Complete-Migration**</span></span>
    
- <span data-ttu-id="8cf24-444">**Get-MigrationStatus**</span><span class="sxs-lookup"><span data-stu-id="8cf24-444">**Get-MigrationStatus**</span></span>
    
- <span data-ttu-id="8cf24-445">**Update-PublicFolder**</span><span class="sxs-lookup"><span data-stu-id="8cf24-445">**Update-PublicFolder**</span></span>
    
- <span data-ttu-id="8cf24-446">**Add-PublicFolderAdministrativePermission**</span><span class="sxs-lookup"><span data-stu-id="8cf24-446">**Add-PublicFolderAdministrativePermission**</span></span>
    
- <span data-ttu-id="8cf24-447">**Get-PublicFolderAdministrativePermission**</span><span class="sxs-lookup"><span data-stu-id="8cf24-447">**Get-PublicFolderAdministrativePermission**</span></span>
    
- <span data-ttu-id="8cf24-448">**Remove-PublicFolderAdministrativePermission**</span><span class="sxs-lookup"><span data-stu-id="8cf24-448">**Remove-PublicFolderAdministrativePermission**</span></span>
    
- <span data-ttu-id="8cf24-449">**New-PublicFolderDatabase**</span><span class="sxs-lookup"><span data-stu-id="8cf24-449">**New-PublicFolderDatabase**</span></span>
    
- <span data-ttu-id="8cf24-450">**Remove-PublicFolderDatabase**</span><span class="sxs-lookup"><span data-stu-id="8cf24-450">**Remove-PublicFolderDatabase**</span></span>
    
- <span data-ttu-id="8cf24-451">**Gruppe-PublicFolderDatabase**</span><span class="sxs-lookup"><span data-stu-id="8cf24-451">**Set-PublicFolderDatabase**</span></span>
    
- <span data-ttu-id="8cf24-452">**New-PublicFolderDatabaseRepairRequest**</span><span class="sxs-lookup"><span data-stu-id="8cf24-452">**New-PublicFolderDatabaseRepairRequest**</span></span>
    
- <span data-ttu-id="8cf24-453">**Update-PublicFolderHierarchy**</span><span class="sxs-lookup"><span data-stu-id="8cf24-453">**Update-PublicFolderHierarchy**</span></span>
    
- <span data-ttu-id="8cf24-454">**Resume-PublicFolderReplication**</span><span class="sxs-lookup"><span data-stu-id="8cf24-454">**Resume-PublicFolderReplication**</span></span>
    
- <span data-ttu-id="8cf24-455">**Suspend-PublicFolderReplication**</span><span class="sxs-lookup"><span data-stu-id="8cf24-455">**Suspend-PublicFolderReplication**</span></span>
    
- <span data-ttu-id="8cf24-456">**Start-RetentionAutoTagLearning**</span><span class="sxs-lookup"><span data-stu-id="8cf24-456">**Start-RetentionAutoTagLearning**</span></span>
    
- <span data-ttu-id="8cf24-457">**Test-SystemHealth**</span><span class="sxs-lookup"><span data-stu-id="8cf24-457">**Test-SystemHealth**</span></span>
    
- <span data-ttu-id="8cf24-458">**Disable-UMServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-458">**Disable-UMServer**</span></span>
    
- <span data-ttu-id="8cf24-459">**Enable-UMServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-459">**Enable-UMServer**</span></span>
    
- <span data-ttu-id="8cf24-460">**Get-UMServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-460">**Get-UMServer**</span></span>
    
- <span data-ttu-id="8cf24-461">**Gruppe-UMServer**</span><span class="sxs-lookup"><span data-stu-id="8cf24-461">**Set-UMServer**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8cf24-462">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cf24-462">See also</span></span>

- [<span data-ttu-id="8cf24-463">Eingabe- und Ausgabetypen für Cmdlets der Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="8cf24-463">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)    
- [<span data-ttu-id="8cf24-464">Abrufen einer Liste von e-Mail-Benutzern mithilfe der Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="8cf24-464">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)    
- [<span data-ttu-id="8cf24-465">Exchange 2013 cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cf24-465">Exchange 2013 cmdlets</span></span>](https://technet.microsoft.com/library/bb124413%28v=exchg.150%29.aspx)
    

