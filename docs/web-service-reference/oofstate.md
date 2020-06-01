---
title: OofState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofState
api_type:
- schema
ms.assetid: 3c486a38-06da-4382-ad20-664d067d76ac
description: Das OofState-Element wird verwendet, um den Abwesenheit (Out of Office, OOF) Zustand des Benutzers abzurufen oder festzulegen.
ms.openlocfilehash: 6aef7d989ee6978019a483f2673895e68a88a7c5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459735"
---
# <a name="oofstate"></a><span data-ttu-id="8a672-103">OofState</span><span class="sxs-lookup"><span data-stu-id="8a672-103">OofState</span></span>

<span data-ttu-id="8a672-104">Das **OofState** -Element wird verwendet, um den Abwesenheit (Out of Office, OOF) Zustand des Benutzers abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8a672-104">The **OofState** element is used to get or set the user's Out of Office (OOF) state.</span></span> 
  
```xml
<OofState>Disabled or Enabled or Scheduled</OofState>
```

 <span data-ttu-id="8a672-105">**OofState**</span><span class="sxs-lookup"><span data-stu-id="8a672-105">**OofState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a672-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8a672-106">Attributes and elements</span></span>

<span data-ttu-id="8a672-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8a672-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a672-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8a672-108">Attributes</span></span>

<span data-ttu-id="8a672-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8a672-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a672-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a672-110">Child elements</span></span>

<span data-ttu-id="8a672-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8a672-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a672-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a672-112">Parent elements</span></span>

|<span data-ttu-id="8a672-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a672-113">**Element**</span></span>|<span data-ttu-id="8a672-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a672-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a672-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="8a672-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="8a672-116">Gibt die Abwesenheitseinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="8a672-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="8a672-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="8a672-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="8a672-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="8a672-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="8a672-119">Enthält die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="8a672-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="8a672-120">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="8a672-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8a672-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="8a672-121">Text value</span></span>

<span data-ttu-id="8a672-122">Für das **OofState** -Element ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8a672-122">A text value is required for the **OofState** element.</span></span> <span data-ttu-id="8a672-123">Die folgende Liste enthält die möglichen Werte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="8a672-123">The following list contains the possible values for this element:</span></span> 
  
- <span data-ttu-id="8a672-124">**Disabled**</span><span class="sxs-lookup"><span data-stu-id="8a672-124">**Disabled**</span></span>
    
- <span data-ttu-id="8a672-125">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="8a672-125">**Enabled**</span></span>
    
- <span data-ttu-id="8a672-126">**Geplant**</span><span class="sxs-lookup"><span data-stu-id="8a672-126">**Scheduled**</span></span>
    
<span data-ttu-id="8a672-127">Der Wert **Scheduled** gibt an, dass der Abwesenheitsstatus während eines Zeitraums, der durch das Element [Duration (UserOofSettings)](duration-useroofsettings.md) angegeben ist, auf **aktiviert** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8a672-127">A value of **Scheduled** indicates that the OOF status is set to **Enabled** during a time period identified by the [Duration (UserOofSettings)](duration-useroofsettings.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8a672-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a672-128">Remarks</span></span>

<span data-ttu-id="8a672-129">Dieses Element ist sowohl in der SetUsersOofSettingRequest-Nachricht als auch in der GetUserOofSettingResponse-Nachricht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8a672-129">This element is required in both the SetUsersOofSettingRequest message and the GetUserOofSettingResponse message.</span></span>
  
<span data-ttu-id="8a672-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8a672-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="8a672-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8a672-131">Example</span></span>

<span data-ttu-id="8a672-132">Im folgenden Beispiel einer SetUserOofSettings-Anforderung wird das **OofState**aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a672-132">The following example of a SetUserOofSettings request enables the **OofState**.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="8a672-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8a672-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a672-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a672-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8a672-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8a672-135">Schema Name</span></span>  <br/> |<span data-ttu-id="8a672-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8a672-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="8a672-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8a672-137">Validation File</span></span>  <br/> |<span data-ttu-id="8a672-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8a672-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8a672-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8a672-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="8a672-140">False</span><span class="sxs-lookup"><span data-stu-id="8a672-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a672-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a672-141">See also</span></span>



[<span data-ttu-id="8a672-142">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8a672-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="8a672-143">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8a672-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

