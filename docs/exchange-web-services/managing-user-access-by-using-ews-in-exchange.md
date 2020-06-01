---
title: Verwalten des Benutzerzugriffs in Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: Erfahren Sie, welche Optionen Sie für die Verwaltung des Zugriffs auf Ihren Exchange-Server für den Benutzerkonto haben.
ms.openlocfilehash: 476292d4db206f22cd84134ce2b46957e9fe85fc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456244"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a><span data-ttu-id="6cc9b-103">Verwalten des Benutzerzugriffs in Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="6cc9b-103">Managing user access by using EWS in Exchange</span></span>

<span data-ttu-id="6cc9b-104">Erfahren Sie, welche Optionen Sie für die Verwaltung des Zugriffs auf Ihren Exchange-Server für den Benutzerkonto haben.</span><span class="sxs-lookup"><span data-stu-id="6cc9b-104">Find out what your options are for managing user account access to your Exchange server.</span></span>
  
<span data-ttu-id="6cc9b-105">Exchange-Webdienste und die verwaltete EWS-API bieten eine beschränkte Anzahl von Vorgängen, die Sie zum Verwalten von Konten auf Exchange Online, Exchange Online im Rahmen von Office 365 oder einer Exchange-Version, die mit Exchange 2013 beginnt, verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6cc9b-105">Exchange Web Services (EWS) and the EWS managed API provide a limited number of operations that you can use to manage accounts on Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="6cc9b-106">Sie können die in der folgenden Abbildung gezeigten Vorgänge verwenden, um Stellvertretungen zu verwalten und Ordnerzugriffsberechtigungen für andere Konten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6cc9b-106">You can use the operations shown in the following figure to manage delegates and to set folder access permissions for other accounts.</span></span> 
  
<span data-ttu-id="6cc9b-107">**EWS-Vorgänge für Stellvertretungs-und Ordner Zugriff**</span><span class="sxs-lookup"><span data-stu-id="6cc9b-107">**EWS operations for delegate and folder access**</span></span>

![EWS-Benutzerverwaltungsoptionen.](media/Exchange_ManagingUserAccess_1.png)
  
<span data-ttu-id="6cc9b-109">Wenn Ihre Anwendung zusätzliche Kontrolle über die Konten auf einem Exchange-Server benötigt, können Sie Exchange-Verwaltungsshell-Cmdlets zum Verwalten der Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="6cc9b-109">If your application needs additional control over the accounts on an Exchange server, you can use Exchange Management Shell cmdlets to manage the accounts.</span></span> <span data-ttu-id="6cc9b-110">Sie können die Exchange-Verwaltungsshell-Cmdlets aufrufen, indem Sie einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="6cc9b-110">You can call the Exchange Management Shell cmdlets by doing one of the following:</span></span>
  
- <span data-ttu-id="6cc9b-111">Schreiben einer Anwendung mithilfe von C# oder Visual Basic, die die Exchange-Verwaltungsshell-Cmdlets aufruft.</span><span class="sxs-lookup"><span data-stu-id="6cc9b-111">Writing an application using C# or Visual Basic that calls the Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="6cc9b-112">Sie können sich den Beispielcode in der [Exchange-Verwaltungsshell-API-Dokumentation](../management/exchange-management-shell.md) ansehen, um zu erfahren, wie Sie ein Cmdlet aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6cc9b-112">You can look at the sample code in the [Exchange Management Shell API documentation](../management/exchange-management-shell.md) to learn how to call a cmdlet.</span></span> 
    
- <span data-ttu-id="6cc9b-113">Verwenden von Windows PowerShell-und Windows PowerShell-Skripts zum Aufrufen von Exchange-Verwaltungsshell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6cc9b-113">Using Windows PowerShell and Windows PowerShell scripts to call Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="6cc9b-114">Eine vollständige Liste der [Exchange Server PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)finden Sie zusammen mit Beispielen, die zeigen, wie Sie verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6cc9b-114">You can find a complete list of the [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), along with examples that show how to use them.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6cc9b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cc9b-115">See also</span></span>

- [<span data-ttu-id="6cc9b-116">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="6cc9b-116">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)   
- [<span data-ttu-id="6cc9b-117">Exchange 2013-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6cc9b-117">Exchange 2013 Cmdlets</span></span>](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)  
    

