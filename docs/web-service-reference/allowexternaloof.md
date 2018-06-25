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
description: Das AllowExternalOof-Element enthält einen Wert, der angibt, den externe Out of Office (OOF) Testnachrichten gesendet werden.
ms.openlocfilehash: 1c87a51676bf6e44b2e650a4e973d0ab89a52e31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757258"
---
# <a name="allowexternaloof"></a><span data-ttu-id="193de-103">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="193de-103">AllowExternalOof</span></span>

<span data-ttu-id="193de-104">Das **AllowExternalOof** -Element enthält einen Wert, der angibt, den externe Out of Office (OOF) Testnachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="193de-104">The **AllowExternalOof** element contains a value that identifies to whom external Out of Office (OOF) messages are sent.</span></span> 
  
- [<span data-ttu-id="193de-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="193de-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
- [<span data-ttu-id="193de-106">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="193de-106">AllowExternalOof</span></span>](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 <span data-ttu-id="193de-107">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="193de-107">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="193de-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="193de-108">Attributes and elements</span></span>

<span data-ttu-id="193de-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="193de-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="193de-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="193de-110">Attributes</span></span>

<span data-ttu-id="193de-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="193de-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="193de-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="193de-112">Child elements</span></span>

<span data-ttu-id="193de-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="193de-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="193de-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="193de-114">Parent elements</span></span>

|<span data-ttu-id="193de-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="193de-115">**Element**</span></span>|<span data-ttu-id="193de-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="193de-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="193de-117">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="193de-117">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="193de-118">Enthält die Antwort Ergebnisse und OOF-Einstellungen für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="193de-118">Contains the response results and the OOF settings for a user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="193de-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="193de-119">Text value</span></span>

<span data-ttu-id="193de-120">Es wird ein Textwert für dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="193de-120">A text value is required for this element.</span></span> <span data-ttu-id="193de-121">Die folgende Tabelle enthält die möglichen Werte für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="193de-121">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="193de-122">**Wert**</span><span class="sxs-lookup"><span data-stu-id="193de-122">**Value**</span></span>|<span data-ttu-id="193de-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="193de-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="193de-124">**None**</span><span class="sxs-lookup"><span data-stu-id="193de-124">**None**</span></span> <br/> |<span data-ttu-id="193de-125">E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an die Benutzer werden keine externe OOF Nachricht beantwortet.</span><span class="sxs-lookup"><span data-stu-id="193de-125">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="193de-126">**Bekannte**</span><span class="sxs-lookup"><span data-stu-id="193de-126">**Known**</span></span> <br/> |<span data-ttu-id="193de-127">E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an den Benutzer nur eine externe OOF Nachrichtenantwort erhält, wenn der Absender in Exchange des Benutzers ist speichern Kontaktliste.</span><span class="sxs-lookup"><span data-stu-id="193de-127">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="193de-128">**All**</span><span class="sxs-lookup"><span data-stu-id="193de-128">**All**</span></span> <br/> |<span data-ttu-id="193de-129">E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an die Benutzer erhalten eine externe OOF Nachrichtenantwort.</span><span class="sxs-lookup"><span data-stu-id="193de-129">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="193de-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="193de-130">Remarks</span></span>

<span data-ttu-id="193de-131">Dieses Element gibt den gleichen Datentyp wie das [ExternalAudience](externalaudience.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="193de-131">This element shares the same type as the [ExternalAudience](externalaudience.md) element.</span></span> 
  
<span data-ttu-id="193de-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="193de-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="193de-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="193de-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="193de-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="193de-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="193de-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="193de-135">Schema Name</span></span>  <br/> |<span data-ttu-id="193de-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="193de-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="193de-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="193de-137">Validation File</span></span>  <br/> |<span data-ttu-id="193de-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="193de-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="193de-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="193de-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="193de-140">False</span><span class="sxs-lookup"><span data-stu-id="193de-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="193de-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="193de-141">See also</span></span>

- [<span data-ttu-id="193de-142">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="193de-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md) 
- [<span data-ttu-id="193de-143">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="193de-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

