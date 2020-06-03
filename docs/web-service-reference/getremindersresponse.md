---
title: GetRemindersResponse
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b1c7288-2a98-4142-8961-4d2ebca5c37c
description: Das GetRemindersResponse-Element gibt die Antwort auf eine reerinnerungers-Anforderung an.
ms.openlocfilehash: 4e4d6a662d2b734b8bb93e3dd4b325bf6e46a6fc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458292"
---
# <a name="getremindersresponse"></a><span data-ttu-id="b72f1-103">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="b72f1-103">GetRemindersResponse</span></span>

<span data-ttu-id="b72f1-104">Das **GetRemindersResponse** -Element gibt die Antwort auf eine **reerinnerungers** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="b72f1-104">The **GetRemindersResponse** element specifies the response to a **GetReminders** request.</span></span> 
  
```XML
<GetRemindersResponse>
   <Reminders></Reminders>
</GetRemindersResponse>

```

 <span data-ttu-id="b72f1-105">**GetRemindersResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b72f1-105">**GetRemindersResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b72f1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b72f1-106">Attributes and elements</span></span>

<span data-ttu-id="b72f1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b72f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b72f1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b72f1-108">Attributes</span></span>

<span data-ttu-id="b72f1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b72f1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b72f1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b72f1-110">Child elements</span></span>

[<span data-ttu-id="b72f1-111">Reminders</span><span class="sxs-lookup"><span data-stu-id="b72f1-111">Reminders</span></span>](reminders.md)
  
### <a name="parent-elements"></a><span data-ttu-id="b72f1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b72f1-112">Parent elements</span></span>

[<span data-ttu-id="b72f1-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b72f1-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="b72f1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b72f1-114">Remarks</span></span>

<span data-ttu-id="b72f1-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b72f1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b72f1-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b72f1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b72f1-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b72f1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b72f1-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b72f1-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b72f1-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b72f1-119">Schema Name</span></span>  <br/> |<span data-ttu-id="b72f1-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b72f1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b72f1-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b72f1-121">Validation File</span></span>  <br/> |<span data-ttu-id="b72f1-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b72f1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b72f1-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b72f1-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="b72f1-124">False</span><span class="sxs-lookup"><span data-stu-id="b72f1-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b72f1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b72f1-125">See also</span></span>



[<span data-ttu-id="b72f1-126">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b72f1-126">ResponseMessages</span></span>](responsemessages.md)


- [<span data-ttu-id="b72f1-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b72f1-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

