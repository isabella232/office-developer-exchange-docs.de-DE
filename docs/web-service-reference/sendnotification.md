---
title: SendNotification
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendNotification
api_type:
- schema
ms.assetid: e45c4451-a286-4aec-a691-119ec41c58e0
description: Das SendNotification-Element enthält, die vom Computer gesendet werden, die Microsoft Exchange Server 2007, an die Clientanwendung ausgeführt wird Pushbenachrichtigungen.
ms.openlocfilehash: 2288dbb5cf97b57a64b3c645eb72836342f4c178
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831345"
---
# <a name="sendnotification"></a><span data-ttu-id="22bab-103">SendNotification</span><span class="sxs-lookup"><span data-stu-id="22bab-103">SendNotification</span></span>

<span data-ttu-id="22bab-104">Das **SendNotification** -Element enthält, die vom Computer gesendet werden, die Microsoft Exchange Server 2007, an die Clientanwendung ausgeführt wird Pushbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="22bab-104">The **SendNotification** element contains the push notifications that are sent by the computer that is running Microsoft Exchange Server 2007 to the client application.</span></span> 
  
```xml
<SendNotification>
   <ResponseMessages/>
</SendNotification>
```

 <span data-ttu-id="22bab-105">**SendNotificationResponseType**</span><span class="sxs-lookup"><span data-stu-id="22bab-105">**SendNotificationResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22bab-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="22bab-106">Attributes and elements</span></span>

<span data-ttu-id="22bab-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="22bab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22bab-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="22bab-108">Attributes</span></span>

<span data-ttu-id="22bab-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="22bab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22bab-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22bab-110">Child elements</span></span>

|<span data-ttu-id="22bab-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="22bab-111">**Element**</span></span>|<span data-ttu-id="22bab-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22bab-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22bab-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="22bab-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="22bab-114">Enthält die Pushbenachrichtigungen, die vom Client Access-Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="22bab-114">Contains the push notifications that are sent by the Client Access server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="22bab-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22bab-115">Parent elements</span></span>

<span data-ttu-id="22bab-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="22bab-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="22bab-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22bab-117">Remarks</span></span>

<span data-ttu-id="22bab-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="22bab-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22bab-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="22bab-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22bab-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="22bab-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="22bab-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="22bab-121">Schema Name</span></span>  <br/> |<span data-ttu-id="22bab-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="22bab-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="22bab-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="22bab-123">Validation File</span></span>  <br/> |<span data-ttu-id="22bab-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="22bab-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="22bab-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="22bab-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="22bab-126">False</span><span class="sxs-lookup"><span data-stu-id="22bab-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22bab-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22bab-127">See also</span></span>



- [<span data-ttu-id="22bab-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="22bab-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="22bab-129">Ereignisbenachrichtigungen in Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="22bab-129">Event notifications in EWS</span></span>](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)
  
[<span data-ttu-id="22bab-130">Beispielanwendung für Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="22bab-130">Push Notification Sample Application</span></span>](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

