---
title: Vorgänge
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Operations
api_type:
- schema
ms.assetid: d8cd41b1-28ae-4c95-9ff6-8b25c8e18306
description: Das Vorgänge Element enthält ein Array von Regelvorgänge, die für einen Ordner Posteingang ausgeführt werden kann.
ms.openlocfilehash: 1030703d5e496be391d557e99e1420f9fddfdb36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830655"
---
# <a name="operations"></a><span data-ttu-id="7499d-103">Vorgänge</span><span class="sxs-lookup"><span data-stu-id="7499d-103">Operations</span></span>

<span data-ttu-id="7499d-104">Das **Vorgänge** Element enthält ein Array von Regelvorgänge, die für einen Ordner Posteingang ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7499d-104">The **Operations** element contains an array of rule operations that can be performed on an Inbox.</span></span> 
  
[<span data-ttu-id="7499d-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="7499d-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
```XML
<Operations>
    <CreateRuleOperation/>
    <SetRuleOperation/>
    <DeleteRuleOperation/>
</Operations>
```

 <span data-ttu-id="7499d-106">**ArrayOfRuleOperationsType**</span><span class="sxs-lookup"><span data-stu-id="7499d-106">**ArrayOfRuleOperationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7499d-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7499d-107">Attributes and elements</span></span>

<span data-ttu-id="7499d-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7499d-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7499d-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="7499d-109">Attributes</span></span>

<span data-ttu-id="7499d-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="7499d-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7499d-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7499d-111">Child elements</span></span>

|<span data-ttu-id="7499d-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="7499d-112">**Element**</span></span>|<span data-ttu-id="7499d-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7499d-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7499d-114">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="7499d-114">CreateRuleOperation</span></span>](createruleoperation.md) <br/> |<span data-ttu-id="7499d-115">Stellt einen Vorgang zum Erstellen einer neuen Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="7499d-115">Represents an operation to create a new Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="7499d-116">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="7499d-116">SetRuleOperation</span></span>](setruleoperation.md) <br/> |<span data-ttu-id="7499d-117">Stellt einen Vorgang, um eine Posteingangsregel zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7499d-117">Represents an operation to update an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="7499d-118">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="7499d-118">DeleteRuleOperation</span></span>](deleteruleoperation.md) <br/> |<span data-ttu-id="7499d-119">Stellt einen Vorgang, um eine Posteingangsregel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7499d-119">Represents an operation to delete an Inbox rule.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7499d-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7499d-120">Parent elements</span></span>

|<span data-ttu-id="7499d-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="7499d-121">**Element**</span></span>|<span data-ttu-id="7499d-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7499d-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7499d-123">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="7499d-123">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="7499d-124">Definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher.</span><span class="sxs-lookup"><span data-stu-id="7499d-124">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7499d-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7499d-125">Remarks</span></span>

<span data-ttu-id="7499d-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7499d-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7499d-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7499d-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7499d-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="7499d-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7499d-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7499d-129">Schema Name</span></span>  <br/> |<span data-ttu-id="7499d-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7499d-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="7499d-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7499d-131">Validation File</span></span>  <br/> |<span data-ttu-id="7499d-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7499d-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7499d-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7499d-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="7499d-134">False</span><span class="sxs-lookup"><span data-stu-id="7499d-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7499d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7499d-135">See also</span></span>



[<span data-ttu-id="7499d-136">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7499d-136">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="7499d-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7499d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

