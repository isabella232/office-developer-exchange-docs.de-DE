---
title: Unified Messaging-Webdienstvorgänge für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Unified
api_type:
- schema
ms.assetid: d92455bd-24e8-4255-9f93-2bdeff00d42d
description: Hier finden Sie Referenzinformationen zu den Unified Messaging-Webdienstvorgängen in Exchange.
ms.openlocfilehash: b13ca2fbc44846db0bc98b3961916ba5d0872310
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529714"
---
# <a name="unified-messaging-web-service-operations-for-exchange"></a><span data-ttu-id="5947b-103">Unified Messaging-Webdienstvorgänge für Exchange</span><span class="sxs-lookup"><span data-stu-id="5947b-103">Unified Messaging web service operations for Exchange</span></span>

<span data-ttu-id="5947b-104">Hier finden Sie Referenzinformationen zu den Unified Messaging-Webdienstvorgängen in Exchange.</span><span class="sxs-lookup"><span data-stu-id="5947b-104">Find reference information for the Unified Messaging web service operations in Exchange.</span></span>
  
<span data-ttu-id="5947b-105">Der Unified Messaging-Webdienst stellt zahlreiche Vorgänge bereit, mit denen Clientanwendungen Unified Messaging-Eigenschaften lesen und ändern, Voicemail-Nachrichten wiedergeben, Begrüßungen aufzeichnen und Postfachelemente über Telefongeräte diktieren können.</span><span class="sxs-lookup"><span data-stu-id="5947b-105">The Unified Messaging web service provides many operations that enable client applications to read and change Unified Messaging properties, play voice mail messages, record greetings, and dictate mailbox items over telephony devices.</span></span> <span data-ttu-id="5947b-106">Die Artikel in diesem Abschnitt enthalten Informationen zur Gesamtstruktur der Anforderungs-und Antwortnachrichten für die Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="5947b-106">The articles in this section provide information about the overall structure of the request and response messages for the operations.</span></span> <span data-ttu-id="5947b-107">Diese Artikel enthalten Beispiele, die allgemeine nachrichtenstrukturen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5947b-107">These articles provide examples that show common message structures.</span></span> <span data-ttu-id="5947b-108">Anhand dieser Beispiele erfahren Sie, was Sie mit einer Unified Messaging-Webdienstanforderung tun können.</span><span class="sxs-lookup"><span data-stu-id="5947b-108">You can use these examples to learn about what you can do with a Unified Messaging web service request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5947b-109">Für Exchange-Versionen, die mit Exchange 2010 beginnen, wird empfohlen, dass Sie die Unified Messaging-Vorgänge verwenden, die in [Exchange-Webdienste](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) anstelle des Unified Messaging-Webdiensts verfügbar sind, aus den folgenden Gründen:</span><span class="sxs-lookup"><span data-stu-id="5947b-109">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the Unified Messaging web service, for the following reasons:</span></span> 
> - <span data-ttu-id="5947b-110">Die EWS-basierten Unified Messaging-Funktionen haben in der verwaltete EWS-API eine erstklassige Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="5947b-110">The EWS-based Unified Messaging features have first-class support in the EWS Managed API.</span></span> 
> - <span data-ttu-id="5947b-111">In Exchange-Versionen, die mit Exchange 2010 beginnen, werden dem EWS neue Unified Messaging-Features hinzugefügt, jedoch nicht dem Unified Messaging-Webdienst.</span><span class="sxs-lookup"><span data-stu-id="5947b-111">In versions of Exchange starting with Exchange 2010, new Unified Messaging features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="5947b-112">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="5947b-112">In this section</span></span>
<span data-ttu-id="5947b-113"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="5947b-113"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="5947b-114">Trennungsvorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-114">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)    
- [<span data-ttu-id="5947b-115">GetCallInfo-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-115">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)   
- [<span data-ttu-id="5947b-116">GetUMProperties-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-116">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)   
- [<span data-ttu-id="5947b-117">IsUMEnabled-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-117">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)   
- [<span data-ttu-id="5947b-118">PlayOnPhone-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-118">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)   
- [<span data-ttu-id="5947b-119">PlayOnPhoneGreeting-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-119">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)   
- [<span data-ttu-id="5947b-120">ResetPIN-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-120">ResetPIN operation (UM web service)</span></span>](resetpin-operation-um-web-service.md)   
- [<span data-ttu-id="5947b-121">SetMissedCallNotificationEnabled-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-121">SetMissedCallNotificationEnabled operation (UM web service)</span></span>](setmissedcallnotificationenabled-operation-um-web-service.md)  
- [<span data-ttu-id="5947b-122">SetOofStatus-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-122">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)    
- [<span data-ttu-id="5947b-123">SetPlayOnPhoneDialString-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-123">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)   
- [<span data-ttu-id="5947b-124">SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5947b-124">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
    
## <a name="see-also"></a><span data-ttu-id="5947b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5947b-125">See also</span></span>

- [<span data-ttu-id="5947b-126">Unified Messaging-Webdienst Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="5947b-126">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
- [<span data-ttu-id="5947b-127">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="5947b-127">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="5947b-128">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="5947b-128">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

