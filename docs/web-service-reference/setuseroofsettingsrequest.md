---
title: SetUserOofSettingsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettingsRequest
api_type:
- schema
ms.assetid: 628acf0b-3ebc-42f1-8ce2-7a02b4c8141f
description: Das SetUserOofSettingsRequest-Element enthält die Argumente verwendet, um ein Postfach des Benutzers Out of Office (OOF) Einstellungen festzulegen.
ms.openlocfilehash: ed54bb1d066da7b15605fb81931a6ef75dfc61bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831474"
---
# <a name="setuseroofsettingsrequest"></a><span data-ttu-id="7b776-103">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="7b776-103">SetUserOofSettingsRequest</span></span>

<span data-ttu-id="7b776-104">Das **SetUserOofSettingsRequest** -Element enthält die Argumente verwendet, um ein Postfach des Benutzers Out of Office (OOF) Einstellungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7b776-104">The **SetUserOofSettingsRequest** element contains the arguments used to set a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<SetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
   <UserOofSettings>...</UserOofSettings>
<SetUserOofSettingsRequest>
```

 <span data-ttu-id="7b776-105">**SetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="7b776-105">**SetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b776-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7b776-106">Attributes and elements</span></span>

<span data-ttu-id="7b776-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7b776-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b776-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7b776-108">Attributes</span></span>

<span data-ttu-id="7b776-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7b776-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b776-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b776-110">Child elements</span></span>

|<span data-ttu-id="7b776-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b776-111">**Element**</span></span>|<span data-ttu-id="7b776-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b776-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b776-113">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="7b776-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="7b776-114">Identifiziert den Postfachbenutzer für eine Anforderung SetUserOofSettings oder GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="7b776-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
|[<span data-ttu-id="7b776-115">' UserOofSettings '</span><span class="sxs-lookup"><span data-stu-id="7b776-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="7b776-116">Gibt die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7b776-116">Specifies the OOF settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b776-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b776-117">Parent elements</span></span>

<span data-ttu-id="7b776-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="7b776-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b776-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7b776-119">Remarks</span></span>

<span data-ttu-id="7b776-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7b776-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="7b776-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b776-121">Example</span></span>

<span data-ttu-id="7b776-122">Im folgenden Beispiel wird eine Anforderung SetUserOofSettings legt eine OOF-Einstellung für zehn Tage fest.</span><span class="sxs-lookup"><span data-stu-id="7b776-122">The following example of a SetUserOofSettings request sets an OOF setting for ten days.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="7b776-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7b776-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b776-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b776-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7b776-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7b776-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7b776-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7b776-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7b776-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7b776-127">Validation File</span></span>  <br/> |<span data-ttu-id="7b776-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7b776-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7b776-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7b776-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="7b776-130">False</span><span class="sxs-lookup"><span data-stu-id="7b776-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b776-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b776-131">See also</span></span>



[<span data-ttu-id="7b776-132">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7b776-132">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

