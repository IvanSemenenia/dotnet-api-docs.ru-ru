### <a name="il-ret-not-allowed-in-a-try-region"></a><span data-ttu-id="5df46-101">Возвращаемое значение IL не допускается в области try</span><span class="sxs-lookup"><span data-stu-id="5df46-101">IL ret not allowed in a try region</span></span>

|   |   |
|---|---|
|<span data-ttu-id="5df46-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="5df46-102">Details</span></span>|<span data-ttu-id="5df46-103">В отличие от компилятора JIT64 компилятор just-in-time RyuJIT (используется в .NET 4.6) не разрешает инструкцию IL ret инструкции в области try.</span><span class="sxs-lookup"><span data-stu-id="5df46-103">Unlike the JIT64 just-in-time compiler, RyuJIT (used in .NET 4.6) does not allow an IL ret instruction in a try region.</span></span> <span data-ttu-id="5df46-104">Возврат из региона try запрещен в спецификации ECMA-335, и ни один известный управляемый компилятор создает такие IL.</span><span class="sxs-lookup"><span data-stu-id="5df46-104">Returning from a try region is disallowed by the ECMA-335 specification, and no known managed compiler generates such IL.</span></span> <span data-ttu-id="5df46-105">Однако компилятор JIT64 выполнит такие IL, если они созданы с помощью порождения отражения.</span><span class="sxs-lookup"><span data-stu-id="5df46-105">However, the JIT64 compiler will execute such IL if it is generated using reflection emit.</span></span>|
|<span data-ttu-id="5df46-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="5df46-106">Suggestion</span></span>|<span data-ttu-id="5df46-107">Если приложение создает IL, который включает в себя ret opcode в области try, приложение предназначено для платформы .NET 4.5, использование старого JIT и избежать этот разрыв.</span><span class="sxs-lookup"><span data-stu-id="5df46-107">If an app is generating IL that includes a ret opcode in a try region, the app may target .NET 4.5 to use the old JIT and avoid this break.</span></span> <span data-ttu-id="5df46-108">Кроме того создаваемый IL-код может быть обновлено до возврата после области try.</span><span class="sxs-lookup"><span data-stu-id="5df46-108">Alternatively, the generated IL may be updated to return after the try region.</span></span>|
|<span data-ttu-id="5df46-109">Область</span><span class="sxs-lookup"><span data-stu-id="5df46-109">Scope</span></span>|<span data-ttu-id="5df46-110">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="5df46-110">Edge</span></span>|
|<span data-ttu-id="5df46-111">Версия</span><span class="sxs-lookup"><span data-stu-id="5df46-111">Version</span></span>|<span data-ttu-id="5df46-112">4.6</span><span class="sxs-lookup"><span data-stu-id="5df46-112">4.6</span></span>|
|<span data-ttu-id="5df46-113">Тип</span><span class="sxs-lookup"><span data-stu-id="5df46-113">Type</span></span>|<span data-ttu-id="5df46-114">Изменение целевой платформы</span><span class="sxs-lookup"><span data-stu-id="5df46-114">Retargeting</span></span>|
