[![SWUbanner](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/banner2-direct.svg)](https://github.com/vshymanskyy/StandWithUkraine/blob/main/docs/README.md)

# GuerrillaNtp #

[![Nuget](https://img.shields.io/nuget/v/GuerrillaNtp)](https://www.nuget.org/packages/GuerrillaNtp/)

GuerrillaNtp is a simple NTP (SNTP) client written in C# that can be embedded in desktop .NET applications
to provide them with accurate network time even when the system clock is unsynchronized.

* Documentation: [Tutorial](https://guerrillantp.machinezoo.com/)
* Download: see [Tutorial](https://guerrillantp.machinezoo.com/)
* Sources: [GitHub](https://github.com/robertvazan/guerrillantp), [Bitbucket](https://bitbucket.org/robertvazan/guerrillantp)
* Issues: [GitHub](https://github.com/robertvazan/guerrillantp/issues), [Bitbucket](https://bitbucket.org/robertvazan/guerrillantp/issues)
* License: [Apache License 2.0](LICENSE)

```csharp
// query the SNTP server
TimeSpan offset;
using (var ntp = new NtpClient(Dns.GetHostAddresses("pool.ntp.org")[0]))
    offset = ntp.GetCorrectionOffset();

// use the offset throughout your app
var accurateTime = DateTime.UtcNow + offset;
```

