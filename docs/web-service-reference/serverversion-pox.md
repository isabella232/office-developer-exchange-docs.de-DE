---
title: ServerVersion (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a
description: Das ServerVersion Element stellt die Versionsnummer des Computers, auf dem Microsoft Exchange Server ausgeführt wird.
ms.openlocfilehash: ef0562e166094d75d0dd92f5f48bb558e11a2cad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831391"
---
# <a name="serverversion-pox"></a><span data-ttu-id="87135-103">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="87135-103">ServerVersion (POX)</span></span>

<span data-ttu-id="87135-104">Das **ServerVersion** Element stellt die Versionsnummer des Computers, auf dem Microsoft Exchange Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87135-104">The **ServerVersion** element represents the version number of the computer that is running Microsoft Exchange Server.</span></span> 
  
- [<span data-ttu-id="87135-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="87135-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="87135-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="87135-106">Response (POX)</span></span>](response-pox.md)
- [<span data-ttu-id="87135-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="87135-107">Account (POX)</span></span>](account-pox.md)
- [<span data-ttu-id="87135-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="87135-108">Protocol (POX)</span></span>](protocol-pox.md)
- [<span data-ttu-id="87135-109">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="87135-109">ServerVersion (POX)</span></span>](serverversion-pox.md)
  
```xml
<ServerVersion/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="87135-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="87135-110">Attributes and elements</span></span>

<span data-ttu-id="87135-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="87135-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87135-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="87135-112">Attributes</span></span>

<span data-ttu-id="87135-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="87135-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="87135-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87135-114">Child elements</span></span>

<span data-ttu-id="87135-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="87135-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="87135-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87135-116">Parent elements</span></span>

|<span data-ttu-id="87135-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="87135-117">**Element**</span></span>|<span data-ttu-id="87135-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87135-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87135-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="87135-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="87135-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="87135-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="87135-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="87135-121">Text value</span></span>

<span data-ttu-id="87135-122">Der Textwert stellt die Versionsnummer des Exchange-Servers.</span><span class="sxs-lookup"><span data-stu-id="87135-122">The text value represents the Exchange server version number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87135-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87135-123">Remarks</span></span>

<span data-ttu-id="87135-124">Der Wert der **ServerVersion** ist nur gültig, wenn das Element [Typ (POX)](type-pox.md) EXCH oder Ausdruck gleich ist.</span><span class="sxs-lookup"><span data-stu-id="87135-124">The **ServerVersion** value is only valid if the [Type (POX)](type-pox.md) element is equal to EXCH or EXPR.</span></span> <span data-ttu-id="87135-125">Der **ServerVersion** Wert ist eine hexadezimale Zahl, die der Hauptversion, MinorVersion und MajorBuildNumber des Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="87135-125">The **ServerVersion** value is a hexadecimal number that contains the MajorVersion, MinorVersion, and MajorBuildNumber of the server.</span></span> 
  
## <a name="example"></a><span data-ttu-id="87135-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="87135-126">Example</span></span>

<span data-ttu-id="87135-127">Das folgende Beispiel konvertiert ein **ServerVersion** Wert, der in einer Antwort der AutoErmittlung abzurufen und anzuzeigen, die Hauptversion, MinorVersion und MajorBuildNumber zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87135-127">The following example coverts a **ServerVersion** value that is returned in an Autodiscover response to obtain and display the MajorVersion, MinorVersion, and MajorBuildNumber.</span></span> <span data-ttu-id="87135-128">In diesem Beispiel können Sie einen Hexadezimalwert für die **ServerVersion** Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="87135-128">This example enables you to enter a hexadecimal value for the **ServerVersion** value.</span></span> <span data-ttu-id="87135-129">Wenn kein **ServerVersion** Wert eingegeben wird, wird der Standardwert **ServerVersion** 738180DA verwendet.</span><span class="sxs-lookup"><span data-stu-id="87135-129">If no **ServerVersion** value is entered, a default **ServerVersion** value of 738180DA is used.</span></span> 
  
```csharp
static void Main(string[] args)
{
    // Convert a ServerVersion value that is returned from an Autodiscover request.
    // The value is a hex value and can be converted to the MajorVersion, MinorVersion,
    // and MajorBuildNumber.
    Console.WriteLine("Enter ServerVersion returned from the Autodiscover (eg. 738180DA) and Enter.");
    Console.WriteLine("To use the default ServerVersion of 738180DA, just hit Enter.");
    // Get the hexadecimal ServerVersion value.
    string serverversionhex = Console.ReadLine();
    // If nothing is entered, use the default server version of "738180DA"
    if (serverversionhex == "")
    {
        serverversionhex = "738180DA";
    }
    Console.WriteLine("ServerVersion (Hex) = " + serverversionhex);
    string serverversionbinary = Convert.ToString(Convert.ToInt32(serverversionhex, 16), 2);
    // The ServerVersion (binary) should be 32 bits in length. If the 
    // server version in binary is a length of 31 characters, the leading
    // zero has been removed in the conversion process. Put the missing zero back.
    if (serverversionbinary.Length == 31)
    {
        serverversionbinary = String.Concat("0", serverversionbinary);
    }
    Console.WriteLine("ServerVersion (bin) = " + serverversionbinary);
    // The first 4 bits represent a number used for comparison against  
    // older version number structures. You can ignore this.
    // The next 6 bits represent the major version number.
    int majorversion = Convert.ToInt32(serverversionbinary.Substring(4, 6), 2);
    Console.WriteLine("MajorVersion: " + majorversion);
    // The next 6 bits represent the minor version number.
    int minorversion = Convert.ToInt32(serverversionbinary.Substring(10, 6), 2);
    Console.WriteLine("MinorVersion: " + minorversion);
    
    // The next bit represent a flag - you can ignore this.
    // The next 15 bits represent the major build number.
    int majorbuild = Convert.ToInt32(serverversionbinary.Substring(17, 15), 2);
    Console.WriteLine("MajorBuildVersion: " + majorbuild);
    Console.WriteLine("\n\nPress any key to continue");
    Console.ReadKey();
}
```

## <a name="see-also"></a><span data-ttu-id="87135-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87135-130">See also</span></span>

- [<span data-ttu-id="87135-131">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="87135-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

