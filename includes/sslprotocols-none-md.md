<span data-ttu-id="a1f10-101">Начиная с .NET Framework 4.7, этот метод выполняет проверку подлинности с помощью <xref:System.Security.Authentication.SslProtocols.None>, что позволяет операционной системе выбрать наилучший протокол для использования и для блокирования протоколов, не являются безопасными.</span><span class="sxs-lookup"><span data-stu-id="a1f10-101">Starting with .NET Framework 4.7, this method authenticates using <xref:System.Security.Authentication.SslProtocols.None>, which allows the operating system to choose the best protocol to use, and to block protocols that are not secure.</span></span> <span data-ttu-id="a1f10-102">В .NET Framework 4.6 (и .NET Framework 4.5 с установлены последние обновления безопасности) допустимые версии протокола TLS/SSL, 1.0, 1.1 и 1.2 (если не отключить устойчивого шифрования с помощью реестра Windows).</span><span class="sxs-lookup"><span data-stu-id="a1f10-102">In .NET Framework 4.6 (and .NET Framework 4.5 with the latest security patches installed), the allowed TLS/SSL protocols versions are 1.2, 1.1, and 1.0 (unless you disable strong cryptography by editing the Windows Registry).</span></span>