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
description: Das SendNotification-Element enthält die Push-Benachrichtigungen, die von dem Computer gesendet werden, der Microsoft Exchange Server 2007 an die Clientanwendung ausführt.
ms.openlocfilehash: 49f2f6cb7f5c8e1171b54ff965ee1d22accc9bf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462115"
---
# <a name="sendnotification"></a><span data-ttu-id="d86d6-103">SendNotification</span><span class="sxs-lookup"><span data-stu-id="d86d6-103">SendNotification</span></span>

<span data-ttu-id="d86d6-104">Das **SendNotification** -Element enthält die Push-Benachrichtigungen, die von dem Computer gesendet werden, der Microsoft Exchange Server 2007 an die Clientanwendung ausführt.</span><span class="sxs-lookup"><span data-stu-id="d86d6-104">The **SendNotification** element contains the push notifications that are sent by the computer that is running Microsoft Exchange Server 2007 to the client application.</span></span> 
  
```xml
<SendNotification>
   <ResponseMessages/>
</SendNotification>
```

 <span data-ttu-id="d86d6-105">**SendNotificationResponseType**</span><span class="sxs-lookup"><span data-stu-id="d86d6-105">**SendNotificationResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d86d6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d86d6-106">Attributes and elements</span></span>

<span data-ttu-id="d86d6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d86d6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d86d6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d86d6-108">Attributes</span></span>

<span data-ttu-id="d86d6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d86d6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d86d6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d86d6-110">Child elements</span></span>

|<span data-ttu-id="d86d6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d86d6-111">**Element**</span></span>|<span data-ttu-id="d86d6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d86d6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d86d6-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d86d6-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d86d6-114">Enthält die Push-Benachrichtigungen, die vom Client Zugriffsserver gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d86d6-114">Contains the push notifications that are sent by the Client Access server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d86d6-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d86d6-115">Parent elements</span></span>

<span data-ttu-id="d86d6-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="d86d6-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d86d6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d86d6-117">Remarks</span></span>

<span data-ttu-id="d86d6-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d86d6-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d86d6-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d86d6-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d86d6-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="d86d6-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d86d6-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d86d6-121">Schema Name</span></span>  <br/> |<span data-ttu-id="d86d6-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d86d6-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d86d6-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d86d6-123">Validation File</span></span>  <br/> |<span data-ttu-id="d86d6-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d86d6-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d86d6-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d86d6-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="d86d6-126">False</span><span class="sxs-lookup"><span data-stu-id="d86d6-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d86d6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d86d6-127">See also</span></span>



- [<span data-ttu-id="d86d6-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d86d6-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d86d6-129">Ereignisbenachrichtigungen in EWS</span><span class="sxs-lookup"><span data-stu-id="d86d6-129">Event notifications in EWS</span></span>](https://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)
  
[<span data-ttu-id="d86d6-130">Beispielanwendung für Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d86d6-130">Push Notification Sample Application</span></span>](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

