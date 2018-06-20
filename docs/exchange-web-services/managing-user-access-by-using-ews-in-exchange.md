---
title: Verwalten des Benutzerzugriffs in Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: Hier finden Sie Informationen zu die Optionen für die Verwaltung von Benutzerkonten den Zugriff auf Ihren Exchange-Server.
ms.openlocfilehash: d93f521f08f93b44b4ecc1f258b03ed24ebdd3dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757031"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a><span data-ttu-id="0211e-103">Verwalten des Benutzerzugriffs in Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="0211e-103">Managing user access by using EWS in Exchange</span></span>

<span data-ttu-id="0211e-104">Hier finden Sie Informationen zu die Optionen für die Verwaltung von Benutzerkonten den Zugriff auf Ihren Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="0211e-104">Find out what your options are for managing user account access to your Exchange server.</span></span>
  
<span data-ttu-id="0211e-105">Exchange-Webdienste (EWS) und die EWS managed API bieten eine begrenzte Anzahl von Operationen, die Sie zum Verwalten von Konten in Exchange Online, Exchange Online als Teil von Office 365 oder eine Version von Exchange, beginnend mit Exchange 2013 verwenden können.</span><span class="sxs-lookup"><span data-stu-id="0211e-105">Exchange Web Services (EWS) and the EWS managed API provide a limited number of operations that you can use to manage accounts on Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="0211e-106">Sie können die Vorgänge in der folgenden Abbildung dargestellt, Stellvertretungen verwalten und Festlegen von Zugriffsberechtigungen für Ordner für andere Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="0211e-106">You can use the operations shown in the following figure to manage delegates and to set folder access permissions for other accounts.</span></span> 
  
<span data-ttu-id="0211e-107">**EWS-Vorgänge für den Delegaten und Ordner**</span><span class="sxs-lookup"><span data-stu-id="0211e-107">**EWS operations for delegate and folder access**</span></span>

![EWS-Benutzerverwaltungsoptionen.](media/Exchange_ManagingUserAccess_1.png)
  
<span data-ttu-id="0211e-109">Wenn die Anwendung zusätzliche Kontrolle über die Konten auf einem Exchange-Server benötigt, können Sie die Exchange-Verwaltungsshell-Cmdlets zum Verwalten von Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="0211e-109">If your application needs additional control over the accounts on an Exchange server, you can use Exchange Management Shell cmdlets to manage the accounts.</span></span> <span data-ttu-id="0211e-110">Sie können die Exchange-Verwaltungsshell-Cmdlets aufrufen, indem Sie einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="0211e-110">You can call the Exchange Management Shell cmdlets by doing one of the following:</span></span>
  
- <span data-ttu-id="0211e-111">Schreiben einer Anwendung mit c# oder Visual Basic, die die Exchange-Verwaltungsshell-Cmdlets aufruft.</span><span class="sxs-lookup"><span data-stu-id="0211e-111">Writing an application using C# or Visual Basic that calls the Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="0211e-112">Betrachten Sie im Beispielcode in der [Exchange Management Shell API-Dokumentation](../management/exchange-management-shell.md) erfahren, wie ein Cmdlet aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0211e-112">You can look at the sample code in the [Exchange Management Shell API documentation](../management/exchange-management-shell.md) to learn how to call a cmdlet.</span></span> 
    
- <span data-ttu-id="0211e-113">Verwenden von Windows PowerShell und Windows PowerShell-Skripts zum Aufrufen der Exchange-Verwaltungsshell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0211e-113">Using Windows PowerShell and Windows PowerShell scripts to call Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="0211e-114">Finden Sie eine vollständige Liste mit den [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), zusammen mit Beispielen, die zeigen, deren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="0211e-114">You can find a complete list of the [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), along with examples that show how to use them.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0211e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0211e-115">See also</span></span>

- [<span data-ttu-id="0211e-116">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="0211e-116">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)   
- [<span data-ttu-id="0211e-117">Exchange 2013-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0211e-117">Exchange 2013 Cmdlets</span></span>](https://docs.microsoft.com/en-us/powershell/exchange/?view=exchange-ps)  
    

