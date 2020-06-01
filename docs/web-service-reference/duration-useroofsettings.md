---
title: Dauer (UserOofSettings)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: Das Duration-Element gibt die Dauer an, für die der Abwesenheitsstatus aktiviert ist, wenn das OofState-Element auf Scheduled festgelegt ist.
ms.openlocfilehash: 0ba0f1ea7498781c0cccb072c7ea0fa05414764c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457298"
---
# <a name="duration-useroofsettings"></a><span data-ttu-id="a35e4-103">Dauer (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="a35e4-103">Duration (UserOofSettings)</span></span>

<span data-ttu-id="a35e4-104">Das **Duration** -Element gibt die Dauer an, für die der Abwesenheitsstatus aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a35e4-104">The **Duration** element specifies the duration that the out of office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>
  
```XML
<Duration>
   <StartTime/>
   <EndTime/> 
</Duration>
```

 <span data-ttu-id="a35e4-105">**Duration**</span><span class="sxs-lookup"><span data-stu-id="a35e4-105">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a35e4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a35e4-106">Attributes and elements</span></span>

<span data-ttu-id="a35e4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a35e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a35e4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a35e4-108">Attributes</span></span>

<span data-ttu-id="a35e4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a35e4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a35e4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a35e4-110">Child elements</span></span>

|<span data-ttu-id="a35e4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a35e4-111">**Element**</span></span>|<span data-ttu-id="a35e4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a35e4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a35e4-113">StartTime</span><span class="sxs-lookup"><span data-stu-id="a35e4-113">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="a35e4-114">Stellt den Anfang der Zeitspanne fest, die mit einem Abwesenheitsstatus festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a35e4-114">Represents the start of the time span set with an OOF status.</span></span> <span data-ttu-id="a35e4-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a35e4-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="a35e4-116">EndTime</span><span class="sxs-lookup"><span data-stu-id="a35e4-116">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="a35e4-117">Stellt das Ende der Zeitspanne fest, die mit einem Abwesenheitsstatus festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a35e4-117">Represents the end of the time span set with an OOF status.</span></span> <span data-ttu-id="a35e4-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a35e4-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a35e4-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a35e4-119">Parent elements</span></span>

|<span data-ttu-id="a35e4-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a35e4-120">**Element**</span></span>|<span data-ttu-id="a35e4-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a35e4-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a35e4-122">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="a35e4-122">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="a35e4-123">Gibt die Abwesenheitseinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="a35e4-123">Specifies the OOF settings.</span></span>  <br/><br/><span data-ttu-id="a35e4-124">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="a35e4-124">The following is the XPath expression to this element:</span></span><br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="a35e4-125">OofSettings</span><span class="sxs-lookup"><span data-stu-id="a35e4-125">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="a35e4-126">Enthält die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="a35e4-126">Contains the OOF settings.</span></span><br/><br/><span data-ttu-id="a35e4-127">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="a35e4-127">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[<span data-ttu-id="a35e4-128">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="a35e4-128">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="a35e4-129">Definiert die Abwesenheit (Out of Office, OOF) Antwortnachricht und eine Dauer für das Senden der Antwortnachricht für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="a35e4-129">Defines the Out of Office (OOF) response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a35e4-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a35e4-130">Remarks</span></span>

<span data-ttu-id="a35e4-131">Der Typ Duration ist auch der Typ für die Elemente [DetailedSuggestionsWindow](detailedsuggestionswindow.md), **Zeit** [Fenster](timewindow.md)und [OutOfOffice](outofoffice.md) .</span><span class="sxs-lookup"><span data-stu-id="a35e4-131">The **Duration** type is also the type for the [DetailedSuggestionsWindow](detailedsuggestionswindow.md), [TimeWindow](timewindow.md), and [OutOfOffice](outofoffice.md) elements.</span></span> 
  
<span data-ttu-id="a35e4-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a35e4-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="a35e4-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a35e4-133">Example</span></span>

<span data-ttu-id="a35e4-134">Im folgenden Beispiel einer [SetUserOofSettings-Vorgangs](setuseroofsettings-operation.md) Anforderung wird die [OofState](oofstate.md) auf **Enabled**, die internen und externen Abwesenheitsnachrichten festgelegt und die Dauer von OOF für 10 Tage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a35e4-134">The following example of a [SetUserOofSettings operation](setuseroofsettings-operation.md) request sets the [OofState](oofstate.md) to **Enabled**, the internal and external OOF messages, and sets the duration of OOF for 10 days.</span></span>
  
```XML
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
        <SetByLegacyClient>false</SetByLegacyClient>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="a35e4-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a35e4-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a35e4-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="a35e4-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a35e4-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a35e4-137">Schema Name</span></span>  <br/> |<span data-ttu-id="a35e4-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a35e4-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="a35e4-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a35e4-139">Validation File</span></span>  <br/> |<span data-ttu-id="a35e4-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a35e4-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a35e4-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a35e4-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="a35e4-142">False</span><span class="sxs-lookup"><span data-stu-id="a35e4-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a35e4-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a35e4-143">See also</span></span>

- [<span data-ttu-id="a35e4-144">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a35e4-144">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)  
- [<span data-ttu-id="a35e4-145">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a35e4-145">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

