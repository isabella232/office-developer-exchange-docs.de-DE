---
title: Agent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 3895095ed4e469cdb9fec489ba6b6e228779a9c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757170"
---
# <a name="agent"></a><span data-ttu-id="c0e4b-103">Agent</span><span class="sxs-lookup"><span data-stu-id="c0e4b-103">agent</span></span>
  
<span data-ttu-id="c0e4b-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0e4b-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="c0e4b-105">Das **Agent** -Element enthält Konfigurationsinformationen zu installierten Agenten.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-105">The **agent** element contains configuration information about an installed agent.</span></span> 
  
- [<span data-ttu-id="c0e4b-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c0e4b-106">configuration</span></span>](configuration.md) 
- [<span data-ttu-id="c0e4b-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="c0e4b-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="c0e4b-108">agentList</span><span class="sxs-lookup"><span data-stu-id="c0e4b-108">agentList</span></span>](agentlist.md)
- [<span data-ttu-id="c0e4b-109">Agent</span><span class="sxs-lookup"><span data-stu-id="c0e4b-109">agent</span></span>](agent.md)
  
```XML
<agent
        name=""
        baseType=""
        classFactory=""
        assemblyPath=""
        enabled="" />
</agent>
```

<span data-ttu-id="c0e4b-110">**AgentType (ComplexType)**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-110">**agentType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c0e4b-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c0e4b-111">Attributes and elements</span></span>

<span data-ttu-id="c0e4b-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0e4b-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0e4b-113">Attributes</span></span>

|<span data-ttu-id="c0e4b-114">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-114">**Attribute**</span></span>|<span data-ttu-id="c0e4b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0e4b-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-116">**name**</span></span> <br/> |<span data-ttu-id="c0e4b-117">Der Name, der angegeben wurde, wenn der Agent installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-117">The name that was specified when the agent was installed.</span></span> <span data-ttu-id="c0e4b-118">Dieses Attribut erfordert einen nicht leeren Zeichenfolgenwert, der maximal 64 Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-118">This attribute requires a nonempty string value that contains a maximum of 64 characters.</span></span>  <br/> |
|<span data-ttu-id="c0e4b-119">**baseType**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-119">**baseType**</span></span> <br/> |<span data-ttu-id="c0e4b-120">Der vollständige Name, einschließlich des Namespace, der Klasse, von der der Agent abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-120">The full name, including the namespace, of the class from which the agent derives.</span></span> <span data-ttu-id="c0e4b-121">Dieses Attribut erfordert einen nicht leeren Zeichenfolgenwert, der mindestens ein Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-121">This attribute requires a nonempty string value that contains at least one character.</span></span>  <br/> |
|<span data-ttu-id="c0e4b-122">**classFactory**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-122">**classFactory**</span></span> <br/> |<span data-ttu-id="c0e4b-123">Der vollständige Name, einschließlich des Namespace, der Klasse, die die Agentfactory implementiert wird, die Instanzen des Agents erstellt.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-123">The full name, including the namespace, of the class that implements the agent factory that creates instances of the agent.</span></span> <span data-ttu-id="c0e4b-124">Dieses Attribut muss den vollqualifizierten Namen der Klasse enthalten, die die Agentfactory implementiert, die Instanzen des Agents erstellt.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-124">This attribute must contain the fully qualified name of the class that implements the agent factory that creates instances of the agent.</span></span> <span data-ttu-id="c0e4b-125">Diese Klasse muss von der [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) oder [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) -Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-125">This class must derive from either the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) or [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.</span></span>  <br/> |
|<span data-ttu-id="c0e4b-126">**assemblyPath**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-126">**assemblyPath**</span></span> <br/> |<span data-ttu-id="c0e4b-127">Der vollständig qualifizierte Pfad, einschließlich Dateiname der Assembly, die den Code für den Agent enthält.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-127">The fully qualified path, including the file name, of the assembly that contains the code for the agent.</span></span> <span data-ttu-id="c0e4b-128">Dieses Attribut erfordert einen nicht leeren Zeichenfolgenwert, der mindestens ein Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-128">This attribute requires a nonempty string value that contains at least one character.</span></span>  <br/> |
|<span data-ttu-id="c0e4b-129">**aktiviert**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-129">**enabled**</span></span> <br/> |<span data-ttu-id="c0e4b-130">Ein boolescher Wert, der angibt, ob der Agent aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-130">A Boolean value that indicates whether the agent is enabled.</span></span> <span data-ttu-id="c0e4b-131">Der Wert ist **true** , wenn der Agent aktiviert ist. Andernfalls ist der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-131">The value is **true** if the agent is enabled; otherwise, the value is **false**.</span></span> <span data-ttu-id="c0e4b-132">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-132">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c0e4b-133">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0e4b-133">Child elements</span></span>

<span data-ttu-id="c0e4b-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-134">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c0e4b-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0e4b-135">Parent elements</span></span>

|<span data-ttu-id="c0e4b-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-136">**Element**</span></span>|<span data-ttu-id="c0e4b-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0e4b-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0e4b-138">agentList</span><span class="sxs-lookup"><span data-stu-id="c0e4b-138">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="c0e4b-139">Ein **Agent** -Element enthält für jeden installierten Agent.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-139">Contains an **agent** element for each installed agent.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="c0e4b-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c0e4b-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0e4b-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0e4b-141">Namespace</span></span>  <br/> |<span data-ttu-id="c0e4b-142">Diese Datei ist nicht auf einen Namespace definieren.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-142">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="c0e4b-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c0e4b-143">Schema Name</span></span>  <br/> |<span data-ttu-id="c0e4b-144">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-144">Not available.</span></span>  <br/> |
|<span data-ttu-id="c0e4b-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c0e4b-145">Validation File</span></span>  <br/> |<span data-ttu-id="c0e4b-146">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-146">Not available.</span></span>  <br/> |
|<span data-ttu-id="c0e4b-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c0e4b-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0e4b-148">Falsch.</span><span class="sxs-lookup"><span data-stu-id="c0e4b-148">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0e4b-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0e4b-149">See also</span></span>

- [<span data-ttu-id="c0e4b-150">Agents Datei Konfigurationselemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="c0e4b-150">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

