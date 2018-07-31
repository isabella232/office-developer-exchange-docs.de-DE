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
ms.openlocfilehash: bd86a4ab2de58e5f04a8d37f17196040bcf38b97
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354358"
---
# <a name="unified-messaging-web-service-operations-for-exchange"></a><span data-ttu-id="16c7f-103">Unified Messaging Web Service-Vorgänge für Exchange</span><span class="sxs-lookup"><span data-stu-id="16c7f-103">Unified Messaging web service operations for Exchange</span></span>

<span data-ttu-id="16c7f-104">Hier finden Sie im Exchange Referenzinformationen für Unified Messaging Web Service-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="16c7f-104">Find reference information for the Unified Messaging web service operations in Exchange.</span></span>
  
<span data-ttu-id="16c7f-105">Der Unified Messaging-Webdienst bietet viele Vorgänge, mit die Clientanwendungen zum Lesen und Unified Messaging-Eigenschaften ändern, wiedergeben Voice Mail-Nachrichten, Grußformeln aufzeichnen und Postfachelemente über Telefoniegeräte bestimmen können.</span><span class="sxs-lookup"><span data-stu-id="16c7f-105">The Unified Messaging web service provides many operations that enable client applications to read and change Unified Messaging properties, play voice mail messages, record greetings, and dictate mailbox items over telephony devices.</span></span> <span data-ttu-id="16c7f-106">Die Artikel in diesem Abschnitt enthalten Informationen über die allgemeine Struktur der Anfrage und-Antwort Nachrichten für die Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="16c7f-106">The articles in this section provide information about the overall structure of the request and response messages for the operations.</span></span> <span data-ttu-id="16c7f-107">Diese Artikel enthalten Beispiele, in denen allgemeine Nachricht Strukturen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="16c7f-107">These articles provide examples that show common message structures.</span></span> <span data-ttu-id="16c7f-108">In diesen Beispielen können Sie erfahren Sie, was Sie mit einem Unified Messaging-webdienstanforderung möglich.</span><span class="sxs-lookup"><span data-stu-id="16c7f-108">You can use these examples to learn about what you can do with a Unified Messaging web service request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="16c7f-109">Exchange beginnend mit Exchange 2010-Versionen wird empfohlen, dass Sie die Unified Messaging-Vorgänge verwenden, die in der [Exchange-Webdienste (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) anstelle der Unified Messaging-Webdienst, aus den folgenden Gründen verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="16c7f-109">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the Unified Messaging web service, for the following reasons:</span></span> 
> - <span data-ttu-id="16c7f-110">EWS-basierte Unified Messaging-Funktionen haben erstklassige Unterstützung in die EWS Managed API.</span><span class="sxs-lookup"><span data-stu-id="16c7f-110">The EWS-based Unified Messaging features have first-class support in the EWS Managed API.</span></span> 
> - <span data-ttu-id="16c7f-111">In Versionen von Exchange, beginnend mit Exchange 2010 werden neue Unified Messaging-Features für EWS jedoch nicht für den Unified Messaging-Webdienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="16c7f-111">In versions of Exchange starting with Exchange 2010, new Unified Messaging features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="16c7f-112">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="16c7f-112">In this section</span></span>
<span data-ttu-id="16c7f-113"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="16c7f-113"></span></span>

- [<span data-ttu-id="16c7f-114">Disconnect-Vorgange (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-114">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)    
- [<span data-ttu-id="16c7f-115">GetCallInfo-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-115">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)   
- [<span data-ttu-id="16c7f-116">GetUMProperties-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-116">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)   
- [<span data-ttu-id="16c7f-117">IsUMEnabled-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-117">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)   
- [<span data-ttu-id="16c7f-118">PlayOnPhone-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-118">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)   
- [<span data-ttu-id="16c7f-119">PlayOnPhoneGreeting-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-119">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)   
- [<span data-ttu-id="16c7f-120">ResetPIN-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-120">ResetPIN operation (UM web service)</span></span>](resetpin-operation-um-web-service.md)   
- [<span data-ttu-id="16c7f-121">SetMissedCallNotificationEnabled-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-121">SetMissedCallNotificationEnabled operation (UM web service)</span></span>](setmissedcallnotificationenabled-operation-um-web-service.md)  
- [<span data-ttu-id="16c7f-122">SetOofStatus-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-122">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)    
- [<span data-ttu-id="16c7f-123">SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-123">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)   
- [<span data-ttu-id="16c7f-124">SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="16c7f-124">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
    
## <a name="see-also"></a><span data-ttu-id="16c7f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16c7f-125">See also</span></span>

- [<span data-ttu-id="16c7f-126">Unified Messaging-webdienstreferenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="16c7f-126">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
- [<span data-ttu-id="16c7f-127">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="16c7f-127">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="16c7f-128">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="16c7f-128">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

