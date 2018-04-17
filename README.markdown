SysInfo
===================
PHP library that can be used to fetch system information like CPU usage, load averages and memory usage (amongst other features). The library was made to accomodate a PHPUnit test listener, so the featureset is pretty slim, and only works on Linux.

I forked this from christeredvartsen/sysinfo for my own use after that package was abandoned.
Use at your own risk.

Installation
------------
To use this library you can specify `backstrap/sysinfo` in your [composer.json](http://getcomposer.org) file.

Usage
-----
```php
<?php
$sysInfo = SysInfo\SysInfo::factory(); // automatically choose instance based on PHP_OS

// or

$sysInfo = new SysInfo\Linux();

$cpu = $sysInfo->getCPU(); // Fetch snapshot of CPU info
$load = $sysInfo->getLoad(); // Fetch snapshot of Load info
$uptime = $sysInfo->getUptime(); // Fetch snapshot of Uptime info
$memory = $sysInfo->getMemory(); // Fetch snapshot of Memory info
$disk = $sysInfo->getDisk(); // Fetch snapshot of Disk info
```

See the CPUInterface.php, DiskInterface.php, LoadInterface.php, UptimeInterface.php and MemoryInterface.php interfaces for more docs.
