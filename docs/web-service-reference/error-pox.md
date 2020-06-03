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
description: Das Error-Element enthält eine AutoErmittlung-Fehlerantwort.
ms.openlocfilehash: 1a1a3e83898674e605921cb75371036a8a561a95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530649"
---
# <a name="error-pox"></a><span data-ttu-id="ec7f9-103">Fehler (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7f9-103">Error (POX)</span></span>

<span data-ttu-id="ec7f9-104">Das **Error** -Element enthält eine AutoErmittlung-Fehlerantwort.</span><span class="sxs-lookup"><span data-stu-id="ec7f9-104">The **Error** element contains an Autodiscover error response.</span></span> 
  
[<span data-ttu-id="ec7f9-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7f9-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="ec7f9-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7f9-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="ec7f9-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7f9-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="ec7f9-108">Fehler (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7f9-108">Error (POX)</span></span>](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="ec7f9-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec7f9-109">Attributes and elements</span></span>

<span data-ttu-id="ec7f9-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec7f9-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec7f9-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec7f9-111">Attributes</span></span>

|<span data-ttu-id="ec7f9-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ec7f9-112">**Attribute**</span></span>|<span data-ttu-id="ec7f9-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec7f9-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec7f9-114">Time</span><span class="sxs-lookup"><span data-stu-id="ec7f9-114">Time</span></span>  <br/> |<span data-ttu-id="ec7f9-115">Stellt die Uhrzeit dar, zu der die Fehlerantwort zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ec7f9-115">Represents the time when the error response was returned.</span></span>  <br/> |
|<span data-ttu-id="ec7f9-116">Id</span><span class="sxs-lookup"><span data-stu-id="ec7f9-116">Id</span></span>  <br/> |<span data-ttu-id="ec7f9-117">Stellt einen Hash des Namens des Computers dar, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ec7f9-117">Represents a hash of the name of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ec7f9-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec7f9-118">Child elements</span></span>

|<span data-ttu-id="ec7f9-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec7f9-119">**Element**</span></span>|<span data-ttu-id="ec7f9-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec7f9-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec7f9-121">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7f9-121">ErrorCode (POX)</span></span>](errorcode-pox.md) <br/> |<span data-ttu-id="ec7f9-122">Enthält den Fehlercode für eine fehlerhafte Auto Ermittlungs Antwort.</span><span class="sxs-lookup"><span data-stu-id="ec7f9-122">Contains the error code for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="ec7f9-123">Nachricht (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7f9-123">Message (POX)</span></span>](message-pox.md) <br/> |<span data-ttu-id="ec7f9-124">Enthält die Fehlermeldung für eine fehlerhafte Auto Ermittlungs Antwort.</span><span class="sxs-lookup"><span data-stu-id="ec7f9-124">Contains the error message for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="ec7f9-125">DebugData (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7f9-125">DebugData (POX)</span></span>](debugdata-pox.md) <br/> |<span data-ttu-id="ec7f9-126">Enthält die Debugdaten für eine fehlerhafte Auto Ermittlungs Antwort.</span><span class="sxs-lookup"><span data-stu-id="ec7f9-126">Contains the debug data for an error Autodiscover response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec7f9-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec7f9-127">Parent elements</span></span>

|<span data-ttu-id="ec7f9-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec7f9-128">**Element**</span></span>|<span data-ttu-id="ec7f9-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec7f9-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec7f9-130">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7f9-130">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="ec7f9-131">Enthält eine AutoErmittlung-Fehlerantwort.</span><span class="sxs-lookup"><span data-stu-id="ec7f9-131">Contains an Autodiscover error response.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec7f9-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec7f9-132">See also</span></span>



[<span data-ttu-id="ec7f9-133">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="ec7f9-133">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

