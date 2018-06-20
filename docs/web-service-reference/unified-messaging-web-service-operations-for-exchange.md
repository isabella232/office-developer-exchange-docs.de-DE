---
title: Unified Messaging Web Service-Vorgänge für Exchange
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
description: Hier finden Sie im Exchange Referenzinformationen für Unified Messaging Web Service-Vorgänge.
ms.openlocfilehash: 21d3469d752ff6cdca4ed4ea9151daca52d51e9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839287"
---
# <a name="unified-messaging-web-service-operations-for-exchange"></a><span data-ttu-id="c1ab0-103">Unified Messaging Web Service-Vorgänge für Exchange</span><span class="sxs-lookup"><span data-stu-id="c1ab0-103">Unified Messaging web service operations for Exchange</span></span>

<span data-ttu-id="c1ab0-104">Hier finden Sie im Exchange Referenzinformationen für Unified Messaging Web Service-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-104">Find reference information for the Unified Messaging web service operations in Exchange.</span></span>
  
<span data-ttu-id="c1ab0-105">Der Unified Messaging-Webdienst bietet viele Vorgänge, mit die Clientanwendungen zum Lesen und Unified Messaging-Eigenschaften ändern, wiedergeben Voice Mail-Nachrichten, Grußformeln aufzeichnen und Postfachelemente über Telefoniegeräte bestimmen können.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-105">The Unified Messaging web service provides many operations that enable client applications to read and change Unified Messaging properties, play voice mail messages, record greetings, and dictate mailbox items over telephony devices.</span></span> <span data-ttu-id="c1ab0-106">Die Artikel in diesem Abschnitt enthalten Informationen über die allgemeine Struktur der Anfrage und-Antwort Nachrichten für die Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-106">The articles in this section provide information about the overall structure of the request and response messages for the operations.</span></span> <span data-ttu-id="c1ab0-107">Diese Artikel enthalten Beispiele, in denen allgemeine Nachricht Strukturen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-107">These articles provide examples that show common message structures.</span></span> <span data-ttu-id="c1ab0-108">In diesen Beispielen können Sie erfahren Sie, was Sie mit einem Unified Messaging-webdienstanforderung möglich.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-108">You can use these examples to learn about what you can do with a Unified Messaging web service request.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="c1ab0-109">Exchange beginnend mit Exchange 2010-Versionen, sollten Sie die Unified Messaging-Vorgänge verwenden, die in der [Exchange-Webdienste (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) anstelle der Unified Messaging-Webdienst, aus den folgenden Gründen zur Verfügung stehen: > des EWS-basierte Unified Messaging-Funktionen haben erstklassige Unterstützung in die EWS Managed API.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-109">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the Unified Messaging web service, for the following reasons: >  The EWS-based Unified Messaging features have first-class support in the EWS Managed API.</span></span> <span data-ttu-id="c1ab0-110">> In Exchange beginnend mit Exchange 2010-Versionen werden neue Unified Messaging-Features für EWS jedoch nicht für den Unified Messaging-Webdienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-110">>  In versions of Exchange starting with Exchange 2010, new Unified Messaging features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="c1ab0-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="c1ab0-111">In this section</span></span>
<span data-ttu-id="c1ab0-112"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="c1ab0-112"></span></span>

- [<span data-ttu-id="c1ab0-113">Trennen Sie (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-113">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-114">GetCallInfo-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-114">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-115">GetUMProperties-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-115">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-116">IsUMEnabled-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-116">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-117">PlayOnPhone-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-117">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-118">PlayOnPhoneGreeting-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-118">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-119">ResetPIN-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-119">ResetPIN operation (UM web service)</span></span>](resetpin-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-120">SetMissedCallNotificationEnabled-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-120">SetMissedCallNotificationEnabled operation (UM web service)</span></span>](setmissedcallnotificationenabled-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-121">SetOofStatus-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-121">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-122">SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-122">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)
    
- [<span data-ttu-id="c1ab0-123">SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="c1ab0-123">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
    
## <a name="see-also"></a><span data-ttu-id="c1ab0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1ab0-124">See also</span></span>

- [<span data-ttu-id="c1ab0-125">Unified Messaging-webdienstreferenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="c1ab0-125">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
- [<span data-ttu-id="c1ab0-126">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="c1ab0-126">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="c1ab0-127">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1ab0-127">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

