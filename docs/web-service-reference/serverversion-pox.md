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
description: Das Server Version vom-Element stellt die Versionsnummer des Computers dar, auf dem Exchange Server läuft.
ms.openlocfilehash: 3ef531a69d2dd00ee9784c9eb191684ce517e842
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461968"
---
# <a name="serverversion-pox"></a><span data-ttu-id="ea447-103">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="ea447-103">ServerVersion (POX)</span></span>

<span data-ttu-id="ea447-104">Das **Server Version vom** -Element stellt die Versionsnummer des Computers dar, auf dem Exchange Server läuft.</span><span class="sxs-lookup"><span data-stu-id="ea447-104">The **ServerVersion** element represents the version number of the computer that is running Microsoft Exchange Server.</span></span> 
  
- [<span data-ttu-id="ea447-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="ea447-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="ea447-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="ea447-106">Response (POX)</span></span>](response-pox.md)
- [<span data-ttu-id="ea447-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="ea447-107">Account (POX)</span></span>](account-pox.md)
- [<span data-ttu-id="ea447-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="ea447-108">Protocol (POX)</span></span>](protocol-pox.md)
- [<span data-ttu-id="ea447-109">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="ea447-109">ServerVersion (POX)</span></span>](serverversion-pox.md)
  
```xml
<ServerVersion/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="ea447-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ea447-110">Attributes and elements</span></span>

<span data-ttu-id="ea447-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ea447-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea447-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="ea447-112">Attributes</span></span>

<span data-ttu-id="ea447-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ea447-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ea447-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea447-114">Child elements</span></span>

<span data-ttu-id="ea447-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="ea447-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ea447-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea447-116">Parent elements</span></span>

|<span data-ttu-id="ea447-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ea447-117">**Element**</span></span>|<span data-ttu-id="ea447-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ea447-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea447-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="ea447-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="ea447-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange ausgeführt wird, auf dem die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ea447-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ea447-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="ea447-121">Text value</span></span>

<span data-ttu-id="ea447-122">Der Wert Text stellt die Versionsnummer von Exchange Server dar.</span><span class="sxs-lookup"><span data-stu-id="ea447-122">The text value represents the Exchange server version number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ea447-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea447-123">Remarks</span></span>

<span data-ttu-id="ea447-124">Der **Server Version vom** -Wert ist nur gültig, wenn der [Typ (POX)-](type-pox.md) Element gleich "$" oder "expr" ist.</span><span class="sxs-lookup"><span data-stu-id="ea447-124">The **ServerVersion** value is only valid if the [Type (POX)](type-pox.md) element is equal to EXCH or EXPR.</span></span> <span data-ttu-id="ea447-125">Der **Server Version vom** -Wert ist eine hexadezimale Zahl, die die MajorVersion, MinorVersion und MajorBuildNumber des Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="ea447-125">The **ServerVersion** value is a hexadecimal number that contains the MajorVersion, MinorVersion, and MajorBuildNumber of the server.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ea447-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ea447-126">Example</span></span>

<span data-ttu-id="ea447-127">Im folgenden Beispiel wird ein **Server Version vom** -Wert behandelt, der in einer Auto Ermittlungs Antwort zurückgegeben wird, um die MajorVersion-, MinorVersion-und MajorBuildNumber-Werte zu erhalten und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ea447-127">The following example coverts a **ServerVersion** value that is returned in an Autodiscover response to obtain and display the MajorVersion, MinorVersion, and MajorBuildNumber.</span></span> <span data-ttu-id="ea447-128">In diesem Beispiel können Sie einen Hexadezimalwert für den **Server Version vom** -Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="ea447-128">This example enables you to enter a hexadecimal value for the **ServerVersion** value.</span></span> <span data-ttu-id="ea447-129">Wenn kein **Server Version vom** -Wert eingegeben wird, wird ein standardmäßiger **Server Version vom** -Wert von 738180DA verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea447-129">If no **ServerVersion** value is entered, a default **ServerVersion** value of 738180DA is used.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="ea447-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea447-130">See also</span></span>

- [<span data-ttu-id="ea447-131">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="ea447-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

