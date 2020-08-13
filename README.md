# asan_link_error_repro
Address Sanitizer Linkage Error Repro

This repository is purely for bug reporting of Address Sanitizer Linkage error of duplicated new/delete symbols.

Bug report: [MFC application fails to link with Address Sanitizer](https://developercommunity.visualstudio.com/content/problem/1144525/mfc-application-fails-to-link-with-address-sanitiz.html)

To reproduce the bug, set your MFC application to link statically to MFC lib, instead of shared MFC DLLs.

2 workarounds are available

* Set /FORCE:MULTIPLE in your linkage command line.
* Temporarily set your MFC application to link to shared MFC DLLs for testing with ASAN
