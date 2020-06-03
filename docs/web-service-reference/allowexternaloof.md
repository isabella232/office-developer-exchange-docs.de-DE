---
title: AllowExternalOof
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowExternalOof
api_type:
- schema
ms.assetid: e5387172-5b92-4bb1-8394-180e9c7ff771
description: Das AllowExternalOof-Element enthält einen Wert, der angibt, an wen externe Abwesenheit (Out of Office, OOF) Nachrichten gesendet werden.
ms.openlocfilehash: e4934bc4bc86e1f9f764279a13ecaeca073d9e5d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464812"
---
# <a name="allowexternaloof"></a><span data-ttu-id="a7fe5-103">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="a7fe5-103">AllowExternalOof</span></span>

<span data-ttu-id="a7fe5-104">Das **AllowExternalOof** -Element enthält einen Wert, der angibt, an wen externe Abwesenheit (Out of Office, OOF) Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-104">The **AllowExternalOof** element contains a value that identifies to whom external Out of Office (OOF) messages are sent.</span></span> 
  
- [<span data-ttu-id="a7fe5-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="a7fe5-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
- [<span data-ttu-id="a7fe5-106">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="a7fe5-106">AllowExternalOof</span></span>](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 <span data-ttu-id="a7fe5-107">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="a7fe5-107">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7fe5-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a7fe5-108">Attributes and elements</span></span>

<span data-ttu-id="a7fe5-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7fe5-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="a7fe5-110">Attributes</span></span>

<span data-ttu-id="a7fe5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7fe5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7fe5-112">Child elements</span></span>

<span data-ttu-id="a7fe5-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a7fe5-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7fe5-114">Parent elements</span></span>

|<span data-ttu-id="a7fe5-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7fe5-115">**Element**</span></span>|<span data-ttu-id="a7fe5-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7fe5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7fe5-117">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="a7fe5-117">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="a7fe5-118">Enthält die Antwortergebnisse und die Abwesenheitseinstellungen für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-118">Contains the response results and the OOF settings for a user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a7fe5-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="a7fe5-119">Text value</span></span>

<span data-ttu-id="a7fe5-120">Für dieses Element ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-120">A text value is required for this element.</span></span> <span data-ttu-id="a7fe5-121">In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-121">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="a7fe5-122">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a7fe5-122">**Value**</span></span>|<span data-ttu-id="a7fe5-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7fe5-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7fe5-124">**Keine**</span><span class="sxs-lookup"><span data-stu-id="a7fe5-124">**None**</span></span> <br/> |<span data-ttu-id="a7fe5-125">E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten keine externe Abwesenheitsnachrichten Antwort.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-125">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="a7fe5-126">**Bezeichnet**</span><span class="sxs-lookup"><span data-stu-id="a7fe5-126">**Known**</span></span> <br/> |<span data-ttu-id="a7fe5-127">E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten nur dann eine externe Abwesenheitsnachrichten Antwort, wenn sich der Absender in der Exchange-Informationsspeicher Kontaktliste des Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-127">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="a7fe5-128">**All**</span><span class="sxs-lookup"><span data-stu-id="a7fe5-128">**All**</span></span> <br/> |<span data-ttu-id="a7fe5-129">E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten eine externe Abwesenheitsnachrichten Antwort.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-129">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7fe5-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7fe5-130">Remarks</span></span>

<span data-ttu-id="a7fe5-131">Dieses Element hat denselben Typ wie das [ExternalAudience](externalaudience.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-131">This element shares the same type as the [ExternalAudience](externalaudience.md) element.</span></span> 
  
<span data-ttu-id="a7fe5-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a7fe5-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7fe5-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a7fe5-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7fe5-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7fe5-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a7fe5-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a7fe5-135">Schema Name</span></span>  <br/> |<span data-ttu-id="a7fe5-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a7fe5-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a7fe5-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a7fe5-137">Validation File</span></span>  <br/> |<span data-ttu-id="a7fe5-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a7fe5-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a7fe5-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a7fe5-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="a7fe5-140">False</span><span class="sxs-lookup"><span data-stu-id="a7fe5-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7fe5-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7fe5-141">See also</span></span>

- [<span data-ttu-id="a7fe5-142">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a7fe5-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md) 
- [<span data-ttu-id="a7fe5-143">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a7fe5-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

