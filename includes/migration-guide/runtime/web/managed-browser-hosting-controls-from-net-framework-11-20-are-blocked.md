### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a><span data-ttu-id="6c855-101">Заблокированы управляемого браузера размещения элементов управления .NET Framework 1.1 и 2.0</span><span class="sxs-lookup"><span data-stu-id="6c855-101">Managed browser hosting controls from the .NET Framework 1.1 and 2.0 are blocked</span></span>

|   |   |
|---|---|
|<span data-ttu-id="6c855-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="6c855-102">Details</span></span>|<span data-ttu-id="6c855-103">Размещение этих элементов управления в Internet Explorer блокируется.</span><span class="sxs-lookup"><span data-stu-id="6c855-103">Hosting these controls is blocked in Internet Explorer.</span></span>|
|<span data-ttu-id="6c855-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="6c855-104">Suggestion</span></span>|<span data-ttu-id="6c855-105">Internet Explorer не сможет запустить приложение, в котором используются управляемые элементы управления, размещенные в браузере.</span><span class="sxs-lookup"><span data-stu-id="6c855-105">Internet Explorer will fail to launch an application that uses managed browser hosting controls.</span></span> <span data-ttu-id="6c855-106">Можно восстановить прежнее поведение, параметру enableiehosting подраздела реестра <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> для <code>1</code> для x86 систем и для 32-разрядных процессов в x64 систем и задав <code>EnableIEHosting</code> значение раздела реестра, <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>для <code>1</code> для 64-разрядных процессов в x64 систем.</span><span class="sxs-lookup"><span data-stu-id="6c855-106">The previous behavior can be restored by setting the EnableIEHosting value of the registry subkey <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> to <code>1</code> for x86 systems and for 32-bit processes on x64 systems, and by setting the <code>EnableIEHosting</code> value of the registry subkey <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code> to <code>1</code> for 64-bit processes on x64 systems.</span></span>|
|<span data-ttu-id="6c855-107">Область</span><span class="sxs-lookup"><span data-stu-id="6c855-107">Scope</span></span>|<span data-ttu-id="6c855-108">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="6c855-108">Minor</span></span>|
|<span data-ttu-id="6c855-109">Версия</span><span class="sxs-lookup"><span data-stu-id="6c855-109">Version</span></span>|<span data-ttu-id="6c855-110">4.5</span><span class="sxs-lookup"><span data-stu-id="6c855-110">4.5</span></span>|
|<span data-ttu-id="6c855-111">Тип</span><span class="sxs-lookup"><span data-stu-id="6c855-111">Type</span></span>|<span data-ttu-id="6c855-112">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="6c855-112">Runtime</span></span>|
