---
title: Fehler (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: Das Error-Element enthält eine Fehlerantwort AutoErmittlung.
ms.openlocfilehash: 3135a352365fe3000ce2d202ad78452d5c8ccc7f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758260"
---
# <a name="error-pox"></a><span data-ttu-id="ab47c-103">Fehler (POX)</span><span class="sxs-lookup"><span data-stu-id="ab47c-103">Error (POX)</span></span>

<span data-ttu-id="ab47c-104">Das **Error** -Element enthält eine Fehlerantwort AutoErmittlung.</span><span class="sxs-lookup"><span data-stu-id="ab47c-104">The **Error** element contains an Autodiscover error response.</span></span> 
  
[<span data-ttu-id="ab47c-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="ab47c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="ab47c-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="ab47c-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="ab47c-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="ab47c-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="ab47c-108">Fehler (POX)</span><span class="sxs-lookup"><span data-stu-id="ab47c-108">Error (POX)</span></span>](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="ab47c-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ab47c-109">Attributes and elements</span></span>

<span data-ttu-id="ab47c-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ab47c-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab47c-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab47c-111">Attributes</span></span>

|<span data-ttu-id="ab47c-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ab47c-112">**Attribute**</span></span>|<span data-ttu-id="ab47c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab47c-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ab47c-114">Zeit</span><span class="sxs-lookup"><span data-stu-id="ab47c-114">Time</span></span>  <br/> |<span data-ttu-id="ab47c-115">Gibt die Zeit an, wann die Fehlerantwort zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ab47c-115">Represents the time when the error response was returned.</span></span>  <br/> |
|<span data-ttu-id="ab47c-116">Id</span><span class="sxs-lookup"><span data-stu-id="ab47c-116">Id</span></span>  <br/> |<span data-ttu-id="ab47c-117">Stellt einen Hash des Namens des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab47c-117">Represents a hash of the name of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ab47c-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab47c-118">Child elements</span></span>

|<span data-ttu-id="ab47c-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab47c-119">**Element**</span></span>|<span data-ttu-id="ab47c-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab47c-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab47c-121">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="ab47c-121">ErrorCode (POX)</span></span>](errorcode-pox.md) <br/> |<span data-ttu-id="ab47c-122">Enthält den Fehlercode für ein Fehler Antwort der AutoErmittlung an.</span><span class="sxs-lookup"><span data-stu-id="ab47c-122">Contains the error code for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="ab47c-123">Nachricht (POX)</span><span class="sxs-lookup"><span data-stu-id="ab47c-123">Message (POX)</span></span>](message-pox.md) <br/> |<span data-ttu-id="ab47c-124">Enthält die Fehlermeldung Fehler Antwort der AutoErmittlung an.</span><span class="sxs-lookup"><span data-stu-id="ab47c-124">Contains the error message for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="ab47c-125">DebugData (POX)</span><span class="sxs-lookup"><span data-stu-id="ab47c-125">DebugData (POX)</span></span>](debugdata-pox.md) <br/> |<span data-ttu-id="ab47c-126">Enthält die Debugdaten für eine Antwort der AutoErmittlung-Fehler.</span><span class="sxs-lookup"><span data-stu-id="ab47c-126">Contains the debug data for an error Autodiscover response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ab47c-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab47c-127">Parent elements</span></span>

|<span data-ttu-id="ab47c-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab47c-128">**Element**</span></span>|<span data-ttu-id="ab47c-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab47c-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab47c-130">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="ab47c-130">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="ab47c-131">Enthält eine Fehlerantwort AutoErmittlung an.</span><span class="sxs-lookup"><span data-stu-id="ab47c-131">Contains an Autodiscover error response.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab47c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab47c-132">See also</span></span>



[<span data-ttu-id="ab47c-133">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="ab47c-133">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

